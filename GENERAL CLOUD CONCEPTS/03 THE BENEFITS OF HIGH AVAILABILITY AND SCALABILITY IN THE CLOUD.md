When building or deploying a cloud application, two of the biggest considerations are uptime (or availability) and the ability to handle demand (or scale).

---

## High availability

When you’re deploying an application, a service, or any IT resources, it’s important the resources are available when needed. High availability focuses on ensuring maximum availability, regardless of disruptions or events that may occur.

When you’re architecting your solution, you’ll need to account for service availability guarantees. These guarantees are part of the service-level agreements (SLAs).

Absolutely — let’s break down **SLAs** in cloud computing, and then I’ll explain the typical percentage guarantees and why even small differences matter.


### What is an SLA?

**SLA** stands for **Service Level Agreement**. It’s a formal contract between a cloud service provider (like AWS, Azure, Google Cloud) and a customer. It defines:
- **What level of service is guaranteed** — typically things like uptime/availability, response time, support response, performance, etc.
- **How service is measured** — for example, “99.9% uptime per month”.
- **Penalties or credits** — what happens if the provider fails to meet the guarantee (e.g., you get a partial refund or credit).

### Common SLA metrics

The main one is **availability** — how much time the service must be operational during a given period (usually a month).
For example:
- **99% uptime**
- **99.9% uptime** (often called “three nines”)
- **99.99% uptime** (“four nines”)
- **99.999% uptime** (“five nines” — very rare and expensive)


### What do the percentages actually mean?

Here’s how downtime works out per month:

|SLA %|Max downtime per month|
|---|---|
|99%|~7.3 hours|
|99.9%|~43.8 minutes|
|99.99%|~4.38 minutes|
|99.999%|~26 seconds|

So the difference between 99.9% and 99.99% is about **39 extra minutes of uptime** per month — which can be critical for services that need to run 24/7, like financial systems or medical apps.


### Why small % differences matter

- **Revenue loss**: For e-commerce, minutes of downtime can cost thousands or millions in lost sales.
- **Reputation**: Frequent outages hurt customer trust.
- **Regulatory or safety impact**: Some sectors like healthcare, banking, or airlines simply can’t afford significant downtime.


### Things to watch out for

- **Exclusions**: SLAs often exclude planned maintenance or downtime due to things outside the provider’s control.
- **Compensation**: SLA breaches usually result in small credits, not big payouts.
- **Shared responsibility**: The SLA covers only what the provider manages — if your own app or config fails, that’s on you.


An SLA is both a guarantee and a risk management tool — but the percentage guarantees must align with how critical uptime is for your business.

---

## Scalability

Another major benefit of cloud computing is the scalability of cloud resources. ==Scalability refers to the ability to adjust resources to meet demand.== If you suddenly experience peak traffic and your systems are overwhelmed, the ability to scale means you can add more resources to better handle the increased demand.

The other benefit of scalability is that you aren't overpaying for services. Because the cloud is a consumption-based model, you only pay for what you use. If demand drops off, you can reduce your resources and thereby reduce your costs.

Scaling generally comes in two varieties: vertical and horizontal. Vertical scaling is focused on increasing or decreasing the capabilities of resources. Horizontal scaling is adding or subtracting the number of resources.

### Vertical scaling

With vertical scaling, if you were developing an app and you needed more processing power, you could vertically scale up to add more CPUs or RAM to the virtual machine. Conversely, if you realized you had over-specified the needs, you could vertically scale down by lowering the CPU or RAM specifications.

### Horizontal scaling

With horizontal scaling, if you suddenly experienced a steep jump in demand, your deployed resources could be scaled out (either automatically or manually). For example, you could add additional virtual machines or containers, scaling out. In the same manner, if there was a significant drop in demand, deployed resources could be scaled in (either automatically or manually), scaling in.


---

## References

https://learn.microsoft.com/en-us/training/modules/describe-benefits-use-cloud-services/