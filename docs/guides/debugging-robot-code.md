# Using IntelliJ IDEA's Debugger with Robot Code
## Configuring GradleRIO
1. Make sure to be using GradleRIO version 2018.01.06 or later
1. In your `build.gradle`, just below where it says `targets << "roborio"`, write “`debug = true`” like so:
    ```Groovy hl_lines="10"
    deploy {
        targets {
            target("roborio", jaci.openrio.gradle.frc.RoboRIO) {
                team = TEAM
            }
        }
        artifacts {
            artifact('frcJava', jaci.openrio.gradle.frc.FRCJavaArtifact) {
                targets << "roborio"
                debug = true
            }
        }
    }
    ```
1. Deploy your code normally. The driver station will say “no robot code.” This is normal.

!!! danger 
    With `debug = true` in your `build.gradle` file, the robot code will not start until you connect a debugger. With this in mind, **never** deploy for a match while configured for debugging.
  
## Configuring IntelliJ
1. Open the dropdown in the top right and select `Edit Run/Debug Configurations`
1. Click the `+` sign and select `Remote` from the list
1. Name it “Remote Robot Debug” or something, it doesn’t matter
1. Set host to your RoboRIO's IP (usually `roborio-<YOUR-TEAM>-frc.local`) and port to `8348`
1. In the `Search sources using module’s classpath` dropdown select “<your project name>_main”
1. Click `OK`
1. Select your debug configuration from the top right dropdown and click the bug right next to it (or press ++ctrl+d++).
