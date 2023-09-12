<!-- title: Set up a service user to integrate with the flight API-->

# Set up a Service User to Integrate With the Flight API

In order to allow third-party flight following systems to update flights in Mobile Maintenance for Aviation using the IFS Cloud Open API, you need to set up a service user, grant necessary permissions, and bind the user to an IAM client.

## Set up a Service User

1. Log in to the IFS Cloud as an administrator.

2. Go to **Solution Manager**/**Users and Permissions/Users/User** and click **New** (+ icon).  

3. Enter the following information:

    a. **Identity**: FLIGHT_API

    b. **Description**: Enter a description. E.g., Flight API user

    c. **User Type**: Service User

4. Leave other fields unchanged.

5. Click **Save**.

6. Go to **User Permissions** and click **Grant Permission Sets** in the **DIRECT GRANTS** tab**.**

7. Select the **MM_FLIGHT_API** permission set and click **OK**.

## Set up an IAM Client

1. Log in to the IFS Cloud as an administrator.

2. Go to **Solution Manager**/**Users and Permissions**/**Identity and Access Manager/IAM Client** and click **New** (+ icon). 

3. Enter the following information:

    a. **Client ID:** *MM_FLIGHT_API*

    b. **Description:** Enter a description. E.g., Flight API User

    c. **Service Accounts**: Yes

    d. **Direct Access Grant**: Yes

    e. **Username**: FLIGHT_API (the user created in the previous procedure)

4. Click **OK**.