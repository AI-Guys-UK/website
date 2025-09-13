---
layout: single
title:  "What is Classical Game AI?"
date:   2025-01-02 16:40:49 +0100
categories: classical ai
---
## Introduction

This article is the first in a two-part series exploring different approaches to AI in video games. These two domains represent distinct approaches to enhancing player experiences through artificial intelligence. Classical game AI, the focus of this article, has been a cornerstone of game development for decades. It relies on time-tested methods such as finite state machines, behavior trees, and pathfinding algorithms to create engaging and believable game worlds. In the next article, we’ll delve into generative game AI, a cutting-edge field that leverages machine learning and neural networks to create dynamic and personalized experiences. Together, these approaches highlight the ongoing evolution of AI in gaming.

## Historical Context

The roots of classical game AI trace back to the earliest days of video gaming, where the limited hardware capabilities of the time necessitated clever, efficient solutions to simulate intelligent behavior. Early examples include the ghosts in "Pac-Man," which used simple rule-based algorithms to create distinct personalities and movement patterns for each ghost, adding depth and unpredictability to the gameplay. Similarly, "Space Invaders" introduced the concept of increasing difficulty over time, with enemy behaviors becoming progressively faster as the player advanced. (Fun fact: The increasing speed of the invaders in "Space Invaders" was not initially designed as a gameplay feature. Instead, it was a result of the game's hardware limitations. As more enemies were eliminated, the processing load decreased, allowing the system to render the remaining invaders faster—an unintended but iconic aspect of the game's challenge.)

During the 1980s and 1990s, advancements in computing power allowed for more sophisticated implementations of AI. Titles like "Civilization" and "StarCraft" showcased the potential of decision trees and rule-based systems in strategy games, enabling complex interactions between players and AI opponents. These systems prioritized resource management, tactical planning, and adaptive responses, creating experiences that felt both challenging and rewarding.

The development of behavior trees and pathfinding algorithms in the late 1990s and early 2000s further revolutionized classical game AI. Games like "Halo: Combat Evolved" utilized behavior trees to model enemy behaviors, resulting in more realistic and engaging combat scenarios. Pathfinding algorithms such as A* became staples of game design, empowering non-player characters (NPCs) to navigate complex environments seamlessly.

The 2000s also saw the emergence of ambitious AI systems that aimed to blend classical techniques with player agency. One notable example is "Black & White," a game by Lionhead Studios that introduced a groundbreaking AI system where players could train a creature to learn behaviors based on rewards and punishments. Interestingly, Demis Hassabis, the lead AI developer for "Black & White," later co-authored the seminal paper on Long Short-Term Memory (LSTM) networks that would pave the way for advances in neural network research and eventually contribute to the foundation of DeepMind, which was later acquired by Google. This blend of decision trees and adaptive learning created a unique gameplay experience where the creature’s actions reflected the player’s choices, expanding the applications of classical AI design.

By the mid-2000s, classical game AI had firmly established itself as an integral part of game design. Iconic games like "The Sims" demonstrated how AI could simulate life-like behaviors and interactions, giving players a sense of immersion and agency. These foundational techniques continue to influence modern game development, underscoring the enduring legacy of classical AI.

## Core Concepts of Classical AI

When developing responsive and engaging AI for video games, developers often rely on a variety of foundational techniques. These methods, while individually powerful, can be combined into more sophisticated systems like Utility Systems or Goal-Oriented Action Planning (GOAP) to create nuanced and adaptive behaviors. Below, we explore some of the most popular and enduring techniques in classical game AI.

### Finite State Machines

Finite State Machines (FSMs) are one of the simplest and most effective tools in classical AI. Beyond gaming, FSMs are a cornerstone of computing in general, serving as a fundamental concept in areas like compiler design, digital circuit implementation, and network protocol analysis. Their structured approach to modeling sequential logic makes them invaluable across multiple domains, including the simulation of AI behaviors in games. They represent AI behavior as a series of states, where each state corresponds to a specific action or decision. Transitions between these states are triggered by predefined conditions, offering a structured and predictable framework for NPC behavior. 

Example: In "Pac-Man," each ghost operates in a finite state such as chase, scatter, or frightened. Their behavior changes dynamically based on the player's actions or game events.

### Behavior Trees

Behavior Trees build on the simplicity of FSMs, organizing AI actions hierarchically for greater flexibility. Each node in a behavior tree represents a potential action or decision, and the root node determines which branch to execute based on the game's context. This method is particularly effective for managing complex behaviors in games. 

Example: In "Halo: Combat Evolved," enemies use behavior trees to determine whether to attack, retreat, or regroup, creating fluid and believable combat scenarios.

### Decision Trees 

Decision Trees are a powerful tool for breaking down choices into a tree-like model of decisions and their possible outcomes. By mapping out conditional logic, they enable AI to make informed and context-sensitive decisions. Decision trees are pivotal in setting high-level goals for AI in strategy games like "Civilization." These trees guide AI leaders in determining whether to ally, trade, or declare war by analyzing the player’s actions and the evolving game state. Unlike behavior trees, which focus on executing specific tasks, decision trees excel at selecting overarching strategies. Once a goal like "attack" or "defend" is chosen, it can be passed to systems such as behavior trees or utility systems. These systems then handle the nuanced execution of that goal, ensuring that AI actions remain both purposeful and adaptive in response to changing conditions.

Example: In strategy games like "Civilization," AI leaders use decision trees to determine diplomacy strategies, whether to ally, trade, or declare war based on the player's actions and game state.

### Utility systems

Utility systems represent a flexible and dynamic approach to decision-making in classical game AI. Unlike finite state machines or behavior trees that rely on predefined transitions or hierarchies, utility systems evaluate multiple potential actions based on a scoring mechanism. Each action is assigned a utility value calculated from various game parameters, such as an NPC's health, proximity to threats, or available resources. The action with the highest utility score is selected, allowing NPCs to adapt their behavior dynamically to changing circumstances.

For example, in a survival game, an NPC could evaluate actions like finding food, fleeing from enemies, or seeking shelter. The utility system weighs the urgency of each need against the current game state, enabling the NPC to act intelligently and prioritize survival.

By combining utility systems with other techniques, such as decision trees or behavior trees, developers can create layered AI that seamlessly transitions between strategic planning and tactical execution, ensuring both high-level coherence and real-time adaptability.

### Pathfinding

Pathfinding algorithms are a cornerstone of classical game AI, enabling non-player characters (NPCs) to traverse complex environments efficiently. These algorithms calculate the optimal path between two points while navigating obstacles and considering terrain costs. Among these, the A* algorithm has become a gold standard due to its balance of efficiency and accuracy. A* employs heuristics to prioritize paths, ensuring quick decision-making even in large and intricate game maps.

Despite their effectiveness, pathfinding algorithms can be computationally expensive, particularly in large-scale or highly dynamic environments. Developers have introduced techniques like hierarchical pathfinding, which simplifies navigation by breaking the environment into smaller, manageable clusters. Flow field pathfinding, another innovation, allows NPCs to share navigation data, reducing computational overhead and improving efficiency in scenarios with many agents.

For example, in "Age of Empires," villagers and soldiers rely on pathfinding to navigate through forests, hills, and enemy fortifications. The smoothness and reliability of these movements not only prevent gameplay disruptions but also enhance the believability of the AI. By integrating pathfinding algorithms with other systems like finite state machines or behavior trees, developers can create NPCs that move purposefully and adaptively within dynamic game worlds.

### Flocking

Flocking behaviors, inspired by biological phenomena like bird flocks and fish schools, are another fascinating application of classical game AI. These simulations rely on simple rules such as separation (avoiding crowding neighbors), alignment (moving in the same direction as the group), and cohesion (staying close to the group's center). Despite their simplicity, these rules combine to produce emergent, lifelike group dynamics that are both realistic and computationally efficient.

A well-known implementation of flocking is the Boids algorithm, created by Craig Reynolds. Boids has been used in countless games and simulations to model crowd behaviors, enemy swarms, and even ambient wildlife. For example, in real-time strategy games, flocking principles can help large groups of units navigate complex terrains without becoming entangled or obstructing each other. Similarly, in action games, enemy swarms can use flocking to appear coordinated while still behaving dynamically.

By integrating flocking algorithms with other AI techniques, developers can create compelling scenarios that mimic the intricacies of group behavior, adding depth and realism to game worlds.

## Applications in Games

Classical game AI plays a pivotal role in creating immersive and interactive experiences in various gaming contexts. One of its key applications is NPC behavior modeling, where artificial intelligence brings characters to life by enabling them to react dynamically to players' actions and environmental changes. Whether it’s an enemy soldier strategically flanking a player or a villager performing daily routines, NPCs rely on AI techniques to improve gameplay immersion.

Another critical application is strategy and decision-making. AI opponents in strategy games use advanced algorithms to plan their moves, manage resources, and adapt to the player's tactics. These systems ensure that the game remains challenging and rewarding, providing a sense of accomplishment for players who outsmart their AI adversaries.

Environmental interactions also benefit greatly from classical AI. By simulating realistic responses to environmental stimuli, such as navigating obstacles or reacting to weather changes, AI enhances the believability of game worlds. For instance, AI-driven wildlife in open-world games may flee from predators, forage for food, or interact with their surroundings in ways that create a vibrant and convincing ecosystem.

## Differences in AI Across Game Genres

Video games span a diverse range of genres, each with its own unique requirements and challenges for artificial intelligence. The design and implementation of AI often vary significantly depending on the type of gameplay, player interaction, and overall objectives of the game. From the split-second reactions needed in first-person shooters to the strategic complexity of real-time strategy games, AI must be carefully tailored to suit the genre.

### First-Person Shooters (FPS):

First-person shooters (FPS) require AI systems that prioritize real-time reactions and dynamic adaptability to create challenging and immersive experiences. At their core, FPS games demand reactive enemy behaviors tailored to fast-paced combat. This involves AI that can assess player actions instantaneously, adapt strategies on the fly, and engage in tactical positioning. For example, an enemy AI might retreat to cover when under heavy fire or flank the player when an opportunity arises.

A hallmark of FPS AI is its reliance on cover systems. These systems enable enemies to use the game environment strategically, seeking out obstacles to shield themselves from player attacks while positioning themselves for counterattacks. This creates a sense of realism and increases the challenge for players, as they must anticipate and counteract these tactical maneuvers.

Squad-based tactics also play a significant role in many FPS games. AI units may coordinate their actions, such as laying down suppressive fire while other units advance, mimicking real-world military strategies. These behaviors are often enhanced by hierarchical decision-making systems, where AI commanders issue orders that individual units execute based on their immediate context.

Compared to other genres, FPS AI places a heavy emphasis on immediate decision-making and responsiveness, distinguishing it from the more deliberative strategies of real-time strategy games or the narrative-driven interactions of role-playing games. By leveraging a combination of reactive systems, pathfinding algorithms, and behavior trees, FPS games deliver fast, fluid, and engaging combat experiences.

### Role-Playing Games (RPG):

Role-playing games (RPGs) demand intricate AI systems to support their narrative-driven and exploratory nature. One of the hallmarks of RPGs is complex NPC interactions, facilitated by dialogue trees and quest logic. These systems allow players to engage in meaningful conversations and make choices that impact the game’s world and story. Whether it’s negotiating with a merchant or choosing a faction to align with, AI helps create a sense of depth and immersion.

Another critical aspect of RPG AI is managing companions and party dynamics. Companions must react to the player’s decisions, follow commands, and assist during combat, all while maintaining their own unique personalities. This requires robust AI to ensure companions feel like integral parts of the story rather than just mechanical allies.

RPGs also emphasize environmental responsiveness, where AI adapts to changes in the world. This could involve wildlife reacting to the time of day or weather conditions, or NPCs altering their routines based on the player’s actions. Such dynamic behaviors bring the game world to life, enhancing the player’s sense of agency and immersion.

Compared to genres like FPS or RTS, RPG AI focuses less on real-time tactics and more on creating believable characters and a rich, interactive environment. This distinction highlights the unique challenges and opportunities in designing AI for narrative-driven experiences.

### Racing Games:

Racing games present unique challenges for AI, as they require a balance between precision, competitiveness, and adaptability. Path optimization is one of the most critical aspects, ensuring that AI opponents can navigate tracks efficiently while adhering to ideal racing lines. These algorithms must account for dynamic factors like the player’s position, track conditions, and other opponents, creating a competitive but fair experience.

Adaptive difficulty is another hallmark of AI in racing games. To maintain player engagement, the AI adjusts its performance dynamically, either increasing or reducing its speed and aggressiveness based on the player’s skill level. This ensures that the game remains challenging without becoming overly frustrating.

Collision avoidance is essential to prevent AI drivers from creating chaotic pileups or unrealistically ignoring other cars. By leveraging predictive algorithms, AI drivers can anticipate potential collisions and make adjustments in real time to avoid crashes, contributing to the overall realism of the racing experience.

Compared to other genres, racing games focus heavily on continuous, precise calculations to simulate smooth and competitive gameplay. Recent innovations, such as incorporating machine learning techniques or offloading certain computations to the GPU, have further enhanced the realism and efficiency of racing AI, keeping it a vital part of modern game design.

### Real-Time Strategy (RTS):

Real-time strategy (RTS) games represent one of the most challenging and rewarding genres for AI development, requiring a blend of large-scale strategic thinking and granular, real-time decision-making. At the core of RTS AI lies resource management and base-building logic. AI opponents must efficiently gather resources, construct buildings, and develop technologies, all while preparing for offensive and defensive actions. This complex interplay of priorities demands AI systems capable of both long-term planning and immediate adaptation.

Tactical unit control is another key element of RTS AI. AI must command diverse units in battle, ensuring they move and act cohesively to achieve strategic objectives. Whether it's positioning archers on high ground or coordinating a multi-pronged assault, effective unit control is essential for challenging human players. Advanced pathfinding algorithms, often augmented with techniques like flocking behaviors or hierarchical planning, are used to navigate units across intricate terrains.

Dynamic adaptation to player strategies is perhaps the most critical component of RTS AI. To maintain engagement, AI must analyze the player's actions and adjust its tactics accordingly. For instance, if a player favors aerial attacks, the AI might shift focus to anti-air defenses. This adaptability requires players to adjust their strategies to remain competitive.

Compared to other genres, RTS games demand a unique combination of high-level strategic decision-making and real-time responsiveness. By integrating decision trees, utility systems, and pathfinding, RTS AI achieves a balance between planning and execution, delivering compelling gameplay experiences that test the limits of strategy and adaptability.

## Advantages of Classical AI

Classical AI offers several compelling advantages, especially in the context of fast-paced video games where decisions must be made in real time. One of its primary strengths lies in predictability and control. Developers can design and fine-tune AI behaviors with precision, ensuring consistent outcomes and a tailored player experience. This is particularly important in competitive or fast-paced games where AI must act quickly and reliably.

Efficiency in resource-constrained environments is another key advantage. Classical AI techniques like finite state machines and decision trees are computationally lightweight, making them ideal for systems where processing power and memory are limited. This efficiency becomes critical in scenarios where heavy computations, such as pathfinding, ray casting, or environmental queries, must be executed without causing performance bottlenecks.

Moreover, classical AI’s simplicity and transparency in design allow for straightforward debugging and iteration. When properly implemented, developers can easily trace AI decisions and understand why certain behaviors are triggered. While modern advancements like GPU-based computations and hierarchical systems can optimize performance, classical AI methods offer straightforward debugging and iteration, making them foundational tools even in today’s complex gaming environments.

## Challenges and Limitations

Classical game AI, while powerful and versatile, comes with its own set of challenges and limitations. One significant drawback is its lack of adaptability and learning. Traditional techniques like finite state machines and decision trees rely on predefined logic, making it difficult for AI to adapt to unexpected scenarios or evolve its strategies over time. This rigidity can lead to predictable patterns that experienced players quickly learn to exploit, reducing the AI's ability to remain challenging over extended play sessions.

Another limitation lies in scalability, particularly in games with complex behaviors or large-scale environments. Algorithms like pathfinding or ray casting, which are integral to many classical AI systems, can become computationally expensive when applied to dynamic or expansive game worlds. The need to continuously query environmental data and process decisions in real time adds further strain, often requiring careful optimization to maintain performance without sacrificing functionality.

Despite these limitations, these challenges are often addressed through modern approaches, such as integrating classical AI with machine learning techniques or offloading computationally intensive tasks to GPUs. These hybrid solutions allow developers to preserve the simplicity and control of classical AI while addressing its inherent shortcomings, ensuring that it remains a vital part of modern game design.

## Modern Adaptations

Classical AI continues to evolve through the integration of hybrid approaches, blending traditional techniques with modern technologies to expand AI's role in games. By incorporating machine learning (ML) methods, developers can enhance the capabilities of classical AI systems, addressing some of their inherent limitations while preserving their efficiency and transparency.

For example, machine learning can be used to complement decision trees by dynamically adjusting the weights or priorities of certain decisions based on player behavior. This allows the AI to refine its strategies over time, creating a sense of intelligence and unpredictability. In a strategy game, ML could enable an AI opponent to learn which units the player prefers to use and adjust its tactics to counter them, improving AI responses to player strategies.

Another application of hybrid AI involves combining classical techniques like behavior trees with reinforcement learning. In an FPS game, reinforcement learning could allow enemies to optimize their use of cover based on the player’s shooting patterns, while the underlying behavior tree ensures that their actions remain coherent and believable.

Offloading computationally intensive tasks like pathfinding and environmental queries to GPUs is another way modern technologies enhance classical AI. This enables large-scale simulations, such as crowd behaviors in open-world games or real-time adjustments in dynamic environments, without sacrificing performance.

By leveraging these hybrid systems, developers can create AI that not only responds to the immediate game state but also adapts and evolves over time, resulting in more engaging and immersive experiences for players.

## Conclusion

Classical AI remains a cornerstone of video game development, providing the structure and reliability needed to create immersive and engaging experiences. Its techniques, such as finite state machines, behavior trees, and pathfinding algorithms, continue to underpin some of the most memorable and dynamic moments in gaming history. Despite its limitations, classical AI has evolved alongside technological advancements, embracing hybrid approaches that combine the best of traditional and modern methods to address challenges like scalability and adaptability.

As we transition to exploring generative AI in the next article, we’ll delve into its ability to personalize and enhance player experiences, as well as assist in the development and creative processes of game design. Generative AI goes beyond traditional procedural generation by leveraging modern techniques, such as transformer models and neural networks, to create game content. While traditional procedural methods rely on predefined algorithms and rules, generative AI utilizes learning from data to craft more nuanced and context-aware outputs, opening new avenues for personalization and depth in gaming experiences. These capabilities allow developers to craft immersive and expansive game worlds that evolve in response to player actions and preferences.

Moreover, generative AI serves as a powerful tool during game development, assisting developers at various stages. During early prototyping, generative AI can rapidly create assets like terrains, character designs, or level layouts, enabling teams to iterate quickly on ideas. In the ideation phase, it can provide inspiration by generating multiple variations of game elements, sparking new creative directions. For final polishing, AI tools can streamline repetitive tasks such as optimizing textures or refining NPC dialogue, freeing developers to focus on more complex and creative challenges. By integrating generative AI into these processes, teams can enhance productivity and push the boundaries of innovation. By automating aspects like terrain generation or NPC dialogue creation, teams can focus on refining core gameplay mechanics and storytelling elements. These advancements open new frontiers for creativity and efficiency in game design.

Additionally, generative AI offers valuable tools for developers during the game development process. From assisting with prototyping to inspiring ideation and streamlining repetitive tasks, these tools enable teams to work more efficiently and explore innovative concepts. By blending the structured methods of classical AI with the creative possibilities of generative AI, the future of game AI holds great potential.

