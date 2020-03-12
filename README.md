-
# LeaderAssit
LUA project - World of Warcraft - Help leader and pug group to commnicate

 
**Objectif:** 
Creation of an addons assisting Raid leaders and MM+ groups. 
User case: 
Healers: 
- Automatically create rotation colddown base en the current heal setup 
- Automatically call for decast to the group (may need another addons like WA) 
- Decast 
- Automatically assign decast base on the current group setup 
- Automatically call for decast to the group (may need another addons like WA) 
- Optionnal:  
- Invitation calendrier : https://www.curseforge.com/wow/addons/iskar-assist 
- Je veux pouvoir programmer mes raids / MM+ utilisant les ranks de la guilde 
- Je veux pouvoir ajouter des personnes dans les invitations régulières (MM+ orientation) 
- Je veux pouvoir créer des invitations régulièrement automatiquement. 
- Je veux pouvoir savoir ce qui manque d’un coup d’oeil à lors d’une invitation 
- Gestion groupe de raid : https://www.curseforge.com/wow/addons/iskar-assist 
- Je veux pouvoir organiser mon groupe raid selon un parttern régulière initiale. 
- Je veux pouvoir customiser l’organisation de mon groupe de raid. 
- Je veux pouvoir changer le groupe de raid même si des membres sont en combat. 
 
Data needed: 
 - Healers Cd’s :  
 - List every Cd for every heal and assit heal CD’s (kind of data base) 

 
/*Database : 
Classe : 
Id 
Name https://wowwiki.fandom.com/wiki/Class 
Color https://wowwiki.fandom.com/wiki/Class_colors */
 
To do: 
 - Get interface infos : 
 - In wow : /run print((select(4,GetBuildInfo()))); 
 - Create a folder “LeaderAssit” and put in in the addon folder: 
 - Put the fil .toc and .lua in it 
 - Wow will look for .toc and inside we will call every part needed 
 - Even on login: 
 - Can say the version 
 - local EventFrame = CreateFrame("Frame") 
 - EventFrame:RegisterEvent("PLAYER_LOGIN") 
 - EventFrame:SetScript("OnEvent", function(self,event,...)  
     ChatFrame1:AddMessage('WhyHelloThar ".. UnitName("Player")) 
end) 
 - Fichier xml to import library 
 - embeds.xml 
 - Use this xml file to specify the locations of libraries that should be loaded (typically referencing the library's own XML file via Include). As an example, using LibStub and loading a pair of Ace3 libraries from a Libs subdirectory in the addon's folder: 
<Ui xsi:schemaLocation="http://www.blizzard.com/wow/ui/ ..\FrameXML\UI.xsd">  <Script file="Libs\LibStub\LibStub.lua"/>  <Include file="Libs\AceAddon-3.0\AceAddon-3.0.xml"/>  <Include file="Libs\AceConsole-3.0\AceConsole-3.0.xml"/></Ui> 
Additional libraries can be added by adding additional Include lines. You could also reference each library's xml file in your addon's .toc file instead, but embeds.xml helps make it clearer which parts of the code belong to the addon itself, and which are part of shared libraries. 
 
 **General:** 
Creation using notepad++ : https://notepad-plus-plus.org/download/v7.6.3.html 
Debug addons :  
https://www.curseforge.com/wow/addons/bugsack 
https://www.curseforge.com/wow/addons/bugsack 
Helper : 
https://www.mmo-champion.com/threads/817817-Creating-Your-Own-WoW-Addon 
https://www.wowhead.com/guide=1949/wow-addon-writing-guide-part-one-how-to-make-your-first-addon 
http://wowprogramming.com/ 
https://www.mmo-champion.com/threads/817817-Creating-Your-Own-WoW-Addon 
https://www.wowace.com/projects/ace3/pages/ace-db-3-0-tutorial to save varaibles ? 
https://www.wowace.com/projects/ace3/pages/ace-gui-3-0-tutorial to help create UI content 
