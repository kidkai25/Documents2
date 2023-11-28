SQL Popup Feature

# SQL Popup Feature

This tool has been developed for internal use among developers to quickly view the SQL queries executed on a given page. It serves a similar purpose to a profiler.

Workflow

When we open an URL Controller/Action **?showsql=1** , a modal/popup appears showing all the SQL queries made on the page (via AJAX calls).

After that, the modal automatically opens every time for each individual action that makes an AJAX call and the call completes.

![](https://github.com/kidkai25/Documents2/blob/main/Picture1.png)

![](https://github.com/kidkai25/Documents2/blob/main/Picture2.png)

The call of ShowSQL() action results in checking if a session object exists with value "showsql", if it does not no view is returned otherwise a partial view containing the Modal/Popup is returned to the client.

But before return the view we reset the static list and also remove the showsql object from the session.

So for viewing the modal/popup the **presence Session["showsql"] session object is a must.**

![](https://github.com/kidkai25/Documents2/blob/main/Picture3.png)

After showing all the SQL queries made on the page via AJAX calls. AJAX Complete handler is setup so now after each new AJAX call on the existing page. A modal is automatically open when that AJAX call completes.

![](https://github.com/kidkai25/Documents2/blob/main/Picture4.png)

Examples:

![](https://github.com/kidkai25/Documents2/blob/main/Picture5.png)