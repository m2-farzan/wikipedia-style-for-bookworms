# Preview
![Preview Image](https://raw.githubusercontent.com/m2-farzan/wikipedia-style-for-bookworms/master/preview.jpg)

# Introduction
I'm not a web designer, nor a typography expert. So most of what follows are mostly my personal opinions. I'm a bookworm. I spend a fair amount of time reading books and e-books but when it comes to Wikipedia, I've caught myself just skipping through the lines, never reading anything carefully.

I know that Wikipedia articles come naturally less consistent compared to actual books. But I think poor visual styling is also a disturbing factor. Those 250-character long lines, written in a sans-serif font, with a mess of blue-colored words here and there that emphasize unimportant parts of the sentence, and so on. Again, I'm not a web designer but come on!

Fortunately, Wikipedia can be totally customized after logging in. So if you're ready to have a bookwormish Wikipedia experience, follow these steps.

# Steps
- Login in to your account.
- Go to your preferences page https://en.wikipedia.org/wiki/Special:Preferences
- Go to tab *Appearance*
- Select *MinervaNeue* Theme.
- In the line after *Shared CSS/JavaScript for all skins:* select *Custom CSS*
- Start creating/editing the page
- Enter the following CSS into the page:
    ```
    /* Use a serif font. Make text slightly larger. */
    body {
        font-family: serif;
        font-size: larger;
    }

    /* Links will appear in black italic style. */
    a:link {
        color: #202122;
        font-style: italic;
    }
    a:visited {color: #202122}
    a:hover {color: #202122}
    a:active {color: #202122}

    /* This keeps text width about 70 characters, which is recommended for readability. */
    .content {max-width: 35em}

    /* Bring some color to life */
    .header-container.header-chrome {background-color: #e9eaa4}
    ```
- Save the page
- Reload (Hold *Shift* and click browser reload button. This will load the new style.)
- Enjoy! If you know CSS, you can tune the page down to the last nuts and bolts. BTW, if you find any problem caused by this CSS or can improve it, don't hesitate. Just create an issue or pull request.

Extra tips:
- Go to your browser settings and set a respectable font as your default serif font! *Times New Roman* is an old friend but give others a chance. Your eyes will thank you. I'm using *Noto Serif* from Google.
- You can use the great extension *Dark Reader* that enables you to read any page in night mode.
