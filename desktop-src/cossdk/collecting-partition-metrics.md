---
description: Collecte des métriques de partition
ms.assetid: 2dc35011-24fa-49df-9cf8-96db2de39efa
title: Collecte des métriques de partition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6467dfb9c891e7ae57505c8ec3815bfa99e49d8a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110410"
---
# <a name="collecting-partition-metrics"></a><span data-ttu-id="c4caf-103">Collecte des métriques de partition</span><span class="sxs-lookup"><span data-stu-id="c4caf-103">Collecting Partition Metrics</span></span>

<span data-ttu-id="c4caf-104">Dans certains cas, une organisation peut souhaiter collecter des informations sur l’utilisation des applications COM+ dans le cadre de la surveillance, de la planification de la capacité et de la gestion des ressources.</span><span class="sxs-lookup"><span data-stu-id="c4caf-104">In some cases, an organization might want to collect information on COM+ application use for the purposes of monitoring, capacity planning, and resource accounting.</span></span>

<span data-ttu-id="c4caf-105">Par exemple, un fournisseur de services d’application (ASP) peut vouloir payer un client pour son utilisation des ressources.</span><span class="sxs-lookup"><span data-stu-id="c4caf-105">For example, an application service provider (ASP) might want to charge a customer for its resource usage.</span></span> <span data-ttu-id="c4caf-106">Pour ce faire, COM+ vous permet de collecter des informations sur les événements et les métriques sur une base par partition.</span><span class="sxs-lookup"><span data-stu-id="c4caf-106">To do this, COM+ allows you to collect event and metrics information on a per-partition basis.</span></span>

<span data-ttu-id="c4caf-107">Pour collecter ces informations pour une partition spécifique, vous pouvez spécifier, pour chaque interface COM+ instrumentation, le membre ID de partition dans la structure d’événement standard.</span><span class="sxs-lookup"><span data-stu-id="c4caf-107">The way to collect this information for a specific partition is by specifying, for each COM+ instrumentation interface, the partition ID member within the standard event structure.</span></span> <span data-ttu-id="c4caf-108">La structure d’événement est la première valeur d’une interface d’instrumentation COM+.</span><span class="sxs-lookup"><span data-stu-id="c4caf-108">The event structure is the first value of a COM+ instrumentation interface.</span></span> <span data-ttu-id="c4caf-109">Pour plus d’informations, consultez [interfaces d’instrumentation com+](com--instrumentation-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="c4caf-109">For more information, see [COM+ Instrumentation Interfaces](com--instrumentation-interfaces.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4caf-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c4caf-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4caf-111">Configuration du cache de partition</span><span class="sxs-lookup"><span data-stu-id="c4caf-111">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="c4caf-112">Regroupement d’applications en partitions</span><span class="sxs-lookup"><span data-stu-id="c4caf-112">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="c4caf-113">Gestion des partitions locales</span><span class="sxs-lookup"><span data-stu-id="c4caf-113">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="c4caf-114">Gestion des partitions dans Active Directory</span><span class="sxs-lookup"><span data-stu-id="c4caf-114">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="c4caf-115">Définition des droits d’administration pour une partition</span><span class="sxs-lookup"><span data-stu-id="c4caf-115">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



