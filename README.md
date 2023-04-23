Download Link: https://assignmentchef.com/product/solved-2110215prog-midterm-1
<br>



<h1>1. Instruction</h1>

<ul>

 <li>Create Java Project named “<strong>2110215_Midterm_Q1</strong>”.</li>

 <li>Copy all folders in “<strong>zip</strong>” to your project directory src folder.</li>

</ul>

<h1>3) You are to implement the following classes (detail for each class is given in section 4)</h1>

<ol>

 <li><strong>Region          </strong>(package logic)</li>

 <li><strong>Database      </strong>(package logic)</li>

</ol>

4) <strong>JUnit for testing is in package test.grader</strong> <strong>5)</strong> <strong>To submit:  </strong>

<strong>5.1.</strong> <strong>go to src folder that you actually do the coding for this question.  </strong>

<strong>5.2.</strong> <strong>Zip this question’s src folder. Name it YOUR-ID_Q1.zip (for example, 6332112121_Q1.zip)  </strong>

<strong>5.3.</strong> <strong>Submit the zipped file as an assignment on MyCourseville.  </strong>




<h2>2. Problem Statement: CPQuest</h2>

<strong> </strong>

You are tasked to finish the backbone code for a “Quest” system for a game. The demo for the system (result from running Main in package main) is shown in section 6. But it is not necessary to know the demo to write the backbone code of the program.

<h2>3. Implementation Detail</h2>

The class package is summarized below.




<h1>Figure 1. Class Diagram</h1>

<strong>You must write java classes using UML diagram specified above.</strong>

<strong>* In the following class description, only details of IMPORTANT fields and methods are</strong><strong> given. * </strong>

<strong>4.1 Package logic </strong>

4.1.1 <strong>Enum Status:</strong> This enum contains the value that can be used to describe the status for the quest.

<strong>/*ALREADY PROVIDED*/</strong> <em>Values </em>

<table width="624">

 <tbody>

  <tr>

   <td width="217">Name</td>

   <td width="407">Description</td>

  </tr>

  <tr>

   <td width="217">AVAILABLE</td>

   <td width="407">This quest is available for everyone to take.</td>

  </tr>

  <tr>

   <td width="217">ACTIVE</td>

   <td width="407">This quest has been taken by someone and is in progress.</td>

  </tr>

  <tr>

   <td width="217">FINISHED</td>

   <td width="407">This quest has been finished.</td>

  </tr>

 </tbody>

</table>

4.1.2 <strong>Class Quest:</strong> This class represents the quest object, which will be used by Player and Region later. It contains the information about single quest.

<strong>/*ALREADY PROVIDED*/</strong>

<h2>Field</h2>

<table width="624">

 <tbody>

  <tr>

   <td width="217">Name</td>

   <td width="407">Description</td>

  </tr>

  <tr>

   <td width="217">– Player author</td>

   <td width="407">The author of the quest.</td>

  </tr>

  <tr>

   <td width="217">– Region region</td>

   <td width="407">The region the quest takes place in (can be different than the author’s home region)</td>

  </tr>

  <tr>

   <td width="217">– String name</td>

   <td width="407">The name of the quest.</td>

  </tr>

  <tr>

   <td width="217">– String description</td>

   <td width="407">The description of the quest.</td>

  </tr>

  <tr>

   <td width="217">– Status status</td>

   <td width="407">The current status of the quest.</td>

  </tr>

  <tr>

   <td width="217">– int rank</td>

   <td width="407">The rank of the quest.</td>

  </tr>

 </tbody>

</table>

<h2>       Constructor</h2>

<table width="624">

 <tbody>

  <tr>

   <td width="217">Name</td>

   <td width="407">Description</td>

  </tr>

  <tr>

   <td width="217">+ Quest(Player author, Region region, String name, String description)</td>

   <td width="407">Create a new Quest with the specified informations. Set the status to Status.AVAILABLE, and the rank to the author’s current rank.</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<h2>Method</h2>

<table width="624">

 <tbody>

  <tr>

   <td width="217">Name</td>

   <td width="407">Description</td>

  </tr>

  <tr>

   <td width="217">+ getter/setter for each field</td>

   <td width="407"></td>

  </tr>

 </tbody>

</table>










4.1.3 <strong>Class Player:</strong> This class represents a player. It contains player information and status.

<strong>/*ALREADY PROVIDED*/</strong>

<h2>         Field</h2>

<table width="624">

 <tbody>

  <tr>

   <td width="217">Name</td>

   <td width="407">Description</td>

  </tr>

  <tr>

   <td width="217">– String name</td>

   <td width="407">The name of the player.</td>

  </tr>

  <tr>

   <td width="217">– int score</td>

   <td width="407">The score of the player</td>

  </tr>

  <tr>

   <td width="217">– Quest currentQuest</td>

   <td width="407">The player’s current ongoing quest. This can be null if the player does not have ongoing quest.</td>

  </tr>

 </tbody>

</table>

<h2>       Constructor</h2>

<table width="624">

 <tbody>

  <tr>

   <td width="217">Name</td>

   <td width="407">Description</td>

  </tr>

  <tr>

   <td width="217">+ Player(String name)</td>

   <td width="407">Create a new Player with the specified name. Set the score to 0 and currentQuest to null.</td>

  </tr>

 </tbody>

</table>

<h2>Method</h2>

<table width="624">

 <tbody>

  <tr>

   <td width="217">Name</td>

   <td width="407">Description</td>

  </tr>

  <tr>

   <td width="217">+ void setName(String name)</td>

   <td width="407">Set the name of the Player.</td>

  </tr>

  <tr>

   <td width="217">+ void setScore(int score)</td>

   <td width="407">Set the score.</td>

  </tr>

  <tr>

   <td width="217">+ void addScore(int amount)</td>

   <td width="407">Adds the specified amount to the score.</td>

  </tr>

  <tr>

   <td width="217">+ int getRank()</td>

   <td width="407">Returns the rank of the player depending on their score.The rank is– 4 (score &gt; 10000)– 3 (7500 &lt; score &lt;= 10000)– 2 (5000 &lt; score &lt;= 7500)– 1 (2500 &lt; score &lt;= 5000)– 0 (score &lt;= 2500)</td>

  </tr>

  <tr>

   <td width="217">+ remaining getter/setter for each field</td>

   <td width="407">  </td>

  </tr>

 </tbody>

</table>




4.1.4 <strong>Class Region:</strong> This class represent a single region. It contains all data related to the region, including the quest list within the region. <strong>You must create this class from scratch</strong>.

<h2>         Field</h2>

<table width="624">

 <tbody>

  <tr>

   <td width="217">Name</td>

   <td width="407">Description</td>

  </tr>

  <tr>

   <td width="217">– String name</td>

   <td width="407">The name of the Region.</td>

  </tr>

  <tr>

   <td width="217">– ArrayList&lt;Player&gt; playerList</td>

   <td width="407">An ArrayList containing all Player in this Region.</td>

  </tr>

  <tr>

   <td width="217">– ArrayList&lt;Quest&gt; questList</td>

   <td width="407">An ArrayList containing all Quest in this Region.</td>

  </tr>

 </tbody>

</table>

<h2>       Constructor</h2>

<table width="624">

 <tbody>

  <tr>

   <td width="217">Name</td>

   <td width="407">Description</td>

  </tr>

  <tr>

   <td width="217">+ Region(String name)</td>

   <td width="407">Create a Region with the specified name.Initialized the ArrayList for both playerList and questList</td>

  </tr>

 </tbody>

</table>

<em> </em>

<h2>Method</h2>

<table width="624">

 <tbody>

  <tr>

   <td width="217">Name</td>

   <td width="407">Description</td>

  </tr>

  <tr>

   <td width="217">+ void setName(String name)</td>

   <td width="407">Set the name of the Region.If the name is blank (Can be checked using name.isBlank()), set it to “Nowhere”</td>

  </tr>

  <tr>

   <td width="217">+ int getPlayerCount()</td>

   <td width="407">Return the size of the playerList</td>

  </tr>

  <tr>

   <td width="217">+ double getRegionRank()</td>

   <td width="407">Return the average rank of all players in the region. (Continued next page)</td>

  </tr>

  <tr>

   <td width="217"></td>

   <td width="407"><strong>The average rank can be obtained by summation of the rank of every player in the region, then divide by the total numbers of the player in the region. <u>Please round the number to 2 decimal points</u> </strong></td>

  </tr>

  <tr>

   <td width="217">+ ArrayList&lt;Quest&gt; getAvailableQuests(Player viewer)</td>

   <td width="407">Return an ArrayList of all Quest in the region that have the status AVAILABLE.<strong>Do note that the viewer must not be able to view the quest that belongs to himself/herself. </strong></td>

  </tr>

  <tr>

   <td width="217">+ voidaddPlayerToRegion(Player p)</td>

   <td width="407">Add Player to the playerList</td>

  </tr>

  <tr>

   <td width="217">+ voidaddQuestToRegion(Quest q)</td>

   <td width="407">Add Quest to the questList</td>

  </tr>

  <tr>

   <td width="217">+ remaining getter/setter for each field</td>

   <td width="407"></td>

  </tr>

 </tbody>

</table>




4.1.5 <strong>Class DatabaseUtil:</strong> This class represents the utility function that has been partially implemented. It contains useful functions you can use to help implementing the Database.

<strong>/*ALREADY PROVIDED*/</strong>

<h2>Method</h2>

<table width="624">

 <tbody>

  <tr>

   <td width="311">Name</td>

   <td width="312">Description</td>

  </tr>

  <tr>

   <td width="311"><u>+ boolean isPlayerExists(ArrayList&lt;Player&gt;</u> <u>playerList, String name)</u></td>

   <td width="312">Return true if the Player with the given name already exists in the playerList.</td>

  </tr>

  <tr>

   <td width="311"><u>+ boolean isRegionExists(ArrayList&lt;Region&gt;</u> <u>regionList, String name)</u></td>

   <td width="312">Return true if the Region with the given name already exists in the regionList.</td>

  </tr>

 </tbody>

</table>




4.1.6 <strong>Class Database:</strong> This class represents the database. It contains all the frontend-backend communications, as well as the players and region list.

<strong>*For simplicity reasons for the Exam, we have used standard Exception here. In real-life scenario, please create a more specific exception for each scenario. * </strong>

<strong>You must create this class from scratch.</strong>

<h2>         Field</h2>

<table width="624">

 <tbody>

  <tr>

   <td width="209">Name</td>

   <td width="415">Description</td>

  </tr>

  <tr>

   <td width="209">– ArrayList&lt;Player&gt; playerList</td>

   <td width="415">An  ArrayList of Player.</td>

  </tr>

  <tr>

   <td width="209">– ArrayList&lt;Region&gt; regionList</td>

   <td width="415">An ArrayList of  Region.</td>

  </tr>

 </tbody>

</table>

<h2>Constructor</h2>

<table width="624">

 <tbody>

  <tr>

   <td width="209">Name</td>

   <td width="415">Description</td>

  </tr>

  <tr>

   <td width="209">+ Database()</td>

   <td width="415">Create a new Database object.Initialize playerList and regionList with empty ArrayList</td>

  </tr>

  <tr>

   <td width="209">+ Database(ArrayList&lt;Player&gt; playerList,ArrayList&lt;Region&gt; regionList)</td>

   <td width="415">Create a new Database object.Initialize playerList and regionList with the specified ArrayList</td>

  </tr>

 </tbody>

</table>

<h2>        Method</h2>

<table width="624">

 <tbody>

  <tr>

   <td width="239">Name</td>

   <td width="384">Description</td>

  </tr>

  <tr>

   <td width="239">+ Player addPlayer(String name,Region region) throws Exception</td>

   <td width="384">•      If the player with the given name does not exist, create a new Player object with the specified detail, then add it to the playerList. <u>Don’t forget</u> <u>to add the player into the region’s own player</u> <u>list using <strong>addPlayerToRegion</strong> from Region class</u>.•      Otherwise, throw an Exception.This method returns the newly created Player object.</td>

  </tr>

  <tr>

   <td width="239">+ boolean addRegion(String name)</td>

   <td width="384">If the region with the given name does not exist before, create a new Region object with specified detail, then add it to the list and <strong>return true</strong>.Otherwise, <strong>return false.</strong></td>

  </tr>

  <tr>

   <td width="239">+ Region getRegionByName(String name)</td>

   <td width="384">Return the Region object from the regionList with the specified name. If no region with the specified name exists, then return null.</td>

  </tr>

  <tr>

   <td width="239">+ void addQuest(Player author, Region region, String name, String description)</td>

   <td width="384">Create the Quest object with the specified detail, then add it into the specified region properly.<u>Hint:</u> Use addQuestToRegion from Region class.</td>

  </tr>

  <tr>

   <td width="239">+ getter/setter for each field</td>

   <td width="384"><strong> </strong></td>

  </tr>

 </tbody>

</table>

<strong>4.2 Package main </strong>

4.2.1 Class Main: This class is the main application. It contains methods required to run the app, as well as the main method. You can run this class to test the application. <strong>/*ALREADY PROVIDED */</strong> 4. Score Criteria

The maximum score for the problem is 20 and will be rounded down to 5.

<table width="370">

 <tbody>

  <tr>

   <td width="240"><strong>5.1 Class Region (RegionTest): </strong></td>

   <td width="48"><strong> </strong></td>

   <td colspan="2" width="82"><strong>= 12 points </strong></td>

  </tr>

  <tr>

   <td width="240">          testConstructor</td>

   <td width="48"></td>

   <td colspan="2" width="82">= 1 points</td>

  </tr>

  <tr>

   <td width="240">testConstructorEmpty</td>

   <td width="48"></td>

   <td colspan="2" width="82">= 1 point</td>

  </tr>

  <tr>

   <td width="240">           testSetName</td>

   <td width="48"></td>

   <td colspan="2" width="82">= 1 points</td>

  </tr>

  <tr>

   <td width="240">         testSetNameEmpty</td>

   <td width="48"></td>

   <td colspan="2" width="82">= 1 points</td>

  </tr>

  <tr>

   <td width="240">testAddPlayerToRegion</td>

   <td width="48"></td>

   <td colspan="2" width="82">= 1 points</td>

  </tr>

  <tr>

   <td width="240">testAddQuestToRegion</td>

   <td width="48"></td>

   <td colspan="2" width="82">= 1 points</td>

  </tr>

  <tr>

   <td width="240">         testGetPlayerCount</td>

   <td width="48"></td>

   <td colspan="2" width="82">= 1 points</td>

  </tr>

  <tr>

   <td colspan="2" width="288">        testGetRegionRank</td>

   <td width="74">= 2 points</td>

   <td width="8"></td>

  </tr>

  <tr>

   <td colspan="2" width="288">       testGetAvailableQuests</td>

   <td width="74">= 3 points</td>

   <td width="8"></td>

  </tr>

  <tr>

   <td colspan="2" width="288"><strong>5.2 Class Database (DatabaseTest):  </strong></td>

   <td width="74"><strong>= 8 points </strong></td>

   <td width="8"></td>

  </tr>

  <tr>

   <td colspan="2" width="288">           testAddPlayer</td>

   <td width="74">= 1 points</td>

   <td width="8"></td>

  </tr>

  <tr>

   <td colspan="2" width="288">        testAddPlayerRepeat</td>

   <td width="74">= 1 points</td>

   <td width="8"></td>

  </tr>

  <tr>

   <td colspan="2" width="288">          testAddRegion</td>

   <td width="74">= 1 points</td>

   <td width="8"></td>

  </tr>

  <tr>

   <td colspan="2" width="288">        testAddRegionRepeat</td>

   <td width="74">= 1 points</td>

   <td width="8"></td>

  </tr>

  <tr>

   <td colspan="2" width="288">           testAddQuest</td>

   <td width="74">= 2 points</td>

   <td width="8"></td>

  </tr>

  <tr>

   <td colspan="2" width="288">          testGetPlayerList</td>

   <td width="74">= 1 points</td>

   <td width="8"></td>

  </tr>

  <tr>

   <td colspan="2" width="288">         testGetRegionList</td>

   <td width="74">= 1 points</td>

   <td width="8"></td>

  </tr>

 </tbody>

</table>

<h3>5. Program Demonstration</h3>

Figure 2: The Initial Screen

First off, as a guest. You can either log in or viewing the statistic. Once you logged in, you will have more options to work with. We will cover the statistics option later.

Once you picked the log in option, you will be presented with the current user list in the system, or you can choose to make the new one. Do note that the new username cannot be the same as the one in the database. If it happened, the system would alert the user.




<h1>Figure 3: Registering new player</h1>

Once you logged in, the start menu changed, and you can access more option.




<h1>Figure 4: New Start Menu once logged in</h1>

For the first option, you can edit your own username, do note that the same restriction as when registering new player applies.




<h1>           Figure 5. Submenu for editing username</h1>

The next option is “Take On a Quest”. You can take on a quest using this option. The system will prompt you to pick the region and will display the current available quest in that region.




<h1>Figure 6. Take On a Quest</h1>

Do note that this option will be changed to Manage Quest Status instead when you have taken a quest. With Manage Quest Status menu, you can mark the quest as finished or decline the quest. By marking the quest as finished, you will obtain the score reward from the quest equal to the quest’s rank. <sub> </sub>




<h1>Figure 7. Manage Quest Status</h1>

The third option is for posting your own quest. Everything here should be selfexplanatory.




<h1>Figure 8. Posting Quest Option</h1>

Finally, the last option is for viewing the status of the region. It displays the player count and average rank of the players in the region.




<h1>Figure 9. Viewing Region Status</h1>


