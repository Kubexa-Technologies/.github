# Kubexa Technologies

<p align="center">
  <img alt="Focus: Kubernetes tools" src="https://img.shields.io/badge/focus-kubernetes%20tools-326ce5.svg">
  <img alt="License: open source" src="https://img.shields.io/badge/license-open%20source-blue.svg">
  <img alt="Status: early work" src="https://img.shields.io/badge/status-early%20work-orange.svg">
  <img alt="Work: unpaid" src="https://img.shields.io/badge/work-unpaid-lightgrey.svg">
</p>

We write open-source tools for Kubernetes, for the time when software agents do much of the work.

An agent is a program that acts on its own. The tools here let an agent act on a cluster without a
long-lived credential, and they show a person what the agent did. You can read the code, run it, and
change it. Every repository here is open source.

## What lives here

This organization holds a family of tools, not one product.

- `hydradb-operator`: an operator for HydraDB on Kubernetes. An operator is a program that keeps
  cluster objects in the state you declare. This one runs our own cluster. It is early work, and its
  README says so.
- A second operator is in design. It has no public repository yet. When it has one, we list it here.

## Where this goes

A software forge takes an idea and returns running software. Most of that path still needs a person
at the controls: review, release, deploy, and the small repairs after them. We want the path to run
itself, with people setting direction and reading results. Each tool here is one part of that path.

## What we run, in public

Many companies write as if they built a whole stack. Few of them say what runs under the hood, which
parts they wrote, and which parts they borrowed. A reader cannot make sure that the claim is true.

We take the other path. We write down our stack at [kubexa.tech](https://kubexa.tech): the hardware,
the network, the storage, the controllers, and the versions. The pages come from the repository that
builds the cluster, so a page cannot drift from what runs. If a device or a service needs a
credential, a page names the path and the shape of the secret, not its value.

We also give back. A tool that we build for our own cluster goes upstream as open source, and we
report what we find in the projects that we depend on. If a part of this platform helps you, it must
not stay in a private repository.

## Everything through git, and safely

We change our platform by changing a repository. A change lands after review, a controller applies
it, and the cluster converges. A controller is a program that watches resources and acts on them. No
person edits a live system by hand, so the repository is the record of what runs and why.

Security follows the same rule. A secret never sits in a repository, in an image, or in a build log.
Secrets live in a vault. An operator copies a secret into the workload that needs it, and a manifest
refers to the secret by name. If a pipeline needs a credential, it asks for a short-lived token
instead of holding a long-lived one.

## Contributing

You can send a bug report, a question, or a pull request. You do not need permission first.

- If you found a bug, open an issue. Say what you ran, what you expected, and what happened.
- If you want a change, open an issue first. We can agree on the shape before you write code.
- If you send a patch, keep it small. Add the test that would have caught the bug.

There is one limit that we state plainly. This work continues next to other projects. We cannot
promise a date for a review or a merge. We read issues and pull requests. They can wait longer than
they would in a project with paid maintainers. If your problem is urgent, say so in the issue and
explain why. That is the one thing that changes the order.

## Contact

- To report a vulnerability, open a private security advisory on the repository, or write to
  security@kubexa.tech.
- For anything else, an issue on the repository reaches us faster than email.
- Email: hello@kubexa.tech.
- Work here is invite-only, and there is nothing to apply for. We have no job openings, no paid
  positions, and no recruitment process. If you want to join, write to hello@kubexa.tech and say what
  you would like to work on. Nobody is paid. People here work on an idea because they asked to join.
- Our stack documentation is at https://kubexa.tech.
