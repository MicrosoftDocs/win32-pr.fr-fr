---
title: Instance du gestionnaire de table de routage
description: Une instance est une table distincte que le gestionnaire de tables de routage utilise pour gérer les informations de routage relatives à un sous-ensemble d’interfaces.
ms.assetid: a17233fc-2c40-4d00-8a6b-86f08fef5690
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d209f254bb9111c786bde6635b43895604785d5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029112"
---
# <a name="routing-table-manager-instance"></a><span data-ttu-id="b669e-103">Instance du gestionnaire de table de routage</span><span class="sxs-lookup"><span data-stu-id="b669e-103">Routing Table Manager Instance</span></span>

<span data-ttu-id="b669e-104">Une instance est une table distincte que le gestionnaire de tables de routage utilise pour gérer les informations de routage relatives à un sous-ensemble d’interfaces.</span><span class="sxs-lookup"><span data-stu-id="b669e-104">An instance is a separate table that the routing table manager uses to maintain routing information about a subset of interfaces.</span></span> <span data-ttu-id="b669e-105">Les instances sont généralement utilisées pour permettre à un routeur physique d’agir comme un ensemble de routeurs virtuels, un routeur virtuel par réseau logique.</span><span class="sxs-lookup"><span data-stu-id="b669e-105">Instances are typically used to enable a physical router to act as a set of virtual routers – one virtual router per logical network.</span></span>

<span data-ttu-id="b669e-106">Actuellement, le gestionnaire de table de routage ne prend en charge qu’une seule instance (identifiée comme zéro, valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="b669e-106">Currently, the routing table manager supports only one instance (identified as zero, the default).</span></span> <span data-ttu-id="b669e-107">Le client peut s’inscrire auprès d’autres instances, mais aucun routeur virtuel, à l’exception de celui par défaut, n’est reconnu ou utilisé par le gestionnaire de routeur.</span><span class="sxs-lookup"><span data-stu-id="b669e-107">The client can register with other instances, but no virtual router except the default one is recognized or used by the router manager.</span></span>

 

 




