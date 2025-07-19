## Infosys 1hr:30 min Interview

# Interview Q&A (Short .md Format)

## 1. Introduction

Full-stack UI developer with 12+ years' experience in React, Angular, Node.js, AWS, and UI architecture.

## 2. What backend services did you work on?

Node.js with NestJS, Express.js, GraphQL APIs, AWS Lambda, API Gateway, DynamoDB.

## 3. Which Frontend technologies did you work?

React.js, Angular 16, TypeScript, Redux, RxJS, HTML5, CSS3, Sass, Highcharts, AG Grid.

## 4. Hardcoding in Frontend and Backend? Why?

Avoid it. Makes updates error-prone and unscalable. Prefer configs, enums, or DB-driven values.

## 5. Tables Structure in Backend?

Normalized with clear entities: user, role, permissions. Use foreign keys and mapping tables.

## 6. Delayed screen feedback by client?

Track all screen specs via JIRA/Confluence. Use wireframes, versioning, and document changes.

## 7. UX suggestions for React apps?

Keep components modular, reusable. Minimize load time. Use skeletons/loaders. Align on design tokens.

## 8. How to handle UX?

Collaborate early with UX team. Validate flows with user feedback. Focus on accessibility and performance.

## 9. Low-Level Design (LLD)?

Break down components, APIs, service classes, DB schema, validations, and interface contracts.

## 10. UI Architecture of React App?

Feature-based folder structure, centralized state (Redux/Context), reusable components, code splitting.

## 11. React.js Architecture?

Component-based. Props for data flow. Hooks for state/effects. Virtual DOM for efficient rendering.

## 12. Libraries in React.js?

Redux Toolkit, Axios, React Router, Formik, Yup, Zod, Lodash, React Query, AG Grid.

## 13. UI Components in React?

Button, Input, Modal, Table, Dropdown, Tooltip, Toast, Accordion, Tabs—abstracted and reused.

## 14. Hooks in React?

useState, useEffect, useMemo, useCallback, useRef, useContext, custom hooks.

## 15. Rendering?

React re-renders based on state/prop changes. Use memoization to avoid unnecessary re-renders.

## 16. jQuery to JS Conversion Time?

Depends on project size. Typically a few days to weeks. Focus on event handling and DOM updates.

## 17. JS vs jQuery: Which is faster?

Vanilla JS is faster. jQuery adds overhead but simplifies cross-browser scripting.

## 18. JS vs jQuery?

JS is native, modern, and powerful. jQuery is easier for beginners, but outdated for modern apps.

## 19. Accessing Camera: HTML or JS?

Both. HTML provides `<video>` tag, JavaScript uses `navigator.mediaDevices.getUserMedia()`.

## 20. Unit Test Cases?

Jest, React Testing Library for frontend. Write tests for components, reducers, and utility functions.

## 21. AWS Cloud?

Worked with S3, Lambda, API Gateway, DynamoDB, CloudWatch, IAM, Cognito.

## 22. CI/CD Cloud?

Used GitHub Actions, Bitbucket Pipelines, and AWS CodePipeline for automated build/test/deploy.

## 23. Why no problem with private variables?

They enforce encapsulation. Outside access is restricted to getter/setter only.

## 24. Private Variable Drawback?

Can’t access directly—need accessor methods. Can slow development if overused.

## 25. Public Method?

Used to safely expose internal state or trigger actions—maintains abstraction.

## 26. How to achieve encapsulation?

Make variables private. Provide public methods to access/update them.

## 27. How we achieve security?

Use encapsulation, authentication, authorization, validation, HTTPS, and secure APIs.

## 28. Setter Method for Bank Balance?

```java
public void setBalance(double balance) {
  this.balance = balance;
}
```

## 29. Purpose of Encapsulation

Encapsulation hides internal state and logic, exposing only what’s necessary through methods. It protects data integrity and makes the codebase easier to maintain.

## 30. Model Class in Setter/Getter

A model class defines private fields and provides public getters/setters to access or modify them. This enforces controlled access to data.

## 31. Model in Java

A model is a simple Java class representing a data entity (e.g., User, Product). It holds fields and provides getters/setters.

## 32. POJO

POJO (Plain Old Java Object) is a lightweight Java class with private variables, constructors, and getter/setter methods, with no extra framework dependencies.

## 33. How to Implement Encapsulation

Declare class variables `private`, use `public` getter/setter methods to access and update them.

## 34. Encapsulation?

A core OOP concept where the internal state of an object is shielded from direct access, reducing complexity and increasing security.

## 35. Virtual DOM vs Real DOM

- **Virtual DOM**: Lightweight JS representation of UI. Fast updates.
- **Real DOM**: Actual browser-rendered structure. Slower updates.
  Virtual DOM is more efficient for UI re-renders.

## 36. WhatsApp/Instagram 25MB Status Upload

Client compresses media before uploading. Reduces upload time and storage requirements on the server.

## 37. VDOM vs Real DOM: Storage

Real DOM needs more memory since it's an actual UI node tree. VDOM is just JS objects, so it's lighter in terms of memory.

## 38. How to Add Permissions (Push) in UI

Store user permissions in app state. Conditionally show/hide actions like push/create using permission flags.

## 39. Core Level Permissions in UI

Set access control at component or route level. Use wrappers or guards to restrict rendering or navigation based on user role/permissions.

## 40. Push, Create Resource, Create User → Permissions

Define permission keys (e.g., `canPush`, `canCreateUser`). Check these flags in UI logic before rendering actions.

## 41. Permissions in Hardcoding?

Avoid hardcoding permissions. Use role-permission mappings from backend or config files to manage access dynamically.

## 42. Database Hardcoding?

Hardcoding DB logic is fragile. Prefer normalized tables and parameterized queries or stored procedures for flexibility and security.

## 43. Role Management DB Tables

- `users`
- `roles`
- `permissions`
- `user_roles`
- `role_permissions`
  This structure supports flexible, scalable access control.

## 44. Ecommerce App Redux

Redux manages global state: cart, user auth, product list. Helps in predictable state transitions and syncing UI with server responses.

## 45. State Management

State can be managed using Redux, Context API, Zustand, etc. Centralizes state for consistency and better debugging.

## 46. Can We AJAX Synchronous?

Yes, but discouraged. Synchronous calls block the main thread, freeze UI. Always prefer async with Promises or `async/await`.

## 47. AJAX Call?

AJAX is used to fetch or send data to the server without reloading the page. Common tools: `fetch()`, `axios`, or `XMLHttpRequest`.

## 48. useState in JavaScript?

`useState` is React’s way to declare reactive state inside functional components. In vanilla JS, closures or IIFEs can somewhat mimic state behavior.

## 49. Scope of Layers in the Application

Divide code into layers:

- **Presentation Layer** (UI)
- **Business Logic Layer** (validation, processing)
- **Service Layer** (API calls)
- **Data Layer** (DB interaction)
  Keeps code modular and easier to manage.

## 50. z-index?

CSS property to control stacking order. Higher `z-index` brings an element visually on top of lower-indexed elements.

## 51. Normalization: Better Table Structure?

Yes. Normalization reduces data redundancy, improves consistency, and maintains referential integrity across tables.

🔧 Suggested Normalized Structure:
users
id firstname lastname age mobile is_active is_prime

addresses
id user_id address1 address2 city state pincode country


