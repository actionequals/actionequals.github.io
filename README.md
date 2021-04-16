"United Pest" is a demo GitHub Pages site for a fictitious company.

The purpose is to show how to configure <form> tags for use with https://actionequals.com/ "forms as a service".

See the [blog article]([GitHub Pages + ActionEquals = Awesome](https://actionequals.com/Blog/GitHub-Pages-+-ActionEquals-=-Awesome)) there for a walk through, but basically, after you get an API Key, you provide 

<code>
<form method=post action='https://actionequals.com/apiKey&f=form'>...</form>
</code>

When forms are submitted, they will be stored in a database which you can view from your ActionEquals.com dashboard.  [Sample Dashboard](https://actionequals.com/dashboard). The dashboard supports complex queries, sorting, and csv export.

Each form corresponds to a table, the form submissions being records.  Generally, you can "create" columns by naming form elements with a capital letter (other fields get written into a multivalued (KVP) "Misc" column).  There are other optional features such as CAPTCHA, "turnkey" login and registration forms.  The CAPTCHA feature requires but a single line of Javascript to inject into the DOM.

You also have access to a REST API for automation.  [Documentation](https://actionequals.com/examples) is thorough.

The service itself grew out of a web application to quickly create and modify pharmaceutical clinical trial questionnaires and collect the results without needing database maintenance or a programmer to set up each different trial.

The main general use case is to be able to support contact forms, surveys, and the like for one or more statically-hosted (e.g. GitHubPages) sites and to be able to collect and query the submitted data.  It is also useful for providing an immediate implementation for forms before any database or custom server-side processing has been written.
