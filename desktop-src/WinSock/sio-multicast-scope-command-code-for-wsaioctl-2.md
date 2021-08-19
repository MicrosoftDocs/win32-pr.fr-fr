---
description: Lorsque la multidiffusion est utilisée, il est généralement nécessaire de spécifier l’étendue sur laquelle la multidiffusion doit se produire.
ms.assetid: 744b43a8-dd89-4e63-ae3c-5bee72864df7
title: SIO_MULTICAST_SCOPE le code de commande pour WSAIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38269167aa2ed142440b0e1105600d26c59514f72d749595ce44ecdf3a0998f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927368"
---
# <a name="sio_multicast_scope-command-code-for-wsaioctl"></a>\_ \_ Code de commande de l’étendue de multidiffusion SIO pour WSAIoctl

Lorsque la multidiffusion est utilisée, il est généralement nécessaire de spécifier l' *étendue* sur laquelle la multidiffusion doit se produire. L’étendue est définie comme le nombre de segments de réseau routé à couvrir. Une étendue égale à zéro indique que la transmission par multidiffusion n’est pas placée sur le câble, mais peut être diffusée sur les sockets au sein de l’hôte local. Une valeur d’étendue de 1 (valeur par défaut) indique que la transmission sera placée sur le câble, mais ne franchira pas de routeurs. Des valeurs de portée supérieures déterminent le nombre de routeurs qui peuvent être franchis. Notez que cela correspond au paramètre de durée de vie (TTL) dans la multidiffusion IP.

La fonction [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) est utilisée pour joindre un nœud terminal dans la session multipoint. Pour plus d’informations sur l’utilisation de cette fonction, consultez les rubriques suivantes.

 

 



