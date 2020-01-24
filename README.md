# Ionic Interview Questions and Answers

Arguably, Ionic is one of the most popular frameworks available. According to the stats, there are 5M Ionic devs in over 200 countries worldwide. Over 75 percent of them build apps for commercial use. Diesel and McDonald’s built their apps with Ionic.

> You could also find all the answers here 👉 https://www.fullstack.cafe/Ionic.

<p align="center">
  <a href="https://www.fullstack.cafe">
  <img src="https://user-images.githubusercontent.com/13550565/73042889-e7533900-3e9d-11ea-94f2-b4a9e87cc018.png">
  </a>
</p>

## Q1: What is Ionic Framework? ⭐

**Answer:**

**Ionic Framework** is an open source UI toolkit for building performant, high-quality mobile and desktop apps using web technologies (HTML, CSS, and JavaScript). Ionic Framework is focused on the frontend user experience, or UI interaction of an app (controls, interactions, gestures, animations). Currently, Ionic Framework has official integrations with Angular and React, and support for Vue is in development.

🔗 **Source:** [ionicframework.com](https://ionicframework.com/docs/intro)


## Q2: What is hybrid app development? ⭐⭐

**Answer:**

**Hybrid apps** are developed using web technologies like HTML, CSS and Javascript, and then wrapped in a native application using platforms like Cordova. The apps are shown in its own embedded browser, like UIWebView in iOS and WebView in Android (not Safari or Chrome). This allows you to use any web-native framework for mobile app development.

🔗 **Source:** [netguru.com](https://www.netguru.com/blog/why-you-should-migrate-your-app-from-ionic-cordova-or-phonegap-to-react-native)


## Q3: How do you pass data from one view to another in Ionic applications? ⭐⭐

**Answer:**

Ionic v.1 uses AngularJS and UI-router. It means you can use Angular services or UI-router’s state `resolve` to pass data from one view to another. Since Angular services are singletons, data stored in services can be accessed across other Angular controllers.

As mentioned, UI-router provides a `resolve` configuration. For example:
```js
$stateProvider
  .state('todos', {
    url: '/todos',
    controller: 'TodosCtrl',
    templateUrl: 'todos.html',
    resolve: {
      todos: function(TodosService) {
        return TodosService.getTodos()
      }
    }
  })
```

One advantage of `resolve` over stateful services is better testing: as `resolve` injects dependencies in the controller, it is easy to test them.

When using Ionic v.4 you have 3 options:
1. Using Query Params (bad)
2. Service and Resolve Function (legit)
3. Using Router Extras State (new since Angular 7.2)

```js
 openDetailsWithState() {
    let navigationExtras: NavigationExtras = {
      state: {
        user: this.user
      }
    };
    this.router.navigate(['details'], navigationExtras);
  }
```

🔗 **Source:** [toptal.com](https://www.toptal.com/ionic/interview-questions)


## Q4: How can you test Ionic applications? ⭐⭐

**Answer:**

Ionic v.1 applications are built using AngularJS. Angular has a rich set of test libraries and frameworks such as Jasmine and Karma test runner. These frameworks can be used to write unit tests for Ionic applications. Also, `ionic-CLI` provides `live reload` feature so the application can be tested in the browser. For example, the `ionic serve` command can be used to load the application in any browser. Thus, we can use Chrome Developer Tools or Mozilla Firefox with Firebug to debug and inspect Ionic applications.

🔗 **Source:** [toptal.com](https://www.toptal.com/ionic/interview-questions)


## Q5: Can we work with Ionic > 1 and AngularJS? ⭐⭐

**Answer:**

Unfortunately, **no**. Ionic (1) at a very high-level is essentially just a wrapper & directive/component library for AngularJS (1). In that same regard, Ionic 2 is built in the same way, utilizing all the benefits of Angular 2+.

Ionic 2 breaks away from being tied to the DOM in the browser, by using angular 2 which is the reason for the massive change between ionic 1.x and ionic 2.x. ( Angular 2.x architecture is not tied down to the DOM unlike the Angular 1.x ).

🔗 **Source:** [toptal.com](https://www.toptal.com/ionic/interview-questions)


## Q6: What is the difference between Cordova and Ionic? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Ionic)**


## Q7: What are some possible security issues with Ionic apps? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Ionic)**


## Q8: What are the most prominent advantages and disadvantages of building applications using the Ionic framework? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Ionic)**


## Q9: What is the difference between PhoneGap, Cordova, and Ionic? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Ionic)**


## Q10: How do you persist data between application launches using Ionic? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Ionic)**


## Q11: What is the advantage of caching the views in Ionic apps? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Ionic)**


## Q12: How can you detect a platform (Android or iOS) at runtime in Ionic application? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Ionic)**


## Q13: How can you access mobile phone native functionality in Ionic applications, for example the camera? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Ionic)**


## Q14: What’s the difference between “ionic build” and “ionic prepare”? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Ionic)**


## Q15: How many Types of Storage Available in Ionic Framework? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Ionic)**


## Q16: How to use observables in the Ionic framework? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Ionic)**


## Q17: What is Ionic Native? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Ionic)**


## Q18: What is Capacitor? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Ionic)**


## Q19: How would you compare Ionic vs Flutter? When would you choose one? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Ionic)**


## Q20:  What does it mean that Ionic became framework-agnostic? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Ionic)**


## Q21: How can you render a 5000 item list in Ionic, without affecting scroll performance? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Ionic)**


## Q22: How is the Ionic Framework v4 different from v3? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Ionic)**


## Q23: What are the new features in Ionic 4? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Ionic)**


## Q24: If more than one component is trying to make an HTTP call to same URL, then how can you restrict making 2 network calls? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Ionic)**


## Q25: What is the difference between Capacitor and Cordova? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Ionic)**


## Q26: What are some security measures should be made for Ionic app? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Ionic)**


## Q27: Performance of Ionic application is bad on older Android devices. Why is this, and what can be done to improve it? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Ionic)**


## Q28: What AOT and JIT and which is used by Ionic? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Ionic)**


## Q29: What Are The Ionic Lifecycle Events? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Ionic)**





