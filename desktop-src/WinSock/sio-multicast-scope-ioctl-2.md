---
description: Utilisation du \_ \_ Code de commande d’étendue de multidiffusion SIO pour spécifier l’étendue sur laquelle la multidiffusion doit se produire.
ms.assetid: 3acec987-9cb4-446c-af6e-ea0e6a96e70c
title: SIO_MULTICAST_SCOPE IOCTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1be65ee600b680805177a44125c03e65e49364ae9008d306349da8f60f9d9de8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559687"
---
# <a name="sio_multicast_scope-ioctl"></a>IOCTL de l' \_ étendue de multidiffusion SIO \_

Lorsque la multidiffusion est utilisée, il est généralement nécessaire de spécifier l’étendue sur laquelle la multidiffusion doit se produire. Ici, l’étendue est définie comme étant le nombre de segments réseau routés à couvrir. Le \_ \_ Code de commande d’étendue de multidiffusion SIO pour [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) est utilisé pour contrôler cela. Une étendue égale à zéro indique que la transmission par multidiffusion n’est pas placée sur le câble, mais peut être diffusée sur les sockets au sein de l’hôte local. Une valeur d’étendue de 1 (valeur par défaut) indique que la transmission sera placée sur le câble, mais ne franchira pas de routeurs. Des valeurs de portée supérieures déterminent le nombre de routeurs qui peuvent être franchis. Notez que cela correspond au paramètre de durée de vie (TTL) dans la multidiffusion IP.

 

 
