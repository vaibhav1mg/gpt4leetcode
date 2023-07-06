# GPT4LeetCode



GPT4LeetCode is a solution generator for Data Structure and Algorithm (DSA) problems, leveraging the capabilities of OpenAI's GPT-4. The tool accepts DSA problem statements, test cases, and expected outputs, and generates Python code to solve the problem. 

![[Project Image 1]([https://i.ibb.co/VJ85xNr/image.png])](https://i.ibb.co/VJ85xNr/image.png)

## Features

- **GPT-4 Integration**: Utilizes the advanced natural language processing abilities of GPT-4 to generate Python code.
- **Local Code Execution**: Executes the generated Python code locally in a secure environment.
- **Automated Testing**: Compares the output of the executed code against the expected results from the provided test cases.
- **Iterative Improvement**: In case of mismatch, the system iterates the process by incorporating the incorrect output as additional context in the problem statement.
- **Manual Override**: Prevents infinite iterations and resource wastage in case of non-convergent scenarios.

## Tech Stack

- **Backend**: Python, Node.js with Express
- **Frontend**: React, Vite, Tailwind
- **AI**: OpenAI's GPT-4

## Setup

1. **Frontend .env**

    Create a `.env` file in the frontend directory with the following content:

    ```
    VITE_BACKEND_URL = 'http://localhost:8000' # or your express/nodejs server
    ```

2. **Backend .env**

    Create a `.env` file in the backend directory with the following content:

    ```
    PASSWORD = 'your-password' # common password you wanna set for authentication
    OPENAI_API_KEY = 'your-gpt-4-API-key' # your gpt-4 API key
    ```

    Note: You can change the model from `model: "gpt-4"` to `gpt-3 turbo` but it's not preferred for complex questions.

3. **Password Setup**

    On the site, in the sidebar, save the password set in the backend `.env`.

## Challenges

- **Token Limit**: GPT-4 has a maximum limit of 8000 tokens for input and output combined. Careful management of problem statements and test cases is required.
- **Stateless Nature**: GPT-4 does not retain any memory of past requests or outputs. Every new request needs to contain all relevant information.
- **Security**: The security of code execution and the effectiveness of the comparison mechanism between produced and expected results are crucial.
- **Efficiency**: The iteration process and speed of response from GPT-4 need to be optimized for an improved user experience.

## Contributing

We welcome contributions! Please see the [contributing guide](CONTRIBUTING.md) for more details.

## License

This project is licensed under the terms of the MIT license. See the [LICENSE](LICENSE.md) file for details.
