# Overview
By connecting your personal Google Fit account to Pipedream, you'll be able to incorporate your fitness data into whatever you're building with any of the 1,300+ apps that are available on Pipedream.

# Getting Started
The Google Fit Developer App in Pipedream can integrate with either a personal Gmail account or a Google workspace email account. Either option involves creating a custom Google App in the Google Cloud Console. This process does not involve any code or special approval by Google. The steps are outlined below:

## Creating a Google Fit app
In order to connect your personal or workspace Google Fit account to Pipedream, you'll need to create a custom OAuth app in Google Cloud.

1. Sign in to the [Google Cloud Console](https://cloud.google.com/)
2. Select an existing project or create a new one

  ![Select an exisiting project or create a a new one in the Google Cloud Console](https://res.cloudinary.com/pipedreamin/image/upload/v1663268100/docs/components/CleanShot_2022-09-15_at_14.54.34_vajyds.png)

3. Select **APIs & Services**
4. Click **Enable APIs & Services**

  ![Select "Enable APIs & Services to open a menu to enable the Google Fitness API for Pipedream to connect to](https://res.cloudinary.com/pipedreamin/image/upload/v1663268316/docs/components/CleanShot_2022-09-15_at_14.58.06_jshirk.png)

5. Search for and select **Fitness API**
6. Click **Enable**

  ![Search for and select the Google Fitness API](https://res.cloudinary.com/dpenc2lit/image/upload/v1692292762/Screenshot_2023-08-17_at_10.03.05_AM_ek8nqq.png)

7. Click **OAuth consent screen** on the left side
   
  ![Click "OAuth consent screen" in the left navigation menu](https://res.cloudinary.com/pipedreamin/image/upload/v1663268506/docs/components/CleanShot_2022-09-15_at_15.01.24_wravfb.png)

8. Select **External** User Type and click “Create”

  ![Select "External" in the OAuth Consent Screen](https://res.cloudinary.com/pipedreamin/image/upload/v1663268545/docs/components/CleanShot_2022-09-15_at_15.02.22_fiekq1.png)

9. Fill in the required fields and click **Save and Continue**
10. Under **Authorized Domains**, add `pipedream.com`
11. Click **Add or remove scopes** and Filter by `Fitness API` select whichever scopes you intend to use and then click "Update". For more information about available Google Fit scopes, please see this [overview](https://developers.google.com/fit/datatypes#authorization_scopes).
12. Click **Save and Continue** to finish the **Scopes** step
13. Add your own email as a **Test User** by clicking **Add Users** then typing in your email in the prompt then clicking **Add** again. Then finally click **Save and Continue** to finish the Test Users portion.
14. You should be prompted with a **Summary** page.

Now you've created an unlisted Google Fit app that you can integrate with Pipedream.

## Create OAuth Credentials

You will need to generate a set of OAuth credentials to connect your new Google Fit app to Pipedream properly.

1. Navigate to the **Credentials** section on the left side.
    
    ![Open the Credentials menu in the left hand nav bar](https://res.cloudinary.com/pipedreamin/image/upload/v1663269973/docs/components/CleanShot_2022-09-15_at_15.13.52_yvllxi.png)

2. Click **Create Credentials** at the top and select **“*OAuth client ID**
   
  ![Click create credentials to start the process](https://res.cloudinary.com/pipedreamin/image/upload/v1663270014/docs/components/CleanShot_2022-09-15_at_15.14.15_hjulis.png)
  
  ![Select the OAuth Client ID option](https://res.cloudinary.com/pipedreamin/image/upload/v1663270093/docs/components/CleanShot_2022-09-15_at_15.14.39_juqtnm.png)

3. Select **Web application** for **Application type**

  ![Web application is the type of OAuth credential we're generating](https://res.cloudinary.com/pipedreamin/image/upload/v1663270117/docs/components/CleanShot_2022-09-15_at_15.14.56_hlseq6.png)

4. Name the app “Pipedream”
5. Click **Add URI** and enter `https://api.pipedream.com/connect/oauth/oa_gA6iex/callback`

  ![Add the Pipedream URL to the Callback Redirect URL option](https://res.cloudinary.com/dpenc2lit/image/upload/v1692295499/Screenshot_2023-08-17_at_11.04.54_AM_blco7y.png)

6. Click **Create** to create your new OAuth keys
7. Note the client ID and client Secret, but keep these private and secure

  ![Store the Client ID and Client Secret keys](https://res.cloudinary.com/pipedreamin/image/upload/v1663270250/docs/components/CleanShot_2022-09-15_at_15.16.29_hvxnkx.png)

## Connect your Google Fit app Pipedream with your Google Fit app OAuth crendentials

At this point, you should have a Google Fit App under your Google Project, and a set of OAuth keys.

1. Now when prompted in Pipedream after trying to connect a Google Fit Developer App, copy and paste your OAuth credentials.
2. Add the scopes that you chose when setting up the app in a space-separate list.
3. Then click **Connect**
4. If you did not publish your Google Fit App in the Google Cloud Console, just click **Continue** to ignore the warning.

    ![Click continue if presented with a warning about an unpublished app](https://res.cloudinary.com/pipedreamin/image/upload/v1663269902/docs/components/CleanShot_2022-09-15_at_15.19.58_jnzlwc.png)

5. Check all of the necessary scopes you'll need for your workflows

    ![Check all scopes to include grant your integration permission](https://res.cloudinary.com/dpenc2lit/image/upload/v1692293421/Screenshot_2023-08-17_at_10.30.15_AM_ymeont.png)

7. Click the final **Connect** and your custom Google Fit app should be integrated into Pipedream!
