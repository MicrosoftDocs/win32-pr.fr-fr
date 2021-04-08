---
title: Bluetooth et getaddrinfo
description: La fonction getaddrinfo permet de traduire le nom d’hôte en adresse pour les transports basés sur IP. Étant donné que la fonction getaddrinfo est spécifique aux transports basés sur IP, elle échoue sur les sockets Bluetooth.
ms.assetid: e17d8542-d4bc-499c-bae4-1f41bff493c3
keywords:
- Bluetooth et getaddrinfo Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c2e62b83ac947b74479ff435b93914661aa8da
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729852"
---
# <a name="bluetooth-and-getaddrinfo"></a>Bluetooth et getaddrinfo

La fonction [**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) permet de traduire le nom d’hôte en adresse pour les transports basés sur IP. Étant donné que la fonction **getaddrinfo** est spécifique aux transports basés sur IP, elle échoue sur les sockets Bluetooth.

Pour effectuer la traduction du nom d’hôte vers l’adresse pour les sockets Bluetooth, utilisez la fonction [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) avec des **\_ conteneurs lup** pour interroger des appareils distants, puis recherchez un nom distant et une adresse correspondants spécifiques.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> </dl>

 

 