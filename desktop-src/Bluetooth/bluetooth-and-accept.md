---
title: Bluetooth et accepter
description: Bluetooth utilise la fonction Accept pour activer les tentatives de connexion entrante sur un Socket.
ms.assetid: 79708118-2f70-4759-b5d6-cf5cfc33c27e
keywords:
- accepter
- Bluetooth
- Bluetooth
- Bluetooth et accepter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28dff84ec05429411614e64a08ab159a5ee134b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509875"
---
# <a name="bluetooth-and-accept"></a>Bluetooth et accepter

Bluetooth utilise la fonction [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) pour activer les tentatives de connexion entrante sur un Socket. L' \_ adresse BTH de l’application cliente est obtenue en lisant la section spécifique au transport Bluetooth de la structure [**sockaddr**](/windows/desktop/WinSock/sockaddr-2) retournée. L’utilisation de la fonction **Accept** avec Bluetooth a le format suivant :

-   Le paramètre *addr* de la fonction [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) est un pointeur facultatif vers une mémoire tampon qui reçoit l’adresse de l’entité qui se connecte, telle qu’elle est connue de la couche de communication. Un pointeur vers une [**structure \_ BTH sockaddr**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) avec l’adresse de l’appareil Bluetooth distant est retourné.
-   Le paramètre *addrlen* de la fonction [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) est un pointeur facultatif vers un entier qui contient la longueur, en octets, de addr. L’entier doit être supérieur ou égal à la valeur de **sizeof** ([**sockaddr \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**accepter**](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 