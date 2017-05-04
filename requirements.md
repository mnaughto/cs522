## Background

The subject of these requirements is an existing web-based GIS application. The application is currently used for collaboration around utility engineering projects and services. In general, the application serves as a central repository of geographic information, and it allows users to create and share content with fine granularity.

It should be noted that specifying the wide range of current functionality is beyond the scope of this document; it is assumed that current functions will be retained. However, this document does provide requirements for changes to existing functionality.

Additionally, there is an administrative area of the application which supports management of data and permissions as well as creation of users and groups. This area is beyond the scope of this project.

## Concepts

Content in the application comes in several forms. The most atomic of these is a _geometry_ (or “object” or “geometry object”). A geometry may be either a point, a line, or a polygon, and represents a physical entity somewhere on the globe. A geometry may have files and attributes associated with it, as well. A layer consists of a set of geometries and defines the possible attributes for its child geometries. A _layer_ may also consist solely of a set of sub-layers. A _service_ consists of a set of related layers. A _layout_ is a saved view of a set of services along with the visibility of those services and layers. For the purposes of this document, a _walkthrough_ can be understood as a set of layouts linked together in sequence.

At present, there are two primary pages for the application. The first, which we can call the _menu page_ or “main page”, consists of a menu of content which users can select to view on the map page. The _map page_ is the page in the application where users spend the majority of their time. It consists of a central “map area” which displays a map view as well several peripheral panes which display loaded layers, search options, selection properties, and visible layers. At the top of the map page is a toolbar.

Lastly, it is important to understand the idea of a _spatial query_. A spatial query is a process by which geometries related to a selected geometry may be discovered. In this application, this involves selecting a set of layers to include in the search (or query), selecting a geometry to query on, and entering any information needed for the query. For instance, a user may select a layer containing poles on which to perform the query, then select an underground pipe to query with, and finally enter a distance from the pipe centerline to search. This spatial query would return all of the poles within the given distance of the pipe centerline.

## Target Audience

The target audience consists of the current users of the application. Around half are young adults who tend to be more tech savvy while the other half are an older crowd (40s and 50s) who are generally not as comfortable with technology. Some of the users primarily work outside as utility locators whereas others primarily work inside as engineers. Around two thirds of users believe they use the application primarily for viewing existing content, almost a third think they use it primarily for authoring content, and a small number use it mostly for presentations.

For our purposes, “presenter users” can be seen as a secondary audience, where the remaining user groups make up the primary audience. Furthermore, there are generally three forms of presentation or large-screen usage of the application. One is largely a walkthrough of functionality, particularly functionality which sets the application apart from other similar applications. Another is the telling of a project story (for sales purposes) using the application. And the last is using the application in project-related meetings.

## Requirements

### User Requirements
- The user must have access to a laptop or desktop on which to access the application
- The user must have a preexisting account on the application
- The user should be familiar with some aspect of civil or utility engineering services
- As a content-viewing user, the user must have familiarity with the content they are viewing or attempting to view
- As a content-viewing user, the user must have permission to view the content they are viewing or attempting to view
- As a content-authoring user, the user must have familiarity with the content they are creating or modifying
- As a content-authoring user, the user must have permission to create or edit the content they are authoring

### Functional Requirements
- Users should be able to access search functionality as soon as they log in
- Users should be able to access layouts, services, and presentations as soon as they log in
- Search should not require separate selections for search type
- Files attached to objects should have the ability to be previewed
- When opening a layout, the map view should restore to a center location and zoom level associated with the layout
- Users should be able to draw multiple geometries without re-enabling the draw operation
- Modifications to geometry objects should save automatically
- When selecting a search result, the map should zoom to the extent of that search result
- There should be a single hierarchical view of data loaded on the map
- It should be possible to query on specific fields of geometries
- It should be possible to obtain a temporary public link to a layout
- It should be possible to secure sensitive information on a public layout link
- It should be possible create a new presentation
- It should be possible to create the individual layouts for inclusion in a presentation
- It should be possible to obtain a public link to a presentation
- Sets of search results should not “disappear”

### Usability Requirements

- Layouts, services, and presentations should be logically organized when displayed
- Navigation should be possible between any layout, service, or presentation and any other layout, service or presentation
- Search capability should be prominent on the map page
- Attribute information for an object or set of objects should be easily accessible
- Attribute information for an object or set of objects should be easily readable
- File download links for objects should be readily available
- The ability to export map data to a file should be readily available
- Layout creation should be readily available
- The ability to activate draw mode should be readily available
- Layers and services should be easier to create
- Spatial search functionality should be more accessible
- Permission settings for content should be easy to understand


### Non-functional Requirements

- The application should be visually appealing on a large screen
- A simple “one-page” help overview should be available
- A more thorough help and support site should be available
- The one-page help overview should be packaged with public layout links
- It should be easy to discover previously-unknown functionality
- It should use metaphors common to the utility and civil engineering field
- The number of required button clicks should be minimized
- Multistep operations should be intuitive
- Multistep operations should allow navigation between steps
- All long-running operations should be cancelable
- The application should be easy for novice users to interact with
- The application should be easy for users who are less technologically inclined to interact with
- The user interface should be consistent – an icon that means one thing should mean the same thing everywhere
- The “operand” of operations should be clear
- Screen space for the map page should be maximized
