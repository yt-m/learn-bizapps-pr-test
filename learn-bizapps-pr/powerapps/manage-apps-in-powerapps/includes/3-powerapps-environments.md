An environment is a container for apps and other resources, such as data connections and flows from Power Automate. It's a way to group items based on business requirements.

![Screenshot of Microsoft Power Platform environments.](../media/power-apps-environments.png)

If you've followed along with this module, you've already been working in [make.powerapps.com](https://make.powerapps.com/?azure-portal=true). Therefore, you've been working in a specific environment the whole time.
In the upper-right corner of the home page, you can view your current environment.

![Screenshot of the Environment with toolbar.](../media/powerapps-environment-picker.png)

If you're new to Microsoft Power Apps, you might have only the default environment at this point. If a drop-down menu is visible next to the environment name, this indicates that other environments are available.

> [!NOTE]
> If you want to work with Power Apps environments, you need a Power Apps Per app plan or Power Apps Per user plan. Additionally, if you want to work with Dynamics 365 restricted tables, you must have a Power Apps for Dynamics 365 license. Learn more about [licenses for Dynamics 365](/power-platform/admin/pricing-billing-skus?azure-portal=true#licenses).

## Reasons to use environments

Reasons to create environments beyond the default one include:

- **Separate app development by department** - In a large organization, each department can work in a different environment. That way, department employees see only apps and company data that are appropriate to their needs.
- **Support application lifecycle management (ALM)** - Separate environments let you separate apps that are in development stages from those that have already been shared. Alternatively, you might want to use a trial environment so that you can receive feedback from employees before publishing the final app. For some organizations, showing apps before they're completely developed and published can present security concerns.
- **Manage data access** - Each environment can have its own source of business data, called a database for Microsoft Dataverse.
Other data connections are specific to an environment and can't be shared across environments.

> [!NOTE]
> Keep in mind that environments are relevant only to app creators and Power Apps admins. When you share an app with users, those users simply run the app, providing they have the correct permissions. In other words, they don't have to worry about what environment the app came from.

## Create an environment

Only an admin can create environments. If you aren't an admin, this information can still be helpful when you talk to your admin about setting up environments.

1. On the [make.powerapps.com](https://make.powerapps.com/?azure-portal=true) home page, select the gear icon near the upper-right corner and then select **Admin center**.

    You can also go directly to [https://admin.powerplatform.microsoft.com](https://admin.powerplatform.microsoft.com/?azure-portal=true)
2. In Microsoft Power Platform admin center, select **+ New**.
3. In the **New environment** dialog box, enter a name for the environment and then select a region and an environment type.
4. To the left of **Create a database for this environment**, select the toggle to Yes.
5. Select **Next**.
6. Select the currency and language for the data that is stored in the database. You cannot change the currency or language after the database is created.
7. Select **Save**.

    It might take several minutes to create the database on Dataverse. After the database is created, the new environment appears in the list of environments on the **Environments** page.

You now have a new environment to work in. If you go back to [make.powerapps.com](https://make.powerapps.com/?azure-portal=true), you will see it in the environments list.

## Manage access to an environment

By default, you can access an environment in one of two ways:

- **System admin** - A system admin has full permissions to create and manage environments.
- **Environment maker** - An environment maker can view all apps in that environment, create apps, and work with Dataverse (other permissions apply).

Environment admins can create other security roles as needed. They can also add and assign users to these roles.

1. Start by going to [https://admin.powerplatform.microsoft.com](https://admin.powerplatform.microsoft.com/?azure-portal=true)
2. On the left pane, **Environments** should be selected by default, if it is not, select **Environments**.
3. Select the test environment that you just created, and then select **Settings** at the top.
4. Select the **Users + permissions** dropdown and select **Users**.
5. Select **Add user** at the top and add the user by entering the email address of the user in your organization and then selecting **Add**. Wait a few minutes for the user to be added.
6. To manage the roles and information of a user, select the user’s **Name**. This will open a new tab with the Dynamics 365 view of that user.
7. Select **Manage Roles** on the top bar.
8. In the **Manage User Roles** box, select the role(s) for the user. In this example, assign the user to the Environment Maker role.
9. Select **OK**.
10. The changes are then saved, so you can close the Dynamics 365 tab in your browser when done.
