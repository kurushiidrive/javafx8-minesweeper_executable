# javafx8-minesweeper_executable
Repository for the executable .jar (Java Archive File) of the project hosted here https://github.com/kurushiidrive/javafx8-minesweeper
The purpose of making this separate is to make it easier to run the game without a specific development environment (JRE 8 is still required).

To run from Terminal or Command Prompt, set your working directory to be the same directory where the jar file is located, then type `java -jar minesweeper.jar`.

Note that on Linux there are complications in running the executable jar if you are using OpenJDK8. As such, it is best to run the jar using a JDK 8 distribution that includes JavaFX, such as the distribution from Zulu contained in [this archive](https://cdn.azul.com/zulu/bin/zulu8.48.0.53-ca-fx-jdk8.0.265-linux_x64.tar.gz) (find the archive that contains a **JDK FX** compatible with your system from [this link](https://www.azul.com/downloads/zulu-community/)). Simply extract the archive you downloaded, optionally adding the bin directory inside of the produced folder to your PATH, and run the same command as above, `/your-zulu-java-home/bin/java -jar minesweeper.jar` (full path isn't needed if you added the zulu installation directory's bin folder to your PATH).

If you would prefer to build the project yourself on your own machine (either the `.class` files or the executable `.jar` file), download the `javafx8-minesweeper.tar.gz` file, and extract it (on Linux/macOS, type `tar xvf javafx8-minesweeper.tar.gz` at the command line).

The `javafx8-minesweeper.tar.gz` tarball contains all the necessary source files and dependencies needed to build the project and make an executable .jar file; the `Makefile` inside of it also has the necessary rules to accomplish this; however, it assumes that the suitable `javac` compiler and `jar` packager are in your PATH.

To build the project and create the executable jar all in one step, type `make` at the command line, which invokes the default `make` target; it first compiles the necessary source files, then creates a `MANIFEST.MF` file, and then combines the produced `.class` files and the existing `.html` and `.gif`/`.png` files that were in the tarball, and creates the `.jar` executable. The executable jar is called `javafx8-minesweeper.jar`, and can be run with `java -jar javafx8-minesweeper.jar`.

The `Makefile` contains other `make` targets with which you may experiment as you wish.
