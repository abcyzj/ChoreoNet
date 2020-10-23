# ChoreoNet

## Dataset

The whole dataset consists of three parts:

- Choreography
- Music
- Motion Capture Data

### Choreography

There are four files in the `data/choreography` directory, corresponding to four different types of dances: Cha-cha, Rumba, Tango and Waltz.

Each file consists an array of choreography objects, and each object has the following attributes:
1. name: the name of the current dance
2. dance_type: one of the four dance types that this dance belongs to.
3. dance_id: the id of this dance.
4. start_pos: the start music frame number of this dance, the FPS is 25. The first CAU starts at this frame.
5. end_pos: the end music frame number of this dance, the FPS is 25. The last CAU ends at this frame.
6. movements: the CAU sequence of this dance.
7. durations: the number of beats of each CAU in this dance.

### Music

The corresponding music of each dance. For example, if the type of this dance is Cha-cha and its `dance_id` is 1, its music is `data/music/C/1.mp3`.

### Motion Capture Data

`data/movement_interval.csv` records the motion capture clip of each CAU. The `movement_tag` attribute is the name of the CAU, and its motion capture clip is in the file denoted by `c3d_file` attribute, and the motion capture clip starts at `start_frame` and ends at `end_frame`. The c3d file is located in `data/raw_c3d` directory.
