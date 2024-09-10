# genkit-promptfoo-sample

TODO: description

- [Requirements](#requirements)
- [Setup](#setup)
- [Usage](#usage)
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

## Usage

1. **Set the `GOOGLE_GENAI_API_KEY` Environment Variable**

Before running the project, you need to provide your Gemini API key.

```bash
$ export GOOGLE_GENAI_API_KEY=your_api_key
```

2. **Run the Genkit server locally**

This command starts the project and automatically opens your default web browser to http://localhost:4000.

```bash
$ npm run genkit
```

TODO: call API

```bash
$ curl -X POST -H "Content-Type: application/json" -d '{"data":"French"}' http://127.0.0.1:3400/menuSuggestionFlow
{"result":"## **Steak Frites with Béarnaise Sauce**\n\nThis classic French dish is simple, elegant, and always a crowd-pleaser. \n\n**Here's why it's a good menu choice:**\n\n* **Familiar yet elevated:** It's a familiar comfort food with a touch of sophistication.\n* **Versatile:** It can be adapted to different dietary needs (e.g., gluten-free fries, vegetarian alternative like a mushroom steak).\n* **Visually appealing:** A beautifully seared steak with crispy fries and a luscious Béarnaise sauce is very photogenic.\n* **High-quality ingredients:**  It allows you to showcase premium ingredients like a high-quality cut of beef and fresh herbs for the sauce.\n* **French authenticity:** It's a true classic French dish, reinforcing the restaurant's theme.\n\n**To add a unique twist:**\n\n* **Try different cuts of beef:**  Filet mignon, ribeye, or even a hangar steak.\n* **Offer different sauce options:**  Mushroom sauce, peppercorn sauce, or even a light truffle oil.\n* **Add a side:**  A small salad, a side of roasted vegetables, or a creamy potato gratin.\n\n**This dish can be a signature item on your French-themed restaurant menu, appealing to a wide range of diners.** \n"}
```

Now you can play with it!

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
