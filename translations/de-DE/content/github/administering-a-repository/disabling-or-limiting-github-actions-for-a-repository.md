---
title: GitHub-Aktionen für ein Repository deaktivieren oder limitieren
intro: 'Repository-Inhaber können {% data variables.product.prodname_actions %} für ein bestimmtes Repository deaktivieren, aktivieren und limitieren.'
versions:
  free-pro-team: '*'
  enterprise-server: '>=2.22'
---

{% data reusables.actions.enterprise-beta %}
{% data reusables.actions.enterprise-github-hosted-runners %}

### Über {% data variables.product.prodname_actions %}-Berechtigungen für Dein Repository

{% data reusables.github-actions.disabling-github-actions %} Weitere Informationen zu {% data variables.product.prodname_actions %} findest Du unter „[Über {% data variables.product.prodname_actions %}](/actions/getting-started-with-github-actions/about-github-actions)."

Du kannst {% data variables.product.prodname_actions %} für Dein Repository aktivieren. {% data reusables.github-actions.enabled-actions-description %} Du kannst {% data variables.product.prodname_actions %} für Dein Repository komplett deaktivieren. {% data reusables.github-actions.disabled-actions-description %}

Alternativ kannst Du {% data variables.product.prodname_actions %} in Deinem Repository aktivieren, aber die Aktionen limitieren, die ein Workflow ausführen kann. {% data reusables.github-actions.enabled-local-github-actions %}

### {% data variables.product.prodname_actions %}-Berechtigungen für Dein Repository verwalten

{% note %}

**Note:** You might not be able to manage these settings if your organization has an overriding policy or is managed by an enterprise account that has overriding policy. For more information, see "[Disabling or limiting {% data variables.product.prodname_actions %} for your organization](/github/setting-up-and-managing-organizations-and-teams/disabling-or-limiting-github-actions-for-your-organization)" or "[Enforcing {% data variables.product.prodname_actions %} policies in your enterprise account](/github/setting-up-and-managing-your-enterprise-account/enforcing-github-actions-policies-in-your-enterprise-account)."

{% endnote %}

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-settings %}
{% data reusables.repositories.settings-sidebar-actions %}
4. Wähle unter „Actions permissions" (Berechtigungen für Aktionen) eine Option aus. ![Aktiviere, deaktiviere oder limitiere die Aktionen für dieses Repository](/assets/images/help/repository/enable-repo-actions.png)

{% if currentVersion == "free-pro-team@latest" or currentVersion ver_gt "enterprise-server@2.22" %}
### Enabling workflows for private repository forks

{% data reusables.github-actions.private-repository-forks-overview %}

#### Configuring the private fork policy for a repository

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-settings %}
{% data reusables.repositories.settings-sidebar-actions %}
{% data reusables.github-actions.private-repository-forks-configure %}
{% endif %}
