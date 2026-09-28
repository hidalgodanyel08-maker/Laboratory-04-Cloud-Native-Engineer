# Checkpoint 7 — Reflection

Your instructor requires **250–350 words**, so don't simply submit a generic reflection. You should connect it to what you actually did.

Here's a draft you can revise:

:::writing{variant="document" id="58321" title="Mission 4 Reflection"}
# Mission 4 Reflection

This laboratory activity helped me understand how containerization differs from traditional Virtual Machines and why containers are widely used in cloud-native environments. A Virtual Machine normally requires a complete guest operating system, so starting one involves booting that operating system and its associated services. A Docker container is different because it uses the host operating system kernel and packages the application and its dependencies into a lightweight environment. Because of this, a container can normally be created and started much faster than installing and booting a complete VM.

The port mapping `-p 8080:80` was necessary because the Nginx web server was listening on port 80 inside the container, while I wanted to access it through port 8080 on the host. Docker uses this mapping to forward requests from the host's port 8080 to port 80 inside the Nginx container. The `curl http://localhost:8080` command allowed me to verify that the web server was actually responding.

When `docker rm` is used, the specified stopped container is removed from Docker. The container itself and its writable container filesystem are removed, so data stored only inside that container should not be treated as permanent storage. Persistent application data should instead be stored using appropriate Docker volumes or external storage when needed.

Containerization also changes how developers and IT operations teams work together. Developers can package applications in a consistent environment, while operations teams can deploy and manage those containers using standardized tools. This supports DevOps practices by making deployment and environment management more consistent.

My GitHub portfolio is also evolving from simple cloud concepts into practical technical documentation. This laboratory added Docker commands, container deployment, lifecycle management, screenshots, and Markdown documentation. It gives me a record of both what I learned and how I performed the practical tasks.
:::

**Before submitting it, change at least a few parts to reflect your actual experience**, especially anything you encountered while using KillerCoda.

---

## Final GitHub commit

After completing the files and screenshots:

```bash
git status
