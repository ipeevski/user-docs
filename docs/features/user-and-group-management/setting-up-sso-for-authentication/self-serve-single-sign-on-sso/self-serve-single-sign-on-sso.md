# Example: Okta SAML Application

An example follows of setting up an Okta SAML application and connecting this to Snyk to facilitate SSO. To configure your Okta to use SSO with Snyk you need an entity ID and a reply url (Assertion Consumer Service URL) from Snyk.

1.  From the drop down at the top left select **GROUP OVERVIEW**.

    <figure><img src="../../../../.gitbook/assets/1 (1) (2).png" alt="Select group overview"><figcaption><p>Select group overview</p></figcaption></figure>
2.  Click on **SSO** and copy the values under **Entity ID** and **ACS URL** or leave the browser tab open for easy access. Also download the **Signing certificate** for later use in Okta.

    <figure><img src="../../../../.gitbook/assets/2 (1).png" alt="Group Settings: SSO"><figcaption><p>Group Settings: SSO</p></figcaption></figure>


3.  Navigate to [Okta](https://www.okta.com/se/login/), open the application menu, and click on **Create App Integration.**

    <figure><img src="../../../../.gitbook/assets/1 (3).png" alt="Okta Applications main page"><figcaption><p>Okta Applications main page</p></figcaption></figure>
4.  Choose **SAML 2.0** and name your application appropriately; click **Next**.

    <figure><img src="../../../../.gitbook/assets/2 (3).png" alt="Okta SAML application creation"><figcaption><p>Okta SAML application creation</p></figcaption></figure>
5.  Add the Entity ID and the sign on URL you copied from Snyk to the appropriate fields.

    <figure><img src="../../../../.gitbook/assets/3 (3).png" alt="Add SSO details in Okta"><figcaption><p>Add SSO details in Okta</p></figcaption></figure>
6.  Scroll down to **Attribute Statements** and add three attributes named with values as follows:

    * **Name**: email, **Value**: user.email
    * **Name**: name, **Value**: user.firstName + ' ' + user.lastName
    *   **Name**: username, **Value**: user.login

        <figure><img src="../../../../.gitbook/assets/5 (2).png" alt="Add Okta attribute statements"><figcaption><p>Add Okta attribute statements</p></figcaption></figure>

    Now click **Next** and enter feedback details if desired or go to the next step.
7. Open your Okta application list again and click on your newly created application and the **Sign on**  tab. To the right of the page, click on **View SAML setup instructions** then from the page that opens, copy the **Identity Provider Single Sign-On URL** and the **X.509 certificate**.
8.  Go back to the previous page and go to the **Assignments** tab. Click on **Assign** and choose users, groups, or both according to your needs.

    <figure><img src="../../../../.gitbook/assets/7 (3).png" alt="Assign the SSO application"><figcaption><p>Assign the SSO application</p></figcaption></figure>
9.  Go back to the Snyk portal, scroll to step 2, and enter the details from step 7.

    <figure><img src="../../../../.gitbook/assets/8.png" alt="Snyk SSO step 2"><figcaption><p>Snyk SSO step 2</p></figcaption></figure>
10. Scroll to step 3 and refer to [step 3](https://docs.snyk.io/features/user-and-group-management/setting-up-sso-for-authentication/self-serve-single-sign-on-sso#step-3.-snyk-sso-settings) of the Snyk self serve SSO guide for how new users should be treated when signing in. Choose the option you would like to use: **Group member, Org collaborator** or **Org admin**. Finally, enter the **profile attributes** as you configured them in Okta, click **Save changes**, **** and verify you can log in, either with the direct URL at the top of step 3 or by going to the [generic SSO login](https://app.snyk.io/login/sso).

    <figure><img src="../../../../.gitbook/assets/9 (3).png" alt="Profile attributes"><figcaption><p>Profile attributes</p></figcaption></figure>
