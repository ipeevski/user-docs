# Example: Azure AD Enterprise Application

An example follows of setting up an Azure AD Enterprise Application and connecting this to Snyk to facilitate SSO. To configure your Azure Enterprise Application to use SSO with Snyk you first need an entity ID and a reply url (Assertion Consumer Service URL) from Snyk.

1.  From the drop down at the top left select **GROUP OVERVIEW**.

    <figure><img src="../../../../.gitbook/assets/1 (1) (2).png" alt="Select group overview"><figcaption><p>Select group overview</p></figcaption></figure>
2.  Click on **SSO** and copy the values under **Entity ID** and **ACS URL** or leave the browser tab open for easy access.

    <figure><img src="../../../../.gitbook/assets/2 (1).png" alt="Group Settings: SSO"><figcaption><p>Group Settings: SSO</p></figcaption></figure>
3.  Navigate to Azure and open Azure AD.

    <figure><img src="../../../../.gitbook/assets/3 (1).png" alt="Azure AD Default Directory"><figcaption><p>Azure AD Default Directory</p></figcaption></figure>
4.  Click **Add** then **Enterprise application**.

    <figure><img src="../../../../.gitbook/assets/4.png" alt="Add Enterprise application"><figcaption><p>Add Enterprise application</p></figcaption></figure>
5.  Choose **Create your own application**.

    <figure><img src="../../../../.gitbook/assets/5.png" alt="Create your own application"><figcaption><p>Create your own application</p></figcaption></figure>
6.  Name the application appropriately, for example, **Snyk-SSO**, making sure that **Integrate any other application you don't find in the gallery (Non-gallery)** is selected and then click **Create**.

    <figure><img src="../../../../.gitbook/assets/6.png" alt="Application name and integration"><figcaption><p>Application name and integration</p></figcaption></figure>
7.  For the new app, select **Set up single sign on** and **Get started**.

    <figure><img src="../../../../.gitbook/assets/7.png" alt="Set up single sign-on, Get started"><figcaption><p>Set up single sign-on, Get started</p></figcaption></figure>
8.  Select **SAML** as the SSO method.

    <figure><img src="../../../../.gitbook/assets/8 (2).png" alt="Select SAML"><figcaption><p>Select SAML</p></figcaption></figure>
9.  Click **Edit** under **Basic SAML configuration**.

    <figure><img src="../../../../.gitbook/assets/9.png" alt="Edit basic SAML configuration"><figcaption><p>Edit basic SAML configuration</p></figcaption></figure>
10. Add the Identity (Entity ID) and reply URL (Assertion Consumer Service URL) you obtained from Snyk and click **Save**; **** then close the edit window.

    <figure><img src="../../../../.gitbook/assets/10 (1).png" alt="Entity ID and Assertion Consumer Service URL"><figcaption><p>Entity ID and Assertion Consumer Service URL</p></figcaption></figure>
11. Scroll to find the login and logout URLs needed to finish the configuration in Snyk. Copy these and paste them into the SSO settings in the Snyk portal.

    <figure><img src="../../../../.gitbook/assets/11.png" alt="Login and logout URLs"><figcaption><p>Login and logout URLs</p></figcaption></figure>

    <figure><img src="../../../../.gitbook/assets/12 (1).png" alt="Sign in and Sign out URLs in Snyk portal"><figcaption><p>Sign in and Sign out URLs in Snyk portal</p></figcaption></figure>
12. Return to Azure AD and click **Download** next to **Certificate (Base64)**.

    <figure><img src="../../../../.gitbook/assets/13.png" alt="Download SAML Certificate (Base 64)"><figcaption><p>Download SAML Certificate (Base 64)</p></figcaption></figure>
13. Open the downloaded certificate in your preferred text editor, copy the text and paste it into the Snyk **X509 signing certificate** field, and add the relevant domains that are supported by this SSO connection. Finally, click **Create Auth0 connection** if you are creating a completely new connection or **Save changes** if you are editing an existing connection.

    <figure><img src="../../../../.gitbook/assets/14.png" alt="Enter certificate and domains supported, set connection"><figcaption><p>Enter certificate and domains supported, set connection</p></figcaption></figure>
14. Refer to [step 3](https://docs.snyk.io/features/user-and-group-management/setting-up-sso-for-authentication/self-serve-single-sign-on-sso#step-3.-snyk-sso-settings) of the Snyk self serve SSO guide for how new users should be treated when signing in and choose the option you would like to use: **Group member, Org collaborator**, or **Org admin**.
15. Return to Azure AD and click **Edit** under **Attributes and Claims**.

    <figure><img src="../../../../.gitbook/assets/15.png" alt="Edit Azure AD attributes and claims"><figcaption><p>Edit Azure AD attributes and claims</p></figcaption></figure>
16. Copy the claim names from Azure to Snyk as follows and **Save changes** in Snyk to finish the configuration.

    <figure><img src="../../../../.gitbook/assets/16.png" alt="Copy from Azure portal"><figcaption><p>Copy from Azure portal</p></figcaption></figure>

    <figure><img src="../../../../.gitbook/assets/17 (1).png" alt="dd claim name in Snyk portal"><figcaption><p>Add claim name in Snyk portal</p></figcaption></figure>

