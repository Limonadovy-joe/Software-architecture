# Software-architecture

## Contents
- [Single page application - SPA](#Single-page-application)


## Single page application

One thing that certainly native mobile application have raised the expectation bar. Other factors that also contribute to the increased expectations include ubiquitous high-speed broadband at home,the office and now on our mobile devices with LTE availability. Users want apps that load and respond quickly. Once loaded they expect snappy responses, smooth transitions and engaging interactions. Many believe that HTML5 does not posses the ability to meet these requirements.

One of the hottest web architecture trends today is Single Page Application or SPA. This architecture eliminates the traditional request-response model the classic web was built upon. Instead it requires only a single page be retrived from the server. Subsequent views are brought in and out of view as needed.
This architecture realies heavily upon AJAX request to pass JSON objects to and from the server to the client to merge with views that present data.

TODO - include img where will be the working procces of SPA, data-binding terms, highlight,format some terms

The benefits of a SPA include much less network activity, faster responses to user interactions, smaller server loads. I also makes it possible to use fancy view transitions, which give the appearance of native application.

### Technical features
- [Client side routing](#Client-side-routing)
- [Markup management](#Markup-management)
- [Data retrieval and Storage](#Data-retrieval-and-Storage)

### Client side routing - route manager
Model-view-controller architecture went more mainstream and with it came the concept of routing. Note that routing itself does not have anything in common with MVC. In ASP.NET you could define routes to trigger controllers that would ultimately generate the desired markup and send it on its way to the client.
A SPA is client-heavy and this responsibility must be moved to the browser.

### Markup management
Traditionally web devs have realied on the server to generate any dynamic markup a page request needs. This generally does not apply for a single page app,
except for the initial  page request. Instead a SPA relies more on creating views in the client as they are needed(on demand).
You can extend these concepts to integrate deferred content loading, offloading and templates to LocalStorage to be retrivied on demand.

### Data retrieval and Storage
You will need a way for the app to display the data and corresponding markup on demand. This means leveraging AJAX, JS templates and in many cases web storage. Data should be retrivied using AJAX call. As modern browsers become more common you can start relying on CORS, which is generally a more secure way to make cross-domain calls. Once data has been retrivied you need a method to merge it with markup and inject it into the DOM. This can be done with a JS template library like Handlebars. Template libs make is possible to merge A JSON object with a template to produce markup combined with content.




