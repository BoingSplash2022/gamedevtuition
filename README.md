# Game Dev Tuition website

A simple HTML/CSS website for www.gamedevtuition.com, ready to edit in VS Code and host free on GitHub Pages.

## What's in the folder

| File | What it is |
|---|---|
| `index.html` | Homepage |
| `resources.html` | YouTube videos and course links |
| `blog.html` | Blog: post list plus the full posts |
| `contact.html` | Contact form (sends to nick.dunn2019@gmail.com) |
| `thank-you.html` | Page shown after someone sends the form |
| `css/style.css` | All the styling. Colours are at the top |
| `js/main.js` | Mobile menu and footer year |
| `images/` | Your images |
| `CNAME` | Tells GitHub Pages to use www.gamedevtuition.com |

## 1. Open it in VS Code

1. Unzip the folder somewhere sensible, e.g. `Documents/gamedevtuition`.
2. In VS Code: **File → Open Folder…** and choose that folder.
3. Install the **Live Server** extension (by Ritwick Dey). Right-click `index.html` and choose **Open with Live Server** to preview. The page reloads every time you save.

## 2. Things to edit

- **Video titles:** in `resources.html`, search for `EDIT:` and replace "Tutorial video 1" etc. with the real video names.
- **Adding a blog post:** in `blog.html`, copy a `post-card` block and an `article` block, change the text, and give them a matching new `id` / `href` (e.g. `id="my-post"` and `href="#my-post"`).
- **Adding a video:** copy a whole `video-card` block in `resources.html` and change the video ID (the part after `youtu.be/`) in both places.
- **Colours:** change `--accent` and `--accent-2` at the top of `css/style.css`.
- **Images:** drop new images into `images/` and point to them with `src="images/your-file.jpg"`.

## 3. Put it on GitHub

1. Create a free account at github.com if you don't have one.
2. Click **New repository**, name it `gamedevtuition`, set it to **Public**, and create it (don't add a README; this folder already has one).
3. In VS Code, open the **Source Control** panel (the branch icon on the left) and click **Initialize Repository**.
4. Type a message such as `First version of site` and click **Commit** (choose **Yes** if asked to stage all changes).
5. Click **Publish Branch**, sign in to GitHub, and pick the `gamedevtuition` repository (or let VS Code create it for you).

After this, whenever you change something: **Commit**, then **Sync Changes**. The live site updates within a minute or two.

## 4. Turn on GitHub Pages

1. On github.com, open the repository → **Settings → Pages**.
2. Under **Build and deployment**, set Source to **Deploy from a branch**, Branch to **main** and folder **/ (root)**, then **Save**.
3. Under **Custom domain**, enter `www.gamedevtuition.com` and **Save**. (The `CNAME` file does this too.)
4. Once the DNS check passes, tick **Enforce HTTPS**.

## 5. Point your domain at GitHub

Log in to the company you bought the domain from and open its **DNS settings**. Add these records:

| Type | Name / Host | Value |
|---|---|---|
| CNAME | `www` | `YOUR-GITHUB-USERNAME.github.io` |
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |

Delete any existing "parking" A or CNAME records for `@` or `www` first. DNS changes can take anywhere from a few minutes to 24 hours. You can check the current values in GitHub's Pages documentation: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site

## 6. Activate the contact form (one time only)

GitHub Pages can't send email by itself, so the form uses **FormSubmit** (free, no sign-up).

1. Once the site is live, go to the Contact page and send yourself a test message.
2. FormSubmit emails nick.dunn2019@gmail.com an **activation link**. Click it. Check your spam folder if it doesn't arrive.
3. From then on, every message arrives in your inbox, and visitors see the thank-you page.

**Tip:** after activating, FormSubmit gives you a random alias address (a string of letters). Replace `nick.dunn2019@gmail.com` in the form's `action="..."` with that alias so spam bots can't pick your email out of the page code.
