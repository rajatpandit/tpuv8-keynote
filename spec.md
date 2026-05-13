# Presentation: Architecting Intelligence

---

## Slide 1: Architecting Intelligence
A Deep Dive into Google's TPU Innovation and the Infrastructure of the Agentic Era

### Speaker Notes
> "Welcome, everyone. Today, we're going to take a journey into the heart of modern artificial intelligence. We aren't just talking about software or models—we are talking about 'Architecting Intelligence.' This is a deep dive into Google's TPU innovation, the very foundation that has brought us into the Agentic Era."

---

## Slide 2: The Hardware Lottery & The Genesis of the TPU
* **The Compute Crisis:** Deep learning requires massive matrix multiplication, exposing a vulnerability in traditional von Neumann architecture where data movement creates a severe bottleneck.
* **The "Voice Search" Calculation:** In 2006, Jeff Dean realized that if every Android user utilized voice search for three minutes a day, Google would need to double its global data center footprint. 
* **The "Generality Tax":** CPUs are designed for sequential instructions, while GPUs (originally for graphics) carry heavy legacy logic that is inefficient for neural network math. 
* **The Radical Solution:** Instead of waiting for commodity hardware to scale, Google engineered an Application-Specific Integrated Circuit (ASIC)—stripping away graphics logic to create the first Tensor Processing Unit (TPU). 

### Speaker Notes
> "Let's step back for a moment. Deep learning brought us to a compute crisis. Standard von Neumann architectures simply choke on moving the massive amounts of data required. Back in 2006, Jeff Dean ran the numbers and saw that just three minutes of voice search per Android user meant doubling Google's data center footprint worldwide. We were paying a 'generality tax'—CPUs are too sequential, and GPUs carried legacy graphics logic we didn't need for neural networks. So, we did something radical: we built an ASIC designed from the ground up for tensor processing. We stripped away the bloat and created the first TPU."

---

## Slide 3: Making the Impossible Possible: RankBrain
* **Minimizing Data Movement:** The core TPU architecture relies on large systolic arrays, achieving a 10x to 30x reduction in inference costs at a highly efficient 40 watts. 
* **The RankBrain Challenge:** Google's first deep learning model for Search had to map words to concepts in a high-dimensional vector space to deduce query intent in real-time. 
* **Beating the Bottleneck:** Running RankBrain on commodity CPUs or GPUs would have caused severe latency and decimated profit margins. 
* **The Result:** The TPU v1 made RankBrain economically and technically viable, allowing the entire search index and complex synonym expansion models to operate with unprecedented speed. 

### Speaker Notes
> "The results were immediate. By leveraging large systolic arrays, we minimized data movement, dropping inference costs by 10 to 30 times at just 40 watts. This breakthrough was the only way we could make RankBrain—our first real-time, high-dimensional deep learning model for Search—actually work. Running that on off-the-shelf CPUs or GPUs would have completely decimated our profit margins due to latency and power costs. The TPU v1 made the impossible, possible."

---

## Slide 4: Powering the Google Ecosystem
* **Everyday Consumer AI:** The TPU enabled sustainable, real-time natural language processing for features like "Smart Reply" in Gmail and Gboard. 
* **On-Device Revolution:** Gemini Nano powers native capabilities on the Pixel smartphone (e.g., Summarize, Magic Compose, Call Notes) through "knowledge distillation" from massive Cloud TPUs. 
* **Search Generative Experience (SGE):** TPUs like the Trillium v6 process billions of complex, multimodal search queries natively. 
* **Enterprise Empowerment:** Google Cloud TPUs power Vertex AI, allowing startups like Fetcherr to simulate millions of airline routing scenarios, and Anysphere (Cursor) to run real-time codebase-aware autonomous agents. 

### Speaker Notes
> "This silicon didn't just stay in a lab; it powers the entire Google ecosystem. It makes everyday consumer AI sustainable—think Smart Reply in Gmail. It’s what allowed us to distill those huge models into Gemini Nano, running right on your Pixel phones. And for those massive billions of multimodal queries in our Search Generative Experience, TPUs process them natively. On the enterprise side, Vertex AI backed by Cloud TPUs empowers startups to run real-time autonomous agents. It's everywhere."

---

## Slide 5: The Evolutionary March of Silicon
* **TPU v1 (2015):** Inference-only ASIC deployment. 
* **TPU v2 (2017):** First generation capable of training, introducing bfloat16 (BF16) to slash memory requirements. 
* **TPU v3 & v4 (2018-2021):** Scaled up to massive 4,096-chip pods, requiring liquid cooling and moving to 3D torus interconnects. 
* **TPU v5 to v7:** Diverged into cost-optimized (v5e) and performance (v5p) lines. Trillium (v6e) quadrupled operations per cycle, while Ironwood (v7) introduced native FP8 precision and dual-chiplet designs. 
* **TPU 8t & 8i (2026):** For the first time, Google physically split the architecture to address the diverging needs of massive training vs. agentic inference. 

### Speaker Notes
> "Look at this evolutionary march. We started with inference-only in 2015. By 2017, we enabled training and introduced bfloat16 to drastically cut memory needs. Then we scaled. From v3 and v4 using liquid cooling in massive pods, all the way to v5, v6, and v7 where we specialized into cost and performance lines, pushed native FP8, and moved to dual-chiplets. And now, in 2026, we reach a turning point: TPU 8t and 8i, fundamentally splitting the architecture to tackle the vastly different needs of scale-out training versus low-latency agentic inference."

---

## Slide 6: AlphaChip: The Recursion of AI Designing AI
* **The Manual Bottleneck:** For sixty years, chip floorplanning was a tedious, manual process taking human experts months to complete due to complex thermal and spatial constraints. 
* **Gamifying Engineering:** DeepMind’s AlphaChip treats the silicon wafer like a game board, using reinforcement learning to place circuit components efficiently. 
* **Superhuman Speed:** AlphaChip generates optimized chip layouts in hours rather than months, beating Google's own physical design experts in minimizing average wirelength. 
* **The Impact:** Reducing design time from six months to a week saves millions of dollars per chip in labor and vastly reduces energy costs across data centers. 
* **A Recursive Loop:** AI software designs increasingly powerful AI hardware. 

### Speaker Notes
> "But here's where it gets truly fascinating. To build better chips, we had to rethink how we design them. For sixty years, chip floorplanning was a human-led bottleneck, taking months. We turned this engineering challenge into a game board for DeepMind's AlphaChip. Using reinforcement learning, it now places components in hours, outperforming our best human experts. We’re saving millions and dropping energy usage significantly. It's a beautiful recursive loop: AI is designing the hardware that will run the next generation of AI."

---

## Slide 7: The Optical Circuit Switching (OCS) Moat
* **The Networking Ceiling:** Training frontier models requires tens of thousands of chips to operate in perfect synchronization for months. Standard copper networks stall entirely if one link fails. 
* **The OCS Advantage:** Google uses arrays of Micro-Electro-Mechanical Systems (MEMS) mirrors to route light directly between fibers, avoiding energy-heavy conversions to electrical signals. 
* **Efficiency & Scale:** TPU clusters utilizing OCS use ~3x less energy and produce ~20x less CO2e than traditional GPU clusters. 
* **Dynamic Resilience:** OCS automatically detects and reroutes around faulty links instantly, protecting cluster-wide goodput without human intervention. 
* **Mathematical Dominance:** A Google Ironwood cluster linked with OCS marshals 9,216 TPUs with 1.77 Petabytes of memory—a scale standard GPU networking struggles to match. 

### Speaker Notes
> "Let's talk about the network, because computing power is nothing without connectivity. When you're training frontier models, tens of thousands of chips must sync flawlessly. A single copper wire failing can crash the whole system. Our moat here is Optical Circuit Switching, or OCS. We use microscopic MEMS mirrors to bounce light directly between fibers, completely bypassing power-hungry electrical conversions. This makes us about three times more energy-efficient and drastically cuts carbon emissions. Moreover, it's dynamically resilient—it routs around failures instantly. A single Ironwood cluster hits over 9,000 TPUs and nearly two petabytes of memory with this OCS backbone. You just can't match that with standard GPU networking."

---

## Slide 8: The Agentic Paradigm Shift
* **Beyond Static Chat:** The industry has moved from text prediction to Agentic AI, where models simulate scenarios, reason in loops, and take autonomous action. 
* **World Models:** Systems like DeepMind's Genie 3 generate photorealistic, interactive 3D environments from text, deployed for tasks like Waymo autonomous driving simulations. 
* **The Workload Bifurcation:**
  * **Training** requires moving exabytes of batch data across thousands of chips (prioritizing throughput). 
  * **Inference** requires millions of agents fetching data from Key-Value caches (crippled by latency). 
* **The Resolution:** A universal chip could no longer excel at both, prompting the radical TPU 8t and 8i split. 

### Speaker Notes
> "Now, the paradigm is shifting. We aren't just doing text prediction anymore. We are in the Agentic AI era, building models that simulate reality, reason, and act autonomously. Take Genie 3, rendering interactive 3D worlds for autonomous driving simulations. This brings us to a stark bifurcation in our workloads. Training wants exabytes of batch data shoved through the pipes—it prioritizes throughput. Inference, however, is now millions of agents constantly querying Key-Value caches, where latency is the ultimate enemy. A single universal chip can no longer serve both masters."

---

## Slide 9: TPU 8t: The Megascale Training Powerhouse
* **The Goal:** Reduce frontier model training cycles from months to weeks. 
* **Massive Scale:** A standard TPU 8t superpod scales to 9,600 chips, marshaling two petabytes of shared HBM and 121 ExaFlops of compute. 
* **Direct Storage Integration:** Bypasses host CPUs to pull massive datasets directly into the TPU's memory, targeting over 97% productive compute time (goodput). 
* **The Virgo Network:** A multi-layer architecture providing near-linear scaling for up to 1 million chips in a single logical cluster, delivering up to 47 petabits per second of non-blocking bandwidth. 

### Speaker Notes
> "This brings us to the TPU 8t: the megascale training powerhouse. The goal was simple but massive—slash the training cycles of frontier models from months down to weeks. A standard superpod marshals 9,600 chips and 121 ExaFlops of compute. We also bypassed host CPUs entirely so we can stream massive datasets straight into TPU memory, hitting over 97% productive compute time. And tying it all together is the Virgo Network, letting us scale near-linearly to a staggering one million chips in a single logical cluster."

---

## Slide 10: The Architectural Divergence
* **The Workload Fork:** A structural divergence where training networks (throughput-optimized) physically separate from inference networks (latency-optimized).

### Speaker Notes
> "But what about the other side of the coin? As we established, training and inference workloads have fundamentally diverged. Let's look at the architectural divergence that brought us the counterpart to the 8t, recognizing that high throughput doesn't solve low latency."

---

## Slide 11: TPU 8i: The Agentic Inference Specialist
* **Breaking the Memory Wall:** Features 288 GB of HBM and an immense 384 MB of on-chip SRAM (a 3x increase) to host massive Key-Value caches directly on silicon. 
* **Collectives Acceleration Engine (CAE):** A novel on-die processor that offloads global synchronization operations, cutting collective latency by up to 5x for MoE routing. 
* **Boardfly Topology:** Completely abandons the 3D torus for a flattened, hierarchical Dragonfly-inspired architecture. 
* **Slashing Latency:** Boardfly utilizes direct optical long-haul cables to reduce the maximum network diameter from 16 hops down to just 7 hops, yielding an 80% better performance-per-dollar metric for low-latency serving. 

### Speaker Notes
> "Meet the TPU 8i, our Agentic Inference Specialist. To break the memory wall that strangles agents, we bumped on-chip SRAM up 3x to 384 Megabytes, hosting those massive Key-Value caches right on the silicon. We also built the Collectives Acceleration Engine directly on-die to handle synchronization, dropping latency by up to 5x. And perhaps the biggest shift: we completely abandoned the 3D torus network for Boardfly, a flattened, Dragonfly-inspired topology. Using long-haul optical cables, we reduced the maximum network hops from 16 down to just 7. This gives us an incredible 80% better performance-per-dollar for low-latency serving."

---

## Slide 12: Conclusion
* The Google Tensor Processing Unit represents a decade-long commitment to system-level co-design, from silicon to software to optical networking.
* By utilizing tools like AlphaChip, Google turned AI upon itself to design the physical limits of its own hardware.
* The divergence into the specialized Virgo network (TPU 8t) and Boardfly topology (TPU 8i) acknowledges that intelligence workloads are no longer monolithic.
* Google’s TPU infrastructure doesn't just accelerate the algorithms of today—it physically defines the boundaries of what intelligence can become tomorrow.

### Speaker Notes
> "To conclude, the TPU isn't just a chip. It's a decade of relentless, system-level co-design covering everything from silicon structure to optical networks. By bringing AlphaChip into the fold, we turned our AI inward to push past physical limitations. Splitting into Virgo for training and Boardfly for inference proves that the monolithic era of intelligence is over. Google’s TPU infrastructure doesn't just run today's algorithms faster—it literally defines the physical boundaries of what artificial intelligence can become tomorrow. Thank you."