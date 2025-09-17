# Azure Hosting Cost Estimate Report

**Project:** Cloud Hosting for *Helproo*  
**Website:** [https://helproo.com](https://helproo.com)  
**Prepared for:** Ibiso  
**Prepared by:** Itaobong  
**Date:** September 2025 

## 1. Introduction

This report provides a clear and concise estimate of the projected cloud infrastructure costs for hosting **Helproo** on Microsoft Azure. It covers three operational scenarios with their expected costs:

1. **Low Case** – Pre-launch configuration for development, testing, and internal demos.  
2. **Base Case** – Live environment with stable production workloads.  
3. **High Case** – Future growth stage with global scaling, redundancy, and high user demand.

These estimates support budget planning, investor communication, and operational readiness.

## 2. Infrastructure Overview

| **Layer**      | **Azure Services** |
|----------------|--------------------|
| **Frontend**   | Azure Web App (Public site), Azure Web App (Super Admin Dashboard), Azure Front Door *(Base and High Case only)* |
| **Backend**    | Azure Web App for Containers (API services), Azure Functions (background jobs), Azure Container Registry (ACR) |
| **Database**   | Azure Database for PostgreSQL Flexible Server |
| **Supporting Services** | Azure Monitor, Application Insights, backups, SSL certificates |

> **Region:** Australia East (Sydney)  
> **Currency:** Australian Dollar (AUD)


## 3. Monthly Cost Estimate

| **Service**                  | **Low Case (Pre-Launch)** <br>*Lean Setup* | **Base Case (Go-Live)** <br>*Stable Production* | **High Case (Growth)** <br>*Global Scale* |
|------------------------------|--------------------------------------------|-----------------------------------------------|------------------------------------------|
| Azure Front Door             | —                                          | $600                                         | $2,100 |
| Web App for Containers (Backend APIs) | $120                                    | $500                                         | $4,200 |
| Azure Web App (Frontend)     | $80                                       | $450                                         | $1,350 |
| Azure Web App (Super Admin Dashboard) | $50                                       | $270                                         | $750 |
| Azure Functions (Background Jobs) | $40                                       | $270                                         | $1,275 |
| PostgreSQL Database (Flexible Server) | $150                                    | $1,200                                       | $5,700 |
| Monitoring & Backups (Logs, SSL, storage) | $50                                 | $525                                         | $2,400 |
| **Total (AUD)**              | **$490**                                   | **$3,815**                                   | **$17,775** |


## 4. Annualised Costs

| **Scenario**      | **Annual Cost (AUD)** |
|-------------------|------------------------|
| **Low Case (Pre-Launch)** | **$5,880** |
| **Base Case (Go-Live)**   | **$45,780** |
| **High Case (Growth)**    | **$213,300** |


## 5. Visual Cost Growth

```mermaid
graph TD
A[Low Case: $490/mo] --> B[Base Case: $3,815/mo]
B --> C[High Case: $17,775/mo]
````

## 6. Cost Drivers

| **Cost Driver**             | **Impact**                                                                             |
| --------------------------- | -------------------------------------------------------------------------------------- |
| **Traffic & Data Transfer** | Increased user traffic raises Azure Front Door and outbound bandwidth costs.           |
| **Backend Scaling**         | More API requests and concurrent sessions require additional container instances.      |
| **Database Sizing**         | Higher vCores, RAM, and geo-redundant backups significantly increase PostgreSQL costs. |
| **Background Processing**   | Azure Functions costs scale with transaction volume and execution time.                |
| **Security & Monitoring**   | Enhanced logging and advanced monitoring add overhead, especially at scale.            |


## 7. Scenario Insights

| **Scenario**  | **Focus Area**                                      | **Operational Strategy**                                                                  |
| ------------- | --------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| **Low Case**  | Pre-launch development, testing, and internal demos | Minimal infrastructure with basic database, no global routing, limited monitoring.        |
| **Base Case** | Stable production environment post-launch           | Add Azure Front Door, redundancy, moderate auto-scaling, daily backups, standard logging. |
| **High Case** | Growth with high traffic and global presence        | Geo-redundancy, high-performance PostgreSQL, WAF-enabled Front Door, expanded monitoring. |


## 8. Summary Table

| **Metric**             | **Low Case** | **Base Case** | **High Case** |
| ---------------------- | ------------ | ------------- | ------------- |
| **Monthly Cost (AUD)** | \$490        | \$3,815       | \$17,775      |
| **Annual Cost (AUD)**  | \$5,880      | \$45,780      | \$213,300     |


## 9. Our Strategy 

1. **We Started Lean by:**

   * Deploying Low Case infrastructure for internal testing and validation before launch.
   * Keeping early costs minimal at approximately **\$490 per month**.

2. **Planning for Launch:**

   * Budgeting **\$3,800 to \$4,000 per month** for stable production once Helproo goes live.
   * Added redundancy and improved monitoring at this stage.

3. **Preparing for Scaling:**

   * Allocating contingency for growth to **\$15,000 - \$18,000 per month** as traffic and global reach expand.
   * Including advanced features like geo-redundancy and WAF protection.

4. **Plan for Continuous Optimisation:**

   * Will use Azure Advisor for cost recommendations.
   * Implement caching and CDN optimisations to reduce data transfer charges.
   * Regularly review scaling rules to prevent idle resources.


## 10. Conclusion

This cost projection provides a roadmap for managing **Helproo**’s infrastructure spend as the platform grows. We are starting lean, scaling strategically at launch, and preparing for high-demand growth, so that we can balance performance, reliability, and cost-effectiveness while maintaining transparency for stakeholders.

| **Phase**                 | **Monthly Cost (AUD)** | **Annual Cost (AUD)** |
| ------------------------- | ---------------------- | --------------------- |
| **Low Case** (Pre-Launch) | \$490                  | \$5,880               |
| **Base Case** (Go-Live)   | \$3,815                | \$45,780              |
| **High Case** (Growth)    | \$17,775               | \$213,300             |
