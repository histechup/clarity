# Clarity
Clarity is a behavioral analytics library written in javascript. It helps you understand how users view and use your website across all modern devices and browsers. Understanding how users navigate, interact and browse your website can provide new insights about your users. Empathizing with your users and seeing where features fail or succeed can help improve your product, grow revenue and improve user retention.

Clarity provides you all these insights by:
* Observing content layout, viewport, and user's interactions with the page
* Inspecting network requests on the page
* Logging the event stream in JSON format to a configurable endpoint

Clarity is a project in active development. While it's not yet ready for production use, we continue making improvements and encourage the community to join us in the process.

## Project Structure
1. **[clarity-js](https://github.com/microsoft/clarity/tree/master/packages/clarity-js)**: Instrumentation code that goes on the website and tracks user interactions as well as layout changes. It is responsible for batching all captured events, computing metrics and encoding data to minimize bytes sent over the wire.

2. **[clarity-decode](https://github.com/microsoft/clarity/tree/master/packages/clarity-decode)**: Code, which usually runs on the server, decodes incoming data back into its original format. From analytics perspective, all analysis should happen on data coming out of decode module and should never run on encoded data from clarity-js directly.

3. **[clarity-visualize](https://github.com/microsoft/clarity/tree/master/packages/clarity-visualize)**: This is what makes Clarity visual and intuitive. It takes the decoded data from clarity-decode and turns it back into pixel-perfect session replay, exactly how the user saw it.

4. **[clarity-devtools](https://github.com/microsoft/clarity/tree/master/packages/clarity-devtools)**: This is a developer tools extension for chromium based browsers. It demonstrates how various components of Clarity come together and enables live session captures against any website, including downloading event data.

## Examples
Here are some example sessions on popular websites visualized to demonstrate the telemetry captured:
1. CNN (Web)
</br><a href="https://thumbs.gfycat.com/AggressiveLankyAbyssiniangroundhornbill-size_restricted.gif"><img src="https://thumbs.gfycat.com/AggressiveLankyAbyssiniangroundhornbill-size_restricted.gif" title="Clarity - CNN Example"/></a>

2. Cook with Manali (Mobile)
</br><a href="https://thumbs.gfycat.com/CoolDependableAdamsstaghornedbeetle-size_restricted.gif"><img src="https://thumbs.gfycat.com/CoolDependableAdamsstaghornedbeetle-size_restricted.gif" title="Clarity - Cook With Manali Example"/></a> 

## Project Goals
* Enable a generic solution that is able to capture telemetry from third-party websites
* Encourage participation from open-source community
* Minimal configuration required by third party web-sites to get started
* Mobile first

## Privacy Notice
Clarity handles sensitive data with care. By default content on the page is masked before upload, so no actual text from the page is sent to the server.

## Improving Clarity
If you haven't already done so, start contributing by following instructions **[here](https://github.com/microsoft/clarity/blob/master/CONTRIBUTING.md)**.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

Happy coding!
