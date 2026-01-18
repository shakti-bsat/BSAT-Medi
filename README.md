# BSAT-Medi

Medi-Mate is developed using a combination of artificial intelligence techniques and system integrations to address the practical challenge of understanding medical prescriptions and improving medication adherence. The solution begins with an image processing pipeline that accepts prescription images uploaded by users. These images often contain handwritten or poorly formatted text, so preprocessing steps such as noise reduction, contrast enhancement, and alignment are applied to improve readability before further analysis.

Optical Character Recognition (OCR) technology is then used to extract textual information from the processed images. This step converts handwritten or printed prescription content into machine-readable text, forming the foundation for subsequent intelligence layers. Given the unstructured and inconsistent nature of medical prescriptions, simple text extraction alone is insufficient. Therefore, Natural Language Processing (NLP) techniques are employed to interpret and structure the extracted content by identifying medicine names, dosage instructions, frequency, and timing.

A Large Language Model (LLM), such as Granite, is used to reason over the extracted prescription data and handle ambiguities commonly found in medical instructions. The model translates complex or unclear dosage details into simple, user-friendly explanations, enabling patients and caregivers to clearly understand when and how medicines should be taken. This reasoning capability also supports conversational interactions, allowing users to ask questions in plain language and receive accurate responses.

Retrieval-Augmented Generation (RAG) is incorporated to ensure reliability and contextual accuracy. Instead of generating responses purely from the model’s general knowledge, RAG grounds answers in the specific prescription data extracted for each user. This approach reduces hallucinations and ensures that responses remain relevant to the uploaded prescription.

An Agentic AI framework orchestrates the overall workflow by coordinating multiple tasks such as image ingestion, text extraction, information parsing, query handling, and reminder preparation. This modular, goal-driven design improves scalability and makes the system easier to extend with additional features.

To support consistent medication adherence, Medi-Mate
