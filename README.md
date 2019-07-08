# BB Solutions Hub


# Setup

### Tools
* JDK 1.8 latest version
* IntelliJ latest version (2017.1 or newer)
* git

After installing the required tools, clone or download a zip of this repository, and place it in your desired
location.

### IntelliJ setup
* From the main menu, click `open` (not `import`!) then navigate to where you placed this repository.
* Click `File->Project Structure`, and set the `Project SDK` to be the JDK you downloaded (by clicking `new` and
nagivating to where the JDK was installed). Click `Okay`.
* Next, click `import` on the `Import Gradle Project` popup, leaving all options as they are.
* If you do not see the popup: Navigate back to `Project Structure->Modules`, clicking the `+ -> Import` button,
navigate to and select the repository folder, select `Gradle` from the next menu, and finally click `Okay`,
again leaving all options as they are.

## Build Project cmd / bash / using gradle
```bash
cd /Users/reza/projects/corda-iou-app
./gradlew deployNodes

```
## Running each Node
```bash
# Open different terminal to run the code

# Notary
cd /Users/reza/projects/corda-iou-app/kotlin-source/build/nodes/Notary
java -jar corda.jar

# Node A
cd /Users/reza/projects/corda-iou-app/kotlin-source/build/nodes/ParticipantA
java -jar corda.jar

# Node B
cd /Users/reza/projects/corda-iou-app/kotlin-source/build/nodes/ParticipantB
java -jar corda.jar

# Node C
cd /Users/reza/projects/corda-iou-app/kotlin-source/build/nodes/ParticipantC
java -jar corda.jar

```


## Starting Web Servers

```bash

# Node A
cd /Users/reza/projects/corda-iou-app/kotlin-source/build/nodes/ParticipantA
java -Dname=ParticipantA -jar corda-webserver.jar

# Node B
cd /Users/reza/projects/corda-iou-app/kotlin-source/build/nodes/ParticipantB
java -Dname=ParticipantB -jar corda-webserver.jar

# Node C
cd /Users/reza/projects/corda-iou-app/kotlin-source/build/nodes/ParticipantC
java -Dname=ParticipantC -jar corda-webserver.jar

```
