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

## Deploy Status

[![Netlify Status](https://api.netlify.com/api/v1/badges/4dcf1798-1247-4749-a3bb-f959eda4543e/deploy-status)](https://app.netlify.com/sites/cranky-swanson-3bb12e/deploys)

## Touch up README

Not sure how the StackBlitz deploy button works, so just delete for now.

## NetlifyForm

Create the astro component, basically dropping the [sample code](https://docs.netlify.com/forms/setup/)

run the dev locally. see what happens!

```bash
# should run this the first time, I guess.
snowpack init
# use Netlify CLI to s
netlify dev
```

## Retreval

Netlify has given our form an 'id', which can be found on the `forms` tab of the site's dashboard.

[This is the page url](https://app.netlify.com/sites/cranky-swanson-3bb12e/forms/6188bf5509e8a70008284359)

Remember to visit this page to `[Download CSV]`and periodically `Delete submissions`.

This downloads a file called `contact.csv`, and has the fields from your form, in addition to system fields "ip","user_agent","referrer","created_at"
