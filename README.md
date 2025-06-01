# ModularPlanting
A little tutorial for modifying stls, specifically for a modular planter

Quick note, this walk through is simply how I went about it wiht a specific software. This is in no way an ABSOLUTE how to, because there are a hundreds of softwares plus millions of ways to do the same thing within each software

### Goal and Attribution
Theis is the source for the models that need to be modified:
- [https://www.printables.com/model/669456-modular-hydroponic-tower-garden/files](https://www.printables.com/model/669456-modular-hydroponic-tower-garden/files) (specifically, the 3-Way_Planting_Module.STEP and the 3-Way_Planting_Module_Hollow.STEP)

this is the model that has a couple features we want on the above models
- [https://www.thingiverse.com/thing:2403922](https://www.thingiverse.com/thing:2403922/files) (specifically, the Module.stl)

Always remember to check licenses, both of these each allow remixing as long as proper attribution is always accreddited, and as long as there is no commercial use. So basically, dont sell it, and dont claim it as your own.

# Importing Alternate Model
since im using f360, and since the thingiverse model doesnt give us nice modifyable step or f3d files, i will start a direct modeling project (i do not recomend using parametric timeline modelling when editing a mesh of any type, including STL), import it as mesh, and use mesh convert into body

![001 Failed](./assets/001.PNG)

![002 Failed](./assets/002.png)

![003 Failed](./assets/003.png)

### Getting Dimension From Alternate Model
we want to get the internal dimension of one of these spouts, because this is the feature we want to overwrite onto the other models. to do this, create a sketch on one of the edge triangles. the make a circle with two points constrained to the two inside points of this triangle. now you can estimate how big the circle needs to be. you can use the measure tool to get the final dimension. I rounded it to 52.7mm

![004 Failed](./assets/004.png)

![005 Failed](./assets/005.png)

### Opening Desired models
this maker supplies both step and stl files. stl is a mesh, made of triangles. step is a bit more unique, and made of bodies. bodies are far easier to remix, so we will use these files. however, f360 has no easy way to "import" step files into an existing project. instead, they must be opened as a new project with no parametic timeline (sad)

![006 Failed](./assets/006.png)

small tip: if paramaetic timeline modelling is important to you, you can then save the step file as an f360 project, then import it as a compnonent into an existing project with the timeline enabled, then simply unlink the component, and edit it to your hearts content :D

if that made no sense, heres a youtube video about it: [https://www.youtube.com/watch?v=0IISPGwFQ0A](https://www.youtube.com/watch?v=0IISPGwFQ0A)

### Applying Dimension From Alternate Model To Desired Models
Zooming in, there is a flat edge we can use for our sketch profile. after creating a sketch profile on this plane, add a circle to the center and use the concentric constraint to center it to the edge we used for the sketch profile (or as a shortcut, let f360 apply this constraint for you by letting it snap to the visual center, as shown below) and apply the dimension we grabbed form the alternate model to this circle (52.7mm) and finish the sketch. do this for all 3 spouts, on both models

![007 Failed](./assets/007.png)

![008 Failed](./assets/008.png)

![009 Failed](./assets/009.png)

### Creating Spout From Sketch
after finishing the sketch, extrude your new sketch profile AND the outer edge (this will be useful later) long enough that all edges are fully inside the inner tube of the model (-80mm) MAKE SURE ITS A NEW BODY and do this for all 3 spouts, on both models

![010 Failed](./assets/010.png)

![011 Failed](./assets/011.png)

### Split The New Bodies
use the inner tube as a plane to cut the new bodies you just made, then select the bodies inside the tube and remove them do this for all 3 bodies on both models

![012 Failed](./assets/012.png)

![013 Failed](./assets/013.png)

![014 Failed](./assets/014.png)

### Join The Leftover Bodies
combine the leftover bodies with the main object, do this for both models

![015 Failed](./assets/015.png)

### Add Fillets (OPTIONAL)
zooming in, you can see there used to be an internal fillet to round out the edge. add a fillet if so desired. zooming in, you can also see that a 3mm fillet is not enough to cover a slight surface indent, this indent is from the previous fillet. the indent would have been alot bigger if the edge was not selected in the much earlier extrude step! a fillet of 4mm completly covers it

![016 Failed](./assets/016.png)

![017 Failed](./assets/017.png)

![018 Failed](./assets/018.png)

![019 Failed](./assets/019.png)
