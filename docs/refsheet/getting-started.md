# Getting Started

First, ensure you have Java 8 JDK and Eclipse/IntelliJ IDEA/some editor of your choice installed on your computer.
You can check your java version by running `java -version` from the command line.
## Creating A Project
### With Eclipse
1. Go to `New > Other > Gradle` and enter a name
1. Click `Finish`
### With IntelliJ IDEA
1. Click `Create New Project` and select `Gradle`, then click `Next`
1. Enter "myfirstproject” in `artifactId`, then click `Next`
1. Check `Use auto-import`
1. Enter a project name and select a directory (It’s a good idea to create a new directory somewhere for robotics projects)
1. Click `Finish`
## Setting Up Gradle
1. Delete everything in your build.gradle file and copy-paste [this](https://gist.github.com/edelmanjm/98966909693829824d7e61a16f359841) in
1. Create source folders (expand)
1. In the `java` folder, create a package called `org.team1540.<yourname>firstrobot`
1. Create a Java class called `Robot` and replace its contents with the contents of [this file](https://gist.github.com/RobinsonZ/aca9e658a018af68dbea4c8fb205d214). Correct the package header at the top to whatever your package is called.
On line 9 of your `build.gradle`, change `org.team1540.sample` to your package name
1. Start writing simple tank drive code for a robot (talk to a manager)
1. Feel free to write all your code in `Robot.java`
## Deploying Your Code
1. Connect to to the robot network (1540_something, ask a manager for the correct one)
1. press ++command+shift+a++ (++ctrl+shift+a++ on Windows)
1. Type `Execute Gradle Task` (it should come up after the first few letters) and press ++enter++
1. Type `deploy` and press ++enter++ again