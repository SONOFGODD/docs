---
title: Cofnigurar SCIM y el inicio de sesión único de SAML con Okta
intro: 'Puedes utilizar el inicio de sesión único (SSO) del Lenguaje de marcado de aserción de seguridad (SAML) y System for Cross-domain Identity Management (SCIM) con Okta para administrar automáticamente el acceso a tu organización en {% data variables.location.product_location %}.'
redirect_from:
  - /github/setting-up-and-managing-organizations-and-teams/configuring-saml-single-sign-on-and-scim-using-okta
permissions: Organization owners can configure SAML SSO and SCIM using Okta for an organization.
versions:
  ghec: '*'
topics:
  - Organizations
  - Teams
shortTitle: Configure SAML & SCIM with Okta
ms.openlocfilehash: c1b6ab48122c97cb1f805399430cc181ed3f30d1
ms.sourcegitcommit: 6185352bc563024d22dee0b257e2775cadd5b797
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/09/2022
ms.locfileid: '148192741'
---
## Acerca de SAML y SCIM con Okta

Puedes controlar el acceso a tu organización en {% data variables.location.product_location %} y a otras aplicaciones web desde una interface central si configuras dicha organización para que utilice el SSO de SAML y SCIM con Okta, un proveedor de identidad (IdP).

{% data reusables.saml.ghec-only %}

El SSO de SAML controla y asegura el acceso a los recursos organizacionales como los repositorios, informes de problemas y solicitudes de extracción. SCIM agrega, administra y elimina automáticamente el acceso a tu organización en {% data variables.location.product_location %} cuando haces cambios en Okta. Para más información, consulta «[Acerca de la administración de identidades y acceso con el inicio de sesión único de SAML](/organizations/managing-saml-single-sign-on-for-your-organization/about-identity-and-access-management-with-saml-single-sign-on)» y «[Acerca de SCIM para organizaciones](/organizations/managing-saml-single-sign-on-for-your-organization/about-scim-for-organizations)».

Después de que habilites SCIM, las siguientes características de aprovisionamiento estarán disponibles para cualquier usuario al que asignes tu aplicación de {% data variables.product.prodname_ghe_cloud %} en Okta.

| Característica | Descripción |
| --- | --- |
| Subir Usuarios Nuevos | Cuando creas un usuario nuevo en Okta, este recibirá un mensaje de correo electrónico para unirse a tu organización de {% data variables.location.product_location %}. |
| Subir Desactivaciones de Usuarios | Cuando desactivas a un usuario en Okta, Okta lo eliminará de tu organización en {% data variables.location.product_location %}. |
| Subir Actualizaciones de Perfil | Cuando actualizas el perfil de un usuario en Okta, Okta actualizará los metadatos de la membrecía de dicho usuario de tu organización en {% data variables.location.product_location %}. |
| Reactivar Usuarios | Cuando reactivas a un usuario en Okta, Okta enviará una invitación por correo electrónico al usuario para que vuelva a unirse a tu organización de {% data variables.location.product_location %}. |

Como alternativa, puedes configurar el SSO de SAML para una empresa utilizando Okta. El SCIM para cuentas empresariales solo está disponible para los usuarios administrados empresariales. Para más información, vea "[Configuración del inicio de sesión único de SAML para la empresa mediante Okta](/admin/identity-and-access-management/managing-iam-for-your-enterprise/configuring-saml-single-sign-on-for-your-enterprise-using-okta)" y "[Configuración del aprovisionamiento de SCIM para usuarios administrados Enterprise con Okta](/admin/identity-and-access-management/managing-iam-with-enterprise-managed-users/configuring-scim-provisioning-for-enterprise-managed-users-with-okta)".

## Configuración de SAML en Okta

{% data reusables.saml.okta-ae-applications-menu %} {% data reusables.saml.okta-browse-app-catalog %} {% data reusables.saml.okta-add-ghec-org-integration %}
1. Rellena el formulario y proporciona el nombre de la organización en {% data variables.product.prodname_dotcom %} y un nombre único para la aplicación de integración de aplicaciones de OAuth.
{% data reusables.saml.assign-yourself-to-okta %} {% data reusables.saml.okta-sign-on-tab %} {% data reusables.saml.okta-view-setup-instructions %}
1. Habilita y prueba el SSO de SAML en {% data variables.product.prodname_dotcom %} utilizando la URL de registro, URL del emisor, y certificados pùblicos de la guìa "Còmo configurar SAML 2.0". Para más información, vea ["Habilitación y prueba del inicio de sesión único de SAML para la organización](/organizations/managing-saml-single-sign-on-for-your-organization/enabling-and-testing-saml-single-sign-on-for-your-organization#enabling-and-testing-saml-single-sign-on-for-your-organization)".

## Configurar el aprovisionamiento de acceso con SCIM en Okta

{% data reusables.scim.dedicated-configuration-account %}

1. Inicia sesión en {% data variables.product.prodname_dotcom_the_website %} con una cuenta que sea propietaria de la organización y que se use, idealmente, solo para la configuración de SCIM.
1. Para crear una sesión activa de SAML para tu organización, ve a `https://github.com/orgs/ORGANIZATION-NAME/sso`. Para más información, vea "[Acerca de la autenticación con el inicio de sesión único de SAML](/authentication/authenticating-with-saml-single-sign-on/about-authentication-with-saml-single-sign-on#about-oauth-apps-github-apps-and-saml-sso)".
1. Ve a Okta.
{% data reusables.saml.okta-dashboard-click-applications %} {% data reusables.saml.okta-applications-click-ghec-application-label %} {% data reusables.saml.okta-provisioning-tab %} {% data reusables.saml.okta-configure-api-integration %} {% data reusables.saml.okta-enable-api-integration %}
1. Haga clic en **Autenticarse con {% data variables.product.prodname_ghe_cloud %} - Organización**.
1. A la derecha del nombre de la organización, haga clic en **Conceder**.

  ![Botón "Conceder" para autorizar la integración de SCIM de Okta a fin de acceder a la organización](/assets/images/help/saml/okta-scim-integration-grant-organization-access.png)
1. Haga clic en **Autorizar OktaOAN**.
{% data reusables.saml.okta-save-provisioning %} {% data reusables.saml.okta-edit-provisioning %}

## Información adicional

- "[Configuración del inicio de sesión único de SAML para la cuenta empresarial mediante Okta](/enterprise-cloud@latest/admin/authentication/managing-identity-and-access-for-your-enterprise/configuring-saml-single-sign-on-for-your-enterprise-using-okta)"
- [Descripción de SAML](https://developer.okta.com/docs/concepts/saml/) en la documentación de Okta
- [Descripción de SCIM](https://developer.okta.com/docs/concepts/scim/) en la documentación de Okta
