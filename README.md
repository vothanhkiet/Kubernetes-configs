# Kubernetes configs

[![GitHub stars](https://img.shields.io/github/stars/HariSekhon/Kubernetes-configs?logo=github)](https://github.com/HariSekhon/Kubernetes-configs//stargazers)
[![GitHub forks](https://img.shields.io/github/forks/HariSekhon/Kubernetes-configs?logo=github)](https://github.com/HariSekhon/Kubernetes-configs/network)
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/0a56edfc0ec9454dafffb02d37890cbc)](https://www.codacy.com/gh/HariSekhon/Kubernetes-configs/dashboard)
[![Lines of Config](https://img.shields.io/badge/lines%20of%20config-33k-lightgrey?logo=codecademy)](https://github.com/HariSekhon/Kubernetes-configs)
[![License](https://img.shields.io/github/license/HariSekhon/Kubernetes-configs)](https://github.com/HariSekhon/Kubernetes-configs/blob/master/LICENSE)
[![GitHub Last Commit](https://img.shields.io/github/last-commit/HariSekhon/Kubernetes-configs?logo=github)](https://github.com/HariSekhon/Kubernetes-configs/commits/master)

[![CI Builds Overview](https://img.shields.io/badge/CI%20Builds-Overview%20Page-blue?logo=circleci)](https://harisekhon.github.io/CI-CD/)
[![Repo on Azure DevOps](https://img.shields.io/badge/repo-Azure%20DevOps-0078D7?logo=azure%20devops)](https://dev.azure.com/harisekhon/GitHub/_git/Kubernetes-configs)
[![Repo on GitHub](https://img.shields.io/badge/repo-GitHub-2088FF?logo=github)](https://github.com/HariSekhon/Kubernetes-configs)
[![Repo on GitLab](https://img.shields.io/badge/repo-GitLab-FCA121?logo=gitlab)](https://gitlab.com/HariSekhon/Kubernetes-configs)
[![Repo on BitBucket](https://img.shields.io/badge/repo-BitBucket-0052CC?logo=bitbucket)](https://bitbucket.org/HariSekhon/Kubernetes-configs)

[![Kubevious](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/kubevious.yaml/badge.svg)](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/kubevious.yaml)
[![Kustomize Installs](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/kustomize-install.yaml/badge.svg)](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/kustomize-install.yaml)
[![Kustomize Namespace](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/kustomize-namespace.yaml/badge.svg)](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/kustomize-namespace.yaml)
[![Kustomize Objects Namespaced](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/kustomize-objects-namespaced.yaml/badge.svg)](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/kustomize-objects-namespaced.yaml)
[![YAML](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/yaml.yaml/badge.svg)](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/yaml.yaml)
[![JSON](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/json.yaml/badge.svg)](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/json.yaml)
[![Validation](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/validate.yaml/badge.svg)](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/validate.yaml)


[![Datree Kustomize](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/datree-kustomize.yaml/badge.svg)](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/datree-kustomize.yaml)
[![Pluto](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/pluto.yaml/badge.svg)](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/pluto.yaml)
[![Kustomize Nova](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/kustomize-nova.yaml/badge.svg)](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/kustomize-nova.yaml)
[![Checkov](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/checkov.yaml/badge.svg)](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/checkov.yaml)
[![Grype](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/grype.yaml/badge.svg)](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/grype.yaml)
[![Kics](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/kics.yaml/badge.svg)](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/kics.yaml)
[![Semgrep](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/semgrep.yaml/badge.svg)](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/semgrep.yaml)
[![Semgrep Cloud](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/semgrep-cloud.yaml/badge.svg)](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/semgrep-cloud.yaml)
[![Trivy](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/trivy.yaml/badge.svg)](https://github.com/HariSekhon/Kubernetes-configs/actions/workflows/trivy.yaml)

[git.io/k8s-configs](https://git.io/k8s-configs)

## Intro

Advanced Kubernetes YAML configurations & templates, based on my experiences running Kubernetes in production at different companies.

The top-level directory contains standard Kubernetes object templates with many Best Practices, Tips & Tricks learned over time across production environments.

The sub-directories contain ready-to-run real world apps that I've run across environments.

## Templates

Start with [deployment.yaml](https://github.com/HariSekhon/Kubernetes-configs/blob/master/deployment.yaml) / [statefulset.yaml](https://github.com/HariSekhon/Kubernetes-configs/blob/master/statefulset.yaml), for advanced users see [kustomization.yaml](https://github.com/HariSekhon/Kubernetes-configs/blob/master/kustomization.yaml).

The [service.yaml](https://github.com/HariSekhon/Kubernetes-configs/blob/master/service.yaml) contains config for using static public IP and locking down your cloud load balancer's firewall rules eg. to Cloudflare Proxied or VPN IPs only.

## Apps

Real-world app deployments are found in the more specific `<app>/` directories.

These follow standard the Kustomize `<app>/base/` and `<app>/overlay/` layout to make it easy to use as-is by just tweaking a couple settings in the overlay to your specific environment.

## CI/CD

Advanced auto-scaling production-grade CI/CD on Kubernetes:

- [ArgoCD](https://argoproj.github.io/cd/) - deployment, configs and optimizations. Start here: [argocd/base/kustomization.yaml](https://github.com/HariSekhon/Kubernetes-configs/blob/master/argocd/base/kustomization.yaml)
- [Jenkins](https://www.jenkins.io/) - jenkins server and dynamically scaling agents on kubernetes. Start here: [jenkins/base/kustomization.yaml](https://github.com/HariSekhon/Kubernetes-configs/blob/master/jenkins/base/kustomization.yaml)
  - see also: [Jenkins](https://github.com/HariSekhon/Jenkins) repo with advanced Jenkinsfile & Jenkins Shared Library
- [TeamCity](https://www.jetbrains.com/teamcity/) - teamcity server and dynamically scaling agents on kubernetes. Start here: [teamcity/base/kustomization.yaml](https://github.com/HariSekhon/Kubernetes-configs/blob/master/teamcity/base/kustomization.yaml)
- [Selenium Grid](https://www.selenium.dev/documentation/grid/) - simple and distributed auto-scaling deployments. Start here: [selenium-grid/base/kustomization.yaml](https://github.com/HariSekhon/Kubernetes-configs/blob/master/selenium-grid/base/kustomization.yaml) / [selenium-grid-distributed/base/kustomization.yaml](https://github.com/HariSekhon/Kubernetes-configs/blob/master/selenium-grid-distributed/base/kustomization.yaml)

## Helm + Kustomize integration

See [kustomization.yaml](https://github.com/HariSekhon/Kubernetes-configs/blob/master/kustomization.yaml) for 2 methods provided:

1. template the Helm chart using a `values.yaml` to Git and serve from there (see [DevOps Bash Tools](https://github.com/HariSekhon/DevOps-Bash-tools) for the `helm_template.sh` convenience script)
2. dynamically load the Helm chart from upstream with a `values.yaml`

...then patch override anything the chart doesn't directly support using the standard Kustomize patching examples given in the [kustomization.yaml](https://github.com/HariSekhon/Kubernetes-configs/blob/master/kustomization.yaml).

## Production Ready Checklist

- Healthchecks - readiness/liveness probes, see [deployment.yaml](https://github.com/HariSekhon/Kubernetes-configs/blob/master/deployment.yaml)
- Horizontal Pod Autoscaler - [horizontal-pod-autoscaler.yaml](https://github.com/HariSekhon/Kubernetes-configs/blob/master/horizontal-pod-autoscaler.yaml)
- Pod Disruption Budget - [pod-disruption-budget.yaml](https://github.com/HariSekhon/Kubernetes-configs/blob/master/pod-disruption-budget.yaml)
- Pod Anti-Affinity - stable vs preemptible, HA across AZs, see [deployment.yaml](https://github.com/HariSekhon/Kubernetes-configs/blob/master/deployment.yaml)
- Ingress Controllers - [Nginx](https://kubernetes.github.io/ingress-nginx/) ([config](ingress-nginx/base/)), [Kong](https://konghq.com/) ([config](kong/base/)) or [Traefik](https://traefik.io/traefik/) ([config](traefik/base/))
- Ingress SSL - [Cert Manager](https://cert-manager.io/) ([config](cert-manager/base/)) for [Automatic Certificate Management](https://en.wikipedia.org/wiki/Automatic_Certificate_Management_Environment) using the popular free Let's Encrypt certificate authority
- App Lifecycle Management - [ArgoCD](https://argoproj.github.io/cd/) ([config](argocd/base/))
- App Ingresses - [ingress.yaml](https://github.com/HariSekhon/Kubernetes-configs/blob/master/ingress.yaml), `*/base/ingress.yaml`
- App Resources - see resources section in [deployment.yaml](https://github.com/HariSekhon/Kubernetes-configs/blob/master/deployment.yaml)
- App Right-Sizing - [Goldilocks](https://www.fairwinds.com/goldilocks) ([config](goldilocks/base/)) to generate VPAs and resource recommendations
- DNS - [External DNS](https://github.com/kubernetes-sigs/external-dns) ([config](external-dns/base/)) integration to AWS Route53, Cloudflare etc.
- Secrets - [External Secrets](https://github.com/external-secrets/external-secrets) ([config](external-secrets/base/)) integration to AWS Secrets Manager, GCP Secret Manager etc. or [Sealed Secrets](https://github.com/bitnami-labs/sealed-secrets) ([config](sealed-secrets/base/))
- Network Policies - [network-policy.yaml](https://github.com/HariSekhon/Kubernetes-configs/blob/master/network-policy.yaml)
- Pod Security Policies - [pod-security-policy.yaml](https://github.com/HariSekhon/Kubernetes-configs/blob/master/pod-security-policy.yaml)
- Governance, Security & Best Practices - [Polaris](https://www.fairwinds.com/polaris) ([config](polaris/base/)) for recommendations
- Find Deprecated API objects to replace - [Pluto](https://pluto.docs.fairwinds.com/) - see [pluto_detect_kustomize_materialize.sh](https://github.com/HariSekhon/DevOps-Bash-tools/blob/master/kubernetes/pluto_detect_kustomize_materialize.sh) and [pluto_detect_kubectl_dump_objects.sh](https://github.com/HariSekhon/DevOps-Bash-tools/blob/master/kubernetes/pluto_detect_kubectl_dump_objects.sh) in the [DevOps Bash Tools](https://github.com/HariSekhon/DevOps-Bash-tools) repo

## Further Documention

The best documentation links are provided at the top of each yaml for fast referencing (my advanced [.vimrc](https://github.com/HariSekhon/DevOps-Bash-tools/blob/master/configs/.vimrc) can open these URLs from the current file via a hotkey!)

## Extra Docs

[Datree Kubernetes ArgoCD best practices](https://www.datree.io/resources/argocd-best-practices-you-should-know)

## Environment Enhancements

[.envrc](https://github.com/HariSekhon/Kubernetes-configs/blob/master/.envrc) - use with `direnv` to auto-load correct Kubernetes context isolated to current shell to avoid race conditions between shells and scripts caused by naively changing the global `~/.kube/config` context

Shortcut symlinks are for faster instantiation from these configs using the standard kubernetes shortcuts such as `new pvc.yaml` - see the [Templates](https://github.com/HariSekhon/Templates) repo for more details on the `new` command to fast create new files from templates.

## History

Forked from the [DevOps Perl tools](https://github.com/HariSekhon/DevOps-Perl-tools) repo, this is now a submodule of the [Templates](https://github.com/HariSekhon/Templates) repo which is a submodule of the DevOps [Bash](https://github.com/HariSekhon/DevOps-Bash-tools), [Perl](https://github.com/HariSekhon/DevOps-Perl-tools) and [Python](https://github.com/HariSekhon/DevOps-Python-tools) tools repos.

## Related Repositories

- [DevOps Bash Tools](https://github.com/HariSekhon/DevOps-Bash-tools) - 1000+ DevOps Bash Scripts, Advanced `.bashrc`, `.vimrc`, `.screenrc`, `.tmux.conf`, `.gitconfig`, CI configs & Utility Code Library - AWS, GCP, Kubernetes, Docker, Kafka, Hadoop, SQL, BigQuery, Hive, Impala, PostgreSQL, MySQL, LDAP, DockerHub, Jenkins, Spotify API & MP3 tools, Git tricks, GitHub API, GitLab API, BitBucket API, Code & build linting, package management for Linux / Mac / Python / Perl / Ruby / NodeJS / Golang, and lots more random goodies

- [Jenkins](https://github.com/HariSekhon/Jenkins) - Advanced Jenkinsfile & Jenkins Groovy Shared Library

- [GitHub-Actions](https://github.com/HariSekhon/GitHub-Actions) - GitHub Actions master template & GitHub Actions Shared Workflows library

- [Terraform](https://github.com/HariSekhon/Terraform) - Terraform templates for AWS / GCP / Azure / GitHub management

- [Templates](https://github.com/HariSekhon/Templates) - dozens of Code & Config templates - AWS, GCP, Docker, Jenkins, Terraform, Vagrant, Puppet, Python, Bash, Go, Perl, Java, Scala, Groovy, Maven, SBT, Gradle, Make, GitHub Actions Workflows, CircleCI, Jenkinsfile, Makefile, Dockerfile, docker-compose.yml, M4 etc.

- [SQL Scripts](https://github.com/HariSekhon/SQL-scripts) - 100+ SQL Scripts - PostgreSQL, MySQL, AWS Athena, Google BigQuery

- [DevOps Python Tools](https://github.com/HariSekhon/DevOps-Python-tools) - 80+ DevOps CLI tools for AWS, GCP, Hadoop, HBase, Spark, Log Anonymizer, Ambari Blueprints, AWS CloudFormation, Linux, Docker, Spark Data Converters & Validators (Avro / Parquet / JSON / CSV / INI / XML / YAML), Elasticsearch, Solr, Travis CI, Pig, IPython

- [DevOps Perl Tools](https://github.com/harisekhon/perl-tools) - 25+ DevOps CLI tools for Hadoop, HDFS, Hive, Solr/SolrCloud CLI, Log Anonymizer, Nginx stats & HTTP(S) URL watchers for load balanced web farms, Dockerfiles & SQL ReCaser (MySQL, PostgreSQL, AWS Redshift, Snowflake, Apache Drill, Hive, Impala, Cassandra CQL, Microsoft SQL Server, Oracle, Couchbase N1QL, Dockerfiles, Pig Latin, Neo4j, InfluxDB), Ambari FreeIPA Kerberos, Datameer, Linux...

- [The Advanced Nagios Plugins Collection](https://github.com/HariSekhon/Nagios-Plugins) - 450+ programs for Nagios monitoring your Hadoop & NoSQL clusters. Covers every Hadoop vendor's management API and every major NoSQL technology (HBase, Cassandra, MongoDB, Elasticsearch, Solr, Riak, Redis etc.) as well as message queues (Kafka, RabbitMQ), continuous integration (Jenkins, Travis CI) and traditional infrastructure (SSL, Whois, DNS, Linux)

- [HAProxy Configs](https://github.com/HariSekhon/HAProxy-configs) - 80+ HAProxy Configs for Hadoop, Big Data, NoSQL, Docker, Elasticsearch, SolrCloud, HBase, Cloudera, Hortonworks, MapR, MySQL, PostgreSQL, Apache Drill, Hive, Presto, Impala, ZooKeeper, OpenTSDB, InfluxDB, Prometheus, Kibana, Graphite, SSH, RabbitMQ, Redis, Riak, Rancher etc.

- [Dockerfiles](https://github.com/HariSekhon/Dockerfiles) - 50+ DockerHub public images for Docker & Kubernetes - Hadoop, Kafka, ZooKeeper, HBase, Cassandra, Solr, SolrCloud, Presto, Apache Drill, Nifi, Spark, Mesos, Consul, Riak, OpenTSDB, Jython, Advanced Nagios Plugins & DevOps Tools repos on Alpine, CentOS, Debian, Fedora, Ubuntu, Superset, H2O, Serf, Alluxio / Tachyon, FakeS3

- [HashiCorp Packer templates](https://github.com/HariSekhon/Packer-templates) - Linux automated bare-metal installs and portable virtual machines OVA format appliances using HashiCorp Packer, Redhat Kickstart, Debian Preseed and Ubuntu AutoInstaller / Cloud-Init

- [Diagrams-as-Code](https://github.com/HariSekhon/Diagrams-as-Code) - Cloud & Open Source architecture diagrams with Python & D2 source code provided - automatically regenerated via GitHub Actions CI/CD - AWS, GCP, Kubernetes, Jenkins, ArgoCD, Traefik, Kong API Gateway, Nginx, Redis, PostgreSQL, Kafka, Spark, web farms, event processing...

[![Stargazers over time](https://starchart.cc/HariSekhon/Kubernetes-configs.svg)](https://starchart.cc/HariSekhon/Kubernetes-configs)

[git.io/k8s-configs](https://git.io/k8s-configs)
