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


# React

- DUMP COMPONENT : Dumb components are also called ‘presentational’ components because their only responsibility is to present something to the DOM

example : 

`
const Footer = (props) => {
  return(
  <div>
    <ul>
      <li>Footer Information</li>
    </ul>
  </div>
  )
}
`

Smart Components : Smart components (or container components) on the other hand have a different responsibility
Because they have the burden of being smart, they are the ones that keep track of state and care about how the app works.

`
class App extends Component {
  constructor(props){
    super(props);
    this.state = {pictures : []};
  }
}
`


- using controlled components to implement forms.
- In a controlled component, form data is handled by a React component
- The alternative is uncontrolled components, where form data is handled by the DOM itself.



– *Container* vs *Presentational components*
– *Smart* vs *Dumb compone*

- That means the stateful components are keeping track of changing data
- stateless components print out what is given to them via props, or they always render the same thing


Examples of stateless components being reusable



Can stateful components be reusable?


## Class Component
A class component must include the extends React.Component statement. This statement creates an inheritance to React.Component, and gives your component access to React.Component's functions.

The component also requires a render() method, this method returns HTML.

`
class Car extends React.Component {
  render() {
    return <h2>Hi, I am a Car!</h2>;
  }
}
`

## Function component

- A Function component also returns HTML, and behaves much the same way as a Class component, but Function components can be written using much less code, are easier to understand, and will be preferred

`
function Car() {
  return <h2>Hi, I am a Car!</h2>;
}
`

- Certainly, stateful components can be reused.


# what is HOC?

- A higher-order component (HOC) is an advanced technique in React for reusing component logic. HOCs are not part of the React API, per se. They are a pattern that emerges from React’s compositional nature.
- A higher-order component is a function that takes a component and returns a new component.




# .NET

oops
-   class scope  - internal  
internal and public

encapsulation - hiding the data
abstration- showing the relevant data 

interface - interface has only signature of class and it has no implementation
            all class drive 
			inheritance - multiple inheritance support
			constractor  - no constractor
			static - no static member , all member are public
			
abstract - abstract class can contain with body and without body.
           inheritance - multiple inheritance not support , only one class inheritance
		   constractor - default constractor
		   static - static memeber, member are public, private, internal
		 

		
		
using System;  
interface A  
{  
    void Hello();  
}  
interface B  
{  
    void Hello();  
}  
class Test : A, B  
{  
    void A.Hello()  
    {  
        Console.WriteLine("Hello to all-A");  
    }  
    void B.Hello()  
    {  
        Console.WriteLine("Hello to all-B");  
    }  
}  
public class interfacetest  
{  
    public static void Main()  
    {  
        A Obj1 = new Test();  
        Obj1.Hello();  
        B Obj2 = new Test();  
        Obj2.Hello();  
    }  
}		
		

base keyword is used to access members of the base class from within a derived class 
       base.calculate
	   
	   
# SQL

## delete duplicate record

delete from dbo.Emp where EmpID not in(SELECT max(EmpID) as id     
  FROM [Employee].[dbo].[Emp]
  group by [name])
  
  
delete from dbo.Emp where EmpID not in(SELECT min(EmpID) as id     
  FROM [Employee].[dbo].[Emp]
  group by [name])  
  
  
  Get Highest 3 record of employee
  
  select top 1 t.salary from 
(SELECT  top 3 [salary]
  FROM [Employee].[dbo].[Emp]
  order by salary desc
  ) as t order by t.salary 


	   
	   



