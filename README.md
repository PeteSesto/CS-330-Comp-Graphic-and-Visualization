# CS-330 Journal: Final Project Reflection

### How Do I Approach Designing Software?

When designing software, I approach the problem by breaking a complex end goal into smaller, manageable building blocks. For this 3D scene, my design process started with a close study of the reference photograph to analyze how natural and structural shapes interact. Instead of trying to build the entire garden as a single complex model, I broke the scene down into basic geometric shapes like cylinders, tapered cones, spheres, toruses, boxes, and planes. From there, I mapped out a unified coordinate system so every object would scale and align naturally in 3D space.

Working through this project helped me develop stronger architectural skills, especially in separating visual appearance from underlying geometry. By creating dedicated functions like `SetTransformations`, `SetShaderMaterial`, and `SetTextureUVScale`, I was able to encapsulate matrix math and shader uniform updates. This kept the main rendering logic clean and readable. In future software projects, I will continue using this top-down decomposition strategy. Breaking down large systems into decoupled, testable components prevents code clutter and makes it much easier to update individual features without breaking the rest of the application.

---

### How Do I Approach Developing Programs?

My approach to developing programs centers on continuous testing, iterative adjustments, and immediate visual feedback. When working in OpenGL, small mistakes in matrix calculations or shader states can cause entire objects to disappear or textures to blow out. To manage this, my development strategy focused on adding one feature at a time, verifying its behavior, and refining it before moving forward.

Iteration played a major role in solving several technical hurdles during development. For example, when applying textures to the long entry hedges, stretching a single box across the full path created distorted stripes on the top face. By testing different approaches, I replaced the single stretched mesh with a modular loop that renders six nearly cubic box segments along the Z axis. This solved the texture distortion while keeping the code compact. Similarly, configuring the Phong lighting model required multiple iterations to balance the key sunlight, overhead fill, and ambient floor. This fine-tuning eliminated washed-out surfaces while keeping the inner ring hedge from dropping into pitch black shadows. Over the course of the milestones, my code evolved from simple hardcoded draw calls into a clean, object-oriented framework that separates rendering, camera math, and window management across dedicated classes.

---

### How Can Computer Science Help Me in Reaching My Goals?

Studying computational graphics provides a practical bridge between abstract computer science theory and high-performance software engineering. On an educational level, working directly with OpenGL has given me a deep, hands-on understanding of linear algebra, 3D coordinate transformations, and GPU shader execution. Seeing how model, view, and projection matrices work together in real time makes mathematical concepts concrete and prepares me for advanced coursework in computer architecture and simulation.

Professionally, the problem-solving discipline required for graphics programming applies directly to building fast, reliable software. Managing real-time render loops, handling user peripheral inputs with GLFW, and managing GPU memory cleanup are essential skills across many software domains. Whether developing interactive user interfaces, optimization tools, or graphics-driven applications, the technical foundation and systematic debugging habits I built in this course will help me write cleaner, more efficient software throughout my career.
