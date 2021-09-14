---
title: Fonctions de configuration des méthodes homologues EAPHost
description: En savoir plus sur les fonctions de configuration des méthodes homologues EAPHost. Consultez la liste des fonctions de configuration et affichez les ressources disponibles supplémentaires.
ms.assetid: ba5c90b2-5185-4810-84a2-d08e62e8105c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3081f8a54482c48c7c506a25bfaf7f18cf3193ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127221452"
---
# <a name="eaphost-peer-method-configuration-functions"></a>Fonctions de configuration des méthodes homologues EAPHost

Les fonctions de configuration de l’API de méthode d’homologue EAP sont les suivantes.



| Fonction                                                                                                  | Description                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapPeerConfigBlob2Xml**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerconfigblob2xml)                                                    | Convertit l’objet blob de configuration au format XML.                                                                                                                                                                                                                          |
| [**EapPeerConfigXml2Blob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerconfigxml2blob)                                                    | Convertit le code XML en objet blob de configuration.                                                                                                                                                                                                                        |
| [**EapPeerCredentialsXml2Blob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeercredentialsxml2blob)                                          | Convertit les informations d’identification XML en objet BLOB.                                                                                                                                                                                                                            |
| [**EapPeerFreeErrorMemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory)                                                  | Libère toutes les mémoires spécifiques aux erreurs EAP retournées par les API homologues EapHost.                                                                                                                                                                                               |
| [**EapPeerFreeMemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreememory)                                                            | Libère toute la mémoire allouée par les paramètres de sortie de la méthode EAP.                                                                                                                                                                                                      |
| [**EapPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeconfigui)                                                    | Déclenche la boîte de dialogue de l’interface utilisateur de configuration de connexion spécifique à la méthode EAP sur le client.                                                                                                                                                                   |
| [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui)                                                | Déclenche une boîte de dialogue d’interface utilisateur interactive personnalisée pour obtenir les informations d’identité de l’utilisateur pour la méthode EAP sur le client.                                                                                                                                          |
| [**EapPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeinteractiveui)                                          | Déclenche une boîte de dialogue d’interface utilisateur interactive personnalisée pour la méthode EAP sur le client.                                                                                                                                                                              |
| [**EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields)                            | Définit l’implémentation d’une fonction spécifique à la méthode EAP qui obtient les champs d’entrée d’informations d’identification pour l’authentification unique (SSO) EAP pour cette méthode EAP.                                                                                                              |
| [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)                      | Définit l’implémentation d’une fonction de demandeur EAP qui obtient les champs d’entrée pour que les composants d’interface utilisateur interactifs soient déclenchés sur le demandeur.                                                                                                     |
| [**EapPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuiblobfrominteractiveuiinputfields)  | Convertit les informations utilisateur en un objet BLOB utilisateur qui peut être consommé par les fonctions d’exécution EAPHost.                                                                                                                                                                   |
| [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) | Définit l’implémentation d’une fonction spécifique à la méthode EAP qui génère un objet blob d’informations d’identification d’utilisateur EAP à partir d’une structure de [**\_ \_ \_ \_ tableau de champs d’entrée de configuration EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) qui contient les données d’identification fournies par un utilisateur demandeur. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions de Run-Time de la méthode homologue EAPHost](eaphost-peer-method-run-time-functions.md)
</dt> </dl>

 

 




