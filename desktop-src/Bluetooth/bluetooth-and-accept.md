---
title: Bluetooth et accepter
description: Bluetooth utilise la fonction accept pour activer les tentatives de connexion entrante sur un socket.
ms.assetid: 79708118-2f70-4759-b5d6-cf5cfc33c27e
keywords:
- accepter
- Bluetooth
- Bluetooth
- Bluetooth et accepter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5f12a7fd9fee508354dfcd9421f830e814eed09bb207cc6024b50705cc3566
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004609"
---
# <a name="bluetooth-and-accept"></a>Bluetooth et accepter

Bluetooth utilise la fonction [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) pour activer les tentatives de connexion entrante sur un socket. l' \_ adresse BTH de l’application cliente est obtenue en lisant la Bluetooth section relative au transport de la structure [**sockaddr**](/windows/desktop/WinSock/sockaddr-2) retournée. l’utilisation de la fonction **accept** avec Bluetooth a le format suivant :

-   Le paramètre *addr* de la fonction [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) est un pointeur facultatif vers une mémoire tampon qui reçoit l’adresse de l’entité qui se connecte, telle qu’elle est connue de la couche de communication. un pointeur vers une [**structure \_ BTH SOCKADDR**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) avec l’adresse de l’appareil Bluetooth distant est retourné.
-   Le paramètre *addrlen* de la fonction [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) est un pointeur facultatif vers un entier qui contient la longueur, en octets, de addr. L’entier doit être supérieur ou égal à la valeur de **sizeof** ([**sockaddr \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**valide**](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 