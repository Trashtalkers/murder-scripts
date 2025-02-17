Verify for signal that you get the udpated row.


Script HLD.  
- Events for room, round, story
- For room, use presence.  On join, it should pull all story_pieces if started. This should fix people leaving, returning and state is wrong
- on start, ScriptBegin, which parses script and updates the database.  It then signals rounds with null, which means pull script
-  Round is only signaled by DM.  This updates started_on and completed_on
  -  On start, pull all stories for   
-  Story signals changing to story_pieces.
  -   Information revealed by DM (shows up for all)
  -   revelation completed_on
  -   task completed_on
  -   item new player_id


- add scripts to database
- Copy auth from scaffold
- build murder page for tablet and mobile
- on new round, pop-up for new items.
- DM page with all things, and drop down for individual players

later todos
- move script import to an endpoing
  - Use a pgsql transaction
- create Round page that shows round, description and queue of DM things (fight, etc)
- In script, add items & money.
- In script, add items that are distributed by dm
- In script, add optional players.  Add depends on player to story_pieces
- Optional players
  - Add optional to player description
  - Add ordinal for optional players
  - What about groups of new players? Maybe make the DM select those in CreateRoom? 
