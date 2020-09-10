# angular
* create empty application
* clear the html and replace it with `<h1>Title: {{ title }}</h1>`
* show ngIf
* show ngFor with string array
* create a button with onClick
* manage boolean state with onClick, showing that you can hide elements
* move ngFor into ngIf to show nesting
* show them what interface and class is, create simple interface person, add one person to it a and show how to control it in html
* do tasks 1-4
* speak about lifecycles, write code in meantime showing basic ngOnInit and ngOnChanges (use the `add dog` button with console logs to show triggers)
* do task from slides
* create a test component with two inputs and use it in main component
* do task 5
* explain outputs. extend test component with a button that outputs static text
* do task 6
* explain forms and show how to bind, extend test component with a form that has input field that binds to value before exporting, button triggers submit event which emits value. Need `FormsModule`
* expain in main component that you can bind parts of interface to input values
* do task 7
* expain what are observables, create service, show with fake one using `of` and `delay`.
* show what happens if value is not set to empty array
* change fake observable to real one, use service with `private http: HttpClient`, also need `HttpClientModule`
* do task 8
* show how modules work and interact with each other
* show that you need to export components and import module
* show how router works. You do need `<router-outlet>` in main component, create navigation bar and all that thingies.
* show how to get router parameters, query parameters, navigationExtras
* show how to send request using those parameters
* do task 9
* show how to do POST


1. Create an interface called Dog that will have fields (name, age, breed)
2. Create dogs array with at least 3 dogs and print all information of dogs in HTML to look like:
```
name: Sparky, age: 5, breed: 'Labrador'
```
3. Add a table that will print out all the dogs information
4. Add button that adds new dog with all the information. Information is hard-coded
5. Create a dogs component that will take all the dogs as input and print them in table 
6. Create a child component that outputs random number after a button press. Assign that number to parent component and display it in HTML.
7. Create a new interface that has two fields (Cat - name, lives(number)), 
  create new component cat-form,
  create variable of that interface and initialize it,
  create form for both of input fields,
  assign both of variable properties to those input fields using ngModel,
  on form submit send cat value to parent using output. Show cat value in parent component
8. Create interface Todo that has fields (userId: number, id: number, title: string, completed: boolean) 
  Create a new my-view component that will act as a parent component. Call this component from app.component: <app-my-view></app-my-view>
  Create a new component `todo-table` that will display all elements of todo list (Todo[] needs to be input)
  create a service `todo.service.ts` that will call API endpoint `https://jsonplaceholder.typicode.com/todos` with GET,
  subscribe to this service result in my-view component and pass `Todo[]` to `todo-table`
9. Create two interfaces: post (id, title, body) and comment (postId, id, name, email, body)
  create post service that will return all posts
  create comments service that will return all comments of specific post
  create post-list component that will show all the posts (title only).
  post-list component needs to be routed as primary component
  create post component that will show all the info of single post: post id, post title, post body and a list of comments
  post component needs to be routed as path: 'post'. It will use query params to fill other fields
  post-list post can be clicked and will redirect url to post component
  post-list component must pass post information to post component (use query params)
  post component reads query parameters and calls comments service to get required comments (switchMap with observable)
