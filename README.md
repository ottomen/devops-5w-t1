# DevOps course | Week 5/Task 1

Help colleagues to complete tasks

Hello!

I’m going to help, because DevOps is looking out for us, that yoga task was thrown on me.
And I'm not kidding. As far as I understand the task, I need to write a plugin for Kubernetes to take some statistics, some logs.

I was given a request for how these plugins will work https://krew.sigs.k8s.io/plugins/ and that’s how it works https://kubernetes.io/docs/tasks/extend-kubectl/kubectl-plugins/

I'm trying to figure out the this code, but it returns the error:

```
$>bash kubeplugin
error: flag needs an argument: 'n' in -n
See 'kubectl --help' for usage.
```

## Solution

The problem was that there were no actual command of getting the resource usage of k8s. I've added the `top` command that shows the resource usage.

Here is how you can use the plugin:

```
bash kubeplugin <resource-type> <namespace>
```

Example of usage:

```
bash kubeplugin nodes default
```
