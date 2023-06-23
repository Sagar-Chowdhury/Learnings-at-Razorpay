# Weeky Learnings/Progress at Razorpay.

![1685697804242](https://github.com/Sagar-Chowdhury/Learnings-at-Razorpay/assets/76145064/1bbf4e5f-0adf-4cb6-95c7-853d3e7bf01c)

### Week 1 (7th June - 14th June , 2023)
1. Started Learning TypeScript Basics.
2. Gradually moved on to Learning Angular, understanding the basics of the framework.
     - Started following the [course](https://youtu.be/3qBXWUpoPHo)
3. Dived deep into Angular Concepts like
      - Directives
      - Pipes
      - Lifecycle Hook and Component Communication
      - Input/Output Decorators
      - ViewChild
      - HttpClient
           - Sending HTTP requests
           - Receiving response
      - RxJs
           - Understood the concept of Observable and Observer
           - Used common operators like ShareReplay, CatchError, of, from, and others
           - Understood their use via code.
      - Routing
           - Basics of Routing
           - Using Route Modules
           - Wild card, dynamic route
           - Lazy Loading
           - Route Guards
      - Angular Forms
           - Template Driven Forms
              - Communication using ngModel
              - Not Scalable
           - Reactive Forms
              - Used Built-in Validators
                      
  4. These learnings are roughly implemented in [repo.](https://github.com/Sagar-Chowdhury/LearningAngular.git)
  
### Week 2 (14th June - 21th June , 2023)
1. I Got assigned a project.
2. Started working on an Email Client, for which I had to make the front-end.
3. The **Project details** are
     - The app opens on the login page
     - The user may decide to signup, so a proper navigation facility is provided using routing.
     - All appropriate error/failure messages are shown using **Toasts(made using ngx-toast)**
     - On successful login user is redirected to the **inbox page**
     - Session management is achieved using an **Authentication token**, gotten from response headers.
     - **Route guards** ensure the user cannot access the inbox page prior to login.
     - The inbox page has a **mailbox** and a **compose mail** section.
       - Mail attachments are sent to the backend by **base64 encoding**.
       - Mailbox is fetched via API.
     - All styling achieved using **ng-bootstrap**.    
 4. [Project Repo](https://github.com/Sagar-Chowdhury/Email-Client-Frontend.git)              
            
