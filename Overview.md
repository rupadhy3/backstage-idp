## What Spotify Backstage is:
### IDP:
An Internal Developer Portal is a portal that helps developers make sense of their engineering ecosystem.  
Spotify Backstage provides a centralized place to look up information about their tooling, services and architecture.  
It allows developers to understand what other teams are working on and how their environments are running.  
It can be thought of as a single pane of glass, or a hub for software development.  

A service catalog, or software catalog, is a list of all of the internal software assets available inside a company.  
In Backstage, this can include services, systems, resources such as S3 buckets, and other concepts.  
It also includes groups of humans, who can own software in the Catalog.  
The Catalog allows users to “look up” internal systems to find information about them.  

On a technical level, Spotify Backstage is a collection of TypeScript libraries which can be combined together  
to create a Developer Portal. The Developer Portal is typically organized and centered around a service catalog.

### Problems tackled by Spotify Backstage:
Backstage helps to solve a number of different problems. They fall broadly into two categories: discoverability and governance.  
#### Discoverability --> Backstage solves this problem by collecting software, tools, teams, people and other assets into one place  
where they can be easily searched and organized.  

#### Opaque software ownership  
The first step towards effective collaboration and InnerSourcing is to be able to easily understand who owns what.  
Backstage addresses this problem by tracking teams and software assets, and making it easy to create a clear linkage between them.  

### The main features of Backstage
Backstage is fundamentally a flexible, plugin based system, which can be modified to suit your use case and the internal  
tools you already love. It’s designed to integrate with existing systems, rather than replacing them.  

#### Software catalog
The software catalog lists all of the software assets in your company, and allows you to associate them with engineering teams and the people on them.  
It supports many different kinds of software asset, including Websites, Services and Libraries. It also supports infrastructure assets called Resources.  

Each entity in the software catalog is described by a specification, usually written in YAML. Here is an example of a basic Service, as represented in Backstage.  
```
apiVersion: backstage.io/v1alpha1
kind: Component
metadata:
  name: sample-service
  title: Sample Service
  description: A service for testing Backstage functionality.
  annotations:
    github.com/project-slug: RoadieHQ/sample-service
spec:
  type: service
  owner: sre-team
  lifecycle: experimental
```

#### Plugins
Most of Backstage’s functionality, including the software catalog, is delivered in the form of plugins. The plugins allow you to mix and match the tools  
which make sense in your particular situation.  
Plugins typically export UI components which you can code into your Backstage application so others at your company can use them. Plugins can be written in JavaScript or TypeScript.  

The plugin marketplace is full of open-source plugins you can easily get started with.  

#### TechDocs
TechDocs provides a way to host technical documentation inside Backstage. Backstage uses a docs-like-code approach where documentation is written in  
the form of Markdown and stored alongside the code. The markdown files are then transformed into HTML and rendered inside Backstage where they are  
searchable and organized by Software Component.  

#### Software templates
Software templates allow you to encode your organization’s best practices into YAML templates which can be used to scaffold new services.  
Each template will typically do a few things:
    Grab a pre-approved skeleton codebase from a known location.
    Pass some parameters into it to customize it.
    Create a new code repository and place the customized codebase in there.
    Hook the codebase up to tools like Continuous Integration, monitoring and logging.

The software templates speed up service creation while improving production consistency.

#### Kubernetes
The Kubernetes plugin is a core part of Backstage. It connects to your Kubernetes clusters and provides people with an easy way to see  
how software is running in the clusters. It makes it easy to look up running pods, image versions and deployment errors.  


