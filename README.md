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
 4. [ Project Repo ](https://github.com/Sagar-Chowdhury/Email-Client-Frontend.git)              
 ### Week 3 (21st June - 28th June , 2023) 
 1. Successfully cloned Rewads-hub-portal on my local mac.
 2. Vikalp guided me in **migrating the Angular version from v8 - v12**
 3. Started exploring the agent portal to gain insights about **missing features and bugs**.
 4. Through the weekend got insights into how **bootstrap** works, and also jotted down some issues in the agent portal.
 5. Migrated to **Angular Version 14**.
 
  ### Week 4 (28th June - 5th July , 2023)
   1. Completed [**Namaste Javascript**](https://youtube.com/playlist?list=PLlasXeu85E9cQ32gLCvAvr9vNaUccPVNP) playlist.
      - Got an **extensive** idea of the following, with coding illustrations
        - Javascript execution environment, and how JS is executed
        - **Hoisting**
        - **var,let,const** in JS and their scope, Block Scope , **Temporal Dead Zone** 
        - **Scope and Lexical Environment** in JS and how it works
        - Undefined v/s Not defined in JS
        - **Closures**
        - Functions as **First Class Citizens**
        - **Web APIS** , and accessing them via global **Window object**
        - **Event Loops**, **CallBack Queues** and **MicroTask queues** in JS.
        - JS Engine inside browsers , also learned how **Googles V8** engine works on a high level
        - **Asynchronous** tasks
          - Using **Callbacks**
            - Understood its Shortcomings and also how Inversion Of Control Works.
          - Using **Promises**
            - Learned its usage and advantages of being immutable
  2. Changes that made it to ***production***.
     - Branch, where I migrated from **Angular v12-v14, merged**.
     - **Drop-down lists and popovers** were not fully functional on the homepage of both mobile and desktop versions, so fixed that.
     - Earlier **concierge client list** was hard coded, now is being fetched from an API.
     - Earlier there was no option to choose **client projects**, now there are fetched projects from an API.
     - Made necessary UI changes to accommodate the above two changes.
     - Added the newly fetched project-id to headers, of all further HTTP requests via **interceptors**.
  ###  Week 5 (5th July - 12th July , 2023)
   1. Started Work on the **Booking History Page**.
   2. Fixed Some **query endpoint parameters** being sent, to fetch filtered lists by various categories.
   3. Added names to some earlier anonymous list columns, and did necessary changes to ui.
   4. Added **Created** filter in the status filter of booking history.
   5. **Ng-Bootstrap components** were not functioning properly, to fix it
      - Migrated to **Bootstrap 5**
      - Made necessary imports 
   6. Started work on ***Displaying Payments and Refunds data*** , along with their transactions via a **Modal and Accordions**.
      - Added a new column in booking history.
      - On click, triggers a modal, showing payment details and their transactions in a table.
 ###  Week 6 (12th July - 19th July , 2023)
   1. Continued work on displaying **payments and refund data** along with their transactions.
   2. Made modifications to the modal UI, for a better UX using **cards, shadows, and proper Accordions**.
   3. So the design finalized was
      - Payments
      - Transaction Table
      - Refunds Drop-down accordion(**fetches data only when opened**)
      - Everything was encapsulated in a card for a particular payment (note: there can be multiple payments for a particular booking id)
      - All this is shown inside a **modal** which is triggered by a button click in booking history (each modal was **labeled by a unique booking id**)
   4. Designed a local caching mechanism where the refunds data are **cached corresponding to the payment-id ,until modal is dismissed** as it prevents **multiple api calls** is refunds accordion is closed and opened.
   5. Worked on some other minor issues
      - Changed the **z-index** of toast to display over modal( error toasts mostly)
      - Added some margins to improve UI in some places.
      - Tested and took precautions for API fetch failure for payments and refunds data.
      - Add **error toasts** for both client and project fetching during login.
   6. Participated in **code reviews** with my buddy and finally my branch got **merged**, deploying changes to the sandbox and to production eventually.
   7. Glimpse of the UI 
    ![image](https://github.com/Sagar-Chowdhury/Learnings-at-Razorpay/assets/76145064/47e30cdf-0654-4a99-a9ce-3b9b3e2a7bd1)
 ###  Week 7 (19th July - 26th July , 2023)
   1. Began Work on **Send payment link** feature.
   2. Integrated the **initiate refund** functionality by adding a column to the booking history.
      - Added necessary checks to ensure that the refund amount is valid.
      - Rewrote the api call, using **pipes and catchError**.
      - Added **success and failure toasts** to the api call, also ensured modal dismisses on completion.
   3. Designed the **email template** , to be sent to the user,on the transaction completion.
   4. Began Work on implementing **Pagination** in the booking history.
 ###  Week 8 (26th July - 2nd August, 2023)
   1. Finalized work on the **Pagination feature**, and tested all use-case scenarios.
      - Added **boundary links** (for quick navigation to the first and last page)
      - Added visible page rotation in about 8-page radius from the current, for avoiding a large pages list.
   2. Raised PR and got approved by my mentor, for the above change.
   3. Integrated functionality for **fetching refund details via booking-id**, so as to make it displayable in the initiate refund modal.
      - Added a drop-down accordion for the same in the initiate refund modal.
   4. The booking history table was getting **overwhelmed with lot of columns**(i.e. visible parameters w.r.t. a booking)
      - To address this replaced **three date columns by a single column** with drop-down to see any date parameter as wish(i.e.Confirmed At, Created At and Updated At)
      - Some sections were large so added a **functionality to toggle their visibility** as per wish.
      
