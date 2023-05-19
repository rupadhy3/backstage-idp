### Introduction to Developer Portals  
#### Overview
Organizations want to improve their software and infrastructure’s discoverability so that their developers’ can benefit from  
accessing and using the organization’s resources. Developer Portals play a central role in enabling automated discoverability  
and providing self-service resources that make autonomy possible at scale.  

#### Discoverability: It Only Works If It’s Automated
Discoverability is defined by how rapidly you can find information about a service, library, tool, team, or repository. In a world where  
dozens—or hundreds—of development teams contribute to several codebases, use tens of development tools, and ship their services daily,  
it is almost impossible to know what you’re looking for in the first place. Given that Cloud native teams wrangle with different stacks and contexts,  
they must come up with a way of communicating with others about what they’re doing and how, as well as learn from other teams. Usually,  
these ways are manual compilations of resources that get pieced together in a document by somebody. The problem is not writing that document but  
keeping it up to date and getting everybody to know it exists.  

Discoverability is hard to achieve unless there’s a unified and reliable way to explore what is available in the organization.  
Providing automated Discoverability has become a significant enabler for improved collaboration at the organizations investing in developing an Inner Source culture.  

#### What Is a Developer Portal?
A Developer Portal is a go-to place for developers when they need to learn about their ecosystem and contribute to it.  
it allows teams to keep working independently, choosing their preferred tools, and deploying daily, but exposes their work so everyone can explore and benefit  
from their microservices, APIs, libraries, websites, pipelines, and algorithms. A Developer Portal serves three purposes: helps developers navigate their ecosystem,  
empowers engineers with self-service capabilities, and provides leaders and teams with insight into the tech’s health and maturity.  

Discoverability in a Developer Portal is automated and centralized into a software catalog. The Developer Portal aggregates information about each component,  
including which team is responsible for it, documentation, availability, deployments, Snyk issues, PagerDuty incidents, and any other information that might be useful to your team.  

Indeed, an often sought-after feature of Developer Portals is their ability to track ownership and interdependencies across services. Each software component  
has a team or individual contributor who owns it and is responsible for it. Additionally, the software catalog graphs the dependencies between the components.  

### Backstage
#### Backstage’s Philosophy
Backstage’s vision is to create the best Developer Experience possible. At the same time it is not intended to be a single source of truth,  
but an aggregator. Backstage doesn’t seek to replace your existing CI/CD manager or LDAP directory, nor to re-implement their UIs. Instead,  
Backstage processes information about your services from different sources and puts them together, so it’s easier for developers to navigate them.  
For Backstage to be effective, it requires every software component to be owned by a single team, who will be responsible for keeping its information up to date.  
And we’ve naturally arrived at the other Backstage pillar: ownership.

#### Backstage Is a Framework
Backstage is not a finished product that you can install and use. Rather, Backstage is a collection of tools and libraries that can be used to  
create your own Developer Portal. Backstage’s core is composed of around 25 packages, which include a CLI, utility tools, API definitions, themes,  
and helpers. But what really makes up Backstage are the more than 150 open source plugin packages available, which include the framework’s main features.  
You can pick and choose what you need and extend its functionality by creating new plugins too.  

But don’t worry, you don’t have to learn what all those packages are to get started. Backstage provides you with a starting point through their CLI,  
and from there, you can add or remove plugins as you please.  

#### Your Backstage Instance
In a nutshell, your Backstage instance is a Node/React app built using Backstage’s core libraries on top of which you install community and private plugins.  
Backstage uses a three-layers model to explain how a Developer Portal is built using its framework.  
```mermaid
graph LR
  Plugin --> App
  Plugin --> App
  Plugin --> App
  Plugin --> App
  App --> Backstage core
```


