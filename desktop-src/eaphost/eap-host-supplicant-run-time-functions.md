---
title: Fonctions Run-Time du demandeur EAPHost
description: En savoir plus sur les fonctions d’exécution du demandeur EAPHost, telles que EapHostPeerBeginSession et EapHostPeerGetResult.
ms.assetid: b1c473ba-9a12-4929-b4d0-27262117e9c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2bbb6aee83cff6354877b661acb7f3389f5b77b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127221500"
---
# <a name="eaphost-supplicant-run-time-functions"></a>Fonctions Run-Time du demandeur EAPHost

Les fonctions d’exécution de l’API du demandeur EAP sont les suivantes.



| Fonction                                                                     | Description                                                                                                                                                                                                          |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)                   | Démarre une session d’authentification EAP.                                                                                                                                                                                |
| [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection)             | Arrête tous les rappels futurs vers le [**NotificationHandler**](/previous-versions/windows/desktop/api) fourni par le demandeur appelant vers EAPHost dans un appel précédent à [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession). |
| [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession)                       | Met fin à une session d’authentification EAP en cours entre EAPHost et le demandeur appelant.                                                                                                                          |
| [**EapHostPeerFreeEapError**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror)                   | Libère toutes les mémoires spécifiques aux erreurs EAP retournées par les API EAPHost.                                                                                                                                                        |
| [**EapHostFreeRuntimeMemory**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreememory)                    | Libère l’espace mémoire utilisé par les API d’exécution.                                                                                                                                                                         |
| [**EapHostPeerGetAuthStatus**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus)                 | Obtient l’état d’authentification EAP actuel du demandeur à partir d’EAPHost.                                                                                                                                             |
| [**EapHostPeerGetIdentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity)                     | Demande des informations d’identité à partir des méthodes internes.                                                                                                                                                                |
| [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes) | Obtient un tableau d’attributs d’authentification EAP à partir d’EAPHost.                                                                                                                                                      |
| [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult)                         | Obtient le résultat de l’authentification pour la session d’authentification EAP spécifiée.                                                                                                                                      |
| [**EapHostPeerGetSendPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetsendpacket)                 | Obtient un paquet d’EAPHost à envoyer à l’authentificateur.                                                                                                                                                          |
| [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)                   | Obtient le contexte de l’interface utilisateur pour le demandeur à partir d’EAPHost qui est utilisé dans les API [**EapHostPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) pour le demandeur.                             |
| [**EapHostPeerInitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize)                       | Initialise EAPHost pour le demandeur. [**EapHostInitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize) et [**EapHostUninitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize) doivent être appelés en tant que paire.                                      |
| [**EapHostPeerProcessReceivedPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket) | Transfère le paquet EAP vers EAPHost après avoir reçu un paquet EAP du serveur.                                                                                                                             |
| [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) | Fournit des attributs d’authentification EAP mis à jour à EAPHost.                                                                                                                                                           |
| [**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext)                   | Fournit un contexte d’interface utilisateur nouveau ou mis à jour à la méthode d’homologue EAP chargée sur EAPHost.                                                                                                                           |
| [**EapHostPeerUninitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize)                   | Unitializes EapHost pour le demandeur. [**EapHostInitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize) et [**EapHostUninitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize) doivent être appelés en tant que paire.                                      |



 

 

 




