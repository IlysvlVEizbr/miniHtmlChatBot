# miniHtmlChatBot
Native HTML frontend that can directly connect to OpenAI-like APIs without additional server-side programs or dependency libraries

## Usage
1. Determine the user's preferred language
- Chines：[main.html](main.html)
- English：[main_en.html](main_en.html)
2. Modifying API related parameters
- Update the parameter `ApiUrl`, `ApiKey` and `ApiModel` in the HTML (costs will be borne by yourself).
- To use SiliconFlow's free API, simply register on the [SiliconFlow website](https://siliconflow.cn/) and generate your API key. Then fill in the `ApiKey`.
3. Open the corresponding HTML file directly using your browser.

### Example Running Effect
<img src="https://i.ibb.co/NK53JRZ/image.png" alt="Running Effect"></img>

## Features / Highlights
- The typical features provided by the `web_demo` based on `Gradio`: multi-round conversation, clear history, regenerate (last) result
- Pre-defined system prompt options + Customizable system prompt word input
- Multiple model selection options available for anytime switching
- AI-generated dialogue title (consumes significant tokens when enable, disable by default)
- Quickly start a conversation via URL parameters, which can be utilized as a customized search engine. URL combination rule: `[HTML file URL]?s=[URL-encoded user prompt]`
- Implemented in a single HTML file, <20kB in size
- Support conversion of some Markdown syntax content to HTML for display

## Original intention of development
After the release of LLM open source models, it usually comes with a `web_demo` for basic usage. One of the most commonly used methods for implementing `web_demo` is `Gradio`. Although `Gradio` can also be integrated with AI APIs, it requires a Python backend running somewhere and has certain requirements for Python versions, which is not very convenient. It does not meet the need for accessing APIs anytime and anywhere using devices like smartphones.

Therefore, I created this project where users can access AI APIs through a frontend interface simply by opening a local file in their browser. To enhance loading speed, I **did not utilize** any dependency libraries or front-end frameworks; instead, I implemented both the appearance and logic using vanilla `html / css / javascript`.

You can also use this HTML as a starting point for building more complex AI apps.

## Acknowledgments
- Thank [SiliconFlow](https://siliconflow.cn/) for providing free APIs
- Thank [Gradio](https://www.gradio.app/) for offering design and code logic references
- Thank [HTMLPAGE](https://htmlpage.cn/) for providing interface design assistance tools
