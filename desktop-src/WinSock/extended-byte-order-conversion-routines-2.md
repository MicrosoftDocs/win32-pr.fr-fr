---
description: Windows Sockets 2 ne suppose pas que l’ordre d’octet du réseau pour tous les protocoles est le même.
ms.assetid: 517c21b5-4b56-49f8-88ae-103fdfce6441
title: Routines de conversion de Byte-Order étendues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2be1c217e89d19e607a64dfc943449351021506dc88f73ebcd4234a26b2b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132522"
---
# <a name="extended-byte-order-conversion-routines"></a>Routines de conversion de Byte-Order étendues

Windows Sockets 2 ne suppose pas que l’ordre d’octet du réseau pour tous les protocoles est le même. Un ensemble de routines de conversion est fourni pour convertir les quantités 16 bits et 32 bits vers et à partir de l’ordre d’octet du réseau. Ces routines prennent comme paramètre d’entrée le handle de socket auquel est associée une structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) . Le membre **NetworkByteOrder** de la structure **WSAPROTOCOL \_ info** spécifie l’ordre d’octet réseau souhaité (à l’heure actuelle Big-endian ou Little-endian).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**htonl**](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[**htons**](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[**ntohl**](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[Portage d’applications de socket vers Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Considérations sur la programmation Winsock](winsock-programming-considerations.md)
</dt> <dt>

[**WSAHtonl**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[**WSANtohl**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> <dt>

[**\_informations WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
</dt> </dl>

 

 
