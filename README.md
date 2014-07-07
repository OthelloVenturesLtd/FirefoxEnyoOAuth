Version 1.0
oauthiframe.js - an Enyo kind for handling OAuth Authentication in Firefox OS
Inspired by the webOS OAuth library at https://github.com/ionull/webOS-OAuth2

In order to use this kind, your app will need to be a privileged app with permission to access the Browser API.
For More Info, See: https://developer.mozilla.org/en-US/docs/Web/API/Using_the_Browser_API

NOTE: You will need to supply your own UI Chrome (ie. buttons, etc.) these can be hooked into this kind by using the
this.$.oAuthIFrame.eventNode object.

USAGE:
	var oauthConfig={
		authorizeUrl: "url", // Your provider's Authorize URL
		accessTokenUrl: "url", // Your provider's Access Token URL
		accessTokenMethod: "POST", // Optional - "GET" by default if not specified
		client_id: "ID", // The Client ID assigned to you by your provider
		client_secret: "SECRET", // The Client Secret assigned to you by your provider
		redirect_uri: "http://localhost", // Optional - The redirect URL registered with your provider. "oob" by default if not specified
		response_type:"code", // One of code or token. Right now, only code is supported.
		scope: ["scope"], // An array of scope names that you are requesting permission to access.
		additionalParameters: "params" // Optional - Any additional parameters required by your provider. IE. AOL Reader requires "&supportedIdType=facebook,google,twitter" to enable all auth types.
	}
	
	this.$.oAuthIFrame.beginOAuth(oauthConfig)
	
Don't forget to catch the events.

LICENSE:

The MIT License (MIT)

Copyright (c) 2014 Othello Ventures Ltd.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
