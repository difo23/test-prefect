![img](https://d33wubrfki0l68.cloudfront.net/a932a03aeeef5a2531bae4f12067eb2efb6d0967/19f1f/illustrations/core-illustration.svg)



[Prefect Core](https://www.prefect.io/products/core) is a new kind of workflow management system that makes it easy to take your data pipelines and add semantics like retries, logging, dynamic mapping, caching, failure notifications, and more.

We started with a simple premise:

> Your code probably works. But sometimes it doesn't.

## Tasks are functions

In a simple sense, Prefect tasks are functions that have special rules about when they should run: they optionally take inputs, perform some work, and optionally return an output. Tasks can process data directly, or orchestrate external systems, or call out to other environments or even languages -- there are almost no restrictions on what a task can do. Furthermore, each task receives metadata about its upstream dependencies before it runs, even if it doesn't receive any explicit data inputs, giving it an opportunity to change its behavior depending on the state of the flow.

Because Prefect is a negative engineering framework, it is agnostic to the code each task runs. There are no restrictions on what inputs and outputs can be.

## Workflows are containers

Workflows (or "flows") are containers for tasks. Flows represent the dependency structure between tasks, but do not perform any logic.

## Automation framework

A proper automation framework has three critical components:

- Workflow definition
- Workflow engine
- Workflow state

Prefect Core includes all three, and the design of each piece was heavily informed by user research and applied knowledge.

## Install

- Use Ubuntu 20.04
- docker --version Docker version 20.10.12, build e91ed57
- docker-compose --version docker-compose version 1.29.2, build 5becea4c
- python3 --version Python 3.8.10

```bash
conda install -c conda-forge prefect
```

You must install docker and docker-compose before you start working with Prefect.

```bash
pip install "prefect[extra_1, extra_2]"
```

Note: You may have problems installing Prefect locally, the problems are usually at the user permissions level, you need to have Prefect installed globally on your machine to be able to start the local server comfortably. In a virtual environment the server can give you several problems.

