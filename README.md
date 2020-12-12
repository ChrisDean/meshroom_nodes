# Meshroom Nodes
A collection of meshroom photogrammetry nodes that might be useful to others


## OldTexturing.py
A copy of the standard meshroom 2020.1.1 Texturing node modified to use 
an older (working) release version of alicevision for LSCM and ABF unwrapping
as a workaround for the bug related to this in the Meshroom 2020.1.1 release.

While developers might be able to work around this bug easily this
node hopefully provides a simple solution for non-developers.

### Usage
Assuming you already have 2020.1.1 or 2020.1.0 already installed

1. Download and extract a seperate copy of Meshroom 2019.2.0
2. Copy the OldTexturing.py node file into your Meshroom-2020.1.1/lib/meshroom/nodes/aliceVision/ folder
3. Open the node file in a text editor and change this line to reflect wherever you just extracted 2019.2.0 to 

(I'm using windows here and have mine in D:/meshroom/Meshroom-2019.2.0/)

(This also works for linux just remember to remove the .exe extension also)

```
commandLine = r'D:/meshroom/Meshroom-2019.2.0/aliceVision/bin/aliceVision_texturing.exe {allParams}'
```

4. Save the file
5. Open your meshroom project and replace your current texturing node with the new "OldTexturing" node that should now 
   appear in the node list
6. Run

Your workflow should compute as normal but step back to the working version 
of the alicevision_texturing bundled in the 2019.2.0 release for 
the texturing step.

Of course you can also modify this to work with any version of the 
alicevision_texturing sub-program that works (you don't have to use 
the old one from 2019.2.0) but given the 2019.2.0 version is a release 
version that works, this is an easier temporary than say building Alicevision 
from scratch.
