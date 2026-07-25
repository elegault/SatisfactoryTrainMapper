# Routing And Signalling II (Redux)

## Connecting Railway Sections

- Rails snap together at their endpoints when placed close and aligned; you can also build junctions/switches by connecting multiple track segments to a single joint.
- Trains follow the physical path of connected track — they cannot dynamically re-route in the middle of a segment, so the layout of connections determines the routing options available at each junction.
- Signals can be built directly on track joints and will automatically snap to them, or built freely along a track segment as long as they're at least 12m from the end — this splits the segment to create a new joint.
- The forward direction of a signal is set by which side of the joint you target, and an arrow shows the direction. Signals are directional — trains can't move against that direction — so for bi-directional railways you need signals facing both ways.

## Block Signals

- Block Signals divide the railway into "blocks"; while a train occupies a block, no other train can enter it.
- The space between two signals placed on the same side of the track is a "segment" (block), and the game randomly colors each segment so you can see its boundaries when holding a signal in the build gun.
- Only one train can be in a block at a time — if it's occupied, following trains wait at the signal until the lead train exits. A long stretch of track with no signals in between counts as one block, so other trains must wait for the whole stretch to clear.
- Rule of thumb from players: make blocks roughly the length of a train, and add more, shorter blocks to fit more trains on the same stretch of track. With signals only at each station on a loop, you effectively create one block per station-to-station stretch — e.g., 2 stations means 4 blocks, so a 3rd train can be added before the loop saturates.

## Path Signals

- Path Signals are advanced signals especially useful for bi-directional railways and complex intersections. They work like Block Signals, but instead of reserving the whole block, a train reserves a specific path through it and will only enter if it can fully pass through.
- A path signal effectively looks ahead to the next signal down the line — so placing one before a junction means a train won't enter the junction unless it can get all the way through it, avoiding trains that block an intersection while waiting.
- Common guidance: use Block Signals for simple stretches of track, and reserve Path Signals for junctions, switches, and intersections. Most track only needs block signals — path signals are generally only needed where you have switch rails or intersections.
- It's almost never a good idea to chain two path signals one after another — this can create pathing/deadlock issues.
- A recommended setup for intersections: place Block Signals at each exit of the intersection, then Path Signals at each entry, so entering trains reserve a full path through before committing.
- If a player manually drives a train onto a Path Signal, the whole block is treated as occupied — the Path Signal effectively behaves like a Block Signal and blocks automated trains from entering.

**Practical rule of thumb:** block signals prevent two trains from colliding on straight/simple track by locking one train per block; path signals prevent a train from entering a junction it can't fully clear, which is critical wherever routes cross or merge. Most networks use mostly block signals with path signals concentrated at intersections and station throats.
