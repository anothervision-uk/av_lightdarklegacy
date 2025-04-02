# av_lightdarklegacy
Typo3 Extension for legacy browsers to better display v13 backend avoiding light-dark()

Older legacy browsers eg:
Firefox <=119
Safari <=17.4
Chrome <=122

May not accurately interpret the color-scheme and light-dark() styles used to render the backend in Typo3 v13+. This can create transparent context menus, illegible modal overlays etc, which can make the editor unusable for clients/editors with older laptops etc.

Install the extension and add the TS 'av_lightdarklegacy' to root template. Custom Backend CSS file will be added, which adjusts rendering on legacy browsers using:

@supports not (color: light-dark(black, white)){
}

**Alpha proof of concept currently for *light mode only*.**

If others find it helpful, I will add more complete CSS, including dark mode styles.
