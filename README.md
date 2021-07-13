# notion-tools-alfred-workflow
An Alfred workflow to add / change tasks to Notion.so

This workflow uses [OneUpdater](https://github.com/vitorgalvao/alfred-workflows/tree/master/OneUpdater) for automatic version updates.

# Keywords

## an: Add Notion task for a project

Simply type your task name, date and time into Alfred to create a task page to Notion.
The date and time are optional.

Title only|With date|With date and time|
:-:|:-:|:-:
|![no date](an1.png)|![with date](an2.png)|![with date and time](an3.png)|

After typing, select a corresponding project from project lists.
The project list was cached into this workflow.
If you want to update the project list, type `shift` + `return` when typing a task name.
|Project selection|Force reload project (shift + return)|
:-:|:-:
|![select project](selectProjects.png)|![Force reload](an4.png)|

## ac: Add calendar event for Notion calendar

Simply type your task name into Alfred to create a task event to Notion calendar.

Title only|With date|With date and start time|With date, start time and end time|
:-:|:-:|:-:|:-:
|![no date](ac1.png)|![with date](ac2.png)|![with date and time](ac3.png)|![with date and time](ac4.png)|

## ar: Add a refrection sentence to today's refrection page

Simply type your sentence into Alfred to append the sentence block to a daily refrection page.
![ar](ar.png)

## pn: Set pomodoro property to today's tasks

Select an unfinished task from list, and settle a correspond pomodoro period.
Select task|Select pomodoro|
:-:|:-:
|![select task](pn1.png)|![select task](pn2.png)|

# Workflow Variables

- `MY_NOTION_TOKEN`: Your Notion token.
- `TASK_ID`: Database ID for your task database.
- `PROJECT_ID`: Database ID for you project database.
- `MY_TZ`: Your timezone.  Defaults to "+09:00".
- `TASK_DATE`: Date property name for the task.
- `TASK_POMO`: Pomodoro property name for the task.  Do not use Japanese character `ポモ`, because of the NFC-NFD problem.
- `TASK_DONE`: Task finished flag property name for the task.
- `TASK_IS_NOT_POMO`: (Optional) Not pomodoro flag property name for the task.
- `TASK_IS_POMO`: (Optional) Pomodoro flag property name for the task.
- `PROJECT_NAME`: Title name for Project database.  Do not use Japanese character `プロジェクト`, because of the NFC-NFD problem.
- `PROJECT_LINK_NAME`: Relation title to Project for the task.  Do not use Japanese character `プロジェクト`, because of the NFC-NFD problem.
- `REFRECTION_TITLE`: Refrection page title.
- `NOTION_CALENDAR`: Calendar name for Notion Calendar.

# How to use

## Notion setup

In this workflow, two Notion database (Task and Project) are required.
A task page belongs to a project page.
Please check [a sample template](https://www.notion.so/Sample-database-for-notion-tools-alfred-workflow-5b5556f7fec84468ad1e4fe2bdea2db3) for these database.

## Notion API setup

Next, set API setting.  Please see [Getting Started](https://developers.notion.com/docs/getting-started) in the Notion Developer page.
Please remind `MY_NOTION_TOKEN` and database_id for the above two databases (`TASK_ID` and `PROJECT_ID`).

## Set workflow variables

In the Alfred worfklow in the upper right corner click the `[x]` icon and add the values from above to the corresponding value field.
Please set the above three parameters, and modify the other environment variables to match the properties of your database.
![environments](environments.png)

## Change keyword and icon image (Optional)

You can change the keyword and the image icon in the keyword box.
![keyword box](keyword.png)

# Download

https://github.com/hkob/notion-tools-alfred-workflow/releases/latest/download/NotionTools.alfredworkflow

