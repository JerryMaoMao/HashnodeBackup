---
title: "Building Applications Faster with ILLA and TiDB"
seoTitle: "Building Applications Faster with ILLA and TiDB"
seoDescription: "ILLA, the low code open source platform for developers, is proud to announce a partnership with PingCAP."
datePublished: Wed Nov 09 2022 11:06:43 GMT+0000 (Coordinated Universal Time)
cuid: cldvkgbjd00000ambc7pea042
slug: building-applications-faster-with-illa-and-tidb
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1675854004163/f8fab5d5-33b7-4dad-b29d-f158c18b41b7.png
tags: low-code, tidb, illa, internal-tool, pingcap

---

[**ILLA**](https://www.illacloud.com/), the low code open source platform for developers, is proud to announce a collaboration with PingCAP’s [**TiDB**](https://www.pingcap.com/tidb/), an open-source distributed NewSQL database that features horizontal scalability, high availability, real-time Hybrid Transactional and Analytical Processing (HTAP), and MySQL compatibility. This partnership aims to simplify application development by providing a database that meets data consistency, reliability, availability, scalability, and disaster tolerance requirements.

Today, organizations have to store, process, and manage more and more data; single-machine databases are hitting their physical limits. Traditional sharding mechanisms are unwieldy and hard to maintain as the business grows. TiDB solves these problems transparently through its distributed architecture while maintaining MySQL compatibility. TiDB Cloud, the fully managed TiDB service, can also simplify deployment, management, and maintenance through a web-based management interface in the cloud.

This tutorial will show you how to set up a TiDB cluster and build an administration panel that allows you to create, read, update, and delete entries. We’ll display the data in a table and use a panel to tab between creating and editing forms. We’ll do all this in less than 10 minutes.

## [**​**](https://www.illacloud.com/blog/building-applications-faster#create-a-free-cluster-on-ti-db-cloud)**Create a free cluster on TiDB Cloud**

To create a cluster on TiDB Cloud:

1. [**Sign in**](https://tidbcloud.com/) with your TiDB Cloud account. If you are a new user, [**sign up**](https://tidbcloud.com/free-trial/) for an account.
    
2. Create a free cluster and connect to it. Click [**Quick Start TiDB**](https://docs.pingcap.com/tidb/dev/dev-guide-build-cluster-in-cloud) to learn how to use it. After running the sample application, you will get the TiDB connection information, including the server name, port number, database name, user name, and password. Be sure to note these; you’ll be using them in later steps.
    

## [**​**](https://www.illacloud.com/blog/building-applications-faster#connect-to-ti-db-with-illa-builder)**Connect to TiDB with ILLA Builder**

Now that you have a free TiDB Cluster, it’s time to connect it to the [**ILLA Builder**](https://github.com/illacloud/illa-builder).

1. Create a free account and sign in on the ILLA Builder welcome page.
    
2. Create a new application.
    
3. Connect to TiDB as an ILLA resource. Do one of the following:
    
    * If you already have a PingCAP resource in ILLA Builder, you can click + **New** to select it.
        
    * If you don’t have a TiDB resource in the ILLA builder, you need to click + **New Resource** to set up a new connection.
        

Test the new connection. If the connection is successful, save the connection as a new resource.

1. Use actions to execute basic create, read, update, and delete (CRUD) operations in the TiDB database. Actions bridge data and ILLA components and are essential to building an application.
    
    a. Choose a TiDB resource and create actions.
    
    b. In the input box, enter the SQL statement, save it as a new action
    
    c. Click **Run** to execute the statement.
    
    d. Run a query action to see if the insert action runs successfully.
    

You can create multiple actions and use different components to control their execution

## [**​**](https://www.illacloud.com/blog/building-applications-faster#connect-the-component-to-the-action)**Connect the component to the action**

Components in ILLA Builder are built-in front-end UI libraries such as buttons and input boxes. To connect a component to an action:

1. Under the component inspect panel on the right, select and drag the “text” and “input” components to the canvas in the middle.
    

![Under the component inspect panel on the right, select and drag the “text” and “input” components to the canvas in the middle.](https://cdn.hashnode.com/res/hashnode/image/upload/v1675854116873/f0e5bcb1-23ce-4bc0-9d08-6ca823c18c21.gif align="left")

<center><figcaption>Select & Drag</figcaption></center>

1. Create and save the required actions. You can refer to the component or action data by typing “{{”
    

Here we will create two actions, tidb\_query\_data and tidb\_insert\_data, for later use.

![Query data from the person table](https://cdn.hashnode.com/res/hashnode/image/upload/v1675854199747/8a2561ae-9cd3-402f-8b0a-9a7ac790b56b.jpeg align="left")

<center><figcaption>Query data from the person table</figcaption></center>

![Insert data into the person table](https://cdn.hashnode.com/res/hashnode/image/upload/v1675854203622/e0eb3920-7971-439d-bec2-d3224cd37662.jpeg align="left")

<center><figcaption>Insert data into the person table</figcaption></center>

You have successfully connected the component to the action.

## [**​**](https://www.illacloud.com/blog/building-applications-faster#implement-a-simple-web-application-with-ti-db-cloud)**Implement a simple web application with TiDB Cloud**

Now that we have everything ready let’s build a simple web application with the basic components to add, delete, modify, or query the data from a TiDB table.

## [**​**](https://www.illacloud.com/blog/building-applications-faster#create-and-configure-an-insert-button)**Create and configure an Insert button**

1. Click on the **Insert** button component you just added to enter the **Inspect** panel on the right.
    
2. Under the **Inspect** panel, add an event handler, and configure the event handler as:
    
    * Event: **Click**
        
    * Action: **Trigger query**
        
    * Query: **tidb\_insert\_data**
        

![Insert Button Setup](https://cdn.hashnode.com/res/hashnode/image/upload/v1675854250946/c3d8c007-4c35-431a-9b9b-6505af64b6f9.gif align="left")

<center><figcaption>Insert Button Setup</figcaption></center>

## [**​**](https://www.illacloud.com/blog/building-applications-faster#query-data-from-a-table)**Query data from a table**

1. Click on the **Query new data** button you just created. This displays the **Inspect** panel on the right side of the screen.
    
2. In the **Inspect** panel, add an event handler, and configure it as follows:
    
    * Event: **Click**
        
    * Action: **Trigger query**
        
    * Query: **tidb\_query\_data**
        

![Query data setup](https://cdn.hashnode.com/res/hashnode/image/upload/v1675854269065/fcb33b6b-2317-4b19-876f-e7e8511ec323.gif align="left")

<center><figcaption>Query Data Setup</figcaption></center>

Now you can execute the query action against the specified table in TiDB.

## [**​**](https://www.illacloud.com/blog/building-applications-faster#visualize-the-query-as-a-chart)**Visualize the query as a chart**

1. In the Inspect panel on the right side, specify the dataset of the chart component to {{tidb\_query\_data.data}}.
    
2. Adjust the chart component settings, such as the chart type, location, and size.
    
3. Adjust the dataset settings, such as dataset values and aggregation method. The chart will update as you go.
    

![Data Visualization](https://cdn.hashnode.com/res/hashnode/image/upload/v1675854313042/8f5df38f-9f81-43b5-8a58-410195eb389e.gif align="left")

<center><figcaption>Data Visualization</figcaption></center>

## [**​**](https://www.illacloud.com/blog/building-applications-faster#summary)**Summary**

In this article, we implemented a simple TiDB application that inserts new data, executes queries, and displays the query results as a chart. Integrating TiDB Cloud and ILLA builder can make developing your applications much faster and more efficient.

![Preview the tool](https://cdn.hashnode.com/res/hashnode/image/upload/v1675854322598/fa149078-a651-4206-9c8b-2bda3477e85e.gif align="left")

<center><figcaption>Preview of the tool</figcaption></center>

We believe the key to a successful open-source project is not only to code but also to collaborate through code. You are welcome to join our project. Check [**ILLA’s website**](https://www.illacloud.com/) or join the [**Discord community**](https://discord.com/invite/illacloud) for more information.

> #### ***You can check ILLA’s website here at:*** [***https://illacloud.com***](https://illacloud.com)
> 
> #### ***GitHub page:*** [***https://github.com/illacloud/illa-builder***](https://github.com/illacloud/illa-builder)
> 
> #### ***Join Discord community:*** [***https://discord.com/invite/illacloud***](https://discord.com/invite/illacloud)