

# Script HLD.  
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

# Todo before mvp
- script editor
  -  view by user by round
  -  determine if we want to keep the room template concept
  -  "Depends on" items.  Need a way to add item if task completed or item is traded
  -  player bio in editor
  -  Create Room, copy existing 
-  Move images to supabase
  -  In editor, drop down for public images, upload for new
-  Map Editor
  -  User add clues/tasks and drags pins
-  Player Bio
-  Known players (with Star and additional text)
-  Injured Timer & Dead state, can't see anything in app
-  num goals complete view
  - with round timer and red/green
  - modify game piece to allow "complete"

later todos
- move script import to an endpoing
  - Use a pgsql transaction
- create Round page that shows round, description and queue of DM things (fight, etc)
- In script, add items & money.
- In script, add items that are distributed by dm
- In script, add optional players.  Add depends on player to story_pieces
- Move script images to buckets
- Optional players
  - Add optional to player description
  - Add ordinal for optional players
  - What about groups of new players? Maybe make the DM select those in CreateRoom? 


# bug
- fix Kalama Kate secrets and clues
- other 
