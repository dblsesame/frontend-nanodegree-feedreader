# Project Overview

In this project I have added jasmine test suite to existing code base.
The test suites spec is at jasmine/spec/feedreader.js and they are

RSS Feeds
The menu
Initial Entries
New Feed Selection

Because the spec is loaded at the same html page so the DOM elements are available in the tests there is little need to create mock objects.  I can directly check the DOM elements.

In the menu test suite, I do have to call the click method to simulate the menu icon click event.

Jasmine done function is used in beforeEach block to ensure the test is done after the async call is finished for the Initial Entries test suite.

For the New Feed Selection test suite, I nested it inside the Initial Entries suite to ensure both async calls are completed.

# Reference
http://jasmine.github.io/2.0/introduction.html
http://stackoverflow.com/questions/6514048/how-do-you-use-jasmine-to-test-a-jquery-click-function-to-see-if-it-called-a-cus
http://stackoverflow.com/questions/9532639/how-check-if-body-has-a-specific-class-with-javascript

