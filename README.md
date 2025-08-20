| Concept               | uDeploy JSON (IBM)                      | Harness YAML (Harness.io)                                |
| --------------------- | --------------------------------------- | -------------------------------------------------------- |
| **Process Name**      | `"name": "Deploy Component"`            | `pipeline: name: WebApp-Deployment`                      |
| **Steps**             | `"componentProcessStep"` objects        | `steps:` under execution                                 |
| **Shell Command**     | `"command": "systemctl stop tomcat"`    | `ShellScript step → script:`                             |
| **Artifact Download** | `"Download Artifacts"` with destination | `DownloadArtifact` with `destinationPath`                |
| **Properties / Vars** | `${p:version/name}` placeholders        | `connectorRef`, `artifactRef`, and environment variables |
| **Tags**              | `"tags": ["deploy","webapp"]`           | `tags: { deploy: "webapp" }`                             |
