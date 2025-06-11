# Three.js Maze Generation Benchmark 🌐
Explore and compare the capabilities of large language models (LLMs) in generating mazes using Three.js.

[Check out the live 3D mazes here!](https://louispaulet.github.io/maze_benchmark/index.html)

## Objective 🎯
Our goal is to create a visually engaging, interactive 3D maze in a web browser environment. Here's what we are aiming for:
- **Maze Generation**: Utilize the recursive backtracking algorithm for maze generation.
- **3D Visualization**: Implement the maze in 3D using Three.js, allowing full interaction.
- **Interactivity**: Users should be able to navigate and inspect the maze thoroughly using mouse controls.
- **Aesthetics**: The maze should feature distinct wall and floor colors, differing from the background to enhance visibility.

Currently, GPT-4 outperforms other models, establishing the `gpt4_maze.html` as the benchmark standard. Other models are challenged to surpass this in their respective `<LLM>_version.html` files.

## Benchmark Rules 📏

1. **Standard Prompt**: All LLMs will begin with this uniform prompt:
`````
Please make a simple HTML page that contains a JS code to generate a maze (30x30 blocks).  
Use recursive backtracking algorithm.
The user can use his mouse click to rotate the scene.
The camera should be placed above the center of the maze and show the entire maze in a top down manner.  
Use three.js lib, here are the CDNs to use:

import * as THREE from 'https://cdn.jsdelivr.net/npm/three@0.121.1/build/three.module.js';
import { OrbitControls } from 'https://cdn.jsdelivr.net/npm/three@0.121.1/examples/jsm/controls/OrbitControls.js';
`````
(We give the needed CDNs as they are hard to guess)

2. **Iteration Process**: We allow 4-5 iterations to refine the code or fix any bugs, ensuring that the prompt's requirements are fully met.

3. **Enhancements**: Specifications for floor and maze/background colors are introduced later for improved user experience, not counted in the initial iteration limits.

4. **Camera Adjustments**: Manual camera adjustments are permitted, as positioning and orientation often require fine-tuning.

These steps ensure that each LLM's output is evaluated fairly from a user's perspective, considering visibility and usability rather than just technical correctness.

(Refer to `prompt.txt` for the latest prompt details.)

## Access the Mazes 🌍

Below are links to the final versions of each LLM-generated maze. Enjoy full navigational controls: use the left click to rotate, right click to translate, and middle click to adjust the zoom level.
You can also browse the entire ranking with previews on [index.html](./index.html).

Ranked from best to worse:  
- [ **NEW BEST** O3 Maze](https://louispaulet.github.io/maze_benchmark/o3.html)
- [GPT-o1 Maze](https://louispaulet.github.io/maze_benchmark/o1_version_A.html)
- [GPT-4o](https://louispaulet.github.io/maze_benchmark/gpt4o_version.html)
- [GPT-4 Reference Maze](https://louispaulet.github.io/maze_benchmark/gpt4_maze.html)
- [LLAMA3-70B Version](https://louispaulet.github.io/maze_benchmark/llama70b_version.html)
- [GPT4o-open interpreter Version](https://louispaulet.github.io/maze_benchmark/gpt4o_open_interpreter_version.html)
- [Zephyr-Orpo-141b-A35b-v0.1 Version](https://louispaulet.github.io/maze_benchmark/zephyr-orpo-141b-A35b-v0.1_version.html)  
- [c4ai-command-r-plus Version](https://louispaulet.github.io/maze_benchmark/c4ai-command-r-plus_version.html)  
  (Note: Zephyr 141B-A35B is an advanced iteration of the Mistral 8x22B model.)  
- [Nous-Hermes-2-Mixtral-8x7B-DPO_version Version](https://louispaulet.github.io/maze_benchmark/Nous-Hermes-2-Mixtral-8x7B-DPO_version.html)   
- Phi-3-mini-4k-instruct: code doesn't work (OrbitControls is not defined), context is too small for debug.  

## Contributing
Contributions to the Maze Benchmark project are more than welcome! If you have suggestions for improving the code, new features, or bug fixes, please feel free to fork the repository and submit a pull request.

## License
This project is licensed under the MIT License — see the [LICENSE](LICENSE) file in the repository for details.

## Learn More
For more information about the Maze Benchmark project, visit our [GitHub repository](https://github.com/louispaulet/maze_benchmark).

## Questions or Feedback
If you have any questions or feedback about the project, please open an issue in the GitHub repository, and we will be happy to assist you.

Thank you for your interest in improving and utilizing the Maze Benchmark!

## Advanced GPTo1 testing

### Car game  

Testing GPT-o1 by making a small procedural car game.  

[Car game](./car_game/car.html).

### AGAR.IO clone

Testing GPT-o1 by making a small AGAR.IO clone.  

[AGAR.IO clone](./agario/agario.html).

### Minecraft clone  

Testing GPT-o1 by making a Minecraft clone.  
[Minecraft clone](./minecraft/minecraft.html)
