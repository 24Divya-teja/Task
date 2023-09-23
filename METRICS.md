To support reporting and Gantt charts in your project management tool, it's important to collect relevant metrics for each task. Here are some key metrics to consider:

Task Duration: Measure the time taken to complete each task. This metric helps track the efficiency of task execution and can be used to calculate project timelines.

Task Dependencies: Identify and track the dependencies between tasks. This metric allows you to determine which tasks need to be completed before others can start, enabling accurate Gantt chart visualization and project scheduling.

Task Progress: Monitor the progress of each task as a percentage or a milestone. This metric provides insight into the completion status of tasks and helps track overall project progress.

Task Assignee: Record the person or team responsible for each task. This metric allows you to track task ownership and workload distribution across team members.

Task Priority: Assign a priority level (e.g., high, medium, low) to each task. This metric helps in prioritizing and scheduling tasks and can be useful for resource allocation.

Task Status: Track the status of each task (e.g., backlog, active, overdue, done). This metric provides an overview of the current state of tasks and can be used for reporting and generating task-specific charts.

Task Start Date: Capture the start date of each task. This metric is essential for calculating task durations, identifying delays, and creating Gantt charts to visualize task timelines.

Task Due Date: Set a due date for each task. This metric helps track task deadlines, identify overdue tasks, and generate alerts or notifications for task management.

Task Comments/Notes: Allow users to add comments or notes to tasks. While not directly a metric, this information provides valuable context, updates, or discussions related to tasks and can be useful for reporting and collaboration purposes.

Task Completion Date: Record the date when a task is marked as complete. This metric helps analyze task completion trends, track actual vs. estimated completion times, and generate performance reports.

By collecting these metrics for each task, you will have a solid foundation for generating insightful reports and visualizations, including Gantt charts. The combination of task durations, dependencies, progress, assignees, priorities, statuses, and dates provides comprehensive data for project analysis, resource allocation, and monitoring overall project health.


## Description why
The modifications and additions to the models are as follows:

In the Task model:

Added start_date field to capture the start date of each task.
Added completion_date field to record the date when a task is marked as complete.
Added progress field to monitor the progress of each task (as a percentage or milestone).
Added assignee_id field to record the user or team responsible for each task.
Added priority field to assign a priority level (e.g., "HIGH", "MEDIUM", "LOW") to each task.
Established a relationship with the TaskDependency model through the dependencies relationship.
Established a relationship with the TaskComment model through the comments relationship.
Introduced the TaskDependency model to represent task dependencies. This model includes the task_id and dependency_id columns, which refer to the task and its dependent task, respectively. Additional fields can be added to capture the type of dependency if needed.

No changes were made to the TaskComment model, as it already exists in the previous model definition.

These modifications allow you to capture and store the necessary data to support the suggested metrics, enabling reporting, analytics, and Gantt chart generation based on task duration, dependencies, progress, assignee, priority, status, start date, due date, comments/notes, and completion date.