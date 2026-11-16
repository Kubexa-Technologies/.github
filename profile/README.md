# Kubexa Technologies

Open-source Kubernetes tools for the agent era, built toward a software forge that runs itself.

## What we build

Kubexa Technologies writes open-source tools for Kubernetes. The tools solve problems that
appear when software agents do the work. They let an agent act on a cluster without holding
long-lived credentials, and they report what they did in a way a person can check.

This organisation is the home for a family of tools, not for one product.

- `hydradb-operator` - the operator for HydraDB on Kubernetes. It is the first one
  published here, and it runs our own cluster.
- A second operator is in design. It does not have a public repository yet. When it
  does, it will be listed here next to the first one.

Everything we publish is open source. You can read the code, run it, and change it.

## Where we are going

A software forge takes an idea and returns running software. Most of that path still needs a
person at the controls: reviews, releases, deploys, and the small repairs after them. We want
that path to run itself, with people setting direction and checking results. Every tool we
publish is a piece of that path.

## Working in the open

Each repository explains what it does and how to run it. Where a page here claims that
something works, the claim came from a measurement, not from a plan.

## What we run, in public

A lot of companies write as if they invented a whole stack. Many of them do not say
what runs under the hood, which parts they built, and which parts they borrowed. A
reader cannot check the claim.

We take the other path. Our stack is written down in public, at
[kubexa.tech](https://kubexa.tech): the hardware, the network, the storage, the
controllers, and the versions. The documentation comes from the repository that
builds the cluster, so a page cannot drift from what runs. Where a device or a service
needs a credential, the documentation names the path and the shape of the secret, not
its value.

We also give back. Tools we build for our own cluster go upstream as open source,
including the operator in this organisation, and we report what we find in the
projects we depend on. If a piece of this platform helps someone else, it should not
sit in a private repository.

## Everything through git, and safely

We change our platform by changing a repository. A commit lands after review, a
controller applies it, and the cluster converges. Nobody edits a live system by hand,
so the repository is the record of what runs and why.

Security follows the same rule. A secret never sits in a repository, in an image or in
a build log. Secrets live in a vault, an operator copies them into the workloads that
need them, and a manifest refers to them by name. Where a pipeline needs a credential,
it asks for a short-lived token instead of holding a long-lived one.

## Contributing

Contributions are welcome, and so are issues. A bug report, a question or a pull request all
help, and none of them needs permission first.

One honest limit. This work continues next to other projects, so there is no promised timeline
for a review or a merge. Issues and pull requests are read, but they can wait longer than they
would in a project with paid maintainers. If something is urgent for you, say so in the issue
and explain why. That is the one thing that changes the order.

## Contact

- Security reports: open a private security advisory on the affected repository.
- Everything else: an issue on the repository in question reaches us faster than email.
- Email: info@kubexa.tech, the same address the website publishes.
- Collaboration is invite-only, and there is nothing to apply for: no job openings, no paid
  positions, no recruitment process. If you want to join anyway, write to info@kubexa.tech and
  say what you would like to work on. This is unpaid work on an idea, done by people who asked
  to join.
- The website and the platform documentation live at https://kubexa.tech.
