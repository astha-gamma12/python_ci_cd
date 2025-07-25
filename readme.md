on: push → Run the workflow when you push code to the main branch.

on: pull_request → Run when someone opens a pull request to main.

🚀 It automatically checks your code when you push or open a pull request.


jobs` → A job is a collection of steps that run in the same environment.
- Here, the job is named `build`

Inside the job, you define **steps** — what should actually be done (e.g., checkout code, install Python, run tests).

---

### 🔧 Step 1: Checkout the code

```yaml
    - name: Checkout code
      uses: actions/checkout@v4



      yaml
    - name: Checkout code
      uses: actions/checkout@v4
This downloads your code from the GitHub repository so the runner can work with it.





CI is used to automatically test your code whenever changes are pushed to the repository.



name: python-app-ci-cd

on:
  push:
    branches:
      - master
  pull_request:
    branches:
      - master

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v4

      - name: Run tests
        run: |
          pytest




_______________________________

name: python-app-ci-cd

on:
  push:
    branches:
      - master
  pull_request:
    branches:
      - master

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v4

      - name: Run tests
        run: |
          pytest