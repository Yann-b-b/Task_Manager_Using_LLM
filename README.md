


### Task Partitioner

This is a modular task breakdown tool powered by LLMs. It takes in a user prompt describing a task and returns subtasks in a structured format.

### Modular Design

- The backend is designed to be easily customizable. You can:
  - **Modify the prompt** inside `backend/socket_server.py` to change how tasks are partitioned.
  - **Swap the Ollama model** to any local model available on your machine (e.g., `llama3`, `mistral`, etc.). Just replace the model name in the subprocess call.

---

### Running the Project

1. **Run the Backend**
    - Open a terminal at the root of the project
    - Navigate to the backend folder:
      ```bash
      cd backend
      ```
    - Run the server:
      ```bash
      python server.py
      ```

2. **Run the Frontend**
    - Open another terminal at the root of the project
    - Navigate to the frontend folder:
      ```bash
      cd frontend
      ```
    - Serve the frontend with:
      ```bash
      python -m http.server
      ```

3. **View the App**
    - Open a browser and go to:  
      `http://localhost:8000/`

---

### Customization Tips

- **Backend Prompt & Model**
  - To change the LLM used, update the model name in the backend’s `subprocess.run()` or similar call.
  - You can tailor the task breakdown logic and instructions passed to the model to suit various workflows (e.g., coding tasks, research planning, multi-step workflows).

- **Frontend Styling**
  - The UI is styled with `style.css` and includes interactive flip animations and a wave-loading indicator.
  - Responsive and accessible design with keyboard and click support.

---

This framework makes it easy to plug-and-play different models and prompting techniques to experiment with intelligent task decomposition.