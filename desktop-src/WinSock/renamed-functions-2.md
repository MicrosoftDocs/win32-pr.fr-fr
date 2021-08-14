---
description: dans deux cas, il était nécessaire de renommer les fonctions utilisées dans les sockets Berkeley afin d’éviter les conflits avec d’autres fonctions de l’API Microsoft Windows.
ms.assetid: b53b1622-cba4-47e3-a371-b3186de6d61b
title: Fonctions renommées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5ba31ed7c200e08ec63957690745e567b3232bfcd0f28e3885ec84d8696828
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993589"
---
# <a name="renamed-functions"></a>Fonctions renommées

dans deux cas, il était nécessaire de renommer les fonctions utilisées dans les sockets Berkeley afin d’éviter les conflits avec d’autres fonctions de l’API Microsoft Windows.

## <a name="close-and-closesocket"></a>Fermer et opération closesocket

Les sockets sont représentés par des descripteurs de fichiers standard dans les sockets Berkeley. la fonction **Close** peut donc être utilisée pour fermer des sockets et des fichiers normaux. bien que rien dans Windows sockets empêche une implémentation d’utiliser des descripteurs de fichiers normaux pour identifier des sockets, rien ne l’exige. sur Windows, les sockets doivent être fermés à l’aide de la routine [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) . sur Windows, l’utilisation de la fonction **close** pour fermer un socket est incorrecte et les effets de cette action ne sont pas définis par cette spécification.

## <a name="ioctl-and-ioctlsocketwsaioctl"></a>IOCTL et ioctlsocket/WSAIoctl

différents systèmes runtime en langage C utilisent les ioctl à des fins non liées à Windows sockets. Par conséquent, la fonction [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) et la fonction [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) ont été définies pour gérer les fonctions de socket qui ont été effectuées par **IOCTL** et **fcntl** dans la distribution de logiciels Berkeley.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)
</dt> <dt>

[Portage d’applications de socket vers Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Considérations sur la programmation Winsock](winsock-programming-considerations.md)
</dt> <dt>

[**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)
</dt> </dl>

 

 



