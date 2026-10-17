# Tahoe Backcountry Ski Patrol website

This repository holds the public website for the Tahoe Backcountry Ski Patrol
(TBSP). The site tells the public who we are, where we patrol, and how to join,
and it carries patrol news.

## Why the site works this way

The site is built so that **any TBSP officer can update it, with no technical
background and no help from a webmaster.**

- **Every page is a plain text file.** Each post or page is a short text file
  in this repository. To change the website, you edit one of those files. You
  don't have to learn a content management system or keep track of a separate
  admin login.
- **You make every change in your web browser.** You edit, add and upload
  files on github.com. You don't need to install anything or use a command
  line.
- **It publishes itself.** When you save a change, GitHub rebuilds the site
  and puts it live within about two minutes.
- **No server to look after.** The site is hosted free on
  [GitHub Pages](https://pages.github.com/). There's no web server, database,
  or software to patch or renew, and nothing to break when an officer's term
  ends.
- **Nothing is ever lost.** GitHub keeps every version of every file, along
  with who changed it and when. You can undo any mistake, and the site can be
  handed from one officer to the next without losing anything.

### How a change gets to the website

1. An officer edits or adds a file on github.com and clicks **Commit changes**.
2. GitHub automatically runs a build (you can watch it in the **Actions** tab).
   A tool called [Hugo](https://gohugo.io/) turns the text files into web pages.
3. GitHub Pages publishes the new pages. The site is currently at
   <https://tbspweb.tbsp.org>.

If a build fails, the previous version of the site stays up. A mistake can't
take the website down.

## Contents

1. [Before you start (one time only)](#1-before-you-start-one-time-only)
2. [Add a new post](#2-add-a-new-post)
3. [Add a photo to a post](#3-add-a-photo-to-a-post)
4. [Check that your post went live](#4-check-that-your-post-went-live)
5. [Edit or delete a post](#5-edit-or-delete-a-post)
6. [Troubleshooting](#6-troubleshooting)
7. [For maintainers](#7-for-maintainers)

---

## 1. Before you start (one time only)

1. Create a free account at <https://github.com/signup> if you don't have one.
2. Send your GitHub username to the webmaster or the Patrol Director and ask
   them to add you to the **tbspweb** organization.
3. Accept the email invitation from GitHub.

Once you've accepted, an **Add file** button appears when you open folders in
this repository. If you don't see it, you don't have access yet.

---

## 2. Add a new post

Posts appear under **Recent Posts** on the home page, newest first.

Each post is a file ending in `.md` on the repository's main page, listed
below the folders (for example `tba-trail-counters.md`). You never need to
open a folder to work on posts.

1. Open this repository's main page on github.com.
2. Click **Add file** (top right), then **Create new file**.
3. In the **Name your file** box, type a short name made of lowercase words
   joined by dashes, ending in `.md`. For example:

   ```
   2026-ski-along-dates.md
   ```

   Type the name straight into the box, without a folder name in front of
   it. Don't use spaces, capital letters, or symbols such as `&`, `?` or `'`.
   The file name becomes part of the web address, so
   `2026-ski-along-dates.md` is published at `tbsp.org/post/2026-ski-along-dates/`.

4. Copy everything in the grey box below and paste it into the large editing
   area:

   ```
   ---
   title: "Ski-Along Dates for the 2026 Season"
   date: 2026-11-01
   featured_image: "/images/tbsp-square-1.jpg"
   tags: ["news"]
   ---

   Write your post here. Leave a blank line between paragraphs.

   You can make text **bold** or *italic*, and add a
   [link like this](https://www.nsp.org).

   - Bullet lists start with a dash and a space
   - Like this

   ## A heading like this starts a new section

   Everything above the first heading appears on the home page.
   ```

5. Replace the example text with your own. The lines between the two `---`
   markers are settings for the post:

   | Line | What to put there |
   |---|---|
   | `title` | The headline of your post. Keep the quotation marks. |
   | `date` | Today's date as **year-month-day**, for example `2026-11-01`. **A future date hides the post** until that day arrives. |
   | `featured_image` | The picture shown next to the post on the home page and across the top of its page. Use one of the existing photos below, or [add your own](#3-add-a-photo-to-a-post). |
   | `tags` | One or more labels in quotation marks, separated by commas, for example `["news", "training"]`. |

   **Don't delete the two `---` lines or any of the quotation marks.** Most
   publishing problems come from a missing `---` line or quotation mark.

   Existing photos you can use for `featured_image`:

   - `/images/tbsp-square-1.jpg`
   - `/images/tbsp-square-3.jpg`
   - `/images/tbsp-square-4.jpg`
   - `/images/tbsp-square-5.jpg`
   - `/images/tbsp-cover-1.jpg`

6. To check your formatting, click the **Preview** tab above the editing area.
   (The preview shows the settings block as a small table. That's normal.)
7. Click the green **Commit changes...** button. In the box that opens:
   - Under *Commit message*, write a short note such as
     `Add ski-along dates post`.
   - Leave **Commit directly to the `main` branch** selected.
   - Click **Commit changes**.

   The website updates itself within about two minutes. See
   [section 4](#4-check-that-your-post-went-live) to check that it worked.

### What appears on the home page

The home page shows each post's **first section** in full: everything from
the top of the post down to its first heading (a line starting with `##`).
Links, lists and bold text all appear just as you wrote them. If the post
continues after that heading, the home page shows a **Continue reading** link
that names the next section and takes readers straight to it.

- For a short post, don't use any headings. The whole post appears on the
  home page.
- For a long post, put the most important part first, then start the
  details with a `##` heading.

### Saving a post without publishing it

To save a draft that doesn't appear on the website yet, add this line between
the `---` markers:

```
draft: true
```

When the post is ready, delete that line (or change it to `draft: false`) and
commit again.

---

## 3. Add a photo to a post

1. Shrink your photo first. Aim for about **1200 pixels wide** and under
   **500 KB**. Photos straight from a phone are usually too big and make the
   site slow. (On a Mac, use Preview → Tools → Adjust Size. On Windows, use
   Photos → Resize.)
2. Rename the photo file using lowercase words and dashes, with no spaces,
   for example `castle-peak-sunrise.jpg`.
3. In this repository, click **`static`**, then **`images`**.
4. Click **Add file**, then **Upload files**. Drag your photo in, then click
   **Commit changes**. Upload the photo **before** you add the post that
   uses it.
5. Use the photo in your post:
   - As the preview picture, put this in the settings block:
     `featured_image: "/images/castle-peak-sunrise.jpg"`
   - Inside the body of the post, put this on its own line:

     ```
     ![A short description of the photo](/images/castle-peak-sunrise.jpg)
     ```

     The text in square brackets is read aloud to visitors who use screen
     readers, so describe what the photo shows.

For the `featured_image`, pick a photo whose subject is near the middle: on
the home page, `.jpg` photos are cropped to a square. `.png` images, which are
usually logos, are shown whole.

Only upload photos that TBSP has permission to use. Ask people before you post
a photo where they can be clearly identified.

---

## 4. Check that your post went live

1. Click the **Actions** tab at the top of this repository.
2. The top row is your change:
   - A yellow circle means it is still publishing. Wait a minute.
   - A green check mark means it is live. Visit the website. If you still see
     the old page, refresh it.
   - A red X means something went wrong. See [Troubleshooting](#6-troubleshooting).
     The previous version of the website stays up, so nothing is broken for
     visitors.

---

## 5. Edit or delete a post

- **Edit:** On the repository's main page, click the post's `.md` file,
  then click the pencil icon (✏️) at the top right. Make your changes and click
  **Commit changes**.
- **Delete:** Open the file, click the **⋯** menu at the top right, then click
  **Delete file** and **Commit changes**.

Every change is saved in the history, so you can always undo a mistake. If you
need to undo something, ask the webmaster.

The **Learn About TBSP** section on the home page works the same way. Its pages
live in the `content/about` folder. Each About page has a
`weight:` line, and the home page lists them from the lowest number to the
highest. To add an About page, give it the next unused number.

---

## 6. Troubleshooting

| Problem | Likely cause and fix |
|---|---|
| My post doesn't appear. | The `date` is in the future, or the post still has `draft: true`. Fix the date or remove the draft line. |
| The Actions tab shows a red X. | Usually the settings block is broken. Check that both `---` lines are present, that every quotation mark has a partner, and that the date looks like `2026-11-01`. Click the red X to see the error message. |
| The picture is missing or broken. | Check that the file name in your post exactly matches the uploaded file, including `.jpg` versus `.JPG`, and that the path starts with `/images/`. |
| The settings appear as text at the top of my post. | The first line of the file must be `---`, with nothing above it, not even a blank line. |
| I don't see the "Add file" button or the pencil. | You aren't signed in, or you haven't been added to the organization yet. See [section 1](#1-before-you-start-one-time-only). |

If you're stuck, email the webmaster with a link to your file.

---

## 7. For maintainers

The site is built with [Hugo](https://gohugo.io/) and the
[Ananke](https://github.com/theNewDynamic/gohugo-theme-ananke) theme, which is
included as a git submodule in `themes/gohugo`. GitHub Actions
(`.github/workflows/hugo.yml`) builds the site and deploys it to GitHub Pages
on every push to `main`.

```
content/_index.md      Home page intro text and banner
*.md (top level)       Blog posts ("Recent Posts"), mounted as content/post/
content/post/_index.md Title of the post list ("What's New")
content/about/         "Learn About TBSP" pages
layouts/index.html     Home page layout
layouts/post/list.html "All posts" page layout
layouts/partials/      Footer override
static/images/         Images, served at /images/...
hugo.toml              Site title, menu, and settings
```

To preview the site on your own computer:

```sh
git clone --recurse-submodules https://github.com/tbspweb/tbspweb.github.io.git
cd tbspweb.github.io
hugo server        # requires Hugo extended 0.146 or newer
```

Then open <http://localhost:1313>.

Every `.md` file in the top level of the repository except `README.md` is
published as a post (see `[module.mounts]` in `hugo.toml`). Don't add other
Markdown files there, such as notes or a CHANGELOG. Put them in a folder, or
add them to `excludeFiles`.
