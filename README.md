# AngryBirds

A [LibGDX](https://libgdx.com/) project generated with [gdx-liftoff](https://github.com/libgdx/gdx-liftoff).

This project extends the template to build an **Angry Birds-inspired game** with projectile physics, level screens, and state-saving functionality using LibGDX.

## Platforms

- `core`: Main module with the application logic shared by all platforms.
- `lwjgl3`: Primary desktop platform using LWJGL3; was called 'desktop' in older docs.

## Requirements

- Java 8 or above
- Git
- No need to install Gradle separately (Gradle Wrapper included)

## Running the Project

Clone the repository:

```bash
git clone [your-github-repo-link]
cd AngryBirds
```

Run using Gradle:

**On Windows:**
```bash
gradlew lwjgl3:run
```

**On Linux/macOS:**
```bash
./gradlew lwjgl3:run
```

This will launch the game on your desktop using LWJGL3.

## Building a Runnable JAR

To build a runnable JAR for sharing or running directly:

```bash
./gradlew lwjgl3:jar
```

The JAR file will be found at:
```
lwjgl3/build/libs
```

To run the JAR:
```bash
java -jar lwjgl3/build/libs/[your-jar-file-name].jar
```

## Gradle

This project uses [Gradle](https://gradle.org/) to manage dependencies.  
You can run Gradle tasks using `gradlew.bat` on Windows or `./gradlew` on Linux/macOS.

Useful Gradle tasks and flags:

- `--continue`: errors will not stop the tasks from running.
- `--daemon`: Gradle daemon will be used for tasks.
- `--offline`: use cached dependency archives.
- `--refresh-dependencies`: forces validation of all dependencies.
- `build`: builds sources and archives of all projects.
- `clean`: removes `build` folders with compiled classes and archives.
- `cleanEclipse`: removes Eclipse project data.
- `cleanIdea`: removes IntelliJ project data.
- `eclipse`: generates Eclipse project data.
- `idea`: generates IntelliJ project data.
- `lwjgl3:run`: starts the application.
- `lwjgl3:jar`: builds the runnable JAR found at `lwjgl3/build/libs`.
- `test`: runs unit tests (if any).

Most tasks can be run with the `name:` prefix to target a specific module. For example:

```bash
core:clean
```

will clean the `build` folder only from the `core` module.

## Notes

- The game automatically saves progress using LibGDX Preferences and JSON serialization, allowing players to resume where they left off.
- The project is structured with clear OOP principles, following SOLID practices, to make it easy to extend with new levels or gameplay features.

