# ![Seppuku](res/seppuku_full.png)

Seppuku is a free, lightweight, open-source [_Minecraft Forge_](https://files.minecraftforge.net/) mod for Minecraft 1.12.2, and soon to be for recent versions...

Originally oriented towards the 9B9T and 2B2T anarchy servers; it is a fully featured client-side mod with an external plugin API, unique exploits, and a [solid Discord community](https://discord.gg/UzWBZPe).

# Requirements
- **JDK 8** (https://adoptopenjdk.net/, https://aws.amazon.com/corretto/)
- __(optional)__ **Git**

# Building

### Linux / Mac
1. Clone the repository: `git clone git@github.com:seppukudevelopment/seppuku.git`
2. Run `./gradlew setupDecompWorkspace` 
3. Edit `build.gradle` and change field `buildmode` to `RELEASE`. (e.g. `def
 buildmode = "RELEASE"`)
4. Run `./gradlew build`.

Your .jar file is in `build/libs/`.

#### Windows
> Using a git shell for Windows and using the linux guide above is highly recommended. (https://git-scm.com/downloads) 
1. Clone the repository.
2. Import the project through Gradle via `build.gradle` (simple tutorials online for 
[intellij](https://stackoverflow.com/questions/31256356/how-to-import-gradle-projects-in-intellij), 
[eclipse](https://stackoverflow.com/questions/10722773/import-existing-gradle-git-project-into-eclipse), etc.)
3. Run the gradle command `setupDecompWorkspace` via the IDE or gradlew.bat file (via command prompt: `gradlew.bat setupDecompWorkspace`) 
4. Refresh the project (reload ide / refresh gradle workspace)
5. Edit `build.gradle` and change field `buildmode` to `RELEASE` ex: `def
buildmode = "RELEASE"`
6. Run the gradle command `build` via the IDE or gradlew.bat file (via
 command prompt: `gradlew.bat build`) 
 
Your .jar file is in `build/libs/`.

# Debugging
- Use VM arg `-Dfml.coreMods.load=me.rigamortis.seppuku.impl.fml.core.SeppukuLoadingPlugin`
- Ensure field `buildmode` in **build.gradle** is set to `IDE` ex: `def buildmode = "IDE"`
