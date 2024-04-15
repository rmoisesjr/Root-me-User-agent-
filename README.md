# Root-me-User-agent-
Root-me User-Agent Challenge Walkthrough
Begin by clicking the "Start the Challenge" button, which will redirect you to a webpage displaying: "Wrong user-agent: you are not the 'admin' browser!"

This indicates that you lack the necessary admin privileges to view the page.

Your objective is to view what an actual admin would see. To achieve this, you need to manipulate the traffic going to and from your browser using a tool called Burp Suite.

Burp Suite: Burp Suite is a web application security testing tool.

After downloading Burp Suite, utilize its proxy feature, which is designed for intercepting and modifying HTTP/S requests and responses between your browser and the target web application.

Go to the proxy section of Burp Suite and activate the intercept feature.

Open a browser within Burp Suite.

Visit the page that previously displayed the "not admin" message using the browser within Burp Suite.

Examine the data in the intercept section of Burp Suite.

Since you aim to change your identity on the website from a regular user to an admin, edit the "user-agent" parameter found in the headers of an HTTP GET request.

Once you've made the necessary edits, click forward in Burp Suite to update the targeted website with the modified request.

You should now see the welcome message for the admin along with the flag.

Congratulations! You have successfully solved this challenge.

Weaknesses Exploited:
Not using HTTPS requests instead of HTTP.
Lack of encryption and security measures that prevent an attacker from tampering with the request.

