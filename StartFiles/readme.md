# 💻 Ready-made sh and bat files to run your server.
[check file](StartFiles/start.sh "start.sh")
You need to put this file in the root directory of your Minecraft server.<br>
If you are using Linux, then go to the server directory and write the command:
```
./start.sh
```
If you are using Windows, then run .bat file.

# 💻 Готовые файлы sh и bat для запуска вашего сервера.
[готовый скрипт](StartFiles/start.sh "start.sh")
Вам нужно поместить этот файл в корневую директорию вашего сервера Minecraft.
Если вы используете Linux, то перейдите в директорию сервера и напишите команду:
```
./start.sh
```
Если вы используете Windows, то запустите файл .bat.

# 💻 You can also use the command.
```
java -Xms8192M -Xmx8192M --add-modules=jdk.incubator.vector -XX:+UseG1GC -XX:+ParallelRefProcEnabled -XX:MaxGCPauseMillis=200 -XX:+UnlockExperimentalVMOptions -XX:+DisableExplicitGC -XX:+AlwaysPreTouch -XX:G1HeapWastePercent=5 -XX:G1MixedGCCountTarget=4 -XX:InitiatingHeapOccupancyPercent=15 -XX:G1MixedGCLiveThresholdPercent=90 -XX:G1RSetUpdatingPauseTimePercent=5 -XX:SurvivorRatio=32 -XX:+PerfDisableSharedMem -XX:MaxTenuringThreshold=1 -Dusing.aikars.flags=https://mcflags.emc.gs -Daikars.new.flags=true -XX:G1NewSizePercent=30 -XX:G1MaxNewSizePercent=40 -XX:G1HeapRegionSize=8M -XX:G1ReservePercent=20 -jar server.jar --nogui
```
