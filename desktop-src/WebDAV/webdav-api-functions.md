---
title: Fonctions de l’API WebDAV
description: Les fonctions suivantes sont utilisées dans l’API WebDAV.
ms.assetid: 489cdc17-aca8-4621-bc61-f0f3b9ac22b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 401f527bcd98f86f8116df5b25ba1ea71e0f432e19dc89eae00582a2a0b4865e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995039"
---
# <a name="webdav-api-functions"></a>Fonctions de l’API WebDAV

Les fonctions suivantes sont utilisées dans l’API WebDAV.



| Fonction                                                             | Description                                                                                                                                                                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DavAddConnection**](/windows/desktop/api/davclnt/nf-davclnt-davaddconnection)                         | Crée une connexion sécurisée à un serveur WebDAV ou à un fichier ou répertoire distant sur un serveur WebDAV.                                                                                                                                   |
| [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback)                                | Le client WebDAV appelle la fonction de rappel [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) définie par l’application pour inviter l’utilisateur à fournir des informations d’identification.                                                                                           |
| [**DavCancelConnectionsToServer**](/windows/desktop/api/davclnt/nf-davclnt-davcancelconnectionstoserver) | Ferme toutes les connexions à un serveur WebDAV ou à un fichier ou répertoire distant sur un serveur WebDAV.                                                                                                                                        |
| [**DavDeleteConnection**](/windows/desktop/api/davclnt/nf-davclnt-davdeleteconnection)                   | Ferme une connexion qui a été créée à l’aide de la fonction [**DavAddConnection**](/windows/desktop/api/davclnt/nf-davclnt-davaddconnection) .                                                                                                                              |
| [**DavFlushFile**](/windows/desktop/api/davclnt/nf-davclnt-davflushfile)                                 | Vide les données de la version locale d’un fichier distant sur le serveur WebDAV.                                                                                                                                                        |
| [*DavFreeCredCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback_freecred)                        | Le client WebDAV appelle la fonction de rappel [*DavFreeCredCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback_freecred) définie par l’application pour libérer les informations d’identification qui ont été récupérées par la fonction de rappel [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) . |
| [**DavGetExtendedError**](/windows/desktop/api/davclnt/nf-davclnt-davgetextendederror)                   | Récupère les informations de code d’erreur étendues retournées par le serveur WebDAV pour l’opération d’e/s précédente ayant échoué.                                                                                                                  |
| [**DavGetHTTPFromUNCPath**](/windows/desktop/api/davclnt/nf-davclnt-davgethttpfromuncpath)               | Convertit le chemin d’accès UNC spécifié en chemin d’accès HTTP équivalent.                                                                                                                                                                           |
| [**DavGetTheLockOwnerOfTheFile**](/windows/desktop/api/davclnt/nf-davclnt-davgetthelockownerofthefile)   | Retourne le propriétaire du verrou de fichier pour un fichier verrouillé sur un serveur WebDAV.                                                                                                                                                             |
| [**DavGetUNCFromHTTPPath**](/windows/desktop/api/davclnt/nf-davclnt-davgetuncfromhttppath)               | Convertit le chemin d’accès HTTP spécifié en chemin d’accès UNC équivalent.                                                                                                                                                                           |
| [**DavInvalidateCache**](/windows/desktop/api/davclnt/nf-davclnt-davinvalidatecache)                     | Invalide le contenu du cache local pour un fichier distant sur un serveur WebDAV.                                                                                                                                                     |
| [**DavRegisterAuthCallback**](/windows/desktop/api/Davclnt/nf-davclnt-davregisterauthcallback)           | Inscrit une fonction de rappel définie par l’application que le client WebDAV peut utiliser pour inviter l’utilisateur à fournir des informations d’identification.                                                                                                                 |
| [**DavUnregisterAuthCallback**](/windows/desktop/api/Davclnt/nf-davclnt-davunregisterauthcallback)       | Annule l’inscription d’une fonction de rappel enregistrée que le client WebDAV utilise pour inviter l’utilisateur à fournir des informations d’identification.                                                                                                                            |



 

 

 




