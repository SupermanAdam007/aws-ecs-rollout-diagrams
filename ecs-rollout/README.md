## ECS Deployment Process

### 1. Initial State
- The ECS cluster starts with **two running Docker containers**, representing the original or old version of your application.
- Sets the baseline for the deployment process.

### 2. Deploy New Container
- A **third Docker container** (new version) is deployed to the ECS cluster.
- Follows the **150% rolling strategy**, temporarily increasing the total number of containers to three.

### 3. Decommission Old Container
- **One old version container** is decommissioned, reducing the total number of containers back to two.
- The cluster now has one old version container and one new version container.

### 4. Rollout Continuation
- Another **new version container** is deployed, and the last old version container is decommissioned.
- Results in the ECS cluster having **two containers**, both running the new version of your application.

Each step is visualized through a separate diagram, showing the transition from the old to the new version in the ECS cluster, in line with the rolling update strategy.
