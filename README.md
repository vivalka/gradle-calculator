Install Gradle Plugin.

Configure Gradle build tool

Create jenkins job

Under Gradle build section

a.involk gradle: user can use configured gradle tool (but it may create problem because same gradle tool should be installed on all the build agent)

b.wrapper location: if we choose this option then gradle automatically installed required gradle on build agent depened on gradlew file under source code.

if you have choosed wrapper location then tick Make gradlew executable

save and build
