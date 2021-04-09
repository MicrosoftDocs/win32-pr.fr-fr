---
description: Il existe une limitation dans le code qui reçoit les paquets encapsulés (en tunnel) et les démultiplexe vers une interface spécifique.
ms.assetid: 6148fca7-adf4-460d-afd6-79c43285af6c
title: Transfert IPv6 de paquets Tunnelés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f95f88a90a358317cf46516808a96f93b792dd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862569"
---
# <a name="ipv6-forwarding-tunneled-packets"></a><span data-ttu-id="5cd6e-103">Transfert IPv6 de paquets Tunnelés</span><span class="sxs-lookup"><span data-stu-id="5cd6e-103">IPv6 Forwarding Tunneled Packets</span></span>

<span data-ttu-id="5cd6e-104">Il existe une limitation dans le code qui reçoit les paquets encapsulés (en tunnel) et les démultiplexe vers une interface spécifique.</span><span class="sxs-lookup"><span data-stu-id="5cd6e-104">There is a limitation in the code that receives encapsulated (tunneled) packets and demultiplexes them to a specific interface.</span></span> <span data-ttu-id="5cd6e-105">Si vous souhaitez transférer des paquets tunnelés reçus via un tunnel configuré, il est nécessaire d’activer le transfert sur les interfaces 6-sur-4 et l’interface \# 2.</span><span class="sxs-lookup"><span data-stu-id="5cd6e-105">If you want to forward tunneled packets received through a configured tunnel, then it is necessary to enable forwarding on any 6-over-4 interfaces as well as interface \#2.</span></span> <span data-ttu-id="5cd6e-106">Le simple fait d’activer le transfert sur l’interface \# 2 ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="5cd6e-106">Just enabling forwarding on interface \#2 will not work.</span></span> <span data-ttu-id="5cd6e-107">En général, lors de la configuration d’un routeur, vous activez le transfert sur toutes les interfaces, à l’exception du bouclage.</span><span class="sxs-lookup"><span data-stu-id="5cd6e-107">Typically when configuring a router, you would enable forwarding on all interfaces except loopback.</span></span>

 

 



