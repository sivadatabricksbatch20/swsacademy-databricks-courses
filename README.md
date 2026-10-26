# SWS Academy · Databricks Courses

Course notebooks for **Machine Learning with Databricks** and **Advanced Machine Learning with Databricks**, ready to use as a Databricks Git folder.

| Folder | Course | Compute |
|---|---|---|
| `01 Machine Learning` | 1 Data Preparation · 2 Model Development · 3 Model Deployment · 4 ML Operations | Serverless (environment version 5) |
| `02 Advanced Machine Learning` | 0 Concept notebooks · 1 Model Development at Scale (A1) · 2 Advanced ML Operations (A2) | A1 and A2: classic cluster, **Databricks Runtime 16.4 LTS ML** (single node is enough). Concept notebooks: serverless |

## Get the course into your workspace

1. In Databricks, open **Workspace**, go to your home folder, and click **Create → Git folder**.
2. Paste the repository URL `https://github.com/sivadatabricksbatch20/swsacademy-databricks-courses` and click **Create Git folder**.
3. To get updates later, open the Git folder, click the branch name at the top, and click **Pull**.

Use the Git folder rather than a DBC or zip export: a DBC keeps notebooks only and drops the plain files that some demos need (for example the Asset Bundle `.yml` files).

## Run the demos as jobs

- **Machine Learning:** open `00 - Create SWSAcademy Demo Jobs` and click **Run all**. Then run the jobs in **Jobs & Pipelines** one at a time: 01 → 02 → 03 → 04.
- **Advanced ML:** attach `00 - Create SWSAcademy Advanced ML Jobs` to your 16.4 LTS ML cluster and click **Run all**. Run the A2 job (or its admin setup) once before the A0 concept job.
- **Clean up:** `99 - SWSAcademy Cleanup and Billing` removes what the demos created. It is a dry run unless `confirm_delete` is set to `YES`.

## Before the Advanced ML CI/CD demo (A2 · M01)

Create a GitHub repository with a README and a personal access token with `repo` permission. Then open
`02 Advanced Machine Learning/2 - swsacademy-advanced-machine-learning-operations/M01 - Streamlining MLOps with Databricks/0 - Generate Tokens`,
run it, and enter your GitHub username, repository name and token in the boxes **at the top of the notebook**. Never type a token into the code. The token is saved in a `var` folder, which this repository ignores so it is never committed.

## Costs

Model Serving endpoints created by the deployment and rollout demos keep running until deleted (they scale to zero when idle). Terminate classic clusters when you finish, or set auto-terminate to 30 minutes.
