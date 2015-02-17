### Using the Browser Console and "console.log()"

One of the nice things when using JavaScript to manipulate web pages, is that we can get feedback in the browser. We use the browser console for this. We can also write JavaScript directly into the console and see the results.

Things to try out: 

1. Open the *index.html* file in this directory and write the following between the &lt;script&gt; tags: 
```javascript
	var mystring = "Hello world!";
	console.log(mystring);
```

2. Open up *index.html* in a browser. Then use *"Ctrl + Shift + I"* (or *"Cmd + Shift + I"*) on a Mac to open the dev tools including the browser console. You should see "Hello world" in the console.

3. Try adding something like this to the script in your *index.html* file:
```javascript
var message = Hi;
```
When you refresh the browser, you will get an error message in the console. This is because string variables always need to be in quotes. Otherwise the value is seen as a variable, and because a variable Hi has not been defined, an error is thrown.

4. We can run JavaScript directly in the console. For example, type in *4 + 3* and press Enter

Some notes: 

 You can also use the *alert()* function to make values visible in the browser. This will create a popup showing the value. But in most cases *console.log()* is the preferable method.

 The rest of the dev tools (in Google Chrome or Firefox) are also very useful. Check out [https://developer.chrome.com/devtools](https://developer.chrome.com/devtools) for the Google Chrome Dev Tools and [https://developer.mozilla.org/en/docs/Tools](https://developer.mozilla.org/en/docs/Tools) for Firefox.

 Another useful tool is [JSHint](http://jshint.com/) which checks for errors and potential problems in your code. 








