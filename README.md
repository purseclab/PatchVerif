# PatchVerif

## Download a virtual machine image
*The virtual machine includes source code of PatchVerif.* <br>

The image is created on VMware Workstation Player

Download <a href="https://purdue0-my.sharepoint.com/:u:/g/personal/kim2956_purdue_edu/EV1WfJvUrL1GnCfzQackHe8BJS25qPhSKoKahAEtdiL7AA?e=JwNdvA">the virtual machine image</a>

OS: Ubuntu 20.04 <br>
User name: Ubuntu-20-04 <br>
password: patchverif <br>

### Execute PatchVerif
```
cd regression/
python2 main.py
```

### Monitor the progress
```
cd ~/Downloads/
./QGroundControl.AppImage
```

## Bugs discovered by PatchVerif
If you want to closely look into bugs discovered by PatchVerif, please review the below documentation.
<a href="https://docs.google.com/spreadsheets/d/1nQhRz0iBTVufcCODja9ppppycSP4fNtPbTJnFY7lnMw/edit?usp=sharing" target="_blank"> <img align="center" width="820"  src="https://github.com/purseclab/PatchVerif/blob/main/Bugs_discovered_by_PatchVerif.png"> </a>

## Demonstration videos
### Case 1
<a href="https://youtu.be/TWK5lFPlLB4" target="_blank"> <img align="center" width="820"  src="https://github.com/purseclab/PatchVerif/blob/main/demo_pivot_turn.png"> </a>

<br><b>Question</b>: Why is this behavior a logic bug? <br>
<b>Answer</b>: ArduPilot supports a pivot turn for ground vehicles (rovers). When a vehicle is near a corner, it decreases its speed, turns towards the next waypoint, and continues the navigation. Yet, a faulty patch makes the vehicle fail to decrease its ground speed even if it is near the corner. As a result, the vehicle deviates from the planned navigation path due to the high speed at the corner.


### Case 2
<a href="https://youtu.be/htnWzS4hoCs" target="_blank"> <img align="center" width="820"  src="https://github.com/purseclab/PatchVerif/blob/main/demo_Dijkstra.png"> </a>

<br> <b>Question</b>: Why is this behavior a logic bug? <br>
<b>Answer</b>: The object avoidance with Dijkstra keeps failing to find a path when the rover is near a circular-shaped object (fence).
