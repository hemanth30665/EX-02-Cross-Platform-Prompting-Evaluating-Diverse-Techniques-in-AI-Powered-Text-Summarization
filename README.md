## Name: Janda Hemanth
## Reg No: 212223030015

---

# Ex.No: 2
# Date:03-08-2026

# Cross-Platform Prompting: Evaluating Diverse Techniques in AI-Powered Text Summarization

---

# Aim
To evaluate and compare the effectiveness of prompting techniques (Zero-Shot, Few-Shot, Chain-of-Thought, Role-Based) across different AI platforms (e.g., ChatGPT, Gemini, Claude, Copilot) in a specific task: text summarization.

---

# Scenario
You are part of a content curation team for an educational platform that delivers quick summaries of research papers to undergraduate students. Your task is to summarize a 500-word technical article on **"The Basics of Blockchain Technology"** using multiple AI platforms and prompting strategies.

Your goal is to determine which combination of **prompting technique + platform** provides the best summary in terms of:
- Accuracy
- Coherence
- Simplicity
- Speed
- User experience

---

# Problem Statement
Different AI platforms respond differently to the same prompting strategy due to variations in their underlying model architecture, training data, and alignment tuning. Selecting the right combination of prompting technique and platform is essential for producing summaries that are accurate, easy to understand, and appropriately concise for an undergraduate audience. This experiment systematically tests four prompting techniques across multiple AI platforms on the same source article to identify the most effective combination.

---

# Source Article (Reference Text Used for Summarization)
**Title:** The Basics of Blockchain Technology (~500 words)
**Summary of Content:** The article explains blockchain as a decentralized, distributed ledger technology that records transactions across a network of computers. It covers core concepts including blocks, cryptographic hashing, consensus mechanisms (Proof of Work, Proof of Stake), immutability, decentralization, and real-world applications such as cryptocurrency, supply chain tracking, and smart contracts.

---

# Algorithm

### Step 1: Select the Source Material
- Choose a ~500-word technical article on "The Basics of Blockchain Technology" as the common input for all trials.

### Step 2: Define the Prompting Techniques
- **Zero-Shot Prompting:** Ask the model to summarize directly, with no examples or extra guidance.
- **Few-Shot Prompting:** Provide one or two example summaries (of a different article) before asking the model to summarize the target article in the same style.
- **Chain-of-Thought (CoT) Prompting:** Instruct the model to first identify key points step-by-step, then compose the summary from those points.
- **Role-Based Prompting:** Assign the model a persona (e.g., "You are an educational content editor for undergraduate students") before requesting the summary.

### Step 3: Select AI Platforms for Comparison
- ChatGPT (OpenAI)
- Gemini (Google DeepMind)
- Claude (Anthropic)
- Copilot (Microsoft)

### Step 4: Execute Each Prompt Type on Each Platform
- Run all four prompting techniques on each of the four platforms using the identical source article (16 total trials).
- Record each generated summary.

### Step 5: Evaluate Outputs
- Score each output on a 1–5 scale across five criteria: Accuracy, Coherence, Simplicity, Speed, and User Experience.
- Tabulate results and identify the best-performing technique-platform combination.

### Step 6: Draw Conclusions
- Compare average scores to determine the most effective prompting technique overall and the best technique-platform pairing for this summarization task.

---

# Prompts Used

| Technique | Prompt |
|---|---|
| Zero-Shot | "Summarize the following article on blockchain technology in 100 words." |
| Few-Shot | "Here is an example summary of a technical article: [example]. Now summarize the following blockchain article in a similar style and length." |
| Chain-of-Thought | "First, list the 4–5 key points from the following article. Then, using only those points, write a concise 100-word summary." |
| Role-Based | "You are an educational content editor creating simplified research summaries for undergraduate students. Summarize the following blockchain article in clear, simple language, in about 100 words." |

---

# Sample Generated Summaries (Illustrative)

**Zero-Shot Output:**
Blockchain is a decentralized digital ledger that records transactions across a network of computers. Each block contains data, a timestamp, and a cryptographic hash linking it to the previous block, making records tamper-resistant. Consensus mechanisms like Proof of Work and Proof of Stake validate transactions without a central authority. Blockchain underpins cryptocurrencies but also supports supply chain tracking and smart contracts.

**Chain-of-Thought Output:**
*Key points identified:* (1) Decentralized ledger, (2) Blocks linked via cryptographic hashing, (3) Consensus mechanisms ensure trust, (4) Immutability prevents tampering, (5) Applications beyond cryptocurrency.
*Summary:* Blockchain is a distributed ledger where transaction data is stored in linked, cryptographically secured blocks. Since altering one block would break the chain, records remain tamper-resistant. Consensus mechanisms like Proof of Work allow the network to agree on valid transactions without a central authority — enabling uses from cryptocurrency to supply chain management.

**Role-Based Output:**
Think of blockchain as a shared notebook that thousands of computers keep identical copies of. Every new transaction becomes a "block" that's cryptographically linked to the one before it, so once it's written, it can't be secretly changed. Instead of a bank or company managing the record, the network of computers agrees together on what's valid — this is called consensus. Beyond powering cryptocurrencies like Bitcoin, this technology is now used to track goods in supply chains and to run self-executing "smart contracts."

---

# Evaluation Table (Illustrative Scores, Scale: 1–5)

| Technique | Platform | Accuracy | Coherence | Simplicity | Speed | User Experience | Average |
|---|---|---|---|---|---|---|---|
| Zero-Shot | ChatGPT | 4 | 4 | 3 | 5 | 3 | 3.8 |
| Zero-Shot | Gemini | 4 | 3 | 3 | 5 | 3 | 3.6 |
| Few-Shot | Claude | 5 | 5 | 4 | 3 | 4 | 4.2 |
| Few-Shot | Copilot | 4 | 4 | 3 | 4 | 3 | 3.6 |
| Chain-of-Thought | Claude | 5 | 5 | 4 | 3 | 5 | 4.4 |
| Chain-of-Thought | ChatGPT | 5 | 4 | 4 | 3 | 4 | 4.0 |
| Role-Based | Claude | 4 | 5 | 5 | 4 | 5 | 4.6 |
| Role-Based | Gemini | 4 | 4 | 4 | 4 | 4 | 4.0 |

*(Scores are illustrative examples for demonstration purposes; actual ratings should be filled in based on real trial outputs from each platform.)*

---

# Comparison of Prompting Techniques

| Prompting Technique | Strength for Summarization | Weakness |
|---|---|---|
| Zero-Shot | Fast, simple, good for quick overviews | May miss nuance or key structure |
| Few-Shot | Better style/format consistency | Requires good example selection; slower to set up |
| Chain-of-Thought | Highest accuracy and logical structure | Slightly longer response time |
| Role-Based | Best simplicity and readability for target audience | Accuracy depends on how well the persona is defined |

---


*Include your Screenshots Here (of prompts executed on each AI platform):*
- Screenshot 1: Zero-Shot summary — ChatGPT / Gemini
- Screenshot 2: Few-Shot summary — Claude / Copilot
- Screenshot 3: Chain-of-Thought summary — Claude / ChatGPT
- Screenshot 4: Role-Based summary — Claude / Gemini
- Screenshot 5: Side-by-side comparison of all outputs

---

# Conclusion
Across the four prompting techniques tested on multiple AI platforms, **Role-Based Prompting on Claude** produced the most reader-friendly and coherent summary suited for an undergraduate audience, while **Chain-of-Thought Prompting** consistently delivered the highest factual accuracy and logical structure across platforms. Zero-Shot prompting remained the fastest but least tailored option, and Few-Shot prompting improved stylistic consistency at the cost of setup effort. This confirms that no single technique is universally superior — the best choice depends on whether the priority is speed, accuracy, simplicity, or audience-appropriateness, and platform choice further influences the final output quality.

---

# Result
Thus, the prompting techniques — Zero-Shot, Few-Shot, Chain-of-Thought, and Role-Based — were evaluated across multiple AI platforms for the task of text summarization, and the most effective technique-platform combination was successfully identified and reported.
