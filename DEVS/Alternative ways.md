# Alternative ways

Here are some SvelteKit + authentication sources the author found (and why they didn't match his needs, directly):

- ["SvelteKit + Firebase: Authentication, protected routes, and persistent login"](https://dev.to/pilcrowonpaper/sveltekit-firebase-authentication-protected-routes-and-persistent-login-dk3) (blog, Feb'22)

	>”We will create a server-rendered website with authentication and protected routes using firebase.”

	**Just is**
		
	- Uses auth + refresh tokens

	**Pros**

	**Cons**
	
	- has a ”sign up”, login -mindset	(not pw-less design)
	- Imports `firebase` client-side as a single, monolithic dependency (it can be imported more granularly)


- [This SO answer](https://stackoverflow.com/a/75564503/14455) (May'23)

	It does a good job of differentiating the auth (with full stack) possibilities. I believe we're heading for "choice 2" (server side session cookies handling).
	
	>Here you'll need a sign-in page where you authenticate the user and create a session cookie (as Tonton-Blax mentioned). You'll also then sign out the user on the client side using Firebase (since you'll be using the cookie). Then in your *server.js files you fetch the cookie to authenticate your requests. And you'll need to implement another sign out feature which expires the cookie you've created. This option requires a bit more work to secure your cookie, set expiry, deal with CSRF, etc.
	
	