# predict-student-performance

#Columns
|カラム|説明|説明2|
|session_id| the ID of the session the event took place in|
|index| the index of the event for the session|
|elapsed_time| - how much time has passed (in milliseconds) between the start of the session and when the event was recorded
event_name - the name of the event type|
|name| - the event name (e.g. identifies whether a notebook_click is is opening or closing the notebook)|
|level| - what level of the game the event occurred in (0 to 22)|
|page| - the page number of the event (only for notebook-related events)|
|room_coor_x| - the coordinates of the click in reference to the in-game room (only for click events)|
|room_coor_y|- the coordinates of the click in reference to the in-game room (only for click events)|
|screen_coor_x| - the coordinates of the click in reference to the player’s screen (only for click events)|
|screen_coor_y| - the coordinates of the click in reference to the player’s screen (only for click events)|
|hover_duration| - how long (in milliseconds) the hover happened for (only for hover events)|
|text| - the text the player sees during this event|
|fqid| - the fully qualified ID of the event|
|room_fqid| - the fully qualified ID of the room the event took place in|
|text_fqid| - the fully qualified ID of the|
|fullscreen| - whether the player is in fullscreen mode|
|hq| - whether the game is in high-quality|
|music| - whether the game music is on or off|
|level_group| - which group of levels - and group of questions - this row belongs to (0-4, 5-12, 13-22)|
