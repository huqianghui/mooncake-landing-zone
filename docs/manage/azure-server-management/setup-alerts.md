---
title: Set up basic alerts
description: Learn how to use Azure server management services to set up alerts and notifications that help keep your IT teams aware of any problems.
author: BrianBlanchard
ms.author: brblanch
ms.date: 05/10/2019
ms.topic: conceptual
ms.service: cloud-adoption-framework
ms.subservice: manage
ms.custom: internal
---

# Set up basic alerts

A key part of managing resources is getting notified when problems occur. Alerts proactively notify you of critical conditions, based on triggers from metrics, logs, or service-health issues. As part of onboarding the Azure server management services, you can set up alerts and notifications that help keep your IT teams aware of any problems.

## Azure Monitor alerts

Azure Monitor offers [alerting](/azure/azure-monitor/alerts/alerts-overview) capabilities to notify you, via email or messaging, when things go wrong. These capabilities are based on a common data-monitoring platform that includes logs and metrics generated by your servers and other resources. By using a common set of tools in Azure Monitor, you can analyze data that's combined from multiple resources and use it to trigger alerts. These triggers can include:

- Metric values.
- Log search queries.
- Activity log events.
- The health of the underlying Azure platform.
- Tests for website availability.

See the [list of Azure Monitor data sources](/azure/azure-monitor/agents/data-sources) for a more detailed description of the sources of monitoring data that this service collects.

For details about manually creating and managing alerts by using the Azure portal, see the [Azure Monitor documentation](/azure/azure-monitor/alerts/alerts-metric).

## Automated deployment of recommended alerts

<!-- docutune:casing "Alert Toolkit" -->

In this guide, we recommend that you create a set of 15 alerts for basic infrastructure monitoring. Find the deployment scripts in the [Alert Toolkit](https://github.com/Microsoft/manageability-toolkits) GitHub repository.

This package creates alerts for:

- Low disk space
- Low available memory
- High CPU use
- Unexpected shutdowns
- Corrupted file systems
- Common hardware failures

The package uses HPE server hardware as an example. Change the settings in the associated configuration file to reflect your OEM hardware. You can also add more performance counters to the configuration file. To deploy the package, run the `New-CoreAlerts.ps1` file.

## Next steps

Learn about operations and security mechanisms that support your ongoing operations.

> [!div class="nextstepaction"]
> [Ongoing management and security](./ongoing-management-overview.md)