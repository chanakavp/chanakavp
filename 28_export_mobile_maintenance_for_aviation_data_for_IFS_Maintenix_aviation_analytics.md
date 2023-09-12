<!-- title: Export Mobile Maintenance for Aviation Data for IFS Maintenix Aviation Analytics-->

# Export Mobile Maintenance for Aviation Data for IFS Maintenix Aviation Analytics

Customers using Mobile Maintenance for Aviation and IFS Maintenix Aviation Analytics for their reliability reporting and can extract data related to faults, component removals, and assembly removals from the IFS Cloud.

You can accomplish this through the following migration jobs in the MIG_MAA migration group:

| **Migration Job ID**      | **Description**                                              |
| ------------------------- | ------------------------------------------------------------ |
| 010_MM_CLOSED_FAULTS_EXPT | Extracts data relevant to all raised and closed faults in Mobile Maintenance for Aviation. |
| 011_MM_COMP_RMVL_EXPT     | Extracts data relevant to component removals associated  with completed tasks and faults, excluding data for assemblies and batch  parts. |
| 012_MM_ASSY_RMVL_EXPT     | Extracts data relevant to assembly removals associated  with completed tasks and faults. |

## Grant Migration Job Access to a User

To allow a user to run migration jobs, you need to grant them access.

1. Log in to the IFS Cloud as an administrator.

2. Go to **Solution Manager**/**Data Management**/**Data Migration**/**Basic Data/Authorized Users**. 

3. Select the user. If the user does not exist, create a user and allow update for the user. 

4. To give access to an individual migration job:

    a. Click **New** (+ icon) under **Migration Jobs granted to the User.**
    
    b. Select the migration job ID. 
    
    c. Click **Save**.

5. To give access to all migration jobs in the MIG_MAA migration group:

    a. Click **Bulk Grant** under **Migration Jobs granted to the User**.
    
    b. From the **Group ID** field in the filter panel, filter migration jobs by *MIG_MAA* group.
    
    c. Select all migration job IDs and click **OK**.

## Execute a Migration Job

To execute a migration job, follow the steps below.

1. Log in to the IFS Cloud as an administrator.

2. Go to **Solution Manager**/**Data Management**/**Data Migration**/**Migration job** and select the migration job by searching for the migration job ID.  

3. Click **Execute Job**.

4. Click **Start Job** > **Online**. Once the migration job execution is complete, a message appears.

5. Go to the **DETAIL** tab and click **Export to File**.

6. For **File Name**, enter a file name recognized by IFS Maintenix Aviation Analytics, as follows:

    | **Migration Job ID**      | **File Name**                  |
    | :------------------------ | ------------------------------ |
    | 010_MM_CLOSED_FAULTS_EXPT | STG_FACT_FAULT.csv             |
    | 011_MM_COMP_RMVL_EXPT     | STG_FACT_COMPONENT_REMOVAL.csv |
    | 012_MM_ASSY_RMVL_EXPT     | STG_FACT_SUBASSY_REMOVAL.csv   |

7. Click **OK**. The .csv file is downloaded to your computer.