# ✔ Конфигурация server.properties
## Одним из самых главных конфигурационных файлов сервера является server.properties. Он находится в корневой директории вашего сервера и имеет следующий вид: 
![image](/images/serverproperties.png)
Данный конфигурационный файл имеет не так много параметров, которые вам скорее всего понадобятся, большинство из вас может его даже не изменять так как он хорошо работает и при стандартных настройках.
> [!IMPORTANT]
> Любые изменения этого файла требуют перезагрузку вашего сервера.
Данный курс написан для людей, которые не горят желанием глубоко уходить в тему создания серверов или только начинают свой путь, поэтому вы можете изменить лишь пару параметров.
<br>
Начиная с версии 23w31a, если этот файл не был найден, то он генерируется со следующим содержанием:
<details>
<summary>Нажми на меня</summary>
  
```
#Minecraft server properties
#(File modification date and time)
enable-jmx-monitoring=false
rcon.port=25575
level-seed=
gamemode=survival
enable-command-block=false
enable-query=false
generator-settings={}
enforce-secure-profile=true
level-name=world
motd=A Minecraft Server
query.port=25565
pvp=true
generate-structures=true
max-chained-neighbor-updates=1000000
difficulty=easy
network-compression-threshold=256
max-tick-time=60000
require-resource-pack=false
use-native-transport=true
max-players=20
online-mode=true
enable-status=true
allow-flight=false
initial-disabled-packs=
broadcast-rcon-to-ops=true
view-distance=10
server-ip=
resource-pack-prompt=
allow-nether=true
server-port=25565
enable-rcon=false
sync-chunk-writes=true
op-permission-level=4
prevent-proxy-connections=false
hide-online-players=false
resource-pack=
entity-broadcast-range-percentage=100
simulation-distance=10
rcon.password=
player-idle-timeout=0
force-gamemode=false
rate-limit=0
hardcore=false
white-list=false
broadcast-console-to-ops=true
spawn-npcs=true
spawn-animals=true
log-ips=true
function-permission-level=2
initial-enabled-packs=vanilla
level-type=minecraft\:normal
text-filtering-config=
spawn-monsters=true
enforce-whitelist=false
spawn-protection=16
resource-pack-sha1=
max-world-size=29999984
```
</details>

## ⚙ allow-flight
Может принимать параметры (boolean):
- true
- false

🔎 Для чего предназначено:<br>
Позволяет пользователям использовать полёт на сервере в режиме выживания, если у них установлен чит, обеспечивающий полет. Не влияет на игроков в креативе или с полётом выданным командой администратора.

## ⚙ allow-nether
Может принимать параметры (boolean):
- true
- false

🔎 Для чего предназначено:<br>
Позволяет игрокам получить доступ к nether миру. Для этой задачи лучше использовать специальные плагины так как после изменения разрешения в этом файле вам потребуется перезагрузка сервера.

## ⚙ broadcast-console-to-ops
Может принимать параметры (boolean):
- true
- false

🔎 Для чего предназначено:<br>
Отправляйте выходные данные консольных команд всем онлайн-операторам.

## ⚙ broadcast-rcon-to-ops
Может принимать параметры (boolean):
- true
- false

🔎 Для чего предназначено:<br>
Отправляйте выходные данные консольных команд rcon всем онлайн-операторам.

## ⚙ difficulty
Может принимать параметры (string):
- peaceful (0)
- easy (1)
- normal (2)
- hard (3)

🔎 Для чего предназначено:<br>
Устанавливает игровую сложность, также можно изменять командой, находясь в игре или используя консоль.

## ⚙ enable-command-block
Может принимать параметры (boolean):
- true
- false

🔎 Для чего предназначено:<br>
Отвечает за включение/выключение работы командных блоков на сервере.

## ⚙ enable-jmx-monitoring
Может принимать параметры (boolean):
- true
- false

🔎 Для чего предназначено:<br>
Предоставляет MBean с именем объекта net.minecraft.server:type=Server и двумя атрибутами averageTickTime и tickTimes, отображающими время срабатывания в миллисекундах.<br>
Чтобы включить JMX в среде выполнения Java, вам также необходимо добавить пару флагов JVM в автозагрузку.

## ⚙ enable-rcon
Может принимать параметры (boolean):
- true
- false

🔎 Для чего предназначено:<br>
Разрешает удаленный доступ к консоли сервера.
> [!WARNING]
> Не рекомендуется подключать RCON к Интернету, поскольку протокол RCON передает все без шифрования. Все данные (включая пароль RCON), передаваемые между сервером RCON и клиентом, могут быть переданы кому-либо, прослушивающему ваше соединение.

## ⚙ enable-status
Может принимать параметры (boolean):
- true
- false

🔎 Для чего предназначено:<br>
Отображает сервер как "подключенный" в списке серверов.

## ⚙ enable-query
Может принимать параметры (boolean):
- true
- false

🔎 Для чего предназначено:<br>
Включает прослушиватель сервера протокола GameSpy4. Используется для получения информации о сервере.

## ⚙ enforce-secure-profile
Может принимать параметры (boolean):
- true
- false

🔎 Для чего предназначено:<br>
Если установлено значение true, игроки без открытого ключа, подписанного Mojang, не смогут подключиться к серверу.

## ⚙ white-list
Может принимать параметры (boolean):
- true
- false

🔎 Для чего предназначено:<br>
Определяет разрешеное ли людям не находящимся в белом списке подключаться к серверу.<br>
Настройка white-list производится внутри игры через команду /whitelist или через консоль сервера. Также можно добавлять/удалять игроков используя файл, находящийся в директории нашего сервера, но это НЕУДОБНО!

## ⚙ entity-broadcast-range-percentage
Может принимать параметры (integer (10-1000)):
- 10 min
- 1000 max 

🔎 Для чего предназначено:<br>
Определяет, насколько близко объекты должны находиться друг к другу перед отправкой клиентам. Чем выше значение, тем дальше они будут отображаться, что может привести к увеличению задержки. Значение выражается в процентах от значения по умолчанию.

## ⚙ force-gamemode
Может принимать параметры :
- true
- false

🔎 Для чего предназначено:<br>
Автоматически переводит людей в заданный режим игры при заходе на сервер.

## ⚙ function-permission-level
Может принимать параметры (integer):
- 1
- 2
- 3
- 4

🔎 Для чего предназначено:<br>
Устанавливает уровень разрешений по умолчанию для функций.

## ⚙ 
Может принимать параметры:
- 
- 
- 

🔎 Для чего предназначено:<br>

## ⚙ 
Может принимать параметры:
- 
- 
- 

🔎 Для чего предназначено:<br>

## ⚙ 
Может принимать параметры:
- 
- 
- 

🔎 Для чего предназначено:<br>

## ⚙ 
Может принимать параметры:
- 
- 
- 

🔎 Для чего предназначено:<br>
