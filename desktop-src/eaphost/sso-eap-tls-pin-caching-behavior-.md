---
title: Comportement de mise en cache du code confidentiel EAP-TLS SSO
description: Fournit une approche étape par étape pour résoudre les problèmes de reprise de session et de réauthentification d’un utilisateur itinérant dans un environnement EAP-TLS SSO.
ms.assetid: aeded6c9-315d-4115-9750-485f017dd8dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8bc8cb112a6def55085cbd0b94068407320e4116a4b0161d7d923319257258f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085883"
---
# <a name="sso-eap-tls-pin-caching-behavior"></a>Comportement de mise en cache du code confidentiel EAP-TLS SSO

Cette rubrique fournit une approche étape par étape pour résoudre les problèmes de reprise de session et de réauthentification d’un utilisateur itinérant dans un environnement EAP-TLS SSO.

## <a name="step-by-step-approach"></a>Approche étape par étape

La liste suivante représente une approche étape par étape pour résoudre les problèmes de reprise de session et de réauthentification d’un utilisateur itinérant dans un environnement EAP-TLS SSO.

-   Après la première authentification réussie dans un environnement SSO avec EAP-TLS, le demandeur conserve par défaut toutes les informations relatives aux informations d’identification de l’utilisateur.
    > [!Note]  
    > Bien que soumis à l’implémentation de demandeur particulière, il est recommandé au demandeur de conserver la structure de [**\_ tableau de \_ \_ champs d’entrée de configuration EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) complète que le demandeur a utilisé en dernier dans l’appel [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) à EAPHost.

     

-   À mesure que l’utilisateur se déplace pour la première fois et que la réauthentification commence, le demandeur appelle à nouveau [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) avec la même structure de [**tableau de \_ \_ \_ champs d’entrée de configuration EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) ; le demandeur doit également passer le même objet blob d’utilisateur conservé après la première authentification réussie.
-   EAPHost transmet ensuite les informations de l’objet BLOB utilisateur à la méthode EAP.
-   La méthode EAP met à jour à son tour l’objet BLOB de l’utilisateur avec les champs d’informations d’identification, le code confidentiel par exemple fourni dans *pEapConfigInputFieldArray*, et conserve les valeurs restantes, le certificat de serveur, par exemple, tel qu’il était dans l’objet blob d’origine de l’utilisateur.
-   Une fois ces étapes terminées, le demandeur peut reprendre l’authentification de manière normale en appelant la fonction runtime [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) avec cet objet blob d’utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Scénarios d’authentification unique EAPHost](why-eaphost-sso.md)
</dt> <dt>

[SSO et PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




