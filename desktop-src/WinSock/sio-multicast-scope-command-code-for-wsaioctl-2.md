---
description: Lorsque la multidiffusion est utilisée, il est généralement nécessaire de spécifier l’étendue sur laquelle la multidiffusion doit se produire.
ms.assetid: 744b43a8-dd89-4e63-ae3c-5bee72864df7
title: SIO_MULTICAST_SCOPE le code de commande pour WSAIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209a43e461907dcded8e59c6ffee9b1376989d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034261"
---
# <a name="sio_multicast_scope-command-code-for-wsaioctl"></a>\_ \_ Code de commande de l’étendue de multidiffusion SIO pour WSAIoctl

Lorsque la multidiffusion est utilisée, il est généralement nécessaire de spécifier l' *étendue* sur laquelle la multidiffusion doit se produire. L’étendue est définie comme le nombre de segments de réseau routé à couvrir. Une étendue égale à zéro indique que la transmission par multidiffusion n’est pas placée sur le câble, mais peut être diffusée sur les sockets au sein de l’hôte local. Une valeur d’étendue de 1 (valeur par défaut) indique que la transmission sera placée sur le câble, mais ne franchira pas de routeurs. Des valeurs de portée supérieures déterminent le nombre de routeurs qui peuvent être franchis. Notez que cela correspond au paramètre de durée de vie (TTL) dans la multidiffusion IP.

La fonction [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) est utilisée pour joindre un nœud terminal dans la session multipoint. Pour plus d’informations sur l’utilisation de cette fonction, consultez les rubriques suivantes.

 

 



