### Design Decisions Document for 3D Scene Project

**Overview:**  
This project involved creating low-polygon 3D models, applying textures, setting up lighting, and adding interactive camera controls, all implemented using OpenGL and C++.

---

**3D Objects:**

**Turtle Design:**

- **Construction:**  
  The turtle model was honestly quite a bit of a happy accident. It started as an attempt to create a mountain using a series of pyramid shapes, but it ended up looking more like a turtle’s shell. So after all the failed efforts to import .obj and .mtl files, I absolutely failed to hesitate in the slightest and decided to run the accidental turtle shell and layout I now had with the shapes from `ShapeMeshes.cpp` After I had the shell where I wanted it, I then went on adding a sphere for the turtles body and another sphere I ended up dedicating specifically for the head. Originally, the head was made using a cone mesh, and was to be a fish model, but after the shell was rendered, I ended up using the fish models sphere shape and put it where the turtles head would naturally sit. In the end, the whole model was brought together with massive amounts of trial and error. I then went on adding shading and unique forms of texture that would really give the red eared slider a natural turtle look and make it stand out. I also did the same thing for the tree, using grass and bark as the texture.
  
- **Textures:**  
For the textures, I used royalty-free images to give the turtle’s body and head a realistic look, keeping quality and not forfeiting any need to have to worry about copyrights. I also made sure the textures blended smoothly across the different parts of the model.

---

**Tree Design:**

- **Trunk and Foliage:**  
  The tree’s trunk was made using a box mesh, and the foliage was created with a cone mesh. I applied a bark texture to the trunk to make it look like wood, while the foliage was textured to resemble grass. I also used a green shader for the leaves to give them a natural look, though they turned out a bit darker than Iinitially wanted due to the shading settings.

---

**Aquarium Glass and Water:**

- **Construction:**  
  The aquarium I designed is made up of two parts: the glass at the top and the glassy-water below and I constructed both halves using box meshes. I applied a "blue-glass" texture to the glass part, giving it a semi-transparent, and slightly reflective appearance. For the water half, I used a similar texture but adjusted the transparency and colored in the blue more to make it distinct from the glass.
  
- **Materials:**  
  I used different materials to achieve the right look for both the glass and the water. The glass was made more transparent and shiny, while the water was given a tile material creating a subtle ripple effect.

---

**Lighting:**

- **Setup:**  
  I used several light sources to make sure that the scene was well-lit from different angles. A main point light simulated the sunlight, while a directional light added overall brightness. I used the `Phong shading model` to balance the different lighting effects which helped to make the scene look realistic and like an actual aquarium.
  
- **Rationale:**
  Good lighting was an important factor in order to make the textures and shapes stand out. This was especially true for the aquariums glass and water, where the areas reflections and levels of transparency all played an important part in keeping the scene to look realistic.

---

**Navigation:**

- **Camera Controls:**  
  I added interactive camera controls so that users can move around the scene by using the `WASD` and `QE` keys, while being able to also adjust their view with the mouse and the speed via the mouses scroll. These controls were designed to make it easier on the user to be able to explore the scene in detail from different angles.
  
- **Display Modes:**  
  Users can switch between orthographic and perspective views, which is useful for both development and presentation.

---

**Best Practices:**

- **Modularity:**  
  I kept the code modular, with specific functions for tasks like setting up textures, applying materials, and transforming objects. This made the code easier to manage and debug, while also keeping possible and easy to reuse parts of the code across the project.
  
- **Commenting:**  
  The code includes clear comments that explain what each part does, making it easier to understand the logic and handle future updates.

---

**Reflection on Development Choices:**

- **Object Selection:**  
  I chose to include a turtle, tree, and aquarium elements like a filter to craft a simple yet visually appealing scene. The turtle's unexpected design led to creative choices that not only enhanced the final render but also contributed to the overall vibe with the color selection.
  
- **Functionality:**  
  I used custom functions for handling textures, materials, and transformations, which helped keep the code organized and made it easier to make edits whenever I needed to add something.

---

**Conclusion:**  
  These were the reasons behind my design decisions. I mainly focused on creating a solid structure and foundation for a program that’s visually appealing both in the code and in the final render of the interactive 3D scene. My goal was to make sure that the final model met all of the expectations while still adhering to industry best practices, resulting in a solid foundation for the render of my turtle tank. I also tried to keep everthing in this project as simple and straightforward as possible, to be able to make it an easy experience for the user to navigate or the next developer to easily hop in the code and add better methods of lighting or adapt the objects in the scene.

---