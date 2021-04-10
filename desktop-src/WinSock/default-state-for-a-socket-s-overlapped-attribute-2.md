---
description: La fonction Socket a créé des sockets avec l’attribut Overlapped défini par défaut dans la première Wsock32.dll, la version 32 bits de Windows Sockets 1,1.
ms.assetid: 2ebf71fd-fcb3-4f2f-bf52-14cd13af012f
title: État par défaut de l’attribut Overlapped d’un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bc46fbf08731b0f73d841291f6815b43d02785
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113087"
---
# <a name="default-state-for-a-sockets-overlapped-attribute"></a><span data-ttu-id="2d259-103">État par défaut de l’attribut Overlapped d’un socket</span><span class="sxs-lookup"><span data-stu-id="2d259-103">Default State for a Socket's Overlapped Attribute</span></span>

<span data-ttu-id="2d259-104">La fonction [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) a créé des sockets avec l’attribut Overlapped défini par défaut dans la première Wsock32.dll, la version 32 bits de Windows sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="2d259-104">The [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function created sockets with the overlapped attribute set by default in the first Wsock32.dll, the 32-bit version of Windows Sockets 1.1.</span></span> <span data-ttu-id="2d259-105">Pour garantir la compatibilité descendante avec les implémentations de Wsock32.dll actuellement déployées, cela continuera d’être le cas pour Windows Sockets 2 également.</span><span class="sxs-lookup"><span data-stu-id="2d259-105">In order to ensure backward compatibility with currently deployed Wsock32.dll implementations, this will continue to be the case for Windows Sockets 2 as well.</span></span> <span data-ttu-id="2d259-106">Autrement dit, dans Windows Sockets 2, les sockets créés avec la fonction **Socket** auront l’attribut Overlapped.</span><span class="sxs-lookup"><span data-stu-id="2d259-106">That is, in Windows Sockets 2 sockets created with the **socket** function will have the overlapped attribute.</span></span> <span data-ttu-id="2d259-107">Toutefois, pour être plus compatible avec le reste de l’API Windows, les sockets créés avec [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) ne sont pas, par défaut, dotés de l’attribut Overlapped.</span><span class="sxs-lookup"><span data-stu-id="2d259-107">However, in order to be more compatible with the rest of the Windows API, sockets created with [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) will not, default, have the overlapped attribute.</span></span> <span data-ttu-id="2d259-108">Cet attribut sera appliqué uniquement si le bit de \_ chevauchement de l’indicateur WSA \_ est défini.</span><span class="sxs-lookup"><span data-stu-id="2d259-108">This attribute will only be applied if the WSA\_FLAG\_OVERLAPPED bit is set.</span></span>

 

 



