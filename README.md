# Interview


# Angular

1. What are lifecycle hooks available?
2. Where is use constructor and ngOnChange?
3. Content Projection in Angular ? 
4. What is Dependency injection [(DI)](https://angular.io/guide/architecture-services#dependency-injection-di)  
5. What is the difference between pure and impure pipe?
6. What is the difference between promise and observable?
7. 


# **Node.js**

1. what is object oriented concepts in JavaScript?




# Answer

ngOnInit(): This is called when the component is loaded into the DOM and it occurs only once.

ngOnChanges(): This is called when there is Input property to the component and it is called before ngOnInit() and occurs every time there is a change in the input property. It is not called if there is no input property to the component

ngDoCheck(): occurs every time there is a change detection and immediately after ngOnChanges() and ngOnInit().

ngOnDestroy(): This is called right before the component gets destroyed and occurs only once.

ngAfterViewInit(): This is called once after the component’s view/ child views are loaded and right after ngAfterContentChecked() and occurs only once.

ngAfterViewChecked(): This is called after component’s view/ child views are loaded and called after ngAfterViewInit() and every time after ngDoCheck().

ngAfterContentInit(): This is called once external content is projected into component’s view and right after the first ngDoCheck() and occurs only once.

ngAfterContentChecked(): This is called after external content projected into component’s view and called after ngAfterContentInit() and every subsequent ngDoCheck().




