# genkit-promptfoo-sample

This project is a sample implementation demonstrating how to use [Firebase Genkit](https://firebase.google.com/docs/genkit) with [Promptfoo](https://www.promptfoo.dev/), a test framework designed to evaluate the output of generative AI models.

- [Requirements](#requirements)
- [Setup](#setup)
- [Run Genkit](#run-genkit)
- [Evaluation](#evaluation)
- [Making Changes](#making-changes)
- [License](#license)

## Requirements

Before you start, make sure you have these installed:

- **Node.js** version 22 or later
- **npm**
- **Genkit**

For Genkit installation, see the [official guide](https://firebase.google.com/docs/genkit/get-started).

Check your installations by running:

```bash
$ node --version # the below version is on my environment
v22.4.1
$ npm --version # the below version is on my environment
10.7.0
$ genkit --version # the below version is on my environment
0.5.4
```

## Setup

**Install Project Dependencies**: Open your terminal, navigate to this project's folder, and run:

```bash
$ npm install
```

## Run Genkit

1. **Set the `GOOGLE_GENAI_API_KEY` Environment Variable**

Before running the project, you need to provide your Google GenAI API key.

```bash
$ export GOOGLE_GENAI_API_KEY=your_api_key
```

2. **Run the Genkit server locally**

This command starts the project and automatically opens your default web browser to `http://localhost:4000`.

```bash
$ npm run genkit
```

To test the functionality, run the following command:

```bash
$ curl -X POST -H "Content-Type: application/json" -d '{"data":"French"}' http://127.0.0.1:3400/menuSuggestionFlow
{"result":"## **Steak Frites with Béarnaise Sauce**\n\nThis classic French dish is simple, elegant, and always a crowd-pleaser. \n\n**Here's why it's a good menu choice:**\n\n* **Familiar yet elevated:** It's a familiar comfort food with a touch of sophistication.\n* **Versatile:** It can be adapted to different dietary needs (e.g., gluten-free fries, vegetarian alternative like a mushroom steak).\n* **Visually appealing:** A beautifully seared steak with crispy fries and a luscious Béarnaise sauce is very photogenic.\n* **High-quality ingredients:**  It allows you to showcase premium ingredients like a high-quality cut of beef and fresh herbs for the sauce.\n* **French authenticity:** It's a true classic French dish, reinforcing the restaurant's theme.\n\n**To add a unique twist:**\n\n* **Try different cuts of beef:**  Filet mignon, ribeye, or even a hangar steak.\n* **Offer different sauce options:**  Mushroom sauce, peppercorn sauce, or even a light truffle oil.\n* **Add a side:**  A small salad, a side of roasted vegetables, or a creamy potato gratin.\n\n**This dish can be a signature item on your French-themed restaurant menu, appealing to a wide range of diners.** \n"}
```

## Evaluation

To evaluate the flow using [Promptfoo](https://www.promptfoo.dev/), follow these steps:

1. Run the evaluation command:

```bash
$ npm run eval:run
```

2. To view the results, run:

```bash
$ npm run eval:view
```

This will automatically open your browser to `http://localhost:15500`.

You can view the results table here:

![Result Table](https://raw.githubusercontent.com/yukinagae/genkit-promptfoo-sample/main/docs/1.png)

Click the 🔍 icon to see detailed information for each test:

![Test Details](https://raw.githubusercontent.com/yukinagae/genkit-promptfoo-sample/main/docs/2.png)

In the details section, you can review the input and output:

![Input and Output](https://raw.githubusercontent.com/yukinagae/genkit-promptfoo-sample/main/docs/3.png)

Additionally, explanations for each assertion are provided:

![Assertions](https://raw.githubusercontent.com/yukinagae/genkit-promptfoo-sample/main/docs/4.png)

For more extensive testing with Promptfoo, you can customize the configuration by editing the `eval/promptfooconfig.yaml` file. For detailed instructions and additional information, please refer to the [official Promptfoo documentation](https://www.promptfoo.dev/docs/intro/).

## Making Changes

### Building the Project

After making changes, you might need to build the project to see your changes in action:

```bash
$ npm run build
```

### Formatting and Linting

To ensure your code follows the project's coding standards, run the formatting and linting tools:

```bash
$ npm run typecheck # type check without modifying files
$ npm run check     # scan without modifying files
$ npm run fix       # modify files
```

### Kill Existing Processes

Sometimes existing processes are still running, preventing you from running genkit locally because the ports are already in use. In that case, run the following command to kill the processes tied to the ports:

```bash
$ npm run kill
```

## License

MIT
