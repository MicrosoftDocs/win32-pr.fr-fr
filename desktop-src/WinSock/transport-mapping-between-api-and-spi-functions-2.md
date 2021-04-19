---
description: Le SPI de transport Winsock est similaire à l’API Winsock en ce que toutes les fonctions de base de socket apparaissent.
ms.assetid: 37ef8a69-2aa0-4824-8ca9-4b84158086db
title: Mappage de transport entre les fonctions API et SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f11b950c48d0887f1e593c65f9d77e27c33917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521099"
---
# <a name="transport-mapping-between-api-and-spi-functions"></a>Mappage de transport entre les fonctions API et SPI

Le SPI de transport Winsock est similaire à l’API Winsock en ce que toutes les fonctions de base de socket apparaissent. Lorsqu’une nouvelle version d’une fonction Winsock et la version d’origine existent toutes les deux dans l’API, seule la nouvelle version s’affiche dans l’index SPI. Cela est illustré dans la liste suivante.

-   [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) et [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) sont mappés à [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))
-   [**accepter**](/windows/desktop/api/Winsock2/nf-winsock2-accept) et [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) mapper à [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)
-   [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) et [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) mappé à [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)

Les autres fonctions d’API qui sont réduites dans les versions améliorées dans SPI sont les suivantes :

-   [**Envoyer**](/windows/desktop/api/Winsock2/nf-winsock2-send)
-   [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto)
-   [**reçu**](/windows/desktop/api/winsock/nf-winsock-recv)
-   [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)
-   [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)

Les fonctions de prise en charge telles que [**htonl**](/windows/desktop/api/winsock/nf-winsock-htonl), [**htons**](/windows/desktop/api/winsock/nf-winsock-htons), [**ntohl**](/windows/desktop/api/winsock/nf-winsock-ntohl)et [**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs) sont implémentées dans la \_32.dll Ws2 et ne sont pas transmises aux fournisseurs de services. Il en va de même pour les versions WSA de ces fonctions.

L’énumération du fournisseur de services Windows Sockets et les fonctions associées au hook de blocage sont réalisées dans la \_32.dll Ws2. par conséquent, [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking), [WSASetBlockingHook](/windows/desktop/api/winsock2/nf-winsock2-wsasetblockinghook)et [WSAUNHOOKBLOCKINGHOOK](/windows/desktop/api/winsock2/nf-winsock2-wsaunhookblockinghook) n’apparaissent pas en tant que fonctions SPI.

Étant donné que les codes d’erreur sont retournés avec les fonctions SPI, les équivalents de [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) et [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) ne sont pas requis dans le SPI.

La manipulation d’objet d’événement et les fonctions d’attente, notamment [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent), [**WSACloseEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent), [**WSASetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetevent), [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)et [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) , sont mappées directement aux services Windows natifs et ne sont donc pas présentes dans le SPI.

Toutes les fonctions de conversion et de résolution de noms spécifiques à TCP/IP dans Windows Sockets 1,1, telles que **GetXbyY**, **WSAAsyncGetXByY** et [**WSACancelAsyncRequest**](/windows/desktop/api/winsock/nf-winsock-wsacancelasyncrequest), ainsi que [**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname) sont implémentées dans le \_32.dll Ws2 en termes de nouvelles fonctions de résolution de noms. Pour plus d’informations, consultez [résolution de noms compatible pour TCP/IP dans le SPI Windows sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md). Les fonctions de conversion telles que [**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) et [**inet \_ NTOA**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa) sont implémentées dans le \_32.dll Ws2.

 

 
