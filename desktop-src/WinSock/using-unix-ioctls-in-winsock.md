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
# <a name="using-unix-ioctls-in-winsock"></a><span data-ttu-id="c2da3-104">Utilisation d’IOCTL UNIX dans Winsock</span><span class="sxs-lookup"><span data-stu-id="c2da3-104">Using UNIX Ioctls in Winsock</span></span>

<span data-ttu-id="c2da3-105">La commande **SIOCGIFCONF** fournie par la plupart des implémentations UNIX est prise en charge sous la forme de fonctions [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) et [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) avec la commande **SIO \_ \_ \_ List interface**.</span><span class="sxs-lookup"><span data-stu-id="c2da3-105">The **SIOCGIFCONF** command provided by most UNIX implementations is supported in the form of [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) and [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) functions with the command **SIO\_GET\_INTERFACE\_LIST**.</span></span> <span data-ttu-id="c2da3-106">Cette commande retourne la liste des interfaces configurées et leurs paramètres.</span><span class="sxs-lookup"><span data-stu-id="c2da3-106">This command returns the list of configured interfaces and their parameters.</span></span>

> [!Note]  
> <span data-ttu-id="c2da3-107">La prise en charge de cette commande est obligatoire pour les fournisseurs de services TCP/IP compatibles Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="c2da3-107">Support of this command is mandatory for Windows Sockets 2-compliant TCP/IP service providers.</span></span>

 

<span data-ttu-id="c2da3-108">Le paramètre *lpvOutBuffer* pointe vers la mémoire tampon dans laquelle [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) et [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) stockent les informations sur les interfaces.</span><span class="sxs-lookup"><span data-stu-id="c2da3-108">The parameter *lpvOutBuffer* points to the buffer in which [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) and [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) store the information about interfaces.</span></span> <span data-ttu-id="c2da3-109">Le nombre d’interfaces (nombre de structures retournées dans *lpvOutBuffer*) peut être déterminé en fonction de la longueur réelle de la mémoire tampon de sortie retournée dans *lpcbBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="c2da3-109">The number of interfaces (number of structures returned in *lpvOutBuffer*) can be determined based on the actual length of the output buffer returned in *lpcbBytesReturned*.</span></span>

 

 
