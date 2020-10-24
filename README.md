# javafx8-minesweeper_executable
Repository for the executable .jar (Java Archive File) of the project hosted here https://github.com/kurushiidrive/javafx8-minesweeper
The purpose of making this separate is to make it easier to run the game without a specific development environment (JRE 8 is still required).

To run from Terminal or Command Prompt, set your working directory to be the same directory where the jar file is located, then type `java -jar minesweeper.jar`.

Note that on Linux there are complications in running the executable jar if you are using OpenJDK8. As such, it is best to run the jar using a JDK 8 distribution that includes JavaFX, such as the distribution from Zulu contained in [this archive](https://cdn.azul.com/zulu/bin/zulu8.48.0.53-ca-fx-jdk8.0.265-linux_x64.tar.gz) (find the archive that contains a **JDK FX** compatible with your system from [this link](https://www.azul.com/downloads/zulu-community/)). Simply extract the archive you downloaded, optionally adding the bin directory inside of the produced folder to your PATH, and run the same command as above, `/your-zulu-java-home/bin/java -jar minesweeper.jar` (full path isn't needed if you added the zulu installation directory's bin folder to your PATH).
