# Manual tests

This is kind-of the specs of the project.

<!-- tbd. Excalidraw picture of the pages, transitions etc.

/shared	# can be accessed non-auth (or auth); shows auth info if not logged in

/project/{x}	# needs login

/login		# the login page

-->


## Can have pages that are visible for everyone

Go to `/shared` 
	- logged: shows general + user info
	- not logged: shows general info

	Visiting here does not suggest logging in.


## Pages that need log-in

- Go to `/project/1`

	- should lead to `/login` and (after login) back to `/project/1`

	- [ ] Make a couple of project pages; allowing (by manipulating the database) access to them

		- ..have a script for that!   `/kitchen/...sh`



## Access rights

- `/project/1` and `/project/2` would have different access rights

	- be auth'ed in `/project/1`
	- try going to `/project/2`

	Should get a suitable reply, maybe just 4xx (no access)?

	Could also think of... asking for access to said project, from the owner.
	

## Login component

- not logged in:
	- shows "Log in" text + dropdown
	- ..with options for social sign-in

- logged: shows your name + avatar (if any)
	- has a "log out" feature (behind dropdown)

	- logout works; leads to `/login` or `/`

