![image](https://github.com/user-attachments/assets/06642d80-3afe-4fd3-a663-6bea5eaff167)


# wagtail-template

This is the template that can be used for projects using wagtail.

It's built using [Django](https://www.djangoproject.com) and the Content Management System (CMS) [Wagtail](https://wagtail.org/).

## Running it locally

### Installing Python and Poetry

You specifically need Python 3.12. If you don't have this version installed, head over to [python.org/downloads](https://python.org/downloads)

You also need Poetry, a Python package manager. Instructions for installation are [available here](https://python-poetry.org/docs/#installing-with-pipx).

### (Recommendation, optional) install the PyCharm IDE

If you're inexperienced with Django or Python specific tooling, the easiest way of developing the project locally will be using PyCharm. This is due to its integrated features for Django, and automated management of the Poetry environment.

PyCharm is available for free, as long as you sign up for the [GitHub student developer pack](https://education.github.com/pack). It is important that you get this because we *need* PyCharm Professional edition, [available here](https://www.jetbrains.com/pycharm/download).

### Using this template

Click on "Use this template" followed by "Create a new repository".

### Running migrations and creating a user 

The project depends on a SQLite database. This is not yet initialized and is the reason why we saw the 'OperationalError' earlier. We need to create this database and a user for accessing the management panel.

- Open up a terminal. This should be the forth option in the bottom left corner of PyCharm. 
- Run: `python manage.py migrate`. This can take a couple of seconds and you should see a lot of text fly by.
- Run: `python manage.py createsuperuser`
  - Type your preferred username, then click enter.
  - Type your email address (nobody needs this; you can enter a fake one...), then click enter.
  - Type a password, click enter. Type the same password again and click enter.
    - It may yell at you if the password is not sufficiently complex. You can type `y` and override this protection. This login only applies to your local version of the website.
- Run the server with `python manage.py runserver` and navigate to [localhost:8000/](http://localhost:8000/) (by default).

### Profit.

The website should now be in working order on your computer. On running the website with the Play button in PyCharm (or command if not using PyCharm), you should no longer see an error message.

### Creating new pages.

New pages can be created by going to [localhost:8000/admin/](http://localhost:8000/admin/) -> Pages -> click on the pencil next to the title -> click on the triple dots on the top of the page -> Add child page.

You can navigate to the page that you created by using the title of your page like this:  
For example if we made a page with the title "testpage", navigate to [localhost:8000/testpage/](http://localhost:8000/testpage/) after you publish using the drop up menu at the bottom of the page.

The child page contains a title and a hero section and body. The formatting of the text can be changed by clicking the green + button that hovers to the left of the textbox. 

Build away!

