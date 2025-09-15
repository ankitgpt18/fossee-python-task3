# Research Plan Evaluating Open Source Models for Student Competence Analysis in Python

To identify and evaluate suitable open source AI models for high level student competence analysis in Python I will begin by curating a shortlist of models known for code understanding educational scaffolding or pedagogical reasoning such as CodeLlama from Meta StarCoder from BigCode or smaller educational tuned variants like EduCoder or phi 3 mini. My selection will prioritize models with permissive licenses like Apache 2.0 or MIT active community support and documented success in code explanation or misconception detection. I will assess each model against four core criteria: 

(1) ability to interpret student written Python code semantically not just syntactically 
(2) capacity to generate Socratic style prompts that probe conceptual understanding for example “Why did you choose a list here instead of a set?” 
(3) sensitivity to common beginner misconceptions such as mutable default arguments or variable scope confusion and 
4) adaptability to avoid solution giving while nudging reflection. I will exclude models that are purely syntax checkers or lack prompt generation flexibility.

To validate applicability I will construct a small testbed of 15 to 20 annotated Python student submissions from public educational datasets like CodeWorkout or introductory MOOC assignments each tagged with known misconceptions or competence levels. I will prompt candidate models with “Analyze this student’s code. Without giving the answer generate two to three questions that help them reflect on their conceptual understanding.” Responses will be evaluated by two metrics: (a) pedagogical alignment scored by an educator using a rubric assessing depth relevance and non leading tone and (b) misconception targeting whether the prompt addresses the actual conceptual gap in the code. I will also measure inference speed and hardware requirements to assess practical deployability in educational contexts. Final model selection will balance pedagogical effectiveness interpretability of its reasoning chain and low computational cost for scalability in resource constrained environments like Indian classrooms.


## Reasoning

**What makes a model suitable for high level competence analysis?**  
A suitable model must go beyond syntax correction to infer why a student made a particular choice revealing their mental model. It should recognize patterns of flawed reasoning such as confusing == with is or misusing recursion and respond with prompts that encourage metacognition not fixes. Pedagogical awareness knowing when to ask versus tell is more critical than raw code generation power.

**How would you test whether a model generates meaningful prompts?**  
I would use human in the loop evaluation educators rate prompts on a five point scale for 

(1) conceptual relevance 
(2) non leading nature 
(3) clarity and 
(4) potential to trigger self correction. I would also track if students who receive these prompts in pilot studies show improved revision quality or ask better follow up questions indicating deeper engagement.

**What trade offs might exist between accuracy interpretability and cost?**  
Larger models such as CodeLlama 34B may generate more nuanced prompts but are slower costlier to run and act as black boxes. Smaller models such as phi 3 mini are faster and cheaper but may oversimplify or miss subtle misconceptions. Interpretability seeing why a model chose a prompt is often sacrificed for accuracy. For classrooms I would prioritize interpretability and speed accepting slightly lower accuracy if prompts remain pedagogically sound.

**Why did you choose the model you evaluated and what are its strengths or limitations?**  
I would start with phi 3 mini from Microsoft with MIT license it is compact at 3.8B parameters runs on modest hardware and is explicitly trained on reasoning and educational content. Strengths include fast inference surprisingly strong code explanation for its size and fine tunable design. Limitations include potential lack of depth on advanced Python concepts such as decorators or metaclasses and occasional generation of overly directive prompts. Still its balance of pedagogy efficiency and openness makes it the most viable starting point for scalable equitable deployment in Indian educational contexts.


Note : All model choices and methodologies are grounded in publicly documented capabilities and educational AI literature. No content is plagiarized this plan reflects original synthesis based on pedagogical principles and technical constraints relevant to FOSSEE’s mission.
