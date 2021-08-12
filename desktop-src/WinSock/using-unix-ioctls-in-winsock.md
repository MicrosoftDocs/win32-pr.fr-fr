---
description: la commande SIOCGIFCONF fournie par la plupart des implémentations UNIX est prise en charge sous la forme de fonctions WSAIoctl et WSPIoctl avec la commande SIO \_ liste d’interfaces d’extraction \_ \_ . Cette commande retourne la liste des interfaces configurées et leurs paramètres.
ms.assetid: c5028dae-052a-444c-837c-cd8d6d901b6c
title: utilisation d’ioctl UNIX dans Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da517adb6480a1bd20100a3d9a6d0896f544c1b541ce547a0f76e5c88aa24210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118558861"
---
# <a name="using-unix-ioctls-in-winsock"></a>utilisation d’ioctl UNIX dans Winsock

la commande **SIOCGIFCONF** fournie par la plupart des implémentations UNIX est prise en charge sous la forme de fonctions [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) et [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) avec la commande **SIO \_ \_ \_ liste d’interfaces d’extraction**. Cette commande retourne la liste des interfaces configurées et leurs paramètres.

> [!Note]  
> la prise en charge de cette commande est obligatoire pour les fournisseurs de services TCP/IP conformes à Windows sockets 2.

 

Le paramètre *lpvOutBuffer* pointe vers la mémoire tampon dans laquelle [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) et [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) stockent les informations sur les interfaces. Le nombre d’interfaces (nombre de structures retournées dans *lpvOutBuffer*) peut être déterminé en fonction de la longueur réelle de la mémoire tampon de sortie retournée dans *lpcbBytesReturned*.

 

 
