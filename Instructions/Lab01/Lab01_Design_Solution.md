**Process Advisor & Importing Solution**

**⏱️ The estimated time to complete this lab is 2 hours 30 minutes.**

**Scenario**

In this lab, you will be working to design the automation of a Construction Loan
Funding process that is currently manually tracked by Relecloud staff.

**High-level lab objectives**

-   Discover the current process

-   Use Process Advisor to visualize and analyze the current process

-   Evaluate automation options

-   Design the automation of the process

-   Import and review the starter solution

**Exercise \# 1 – Discover Current Process**

In this exercise you are going to get to know the current manual process.

**Task 1: Review the process scenario**

The following companies or people are involved in the process you will be
automating.

| **Company or people** | **Description**                                                                                                                             |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| Borrower              | Borrows money from bank to build a house.                                                                                                   |
| Builder               | Has an agreement to build house for Borrower and gets paid as the house is built by Loan Draws from the borrower’s loan.                    |
| Woodgrove Bank        | Loans borrower money to build house, hires Relecloud to manage the construction loan draw funding as the house is built by the builder.     |
| Relecloud             | Escrow company that manages the process for the bank. They do all the manual work today and this is who you are automating the process for. |
| Fabrikam Inspections  | An inspection company that goes on site to verify and provide proof of work completed.                                                      |
| A Datum               | A risk management company that helps banks reduce losses from bad loans. They provide a risk score used in the process.                     |

The following describes the current manual process:

Woodgrove Bank does construction loans to builders to build homes. Woodgrove
does not give all the loan money to the builders on initial approval they only
give it as construction progresses. Each month, builders can request loan funds
(a draw) for the progress made and funds spent during the last month.

Woodgrove is too busy to manage the process, so they hired Relecloud to manage
it. Each month builders email forms requesting funds to Relecloud. After review,
Relecloud requests Fabrikam Inspections via their website to do an onsite
inspection to verify the work stated was actually done.

Once the inspection is completed, Relecloud does a risk check using a website A
Datum has that confirm that the builder hasn’t become high risk. After these
checks, Relecloud uses a Windows form app provided by Woodgrove to request
funding. Someone from Relecloud checks the app each day for any completed
requests and then they notify of funding completed.

Today Relecloud does each process step manually. You have been asked if you can
improve the process by automating some of the process.

**Task 2: Review the draw request form**

1.  Go to the lab resources folder and open the Draw1-MC3747.pdf file.

2.  Review the form.

3.  This form is completed for each draw by the builder and emailed to
    Relecloud.

**Task 3: Review the loan tracking Excel file**

1.  Go to the lab resources folder and open the LoanTracking-MC3747.xlsx file.

2.  Review the loan tracking file.

3.  Relecloud staff creates one of these worksheet files for each loan and uses
    it to track the draws on the loan.

**Exercise \# 2 – Use Process Advisor with Data**

In this exercise, you will create a process advisor from existing process data
and review the analytics.

**Task 1: Create process advisor**

1.  Navigate to https://make.powerautomate.com and select **Get started** to
    dismiss the welcome prompt, if necessary.

2.  Select the **Dev One** environment from the **Environment** drop-down.

3.  Select **Process mining** from the left navigation pane and select **+ Start
    here**.

![Select process advisor](media/d08815633b5a8b6a8e67e35bc24697d3.png)

1.  Enter Loan Funding - Data for **Process name** and select **Continue**.

![Select data to create the process](media/4b54e77a18dd9a31584c8245185f641a.png)

1.  Select **Excel workbook**.

2.  Select **Upload file** and click **Browse**.

![Select Upload file and click
Browse.](media/c2fedd56ab65db47f20564422c0d2303.png)

1.  Select the **ExistingProcessData.xlsx** file located in the lab resources
    folder and click **Open**.

2.  Select **Sign in**.

![select the file location and then sign
in](media/1eb90edb5b8371fba3903afb1d5408c1.png)

\> Note: You may need to configure your pop-up blocker to allow this site to
create pop-up windows.

1.  Provide your credentials and sign in.

2.  Select **Next**.

![confirm credentials and select
next](media/a98b7328aa7010f01bf3115763dacb6e.png)

1.  Select the **ConstructionFunding** item and select **Next**.

![select the data and choose next](media/df41f6bcff75c35d28cf4b9bc6f071e4.png)

1.  Select **Next**.

![Click Next](media/858cae32165e971a45c2fd22f0c5785b.png)

1.  Map the mandatory fields. For each **Event Level Attribute** drop-down,
    select as follows:

    -   StartTimestamp: **Event Start**

    -   CaseId: **Case ID**

    -   ActivityName: **Activity**

![Map your data](media/90ad0fd702ebeb593bf94f26b9f9bc8a.png)

1.  Select **Save and analyze**.

2.  **Wait** for the analyzing to complete.

**Task 2: Review analytics**

1.  The produced process map should look similar to the image below.

![process map for review](media/c59c564e7bf61a79b53858e484165231.png)

1.  Zoom in to find the **Request Funding** activity. Notice there is a path or
    variant for approved draw and a different one for denied draw.

![drill into mapping for review](media/1fd5bb26f267fd07d4d1212b66d46eee.png)

1.  Go to the **Variants \> Frequency** chart and select the bar with the
    highest frequencies. This is the most common path the process takes; in our
    case this is the **Draw Approved** path.

![process data to review](media/5fb18313f229aab61692d8c55515414e.png)

1.  Go to the **Variants \> Frequency** chart and select the second bar. This is
    the frequency for the approved draw path.

![review frequencies](media/0a561d188c96ac5daaa111b182f60019.png)

1.  Select the last bar. This is the frequency for the denied draw.

![additional data to review](media/9d15e82bcaf5df1bdc3a874692426593.png)

\> \*\*Note:\*\* These Power BI charts allow drilling down on a specific data
point and filtering.

**Exercise \# 3 – Use Process Mining with Recording**

In this exercise, you will perform task analysis by recording using the
Woodgrove Bank Funding Manager application, add activities, and then analyze it.

**Task 1: Create process advisor**

1.  Navigate to
    [https://make.powerautomate.com](https://make.powerautomate.com/) and make
    sure you are in the **Dev** environment.

2.  Select **Process mining** and select **+ Start here**.

![start process advisor](media/d08815633b5a8b6a8e67e35bc24697d3.png)

1.  Enter **Loan Funding - Recording** for Process name, select **Recordings**,
    and select **Continue**.

![select recording option](media/99e265e341680420e8480f057965d7a0.png)

1.  Select **Add a recording**.

![choose add a recording](media/4908c04c770813a6fe4d3f2cb9d6304f.png)

1.  Power Automate desktop should launch. The browser may prompt "This site is
    trying to open Power Automate Designer", select **Open**.

2.  Do not start recording yet.

**Task 2: Record process**

Before you start recording, you should familiarize yourself with the
application, so the recording goes smoothly.

1.  Minimize or close all windows except Power Automate Desktop.

2.  Go to the Start menu and launch the **Woodgrove Bank Funding Manager**
    application. If not displayed, go to the lab resources folder
    (C:\\Labs\\Resources\\Funding manager app) and launch from there.

![Find and open the app](media/e89882da12c32d1f44341e2332080042.png)

1.  Enter your name for username, pass@word1 for password and select **Login**.

![Follow login prompts](media/b2c31b88d95f46657d931d28095742f5.png)

1.  Enter **JG7165** for Loan number and select **Lookup**.

2.  Select **Draw Funds**.

![review and click draw funds](media/3898d5ae58759be59f5882b03bc2b472.png)

1.  Enter 100000 for **Amount**, 12345 for **Inspection job number**, 65 for
    **Risk Score**, check the **Borrower Approved Draw** checkbox, and select
    **Draw Funds**.

![Fill out listed details and select draw
funds](media/6afd4cc64109194c8f50a1533dcece3f.png)

1.  Select **OK**.

2.  Repeat steps **4 to 7** a few more times or until you feel comfortable with
    using the funding application.

3.  You are now ready to record. Go to the recorder and select **Record**.

![record the listed steps](media/6e6bff4dcbd0b71846411e0407b4d60a.png)

1.  Go to the funding application and repeat steps **4 to 7**.

2.  On the recorder, select **Finish**.

3.  Select **Got it** and return to Power Automate web portal, select **View
    recording**.

![click View recording](media/3db0cfe701568540f7b757af885ebf1c.png)

1.  The recording should look like the image below. You can delete and record
    again if you are not happy with recoding.

![image of recorded steps](media/f3a0f60b6f26d510c64ac76806e17503.png)

1.  Select each action and examine the action details.

![review the resulting steps](media/f92d77bf3cdd34a06f5e3ffc0f5d17b2.png)

1.  Notice the auto-created activities.

![review auto-created steps](media/a66864a0cdc8e30f1e9453335672b08b.png)

1.  We will delete these auto-created activities and create our own in the next
    task.

2.  Do not navigate away from this page.

**Task 3: Create activities**

In this task, you will group actions into activities.

1.  Navigate to the process by clicking on the name of the process.

![navigate to the process
definition](media/51fe16353931997ccf1b4532608d3c23.png)

1.  Select **Create activity names**.

![select create activities](media/c1d8cc0bbe75e6995eb68b4ea41c0a0a.png)

1.  Select **+ New name**.

2.  Enter **Lookup** and select **+ New name** again.

![create listed activities](media/13bc34601f58d0643dfa13a973bcd436.png)

1.  Enter Draw Request and select **+ New name** again.

2.  Enter Approve and select **+ New name** one more time.

3.  Enter Fund and select **Save**.

![create listed activities](media/acf3e4b6789016049fbc814e1b49026a.png)

1.  **Close** the create activity names pane.

2.  Go to the **Recordings** section and select to open the recording.

![open the recording](media/1d2b1755c6288802ea3827ba0ebcc3d7.png)

1.  Select **Delete all activities**.

![delete activities that were auto
created](media/1fcf7213ff01e875206457e932a3a8f0.png)

1.  Select **Delete**.

2.  Select **+ Add activity**.

![add activities you created](media/67f471d3c4ac2cdc16d95df5950f0040.png)

1.  Select the **Name** drop-down and choose **Lookup**.

![select the lookup activity](media/fa6b6d4470996bb444fe7c5fb24b14b8.png)

1.  The Lookup activity will be added.

2.  Select **+ Add activity** again.

3.  Select the **Name** drop-down and choose **Draw Request**.

4.  The Draw Request activity will be added.

5.  Select **+ Add activity** again and add **Approve**.

6.  Select **+ Add activity** one more time and add **Fund**.

7.  You should now have 4 activities added.

![review added activities](media/06332bd7618b19a16eb3fe7298fedfe0.png)

1.  Drag the **Draw Request** activity and place it below the second action. You
    are combing the first two actions into one **Lookup** activity.

![order items into the activities](media/88519ef11cc38c59dc6522de163818df.png)

1.  Drag the **Fund** activity and place it below the **Draw Funds** action.

2.  Drag the **Approve** activity and place it below the **Draw Funds 2**
    action.

3.  The activities should now look like the image below.

![all activities and actions should be
organized](media/a310ad72e32fe77affe94adc23f4d648.png)

1.  Select **Save and analyze**.

2.  **Wait** for the process to be analyzed.

3.  Do not navigate away from this page.

**Task 4: Review analytics**

1.  Select **View analytics**.

![select to view the analytics](media/89249723fccaf71c3923be311e042a4e.png)

1.  The process should look like the image below.

![review the process](media/922492314e0a4189f39d05355b52ed89.png)

1.  Select the **Application** tab and review it.

![review the charts](media/6082e6cdc632142b0abfc3e96073fa6e.png)

**Exercise \# 4 – Evaluate Automation Options**

When you automate a process, you want to use the most efficient and reliable
means of automation possible. In this exercise you will re-review what you know
about the process and what should be automating an app and what should use an
API.

**Task 1: Review and make notes of what should use an app and what should be a
connector**

A discovery process has been completed by the project team. The following is the
original scenario with our notes from the discovery added.

Woodgrove Bank does construction loans to builders to build homes. Woodgrove
does not give all the loan money to the builders on initial approval they only
give it as construction progresses. Each month, builders can request loan funds
(a draw) for the progress made and funds spent during the last month.

Woodgrove is too busy to manage the process, so they hired Relecloud to manage
it. Each month builders email forms requesting funds to Relecloud. After review,
Relecloud requests Fabrikam Inspections via their website to do an onsite
inspection to verify the work stated was actually done. *During discovery we
learned that Fabrikam has no plans to offer an API*.

Once the inspection is completed, Relecloud does a risk check using a website A
Datum has that confirm that the builder hasn’t become high risk. *During
discovery we learned A Datum has a RESTful API for the risk check*.

After these checks, Relecloud uses a Windows form app provided by Woodgrove to
request funding. Someone from Relecloud checks the app each day for any
completed requests and then they notify of funding completed. *During discovery
we learned that Woodgrove plans to modernize the app in the future*.

Today Relecloud does each process step manually. You have been asked if you can
improve the process by automating some of the process.

**Exercise \# 5 – Design the automation**

In this exercise, you will review the design the team came up with. In the rest
of this course, you will be building out this automation.

**Task 1 – Review the process diagram**

![process diagram](media/a5eb8462c83e313d61e24f384538d9e9.png)

**Task 2 – Review design notes**

-   A shared mailbox will be used to not be dependent on individual users

-   Dataverse tables will be used instead of Excel worksheets to track the
    process. There will be a Loan, Loan Draw and Inspection Photo tables.

-   Child flows will be used for Lookup, Inspection and Funding to keep the main
    cloud flow maintainable.

-   Inspection website will be automated with an unattended desktop flow which
    will include a JSON array of work site photos.

-   The inspection child flow will run the inspection desktop flow and then
    download and persist the work site photos to the Dataverse table.

-   A custom connector will be built for A Datum’s Risk API.

-   The Woodgrove Funding Manager Windows app will be automated with a desktop
    flow.

**Exercise \# 6 – Import starting solution**

In this exercise, you will import a solution into your dev environment, review
the components in the solution, run a cloud flow that will add test data to your
environment, and run the loan manager app included in the solution.

**Task 1: Import solution**

1.  Navigate to https://make.powerapps.com and make sure you are in the **Dev**
    environment.

2.  Select **Solutions** and select **Import solution**.

![Import the provided solution](media/a915db97dbe754debafa74f02c8bbf9a.png)

1.  Select **Browse**.

2.  Select the **ConstructionFunding** solution file located in the lab
    resources folder and click **Open**.

![select the solution provided](media/0a98d33dbb9eb8f3e73da61cfd16dc45.png)

1.  Select **Next**.

2.  Select **Next** again.

3.  Wait for the listed connection to sign in automatically and show a green
    check.

4.  Select **Import** and wait for the import to complete.

5.  You will get a notification when the import completes.

![success message](media/0deaa0bb30a3a1c85449ccc44c60e2f4.png)

1.  Select **Publish all customizations** and wait for the publishing to
    complete.

![publish customizations from imported
solution](media/c6a0dee6b49f3983e899397433d679ad.png)

1.  Do not navigate away from this page.

**Task 2: Review components**

1.  Open the recently imported **Construction Funding** solution.

![review solution components](media/267c327653d35762f04898450ffe7500.png)

1.  The solution should have several components including 1 application, 1 cloud
    flow, 1 connection reference, 1 sitemap, and 3 tables.

2.  Expand **Tables**, expand the **Loan** table and select **Columns**.

3.  Review the columns for this **Loan** table.

![solution contains tables](media/526cfdd35421e061d17da5e1f269acc5.png)

1.  Expand the **Loan Draw** table and select **Columns**.

2.  Review the columns for this **Loan Draw** table.

3.  Select **Cloud flows** and open the **Create Test Data** cloud flow.

![select cloud flow to run](media/a72e54ed3dbc96a09705f8cd2d806ae7.png)

1.  Select **Edit**.

![select edit](media/1529d83046dcf544e9b8647822f57871.png)

1.  Expand the **Parse JSON** step and review the data that will be added to
    your environment.

![expanded parse JSON step](media/ce09b84f22ae831a38a1331fb18c5d15.png)

1.  Select the back button.

2.  Do not navigate away from this page.

**Task 3: Run flow**

1.  Select **Cloud flows** and select **Details** to open the **Create Test
    Data** cloud flow.

![select the flow to run](media/a72e54ed3dbc96a09705f8cd2d806ae7.png)

1.  Select **Run**.

![run the flow](media/f4518a3c9e2224891f862ebf2d42e75f.png)

1.  Select **Run flow**.

2.  Select **Done**.

3.  **Wait** for the flow run to complete.

4.  Select the refresh button until you see the success message.

![flow successed](media/5bb0703fee4a165f9f9e33d72d9e51d5.png)

**Task 4: Run loan manager app**

1.  Navigate to https://make.powerapps.com and make sure you are in the **Dev**
    environment.

2.  Select **Apps** and launch the **Loan Manager** application.

![start the app](media/52dbfbd920d573add672f2dd66da8d73.png)

1.  You should see the data added by the cloud flow. Open one of the loan
    records.

![review data](media/4c364674993d88f1d1ff212637f6a9d9.png)

1.  Review the loan.

![review load record](media/a91e8235e2efd2bec19bd2e865b2887c.png)
