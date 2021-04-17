---
description: Un autre aspect du développement d’applications à prendre en compte est la différence de comportement entre les opérations locales, intracomputer et le comportement lorsque des opérations se produisent entre deux ordinateurs en réseau.
ms.assetid: e6f48446-948c-458c-8ecf-04ffb249c8a4
title: Comportement de l’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a9b871a2c0535d9ef4220824651657332a224a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526212"
---
# <a name="application-behavior"></a><span data-ttu-id="2a801-103">Comportement de l’application</span><span class="sxs-lookup"><span data-stu-id="2a801-103">Application Behavior</span></span>

<span data-ttu-id="2a801-104">Un autre aspect du développement d’applications à prendre en compte est la différence de comportement entre les opérations locales, intracomputer et le comportement lorsque des opérations se produisent entre deux ordinateurs en réseau.</span><span class="sxs-lookup"><span data-stu-id="2a801-104">Another aspect of application development to consider is the difference in behavior between local, or intracomputer operations, and behavior when operations take place between two networked computers.</span></span> <span data-ttu-id="2a801-105">Il existe des comportements d’application qui peuvent fonctionner correctement bien sur un ordinateur local, mais lorsqu’ils sont exécutés sur un réseau, entraînent une dégradation significative des performances et la consommation des ressources.</span><span class="sxs-lookup"><span data-stu-id="2a801-105">There are application behaviors that may work acceptably well on a local computer, but when run across a network, cause significant performance degradation and resource consumption.</span></span> <span data-ttu-id="2a801-106">Les comportements d’application suivants doivent être évités lors du développement d’applications Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="2a801-106">The following application behaviors should be avoided when developing Windows Sockets applications.</span></span>

## <a name="behaviors-to-avoid"></a><span data-ttu-id="2a801-107">Comportements à éviter</span><span class="sxs-lookup"><span data-stu-id="2a801-107">Behaviors to Avoid</span></span>

-   <span data-ttu-id="2a801-108">Applications bavardes.</span><span class="sxs-lookup"><span data-stu-id="2a801-108">Chatty Applications.</span></span>

    <span data-ttu-id="2a801-109">Certaines applications effectuent de nombreuses petites transactions.</span><span class="sxs-lookup"><span data-stu-id="2a801-109">Some applications perform many small transactions.</span></span> <span data-ttu-id="2a801-110">En cas de combinaison avec la surcharge du réseau associée à chaque transaction, l’effet est multiplié.</span><span class="sxs-lookup"><span data-stu-id="2a801-110">When combined with the network overhead associated with each such transaction, the effect is multiplied.</span></span> <span data-ttu-id="2a801-111">Dans la mise en réseau, les petites transactions peuvent consommer autant de ressources et autant de fois que de grandes transactions.</span><span class="sxs-lookup"><span data-stu-id="2a801-111">In networking, small transactions can consume as many resources and as much time as large transactions.</span></span> <span data-ttu-id="2a801-112">Une meilleure approche consiste à combiner de nombreuses petites transactions en une seule transaction de grande taille.</span><span class="sxs-lookup"><span data-stu-id="2a801-112">A better approach is to combine many small transactions into a single large transaction.</span></span>

-   <span data-ttu-id="2a801-113">Transactions sérialisées.</span><span class="sxs-lookup"><span data-stu-id="2a801-113">Serialized Transactions.</span></span>

    <span data-ttu-id="2a801-114">Une sérialisation inutile des transactions peut entraîner des performances médiocres et un impact sur l’évolutivité.</span><span class="sxs-lookup"><span data-stu-id="2a801-114">Unnecessary serialization of transactions can result in poor performance, and affect scalability.</span></span> <span data-ttu-id="2a801-115">Par exemple, 1000 transactions sérialisées prennent au moins 1000 temps \* RTT pour se terminer.</span><span class="sxs-lookup"><span data-stu-id="2a801-115">For example, 1000 serialized transactions take at least 1000 \* RTT to complete.</span></span> <span data-ttu-id="2a801-116">Une meilleure approche consiste à exécuter des transactions non liées en parallèle.</span><span class="sxs-lookup"><span data-stu-id="2a801-116">A better approach is to run unrelated transactions in parallel.</span></span> <span data-ttu-id="2a801-117">Lorsque des applications sérialisées sont associées à des applications bavardes, la réactivité peut être sérieusement gênée.</span><span class="sxs-lookup"><span data-stu-id="2a801-117">When serialized applications are combined with chatty applications, responsiveness can be seriously hampered.</span></span>

    > [!Note]  
    > <span data-ttu-id="2a801-118">La désérialisation d’une application peut s’avérer difficile.</span><span class="sxs-lookup"><span data-stu-id="2a801-118">Properly deserializing an application can be difficult.</span></span> <span data-ttu-id="2a801-119">Si la modification de la sérialisation en parallèle prouve trop difficile, envisagez de combiner plusieurs transactions en moins de transactions volumineuses.</span><span class="sxs-lookup"><span data-stu-id="2a801-119">If changing from serialized to parallel proves too difficult, consider combining multiple transactions into fewer large transactions.</span></span>

     

-   <span data-ttu-id="2a801-120">Transactions FAT.</span><span class="sxs-lookup"><span data-stu-id="2a801-120">Fat Transactions.</span></span>

    <span data-ttu-id="2a801-121">Les applications qui envoient des octets inutiles sur le réseau sont considérées comme des applications FAT.</span><span class="sxs-lookup"><span data-stu-id="2a801-121">Applications that send unnecessary bytes on the network are considered fat applications.</span></span> <span data-ttu-id="2a801-122">Les applications qui envoient des octets inutiles sur le réseau augmentent la surcharge du réseau et les performances sont gênées.</span><span class="sxs-lookup"><span data-stu-id="2a801-122">Applications that send unnecessary bytes on the network increase network overhead, and performance is hampered.</span></span> <span data-ttu-id="2a801-123">Cette situation provient souvent de structures de données inefficaces ou d’une diffusion de données inefficace.</span><span class="sxs-lookup"><span data-stu-id="2a801-123">This situation often comes from inefficient data structures or inefficient data streaming.</span></span> <span data-ttu-id="2a801-124">Pour y remédier, optimisez les structures de données ou envisagez d’utiliser la compression.</span><span class="sxs-lookup"><span data-stu-id="2a801-124">To remedy this, optimize data structures, or consider using compression.</span></span>

<span data-ttu-id="2a801-125">Les sections suivantes traitent des aspects du développement d’applications à prendre en compte.</span><span class="sxs-lookup"><span data-stu-id="2a801-125">The following sections address aspects of application development to consider.</span></span>

-   [<span data-ttu-id="2a801-126">Problèmes spécifiques à TCP/IP</span><span class="sxs-lookup"><span data-stu-id="2a801-126">TCP/IP-specific Issues</span></span>](tcp-ip-specific-issues-2.md)
-   [<span data-ttu-id="2a801-127">Reconnaître les applications lentes</span><span class="sxs-lookup"><span data-stu-id="2a801-127">Recognizing Slow Applications</span></span>](recognizing-slow-applications-2.md)
-   [<span data-ttu-id="2a801-128">Calcul de la surcharge avec netstat</span><span class="sxs-lookup"><span data-stu-id="2a801-128">Calculating Overhead with Netstat</span></span>](calculating-overhead-with-netstat-2.md)

## <a name="related-topics"></a><span data-ttu-id="2a801-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2a801-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a801-130">Applications Windows Sockets hautes performances</span><span class="sxs-lookup"><span data-stu-id="2a801-130">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



