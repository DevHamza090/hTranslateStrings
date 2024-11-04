# String Translator for Android strings.xml

**hTranslateString** is a tool designed to facilitate the translation of Android strings.xml files by providing a convenient way to batch-translate strings using Google Translate. If you've ever tried translating a large number of expressions in your Android project, you might have encountered issues where Google displays a captcha page, rendering automated translation impractical. This is where htranslate comes to the rescue, offering a manual translation approach that allows you to efficiently handle numerous translations, potentially resulting in better context-aware translations.

## Prerequisites

Before you get started, ensure you have the following prerequisite installed:

- Python 3

## How it Works

Here's a step-by-step guide on how to use htranslate for translating your Android strings.xml files:

### 1. Original File

Begin by copying your `strings.xml` file into the project directory where htranslate is located.

### 2. Create Flat Files to be Translated

Use the following command to parse your `strings.xml` and generate the necessary files for translation:

```bash
python3 htranslate.py
```

This step will:

- Create files formatted for easy copy-and-paste into Google Translate (e.g., `totranslate-1.txt`, `totranslate-2.txt`, etc. by default).
- Generate empty files where you can paste the translated results from Google Translate (e.g., `translated-1.txt`, `translated-2.txt`, etc. by default).

### 3. Translate

Now, manually copy the content from the "totranslate-X.txt" files into Google Translate one by one and perform the translations.

### 4. Paste Results

After obtaining the translations from Google Translate, paste them into the corresponding "translated-X.txt" files.

### 5. Recreate strings.xml for Android

To finalize the process and generate the translated `strings.xml` file for your Android project, use the following command:

```bash
python3 htranslate-recreate.py
```

This will generate the `strings-translated.xml` file (by default) containing the translated data.

The generated files can be found in the "work" directory within the project directory.

Enjoy the convenience of translating your Android strings.xml files with htranslate!

---

Feel free to contribute to this project or report any issues on the GitHub repository: [Link to GitHub Repository](https://github.com/DevHamza090/hTranslateStrings)

If you find this tool helpful, please consider giving it a star to show your support!
