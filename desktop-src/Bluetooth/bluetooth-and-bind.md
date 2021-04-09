---
title: Bluetooth et liaison
description: Bluetooth utilise la fonction de liaison pour établir une liaison à un Socket.
ms.assetid: 308d2680-de51-49e6-a0da-7aba494d9572
keywords:
- bind
- Bluetooth
- Bluetooth
- Bluetooth et liaison
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ccbd088ab61edcfa3dfc511ea591593d0cf781
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842681"
---
# <a name="bluetooth-and-bind"></a>Bluetooth et liaison

Bluetooth utilise la fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) pour établir une liaison à un Socket. Pour lier un Socket Bluetooth, appelez la fonction **Bind** à l’aide de la structure [**\_ BTH sockaddr**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) . Utilisez la **structure \_ BTH sockaddr** avec les paramètres suivants :

``` syntax
name.addressFamily = AF_BTH;
name.btAddr = 0;
name.serviceClassId = GUID_NULL;
name.port = number of service channel, 0 or BT_PORT_ANY;
```

Sur les applications clientes, le membre de port doit être égal à zéro pour permettre l’attribution d’un point de terminaison local approprié. Sur les applications serveur, le membre de port doit être un numéro de port ou un port BT valide \_ \_ . les ports attribués automatiquement à l’aide \_ du port BT \_ peuvent être interrogés par la suite avec un appel à la fonction [**GetSockName**](bluetooth-and-getsockname.md) . La plage valide pour la demande d’un port RFCOMM spécifique est comprise entre 1 et 30. Les canaux de serveur sont des ressources globales, et seulement 30 canaux de serveurs sont disponibles pour la RFCOMM sur n’importe quel périphérique Bluetooth, qui doit être partagé par tous les sockets Windows appartenant à la famille d’adresses Bluetooth. Si aucun canal serveur n’est disponible, ou si le canal serveur spécifié est déjà réservé, l’appel de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) échoue.

En cas de retour réussi de bind, le canal serveur est réservé jusqu’à la fermeture du Socket. Utilisez la fonction [**GetSockName**](bluetooth-and-getsockname.md) pour récupérer le numéro de canal pour l’inscription SDP.

Les applications doivent utiliser l’allocation automatique pour le canal serveur.

La fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) ne publie pas automatiquement l’application serveur à l’aide du SDP Bluetooth ; les applications doivent appeler la fonction [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) pour être recherchées par les applications Bluetooth distantes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**établis**](/windows/desktop/api/winsock/nf-winsock-bind)
</dt> </dl>

 

 