---
title: Workers and Queues
---

With the **Workers and Queues** page, users can:

* Monitor resources (CPU and GPU, memory, video memory, and network usage) used by the experiments / Tasks that workers
  execute
* View workers and the queues they listen to
* Create and rename queues; delete empty queues; monitor queue utilization
* Reorder, move, and remove experiments from queues



## Resources Utilization

**To monitor resource utilization:**

1. In the **WORKERS** tab, click a worker. The chart refreshes showing resource utilization over time for that worker. The
   worker **INFO** slides open, showing information about the worker:
   * Name
   * Current experiment
   * Current runtime
   * Last iteration
   * Last update time.

1. Select a metric and time frame:

    1. In the list of resources (top left side), select **CPU and GPU Usage**, **Memory Usage**, **Video Memory Usage**, or **Network Usage**.

    1. In the period list (top right side), select **3 Hours**, **6 Hours**, **12 Hours**, **1 Day**, **1 Week**, or **1 Month**.

![Worker management](../img/agents_queues_resource_management.png)



## Worker Utilization

Optimize worker use by monitoring worker utilization in the **Workers** tab.

**To monitor worker utilization:**

* Open the **Workers** tab in the **Workers & Queues** page. The worker utilization chart
  appears. Hover over any data point and see average workers and total workers.



## Queue Utilization

**To monitor all queues:**

* Open the **Queues** tab in the **Workers & Queues** page. The queue utilization chart appears and shows
 average wait time (seconds) and number of experiments queued for all queues.
* Hover over any data point and see average wait time and number of experiments.

![image](../img/4100.png)

**To monitor a queue:**

1. In the queues list (below the plot on the left), click a queue.
1. The chart refreshes, showing metrics for the selected queue. The info panel slides open with two tabs:
   1. To see the enqueued experiments on the queue, click the **EXPERIMENTS** tab.
   2. To view information about the workers listening to the queue, click the **WORKERS** tab.



## Queue Management

The **Queues** tab lets you manage your queues and their contents:

* Create a queue - Click **+ NEW QUEUE** (top right)
* Right-click on a queue in the queues list to modify the queue:
  
  ![Queue context menu](../img/webapp_workers_queues_context.png)
  
    * Delete - Delete the queue. Any pending tasks will be dequeued.
    * Rename - Change the queue’s name
    * Clear - Remove all pending tasks from the queue
    * Custom action - The ClearML Enterprise Server provides a mechanism to define your own custom actions, which will 
      appear in the context menu. See [Custom UI Context Menu Actions](../deploying_clearml/clearml_server_config.md#custom-ui-context-menu-actions)
* Click on a queue to select it and see its task and worker information. Click on a
  task’s menu button <img src="/docs/latest/icons/ico-dots-v-menu.svg" alt="Menu button" className="icon size-md space-sm" />
  in the **EXPERIMENTS** tab to reorganize your queue. 
  
  ![Queue experiment's menu](../img/workers_queues_experiment_actions.png)  
  
    * Move a task to the top or bottom of the queue
    * Move the task to a different queue
    * Dequeue the task
    
  You can also reorder experiments in a queue by dragging an experiment to a new position in the queue
