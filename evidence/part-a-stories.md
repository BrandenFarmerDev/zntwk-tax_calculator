Epic: Modernise Tax Calculator

Modernise the static, manually deployed tax calculator using containers, IBM Cloud Code Engine, and a tested build pipeline.

Story 1: Containerize the application
As a developer, I need a Docker image of the tax calculator so that it runs consistently across environments.
Acceptance: all seven Jasmine tests pass before container deployment; a failing test blocks deployment. nginx serves the five supplied static assets; image builds; port 8080 displays a working calculator.

Story 2: Deploy the application on IBM Cloud
As a user, I need an accessible cloud application so that I can calculate tax through a browser.
Acceptance: image pushed to the provided IBM registry namespace; Code Engine reports ready; the application URL works.

Story 3: Create the packaging pipeline
As a developer, I need a pipeline that installs dependencies, runs tests, and builds/pushes the image so that a failing test prevents packaging.
Acceptance: clone → npm install → Jasmine → buildah order; all seven tests pass; genuine successful run logs and deployed final UI captured.
