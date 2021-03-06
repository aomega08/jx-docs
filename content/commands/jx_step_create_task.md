---
date: 2019-03-01T08:42:15Z
title: "jx step create task"
slug: jx_step_create_task
url: /commands/jx_step_create_task/
---
## jx step create task

Creates a Knative Pipeline Run for the current folder or given build pack

### Synopsis

Creates a Knative Pipeline Run for a project

```
jx step create task [flags]
```

### Examples

```
  # create a Knative Pipeline Run and render to the console
  jx step create task
  
  # create a Knative Pipeline Task
  jx step create task -o mytask.yaml
  
  # view the steps that would be created
  jx step create task --view
```

### Options

```
      --branch string            The git branch to trigger the build in. Defaults to the current local branch name
      --clone-git-url string     Specify the git URL to clone to a temporary directory to get the source code
  -c, --context string           The pipeline context if there are multiple separate pipelines for a given branch
      --delete-temp-dir          Deletes the temporary directory of cloned files if using the 'clone-git-url' option
  -d, --dir string               The directory to query to find the projects .git directory
      --docker-registry string   The Docker Registry host name to use which is added as a prefix to docker images
      --duration duration        Retry duration when trying to create a PipelineRun (default 30s)
  -h, --help                     help for task
      --image string             Specify a custom image to use for the steps which overrides the image in the PodTemplates
  -k, --kind string              The kind of pipeline to create such as: release, pullrequest, feature (default "release")
  -l, --labels stringArray       List of custom labels to be applied to resources that are created
      --no-apply                 Disables creating the Pipeline resources in the kubernetes cluster and just outputs the generated Task to the console or output file
      --no-release-prepare       Disables creating the release version number and tagging git and triggering the release pipeline from the new tag
  -o, --output string            The directory to write the output to as YAML
  -p, --pack string              The build pack name. If none is specified its discovered from the source code
      --pr-number string         If a Pull Request this is it's number
  -r, --ref string               The Git reference (branch,tag,sha) in the Git repository to use
      --revision string          The git revision to checkout, can be a branch name or git sha
      --service-account string   The Kubernetes ServiceAccount to use to run the pipeline (default "tekton-bot")
      --source string            The name of the source repository (default "source")
      --target-path string       The target path appended to /workspace/${source} to clone the source code
  -t, --trigger string           The kind of pipeline trigger (default "manual")
  -u, --url string               The URL for the build pack Git repository
      --view                     Just view the steps that would be created
```

### Options inherited from parent commands

```
  -b, --batch-mode                Runs in batch mode without prompting for user input
      --install-dependencies      Enables automatic dependencies installation when required
      --log-level string          Sets the logging level (panic, fatal, error, warning, info, debug) (default "info")
      --no-brew                   Disables brew package manager on MacOS when installing binary dependencies
      --skip-auth-secrets-merge   Skips merging the secrets from local files with the secrets from Kubernetes cluster
      --verbose                   Enables verbose output
```

### SEE ALSO

* [jx step create](/commands/jx_step_create/)	 - create [command]

###### Auto generated by spf13/cobra on 1-Mar-2019
