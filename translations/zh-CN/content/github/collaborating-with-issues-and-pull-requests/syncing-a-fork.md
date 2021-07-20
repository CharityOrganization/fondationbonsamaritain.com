---
title: 同步复刻
intro: 同步仓库的复刻以通过上游仓库使其保持最新。
redirect_from:
  - /articles/syncing-a-fork
versions:
  free-pro-team: '*'
  enterprise-server: '*'
---

必须在 Git 中[配置指向上游仓库的远程仓库](/articles/configuring-a-remote-for-a-fork)，然后才能将您的复刻与上游仓库同步。

{% data reusables.command_line.open_the_multi_os_terminal %}
2. 将当前工作目录更改为您的本地仓库。
3. 从上游仓库获取分支及其各自的提交。 对 `master` 的提交将存储在本地分支 `upstream/master` 中。
  ```shell
  $ git fetch upstream
  > remote: Counting objects: 75, done.
  > remote: Compressing objects: 100% (53/53), done.
  > remote: Total 62 (delta 27), reused 44 (delta 9)
  > Unpacking objects: 100% (62/62), done.
  > From https://{% data variables.command_line.codeblock %}/<em>ORIGINAL_OWNER</em>/<em>ORIGINAL_REPOSITORY</em>
  >  * [new branch]      main     -> upstream/main
  ```
4. Check out your fork's local `main` branch.
  ```shell
  $ git checkout main
  > Switched to branch 'main'
  ```
5. Merge the changes from `upstream/main` into your local `main` branch. This brings your fork's `main` branch into sync with the upstream repository, without losing your local changes.
  ```shell
  $ git merge upstream/main
  > Updating a422352..5fdff0f
  > Fast-forward
  >  README                    |    9 -------
  >  README.md                 |    7 ++++++
  >  2 files changed, 7 insertions(+), 9 deletions(-)
  >  delete mode 100644 README
  >  create mode 100644 README.md
  ``` If your local branch didn't have any unique commits, Git will instead perform a "fast-forward":
  ```shell
  $ git merge upstream/main
  > Updating 34e91da..16c56ad
  > Fast-forward
  >  README.md                 |    5 +++--
  >  1 file changed, 3 insertions(+), 2 deletions(-)
  ```

{% tip %}

**提示**：同步复刻仅更新仓库的本地副本。 要在 {% data variables.product.product_location %} 上更新复刻，您必须[推送更改](/articles/pushing-commits-to-a-remote-repository/)。

{% endtip %}
