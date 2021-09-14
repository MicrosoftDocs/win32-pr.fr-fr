---
description: Le service de distribution d’homologues Microsoft prend en charge des fonctions pour les scénarios de rôle de consommateur et de rôle d’éditeur.
ms.assetid: 3f5af891-4f5d-4523-8fe6-47fc6ff13b35
title: Fonctions de l’API de distribution d’homologue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2532ad8bf5cbb14e18bd16a14bb1be2d79c1791
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009214"
---
# <a name="peer-distribution-api-functions"></a>Fonctions de l’API de distribution d’homologue

Le service de distribution d’homologues Microsoft prend en charge des fonctions pour les scénarios de rôle de consommateur et de rôle d’éditeur.

## <a name="the-following-functions-are-common-in-both-client-and-server-scenarios"></a>Les fonctions suivantes sont communes dans les scénarios « client » et « serveur ».



| Fonctions communes                                                                                       | Description                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)                                                             | Crée une instance **de \_ \_ handle d’instance PEERDIST** qui doit être passée à toutes les autres API de distribution d’homologue. |
| [**PeerDistShutdown**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistshutdown)                                                           | Libère les ressources allouées par l’appel à [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup).                         |
| [**PeerDistGetStatus**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistgetstatus)                                                         | Retourne l’état actuel du service de distribution d’homologue.                                                        |
| [**PeerDistGetStatusEx**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistgetstatusex)                                                     | Retourne l’état actuel et les fonctionnalités du service de distribution d’homologue.                                   |
| [**PeerDistGetOverlappedResult**](/windows/desktop/api/peerdist/nf-peerdist-peerdistgetoverlappedresult)                                     | Récupère les résultats des opérations asynchrones.                                                               |
| [**PeerDistRegisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistregisterforstatuschangenotification)     | Demande que le service de distribution d’homologue avertisse l’appelant lorsqu’un changement d’État se produit.                      |
| [**PeerDistRegisterForStatusChangeNotificationEx**](/windows/desktop/api/peerdist/nf-peerdist-peerdistregisterforstatuschangenotificationex) | Demande que le service de distribution d’homologue avertisse l’appelant lorsqu’un changement d’État se produit.                      |
| [**PeerDistUnregisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistunregisterforstatuschangenotification) | Annule l’inscription de la notification de modification d’État pour la session associée au handle fourni.                 |



 

## <a name="the-following-functions-are-only-supported-in-client-scenarios"></a>Les fonctions suivantes sont prises en charge uniquement dans les scénarios « client ».



| Fonctions clientes                                                                             | Description                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)                               | Ouvre et retourne un **\_ \_ handle de contenu PEERDIST** pour référencer ce contenu.                                                                                                                                                                                                                                                                     |
| [**PeerDistClientCloseContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientclosecontent)                             | Ferme le **\_ \_ handle de contenu PEERDIST**.                                                                                                                                                                                                                                                                                                        |
| [**PeerDistClientGetInformationByHandle**](/windows/desktop/api/peerdist/nf-peerdist-peerdistclientgetinformationbyhandle)         | Récupère des informations supplémentaires à partir du service de distribution d’homologue pour un handle de contenu spécifique.                                                                                                                                                                                                                                               |
| [**PeerDistClientAddContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientaddcontentinformation)           | Ajoute des informations de contenu qui sont ensuite associées **au \_ \_ descripteur de contenu PEERDIST**. Un **\_ \_ descripteur de contenu PEERDIST** peut être associé à n’importe quelle information de contenu.                                                                                                                                                                        |
| [**PeerDistClientCompleteContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientcompletecontentinformation) | Indique la fin des informations de contenu.                                                                                                                                                                                                                                                                                                    |
| [**PeerDistClientAddData**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientadddata)                                       | Utilisé pour fournir du contenu au cache local. En général, cette opération est effectuée lorsque les données sont introuvables sur le réseau local comme indiqué lors de l’exécution de [**PeerDistClientBlockRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientblockread) ou [**PeerDistClientStreamRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientstreamread) avec un **\_ délai d’erreur** ou une **\_ erreur \_ \_ PEERDIST**. |
| [**PeerDistClientBlockRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientblockread)                                   | Fournit un accès aléatoire au flux de contenu.                                                                                                                                                                                                                                                                                                    |
| [**PeerDistClientStreamRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientstreamread)                                 | Fournit un accès séquentiel au flux de contenu.                                                                                                                                                                                                                                                                                                |
| [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent)                             | Supprime le contenu qui a été précédemment ajouté au système de distribution d’homologue local.                                                                                                                                                                                                                                                            |
| [**PeerDistClientCancelAsyncOperation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientcancelasyncoperation)             | Annule l’opération asynchrone associée à une structure [OVERLAPPED](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) et le handle de contenu retourné par [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent).                                                                                                                     |



 

## <a name="the-following-functions-are-only-supported-in-server-scenarios"></a>Les fonctions suivantes sont prises en charge uniquement dans les scénarios « serveur ».



| Fonctions du serveur                                                                             | Description                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream)                           | Crée le **\_ \_ handle de flux PEERDIST** qui peut être utilisé avec [**PeerDistServerPublishAddToStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishaddtostream) pour créer des informations de contenu pour le flux de contenu. |
| [**PeerDistServerPublishAddToStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishaddtostream)                 | Ajoute des données au flux référencé par le handle de flux PeerDist.                                                                                                                                  |
| [**PeerDistServerPublishCompleteStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishcompletestream)           | Appelé pour indiquer que toutes les données ont été ajoutées au flux.                                                                                                                                     |
| [**PeerDistServerCloseStreamHandle**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverclosestreamhandle)                   | Ferme le handle de flux.                                                                                                                                                                          |
| [**PeerDistServerUnpublish**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverunpublish)                                   | Annule la publication du contenu précédemment publié dans le service de distribution d’homologue.                                                                                                                         |
| [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)         | Ouvre un **\_ \_ handle CONTENTINFO CONTENTINFO** pour le contenu publié.                                                                                                                                   |
| [**PeerDistServerOpenContentInformationEx**](/windows/desktop/api/peerdist/nf-peerdist-peerdistserveropencontentinformationex)     | Ouvre un **\_ \_ handle CONTENTINFO CONTENTINFO** pour le contenu publié.                                                                                                                                   |
| [**PeerDistServerRetrieveContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverretrievecontentinformation) | Récupère les informations de contenu associées au contenu publié.                                                                                                                               |
| [**PeerDistServerCloseContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverclosecontentinformation)       | **PEERDIST \_ \_Gestionnaire CONTENTINFO** ouvert par [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation).                                                                  |
| [**PeerDistServerCancelAsyncOperation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistservercancelasyncoperation)             | Annule l’opération asynchrone associée à l’identificateur de contenu et à la structure [OVERLAPPED](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .                                             |



 

 

 
