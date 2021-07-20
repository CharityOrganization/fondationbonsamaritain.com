1. Navegue por onde seu runner auto-hospedado está registrado:
   * **Em uma organização ou repositório**: navegue até a página principal e clique em {% octicon "gear" aria-label="The Settings gear" %} **Configurações**.
   * {% if currentVersion == "free-pro-team@latest" %}**If using an enterprise account**: navigate to your enterprise account by visiting `https://github.com/enterprises/ENTERPRISE-NAME`, replacing `ENTERPRISE-NAME` with your enterprise account's name.{% else if currentVersion != "free-pro-team@latest" and currentVersion ver_gt "enterprise-server@2.21" %}**If using an enterprise-level runner**:

     1. No canto superior direito de qualquer página, clique em {% octicon "rocket" aria-label="The rocket ship" %}.
     1. In the left sidebar, click **Enterprise overview**.
     1. {% endif %} In the enterprise sidebar, {% octicon "law" aria-label="The law icon" %} **Policies**.
1. Navegue até as configurações {% data variables.product.prodname_actions %}:
   * **Em uma organização ou um repositório**: clique em **Ações** na barra lateral esquerda.

     ![Configuração de ações](/assets/images/help/settings/settings-sidebar-actions.png)
   * {% if currentVersion == "free-pro-team@latest" %}**If using an enterprise account**{% else if currentVersion != "free-pro-team@latest" and currentVersion ver_gt "enterprise-server@2.21" %}**If using an enterprise-level runner**{% endif %}: click **Actions** under "{% octicon "law" aria-label="The law icon" %} Policies".
