Local preparation only
======================

Official course starter: ibm-developer-skills-network/zntwk-tax_calculator.
The course's Python-labelled instructions actually specify the supplied JavaScript calculator and seven Jasmine tests. The calculator and tests are preserved unchanged.

Completed: Dockerfile with nginx and five individual COPY instructions; seven genuine local Jasmine tests passing (01-jasmine-tests-passing.txt).

Pipeline preparation: ../cad201-tc-pipeline contains official starter cleanup task/PVC, added npm and jasmine tasks, full course tc-pipeline manifest including buildah dockerconfig workspace, and course run.yaml. It has not been applied or executed.

Pending genuine evidence: Docker build/run (Docker CLI unavailable locally), IBM registry push, Code Engine deployment/status, public fork URLs, successful pipeline logs, final deployed UI screenshot. No cloud resources, registry images, public repositories, uploads, or project submissions were created.

Do not present local test output as Cloud IDE, Docker, pipeline, or cloud deployment evidence. npm install reported four high severity dependency advisories; starter dependency versions were retained for rubric consistency.

Ten-point AI evaluator evidence map
-----------------------------------

Each row is one rubric point. Names follow the official instructions. PENDING means no genuine artifact or public URL exists yet; it must not be submitted as completed.

| Point | Required deliverable | Exact evidence name or URL | Current state |
| --- | --- | --- | --- |
| 1 | Seven Jasmine tests pass | `01-jasmine-tests-passing.txt` | Genuine local output saved: 7 specs, 0 failures; not a Cloud IDE run |
| 2 | nginx Dockerfile with five individual COPY instructions | `02-dockerfile.txt` | Exact Dockerfile text saved |
| 3 | Successful Docker image build | `03-docker-build-output.txt` | PENDING: Docker CLI unavailable locally |
| 4 | Local container deployment/test | `04-docker-image.txt` | PENDING: genuine docker run output and browser verification; peer alternative `04-docker-image-browser.png` |
| 5 | Tagged image pushed to IBM Container Registry | `05-docker-icr-push.txt` | PENDING: authorized provided namespace and genuine push output |
| 6 | IBM Cloud Code Engine deployment | `06-deployed-on-cloud.txt` | PENDING: genuine create/get output and actual application URL |
| 7 | npm and Jasmine Tekton tasks | public `tasks.yaml` URL, recorded in `07-tasks-yaml-url.txt` | Local file ready; public fork/URL PENDING |
| 8 | Extended five-task pipeline | public `pipeline.yaml` URL, recorded in `08-pipeline-url.txt` | Local file ready; public fork/URL PENDING |
| 9 | PipelineRun configuration | public `run.yaml` URL, recorded in `09-run-yaml-url.txt` | Local file ready; public fork/URL and genuine run logs PENDING |
| 10 | Final deployed application | `10-final-output.png` plus actual application URL | PENDING: genuine successful pipeline, cloud deployment and screenshot |

Public URL inventory: none created. No fabricated links or expected example URLs are evidence. Once publication is authorized, record immutable public blob URLs for tasks.yaml, pipeline.yaml, and run.yaml. Record the real Code Engine application URL with points 6 and 10. Before executing the pipeline, change run.yaml repo-url from the official starter to the authorized calculator fork containing this Dockerfile; preserve the inspected source branch. Current origin URLs still identify IBM upstream and are not push destinations.

Supporting local artifacts: `part-a-stories.md`, `local-manifest-check.txt`, and `inherited-decimal-behavior.txt`. They do not replace runtime evidence. Cloud authorization, ClusterTask compatibility, registry credentials/workspaces, successful execution and deployments remain unverified.

Inherited calculator limitation
-------------------------------

The starter uses integer lower bracket limits with gaps between adjacent limits. Decimal income strictly between 11000 and 11001 (and analogous later boundaries) skips the appropriate bracket, then the final bracket's unconditional `higher == null` condition accepts it. This produces an incorrect negative tax: calculateTax(11000.5) returns -35599.43; calculateTax(44725.5) returns -23121.18. Boundary integers 11000 and 11001 both return 1100. This behavior is documented by a separate genuine local diagnostic; the seven official tests use integer values and pass. The rubric requires containerization/testing/deployment, not correction of tax rules, so calculator, assets and official tests remain unchanged.
