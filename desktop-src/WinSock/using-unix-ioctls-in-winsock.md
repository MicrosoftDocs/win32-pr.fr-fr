---
description: La commande SIOCGIFCONF fournie par la plupart des implémentations UNIX est prise en charge sous la forme de fonctions WSAIoctl et WSPIoctl avec la commande SIO \_ \_ \_ List interface. Cette commande retourne la liste des interfaces configurées et leurs paramètres.
ms.assetid: c5028dae-052a-444c-837c-cd8d6d901b6c
title: Utilisation d’IOCTL UNIX dans Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0b52c311ea8c5f67dc374503f00c3ca16c5d053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534568"
---
# <a name="using-unix-ioctls-in-winsock"></a>Utilisation d’IOCTL UNIX dans Winsock

La commande **SIOCGIFCONF** fournie par la plupart des implémentations UNIX est prise en charge sous la forme de fonctions [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) et [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) avec la commande **SIO \_ \_ \_ List interface**. Cette commande retourne la liste des interfaces configurées et leurs paramètres.

> [!Note]  
> La prise en charge de cette commande est obligatoire pour les fournisseurs de services TCP/IP compatibles Windows Sockets 2.

 

Le paramètre *lpvOutBuffer* pointe vers la mémoire tampon dans laquelle [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) et [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) stockent les informations sur les interfaces. Le nombre d’interfaces (nombre de structures retournées dans *lpvOutBuffer*) peut être déterminé en fonction de la longueur réelle de la mémoire tampon de sortie retournée dans *lpcbBytesReturned*.

 

 
