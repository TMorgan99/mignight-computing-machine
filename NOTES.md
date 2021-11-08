# Build a quick site in Netlify-Github

Select a folder name...

```bash
# Astro init
npm init astro <folderName> && code $_
```

- Next, [create a new Github repo](http://github.com/new)
- Grab the third code section (push an existing repository) and paste it behind the git init

Now, in VSCode, open the terminal to continue...

```bash
git init ; git add -A . ; git commit -m 'Commit 0'

# pasted bit
git remote add origin https://github.com/TMorgan99/mignight-computing-machine.git
git branch -M main
git push -u origin main

# npm init will bring in the github details.
# npm init

npx netlify init
# Create and configure a new site.
# Netlify CLI to configure the keys.
# set build to (astro build) see if we get the .toml file back.

# this will bring in the details of the repository we just set up.
npm init --yes
```

## now what?

Delete the Astro README.

I recently updated the passwords, so I guess Netlify is confused ?

 ›   Error: Failed retrieving GitHub repository information with error: Bad credentials

Checkout the [Github page](https://github.com/TMorgan99/mignight-computing-machine)

See where the netlify tools are located. Grab the `Admin` and `Site` urls for reference.

```bash
netlify status
```

How to fix the issue with the Bad credentials we saw earlier.

`[Build & deploy]` opens a `[Build Settings]` box with a `[Link site to Git]` button.

This gets us to browse the repos, and check out the basic settings, then `[Deploy Site]`

Build command => `npm run build`, which gets the script from `package.json`,
which we see is `astro build`.
This is what we see in `netlify.toml` so we should be good to go!
