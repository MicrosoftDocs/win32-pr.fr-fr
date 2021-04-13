---
description: Fonctions de transport de données exposées par Ws2spi. h.
ms.assetid: 6900faa3-79bb-4ed8-b83e-148eb10425a0
title: Fonctions de transport de données génériques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63de41b90148210ea8a99d5271b62c5d8bc0c08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526175"
---
# <a name="generic-data-transport-functions"></a>Fonctions de transport de données génériques

Cette section répertorie les fonctions de transport de données exposées par Ws2spi. h.



| Fonction                                                   | Description                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)                           | Une connexion entrante est reconnue et associée à un socket créé immédiatement. Le socket d’origine est retourné à l’état d’écoute. Cette fonction permet également l’acceptation conditionnelle. |
| [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85))                 | Exécute une version asynchrone de [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)).                                                                                                                                      |
| [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85))                               | Assigne un nom local à un socket sans nom.                                                                                                                                                              |
| [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85))   | Annule un appel Windows Sockets bloquant en attente.                                                                                                                                                   |
| [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85))                         | Se déconnecte du fournisseur de services Windows Sockets sous-jacent.                                                                                                                                         |
| [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                 | Supprime un socket de la table de référence d’objet par processus. Bloque uniquement si ce \_ reste est défini avec un délai d’expiration différent de zéro sur un socket bloquant.                                                            |
| [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))                         | Initialise une connexion sur le socket spécifié. Cette fonction permet également l’échange de données de connexion et de spécification QoS.                                                                           |
| [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85))         | Retourne une structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) qui peut être utilisée pour créer un nouveau descripteur de socket pour un socket partagé.                                                             |
| [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85))     | Découvre des occurrences d’événements réseau.                                                                                                                                                                |
| [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))                 | Associe des événements réseau à un objet d’événement.                                                                                                                                                         |
| [**WSPGetOverlappedResult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult) | Obtient l’état d’achèvement de l’opération Overlapped.                                                                                                                                                         |
| [**WSPGetPeerName**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85))                 | Récupère le nom de l’homologue connecté au socket spécifié.                                                                                                                                       |
| [**WSPGetSockName**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85))                 | Récupère l’adresse locale à laquelle le socket spécifié est lié.                                                                                                                                     |
| [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))                   | Récupère les options associées au socket spécifié.                                                                                                                                                 |
| [**WSPGetQOSByName**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetqosbyname)               | Fournit des paramètres de qualité de service basés sur un nom de service bien connu.                                                                                                                                             |
| [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))                             | Fournit le contrôle pour les sockets.                                                                                                                                                                           |
| [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)                       | Joint un nœud terminal dans une session multipoint.                                                                                                                                                            |
| [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))                           | Écoute les connexions entrantes sur un socket spécifié.                                                                                                                                                 |
| [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))                               | Reçoit des données à partir d’un socket connecté ou non connecté. Cette fonction prend en charge les e/s de ventilation/regroupement, les sockets superposés et fournit le paramètre flags comme étant en entrée/sortie.                                    |
| [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85))           | Met fin à la réception sur un socket et récupère les données de déconnexion si le socket est orienté connexion.                                                                                                |
| [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85))                       | Reçoit des données à partir d’un socket connecté ou non connecté. Cette fonction prend en charge les e/s de ventilation/regroupement, les sockets superposés et fournit le paramètre flags comme étant en entrée/sortie.                              |
| [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85))                           | Effectue un multiplexage des e/s synchrones.                                                                                                                                                                  |
| [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85))                               | Envoie des données à un socket connecté. Cette fonction prend également en charge les e/s de ventilation/regroupement et les sockets superposés.                                                                                            |
| [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85))           | Lance l’arrêt d’une connexion de socket et envoie éventuellement des données de déconnexion.                                                                                                                       |
| [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85))                           | Envoie des données à un socket connecté ou non connecté. Cette fonction prend également en charge les e/s de ventilation/regroupement et les sockets superposés.                                                                      |
| [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85))                   | Stocke les options associées au socket spécifié.                                                                                                                                                    |
| [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85))                       | Ferme une partie d’une connexion duplex intégral.                                                                                                                                                            |
| [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)                           | Fonction de création de socket qui prend une structure d' [**\_ informations WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) comme entrée et permet la création de sockets superposés.                                                |
| [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup)                         | Initialise le fournisseur de services Windows Sockets sous-jacent.                                                                                                                                            |



 

 

 
