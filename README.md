# Styled Google Translate Widget

**Transform the default Google Translate widget into a professional and responsive element.**

---

This project provides the CSS and JavaScript needed to completely overhaul the Google Translate widget on your website. Instead of the default boring dropdown, you'll get a custom-styled language selector that hides Google's logo and banner. Most importantly, it **automatically collapses into a neat icon on mobile devices**.

*(Replace this with a screenshot of your project! Showing both desktop and mobile views is highly recommended to showcase its responsive nature.)*

## 📖 Table of Contents

* [✨ Features](#-features)
* [🚀 How to Use](#-how-to-use)
* [🎨 Advanced Customization](#-advanced-customization)
* [🤝 Contributing](#-contributing)
* [👨‍💻 Author](#-author)
* [📝 License](#-license)

## ✨ Features

* **Clean Interface:** Completely removes Google's logo, promotional banner, and other unnecessary elements.
* **Responsive Design:** Displays as a dropdown on large screens and collapses into a single translation icon on screens smaller than 550px.
* **Quick Integration:** Easily add it to any web project in just three simple steps.
* **Custom Icon:** Uses a custom icon for the mobile view, allowing it to blend seamlessly with your site's design.
* **Open Source:** Completely free to use, customize, and improve.

## 🚀 How to Use

Follow these steps to integrate the widget into your website.

### 1. Add HTML

First, make sure to link the stylesheet in the `<head>` of your HTML document.
```html
<link rel="stylesheet" href="style.css">

<div id="google_translate_element"></div>

<script type="text/javascript" src="//translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"></script>
<script type="text/javascript" src="script.js"></script>
```
### 2. Add CSS
Copy the **entire** content below and paste it into your `style.css` file. This is the core that styles the widget.

```css
div#\:0\.targetLanguage,
a.VIpgJd-ZVi9od-l4eHX-hSRGPd {
    display: none;
}

.goog-logo-link {
    display: none !important;
}

.goog-te-gadget {
    height: 100%;
    color: transparent !important;
}

select.goog-te-combo {
    height: 30px;
    width: 100%;
    border: 1px solid #dcdcdc;
}

.skiptranslate:not(.goog-te-gadget) {
    visibility: hidden !important;
}

.goog-te-banner-frame.skiptranslate,
.VIpgJd-ZVi9od-aZ2wEe-wOHMyf.VIpgJd-ZVi9od-aZ2wEe-wOHMyf-ti6hGc {
    visibility: hidden !important;
}

.skiptranslate .goog-te-gadget {
    display: inline;
}

#google_translate_element {
    display: inline-block;
    position: relative;
    width: 150px;
}

.nav-item {
    position: relative;
}

#\:0\.targetLanguage {
    display: inline-block !important;
    height: 100%;
}

@media screen and (max-width: 550px) {
  #google_translate_element {
      width: 30px !important;
      height: 30px !important;
  }

  select.goog-te-combo {
      width: 100% !important;
  }

  .goog-te-combo {
    height: 100% !important;
    appearance: none !important;
    -webkit-appearance: none;
    -moz-appearance: none;
    background: url('https://raw.githubusercontent.com/TranDangKhoaAutomation/Styled-Google-Translate-Widget/main/images/translate.png') no-repeat center;
    background-color: transparent !important;
    background-size: 20px 20px;
    text-indent: -9999px;
    height: 35px;
    font-size: 14px;
    border: 1px solid #ccc;
    border-radius: 5px;
    background-color: white;
    margin: 0px !important;
  }
}
```
### 3. Activate with JavaScript
Create a `script.js` file and add the following code to initialize the widget.
```javascript
function googleTranslateElementInit() {
    new google.translate.TranslateElement({
        pageLanguage: 'vi', // Your website's original language
        layout: google.translate.TranslateElement.InlineLayout.HORIZONTAL
    }, 'google_translate_element');
}
```
## 🎨 Advanced customization
You can easily change the following parameters in the `style.css` file:

* **Breakpoint:** Edit the `550px` value in `@media screen and (max-width: 550px)` to change the screen size at which the interface collapses to an icon.

* **Custom Icon:** Edit the URL in the `background` property of the `.goog-te-combo` class (within the media query) to use your own icon.

* **Desktop Size:** Change `width: 150px` in the `#google_translate_element` selector to adjust the dropdown's width on large screens.

## 🤝 Contributing
Contributions and ideas are welcome! Feel free to create a **Pull Request** or open an **Issue** to discuss what you'd like to change.

## 👨‍💻 Author
This project was created and is maintained by **Tran Dang Khoa (TranDangKhoaAutomation)**.

* **GitHub**: https://github.com/TranDangKhoaAutomation

* **YouTube**: https://youtube.com/@codewithkhoa

* **Facebook**: https://www.facebook.com/OfficialTranDangKhoa

## 📝 License
This project is licensed under the **MIT License**.