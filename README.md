# Skill Garden

Skill Garden Coaches users to enforce "Get Better Mindset" by setting goals, tracking progress towards them and recording them as skills or accomplishments. 

Example: 

Career on information technology can be seen as set of learning challenges. Learning challanges can be modelled as goals and accomplished using tools like self paced courses. When planned activity dates (now = due date of learning task) it might be taken in to past archievements if user confirms it done. Past achievements can be seen as inventory and short and long term plans as career goals. 

Vision:

This could be mobile or web system with broad user base like "everyone in world" or "any linkedin user". System could be linked to HR systems and used to facilitate career planning and skill inventory, but it could be also used individually by single person. 

CV generator with markdown template is possible extension point, which could make such system interesting for broader community.

## Conceptual model

![central ideas](diagrams/skill-metafors.png)

Note: Mental accounts like "heavy rocker" or "work" are defined by user, but there might be set of defaults offered.

## Theory

https://hbr.org/2016/01/what-having-a-growth-mindset-actually-means

## Tools

### Mobile UI & Cloud

- Flutter (= Skia + Dart)
- Aws Amplify https://aws.amazon.com/blogs/mobile/announcing-aws-amplify-flutter-developer-preview/

### mobile paas 

- aws amplify & aws cognito & ..
- example: https://github.com/nikkijuk/aws-image-gallery

### user identity

- Linkedin as identity provider
- auth0 as technology connecting linkedin to apps https://auth0.com/docs/connections/social/linkedin
- aws cognito as cloud service https://aws.amazon.com/premiumsupport/knowledge-center/cognito-linkedin-auth0-social-idp/

### export (is there need for import?)

- users can sync their data with remote sources like own employer
- manual sync or automatic sync
- example: Company X has trust relationship to person Y and provides api to receive synced information (async or sync, everything goes)

### Data

- S3 with blob of json per user is simplest possible storage as data is used by single user and there's no need for ACID properties 
- GraphQl + graph data store could also work well, but might not provide any benefits over json blob
- relational database is not very practical here

### DSL

- Persons skills (inventory) and goals (plan) can be expressed using "Get Better DSL" or "Growth Mindset DSL" or "Skills and Goals DSL"
- Instance of DSL can be saved and shared as JSON (or YAML if human readability is important)
- DSL makes it simple to share information between providers and consumers of different type or make backups or migrate to other service

### Code editing

- Visual Studio Code
- Android Studio

### Diagrams

- Draw.io
- Plant UML
