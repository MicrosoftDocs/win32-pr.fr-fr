---
description: La disponibilité est la capacité d’une application à tolérer les défaillances dans les ressources du serveur.
ms.assetid: 5d9a8216-a568-4443-b94f-1b2f2827a4be
title: Conception pour la disponibilité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222583c9f53a1ccc88f2a4f984f445de02a2c976
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523548"
---
# <a name="designing-for-availability"></a><span data-ttu-id="75ba1-103">Conception pour la disponibilité</span><span class="sxs-lookup"><span data-stu-id="75ba1-103">Designing for Availability</span></span>

<span data-ttu-id="75ba1-104">La disponibilité est la capacité d’une application à tolérer les défaillances dans les ressources du serveur.</span><span class="sxs-lookup"><span data-stu-id="75ba1-104">Availability is the ability of an application to tolerate failures in server resources.</span></span> <span data-ttu-id="75ba1-105">Cela signifie que le client continue à être traité par la défaillance et que, idéalement, l’échec est transparent pour le client.</span><span class="sxs-lookup"><span data-stu-id="75ba1-105">This means that the client continues to be served through the failure and that, ideally, the failure is transparent to the client.</span></span> <span data-ttu-id="75ba1-106">Évidemment, l’échec peut provenir de sources matérielles ou logicielles. vous devez donc développer dans les deux cas.</span><span class="sxs-lookup"><span data-stu-id="75ba1-106">Obviously, the failure can come from either hardware or software sources, so you must develop for both cases.</span></span>

<span data-ttu-id="75ba1-107">La disponibilité peut être affectée par les facteurs suivants :</span><span class="sxs-lookup"><span data-stu-id="75ba1-107">Availability can be affected by the following factors:</span></span>

-   <span data-ttu-id="75ba1-108">Modèle d’application.</span><span class="sxs-lookup"><span data-stu-id="75ba1-108">Application model.</span></span> <span data-ttu-id="75ba1-109">Pour la haute disponibilité, assurez-vous que la logique d’application critique est effectuée à l’aide du service de [transactions com+](com--transactions.md) .</span><span class="sxs-lookup"><span data-stu-id="75ba1-109">For highest availability, ensure that the critical application logic is conducted using the [COM+ transactions](com--transactions.md) service.</span></span> <span data-ttu-id="75ba1-110">En outre, l’utilisation d’un mécanisme de compensation peut être efficace pour s’assurer que les ressources restent dans un état sain après des échecs.</span><span class="sxs-lookup"><span data-stu-id="75ba1-110">In addition, using a compensation mechanism can be effective in ensuring that resources remain in a healthy state after failures.</span></span>
-   <span data-ttu-id="75ba1-111">Modèle client.</span><span class="sxs-lookup"><span data-stu-id="75ba1-111">Client model.</span></span> <span data-ttu-id="75ba1-112">Intégrer la logique « réessayer en cas d’échec » à l’application cliente et s’efforcer de dégrader normalement l’application si les ressources ou les services ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="75ba1-112">Integrate "retry on failure" logic into the client application, and strive for a graceful degradation in the application if resources or services are unavailable.</span></span> <span data-ttu-id="75ba1-113">Comprenez ce que le client attend de l’application, et créez une conception qui permet d’autres solutions en cas de défaillance.</span><span class="sxs-lookup"><span data-stu-id="75ba1-113">Understand what the client is expecting from the application, and create a design that allows for alternatives when a failure occurs.</span></span>
-   <span data-ttu-id="75ba1-114">Disponibilité des données/États.</span><span class="sxs-lookup"><span data-stu-id="75ba1-114">Data/state availability.</span></span> <span data-ttu-id="75ba1-115">Pour un accès cohérent aux données persistantes, utilisez le clustering Windows pour assurer la prise en charge du basculement.</span><span class="sxs-lookup"><span data-stu-id="75ba1-115">For consistent access to persistent data, use Windows Clustering to provide failover support.</span></span>
-   <span data-ttu-id="75ba1-116">Disponibilité du service.</span><span class="sxs-lookup"><span data-stu-id="75ba1-116">Service availability.</span></span> <span data-ttu-id="75ba1-117">Vous pouvez utiliser l’équilibrage de la charge réseau pour équilibrer la charge des demandes IP entrantes sur un cluster de serveurs.</span><span class="sxs-lookup"><span data-stu-id="75ba1-117">You can use Network Load Balancing to load balance incoming IP requests across a cluster of servers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75ba1-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="75ba1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75ba1-119">Conception pour le déploiement</span><span class="sxs-lookup"><span data-stu-id="75ba1-119">Designing for Deployment</span></span>](designing-for-deployment.md)
</dt> <dt>

[<span data-ttu-id="75ba1-120">Conception pour l’évolutivité</span><span class="sxs-lookup"><span data-stu-id="75ba1-120">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> <dt>

[<span data-ttu-id="75ba1-121">Conception pour la sécurité</span><span class="sxs-lookup"><span data-stu-id="75ba1-121">Designing for Security</span></span>](designing-for-security.md)
</dt> </dl>

 

 



