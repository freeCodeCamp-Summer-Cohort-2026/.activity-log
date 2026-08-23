## 2026-08-11

Working on [shiftlog](https://github.com/freeCodeCamp-Summer-Cohort-2026/shiftlog)

- Read up on [docs from fCC](https://contribute.freecodecamp.org/basic-git-workflow/) re: creating a fork of a repo, cloning it, connecting to upstream, creating a new branch. Did all of these for the shiftlog repo. 
- Installed docker and got it running to be able to run the shiftlog and view at localhost
- Learned how to install dependencies using `pip install -r requirements.txt` and had to troubleshoot issues b/c I set up my .venv with the wrong python version at first. Fixed that.

I now have a clean fork and branch, and am ready to start working on the issue I've claimed (will start tomorrow).

## 2026-08-13

Working on Working on [shiftlog](https://github.com/freeCodeCamp-Summer-Cohort-2026/shiftlog), [issue 40]([url](https://github.com/freeCodeCamp-Summer-Cohort-2026/shiftlog/issues/40)).

Spent some time today learning how the existing `list_workers()` function in `app.routers.workers` works. Then started drafting a function that is currently the right overall approach I think but it's a bit bare bones and the moment. It needs more work to check if the role parameter was added correctly, to return an empty list if not, etc. 

Haven't started on tests yet.

## 2026-08-17

- Ran into an issue where the Swagger UI for shiftlog was returning a 500 internal server error. Spent time trying to figure out why and how to address it.
- Started working on [shiftlog issue 75](https://github.com/freeCodeCamp-Summer-Cohort-2026/shiftlog/issues/75) and found that it is more complicated than I had originally thought. Spent time trying to work through what is needed to fix various parts of the codebase to use timezone-aware objects rather than timezone-naive ones (which is what is in the codebase right now). This is going to take some time to figure out and I'm deciding whether to let someone with more skills take this one on.

## 2026-08-20

- Spent a lot of time today on [shiftlog issue 75](https://github.com/freeCodeCamp-Summer-Cohort-2026/shiftlog/issues/75). Making the necessary syntax change was easy. Trying to figure out if it was going to break anything was not. I spent many hours today and for the past few days trying to understand enough to feel confident that this would not break anything.
- It won't, but it hides a deeper issue that I'll document and we probably don't want to deal with for the purpose of this sprint--even though this change uses timezone-aware objects the database will still strip the timezone info out so it will disappear. This is already happening in current functionality even when timezone is added by the user when creating shifts, so it doesn't change anything in current functionality. It's just that if this were production and used by people in different timezones that could be an issue.

## 2026-08-22

- I was interested in working on datalens in addition to shiftlog (which I've been working on the whole sprint). Spent a few hours reviewing the datalens codebase and familiarizing myself with Jupyter Hub.

## 2026-08-23

- Worked on [issue #44 in datalens](https://github.com/freeCodeCamp-Summer-Cohort-2026/datalens/issues/44): add an outlier detection cell to the demo notebook.
- Spent time learning about IQR outlier detection and boxplots
- Created a cell that shows the first 10 outlier rows using the `detect_outliers` function in `datalens/analysis.py`
- Created another cell that generates a boxplot of all outliers in the cleaned `data/sample.csv` file
