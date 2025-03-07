---
title: Senden von Unternehmensbeiträgen an dein GitHub.com-Profil
intro: You can highlight your work on {% data variables.product.prodname_enterprise %} by sending the contribution counts to your {% data variables.product.prodname_dotcom_the_website %} profile.
redirect_from:
- /articles/sending-your-github-enterprise-contributions-to-your-github-com-profile
- /articles/sending-your-github-enterprise-server-contributions-to-your-github-com-profile
- /articles/sending-your-github-enterprise-server-contributions-to-your-githubcom-profile
- /github/setting-up-and-managing-your-github-profile/sending-your-github-enterprise-server-contributions-to-your-githubcom-profile
- /github/setting-up-and-managing-your-github-profile/managing-contribution-graphs-on-your-profile/sending-your-github-enterprise-server-contributions-to-your-githubcom-profile
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
- Profiles
shortTitle: Send enterprise contributions
ms.openlocfilehash: 19b26c9e274b66df16434727e42c5c291bacfea7
ms.sourcegitcommit: 67064b14c9d4d18819db8f6398358b77a1c8002a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2022
ms.locfileid: "145090036"
---
## <a name="about-enterprise-contributions-on-your--data-variablesproductprodname_dotcom_the_website--profile"></a>Informationen zu Unternehmensbeiträgen zu deinem {% data variables.product.prodname_dotcom_the_website %}-Profil

In deinem {% data variables.product.prodname_dotcom_the_website %}-Profil wird die Anzahl der {% ifversion fpt or ghec %}{% data variables.product.prodname_enterprise %}{% else %}{% data variables.product.product_name %}{% endif %}-Beiträge der letzten 90 Tage angezeigt. Die {% data reusables.github-connect.sync-frequency %}-Beiträge von {% ifversion fpt or ghec %}{% data variables.product.prodname_enterprise %}{% else %}{% data variables.product.product_name %}{% endif %} gelten als private Beiträge. Die Commitdetails enthalten nur die Beitragsanzahl und dass diese Beiträge in einer {% data variables.product.prodname_enterprise %}-Umgebung außerhalb von {% data variables.product.prodname_dotcom_the_website %} vorgenommen wurden.

Du entscheidest, ob die Anzahl privater Beiträge auf deinem Profil angezeigt werden soll. Weitere Informationen findest du unter [Veröffentlichen oder Ausblenden deiner privaten Beiträge in deinem Profil](/articles/publicizing-or-hiding-your-private-contributions-on-your-profile/).

Weitere Informationen dazu, wie Beiträge berechnet werden, findest du unter [Verwalten von Beitragsdiagrammen auf deinem Profil](/articles/managing-contribution-graphs-on-your-profile/).

{% note %}

**Hinweise:**
- Die Verbindungen zwischen deinen Konten werden durch die [Datenschutzbestimmungen von GitHub](/free-pro-team@latest/github/site-policy/github-privacy-statement/) geregelt, und Benutzer*innen, die solche Verbindungen erlauben, sind mit den [Nutzungsbedingungen von GitHub](/free-pro-team@latest/github/site-policy/github-terms-of-service) einverstanden.

- Damit du dein {% ifversion fpt or ghec %}{% data variables.product.prodname_enterprise %}{% else %}{% data variables.product.product_name %}{% endif %}-Profil mit deinem {% data variables.product.prodname_dotcom_the_website %}-Profil verbinden kannst, muss der Unternehmensbesitzer {% data variables.product.prodname_github_connect %} aktivieren und die Beitragsfreigabe zwischen den Umgebungen aktivieren. Für weitere Informationen hierzu wendest du dich an deinen Unternehmensbesitzer.

{% endnote %}

## <a name="sending-your-enterprise-contributions-to-your--data-variablesproductprodname_dotcom_the_website--profile"></a>Senden von Unternehmensbeiträgen zu deinem {% data variables.product.prodname_dotcom_the_website %}-Profil

{% ifversion fpt or ghec %}

- Informationen zum Senden von Unternehmensbeiträgen von {% data variables.product.prodname_ghe_server %} an dein {% data variables.product.prodname_dotcom_the_website %}-Profil findest du unter [Senden von Unternehmensbeiträgen an dein {% data variables.product.prodname_dotcom_the_website %}-Profil](/enterprise-server/account-and-profile/setting-up-and-managing-your-github-profile/managing-contribution-graphs-on-your-profile/sending-enterprise-contributions-to-your-githubcom-profile) in der Dokumentation zu {% data variables.product.prodname_ghe_server %}.
- Informationen zum Senden von Unternehmensbeiträgen von {% data variables.product.prodname_ghe_managed %} an dein {% data variables.product.prodname_dotcom_the_website %}-Profil findest du unter [Senden von Unternehmensbeiträgen an dein {% data variables.product.prodname_dotcom_the_website %}-Profil](/github-ae@latest/account-and-profile/setting-up-and-managing-your-github-profile/managing-contribution-graphs-on-your-profile/sending-enterprise-contributions-to-your-githubcom-profile) in der Dokumentation zu {% data variables.product.prodname_ghe_managed %}.

{% elsif ghes %}

1. Melde dich bei {% data variables.product.prodname_ghe_server %} und {% data variables.product.prodname_dotcom_the_website %} an.
1. Klicke rechts oben auf einer {% data variables.product.prodname_ghe_server %}-Seite auf dein Profilfoto und dann auf **Einstellungen**.
   ![Symbol „Einstellungen“ auf der Benutzerleiste](/assets/images/help/settings/userbar-account-settings.png) {% data reusables.github-connect.github-connect-tab-user-settings %} {% data reusables.github-connect.connect-dotcom-and-enterprise %}
1. Überprüfe die Ressourcen, auf die {% data variables.product.prodname_ghe_server %} von deinem {% data variables.product.prodname_dotcom_the_website %}-Konto zugreifen wird, und klicke dann auf **Autorisieren**.
   ![Autorisieren der Verbindung zwischen GitHub Enterprise Server und GitHub.com](/assets/images/help/settings/authorize-ghe-to-connect-to-dotcom.png) {% data reusables.github-connect.send-contribution-counts-to-githubcom %}

{% elsif ghae %}

1. Melde dich bei {% data variables.product.prodname_ghe_managed %} und {% data variables.product.prodname_dotcom_the_website %} an.
1. Klicke rechts oben auf einer {% data variables.product.prodname_ghe_managed %}-Seite auf dein Profilfoto und dann auf **Einstellungen**.
   ![Symbol „Einstellungen“ auf der Benutzerleiste](/assets/images/help/settings/userbar-account-settings.png) {% data reusables.github-connect.github-connect-tab-user-settings %} {% data reusables.github-connect.connect-dotcom-and-enterprise %} {% data reusables.github-connect.authorize-connection %} {% data reusables.github-connect.send-contribution-counts-to-githubcom %}

{% endif %}
