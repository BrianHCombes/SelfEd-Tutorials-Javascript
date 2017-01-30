#**SelfEd - Javascript - Asynchronous Calls**#
**SelfEd**          |  **Info** 
------------------- | ------------------------------------------------------------------------
**Date:**           | 11/27/2016
                    | 01/27/2017 (Update)
**Archive_Title:**  | SelfEd-Javascript-Functions-Asynchronous-Calls
**Objective:**      | To better understand asynchronous functions (calls) to better understand things like 'promises'
**Catalyst:**       | Was reviewing node.js, namely these references:
                    | [nodeJS callbacks](https://www.tutorialspoint.com/nodejs/nodejs_callbacks_concept.htm)
                    | [SelEd-Javascript-Functions-Closures]()
                    | [SelfEd-NodeJS-Server-Creating-Of-B]()
                    | and still felt unsatisfied about the underlying mechanism that makes a function asynchronous. Explanations seemed lacking and examples seemed overly complex. But I have a hunch and am developing that hunch in this SelfEd.


**References:**       | **Sites visited to learn and apply to this SelfEd**
----------------------|-----------------------
1                     | http://javascriptissexy.com/understand-javascript-callback-functions-and-use-them/
2                     | http://edumaven.com/javascript-programming/passing-function-as-parameter
3                     | http://javascriptissexy.com/understand-javascript-closures-with-ease/
4                     | https://www.smashingmagazine.com/2014/07/dont-be-scared-of-functional-programming/
5                     | http://recurial.com/programming/understanding-callback-functions-in-javascript/

Process:

Load this SeflEd in a broswer for the instructional reading of it.     
(or)    
Use the Plunker link below (preferred).    

- **[View This SelfEd in Plunker](https://plnkr.co/edit/vaAyx2nm6eVaW3rhJUy5?p=preview)**    
 **Note:** This SelfEd on function closures is simple. Please refer to the sites I visited (links above) for more depth on the subject. 





      SelfEd Date:        11/27/2016

      SelfEd Title:       SelfEd-Javascript-Functions-Asynchronous-Calls

      SelfEd Objective:   To better understand asynchronous functions (calls) to better
                          understand things like 'promises'

SelfEd Catalyst:    Was reviewing node.js, namely these references:
                    
                    https://www.tutorialspoint.com/nodejs/nodejs_callbacks_concept.htm
                    SelEd-Javascript-Functions-Closures
                    SelfEd-NodeJS-Server-Creating-Of-B

                    and still felt unsatisfied about the underlying mechanism that
                    makes a function asynchronous. Explanations seemed lacking and
                    examples seemed overly complex. But I have a hunch and am
                    developing that hunch in this SelfEd.

SelfEd References:  Primary tutorial credit goes to:
                    Christopher Buecheler. His tutorial that helped me the most
                    is here: http://cwbuecheler.com/web/tutorials/2013/javascript-callbacks/

                    https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/async_function
                    https://blog.ometer.com/2011/07/24/callbacks-synchronous-and-asynchronous/
                    http://callbackhell.com/ (Lots of good explanation in this one)
                    http://esbueno.noahstokes.com/post/77292606977/self-executing-anonymous-functions-or-how-to-write


                    http://stackoverflow.com/questions/6921895/synchronous-delay-in-code-execution
                    http://esbueno.noahstokes.com/post/77292606977/self-executing-anonymous-functions-or-how-to-write
                    https://www.impressivewebs.com/callback-functions-javascript/
                    http://cwbuecheler.com/web/tutorials/2013/javascript-callbacks/
                    http://softwareengineering.stackexchange.com/questions/194580/how-does-javascript-code-become-asynchronous-when-using-callbacks
                    
                    SelfEd: SelfEd-Javascript-Functions-Passing-Of

Process:

    First Approach: call setTimeout() functions within defined functions

    I decided to set up three functions called time1, time2, time3. I installed
    the setTimeout() function in each one. I set them to 1000, 2000, 3000
    milliseconds and called them upon page load. They executed accordingly.
    But now I wonder if the setTimeout() function is asynchronous itself. 
    So I looked it up.

    Amazingly one web page I found lays out an experiment very much like to my 
    approach. It is:

                    http://www.hiddenwebgenius.com/blog/guides/understanding-javascripts-asynchronous-code/
                    https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/async_function

    12/3/2016 Note: My quest for asynchronous javascript without the help of NodeJS is not complete.            

    12/4/2016 Note: I'm back trying to better grasp how callback functions work. I'm fairly comfortable
                    using them but I want to know how they work. Heres a hopeful reference:

                    http://cwbuecheler.com/web/tutorials/2013/javascript-callbacks/

                    I decided to follow this guy's tutorials on callbacks. He seems to
                    break it down nicely into progressively understandable 
                    examples.

                    Refer to file callback_Exp0.html where I started

                    Got to creating callback_Exp2.html when: I wondered what makes
                    javascript know it's encountered a function meant to be 
                    asynchronous?

                    I queried the question and found this link:

                    http://softwareengineering.stackexchange.com/questions/194580/how-does-javascript-code-become-asynchronous-when-using-callbacks

                    Seems the opening question is exactly what I'm thinking.

    01/06/2017
    This is a return visit. I'm working on:
                < SelfEd-Angular-Practice-ProjectA-HTTP-Service > 
    See < code section AAA > in file: < Client-Server_Exp4.html >          
    I have a working RESTful call ($http.get) in file: 
    < Client-Server_Exp3.html > 
    and have a problem where I'm receiving an empty object from a RESTful
    service, namely < $http.get >. I suspect the behavior is because the code
    is not behaving asynchronously. It's supposed to wait for the < $http.get >
    server call to return something. I think it's blazing right past the server
    call. This has lead me to the < .then() > method and promises. These objects
    are Javascript objects and don't seem exclusive to Angular. Yeah!
    Going to the < Promise > link below looks like good reading.

    < https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/then >
    < https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise >

    All this seems good for fully deciphering the nuances and management of
    asynchronous functions. 

    The catalyst for this quest is because I'm moving an < $http.get > service
    from a controller to a service method. And as usual it doesn't work which
    means I don't understand something.

    http://andyshora.com/promises-angularjs-explained-as-cartoon.html

    01/11/2017
    I think I have a little more understanding of asynchronous functions. 
    Refer to file:  < callback_Exp2.html > of which I've done more work on.
    The setTimeout function is used for the asynchronous behavior. 
    As it turns out, all functions outside the setTimeout function are 
    executed right away. The setTimeout function and all functions within
    the setTimeout function are executed after the time out completes.
    It seems kinda obvious now. Load the page to see what's up.

    But last and maybe the most important thing!!!!!!!!!!!!!!!!!!!!!!!!!!!!
    Asynchronous behavior appears exclusive to system or query level calls.
    setTimeout() is a call to the system. A query is a call to a server, etc.
    These are things outside of the javascript sandbox.
    
    ****************************************************************************
    Publishable     Publishable     Publishable     Publishable    Publishable
    ****************************************************************************