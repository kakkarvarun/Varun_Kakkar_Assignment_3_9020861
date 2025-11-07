# cdevops-gitea
k8s gitea lab to take dev (sqlite based) to prod (mysql based)

TLDR;

```bash
pip install ansible kubernetes
git submodule update --init --recursive
ansible-playbook up.yml
```

Wait until `kubectl get pod` shows all pods running and:

```bash
kubectl port-forward svc/gitea-http 3000:3000
```

Now you should be able to access gitea in development mode.

The challenge is to run this in production mode.

### Points to Cover

## Marking

|Item|Out Of|
|--|--:|
|use [the gitea helm](https://gitea.com/gitea/helm-gitea) to make the repository data persistent|3|
|make gitea use external database|1|
|Expose your gitea instance publically|3|
|make the README easy to use and ACCURATE|3|
|||
|total|10|
