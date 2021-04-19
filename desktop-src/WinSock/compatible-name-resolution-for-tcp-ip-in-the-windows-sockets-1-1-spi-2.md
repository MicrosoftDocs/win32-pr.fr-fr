---
description: Windows Sockets 1,1 a défini un certain nombre de routines qui ont été utilisées pour la résolution de noms IPv4 avec des réseaux TCP/IP. Ils sont habituellement appelés les fonctions GetXbyY et incluent les éléments suivants.
ms.assetid: 7a3ff7f3-d4b9-4900-8fd8-708a89c78c0a
title: Résolution de noms compatible pour TCP/IP dans le SPI Windows Sockets 1,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ca58f8868c17c9dad7c67fed083e9460272944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517270"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-spi"></a>Résolution de noms compatible pour TCP/IP dans le SPI Windows Sockets 1,1

Windows Sockets 1,1 a défini un certain nombre de routines qui ont été utilisées pour la résolution de noms IPv4 avec des réseaux TCP/IP. Ils sont habituellement appelés les fonctions **GetXbyY** et incluent les éléments suivants.

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

Ces fonctions sont spécifiques aux réseaux TCP/IP ; les développeurs d’applications indépendantes du protocole sont déconseillés de continuer à utiliser ces fonctions spécifiques au transport. Toutefois, pour conserver une compatibilité descendante stricte avec Windows Sockets 1,1, les fonctions précédentes continuent à être prises en charge tant qu’au moins un fournisseur d’espace de noms est présent et prend en charge la \_ famille d’adresses d’inet AF.

Le *\_32.dllWs2* implémente ces fonctions de compatibilité en termes de nouvelles fonctionnalités de résolution de noms indépendantes du protocole à l’aide d’une séquence appropriée d’appels de fonction [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) . Les détails de la façon dont les fonctions **GetXbyY** sont mappées aux fonctions de résolution de noms sont fournis ci-dessous. Le \_32.dll Ws2 gère les différences entre les versions asynchrone et synchrone des fonctions **GetXbyY** , de sorte que seule l’implémentation des fonctions **GetXbyY** synchrones soit discutée.

 

 
