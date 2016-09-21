# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components.

    ```md
    In an email app emails could be displayed on the inital screen as just the
    subject line and 'from' field, and many could be shown at once. To the left of this,
    contacts could be shown as just names. When you click on an email on the page
    page you are taken to a view with the body of the email and all other
    fields and options (CC, forward, etc). If you click on a contact on the main page
    you are taken to a view with more info about that specific contact. Both email messages
    and contacts would be components. Their more atomic pieces such as subject line 
    or a contact's profile picture would all be components as well.
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember generate component my-map
    ```

1.  What files are edited to produce a component, and what are their
    responsibilities?

    ```md
    When a component is generated a component.js file, a corresponding
    template.hbs and a component-test.js file are created. The template determines
    how the component looks to the user. The component.js file contains the actions
    associated with the component which gives it functionality. The test file is
    pre-made tests for the component. You can edit or add more tests if necessary.
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` path. What is
    the syntax for loading this component inside that template?

    ```html
    {{my-contact contact=model}}
    ```

    Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{my-contact/my-phone phoneNumber=phoneNumber}}
    ```
