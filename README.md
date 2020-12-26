1. In Redux, we store our application state inside a single JavaScript
   called "the store". This object is the single source of truth for our
   application state, and is accessible by all parts of the UI.
2. We cannot directly modify or mutate the store. Because Redux is built
   on top of functional programming principles.I functional programming,
   we do not mutate state.
3. As a result, we cannot write code like:
   store.currentUser = { name : "cici" }
   because store is an immutable object.
4. To update store, we should create a function that takes the store
   as an argument and returns the updated store.

   function reducer(store, action){
   // return updated store, 方法一： create a copy of the store,
   const updated = { ...store };
   updated.products = ???
   //方法二：use libraries like immer/ immutablJS,但是麻烦
   }

5. reducer is a function that takes the current instance of the
   store and returns the updated store. You can think it as an
   eventhandler without object mutation.

6.
