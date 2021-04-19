---
description: Cette section décrit la programmation de la multidiffusion basée sur l’état final à l’aide d’IOCTL au lieu des options de Socket. Pour obtenir une vue d’ensemble de la façon dont la programmation de la multidiffusion basée sur l’État diffère de la programmation de multidiffusion basée sur les modifications, consultez programmation de la multidiffusion.
ms.assetid: 71c05393-3f8c-42c0-9060-e0df9b5e2578
title: Programmation de la multidiffusion basée sur l’état final
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6abfebfc7efe27f1c5a6d63312c376bd659dce57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513408"
---
# <a name="final-state-based-multicast-programming"></a><span data-ttu-id="48f1e-104">Programmation de la multidiffusion basée sur l’état final</span><span class="sxs-lookup"><span data-stu-id="48f1e-104">Final-State-Based Multicast Programming</span></span>

<span data-ttu-id="48f1e-105">Cette section décrit la programmation de la multidiffusion basée sur l’état final à l’aide d’IOCTL au lieu des options de Socket.</span><span class="sxs-lookup"><span data-stu-id="48f1e-105">This section describes final-state-based multicast programming using IOCTLs instead of socket options.</span></span> <span data-ttu-id="48f1e-106">Pour obtenir une vue d’ensemble de la façon dont la programmation de la multidiffusion basée sur l’État diffère de la programmation de multidiffusion basée sur les modifications, consultez programmation de la [multidiffusion](multicast-programming.md).</span><span class="sxs-lookup"><span data-stu-id="48f1e-106">For an overview of how final-state-based multicast programming differs from change-based multicast programming, see [Multicast Programming](multicast-programming.md).</span></span>

<span data-ttu-id="48f1e-107">Le tableau suivant décrit les IOCTL Windows Sockets utilisés pour la programmation multidiffusion sur Windows.</span><span class="sxs-lookup"><span data-stu-id="48f1e-107">The following table describes the Windows Sockets IOCTLs used for multicast programming on Windows.</span></span> 

| <span data-ttu-id="48f1e-108">IOCTL</span><span class="sxs-lookup"><span data-stu-id="48f1e-108">IOCTL</span></span>                       | <span data-ttu-id="48f1e-109">Type d’argument</span><span class="sxs-lookup"><span data-stu-id="48f1e-109">Argument type</span></span>                                   |
|-----------------------------|-------------------------------------------------|
| <span data-ttu-id="48f1e-110">SIOCSMSFILTER</span><span class="sxs-lookup"><span data-stu-id="48f1e-110">SIOCSMSFILTER</span></span>               | <span data-ttu-id="48f1e-111">[**Groupe \_**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) Structure de filtre</span><span class="sxs-lookup"><span data-stu-id="48f1e-111">[**GROUP\_FILTER**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) structure</span></span> |
| <span data-ttu-id="48f1e-112">SIOCGMSFILTER</span><span class="sxs-lookup"><span data-stu-id="48f1e-112">SIOCGMSFILTER</span></span>               | <span data-ttu-id="48f1e-113">[**Groupe \_**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) Structure de filtre</span><span class="sxs-lookup"><span data-stu-id="48f1e-113">[**GROUP\_FILTER**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) structure</span></span> |
| <span data-ttu-id="48f1e-114">SIO \_ recevoir le \_ filtre de multidiffusion \_</span><span class="sxs-lookup"><span data-stu-id="48f1e-114">SIO\_GET\_MULTICAST\_FILTER</span></span> | <span data-ttu-id="48f1e-115">structure [**IP \_ msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)</span><span class="sxs-lookup"><span data-stu-id="48f1e-115">[**ip\_msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) structure</span></span>   |
| <span data-ttu-id="48f1e-116">SIO \_ définir un \_ filtre de multidiffusion \_</span><span class="sxs-lookup"><span data-stu-id="48f1e-116">SIO\_SET\_MULTICAST\_FILTER</span></span> | <span data-ttu-id="48f1e-117">structure [**IP \_ msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)</span><span class="sxs-lookup"><span data-stu-id="48f1e-117">[**ip\_msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) structure</span></span>   |



 

<span data-ttu-id="48f1e-118">Notez que les IOCTL **SIOCSMSFILTER** et **SIOCGMSFILTER** sont disponibles sur Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="48f1e-118">Note that the **SIOCSMSFILTER** and **SIOCGMSFILTER** IOCTLS are available on Windows Vista and later.</span></span>

<span data-ttu-id="48f1e-119">L’utilisation de ces ioctl pour la programmation de la multidiffusion présente des avantages en matière de performances lorsque vous utilisez des listes de sources volumineuses.</span><span class="sxs-lookup"><span data-stu-id="48f1e-119">Using these IOCTLs for multicast programming has performance benefits when working with large source lists.</span></span> <span data-ttu-id="48f1e-120">Pour plus d’informations sur les paramètres et les paramètres associés à l’utilisation de SIO Filter multicast ou d’un filtre de \_ \_ \_ \_ \_ multidiffusion SIO \_ , consultez la page de référence de [**\_ filtre de groupe**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) .</span><span class="sxs-lookup"><span data-stu-id="48f1e-120">For more information about the parameters and settings associated with using SIO\_GET\_MULTICAST\_FILTER or SIO\_SET\_MULTICAST\_FILTER, consult the [**GROUP\_FILTER**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) reference page.</span></span> <span data-ttu-id="48f1e-121">Pour plus d’informations sur les paramètres et les paramètres associés à l’utilisation de SIO \_ \_ , obtenir un filtre de multidiffusion \_ ou SIO \_ définir \_ \_ un filtre de multidiffusion, consultez la page de référence [**\_ msfilter IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) .</span><span class="sxs-lookup"><span data-stu-id="48f1e-121">For more information about the parameters and settings associated with using SIO\_GET\_MULTICAST\_FILTER or SIO\_SET\_MULTICAST\_FILTER, consult the [**ip\_msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) reference page.</span></span>

 

 



