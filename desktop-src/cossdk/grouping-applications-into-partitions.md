---
description: Regroupement d’applications en partitions
ms.assetid: bdfe2428-9769-4bcb-b74e-a141ba67a67e
title: Regroupement d’applications en partitions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b35c726662d7dbe2cf039678ba5cdb4f94eeea
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514760"
---
# <a name="grouping-applications-into-partitions"></a><span data-ttu-id="d2e2a-103">Regroupement d’applications en partitions</span><span class="sxs-lookup"><span data-stu-id="d2e2a-103">Grouping Applications into Partitions</span></span>

<span data-ttu-id="d2e2a-104">Lorsque vous décidez comment regrouper des applications en partitions, les administrateurs doivent être conscients de certaines règles et restrictions, y compris les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d2e2a-104">When deciding how to group applications into partitions, administrators need to be aware of certain rules and restrictions, including the following:</span></span>

-   <span data-ttu-id="d2e2a-105">Une application peut être installée dans une ou plusieurs partitions.</span><span class="sxs-lookup"><span data-stu-id="d2e2a-105">An application can be installed into one or more partitions.</span></span>
-   <span data-ttu-id="d2e2a-106">Une seule instance d’un composant donné peut exister dans une application.</span><span class="sxs-lookup"><span data-stu-id="d2e2a-106">Only one instance of a given component can exist in an application.</span></span>

## <a name="public-and-private-components"></a><span data-ttu-id="d2e2a-107">Composants publics et privés</span><span class="sxs-lookup"><span data-stu-id="d2e2a-107">Public and Private Components</span></span>

<span data-ttu-id="d2e2a-108">D’autres restrictions existent quand vous décidez comment grouper des applications COM+.</span><span class="sxs-lookup"><span data-stu-id="d2e2a-108">Other restrictions exist when deciding how to group COM+ applications.</span></span> <span data-ttu-id="d2e2a-109">Ces restrictions s’appliquent aux composants publics et privés au sein d’une application.</span><span class="sxs-lookup"><span data-stu-id="d2e2a-109">These restrictions pertain to public versus private components within an application.</span></span> <span data-ttu-id="d2e2a-110">Les composants de l’application peuvent généralement être publics ou privés.</span><span class="sxs-lookup"><span data-stu-id="d2e2a-110">Application components can generally be either public or private.</span></span> <span data-ttu-id="d2e2a-111">Toutefois, lorsque vous regroupez des applications en partitions, les administrateurs doivent tenir compte de certaines restrictions concernant les composants publics et privés.</span><span class="sxs-lookup"><span data-stu-id="d2e2a-111">However, when grouping applications into partitions, administrators should be aware of some restrictions around public and private components.</span></span> <span data-ttu-id="d2e2a-112">Le tableau suivant répertorie ces restrictions.</span><span class="sxs-lookup"><span data-stu-id="d2e2a-112">The following table lists these restrictions.</span></span>



| <span data-ttu-id="d2e2a-113">Si une application est :</span><span class="sxs-lookup"><span data-stu-id="d2e2a-113">If an application is:</span></span>              | <span data-ttu-id="d2e2a-114">Les composants d’une partition peuvent être :</span><span class="sxs-lookup"><span data-stu-id="d2e2a-114">Then components in a partition can be:</span></span>                                                                                   |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2e2a-115">Une application serveur</span><span class="sxs-lookup"><span data-stu-id="d2e2a-115">A server application</span></span><br/>    | <span data-ttu-id="d2e2a-116">Public et privé.</span><span class="sxs-lookup"><span data-stu-id="d2e2a-116">Public and private.</span></span><br/>                                                                                           |
| <span data-ttu-id="d2e2a-117">Une application de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d2e2a-117">A library application</span></span><br/>   | <span data-ttu-id="d2e2a-118">Public uniquement.</span><span class="sxs-lookup"><span data-stu-id="d2e2a-118">Public only.</span></span> <span data-ttu-id="d2e2a-119">Dans le cas contraire, l’application appelants pourrait avoir les mêmes composants, ce qui créerait une ambiguïté.</span><span class="sxs-lookup"><span data-stu-id="d2e2a-119">Otherwise, the callers application could have the same components, which would create ambiguity.</span></span><br/> |
| <span data-ttu-id="d2e2a-120">Dans la partition globale</span><span class="sxs-lookup"><span data-stu-id="d2e2a-120">In the global partition</span></span><br/> | <span data-ttu-id="d2e2a-121">Public uniquement.</span><span class="sxs-lookup"><span data-stu-id="d2e2a-121">Public only.</span></span> <span data-ttu-id="d2e2a-122">Cela garantit la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="d2e2a-122">This ensures backward compatibility.</span></span><br/>                                                             |



 

## <a name="application-ids"></a><span data-ttu-id="d2e2a-123">ID d’application</span><span class="sxs-lookup"><span data-stu-id="d2e2a-123">Application IDs</span></span>

<span data-ttu-id="d2e2a-124">Chaque application COM+ installée sur un ordinateur possède un ID d’application unique.</span><span class="sxs-lookup"><span data-stu-id="d2e2a-124">Every COM+ application installed on a computer has a unique application ID.</span></span> <span data-ttu-id="d2e2a-125">Toutefois, les noms d’application ne doivent être uniques que dans une seule partition et non sur l’intégralité de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d2e2a-125">However, application names need only be unique within a single partition and not on the entire computer.</span></span>

<span data-ttu-id="d2e2a-126">Le tableau suivant montre ce qui se passe à l’ID d’application lorsqu’une application est importée dans une partition ou exportée à partir d’une partition.</span><span class="sxs-lookup"><span data-stu-id="d2e2a-126">The following table shows what happens to the application ID when an application is imported into a partition or exported from a partition.</span></span>



| <span data-ttu-id="d2e2a-127">Si une application est :</span><span class="sxs-lookup"><span data-stu-id="d2e2a-127">If an application is:</span></span>                                              | <span data-ttu-id="d2e2a-128">Ensuite, l’ID d’application :</span><span class="sxs-lookup"><span data-stu-id="d2e2a-128">Then the application ID:</span></span>                    |
|--------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="d2e2a-129">Importé dans la partition globale</span><span class="sxs-lookup"><span data-stu-id="d2e2a-129">Imported to the global partition</span></span><br/>                        | <span data-ttu-id="d2e2a-130">Reste le même</span><span class="sxs-lookup"><span data-stu-id="d2e2a-130">Remains the same</span></span><br/>                 |
| <span data-ttu-id="d2e2a-131">Importé dans une partition autre que la partition globale</span><span class="sxs-lookup"><span data-stu-id="d2e2a-131">Imported to a partition other than the global partition</span></span><br/> | <span data-ttu-id="d2e2a-132">Est modifié</span><span class="sxs-lookup"><span data-stu-id="d2e2a-132">Is changed</span></span><br/>                       |
| <span data-ttu-id="d2e2a-133">Exporté</span><span class="sxs-lookup"><span data-stu-id="d2e2a-133">Exported</span></span><br/>                                                | <span data-ttu-id="d2e2a-134">Est inclus dans le fichier exporté</span><span class="sxs-lookup"><span data-stu-id="d2e2a-134">Is included in the exported file</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="d2e2a-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d2e2a-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2e2a-136">Collecte des métriques de partition</span><span class="sxs-lookup"><span data-stu-id="d2e2a-136">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="d2e2a-137">Configuration du cache de partition</span><span class="sxs-lookup"><span data-stu-id="d2e2a-137">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="d2e2a-138">Gestion des partitions locales</span><span class="sxs-lookup"><span data-stu-id="d2e2a-138">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="d2e2a-139">Gestion des partitions dans Active Directory</span><span class="sxs-lookup"><span data-stu-id="d2e2a-139">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="d2e2a-140">Définition des droits d’administration pour une partition</span><span class="sxs-lookup"><span data-stu-id="d2e2a-140">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




