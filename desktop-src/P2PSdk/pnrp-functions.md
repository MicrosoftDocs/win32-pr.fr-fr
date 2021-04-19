---
description: L’API du fournisseur d’espace de noms PNRP utilise les fonctions suivantes.
ms.assetid: 7c9f2dd7-8dbc-4bbe-b53c-8036c79faa8a
title: Fonctions PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0e811c2d10927064e380970456c76f30730ee4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518686"
---
# <a name="pnrp-functions"></a>Fonctions PNRP

L’API du fournisseur d’espace de noms PNRP utilise les fonctions suivantes.



| Fonction                                                             | Description                                                                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerNameToPeerHostName**](/windows/desktop/api/P2P/nf-p2p-peernametopeerhostname)             | Encode le nom d’homologue fourni sous la forme d’un format qui peut être utilisé avec un appel ultérieur à la fonction Windows Sockets [**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) . |
| [**PeerHostNameToPeerName**](/windows/desktop/api/P2P/nf-p2p-peerhostnametopeername)             | Décode un nom d’hôte retourné par [**PeerNameToPeerHostName**](/windows/desktop/api/P2P/nf-p2p-peernametopeerhostname) dans la chaîne de nom d’homologue qu’il représente.                            |
| [**PeerPnrpStartup**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartup)                           | Démarre le service PNRP (Peer Name Resolution Protocol) pour l’homologue appelant.                                                                                |
| [**PeerPnrpShutdown**](/windows/desktop/api/P2P/nf-p2p-peerpnrpshutdown)                         | Arrête une instance en cours d’exécution du service PNRP (Peer Name Resolution Protocol) et libère toutes les ressources qui lui sont associées.                             |
| [**PeerPnrpRegister**](/windows/desktop/api/P2P/nf-p2p-peerpnrpregister)                         | Inscrit un homologue auprès d’un Cloud PNRP et retourne un descripteur qui peut être utilisé pour les mises à jour d’inscription.                                                           |
| [**PeerPnrpUpdateRegistration**](/windows/desktop/api/P2P/nf-p2p-peerpnrpupdateregistration)     | Met à jour les informations d’inscription PNRP pour un nom.                                                                                                        |
| [**PeerPnrpUnregister**](/windows/desktop/api/P2P/nf-p2p-peerpnrpunregister)                     | Annule l’inscription d’un homologue d’un Cloud PNRP.                                                                                                                        |
| [**PeerPnrpResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpresolve)                           | Obtient les adresses de point de terminaison inscrites pour un nom d’homologue spécifique.                                                                                        |
| [**PeerPnrpStartResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartresolve)                 | Démarre une opération de résolution de nom d’homologue asynchrone.                                                                                                       |
| [**PeerPnrpGetCloudInfo**](/windows/desktop/api/P2P/nf-p2p-peerpnrpgetcloudinfo)                 | Récupère des informations sur les clouds PNRP (Peer Name Resolution Protocol) auxquels l’homologue appelant participe.                                         |
| [**PeerPnrpEndResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpendresolve)                     | Ferme le handle pour une opération de résolution PNRP asynchrone lancée à l’aide d’un appel précédent à [**PeerPnrpStartResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartresolve).      |
| [PNRP et WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md) | Démarre le processus qui permet à une application de résoudre les noms et d’énumérer les clouds réseau.                                                                 |
| [PNRP et WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)     | Termine une requête lancée lors d’un appel précédent à [**WSALookupServiceBegin**](winsock-nsp-reference-links.md).                                             |
| [PNRP et WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)   | Correspond aux requêtes spécifiées dans un appel précédent à [**WSALookupServiceBegin**](winsock-nsp-reference-links.md).                                                |
| [PNRP et WSANSPIoctl](pnrp-and-wsanspioctl.md)                     | Reçoit des notifications sur les modifications apportées à la liste de Cloud réseau et la disponibilité des résultats d’une demande de résolution de noms.                                     |
| [PNRP et WSASetService](pnrp-and-wsasetservice.md)                 | Inscrit ou supprime des [noms d’homologues](peer-names.md).                                                                                                           |



 

 

 
