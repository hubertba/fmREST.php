# fmREST.php

A free tool from soSIMPLE Software

Simplifies & manages PHP connections to FileMaker 17’s REST-based Data API.

NOTE: UPGRADED TO WORK WITH FILEMAKER 17. NO LONGER WORKS WITH FILEMAKER 16 - use a earlier branch for that. 
Also note, FileMaker 16 Data API is trial mode only and will stop working on September 18, 2018.

We created this class file to make it easier to manage dynamic REST sessions for soSIMPLE and our custom development. The goal of the class file was to help PHP developers start using the new REST engine as quickly and easily as possible.

# What fmREST.php does:

- Makes every REST call available as a PHP function.
- Automatically login into FileMaker Server whenever you call any REST functions
- Saves your token for 15 minutes to reuse
- Checks for a broken or disconnected token and automatically reconnects and runs your function again

# Documentation:
Sample.php is a simple form that demonstrates most of the calls available by the fmREST.php class.

1. Follow the setup instructions on our site and FileMaker's site for the Data API (see link below)
2. Place the class file (fmREST.php) and the sample file (sample.php) in the https root of your FileMaker Server-hosted web server directory (See FileMaker Server docs for location). You can also host the php scripts on any other php enabled web server that can connect to your FileMaker Server address. 
3. Create a new Contacts.fmp12 based on the FileMaker sample template of the same name (be sure you're using the Contacts file from the "Sample" area, not the "Starter" area. Upload this file to your FileMaker Server 17.
4. Add a user with the name "rest" and the password "rest" 
5. Assign this user to a privilege set with the extended privilege "fmrest" 
6. Load sample.php in a web browser over https protocol. You should see a form that will allow you to do simple record modification. (The sample form will still work without ssl, but the tokens will not be saved between calls so you will see multiple REST connections on your FileMaker Server).

For complete documentation and support please visit out website:
http://www.sosimplesoftware.com/fmrest.php

We’ll also be updating it with new features. If you’d like to add something to it or have any comments, please let us know.

Copyright 2017 Paradise Partners, Inc DBA soSIMPLE Software / Ken d'Oronzio

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
