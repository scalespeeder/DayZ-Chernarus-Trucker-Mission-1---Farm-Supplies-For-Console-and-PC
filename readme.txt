DayZ Chernarus "Trucker Mission 1 - Farm Supplies" For Console and PC json Custom Spawner Mod Instructions & Terms Of Use

This custom object spawner json file will spawn in Garden Lime Compost, Seeds & Garden Hoes in trucks in the traffic jam in the South West of Chernarus, at 894.32 / 1981.51,
and a "Experimental Farm" (a military tent!) at 6796.86 / 15108.62.

Also included in the Github repository is a map of locations for the mission, and screenshots of those locations too. (Plus the .dze for customisation in the DayZ Editor Mod.)

Limited Testing on PC Chernarus Local Server DAYZ Version 1.20 Mar 2023.

Created by @scalespeeder. Please report bugs & errors to scalespeeder@gmail.com with screenshots.

Many Thanks To Inclement Dab for his amazing DayZ Editor that makes this all possible: https://steamcommunity.com/sharedfiles/filedetails/?id=2250764298

TERMS OF USE
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS
OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN
AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH
THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Using these modded xml / json files and instructions could break the functioning of your DAYZ server, requiring a reinstall that would wipe
all player progress.

Using these modded files neccessitates increased regular restarts to prevent server crashing.

It is suggested you thoroughly test your server after applying these files to ensure proper
functioning of your server.

I always recomend you validate your files at: https://www.xmlvalidation.com/ and https://jsonformatter.curiousconcept.com/

There are three parts to implementing this mission: Spawning the items, informing your community, then removing it all when you're done.

I recommend you read all the instructions before proceeding.

--------------------------

Instructions To Spawn Supplies & "Experimental Farm":

Click the "Code" button and "Download Zip" on the Github Repository and extract the files on your local PC for access.

(Optional: For advanced users I have included the original DayZ Editor Mod file "tm1-editor-file.dze" which can be imported into DayZ Editor Mod on PC for customisation.)

Ensure your DayZ Server has activated the cfggameplay.json. For console users on Nitrado Servers, go to "General Settings" on your server and tick "Enable cfggameplay.json".

On PC Servers add the following line to your serverDZ.cfg:

enableCfgGameplayFile = 1;

(On some PC servers, including Nitrado, the serverDZ.cfg is "hidden", so you need to enable "expert mode" in settings,
then go to "expert settings", which is the serverDZ.cfg. Stop the server before making changes this way.)

Upload "truck-mission-1-farming-supplies.json" from the extracted files to inside the "custom" folder of the mission directory on your server. This file places the tent and items on your map.
(If you haven't got a "custom" folder, create one.)

Open the cfggameplay.json file in the correct mission file for your server and look for the "objectSpawnersArr" line.

This file tells your server to access your custom file.

Edit it to look like this: 

	"objectSpawnersArr": ["custom/truck-mission-1-farming-supplies.json"],
	
If you already are calling custom jsons to spawn items, seperate the files like this:

	"objectSpawnersArr": ["custom/truck-mission-1-farming-supplies.json","custom/anotherfile.json","custom/differentfile.json"],
	
Save your changes & upload if you need to.

Restart your server and the suppliers & farm will appear immediatly. 

-----------------------

Now it's time to inform your community of the available mission - to find the lime, seeds and tools, then take some to the experimental farm and use the rest to supply the shops
detailed on the included map.

In my discord for example, I posted this:

Transport Truck Mission Available: Scouts have spotted a large quantity of Garden Lime Compost, Tools & Seeds amongst the remains of a traffic queue in the South Western
Corner of Chernarus. We could make good use of these resources, so volunteers are required to move some of the goods to an experimental farm in the North, with the rest
being distributed around village shops. See the supplied map and photos for details. (Post screen-shots below to show delivered goods.) Good luck survivors!

(Then I posted the included map and photos)

----------------------


After the mission has finished, probably about a week, remove the entry from the "objectSpawnersArr" line,

so it looks like 

"objectSpawnersArr": [""],

or

"objectSpawnersArr": ["custom/anotherfile.json","custom/differentfile.json"],

Then save and restart your server so that the resources and the farm despawn.

-------------------------

Thanks, Rob.
