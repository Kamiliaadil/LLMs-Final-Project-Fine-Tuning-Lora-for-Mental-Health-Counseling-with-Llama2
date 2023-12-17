Kamilia Adil

Large Language Models and Chat GPT







Mental Health Counseling with Llama2-Fine-Tuning-Lora














Table of Contents:
1.	Introduction
2.	Research Question
3.	Data Description
4.	Audience
5.	Methodology 
6.	Social Implications
7.	Conclusion


















I.	Introduction:

In this project, I explore the intersection of mental health and language models, specifically using Large Language Models (LLMs) to offer guidance and support. Focusing on the effectiveness of LLMs in providing mental health advice and the associated social implications, I outline the methodology, dataset, and audience. The aim is to create a user-friendly and accessible tool for individuals facing mental health challenges, recognizing both the positive and negative impacts of integrating AI into this sensitive domain.

II.	Research Question:

How can a fine-tuned language model effectively provide mental health advice and support to individuals expressing feelings of worthlessness and related concerns? Additionally, what are the social implications of such models?

•	How does the language model understand and respond to expressions of worthlessness in counseling conversations?

•	What potential positive and negative effects might individuals experience when using a language model for mental health advice and support?


III.	Data Description:

The dataset for this project originates from two well-established online counseling and therapy platforms. It comprises anonymized user queries and the corresponding responses from qualified psychologists. User questions are found in the 'Context' field, and psychologists' advice is in the 'Response' field. Rigorous cleaning processes have been applied to prioritize privacy, covering a wide array of mental health topics. The dataset is accessible on the Hugging Face platform, and the dataset is available here.


IV.	Audience:

My audience for this project is everyone because mental health affects us all, and we all face challenges. Specifically, I aim to reach individuals seeking mental health advice and support. The model is designed to offer a user-friendly and accessible way for people to get guidance during difficult times.

V.	Methodology:

In my approach to developing the fine-tuned language model using the llama architecture, I initially accessed the LLaMa2 model through Hugging Face. I utilized the "NousResearch/Llama-2-7b-chat-hf" model, calling both this model and the dataset from Hugging Face via the API. I designated the new model as "llama-2-7b-mental_health."

For the training configuration, I incorporated techniques such as Quantized LoRA (QLoRA) and BitsAndBytes (BNB) quantization. QLoRA parameters, including attention dimension, alpha scaling, and dropout probability, underwent fine-tuning. Moreover, I implemented 4-bit precision base model loading with nested quantization for optimized model efficiency.

I defined the training parameters, encompassing aspects like batch size, learning rate, and optimization strategies. The training process encompassed supervised fine-tuning using the SFTTrainer class, directing the model to generate contextually relevant responses to mental health queries. I consolidated 'Context' and 'Response' columns into a unified 'text' column, proceeded with model training, and saved checkpoints at regular intervals.

To augment the model's efficiency, I leveraged the LoRA (Learned Random Access) attention mechanism and BitsAndBytes quantization. The resulting model was then saved as "llama-2-7b-mental_health" for future utilization.

VI.	Social Implications:

I acknowledge that the model I created carries both positive and negative social impacts, especially considering its role in providing mental health advice and support—a domain involving complex and intricate matters. Here are some aspects I've considered:

A.	Positive Implications:

•	Therapy chatbots offer exceptional ease and accessibility. In situations where there's a shortage of human therapists, AI chatbots can fill the gap. Individuals have the flexibility to engage with a chatbot whenever they need, beyond the constraints of appointment availability. For instance, even confined to my bed, I could utilize it at 4 a.m.

•	Some individuals may find comfort in interacting with chatbots over humans, as they perceive a reduced stigma in seeking help when there's no human on the other end. People might express things to machines that they would hesitate to share with a human, potentially lowering the stakes and diminishing vulnerability. Chatbots can provide a less intimidating, private, and user-friendly avenue for individuals to seek support.

•	Therapy chatbots provide valuable support by tackling obstacles like the prohibitive costs of traditional therapy and societal taboos related to mental health. The combination of high costs and stigmatization often discourages individuals from exploring conventional options, creating an opportunity for discreet and affordable alternatives to fill the void.

B.	Negative Implications:

•	Chatbots may not be universally appealing and are susceptible to potential misuse or misunderstanding. Critics highlight instances where computers misunderstood users, generating messages that could be potentially damaging. Personally, as a French speaker, when I represent myself in English or another language, I experience a shift in my persona and personality—this shift becomes more pronounced when expressing feelings of worthlessness. The challenge lies in how accurately LLMs can comprehend and appropriately respond to such nuanced and culturally diverse instances.

•	Chatbots face limitations in offering high-quality advice, often failing to recognize cues that a human would identify as indicative of underlying issues. During the final review, a classmate shared feeling stressed and sad due to concerns about body weight. The model responded with empathy, providing advice on building confidence and losing weight.  However, if my classmate were severely underweight and seeking guidance on weight loss, a clinical intervention might be necessary, surpassing the scope of simple advice.

•	Algorithms have not reached a stage where they can replicate the intricate nuances of human emotion, let alone emulate genuine empathetic care. For instance, whenever I engage with my model, it consistently responds with, "I am sorry to hear that you are feeling that..." regardless of my prompts or inquiries. This creates an impression of simulated empathy, which feels somewhat peculiar.

•	I recognize that my model, like all AI systems, depends on pre-existing data that may carry embedded human biases. I am aware that this reliance on biased data could lead to the model providing answers with unfair opinions. For instance, if the dataset predominantly represents certain individuals or specific mental health situations, the model might unintentionally perpetuate those biases in its responses.



VII.	Conclusion:

In reflecting on the outcomes of my model, I acknowledge the significant progress seen in large language models (LLMs) in recent years. While the model I developed provided beneficial mental health advice, it's crucial to recognize its limitations. It can't replace the essential clinical expertise, empathy, and compassion offered by psychiatrists, psychologists, and therapists.

I observed potential issues in the model's understanding of users, an inability to replicate the intricate nuances of human emotion, and a lack of genuine empathetic care. Additionally, concerns about data privacy and biases highlight the complexity of integrating AI into mental health.

I firmly assert that artificial intelligence is not ready to replace the pivotal role of traditional therapy and should never aim to do so. Instead, therapy chatbots, including the one I created, should be seen as complementary tools. While they offer valuable support, they fall short of replicating the profound human connection and nuanced understanding provided by human therapists. It is crucial to perceive AI in mental health as a helpful addition to traditional methods and practices.



