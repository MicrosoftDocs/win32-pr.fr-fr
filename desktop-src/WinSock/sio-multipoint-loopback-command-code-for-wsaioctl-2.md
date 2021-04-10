---
description: Lorsque \_ les sockets feuille d sont utilisés dans un plan de données sans racine, il est souhaitable que le trafic envoyé soit renvoyé sur le même socket. Le \_ Code de \_ commande de bouclage multipoint SIO pour WSAIoctl est utilisé pour activer ou désactiver le bouclage du trafic multipoint.
ms.assetid: 5e267287-0ff5-4943-882f-5fe6687cca10
title: SIO_MULTIPOINT_LOOPBACK le code de commande pour WSAIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc61e58a9f1db6f246e9e76ec527e57353bb35cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951170"
---
# <a name="sio_multipoint_loopback-command-code-for-wsaioctl"></a><span data-ttu-id="54259-104">SIO \_ \_ Code de commande de bouclage multipoint pour WSAIoctl</span><span class="sxs-lookup"><span data-stu-id="54259-104">SIO\_MULTIPOINT\_LOOPBACK Command Code for WSAIoctl</span></span>

<span data-ttu-id="54259-105">Lorsque \_ les sockets feuille d sont utilisés dans un plan de données sans racine, il est souhaitable que le trafic envoyé soit renvoyé sur le même socket.</span><span class="sxs-lookup"><span data-stu-id="54259-105">When d\_leaf sockets are used in a nonrooted data plane, it is desirable to have traffic that is sent out received back on the same socket.</span></span> <span data-ttu-id="54259-106">Le \_ Code de \_ commande de bouclage multipoint SIO pour [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) est utilisé pour activer ou désactiver le bouclage du trafic multipoint.</span><span class="sxs-lookup"><span data-stu-id="54259-106">The SIO\_MULTIPOINT\_LOOPBACK command code for [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) is used to enable or disable loopback of multipoint traffic.</span></span>

 

 



