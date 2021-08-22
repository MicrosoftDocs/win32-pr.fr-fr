---
description: Windows Les sockets 1,1 définissaient un certain nombre de routines qui ont été utilisées pour la résolution de noms IPv4 avec des réseaux TCP/IP. Ils sont habituellement appelés les fonctions GetXbyY et incluent les éléments suivants.
ms.assetid: 7a3ff7f3-d4b9-4900-8fd8-708a89c78c0a
title: résolution de noms Compatible pour TCP/IP dans le SPI Windows sockets 1,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea355eb85d41a507e4970bf0c8d925a41ed81ca51c08b9c77955ad702a62d27c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051677"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-spi"></a>résolution de noms Compatible pour TCP/IP dans le SPI Windows sockets 1,1

Windows Les sockets 1,1 définissaient un certain nombre de routines qui ont été utilisées pour la résolution de noms IPv4 avec des réseaux TCP/IP. Ils sont habituellement appelés les fonctions **GetXbyY** et incluent les éléments suivants.

[**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname)

[**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)

[**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)

[**getprotobyname**](/windows/desktop/api/winsock/nf-winsock-getprotobyname)

[**getprotobynumber**](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)

[**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)

[**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport)

Les versions asynchrones de ces fonctions ont également été définies.

[**WSAAsyncGetHostByAddr**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)

[**WSAAsyncGetHostByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)

[**WSAAsyncGetProtoByName**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)

[**WSAAsyncGetProtoByNumber**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)

[**WSAAsyncGetServByName**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)

[**WSAAsyncGetServByPort**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)

Ces fonctions sont spécifiques aux réseaux TCP/IP ; les développeurs d’applications indépendantes du protocole sont déconseillés de continuer à utiliser ces fonctions spécifiques au transport. toutefois, pour conserver une compatibilité descendante stricte avec Windows sockets 1,1, les fonctions précédentes continuent à être prises en charge tant qu’au moins un fournisseur d’espace de noms est présent et prend en charge la \_ famille d’adresses d’INET AF.

Le *\_32.dllWs2* implémente ces fonctions de compatibilité en termes de nouvelles fonctionnalités de résolution de noms indépendantes du protocole à l’aide d’une séquence appropriée d’appels de fonction [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) . Les détails de la façon dont les fonctions **GetXbyY** sont mappées aux fonctions de résolution de noms sont fournis ci-dessous. Le \_32.dll Ws2 gère les différences entre les versions asynchrone et synchrone des fonctions **GetXbyY** , de sorte que seule l’implémentation des fonctions **GetXbyY** synchrones soit discutée.

 

 
