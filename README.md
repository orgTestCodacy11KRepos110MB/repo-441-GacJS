# GacJS

**Read the [LICENSE](https://github.com/vczh-libraries/GacJS/blob/master/LICENSE.md) first.**

Running GacUI in Browsers!

## Source code is abondoned. This repo will be used to port GacUI to WebAssembly. All content will be deleted later.

## Notice

Some content is under development. I will keep all code compatible across browsers by only testing the code using the **latest version of IE, Firefox and Chrome**. After Windows 10 releases, Edge will be included.

In the future, GacGen.exe can translate GacUI XML resource files to javascript codes, mapping all classes to javascript. You can just create an instance of your control class and plug it in the DOM tree at wherever you want, and the UI will appear in the web page.

This project's priority is not very high. The first step is to re-implement GacUI's layout system using javascript, and then use it to develop the GacUI document generator with C++ and XML comments.

## Running test pages

Running test pages is very simple, just follow the steps:
* Clone this repo to your disk.
* Create a web site on the cloned folder using IIS.
* Launch http://127.0.0.1:< port >/Entrance.html according to your configuration.

## Content

* **[Package.js](https://github.com/vczh-libraries/GacJS/blob/master/Script/Package.js)** : A package infrastructure. All JavaScript components in this project will be build as packages. You don't need to worry about the order -- except that **Package.js** should be the first one -- when including coupled JavaScript files in your HTML document.
* **[Test.js](https://github.com/vczh-libraries/GacJS/blob/master/Script/Test.js)** : A very simple unit test framework, that only me will use it.
* **[Class.js](https://github.com/vczh-libraries/GacJS/blob/master/Script/Class.js)** : An object oriented type definition library for translating Workflow script to Javascript, including
    * Inheritance and virtual inheritance.
    * Virtual, Override and New functions.
    * Private, Protected and Public functions. Which means that, inside the class all code can see private and protected members, but outside the class only public members are visible.
    * Properties and Events.
    * POD
    * Enum
    * Unit test for Class.js in **[Class.html](https://github.com/vczh-libraries/GacJS/blob/master/Class.html)**.
* **[Html/](https://github.com/vczh-libraries/GacJS/tree/master/Script/Html)** : HTML related packages.
   * **[Events.js](https://github.com/vczh-libraries/GacJS/blob/master/Script/Html/Events.js)** : A general custom event framework.
   * **[RunAfterWindowLoaded.js](https://github.com/vczh-libraries/GacJS/blob/master/Script/Html/RunAfterWindowLoaded.js)** : Execute a function. If window is not loaded then delay the execution.
   * **[ResizeEvent.js](https://github.com/vczh-libraries/GacJS/blob/master/Script/Html/ResizeEvent.js)** : ConnectionToBodyChanged and Resize custom event that works on every elements.
   * **[Navigation.js](https://github.com/vczh-libraries/GacJS/blob/master/Script/Html/Navigation.js)** : A pure front-end navigation system driven by hash in the url. Test page: **[Navigation.html](https://github.com/vczh-libraries/GacJS/blob/master/Navigation.html)**.
   * **[Razor.js](https://github.com/vczh-libraries/GacJS/blob/master/Script/Html/Razor.js)** : Razor template engine driven by JavaScript. Test page: **[Razor.html](https://github.com/vczh-libraries/GacJS/blob/master/Razor.html)**.
* **[IO/](https://github.com/vczh-libraries/GacJS/tree/master/Script/IO)** : IO related packages.
   * **[Delay.js](https://github.com/vczh-libraries/GacJS/blob/master/Script/IO/Delay.js)** : A delay execution framework. Test page: **[Navigation.html](https://github.com/vczh-libraries/GacJS/blob/master/Delay.html)**.
   * **[Wildcard.js](https://github.com/vczh-libraries/GacJS/blob/master/Script/IO/Wildcard.js)** : Convert wildcards to regular expressions. Test page: **[Navigation.html](https://github.com/vczh-libraries/GacJS/blob/master/Wildcard.html)**.
   * **[Resource.js](https://github.com/vczh-libraries/GacJS/blob/master/Script/IO/Resource.js)** : A delay static resource loader. Test page: **[Navigation.html](https://github.com/vczh-libraries/GacJS/blob/master/Resource.html)**.
* **[GacUI/](https://github.com/vczh-libraries/GacJS/tree/master/Script/GacUI)** : GacUI in Browsers!.
   * **[Types.js](https://github.com/vczh-libraries/GacJS/blob/master/Script/GacUI/Types.js)** : Basic types that used in GacJS.
   * **[Elements/](https://github.com/vczh-libraries/GacJS/tree/master/Script/GacUI/Elements)** : GacUI Predefined Graphic Elements. Test page: **[Element.html](https://github.com/vczh-libraries/GacJS/blob/master/Element.html)**.
      * **[Interface.js](https://github.com/vczh-libraries/GacJS/blob/master/Script/GacUI/Elements/Interface.js)**
      * **[Basic.js](https://github.com/vczh-libraries/GacJS/blob/master/Script/GacUI/Elements/Basic.js)**
      * **[ColorizedText.js](https://github.com/vczh-libraries/GacJS/blob/master/Script/GacUI/Elements/ColorizedText.js)**
      * **[Document.js](https://github.com/vczh-libraries/GacJS/blob/master/Script/GacUI/Elements/Document.js)**
   * **[GacUI/Layout/](https://github.com/vczh-libraries/GacJS/tree/master/Script/GacUI/Layout)** : GacUI Predefined Layout Components. Test page: **[Layout.html](https://github.com/vczh-libraries/GacJS/blob/master/Layout.html)**.
      * **[Basic.js](https://github.com/vczh-libraries/GacJS/blob/master/Script/GacUI/Layout/Basic.js)**
      * **[Bounds.js](https://github.com/vczh-libraries/GacJS/blob/master/Script/GacUI/Layout/Bounds.js)**
      * **[Stack.js](https://github.com/vczh-libraries/GacJS/blob/master/Script/GacUI/Layout/Stack.js)**
      * **[Table.js](https://github.com/vczh-libraries/GacJS/blob/master/Script/GacUI/Layout/Table.js)**
      * **[Misc.js](https://github.com/vczh-libraries/GacJS/blob/master/Script/GacUI/Layout/Misc.js)**
   * **Templates.js**
   * **Controls.js**
