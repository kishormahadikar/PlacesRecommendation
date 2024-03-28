Places recommendation system using foursquare API 


Changes you need to do to make code work-

1- Make sure file path is correct and working in block 3&4
2- Create a foursquare developer account and create places api. Use the information in the necessary code blocks

How to get Access token for foursquare api-

1. **Go to Foursquare Developer Settings:**
   Visit the "App Settings" page on the Foursquare Developer Console.

2. **Set Redirect URL:**
   In the "Web Addresses" section, set the "Redirect URL" to https://www.google.com.

3. **Authenticate with Foursquare:**
   Paste this URL into your web browser, replacing YOUR_CLIENT_ID with your actual client ID:
   ```
   https://foursquare.com/oauth2/authenticate?client_id=YOUR_CLIENT_ID&response_type=code&redirect_uri=https://www.google.com
   ```
   This will redirect you to a Google page asking for permission to connect. Accept it.

4. **Get Authorization Code:**
   After accepting, look at the URL in your browser. Note the value after the 'code' part. It should look like https://www.google.com/?code=CODE. Copy the 'CODE' value.

5. **Request Access Token:**
   Paste and enter this URL into your web browser, replacing placeholders with actual values:
   ```
   https://foursquare.com/oauth2/access_token?client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET&grant_type=authorization_code&redirect_uri=https://www.google.com&code=CODE
   ```
   This should lead you to a page where you'll receive your access token.

Following these steps should allow you to successfully obtain an access token from Foursquare.