---
description: Dans deux cas, il était nécessaire de renommer les fonctions utilisées dans les sockets Berkeley afin d’éviter les conflits avec d’autres fonctions de l’API Microsoft Windows.
ms.assetid: b53b1622-cba4-47e3-a371-b3186de6d61b
title: Fonctions renommées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8fd2af33bdeb74dd7a4c83fe535bae2a020530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863814"
---
# <a name="renamed-functions"></a>Fonctions renommées

Dans deux cas, il était nécessaire de renommer les fonctions utilisées dans les sockets Berkeley afin d’éviter les conflits avec d’autres fonctions de l’API Microsoft Windows.

## <a name="close-and-closesocket"></a>Fermer et opération closesocket

Les sockets sont représentés par des descripteurs de fichiers standard dans les sockets Berkeley. la fonction **Close** peut donc être utilisée pour fermer des sockets et des fichiers normaux. Bien que rien dans Windows Sockets ne permette à une implémentation d’utiliser des handles de fichiers normaux pour identifier des sockets, rien ne l’exige. Sur Windows, les sockets doivent être fermés à l’aide de la routine [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) . SUR Windows, l’utilisation de la fonction **Close** pour fermer un socket est incorrecte et les effets de cette action ne sont pas définis par cette spécification.

## <a name="ioctl-and-ioctlsocketwsaioctl"></a>IOCTL et ioctlsocket/WSAIoctl

Différents systèmes Runtime en langage C utilisent les IOCTL à des fins non liées à Windows Sockets. Par conséquent, la fonction [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) et la fonction [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) ont été définies pour gérer les fonctions de socket qui ont été effectuées par **IOCTL** et **fcntl** dans la distribution de logiciels Berkeley.

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

 

 



