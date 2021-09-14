---
title: Vue d’ensemble de l’API EAPHost SSO
description: Fournit une vue d’ensemble des API EAPHost qui prennent en charge l’authentification unique (SSO).
ms.assetid: 3c01d10a-9098-4965-8983-c7f65be31884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c047205946293c2116c1ab3537ad4d9250857d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915063"
---
# <a name="sso-eaphost-api-overview"></a>Vue d’ensemble de l’API EAPHost SSO

Cette rubrique fournit une vue d’ensemble des API EAPHost qui prennent en charge l’authentification unique (SSO). Pour des scénarios d’authentification unique spécifiques, consultez [scénarios EAPHost SSO](why-eaphost-sso.md).

## <a name="eaphost-enumerations"></a>Énumérations EAPHost

Les énumérations suivantes prennent en charge l’authentification unique.



| Nom                                                                    | Objectif                                                                                      |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_type de \_ champ d’entrée de configuration \_ EAP \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type)  | Définit un ensemble de types de champs d’entrée possibles disponibles lors de l’interrogation des informations d’identification de l’utilisateur.    |
| [**\_type de \_ données de l’interface utilisateur interactive EAP \_ \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type) | Spécifie les types de données de contexte d’interface utilisateur interactives fournis à certains appels d’API demandeur. |



 

## <a name="eaphost-structures"></a>Structures EAPHost

Les structures de données suivantes prennent en charge l’authentification unique.



| Nom                                                                     | Objectif                                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_données du \_ champ d’entrée de la configuration EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)   | Contient les données associées à un champ d’entrée unique.                                                                                                                         |
| [**\_tableau de \_ champs d’entrée de configuration \_ EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) | Contient un ensemble de structures de [**\_ \_ \_ \_ données de champ d’entrée de configuration EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) qui contiennent collectivement les données de champ d’entrée utilisateur obtenues auprès de l’utilisateur. |
| [**\_données de \_ l’interface utilisateur interactive EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)            | Contient des informations de configuration pour les composants d’interface utilisateur interactifs déclenchés sur un demandeur EAP.                                                                                   |
| [**\_demande EAP cred \_**](eap-cred-req.md)                                   | Contient les informations d’identification EAP anciennes et nouvelles pour les opérations de modification des informations d’identification.                                                                                               |
| [**réponse d’identification EAP \_ \_**](eap-cred-resp.md)                                 | Contient les informations d’identification EAP anciennes et nouvelles pour les opérations de modification des informations d’identification.                                                                                               |
| [**demande d’expiration d’un \_ cred EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)                    | Contient les informations d’identification EAP anciennes et nouvelles pour les opérations d’expiration des informations d’identification.                                                                                                 |
| [**réponse d’expiration d’un \_ cred EAP \_ \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))              | Contient les informations d’identification EAP anciennes et nouvelles pour les opérations d’expiration des informations d’identification.                                                                                                 |



 

## <a name="eaphost-peer-supplicant-apis"></a>API EAPHost (demandeur)

Les fonctions suivantes du demandeur prennent en charge l’authentification unique.

Les fonctions [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields) et [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) sont exclusives à SSO.



| Nom                                                                                                             | Objectif                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Ordre appelé |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields)                     | Obtient les champs d’entrée pour que les composants d’interface utilisateur interactifs soient déclenchés sur le demandeur.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 4            |
| [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)                           | Permet à l’utilisateur de déterminer quel type d’informations d’identification est requis par les méthodes pour effectuer l’authentification dans un scénario d’authentification unique.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 1            |
| [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields) | Convertit les informations utilisateur en un objet BLOB utilisateur qui peut être consommé par les fonctions d’exécution EAPHost.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 5            |
| [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields)   | Obtient un objet BLOB d’informations d’identification qui peut être utilisé pour démarrer l’authentification à partir de l’entrée utilisateur reçue par l’interface utilisateur de l’authentification unique.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 2            |
| [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)                                                       | Le demandeur utilise l’indicateur de **\_ pré-ouverture de \_ \_ session de l’indicateur EAP** pour indiquer que EAPHost doit fournir l’authentification unique. Si le code d’action [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) est retourné, EAPHost appelle [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields), puis appelle [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields)<br/> Si le code d’action [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) n’est pas retourné, EAPHost passe à la séquence d’appel standard non SSO. Pour plus d’informations, voir séquence d’appel de l' [API demandeur](supplicant-api-call-sequence.md).<br/> | 3            |



 

## <a name="eaphost-peer-method-apis"></a>API de méthode homologue EAPHost

Les fonctions homologues suivantes prennent en charge l’authentification unique.

Les fonctions [**EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields) et [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) sont exclusives à SSO.



| Nom                                                                                                      | Objectif                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Ordre appelé |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)                      | Définit l’implémentation d’une API de méthode EAP qui fournit les champs d’entrée pour que les composants d’interface utilisateur interactifs soient déclenchés sur le demandeur.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 4            |
| [**EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields)                            | Définit l’implémentation d’une fonction spécifique à la méthode EAP qui obtient les champs d’entrée d’informations d’identification SSO EAP pour cette méthode EAP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | 1            |
| [**EapPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuiblobfrominteractiveuiinputfields)  | Convertit les informations utilisateur en un objet BLOB utilisateur qui peut être consommé par les fonctions d’exécution EAPHost.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | 5            |
| [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) | Définit l’implémentation d’une fonction de méthode EAP qui obtient les données d’objet BLOB de l’utilisateur fournies par l’interface utilisateur SSO interactive générée sur le demandeur.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | 2            |
| [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)                                                        | L’indicateur de **\_ pré-ouverture de \_ \_ session de l’indicateur EAP** indique qu’EAPHost doit fournir l’authentification unique. Dans un scénario d’authentification unique, si le code d’action **EapPeerResponseInvokeUI** est retourné, EAPHost appelle [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields), puis appelle [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields)<br/> Si le code d’action **EapPeerResponseInvokeUI** n’est pas retourné, EAPHost passe à la séquence d’appel standard non SSO. Pour plus d’informations, consultez séquence d’appel de l' [API de méthode homologue](peer-method-api-call-sequence.md).<br/> | 3            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[SSO et PLAP](understanding-sso-and-plap.md)
</dt> <dt>

[Scénarios d’authentification unique EAPHost](why-eaphost-sso.md)
</dt> </dl>

 

