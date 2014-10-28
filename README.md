############################################################
# +------------------------------------------------------+ #
# |                       Notes                          | #
# +------------------------------------------------------+ #
############################################################

# If you want to use special characters in this document, such as accented letters, you MUST save the file as UTF-8, not ANSI.
# If you receive an error when Essentials loads, ensure that:
#   - No tabs are present: YAML only allows spaces
#   - Indents are correct: YAML hierarchy is based entirely on indentation
#   - You have "escaped" all apostrophes in your text: If you want to write "don't", for example, write "don''t" instead (note the doubled apostrophe)
#   - Text with symbols is enclosed in single or double quotation marks

# If you have problems join the Essentials help support channel: http://tiny.cc/EssentialsChat

############################################################
# +------------------------------------------------------+ #
# |                 Essentials (Global)                  | #
# +------------------------------------------------------+ #
############################################################

# A color code between 0-9 or a-f. Set to 'none' to disable.
ops-name-color: '4'

# The character(s) to prefix all nicknames, so that you know they are not true usernames.
nickname-prefix: '~'

# The maximum length allowed in nicknames. The nickname prefix is included in this.
max-nick-length: 15

# Disable this if you have any other plugin, that modifies the displayname of a user.
change-displayname: true

# When this option is enabled, the (tab) player list will be updated with the displayname.
# The value of change-displayname (above) has to be true.
#change-playerlist: true

# When essentialschat.jar isn't used, force essentials to add the prefix and suffix from permission plugins to displayname.
# This setting is ignored if essentialschat.jar is used, and defaults to 'true'.
# The value of change-displayname (above) has to be true.
# Do not edit this setting unless you know what you are doing!
#add-prefix-suffix: false

# If the teleport destination is unsafe, should players be teleported to the nearest safe location?
# If this is set to true, Essentials will attempt to teleport players close to the intended destination.
# If this is set to false, attempted teleports to unsafe locations will be cancelled with a warning.
teleport-safety: true

# The delay, in seconds, required between /home, /tp, etc.
teleport-cooldown: 3

# The delay, in seconds, before a user actually teleports.  If the user moves or gets attacked in this timeframe, the teleport never occurs.
teleport-delay: 3

# The delay, in seconds, a player can't be attacked by other players after they have been teleported by a command.
# This will also prevent the player attacking other players.
teleport-invulnerability: 4

# The delay, in seconds, required between /heal or /feed attempts.
heal-cooldown: 690

# What to prevent from /i /give.
# e.g item-spawn-blacklist: 46,11,10
item-spawn-blacklist:

# Set this to true if you want permission based item spawn rules.
# Note: The blacklist above will be ignored then.
# Example permissions (these go in your permissions manager):
#  - essentials.itemspawn.item-all
#  - essentials.itemspawn.item-[itemname]
#  - essentials.itemspawn.item-[itemid]
#  - essentials.give.item-all
#  - essentials.give.item-[itemname]
#  - essentials.give.item-[itemid]
#  - essentials.unlimited.item-all
#  - essentials.unlimited.item-[itemname]
#  - essentials.unlimited.item-[itemid]
#  - essentials.unlimited.item-bucket # Unlimited liquid placing
#
# For more information, visit http://wiki.ess3.net/wiki/Command_Reference/ICheat#Item.2FGive
permission-based-item-spawn: false

# Mob limit on the /spawnmob command per execution.
spawnmob-limit: 10

# Shall we notify users when using /lightning?
warn-on-smite: true

# motd and rules are now configured in the files motd.txt and rules.txt.

# When a command conflicts with another plugin, by default, Essentials will try to force the OTHER plugin to take priority.
# Commands in this list, will tell Essentials to 'not give up' the command to other plugins.
# In this state, which plugin 'wins' appears to be almost random.
#
# If you have two plugin with the same command and you wish to force Essentials to take over, you need an alias.
# To force essentials to take 'god' alias 'god' to 'egod'.
# See http://wiki.bukkit.org/Bukkit.yml#aliases for more information

overridden-commands:
#  - god
#  - info

# Disabling commands here will prevent Essentials handling the command, this will not affect command conflicts.
# Commands should fallback to the vanilla versions if available.
# You should not have to disable commands used in other plugins, they will automatically get priority.
disabled-commands:
#  - nick
#  - clear

# These commands will be shown to players with socialSpy enabled.
# You can add commands from other plugins you may want to track or
# remove commands that are used for something you dont want to spy on.
socialspy-commands:
  - msg
  - w
  - r
  - mail
  - m
  - t
  - whisper
  - emsg
  - tell
  - er
  - reply
  - ereply
  - email
  - action
  - describe
  - eme
  - eaction
  - edescribe
  - etell
  - ewhisper
  - pm

# If you do not wish to use a permission system, you can define a list of 'player perms' below.
# This list has no effect if you are using a supported permissions system.
# If you are using an unsupported permissions system, simply delete this section.
# Whitelist the commands and permissions you wish to give players by default (everything else is op only).
# These are the permissions without the "essentials." part.
player-commands:
  - afk
  - afk.auto
  - back
  - back.ondeath
  - balance
  - balance.others
  - balancetop
  - build
  - chat.color
  - chat.format
  - chat.shout
  - chat.question
  - clearinventory
  - compass
  - depth
  - delhome
  - getpos
  - geoip.show
  - help
  - helpop
  - home
  - home.others
  - ignore
  - info
  - itemdb
  - kit
  - kits.tools
  - list
  - mail
  - mail.send
  - me
  - motd
  - msg
  - msg.color
  - nick
  - near
  - pay
  - ping
  - protect
  - r
  - rules
  - realname
  - seen
  - sell
  - sethome
  - setxmpp
  - signs.create.protection
  - signs.create.trade
  - signs.break.protection
  - signs.break.trade
  - signs.use.balance
  - signs.use.buy
  - signs.use.disposal
  - signs.use.enchant
  - signs.use.free
  - signs.use.gamemode
  - signs.use.heal
  - signs.use.info
  - signs.use.kit
  - signs.use.mail
  - signs.use.protection
  - signs.use.repair
  - signs.use.sell
  - signs.use.time
  - signs.use.trade
  - signs.use.warp
  - signs.use.weather
  - spawn
  - suicide
  - time
  - tpa
  - tpaccept
  - tpahere
  - tpdeny
  - warp
  - warp.list
  - world
  - worth
  - xmpp

# Note: All items MUST be followed by a quantity!
# All kit names should be lower case, and will be treated as lower in permissions/costs.
# Syntax: - itemID[:DataValue/Durability] Amount [Enchantment:Level].. [itemmeta:value]...
# For Item meta information visit http://wiki.ess3.net/wiki/Item_Meta
# 'delay' refers to the cooldown between how often you can use each kit, measured in seconds.
# For more information, visit http://wiki.ess3.net/wiki/Kits
kits:
  res:
    delay: 980
    items:
      - 290 1 name:&a&l\\\&c&l-RES-&a&l///
  Akcija:
    delay: 96000
    items:
      - 276 1 unbreaking:1 name:&6&l[&9&lKardas&6&l] knockback:1 sharpness:1
      - 297 64 name:&6&lDuona
      - 364 5 name:&6&lMesa
      - 290 1 name:&a&l\\\&c&l-RES-&a&l///
      - 310 1 name:&9&lKepure protection:1
      - 311 1 name:&9&lMaikute protection:1
      - 312 1 name:&9&lDzinsai protection:1
      - 313 1 name:&9&lBateliai protection:1
      - 266 4 name:&e&lAuksas
      - 265 3 name:&f&lSidabras 
      - 384 64 name:&a&lPatirtis
      - apple 32 name:&6&lObuolys
  Prasciokas:
    delay: 48000
    items:
      - 272 1 unbreaking:1 name:&9&lKardas
      - 273 1 unbreaking:1 name:&9&lKastuvas
      - 274 1 unbreaking:1 name:&9&lKirtiklis
      - 275 1 unbreaking:1 name:&9&lKirvis
      - 297 64 name:&6&lMaistas
      - 5 64 name:&1&lMedziaga
      - 5 64 name:&1&lMedziaga
      - 50 16 name:&a&lSviesa
      - 54 2 name:&7&lSkrynia
      - 61 1 name:&2&lKrosnis
      - 364 5 name:&6&lMaistas
      - 260 5 name:&6&lMaistas
      - 298 1 color:25,25,25 name:&5&lKepure
      - 299 1 color:25,25,25 name:&5&lMaikute
      - 300 1 color:25,25,25 name:&5&lDzinsai
      - 301 1 color:25,25,25 name:&5&lBateliai
      - 266 4 name:&e&lAuksas
      - 265 3 name:&f&lSidabras 
      - 384 32 name:&a&lPatirtis
  Valstietis:
    delay: 48000
    items:
      - 267 1
      - 369 6
      - 372 3
      - 5 64
      - 5 64
      - 5 64
      - 266 4
      - 322:1 1
      - 264 1
  Globejas:
    delay: 48000
    items:
      - 264 3
      - 322:1 1
      - 322 3
      - 279 1
      - 320 3
      - 5 64
      - 5 64
      - 15 10
      - 267 1
  Meistras:
    delay: 48000
    items:
      - 306 1
      - 307 1
      - 308 1
      - 309 1
      - 322:1 1
      - 17 64
      - 292 1
      - 257 1
      - 372 1
  Seniunas:
    delay: 48000
    items:
      - 276 1 knockback:4 fireaspect:2
      - 289 16
      - 264 5
      - 322:1 2
  Rektorius:
    delay: 48000
    items:
      - 383:100 1
      - 419 1
      - 329 2
      - 327 1
  Rastininkas:
    delay: 48000
    items:
      - 47 28
      - 49 12
      - 50 64
      - 46 12
  Dvarininkas:
    delay: 48000
    items:
      - 383:95
      - 352 3
      - 354 2
      - 357 3
  Zudikas:
    delay: 48000
    items:
      - 56 12
      - 88 5
      - 373:8193 1
      - 373:16428 1
      - 373:16458 1
      - 375 3
  Imperatorius:
    delay: 48000
    items:
      - 322:1 3
      - 266 12
      - 91 2
      - 289 16
  vip:
    delay: 48000
    items:
      - 276 1 alldamage:5 smite:2 name:&6&lVIP
      - 277 1 digspeed:3 silktouch:1 name:&6&lVIP
      - 278 1 digspeed:3 silktouch:1 name:&6&lVIP
      - 279 1 digspeed:3 silktouch:1 name:&6&lVIP
      - 384 64 name:&a&lPatirtis
      - 384 64 name:&a&LPatirtis
      - 322:1 4 name:&1&LMaistas
      - enderpearl 8 name:&5&lTele
      - 383:100 2 name:&7&LTransportas
  premium:
    delay: 48000
    items:
      - 310 1 unbreaking:2 blastprotection:1 protection:4 name:&3&LSalmas
      - 311 1 unbreaking:2 blastprotection:1 protection:4 name:&3&LAntkrutis
      - 312 1 unbreaking:2 blastprotection:1 protection:4 name:&3&LKelnes
      - 313 1 unbreaking:2 blastprotection:1 protection:4 name:&3&LBatai
      - 261 1 flame:1 power:2 name:&5&LLankas
      - arrow 32 name:&7&lStreles
      - 52 1 name:&2&lMonstrai
      - 322:1 5 name:&6&LObuolys
      - 364 64 name:&9&lKepsnys
  xp:
    delay: 48000
    items:
      - 384 64 name:&a&lPatirtis
      - 384 64 name:&a&lPatirtis
      - 384 64 name:&a&lPatirtis
      - 384 64 name:&a&lPatirtis
      - 384 64 name:&a&lPatirtis
  mobeggs:
    delay: 48000
    items:
      - 383:100 3 name:&eŽ&lirgas
      - 383:57 16 name:&e&lKiauliažmogis
      - 383:50 16 name:&e&lPasal&e&eūnas
      - 383:58 16 name:&e&lPabaigažmogis
      - 383:90 17 name:&e&lKiaul&r&eė
  firework:
    delay: 6000
    items:
      - 401 1 name:Angry_Creeper color:red fade:green type:creeper power:1
      - 401 1 name:StarryNight color:yellow,orange fade:blue type:star effect:trail,twinkle power:1
      - 401 2 name:SolarWind color:yellow,orange fade:red shape:large effect:twinkle color:yellow,orange fade:red shape:ball effect:trail color:red,purple fade:pink shape:star effect:trail power:1
  udali ten tekst i napish CTRL+V

# Essentials Sign Control
# See http://wiki.ess3.net/wiki/Sign_Tutorial for instructions on how to use these.
# To enable signs, remove # symbol. To disable all signs, comment/remove each sign.
# Essentials Colored sign support will be enabled when any sign types are enabled.
# Color is not an actual sign, it's for enabling using color codes on signs, when the correct permissions are given.

enabledSigns:
  - color
  - balance
  - buy
  - sell
  - trade
  - free
  - disposal
  - warp
  - kit
  - mail
  - enchant
  - gamemode
  - heal
  - info
  - spawnmob
  - repair
  - time
  - weather

# How many times per second can Essentials signs be interacted with per player.
# Values should be between 1-20, 20 being virtually no lag protection.
# Lower numbers will reduce the possibility of lag, but may annoy players.
sign-use-per-second: 4

# Backup runs a batch/bash command while saving is disabled.
backup:
  # Interval in minutes.
  interval: 30
  # Unless you add a valid backup command or script here, this feature will be useless.
  # Use 'save-all' to simply force regular world saving without backup.
  #command: 'rdiff-backup World1 backups/World1'

# Set this true to enable permission per warp.
per-warp-permission: false

# Sort output of /list command by groups.
# You can hide and merge the groups displayed in /list by defining the desired behaviour here.
# Detailed instructions and examples can be found on the wiki: http://wiki.ess3.net/wiki/List
list:
    # To merge groups, list the groups you wish to merge
    #Staff: owner admin moderator
    Admins: owner admin
    # To limit groups, set a max user limit
    #builder: 20
    # To hide groups, set the group as hidden
    #default: hidden
    # Uncomment the line below to simply list all players with no grouping
    #Players: '*'

# More output to the console.
debug: false

# Set the locale for all messages.
# If you don't set this, the default locale of the server will be used.
# For example, to set language to English, set locale to en, to use the file "messages_en.properties".
# Don't forget to remove the # in front of the line.
# For more information, visit http://wiki.ess3.net/wiki/Locale
locale: lt

# Turn off god mode when people exit.
remove-god-on-disconnect: false

# Auto-AFK
# After this timeout in seconds, the user will be set as afk.
# This feature requires the player to have essentials.afk.auto node.
# Set to -1 for no timeout.
auto-afk: 300

# Auto-AFK Kick
# After this timeout in seconds, the user will be kicked from the server.
# essentials.afk.kickexempt node overrides this feature.
# Set to -1 for no timeout.
auto-afk-kick: -1

# Set this to true, if you want to freeze the player, if he is afk.
# Other players or monsters can't push him out of afk mode then.
# This will also enable temporary god mode for the afk player.
# The player has to use the command /afk to leave the afk mode.
freeze-afk-players: false

# When the player is afk, should he be able to pickup items?
# Enable this, when you don't want people idling in mob traps.
disable-item-pickup-while-afk: false

# This setting controls if a player is marked as active on interaction.
# When this setting is false, you will need to manually un-AFK using the /afk command.
cancel-afk-on-interact: true

# Should we automatically remove afk status when the player moves?
# Player will be removed from AFK on chat/command regardless of this setting.
# Disable this to reduce server lag.
cancel-afk-on-move: true

# You can disable the death messages of Minecraft here.
death-messages: true

# Should operators be able to join and part silently.
# You can control this with permissions if it is enabled.
allow-silent-join-quit: false

# You can set a custom join message here, set to "none" to disable.
# You may use color codes, use {USERNAME} the player's name or {PLAYER} for the player's displayname.
custom-join-message: "&b&l[&7&l{USERNAME}&b&l] &6&lPrisijunge i serveri!"

# You can set a custom quit message here, set to "none" to disable.
# You may use color codes, use {USERNAME} the player's name or {PLAYER} for the player's displayname.
custom-quit-message: "&b&l[&7&l{USERNAME}&b&l] &6&lAtsijunge nuo serverio..."

# Add worlds to this list, if you want to automatically disable god mode there.
no-god-in-worlds:
#  - world_nether

# Set to true to enable per-world permissions for teleporting between worlds with essentials commands.
# This applies to /world, /back, /tp[a|o][here|all], but not warps.
# Give someone permission to teleport to a world with essentials.worlds.<worldname>
# This does not affect the /home command, there is a separate toggle below for this.
world-teleport-permissions: false

# The number of items given if the quantity parameter is left out in /item or /give.
# If this number is below 1, the maximum stack size size is given. If over-sized stacks.
# are not enabled, any number higher than the maximum stack size results in more than one stack.
default-stack-size: -1

# Over-sized stacks are stacks that ignore the normal max stack size.
# They can be obtained using /give and /item, if the player has essentials.oversizedstacks permission.
# How many items should be in an over-sized stack?
oversized-stacksize: 64

# Allow repair of enchanted weapons and armor.
# If you set this to false, you can still allow it for certain players using the permission.
# essentials.repair.enchanted
repair-enchanted: true

# Allow 'unsafe' enchantments in kits and item spawning.
# Warning: Mixing and overleveling some enchantments can cause issues with clients, servers and plugins.
unsafe-enchantments: false

#Do you want essentials to keep track of previous location for /back in the teleport listener?
#If you set this to true any plugin that uses teleport will have the previous location registered.
register-back-in-listener: false

#Delay to wait before people can cause attack damage after logging in.
login-attack-delay: 5

#Set the max fly speed, values range from 0.1 to 1.0
max-fly-speed: 0.8

#Set the max walk speed, values range from 0.1 to 1.0
max-walk-speed: 0.8

#Set the maximum amount of mail that can be sent within a minute.
mails-per-minute: 1000

# Set the maximum time /tempban can be used for in seconds.
# Set to -1 to disable, and essentials.tempban.unlimited can be used to override.
max-tempban-time: -1

############################################################
# +------------------------------------------------------+ #
# |                   EssentialsHome                     | #
# +------------------------------------------------------+ #
############################################################

# Allows people to set their bed at daytime.
update-bed-at-daytime: true

# Set to true to enable per-world permissions for using homes to teleport between worlds.
# This applies to the /home only.
# Give someone permission to teleport to a world with essentials.worlds.<worldname>
world-home-permissions: false

# Allow players to have multiple homes.
# Players need essentials.sethome.multiple before they can have more than 1 home.
# You can set the default number of multiple homes using the 'default' rank below.
# To remove the home limit entirely, give people 'essentials.sethome.multiple.unlimited'.
# To grant different home amounts to different people, you need to define a 'home-rank' below.
# Create the 'home-rank' below, and give the matching permission: essentials.sethome.multiple.<home-rank>
# For more information, visit http://wiki.ess3.net/wiki/Multihome
sethome-multiple:
  default: 3
  vip: 5
  staff: 10

# In this example someone with 'essentials.sethome.multiple' and 'essentials.sethome.multiple.vip' will have 5 homes.

# Set timeout in seconds for players to accept tpa before request is cancelled.
# Set to 0 for no timeout.
tpa-accept-cancellation: 120

############################################################
# +------------------------------------------------------+ #
# |                   EssentialsEco                      | #
# +------------------------------------------------------+ #
############################################################

# For more information, visit http://wiki.ess3.net/wiki/Essentials_Economy

# Defines the balance with which new players begin.  Defaults to 0.
starting-balance: 0

# worth-# defines the value of an item when it is sold to the server via /sell.
# These are now defined in worth.yml

# Defines the cost to use the given commands PER USE.
# Some commands like /repair have sub-costs, check the wiki for more information.
command-costs:
  # /example costs $1000 PER USE
  #example: 1000
  # /kit tools costs $1500 PER USE
  #kit-tools: 1500

# Set this to a currency symbol you want to use.
currency-symbol: '$'

# Set the maximum amount of money a player can have.
# The amount is always limited to 10 trillion because of the limitations of a java double.
max-money: 10000000000000

# Set the minimum amount of money a player can have (must be above the negative of max-money).
# Setting this to 0, will disable overdrafts/loans completely.  Users need 'essentials.eco.loan' perm to go below 0.
min-money: -10000

# Enable this to log all interactions with trade/buy/sell signs and sell command.
economy-log-enabled: false

############################################################
# +------------------------------------------------------+ #
# |                   EssentialsHelp                     | #
# +------------------------------------------------------+ #
############################################################

# Show other plugins commands in help.
non-ess-in-help: true

# Hide plugins which do not give a permission.
# You can override a true value here for a single plugin by adding a permission to a user/group.
# The individual permission is: essentials.help.<plugin>, anyone with essentials.* or '*' will see all help regardless.
# You can use negative permissions to remove access to just a single plugins help if the following is enabled.
hide-permissionless-help: true

############################################################
# +------------------------------------------------------+ #
# |                   EssentialsChat                     | #
# +------------------------------------------------------+ #
############################################################

chat:

  # If EssentialsChat is installed, this will define how far a player's voice travels, in blocks.  Set to 0 to make all chat global.
  # Note that users with the "essentials.chat.spy" permission will hear everything, regardless of this setting.
  # Users with essentials.chat.shout can override this by prefixing text with an exclamation mark (!)
  # Users with essentials.chat.question can override this by prefixing text with a question mark (?)
  # You can add command costs for shout/question by adding chat-shout and chat-question to the command costs section."
  radius: 0

  # Chat formatting can be done in two ways, you can either define a standard format for all chat.
  # Or you can give a group specific chat format, to give some extra variation.
  # If set to the default chat format which "should" be compatible with ichat.
  # For more information of chat formatting, check out the wiki: http://wiki.ess3.net/wiki/Chat_Formatting

  format: '<{DISPLAYNAME}> {MESSAGE}'
  format: '&0&l[[FACTION]&0&l] &r &e&l<&r{DISPLAYNAME}&e&l>>&r&7 {MESSAGE}'

  group-formats:
    Savininkas: '&r &e&l<&r&n{DISPLAYNAME}&e&l>>&r&7&l {MESSAGE}'
  #  Admins: '{WORLDNAME} &c[{GROUP}]&r {DISPLAYNAME}&7:&c {MESSAGE}'

  # If you are using group formats make sure to remove the '#' to allow the setting to be read.

############################################################
# +------------------------------------------------------+ #
# |                 EssentialsProtect                    | #
# +------------------------------------------------------+ #
############################################################

protect:

  # General physics/behavior modifications.
  prevent:
    lava-flow: false
    water-flow: false
    water-bucket-flow: false
    fire-spread: true
    lava-fire-spread: true
    flint-fire: false
    lightning-fire-spread: true
    portal-creation: false
    tnt-explosion: false
    tnt-playerdamage: false
    tnt-minecart-explosion: false
    tnt-minecart-playerdamage: false
    fireball-explosion: false
    fireball-fire: false
    fireball-playerdamage: false
    witherskull-explosion: false
    witherskull-playerdamage: false
    wither-spawnexplosion: false
    wither-blockreplace: false
    creeper-explosion: false
    creeper-playerdamage: false
    creeper-blockdamage: false
    enderdragon-blockdamage: true
    enderman-pickup: false
    villager-death: false
    # Monsters won't follow players.
    # permission essentials.protect.entitytarget.bypass disables this.
    entitytarget: false
    # Prevent the spawning of creatures.
    spawn:
      creeper: false
      skeleton: false
      spider: false
      giant: false
      zombie: false
      slime: false
      ghast: false
      pig_zombie: false
      enderman: false
      cave_spider: false
      silverfish: false
      blaze: false
      magma_cube: false
      ender_dragon: false
      pig: false
      sheep: false
      cow: false
      chicken: false
      squid: false
      wolf: false
      mushroom_cow: false
      snowman: false
      ocelot: false
      iron_golem: false
      villager: false
      wither: false
      bat: false
      witch: false
      horse: false

  # Maximum height the creeper should explode. -1 allows them to explode everywhere.
  # Set prevent.creeper-explosion to true, if you want to disable creeper explosions.
  creeper:
    max-height: -1

  # Disable various default physics and behaviors.
  disable:
    # Should fall damage be disabled?
    fall: false

    # Users with the essentials.protect.pvp permission will still be able to attack each other if this is set to true.
    # They will be unable to attack users without that same permission node.
    pvp: false

    # Should drowning damage be disabled?
    # (Split into two behaviors; generally, you want both set to the same value.)
    drown: false
    suffocate: false

    # Should damage via lava be disabled?  Items that fall into lava will still burn to a crisp. ;)
    lavadmg: false

    # Should arrow damage be disabled?
    projectiles: false

    # This will disable damage from touching cacti.
    contactdmg: false

    # Burn, baby, burn!  Should fire damage be disabled?
    firedmg: false

    # Should the damage after hit by a lightning be disabled?
    lightning: false

    # Should Wither damage be disabled?
    wither: false

    # Disable weather options?
    weather:
      storm: false
      thunder: false
      lightning: false

############################################################
# +------------------------------------------------------+ #
# |                EssentialsAntiBuild                   | #
# +------------------------------------------------------+ #
############################################################

  # Disable various default physics and behaviors
  # For more information, visit http://wiki.ess3.net/wiki/AntiBuild

    # Should people with build: false in permissions be allowed to build?
    # Set true to disable building for those people.
    # Setting to false means EssentialsAntiBuild will never prevent you from building.
    build: true

    # Should people with build: false in permissions be allowed to use items?
    # Set true to disable using for those people.
    # Setting to false means EssentialsAntiBuild will never prevent you from using items.
    use: true

    # Should we tell people they are not allowed to build?
    warn-on-build-disallow: true

  # For which block types would you like to be alerted?
  # You can find a list of IDs in plugins/Essentials/items.csv after loading Essentials for the first time.
  # 10 = lava :: 11 = still lava :: 46 = TNT :: 327 = lava bucket
  alert:
    on-placement: 10,11,46,327
    on-use: 327
    on-break:

  blacklist:

    # Which blocks should people be prevented from placing?
    placement: 10,11,327

    # Which items should people be prevented from using?
    usage: 

    # Which blocks should people be prevented from breaking?
    break:

    # Which blocks should not be pushed by pistons?
    piston:

    # Which blocks should not be dispensed by dispensers
    dispenser:

############################################################
# +------------------------------------------------------+ #
# |            Essentials Spawn / New Players            | #
# +------------------------------------------------------+ #
############################################################

newbies:
  # Should we announce to the server when someone logs in for the first time?
  # If so, use this format, replacing {DISPLAYNAME} with the player name.
  # If not, set to ''
  #announce-format: ''
  announce-format: '&6&lSveikas(-a) {DISPLAYNAME} &6&latvykes i &a&lPowder.LT &6&lserveri pirma karta!'

  # When we spawn for the first time, which spawnpoint do we use?
  # Set to "none" if you want to use the spawn point of the world.
  spawnpoint: newbies

  # Do we want to give users anything on first join? Set to '' to disable
  # This kit will be given regardless of cost, and permissions.
  #kit: ''
  kit: Akcija

# Set this to lowest, if you want Multiverse to handle the respawning.
# Set this to high, if you want EssentialsSpawn to handle the respawning.
# Set this to highest, if you want to force EssentialsSpawn to handle the respawning.
respawn-listener-priority: high

# When users die, should they respawn at their first home or bed, instead of the spawnpoint?
respawn-at-home: false

# End of File <-- No seriously, you're done with configuration.
