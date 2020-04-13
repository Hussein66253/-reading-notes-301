# Partials
When using the default view engine **(ejs)**, Sails supports the use of partials *view partials*.   
- Partials are basically just views that are designed to be used from within other views.   

- They are particularly useful for reusing the same markup between different views, layouts, and even other partials.

        <%- partial('./partials/navbar.ejs') %>
- This should render the partial located at views/partials/navbar.ejs, which might look something like this:

                <%
                /**
                * views/partials/navbar.ejs
                *
                * > Note: This EJS comment won't show up in the ejs served to the browser.
                * > So you can be as verbose as you like.  Just be careful not to inadvertently
                * > type a percent sign followed by a greater-than sign (it'll bust you out of
                * > the EJS block).
                *
                */%>
                <nav class="navbar">
                <a href="/">Dashboard</a>
                <a href="/inbox">Inbox</a>
                </nav>
- The target path that you pass in as the first argument to **partial()** should be relative from the view, layout, or partial where you call it. So if you are calling **partial()** from within a view file located at* views/pages/dashboard/user-profile.ejs*, and want to load views/partials/widget.ejs then you would use:

        <%- partial('../../partials/navbar.ejs') %>
### Partials and view locals
- Partials automatically inherit the view locals that are available wherever they are used. For example, if you call **partial()** within a view where a variable named *currentUser* is available, then *currentUser* will also be available within the partial:

            <%
            /**
            * views/partials/navbar.ejs
            *
            * The navbar at the top of the page.
            *
            * @needs {Dictionary} currentUser
            *   @property {Boolean} isLoggedIn
            *   @property {String} username
            */%>
            <nav class="navbar">
            <div class="links">
                <a href="/">Dashboard</a>
                <a href="/inbox">Inbox</a>
            </div>
            <span class="login-or-signup"><%
            // If the user accessing this page is logged in...
            if (currentUser.isLoggedIn) {
            %>
                You are signed in as <a href="/<%= currentUser.username %>"><%= currentUser.username %></a>.
            <%
            }
            // Otherwise the user accessing this page must be a visitor:
            else {
            %>
                <a href="/login">Log in</a>
            <%
            }
            %>
            </span>
            </nav>
