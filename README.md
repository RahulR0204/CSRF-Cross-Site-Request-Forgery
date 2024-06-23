# Cross-Site Request Forgery (CSRF)

Cross-Site Request Forgery (CSRF) is a type of security vulnerability found in web applications. Also known as XSRF, Session Riding, or one-click attacks, it tricks a web browser into executing an unwanted action on a trusted site. The attacker abuses the trust that a web application has for the victim’s browser, exploiting the trust a web application has in an authenticated user.

## Execution Method of CSRF 

1. **Social Engineering**: Attackers use social engineering techniques to persuade the victim to click a link via email, chat message, or similar form of communication.

2. **Triggering Requests**: Either the malicious link itself, or a web page the user visits, triggers a request to the targeted site.

3. **User's Session Exploitation**: The request supposedly comes from the user, and takes advantage of the fact that the user is already signed into the website.

4. **Unwanted Actions**: The website acknowledges the request and performs the attacker’s requested action, without the user’s knowledge or consent.

## Git Link

[https://shorturl.at/csoHP](https://shorturl.at/csoHP)

## Preventive Measures

### 1. Anti-CSRF Tokens

Tokens that are unique to each session or request, embedded in forms or URLs, and verified by the server upon form submission or request.

### 2. Same Site Cookie Attribute

A cookie attribute that restricts how cookies are sent with cross-site requests.

**Example:**

- **SameSite=Strict**: The cookie is not sent with any cross-site requests.
- **SameSite=Lax**: The cookie is sent with top-level navigations but not with third-party contexts (e.g., embedded iframes).
- **SameSite=None**: The cookie is sent with cross-site requests, but only if Secure is also set.

### 3. Origin and Referrer Headers:

 Validate the Origin and Referer headers on incoming requests. Ensure that requests originate from trusted domains and reject requests with unexpected origins or missing/invalid referrers.

### 4. Session Management: 

Implement secure session management practices, such as expiring sessions after a period of inactivity, using secure cookies, and ensuring sessions are invalidated properly after logout.


## Usage 
Clone the repository:
```bash
git clone git clone https://shorturl.at/csoHP
cd csoHP
```


Explore the code and documentation to understand and defend against CSRF attacks effectively.

