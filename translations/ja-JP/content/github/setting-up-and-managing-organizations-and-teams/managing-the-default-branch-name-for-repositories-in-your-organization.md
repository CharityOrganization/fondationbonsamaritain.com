---
title: Organization のリポジトリのデフォルブランチ名を管理する
intro: Organization でメンバーが作成するリポジトリについて、デフォルトブランチ名を設定できます。
versions:
  free-pro-team: '*'
  enterprise-server: '>=2.23'
---

### デフォルトブランチ名について

Organization のメンバーが新しいリポジトリを作成するとき、{% data variables.product.prodname_dotcom %} はブランチを 1 つ作成し、それをリポジトリのデフォルトブランチに設定します。 {% data variables.product.prodname_dotcom %} は現在、デフォルトブランチに `master` という名前を付けまが、開発環境でわかりやすいようにデフォルトブランチには任意の名前を設定することができます。

{% data reusables.branches.set-default-branch %}

{% data reusables.branches.rename-existing-branch %}

### デフォルトブランチ 名を設定する

{% data reusables.profile.access_profile %}
{% data reusables.profile.access_org %}
{% data reusables.organizations.org_settings %}
{% data reusables.organizations.repository-defaults %}
3. [Repository default branch] で、[**Change default branch name now**] をクリックします。 ![[Override] ボタン](/assets/images/help/organizations/repo-default-name-button.png)
    {% note %}

    **ノート:** Enterprise オーナーがデフォルト名についてポリシーを施行している場合、ここでデフォルト名を変更することはできません。 個々のリポジトリでデフォルトブランチを設定することは可能です。 詳しい情報については、「[デフォルトブランチ名に関するポリシーを施行する](/github/setting-up-and-managing-your-enterprise-account/enforcing-repository-management-policies-in-your-enterprise-account#enforcing-a-policy-on-the-default-branch-name)」と「[デフォルトブランチを設定する](/github/administering-a-repository/setting-the-default-branch)」を参照してください。

    {% endnote %}
4. 新しいブランチに使用したいデフォルト名を入力します。 ![デフォルト名を入力するテキストフィールド](/assets/images/help/organizations/repo-default-name-text.png)
5. [**Update**] をクリックします。 ![[Update] ボタン](/assets/images/help/organizations/repo-default-name-update.png)

### 参考リンク

- [リポジトリのデフォルトブランチ名を管理する](/github/setting-up-and-managing-your-github-user-account/managing-the-default-branch-name-for-your-repositories)
