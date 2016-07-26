# &lt;wc-vanilla-textbox&gt;

> Custom Input box built using vanilla web component

	
## Prerequisites

In order to run it locally you'll need to fetch some dependencies and a basic server setup.

1. Node.js v4.4.7+

2. npm v2

3. Install bower and bower-cli as global module

 	 	npm install -g bower
		npm install -g bower-cli

4. Install [polyserve](https://npmjs.com/polyserve):

 	 	npm install -g polyserve

Note : polyserve works only with Node.js v4.x.x +	

## Install

Install the component using [Bower](http://bower.io/):

```
bower install wc-vanilla-textbox --save
```

Or [download as ZIP](https://github.com/disney/wc-vanilla-textbox/archive/master.zip).

## Usage

1. Import polyfill:

    ```html
    <script src="bower_components/webcomponentsjs/webcomponents.min.js"></script>
    ```

2. Import custom element:

    ```html
    <link rel="import" href="bower_components/wc-vanilla-textbox/wc-vanilla-textbox.html">
    ```

3. Start using it!

    ```html
    <wc-vanilla-textbox></wc-vanilla-textbox>
    ```


## Development


1. Install local dependencies:

    ```
    bower install
    ```

2. Start development server and open `http://localhost:8080/components/wc-vanilla-textbox/`.

    ```
    $ polyserve
    ```

3.  Test in IE11+ , latest google chrome and firefox browser
 
## Known Issues
1. Since multiple shadow DOM is not supported anymore and web components is in working draft, creating custom elements by extending Native HTML element using shadow DOM using **vanilla Components** is not currently supported. It throws below error :	
Note :  But is works with polymer Shady DOM. 
		
		Uncaught InvalidStateError: Failed to execute 'createShadowRoot' on 'Element': 
		Shadow root cannot be created on a host which already hosts an user-agent shadow tree.


2. Since shadow DOM is not used, styling of custom elements are not encapsulated. This means it cannot prevent application/document level styles from leaking into into custom elements using **vanilla Components**. But it can, however prevents leaking styles of custom elements to outside world. But is works with polymer Shady DOM.  Styling of host element using :host is not  working. Instead use something like this **input[is="wc-vanilla-textbox"]**. 


		
		