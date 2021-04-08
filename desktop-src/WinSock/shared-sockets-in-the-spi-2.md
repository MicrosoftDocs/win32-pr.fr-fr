---
description: Partage de sockets dans Windows Sockets (Winsock).
ms.assetid: dad31820-6f60-4c3b-9cdf-e301a5ffce48
title: Sockets partagés dans le SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21ff0d8f73d2bd9de942d17de7f9564158d1810c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864038"
---
# <a name="shared-sockets-in-the-spi"></a>Sockets partagés dans le SPI

Le partage de socket entre les processus dans Windows Sockets est implémenté comme suit. Un processus source appelle [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) pour obtenir une structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) spéciale. Il utilise un mécanisme de communication interprocessus (IPC) pour passer le contenu de cette structure à un processus cible. Le processus cible utilise ensuite la structure d' **\_ informations WSAPROTOCOL** dans un appel à [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket). Le descripteur de socket retourné par cette fonction sera un descripteur de socket supplémentaire vers un Socket sous-jacent qui devient donc partagé.

Il incombe au fournisseur de services d’effectuer toutes les opérations nécessaires dans le contexte du processus source et de créer une structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) qui sera reconnue lorsqu’il apparaîtra par la suite en tant que paramètre pour [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) dans le contexte des processus cibles. Le membre **dwProviderReserved** de la structure **WSAPROTOCOL \_ info** est disponible pour l’utilisation du fournisseur de services et peut être utilisé pour stocker des informations de contexte utiles, y compris un handle dupliqué.

Ce mécanisme est conçu pour être approprié pour les versions multithread à thread unique et préemptif de Windows. Notez cependant que les sockets peuvent être partagés entre les threads d’un processus donné sans utiliser la fonction [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) , dans la mesure où un descripteur de socket est valide dans tous les threads d’un processus.

Comme décrit dans allocation de [descripteur](descriptor-allocation-2.md)de section, lorsque de nouveaux descripteurs de socket sont alloués, les fournisseurs IFS doivent appeler [**WPUModifyIFSHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle) et les fournisseurs non-IFS doivent appeler [**WPUCreateSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle).

Un scénario possible pour l’établissement et l’utilisation d’un socket partagé en mode de remise est illustré dans le tableau suivant.

| Processus source                                                                                                                          | IPC    | Processus de destination                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| 1) [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket), [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))                                                                 |        |                                                                               |
| 2) demande l’identificateur du processus cible.                                                                                                  | ==> |                                                                               |
|                                                                                                                                         |        | 3) reçoit la demande d’identificateur de processus et répond.                          |
| 4) reçoit l’identificateur de processus.                                                                                                         | <== |                                                                               |
| 5) appelle [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) pour obtenir une structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) spéciale. |        |                                                                               |
| 6) envoie la structure des **\_ informations de WSAPROTOCOL** à la cible.                                                                                     |        |                                                                               |
|                                                                                                                                         | ==> | 7) reçoit la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .        |
|                                                                                                                                         |        | 8) appelle [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) pour créer un descripteur de socket partagé. |
|                                                                                                                                         |        | 9) utilise un socket partagé pour l’échange de données.                                       |
| 10) [ **WSPClosesocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                          | <== |                                                                               |



 

 

 
