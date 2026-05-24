Reflection:
1. How did your prompt evolve across iterations?
The prompt evolved from a basic instruction-based approach to a structured and constrained extraction system.
In the initial iteration, the model was asked to summarise meeting content and identify risks and next steps. While this produced usable outputs, the structure was inconsistent, and the model occasionally introduced inferred or generic information.
In the second iteration, a strict JSON schema was introduced. This significantly improved the organisation of the output, ensuring that each response followed a predefined format. Additionally, grounding instructions were added to limit the model to information contained within the uploaded documents.
The final iteration introduced strong constraints and evidence-based extraction rules. The model was explicitly instructed not to infer or generalise and to include supporting evidence for risks and key insights. This resulted in more reliable, traceable, and production-ready outputs.
Overall, the evolution focused on moving from flexibility to control, improving both accuracy and consistency. 
2. What model selection trade-offs did you observe?
The primary trade-off was between speed, cost, and reasoning capability.
•	Gemini Flash performed well for rapid iteration, providing quick responses with acceptable accuracy. It was particularly useful during prompt development.
•	Gemini Pro, while slower, provided more accurate and context-aware outputs, especially when handling complex or ambiguous meeting content.
This highlighted a common production consideration:
•	Use lighter models for real-time interaction
•	Use more advanced models for critical reasoning tasks
3. How did Stitch accelerate or constrain UX design?
Stitch significantly accelerated the UI design process by allowing rapid generation of high-quality interface mockups from simple prompts. This eliminated the need for manual design work and enabled quick iteration of layouts.
However, Stitch also introduced constraints:
•	Limited customisation options
•	Lack of interactivity in generated screens
•	Static outputs (PNG) rather than functional UI
Despite these limitations, Stitch was effective for prototyping and demonstrating UX concepts, which aligns with the assignment requirements.

4. What would you change to productionise this system?
To productionise this system, several improvements would be required:
Technical Enhancements
•	Implement a backend API (e.g., FastAPI)
•	Deploy using Cloud Run for scalability
•	Add structured output validation (schema enforcement)
Data Handling
•	Improve document parsing via chunking
•	Introduce semantic search for large documents
•	Add caching for repeated queries
Reliability & Monitoring
•	Add logging and traceability
•	Monitor model responses for failures
•	Implement fallback mechanisms
UX Improvements
•	Replace static UI with interactive frontend
•	Add loading states and error handling
•	Enable user feedback and editing
These enhancements would transform the solution from a prototype into a scalable, deployable AI application.
