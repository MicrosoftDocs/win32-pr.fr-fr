---
title: Fonctions de Run-Time de la méthode homologue EAPHost
description: En savoir plus sur les fonctions d’exécution de l’API de méthode homologue EAPHost. Afficher une liste de fonctions et afficher des ressources supplémentaires disponibles.
ms.assetid: fdfa595d-acf7-4489-88a8-113093567fe5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3134a2b118b4bce4511e79d8d9ef58708f6b1c2bd7a93ed820fc16ec073914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118275022"
---
# <a name="eaphost-peer-method-run-time-functions"></a>Fonctions de Run-Time de la méthode homologue EAPHost

Les fonctions d’exécution de l’API de méthode d’homologue EAP sont les suivantes.



| Fonction                                                                   | Description                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)                         | Démarre une nouvelle session d’authentification sur l’homologue EAPHost.                                                                                                                                                                    |
| [**EapPeerEndSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession)                             | Met fin à une session d’authentification EAP en cours entre EAPHost et l’homologue.                                                                                                                                               |
| [**EapPeerGetConfigBlobAndUserBlob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) | Permet aux développeurs de méthodes EAP de fournir les diverses propriétés de connexion et les propriétés utilisateur prises en charge par la méthode. EAPHost appelle cette fonction pour créer la propriété de connexion et la propriété utilisateur de la méthode EAP. |
| [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity)                           | Obtient l’identité de la méthode EAP qui appelle.                                                                                                                                                                    |
| [**EapPeerGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo)                                   | Obtient un ensemble de pointeurs fonction pour une implémentation de la méthode homologue EAP chargée.                                                                                                                                     |
| [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes)       | Obtient un tableau d’attributs EAP à partir de la méthode EAP.                                                                                                                                                                     |
| [**EapPeerGetResponsePacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponsepacket)               | Obtient un paquet de réponse à partir de la méthode EAP.                                                                                                                                                                              |
| [**EapPeerGetResult**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult)                               | Obtient le résultat d’une session d’authentification à partir de la méthode EAP.                                                                                                                                                        |
| [**EapPeerGetUIContext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext)                         | Obtient le contexte de l’interface utilisateur à partir de la méthode EAP.                                                                                                                                                                     |
| [**EapPeerInitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize)                             | Initialise EAPHost pour la méthode homologue.                                                                                                                                                                                    |
| [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket)         | Traite un paquet reçu par EAPHost à partir d’un demandeur.                                                                                                                                                                   |
| [**EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials)                     | Fournit des informations d’identification utilisateur nouvelles ou mises à jour à la méthode EAP.                                                                                                                                                                 |
| [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes)       | Fournit un tableau d’attributs EAP mis à jour à la méthode EAP.                                                                                                                                                              |
| [**EapPeerSetUIContext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext)                         | Fournit un contexte d’interface utilisateur à la méthode EAP.                                                                                                                                                                        |
| [**EapPeerShutdown**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeershutdown)                                 | Arrête la méthode EAP et prépare le déchargement de la DLL correspondante.                                                                                                                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions de configuration des méthodes homologues EAPHost](eaphost-peer-method-run-time-functions.md)
</dt> </dl>

 

 




