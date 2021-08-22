---
description: La fonction WSADuplicateSocket est introduite pour permettre le partage de socket entre les processus.
ms.assetid: f7cf40e9-f3a6-4b62-8a78-df25464e2365
title: Sockets partagés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98e3f2663aa618b1bacab40b1cb29735c972e1d8b9e9db3528ee5079a336747c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612909"
---
# <a name="shared-sockets"></a>Sockets partagés

La fonction [**WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) est introduite pour permettre le partage de socket entre les processus. Un processus source appelle **WSADuplicateSocket** pour obtenir une structure [**d' \_ informations de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) spéciale pour un identificateur de processus cible. Il utilise un mécanisme de communication interprocessus (IPC) pour passer le contenu de cette structure à un processus cible. Le processus cible utilise ensuite la structure d' **\_ informations WSAPROTOCOL** dans un appel à [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket). Le descripteur de socket retourné par cette fonction sera un descripteur de socket supplémentaire vers un Socket sous-jacent qui devient donc partagé. Les sockets peuvent être partagés entre les threads d’un processus donné sans utiliser la fonction **WSADuplicateSocket** , car un descripteur de socket est valide dans tous les threads d’un processus.

Les deux descripteurs (ou plus) qui font référence à un socket partagé peuvent être utilisés indépendamment en ce qui concerne les e/s. Toutefois, l’interface Winsock n’implémente aucun type de contrôle d’accès, de sorte que les processus doivent coordonner les opérations sur un socket partagé. Un exemple classique de partage de sockets consiste à utiliser un processus pour créer des sockets et établir des connexions. Ce processus transmet ensuite les sockets aux autres processus qui sont responsables de l’échange d’informations.

La fonction [**WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) crée des descripteurs de socket et non le Socket sous-jacent. Par conséquent, tous les États associés à un socket sont communs à tous les descripteurs. Par exemple, une opération [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) effectuée à l’aide d’un descripteur est ensuite visible à l’aide d’un [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) à partir d’un ou de tous les descripteurs. Un processus peut appeler [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) sur un socket dupliqué et le descripteur est libéré. Toutefois, le Socket sous-jacent reste ouvert jusqu’à ce que **opération closesocket** soit appelé avec le dernier descripteur restant.

La notification sur les sockets partagés est soumise aux contraintes habituelles des fonctions [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) et [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) . L’émission de l’un de ces appels à l’aide de l’un des descripteurs partagés annule toute inscription d’événement précédente pour le socket, quel que soit le descripteur utilisé pour effectuer cette inscription. Par exemple, il n’est pas possible d’avoir des événements de lecture de lecture FD de réception \_ et de traitement B pour les événements d' \_ écriture FD. Dans les situations où une coordination étroite est nécessaire, il est suggéré aux développeurs d’utiliser des threads au lieu de processus distincts.

 

 
