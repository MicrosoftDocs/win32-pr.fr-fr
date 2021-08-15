---
title: Bluetooth et getaddrinfo
description: La fonction getaddrinfo permet de traduire le nom d’hôte en adresse pour les transports basés sur IP. étant donné que la fonction getaddrinfo est spécifique aux transports basés sur IP, elle échoue sur Bluetooth sockets.
ms.assetid: e17d8542-d4bc-499c-bae4-1f41bff493c3
keywords:
- Bluetooth et getaddrinfo Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de9faea4cebf9eee183942da04f39dfae123feea4900483d27ae2d70d8cb5b82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004529"
---
# <a name="bluetooth-and-getaddrinfo"></a>Bluetooth et getaddrinfo

La fonction [**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) permet de traduire le nom d’hôte en adresse pour les transports basés sur IP. étant donné que la fonction **getaddrinfo** est spécifique aux transports basés sur IP, elle échoue sur Bluetooth sockets.

pour effectuer la traduction du nom d’hôte vers l’adresse de Bluetooth sockets, utilisez la fonction [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) avec des **\_ conteneurs LUP** pour interroger des appareils distants, puis recherchez un nom distant et une adresse correspondants spécifiques.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> </dl>

 

 