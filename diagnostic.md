# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components.

    ```md
    For data down the information of the model goes to the component and then it is sent to the template.
    Say you have information on daily chores and you want to display the information as a list.  You can use the information from the route and pass it to a component to render a list of chores.
    But when it bubbles up the information stays in component unless you send the action out to the route.
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember g component my-map
    ```

1.  What files are edited to produce a component, and what are their
    responsibilities?

    ```md
    You would want to edit the components files (component.js and the template.hbs) and in the template of whatever path you want to pass in the component and bind it to data in handlebars.
    {{component data=data}}

    Component file responsibilities: component file allows you to pass html bindings, event actions, or click handlers to the template.  The template just renders the information in handlebars.
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` path. What is
    the syntax for loading this component inside that template?

    ```html
    {{#each model as |contact|}}
    {{my-contact contact=contact}}
    {{/each}}
    ```

    Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{#each contacts.phones as |phone|}}
    {{my-contact/my-phone phone=phone}}
    {{/each}}
    ```
