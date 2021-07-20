---
title: Condições para arquivos grandes
intro: 'O {% data variables.product.product_name %} limita o tamanho dos arquivos permitidos nos repositórios e irá bloquear um push para um repositório se os arquivos forem maiores que o limite máximo de arquivos.'
redirect_from:
  - /articles/conditions-for-large-files
versions:
  free-pro-team: '*'
  enterprise-server: '*'
---

{% data reusables.large_files.use_lfs_tip %}

### Aviso para arquivos maiores que {% data variables.large_files.warning_size %}

Se você tentar adicionar ou atualizar um arquivo maior do que {% data variables.large_files.warning_size %}, você receberá um aviso do Git. As alterações ainda serão carregadas no seu repositório com sucesso, mas você pode considerar remover o commit para minimizar o impacto no desempenho. Para obter mais informações, consulte "[Remover arquivos do histórico de um repositório](/github/managing-large-files/removing-files-from-a-repositorys-history)".

### Pushes bloqueados para arquivos grandes

{% if currentVersion != "free-pro-team@latest" %}Por padrão, blocos do {% endif %}{% data variables.product.product_name %} fazem pushes que excedem {% data variables.large_files.max_github_size %}. {% if currentVersion != "free-pro-team@latest" %}No entanto, um administrador do site pode configurar um limite diferente para a sua instância de {% data variables.product.prodname_ghe_server %}. Para obter mais informações, consulte "[Definir limites de push do Git](/enterprise/{{ currentVersion }}/admin/guides/installation/setting-git-push-limits)".{% endif %}
