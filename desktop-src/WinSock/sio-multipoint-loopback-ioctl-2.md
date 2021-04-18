---
description: Utilisation \_ \_ du code de commande de bouclage SIO multipoint pour activer ou désactiver le bouclage du trafic multipoint.
ms.assetid: 7e11932b-ce9a-4500-888f-8a08ab67b46c
title: SIO_MULTIPOINT_LOOPBACK IOCTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c9f0c7527c8c8b8b32b872eccbbbcdc9a3a2c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519024"
---
# <a name="sio_multipoint_loopback-ioctl"></a><span data-ttu-id="bea51-103">\_IOCTL de \_ bouclage SIO multipoint</span><span class="sxs-lookup"><span data-stu-id="bea51-103">SIO\_MULTIPOINT\_LOOPBACK Ioctl</span></span>

<span data-ttu-id="bea51-104">Lorsque \_ les sockets feuille d sont utilisés dans un plan de données sans racine, il est généralement préférable de pouvoir contrôler si le trafic envoyé est également renvoyé sur le même socket.</span><span class="sxs-lookup"><span data-stu-id="bea51-104">When d\_leaf sockets are used in a nonrooted data plane, it is generally desirable to be able to control whether traffic sent out is also received back on the same socket.</span></span> <span data-ttu-id="bea51-105">Le \_ \_ Code de commande de bouclage multipoint SIO pour [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) est utilisé pour activer ou désactiver le bouclage du trafic multipoint.</span><span class="sxs-lookup"><span data-stu-id="bea51-105">The SIO\_MULTIPOINT\_LOOPBACK command code for [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) is used to enable or disable loopback of multipoint traffic.</span></span>

 

 
