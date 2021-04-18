---
title: Fonctions de méthode de l’authentificateur EAPHost
description: En savoir plus sur les fonctions d’API de méthode d’authentificateur EAPHost, telles que EapMethodAuthenticatorFreeErrorMemory.
ms.assetid: 319516ee-b21d-4375-8c90-e3abe0a457e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93fac5114085fe6c620084d564bbff97cc3b4535
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106512340"
---
# <a name="eaphost-authenticator-method-functions"></a>Fonctions de méthode de l’authentificateur EAPHost

Les fonctions de l’API de la méthode d’authentificateur EAPHost sont les suivantes.



| Fonction                                                                                               | Description                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapMethodAuthenticatorBeginSession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession)                       | Crée une nouvelle session d’authentification EAP sur le serveur EAPHost.                                                                                                                             |
| [**EapMethodAuthenticatorEndSession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorendsession)                           | Ferme une session d’authentification EAP sur le serveur EAPHost.                                                                                                                                 |
| [**EapMethodAuthenticatorFreeErrorMemory**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorfreeerrormemory)                 | Libère la mémoire spécifique aux erreurs allouée par la méthode d’authentificateur EAP.                                                                                                                   |
| [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes)                     | Obtient un tableau d’attributs d’authentification EAP à partir de la méthode d’authentificateur EAP.                                                                                                        |
| [**EapMethodAuthenticatorGetInfo**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetinfo)                                 | Obtient un ensemble de pointeurs fonction pour une implémentation de la méthode d’authentificateur EAP chargée.                                                                                            |
| [**EapMethodAuthenticatorGetResult**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetresult)                             | Obtient le résultat de l’authentification à partir de la méthode d’authentificateur EAP.                                                                                                                        |
| [**EapMethodAuthenticatorInitialize**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorinitialize)                           | Initialise une méthode d’authentificateur EAP pour le serveur EAPHost.                                                                                                                             |
| [**EapMethodAuthenticatorInvokeConfigUI**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorinvokeconfigui)                   | Définit une fonction qui déclenche la boîte de dialogue interface utilisateur de configuration de connexion de la méthode EAP sur le client.                                                                           |
| [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket)                     | Traite un paquet d’authentification EAP reçu par le serveur EAPHost et retourne une action de réponse.                                                                                        |
| [**EapMethodAuthenticatorSendPacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket)                           | Obtient un paquet d’authentification à partir de la méthode d’authentificateur EAP à envoyer au demandeur.                                                                                               |
| [**EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes)                     | Fournit des attributs d’authentification EAP mis à jour à définir sur la méthode d’authentificateur EAP.                                                                                                      |
| [**EapMethodAuthenticatorShutdown**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorshutdown)                               | Arrête la méthode de l’authentificateur EAP et prépare son déchargement à partir du serveur EAPHost.                                                                                                  |
| [**EapMethodAuthenticatorUpdateInnerMethodParams**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorupdateinnermethodparams) | Met à jour les paramètres de session d’authentification EAP précédents établis par un appel à [**EapMethodAuthenticatorBeginSession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession) à partir du serveur EAPHost. |



 

 

 




