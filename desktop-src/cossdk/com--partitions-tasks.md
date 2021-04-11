---
description: Tâches des partitions COM+
ms.assetid: ebcbfced-7d7a-46dc-a728-cdb920ccb874
title: Tâches des partitions COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055976effb5d6a93523bab9d570aec685872ab91
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200929"
---
# <a name="com-partitions-tasks"></a><span data-ttu-id="190f3-103">Tâches des partitions COM+</span><span class="sxs-lookup"><span data-stu-id="190f3-103">COM+ Partitions Tasks</span></span>

<span data-ttu-id="190f3-104">Les rubriques suivantes de cette section fournissent des instructions pas à pas pour l’utilisation des partitions COM+.</span><span class="sxs-lookup"><span data-stu-id="190f3-104">The following topics in this section provide step-by-step instructions for using COM+ partitions.</span></span>

<span data-ttu-id="190f3-105">**Windows XP :** La possibilité de créer, de configurer ou de déléguer des partitions COM+ n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="190f3-105">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="190f3-106">La partition globale est la seule partition COM+ disponible.</span><span class="sxs-lookup"><span data-stu-id="190f3-106">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="190f3-107">\* \* Windows 2000 : \* \* le service partitions COM+ n’est pas disponible dans Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="190f3-107">\*\*Windows 2000:  \*\* The COM+ partitions service is not available in Windows 2000.</span></span>



| <span data-ttu-id="190f3-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="190f3-108">Topic</span></span>                                                                                                         | <span data-ttu-id="190f3-109">Description</span><span class="sxs-lookup"><span data-stu-id="190f3-109">Description</span></span>                                                                                    |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="190f3-110">Création et configuration de partitions COM+</span><span class="sxs-lookup"><span data-stu-id="190f3-110">Creating and Configuring COM+ Partitions</span></span>](creating-and-configuring-com--partitions.md)<br/>           | <span data-ttu-id="190f3-111">Décrit comment créer et configurer une partition COM+.</span><span class="sxs-lookup"><span data-stu-id="190f3-111">Describes how to create and configure a COM+ partition.</span></span><br/>                             |
| [<span data-ttu-id="190f3-112">Gestion des partitions locales</span><span class="sxs-lookup"><span data-stu-id="190f3-112">Managing Local Partitions</span></span>](managing-local-partitions.md)<br/>                                         | <span data-ttu-id="190f3-113">Décrit comment gérer des partitions COM+ qui ne se trouvent pas dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="190f3-113">Describes how to manage COM+ partitions that are not within Active Directory.</span></span><br/>       |
| [<span data-ttu-id="190f3-114">Gestion des partitions dans Active Directory</span><span class="sxs-lookup"><span data-stu-id="190f3-114">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)<br/>     | <span data-ttu-id="190f3-115">Décrit comment gérer les partitions COM+ spécifiées dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="190f3-115">Describes how to manage COM+ partitions that are specified within Active Directory.</span></span><br/> |
| [<span data-ttu-id="190f3-116">Définition des droits d’administration pour une partition</span><span class="sxs-lookup"><span data-stu-id="190f3-116">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)<br/> | <span data-ttu-id="190f3-117">Décrit comment définir des privilèges de sécurité pour une partition COM+.</span><span class="sxs-lookup"><span data-stu-id="190f3-117">Describes how to set security privileges for a COM+ partition.</span></span><br/>                      |
| [<span data-ttu-id="190f3-118">Regroupement d’applications en partitions</span><span class="sxs-lookup"><span data-stu-id="190f3-118">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)<br/>                 | <span data-ttu-id="190f3-119">Décrit comment configurer des applications COM+ pour qu’elles appartiennent à une partition COM+.</span><span class="sxs-lookup"><span data-stu-id="190f3-119">Describes how to configure COM+ applications to belong to a COM+ partition.</span></span> <br/>        |
| [<span data-ttu-id="190f3-120">Collecte des métriques de partition</span><span class="sxs-lookup"><span data-stu-id="190f3-120">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)<br/>                                   | <span data-ttu-id="190f3-121">Décrit comment collecter des données sur les partitions COM+.</span><span class="sxs-lookup"><span data-stu-id="190f3-121">Describes how to collect data about COM+ partitions.</span></span><br/>                                |
| [<span data-ttu-id="190f3-122">Configuration du cache de partition</span><span class="sxs-lookup"><span data-stu-id="190f3-122">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)<br/>                             | <span data-ttu-id="190f3-123">Décrit comment configurer le cache de partition COM+.</span><span class="sxs-lookup"><span data-stu-id="190f3-123">Describes how to configure the COM+ partition cache.</span></span><br/>                                |



 

> [!Note]  
> <span data-ttu-id="190f3-124">Le service partitions COM+ n’est pas activé par défaut.</span><span class="sxs-lookup"><span data-stu-id="190f3-124">The COM+ Partitions service is not enabled by default.</span></span> <span data-ttu-id="190f3-125">Pour utiliser le service partitions COM+, vous devez l’activer par le biais de l’outil d’administration Services de composants ou en modifiant la propriété PartitionsEnabled de la collection [**LocalComputer**](localcomputer.md) sur true.</span><span class="sxs-lookup"><span data-stu-id="190f3-125">To use the COM+ partitions service, you must enable it through the Component Services administration tool or by changing the PartitionsEnabled property on the [**LocalComputer**](localcomputer.md) collection to True.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="190f3-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="190f3-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="190f3-127">Concepts des partitions COM+</span><span class="sxs-lookup"><span data-stu-id="190f3-127">COM+ Partitions Concepts</span></span>](com--partitions-concepts.md)
</dt> </dl>

 

 




