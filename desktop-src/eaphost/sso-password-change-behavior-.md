---
title: Comportement de modification du mot de passe SSO
description: Fournit une approche pas à pas pour résoudre le comportement de modification du mot de passe SSO.
ms.assetid: c52ffeb8-ecee-4398-a7df-388b523c737c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005fe5191b3bdccf2bb1643be50817a3b0405336
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "106536884"
---
# <a name="sso-password-change-behavior"></a>Comportement de modification du mot de passe SSO

Cette rubrique fournit une approche étape par étape pour résoudre le comportement de modification du mot de passe SSO.

## <a name="step-by-step-approach"></a>Approche étape par étape

La liste suivante représente une approche étape par étape pour la résolution du comportement de modification du mot de passe SSO.

-   Une fois que la méthode EAP est notifiée d’une modification de mot de passe, la méthode notifie EAPHost ; EAPHost notifie à son tour le demandeur en retournant le code d’action, [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).
-   Après avoir reçu le code d’action [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) d’EAPHost, le demandeur obtient le contexte de l’interface utilisateur à partir de la méthode EAP en appelant la fonction [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext) ; EAPHost obtient ensuite le contexte de l’interface utilisateur à partir de la méthode EAP en appelant la fonction de méthode correspondante
-   Le demandeur passe le contexte de l’interface utilisateur au processus d’interface utilisateur (à l’aide d’une forme de communication inter-processus).
-   Le processus d’interface utilisateur appelle [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) sur EAPHost.
-   EAPHost collecte le contexte de l’interface utilisateur en appelant [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields) sur la méthode EAP.
-   La méthode EAP fournit toutes les informations de contexte d’interface utilisateur nécessaires dans la structure de données de l' [**\_ \_ interface utilisateur \_ interactive EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) , où *DwDataType* a la valeur *EapCredExpiryReq* et *pbUiData* pointe vers une structure de type [**EAP \_ cred \_ req**](eap-cred-req.md).
-   Lors du remplissage de la structure de données de l' [**\_ \_ \_ interface utilisateur interactive EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) , cette méthode EAP ne renseigne que le paramètre *curCreds* et ne définit pas l’indicateur de [**\_ \_ \_ \_ \_ lecture \_ seule des champs d’entrée de l’interface utilisateur EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) dans la structure de **\_ \_ \_ \_ données du champ d’entrée de la configuration EAP** .
    > [!Note]  
    > L’indicateur de [**\_ \_ \_ \_ \_ lecture \_ seule des champs d’entrée de l’interface utilisateur EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) concerne les champs de membre qui doivent être modifiés.

     

-   Après avoir collecté le contexte de l’interface utilisateur informtion, le processus de l’interface utilisateur affiche une interface utilisateur pour collecter les informations de mot de passe de modification de l’utilisateur. Ces informations sont renseignées dans le paramètre *NewCreds* de la structure de [**demande d’expiration d' \_ \_ expiration \_ du protocole EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req) .
-   Le processus d’interface utilisateur transmet la structure de [**\_ \_ réponse EAP cred**](eap-cred-resp.md) à EAPHost via [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields).
-   Le processus d’interface utilisateur transmet cet objet BLOB d’utilisateur au demandeur, et le demandeur continue les fonctions d’exécution EAPHost comme d’habitude.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Scénarios d’authentification unique EAPHost](why-eaphost-sso.md)
</dt> <dt>

[SSO et PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




