# AEM Brackets Extension
![](https://raw.githubusercontent.com/wiki/adobe-marketing-cloud/aem-brackets-extension/screenshots/brackets.png)

This extension provides a smooth workflow to edit AEM components and client libraries, and leverages the power of the [Brackets](http://brackets.io) code editor, which gives access from within the code editor to Photoshop files and layers. The easy synchronization provided by the AEM Brackets Extension (no Maven or File Vault required) increases developer efficiency and also helps front-end developers with limited AEM knowledge to participate on projects. This extension also provides some [HTL](https://github.com/Adobe-Marketing-Cloud/htl-spec) support, a template language that takes away the complexity of JSP to make component development easier and more secure.

## Documentation
Please refer to the [documentation page](http://docs.adobe.com/content/docs/en/dev-tools/aem-brackets.html) for instructions on how to install the extension, as well as detailed information about the features.

## Get Started
If you don't have of your own a project with a content-package to try out, you can try out the [HTL TodoMVC Example](https://github.com/Adobe-Marketing-Cloud/aem-htl-sample-todomvc) sample application that was built with the AEM Brackets Extension. Download the ZIP from GitHub, extract the files locally, open the `jcr_root` folder in Brackets, setup the Project Settings, and upload the whole package to your AEM development instance by doing an Export Content Package.

After these steps, you should be able to access the `/content/todo.html` URL on your AEM development instance and you can start doing modifications to the code in Brackets and see how, after doing a refresh in the web browser, the changes were immediately synchronized to the AEM server.

## Known Issues or Limitations
* Embedded content packages are not supported.

## Reporting Bugs
Please report any issues you encounter using GitHub's [issue tracker from](https://github.com/Adobe-Marketing-Cloud/aem-brackets-extension/issues).

In order to help us investigate the reported issues, please include at minimum, the following information:

1. Brackets version (e.g. sprint 42)
2. AEM Brackets Extension version (e.g. 0.0.4)
3. OS and architecture (e.g. Windows 8.1 x64, Mac OS X 10.9.4, Ubuntu 14.04 32-bit, etc.)
4. a brief list of steps to reproduce the issue; in case there's a complex setup involved, please provide a testing content-package)
5. the expected outcome
6. the actual outcome

You can use the following Markdown template:
```markdown
**Brackets version:** sprint 42  
**AEM Brackets Extension:** 0.0.4  
**OS and architecture:** Windows 8.1 x64  

#### Steps to reproduce:
1. use content package [my-content](http://www.example.com/my-content.zip)
2. step 2
3. step 3

#### Expected outcome
It works!

#### Actual outcome
It actually doesn't...
```

## Development
The AEM Brackets Extension is a Node.js module. The following steps need to be followed if you want to start hacking on new features:

1. install [Node.js](http://nodejs.org/ "node.js") for your platform
2. clone this repository
    
    ```bash
    git clone git@github.com:Adobe-Marketing-Cloud/aem-brackets-extension.git
    ```
3. in the `aem-brackets-extension` folder run
    
    ```bash
    npm install
    grunt
    ```

## Credits
* [Nicolas Peltier](https://github.com/nicolasATadobe): Initial plug-in with HTL support (syntax highlighting and auto-completion for expressions and statements), and synchronisation to AEM (automatic and manual import and export).
* [Radu Cotescu](https://github.com/raducotescu): Added project preferences, improved synchronisation to use the Package Manager HTTP Service API, added support for `filter.xml` rules, enhanced UI with sync notifications.
