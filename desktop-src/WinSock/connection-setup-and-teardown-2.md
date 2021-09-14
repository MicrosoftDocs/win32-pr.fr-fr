---
description: La fonction WSAAccept permet à une application d’obtenir des informations sur l’appelant, telles que l’identificateur de l’appelant et la qualité de service, avant de décider d’accepter ou non une demande de connexion entrante.
ms.assetid: 65883556-6890-4d0a-8c7f-c4ff68642caf
title: Configuration et destruction de la connexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c4ac1f32524d097e11825f8104eb41fee3c528
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414524"
---
# <a name="connection-setup-and-teardown"></a>Configuration et destruction de la connexion

La fonction [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) permet à une application d’obtenir des informations sur l’appelant, telles que l’identificateur de l’appelant et la qualité de service, avant de décider d’accepter ou non une demande de connexion entrante. Cela est effectué avec un rappel à une fonction de condition fournie par l’application.

Les données utilisateur à utilisateur spécifiées par des paramètres dans la fonction [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) et la fonction condition de [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) peuvent être transférées à l’homologue lors de l’établissement de la connexion, à condition que cette fonctionnalité soit prise en charge par le fournisseur de services.

Il est également possible (pour les protocoles qui le prennent en charge) d’échanger des données utilisateur entre les points de terminaison au moment de la destruction de la connexion. La fin qui initie la destruction peut appeler la fonction [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) pour indiquer qu’il n’y a plus de données à envoyer et à initialiser la séquence de destruction de la connexion. Pour certains protocoles, une partie de la déconnexion est la remise de données déconnectées de l’initiateur de destruction. Après avoir reçu une notification indiquant que la terminaison distante a initié la déconnexion (généralement par l' \_ indication FD Close), la fonction [**WSARecvDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) peut être appelée pour recevoir les données de déconnexion, le cas échéant.

Pour illustrer la façon dont les données de déconnexion peuvent être utilisées, examinez le scénario suivant. La moitié du client d’une application client/serveur est responsable de l’arrêt d’une connexion de Socket. Coïncide avec l’arrêt, il fournit (à l’aide de données déconnectées) le nombre total de transactions qu’il a traitées avec le serveur. Le serveur répond à son tour avec le total cumulé des transactions qu’il a traitées avec tous les clients. La séquence d’appels et d’indications peut se présenter comme suit :

| Côté client                                                                                                              | Côté serveur                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (1) appelez [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) pour conclure la session et le total de la transaction d’approvisionnement.            |                                                                                                                                                                                                                               |
|                                                                                                                          | (2) obtenir FD \_ Close, [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) avec une valeur de retour égale à zéro, ou un retour d’erreur [WSAEDISCON](windows-sockets-error-codes-2.md) de [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) indiquant un arrêt correct en cours. |
|                                                                                                                          | (3) appelez [**WSARecvDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) pour connaître le total de la transaction du client.                                                                                                                                |
|                                                                                                                          | (4) calcul total cumulé de toutes les transactions.                                                                                                                                                                       |
|                                                                                                                          | (5) appelez [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) pour transmettre le total général.                                                                                                                                          |
| (6) recevoir l' \_ indication FD Close.                                                                                        | (5A) appeler [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket).                                                                                                                                                                             |
| (7) appelez [**WSARecvDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) pour recevoir et stocker le total cumulé des transactions. |                                                                                                                                                                                                                               |
| (8) appeler [ **opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)                                                                          |                                                                                                                                                                                                                               |



 

Notez que l’étape (5A) doit suivre l’étape (5), mais qu’elle n’a pas de relation de synchronisation avec STEP (6), (7) ou (8).

 

 



