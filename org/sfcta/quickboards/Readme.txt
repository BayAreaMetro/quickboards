from above "org" dir:

To compile:
set JARNAME=qbtemp
set JARDIR=[directory where you're running these commands]

javac -cp M:\Software\Quickboards\sfcta.jar org\sfcta\quickboards\*.java
jar -cvfm %JARNAME%.jar org\sfcta\quickboards\Manifest.txt org\sfcta\quickboards\*.class
jar -tvf %JARNAME%.jar

To run:
java -Xms64m -Xmx512m -cp "%JARDIR%\%JARNAME%.jar;M:\Software\Quickboards\sfcta.jar" org.sfcta.quickboards.QuickBoards quickboards.ctl quickboards_out.xls

To deploy:
Compile with JARNAME=quickboards
Copy the resulting quickboards.jar and sfcta.jar to CTRAMP\runtime