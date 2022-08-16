---
page_type: sample
languages:
- csharp
products:
- azure
description: "Azure Managed Instance for Apache Cassandra is a 1st party hosting service for open-source Apache Cassandra clusters in Azure"
urlFragment: azure-cassandra-mi-dotnet-core-getting-started
---

# Developing a .NET Core app with Azure Managed Instance for Apache Cassandra
Azure Managed Instance for Apache Cassandra provides automated deployment and scaling operations for managed open-source Apache Cassandra datacenters. It accelerates hybrid scenarios and reduces ongoing maintenance.

This quick start demonstrates how to connect to a Cassandra Managed instance cluster. You'll then build a user profile console app, output as shown in the following image, with sample data.

## Pre-Requisites

Before you can run this sample, you must have the following pre-requisites:

* An Azure Managed Instance for Apache Cassandra cluster. Check out our Quickstart guide [here](https://docs.microsoft.com/azure/managed-instance-apache-cassandra/create-cluster-portal).
* Networking access from this application to your Azure Managed Instance for Apache Cassandra cluster (the service only deploys private IP addresses injected into a Virtual network).
* Code editing: [Microsoft Visual Studio](https://www.visualstudio.com) or [Microsoft Visual Studio Code](https://code.visualstudio.com/) (or another editor capable of editing C# files)
* The [.NET Core SDK](https://dotnet.microsoft.com/download/) - this sample uses .NET Core 3.1. Download and install the SDK for your platform.
* [Git client](http://git-scm.com/).

## Running this sample

1. Clone this repository using `git clone https://github.com/Azure-Samples/azure-cassandra-mi-dotnet-core-getting-started.git`

2. If you're using Visual Studio, open the CassandraQuickStartSample.sln solution. If you're using Visual Studio (VS) Code, open the folder containing the CassandraQuickStartSample.sln solution file in VS Code. Otherwise, use your preferred text or code editor.

3. Edit CassandraQuickStart/Program.cs. Substitute values for your cluster username, password, and contact points for the "&lt;PROVIDE&gt;" placeholders at the top of the class definition. Note: you will need access to the private IP addresses

4. If you're using Visual Studio: you can either install the Cassandra .NET driver using the Package Manager Console window, using the following command, or simply right-click the project node and select "Rebuild", which will restore missing Nuget packages including the Cassandra .NET driver.
  
```bash
PM> Install-Package CassandraCSharpDriver
```

5. If you're using VS Code: under the "Debug" menu, you can use "Start Debugging" (F5) or "Run without Debugging" (Ctrl-F5) to restore, build, and run the application.

6. Otherwise you can use the dotnet command line. At a prompt, navigate to the /CassandraQuickStart folder (this folder contains the CassandraQuickStart.csproj file) and type the following command.

```bash
dotnet run
```

You should see output similar to the following in your console or prompt:

![User Data](/img.PNG?raw=true "user data")

## About the code

The code included in this sample is intended to get you quickly started with a C# application using Cassandra C# driver that connects to Azure Managed Instance for Apache Cassandra.

Note that the CassandraCSharpDriver package used in this QuickStart is compatible with recent versions of .NET Framework and .NET Standard also. For details, see the package's Nuget page or project repository.

## More information

- [Azure Managed Instance for Apache Cassandra](https://docs.microsoft.com/azure/managed-instance-apache-cassandra/)
