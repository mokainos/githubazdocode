https://www.markdownguide.org/cheat-sheet/
# Tiggers
1. All trigger paths are case-sensitive.
2. Continuous integration (CI) triggers vary based on the type of repository you build in your pipeline
3. Pull request validation (PR) triggers also vary based on the type of repository.
4. Comment triggers are supported only for GitHub repositories.
5. Scheduled triggers are independent of the repository and allow you to run a pipeline according to a schedule.
6.  Pipeline triggers in YAML pipelines and build **completion triggers**  in classic build pipelines allow you to trigger one pipeline upon the completion of another.
7.  For example, YAML pipelines in a GitHub repository have **CI triggers and PR triggers** enabled by default.
8.  You can combine scheduled and event-based triggers in your pipelines, for example to validate the build every time a push is made (CI trigger), when a pull request is made > (PR trigger), and a nightly build > (Scheduled trigger)

## Schedule Triggers
    You can't use pipeline variables when specifying schedules
    By default, your pipeline doesn't run as scheduled if there have been no code changes since the last successful scheduled run.
        ```
            schedules:
            - cron: string # cron syntax defining a schedule
            displayName: string # friendly name given to a specific schedule
            branches:
            include: [ string ] #which branches the schedule applies o
            exclude: [ string ] # which branches to exclude from the schedule
            always: boolean # whether to always run the pipeline or only if there have been source code changes since the last successful scheduled run. The default is false.
        ```
### CI Triggers
    Continuous integration (CI) triggers cause a pipeline to run whenever you push an update to the specified branches or you push specified tags.
    If you use templates to author YAML files, then you can only specify triggers in the main YAML file for the pipeline. You cannot specify triggers in the template files.
