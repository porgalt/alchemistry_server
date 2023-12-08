## These are just notes on my experience setting up the Antimatter Chemistry minecraft modpack.
I am using a Debian 12 server with default settings
I am joining the server on a windows device with the full modpack direct from curseforge every time

First, I installed the file onto my server

    wget https://mediafilez.forgecdn.net/files/4678/538/Antimatter-Chemistry-1.4.4-server.zip

Then i realised i didnt have java, so i installed it. But when i tried to install forge, it needed java 8, so i followed this proccess:

    sudo apt install -y wget apt-transport-https
    mkdir -p /etc/apt/keyrings
    wget -O https://packages.adoptium.net/artifactory/api/gpg/key/public | tee /etc/apt/keyrings/adoptium.asc
    echo "deb [signed-by=/etc/apt/keyrings/adoptium.asc] https://packages.adoptium.net/artifactory/deb $ (awk -F= '/^VERSION_CODENAME/ {print$2}' /etc/os-release) main" | tee /etc/apt/sources.list.d/adoptium.list
    sudo apt update
    apt install temurin-8-jdk

 # Mods:
 
### Forge with no mods:
 - accepted eula
 - turned on port forwarding for minecraft port 
 - works

### Alchemistry
 - doesnt work on its own
 - requires:
   - [ForgeLIN](#ForgeLIN)
   - [aLib](#aLib)
- with [ForgeLIN](#ForgeLIN) and [aLib](#aLib)
  - server seems to start
  - server starts, and is joinable

### aLib
  - starting with [Alchemistry](#Alchemistry) and [ForgeLIN](#ForgeLIN)

### AntiMatter Tweaks
  - server seems to start
  - server starts, and is joinable

### Apotheosis
  - doesnt work on its own
  - reqiures [Placebo](#Placebo)
  - with [Placebo](#Placebo)
    - server seems to start
    - server starts, and is joinable

### AppleCore
  - server seems to start
  - server starts, and is joinable

### AppleSkin
  - server seems to start
  - server starts, and is joinable

### Applied Energistics 2
  - server seems to start
  - server starts, and is joinable

### Atum
  - server seems to start
  - server starts, but i get error: internal exception java.io.ioexception connection was forcibly closed by remote host
  - updated JDK/java version on client
  - server is joinable

### Avaritia
  - does not work on its own
  - requires [Code Chicken Lib](#Code-Chicken-Lib)
  - with [Code Chicken Lib](#Code-Chicken-Lib)
    - server seems to start
    - server starts, and is joinable

### Avaritia Addons
  - does not work on its own
  - requires [Wanion Lib](#Wanion-Lib)
  - with [Wanion Lib](#Wanion-Lib)
    - server seems to start
    - server starts, and is joinable

### Bad Wither No Cookie Reloaded
  - mod appears to be client side from documentation, although minecraft version here is 1.12.2 and 1.18.2 is reqiured to not run the mod server side
  - server seems to start
  - server starts, and is joinable

### BaseLib
  - server seems to start, but is now much slower than it has been. my server isnt that powerful though so its not all that surprising.
  - once server was joined, it crashed due to a corrupted tile entity. it now will not start due to lack of memory. i will upgrade the server soon to counteract this

base-1.12.2-3.14.0.jar
Baubles-1.12-1.5.2.jar
BetterAdvancements-1.12.2-0.1.0.77.jar
BetterBuildersWands-1.12.2-0.13.2.271+5997513.jar
BetterFps-1.4.8.jar
blockcraftery-1.12.2-1.3.1.jar
bogosorter-1.2.8.jar
Bookshelf-1.12.2-2.3.590.jar
BrandonsCore-1.12.2-2.4.20.162-universal.jar
BuildingGadgets-2.8.4.jar
censoredasm5.14.jar
Chameleon-1.12-4.1.3.jar
ChestTransporter-1.12.2-2.8.8.jar
chiselsandbits-14.33.jar
Clumps-3.1.2.jar

### Code Chicken Lib
  - starting with [Avaritia](#Avaritia)

CodeChickenLib-1.12.2-3.2.3.358-universal.jar
CoFHCore-1.12.2-4.6.6.1-universal.jar
CoFHWorld-1.12.2-1.4.0.1-universal.jar
conarm-1.12.2-1.2.5.10.jar
ContentTweaker-1.12.2-4.10.0.jar
Controlling-3.0.12.2.jar
CraftingTweaks_1.12.2-9.0.1.jar
CraftTweaker2-1.12-4.1.20.690.jar
CropDusting-0.7-[1.12.2].jar
CTM-MC1.12.2-1.0.2.31.jar
CustomMainMenu-MC1.12.2-2.0.9.1.jar
DarkUtils-1.12.2-1.8.230.jar
deepmoblearning-1.12.2-2.5.4-universal.jar
DefaultOptions_1.12.2-9.2.8.jar
DefaultWorldGenerator-port-1.12-2.3.1.jar
denseneutroncollectors-1.1.jar
DimensionalEdibles-1.12.2-1.3.2.jar
DiscordCraft-2.0.jar
Draconic-Evolution-1.12.2-2.3.28.354-universal.jar
Earthworks-1.12-1.3.7.ED.jar
EnderStorage-1.12.2-2.4.9.jar
EqualDragons-1.1.jar
Exchangers-1.12.2-2.10.2.jar
ExtraBitManipulation-1.12.2-3.4.1.jar
ExtraCells-1.12.2-2.6.7.jar
extrautils2-1.12-1.9.9.jar
foamfix-0.10.15-1.12.2.jar
forbidden_arcanus-1.12.2-1.1.4.jar

### ForgeLIN
  - starting with [Alchemistry](#Alchemistry) and [aLib](#aLib)

FTBBackups-1.1.0.1.jar
FTBLib-5.4.7.2.jar
FTBQuests-1202.9.0.15.jar
FTBUtilities-5.4.1.131.jar
GameStages-1.12.2-2.0.123.jar
GunpowderLib-1.12.2-1.1.jar
HadEnoughItems_1.12.2-4.25.0.jar
Harvest-1.12-1.2.8-25.jar
incontrol-1.12-3.9.18.jar
industrialforegoing-1.12.2-1.12.13-237.jar
IntegrationForegoing-1.12.2-1.11.jar
ironchest-1.12.2-7.0.72.847.jar
ItemFilters-1.0.4.2.jar
jeiintegration_1.12.2-1.6.0.jar
journeymap-1.12.2-5.7.1.jar
JustEnoughResources-1.12.2-0.9.2.60.jar
lazy-ae2-1.12.2-1.1.26.jar
libnine-1.12.2-1.2.1.jar
Mantle-1.12-1.3.3.55.jar
mcjtylib-1.12-3.5.4.jar
memory_repo
modnametooltip_1.12.2-1.10.1.jar
modtweaker-4.0.20.11.jar
modularui-2.0.5.jar
moreoverlays-1.15.1-mc1.12.2.jar
mousetweaks-1.12.2-3.1.4.jar
mpbasic-1.12.2-1.4.11.jar
MPUtils-1.12.2-1.5.7.jar
MTLib-3.0.7.jar
mysticallib-1.12.2-1.13.0.jar
NC-ReactorBuilder-1.12.2-1.0.4b.jar
Neat1.4-17.jar
noautojump-1.12.2-1.jar
NotEnoughEnergistics-1.12.2-2.0.5-2.0.5.jar
NuclearCraft-2.18zzz-1.12.2.jar
oauth-1.06.4.jar
OpenBlocks-1.12.2-1.8.1.jar
OpenModsLib-1.12.2-0.12.2.jar
OreExcavation-1.4.150.jar
p455w0rdslib-1.12.2-2.3.161.jar
Patchouli-1.0-23.6.jar

### Placebo
  - starting with [Apotheosis](#Apotheosis)

ProjectIntelligence-1.12.2-1.0.9.28-universal.jar
randompatches-1.12.2-1.22.1.10.jar
rangedpumps-0.5.jar
RebornCore-1.12.2-3.19.5-universal.jar
RecipeStages-1.1.3.8.jar
RedstoneFlux-1.12-2.1.1.1-universal.jar
ResourceLoader-MC1.12.1-1.5.3.jar
rftools-1.12-7.73.jar
rftoolsdim-1.12-5.71.jar
serializationisbad-1.3.jar
SimplyJetpacks2-1.12.2-2.2.20.0.jar
Singularities-1.12.2-2.4.1.jar
Sledgehammer-1.12.2-2.0.23.jar
solcarrot-1.12.2-1.8.4.jar
spark-forge1122.jar
splashlogofix-1.0.jar
startuptimer-1.0.1.jar
StorageDrawers-1.12.2-5.5.0.jar
StructureUtils-1.1.0.4.jar
TConstruct-1.12.2-2.13.0.183.jar
tesla-core-lib-1.12.2-1.0.18.jar
theoneprobe-1.12-1.4.28.jar
ThermalDynamics-1.12.2-2.5.6.1-universal.jar
ThermalExpansion-1.12.2-5.5.7.1-universal.jar
ThermalFoundation-1.12.2-2.6.7.1-universal.jar
tieredmagnets-1.12.2-0.0.3.jar
TinkerToolLeveling-1.12.2-1.1.0.jar
tinyprogressions-1.12.2-3.3.34-Release.jar
tombstone-4.6.2-1.12.2.jar
UniDict-1.12.2-3.0.10.jar
UniversalTweaks-1.12.2-1.7.1.jar
voidislandcontrol-1.5.3.jar

### Wanion Lib
  - starting with [Avarita Addons](#Avarita-Addons)

WanionLib-1.12.2-2.91.jar
XenCraft-1.0.0.4.jar
xnet-1.12-1.8.2.jar
