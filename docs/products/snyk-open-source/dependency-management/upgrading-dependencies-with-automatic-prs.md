# Upgrading dependencies with automatic PRs

After importing the chosen Git repositories to Snyk, Snyk continuously monitors these repositories by scanning them for vulnerability, license, and dependency health issues. In addition to providing fix advice, Snyk also creates pull requests (PRs) on your behalf (configured by you).

## Supported languages and SCMs

Snyk currently supports the **Automatic dependency upgrade pull requests** feature for npm, Yarn, and Maven-Central repositories via the following SCMs: GitHub, GitHub Enterprise, and Bitbucket Cloud.

You can also use this feature with the Snyk Broker. To use this feature, Snyk Broker must be upgraded to a minimum of v. 1.4.55.0 or later. For more information, see [Upgrade your Snyk Broker client](../../../features/snyk-broker/set-up-snyk-broker/how-to-install-and-configure-your-snyk-broker-client.md#upgrade-your-snyk-broker-client).

![](<../../../.gitbook/assets/Upgrade Broker.png>)

## Automatic dependency (upgrade) PRs

1. The **Automatic dependency upgrade pull requests** option is enabled (in [the Integration Settings on the organization level](upgrading-dependencies-with-automatic-prs.md#enabling-the-automatic-dependency-upgrade-prs-option-for-an-entire-organization) or [the Project Settings](upgrading-dependencies-with-automatic-prs.md#enabling-the-automatic-dependency-upgrade-prs-option-for-a-specific-project)).
2. When you import your repos to Snyk, Snyk scans the repos and provides you with the scan results. Snyk then continues to monitor your Open Source Projects, scanning them on a regular basis.
3. Per scan, when new versions for your dependencies are identified, Snyk does the following:
   * Snyk creates automatic upgrade PRs.\
     **Note**: The re-scan frequency is based on the schedule set in the Project Settings.
   * Snyk will not open a new upgrade PR for a dependency that is already changed (upgraded or patched) in another open Snyk PR.
   * Snyk opens separate PRs for each dependency.
   * By default, Snyk will not create upgrade PRs for a Project that has 5 or more open Snyk PRs. If the limit of open PRs is reached, no new PRs are created. This limit number can be set to be between 1-10 on the Integration or Project Settings. This limit only applies to Upgrade PRs, but it does count Fix PRs. However, Fix PRs are not limited in this way.
   * By default, Snyk recommends only patch and minor upgrades. However, recommendations for major version upgrades can be requested in the Settings page where the feature is enabled.
   * If the latest eligible version contains vulnerabilities that are not found yet in your Project, Snyk will not recommend an upgrade.
   * Snyk does not recommend upgrades to versions that are less than 21 days old. This is to avoid versions that introduce functional bugs and subsequently get unpublished, or versions that are released from a compromised account (where the account owner has lost control to someone with a malicious intent).

## Enabling the Automatic dependency upgrade PRs option

You can configure Snyk to regularly check your dependency health, recommend dependency upgrades, and automatically submit PRs for upgrades on your behalf for an entire organization or a specific Project. Once configured, Snyk automatically creates PRs for all the necessary dependencies as upgrades become available for the scanned Projects.

By default, the Project Settings inherit the organization Settings. However, when the Settings on the organization and Project levels are different, the Project Settings override the organization Settings.

### Enabling the Automatic dependency upgrade PRs option for an entire organization

**To configure automatic upgrade PRs for an entire organization:**

1\. On the Snyk Web UI, open the required organization:

![](<../../../.gitbook/assets/OS - Automatic Dependency Upgrade - Selecting Organization (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (8).png>)

2\. Once the required organization is open, click the **Org Settings** button <img src="../../../.gitbook/assets/Org Settings button - Icon (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2).png" alt="" data-size="line"> on the top menu:

![](<../../../.gitbook/assets/OS - Automatic Dependency Upgrade - Org Settings button (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)

3\. On the **Settings** page, select **Integrations** on the left menu. Then, locate your configured and required SCM, and click the **Edit settings** option at the end of its row:

**Note**: You can enable this feature only for the following SCMs: GitHub, GitHub Enterprise, and Bitbucket Cloud.

![](<../../../.gitbook/assets/OS - Automatic Dependency Upgrade - Organization - Integrations page (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2).png>)

4\. On the **Settings** page of the selected integration, scroll down to the **Automatic dependency upgrade pull requests** section:

![](<../../../.gitbook/assets/OS - Automatic Dependency Upgrade - Organization - Integration Settings - Automatic Upgrade section .png>)

5\. On the **Automatic dependency upgrade pull requests** section perform the following:

* Slider - change to **Enabled**.
* **Include major version in upgrade recommendation** – select one of the available options to define if major version upgrades will be included in the recommendations. By default, only patches and minor versions are included in the upgrade recommendations.
* **Limit Snyk to this many dependency upgrade PRs open simultaneously** – define how many open Snyk PRs a Project can have, in order to also receive a dependency upgrade PR. By default, a Project can have 4 open PRs at the most, in order to also receive a dependency upgrade PR. You can set a number between 1 -10. When the limit of the open PRs is reached, no new upgrade PRs are created.
* **Dependencies to ignore** – enter the exact name of the dependencies that should NOT be included in the **Automatic upgrade** operation. You can only enter lower case letters.

![](<../../../.gitbook/assets/OS - Automatic Dependency Upgrade - Project Settings - Integration - Automatic Upgrade section - Enabled.png>)

7\. To save and apply your changes, click one of the following:

* **Apply changes to all overridden projects** option – your changes are saved, and will be applied to all the Projects in the organization. Projects that have Custom Settings will inherit these organization Settings, and their Custom Settings will be override. After you click this option, a message appears, asking you to confirm the override:\
  ![](<../../../.gitbook/assets/Snyk Code - PR Checks - Integration Settings - Automatic Upgrade section - Override message (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)
* **Save changes** button – your changes are saved, and will be applied to all the Projects in the organization that are configured to inherit these Settings from the organization. Projects that have Custom Settings will not be influenced by this change.

![](<../../../.gitbook/assets/OS - Automatic Dependency Upgrade - Org- Integration - Automatic Upgrade section - Save options (1).png>)

From now on, every time Snyk will scan any Project in the organization, it will automatically submit Upgrade PRs if the scan discovers that an upgrade is available. If a newer version is released for an existing Snyk Upgrade PR or for an existing Fix PR, the existing PR must be closed or merged before Snyk can raise a new PR.

***

### Enabling the Automatic dependency upgrade PRs option for a specific Project

The Settings on the Project level override the Settings on the organization level. However, the Settings on the Organization level can override the Custom Settings of a Project, if they are configured after the Project level customization, and are saved with the option - **Apply changes to all overridden projects** (see Step 7 above).

***

**To configure automatic upgrade PRs for a specific Project:**

1\. On the Snyk Web UI, open the organization that includes the required Project:

![](<../../../.gitbook/assets/OS - Automatic Dependency Upgrade - Selecting Organization (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (8).png>)

2\. Move to the **Projects** page by clicking the **Projects** tab on the top menu.

3\. Locate the Project for which you want to enable automatic upgrade PRs. Then, click the **Settings** button on the right side of its row:

![](<../../../.gitbook/assets/OS - Automatic Dependency Upgrade - Project Settings button .png>)

4\. On the Project **Settings** page, click the relevant **integration** tab on left menu:

![](<../../../.gitbook/assets/OS - Automatic Dependency Upgrade - Project Settings - Integration tab.png>)

5\. On the **integration** page, scroll down to the **Automatic dependency upgrade pull requests** section. Then, select one of the following:

* **Inherit from Integration settings** – apply the Integration Settings of the organization to the selected Project. Note that if the **Automatic dependency upgrade pull requests option is disabled for the organization, this option will also be disabled for the Project.** If you selected this option, move to Step 7.
* **Customize for only this project** – apply specific settings of the **Automatic dependency upgrade pull requests** option on the Project. If you selected this option, move to the next step.

![](<../../../.gitbook/assets/OS - Automatic Dependency Upgrade - Project Settings - Integration - Automatic Upgrade section (1).png>)

6\. \[For the **Customize** option only] If you selected the **Customize for only this project** option, perform the following:

* Slider - change to **Enabled**.
* **Include major version in upgrade recommendation** – select one of the available options to define if major version upgrades will be included in the recommendations. By default, only patches and minor versions are included in the upgrade recommendations.
* **Limit Snyk to this many dependency upgrade PRs open simultaneously** – define how many open Snyk PRs a Project can have, in order to also receive a dependency upgrade PR. By default, a Project can have 4 open PRs at the most, in order to also receive a dependency upgrade PR. You can set a number between 1 -10. When the limit of the open PRs is reached, no new upgrade PRs are created.
* **Dependencies to ignore** – enter the exact name of the dependencies that should NOT be included in this **Automatic upgrade** operation. You can only enter lower case letters.

![](<../../../.gitbook/assets/OS - Automatic Dependency Upgrade - Project Settings - Integration - Automatic Upgrade - Customize options.png>)

**7.** Click the **Update dependency upgrade settings** button to save your settings.

From now on, every time Snyk will scan this Project, it will automatically submit Upgrade PRs if the scan discovers that an upgrade is available. If a newer version is released for an existing Snyk Upgrade PR or for an existing Fix PR, the existing PR must be closed or merged before Snyk can raise a new PR.
