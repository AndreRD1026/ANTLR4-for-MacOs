# Install ANTLR4 on MacOs

## 1. Install JDK (version 11 or higher)
`You can see here:` https://www.oracle.com/java/technologies/downloads/#jdk20-mac <br>

## 2. Download Jar File
In this case you need the file <br><br>
First step: Go to lib <br><br>
`cd /usr/local/lib` <br><br>
Second step: Download the jar<br><br>
`curl -O https://www.antlr.org/download/antlr-4.13.0-complete.jar`<br><br>
You can choose another version of antlr4 for example 4.10.1<br><br>
Stable Versions : https://pub.dev/packages/antlr4/versions <br><br>
## 3. Add ANTLR to PATH
You need to edit `.zshrc` file and add the below commands<br><br>
`export CLASSPATH=".:/usr/local/lib/antlr-4.13.0-complete.jar:$CLASSPATH"`<br><br>
`alias antlr4='java -Xmx500M -cp "/usr/local/lib/antlr-4.13.0-complete.jar:$CLASSPATH" org.antlr.v4.Tool'`<br><br>
`alias grun='java -Xmx500M -cp "/usr/local/lib/antlr-4.10.1-complete.jar:$CLASSPATH" org.antlr.v4.gui.TestRig'`<br><br>
Now `source ~/.zshrc` to make changes<br><br>
If you want to test installation of ANTLR `java org.antlr.v4.Tool` <br><br>
You see the next line `ANTLR Parser Generator  Version 4.13.0` <br><br>
For more information : https://github.com/antlr/antlr4/blob/master/doc/getting-started.md
