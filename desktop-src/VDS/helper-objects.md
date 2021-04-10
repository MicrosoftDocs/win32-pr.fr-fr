---
description: 'VDS fournit deux objets d’assistance : l’objet d’énumération et l’objet Async. Cette rubrique décrit chacun de ces objets et fournit des liens vers des exemples de la façon dont les appelants fonctionnent avec chacun d’eux.'
ms.assetid: 0f809c71-a3bd-4c62-8086-9651ea1a3400
title: Objets d’assistance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac5193003abd10d9fa2c311b250272d9ad5847a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210749"
---
# <a name="helper-objects"></a><span data-ttu-id="230ff-104">Objets d’assistance</span><span class="sxs-lookup"><span data-stu-id="230ff-104">Helper Objects</span></span>

<span data-ttu-id="230ff-105">\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="230ff-105">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="230ff-106">VDS fournit deux objets d’assistance : l’objet d’énumération et l’objet Async.</span><span class="sxs-lookup"><span data-stu-id="230ff-106">VDS provides two helper objects: the enumeration object and the async object.</span></span> <span data-ttu-id="230ff-107">Cette rubrique décrit chacun de ces objets et fournit des liens vers des exemples de la façon dont les appelants fonctionnent avec chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="230ff-107">This topic describes each of these objects and provides links to examples of how callers work with each.</span></span>

## <a name="enumeration-object"></a><span data-ttu-id="230ff-108">Objet d’énumération</span><span class="sxs-lookup"><span data-stu-id="230ff-108">Enumeration Object</span></span>

<span data-ttu-id="230ff-109">Un objet d’énumération énumère un ensemble d’objets VDS d’un type donné.</span><span class="sxs-lookup"><span data-stu-id="230ff-109">An enumeration object enumerates through a set of VDS objects of a given type.</span></span> <span data-ttu-id="230ff-110">Les objets peuvent être des fournisseurs, des sous-systèmes, des contrôleurs, des numéros d’unités logiques, des plex LUN, des lecteurs, des disques, des disques, des volumes ou des plex de volume.</span><span class="sxs-lookup"><span data-stu-id="230ff-110">Objects can be providers, subsystems, controllers, LUNs, LUN plexes, drives, disk packs, disks, volumes, or volume plexes.</span></span> <span data-ttu-id="230ff-111">Les appelants peuvent obtenir un pointeur vers un objet spécifique en sélectionnant l’objet souhaité à partir de l’énumération retournée par la méthode appropriée.</span><span class="sxs-lookup"><span data-stu-id="230ff-111">Callers can get a pointer to a specific object by selecting the desired object from the enumeration that is returned by the appropriate method.</span></span> <span data-ttu-id="230ff-112">Pour obtenir un exemple de code, consultez [utilisation des objets d’énumération](working-with-enumeration-objects.md).</span><span class="sxs-lookup"><span data-stu-id="230ff-112">For a code example, see [Working with Enumeration Objects](working-with-enumeration-objects.md).</span></span>

<span data-ttu-id="230ff-113">Le tableau suivant répertorie les interfaces, énumérations et structures associées.</span><span class="sxs-lookup"><span data-stu-id="230ff-113">The following table lists related interfaces, enumerations, and structures.</span></span> 

| <span data-ttu-id="230ff-114">Type</span><span class="sxs-lookup"><span data-stu-id="230ff-114">Type</span></span>                                              | <span data-ttu-id="230ff-115">Élément</span><span class="sxs-lookup"><span data-stu-id="230ff-115">Element</span></span>                                  |
|---------------------------------------------------|------------------------------------------|
| <span data-ttu-id="230ff-116">Interfaces toujours exposées par cet objet</span><span class="sxs-lookup"><span data-stu-id="230ff-116">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="230ff-117">**IEnumVdsObject**</span><span class="sxs-lookup"><span data-stu-id="230ff-117">**IEnumVdsObject**</span></span>](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) |
| <span data-ttu-id="230ff-118">Énumérations associées</span><span class="sxs-lookup"><span data-stu-id="230ff-118">Associated enumerations</span></span>                           | <span data-ttu-id="230ff-119">Aucun</span><span class="sxs-lookup"><span data-stu-id="230ff-119">None.</span></span>                                    |
| <span data-ttu-id="230ff-120">Structures associées</span><span class="sxs-lookup"><span data-stu-id="230ff-120">Associated structures</span></span>                             | <span data-ttu-id="230ff-121">Aucun</span><span class="sxs-lookup"><span data-stu-id="230ff-121">None.</span></span>                                    |



 

## <a name="async-object"></a><span data-ttu-id="230ff-122">Objet Async</span><span class="sxs-lookup"><span data-stu-id="230ff-122">Async Object</span></span>

<span data-ttu-id="230ff-123">Un objet Async gère les opérations asynchrones.</span><span class="sxs-lookup"><span data-stu-id="230ff-123">An async object manages asynchronous operations.</span></span> <span data-ttu-id="230ff-124">Les méthodes qui lancent des opérations asynchrones retournent un pointeur vers une interface [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) , qui permet à l’appelant d’annuler, d’attendre et de demander l’état de l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="230ff-124">Methods that initiate asynchronous operations return a pointer to an [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) interface, which allows the caller to cancel, wait for, and query the status of the asynchronous operation.</span></span>

<span data-ttu-id="230ff-125">Les opérations VDS de longue durée ont tendance à être implémentées de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="230ff-125">Long-running VDS operations tend to be implemented asynchronously.</span></span> <span data-ttu-id="230ff-126">Les programmes de base et dynamiques du fournisseur de logiciels implémentent des méthodes asynchrones de manière cohérente pour les opérations de volume, de partition et de disque.</span><span class="sxs-lookup"><span data-stu-id="230ff-126">The basic and dynamic software provider programs implement asynchronous methods consistently for volume, partition, and disk operations.</span></span> <span data-ttu-id="230ff-127">Les fournisseurs de matériel implémentent éventuellement des méthodes asynchrones asynchrones.</span><span class="sxs-lookup"><span data-stu-id="230ff-127">Hardware providers optionally implement async-related methods asynchronously.</span></span> <span data-ttu-id="230ff-128">Quelle que soit la façon dont le fournisseur implémente la méthode, l’opération doit retourner un pointeur vers une interface [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="230ff-128">Regardless of how the provider implements the method, the operation must return a pointer to an [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) interface to the caller.</span></span> <span data-ttu-id="230ff-129">Pour obtenir un exemple de code, consultez [gestion des opérations asynchrones](managing-asynchronous-operations.md).</span><span class="sxs-lookup"><span data-stu-id="230ff-129">For a code example, see [Managing Asynchronous Operations](managing-asynchronous-operations.md).</span></span>

<span data-ttu-id="230ff-130">Les opérations asynchrones sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="230ff-130">Asynchronous operations include:</span></span>

-   <span data-ttu-id="230ff-131">Création d’un numéro d’unité logique (LUN), d’un volume ou d’une partition.</span><span class="sxs-lookup"><span data-stu-id="230ff-131">Creating a LUN, volume, or partition.</span></span>
-   <span data-ttu-id="230ff-132">Formatage d’un volume ou d’une partition.</span><span class="sxs-lookup"><span data-stu-id="230ff-132">Formatting a volume or partition.</span></span>
-   <span data-ttu-id="230ff-133">Ajout ou suppression d’un numéro d’unité logique ou d’un plex de volume.</span><span class="sxs-lookup"><span data-stu-id="230ff-133">Adding or removing a LUN or volume plex.</span></span>
-   <span data-ttu-id="230ff-134">Interruption d’un plex de volume.</span><span class="sxs-lookup"><span data-stu-id="230ff-134">Breaking a volume plex.</span></span>
-   <span data-ttu-id="230ff-135">Extension ou réduction d’un numéro d’unité logique ou d’un volume.</span><span class="sxs-lookup"><span data-stu-id="230ff-135">Extending or shrinking a LUN or volume.</span></span>
-   <span data-ttu-id="230ff-136">Récupération d’un numéro d’unité logique ou d’un volume.</span><span class="sxs-lookup"><span data-stu-id="230ff-136">Recovering a LUN or volume.</span></span>
-   <span data-ttu-id="230ff-137">Nettoyage d’un disque.</span><span class="sxs-lookup"><span data-stu-id="230ff-137">Cleaning a disk.</span></span>
-   <span data-ttu-id="230ff-138">Remplacement d’un disque.</span><span class="sxs-lookup"><span data-stu-id="230ff-138">Replacing a disk.</span></span>

<span data-ttu-id="230ff-139">Le tableau suivant répertorie les interfaces, énumérations et structures associées.</span><span class="sxs-lookup"><span data-stu-id="230ff-139">The following table lists related interfaces, enumerations, and structures.</span></span> 

| <span data-ttu-id="230ff-140">Type</span><span class="sxs-lookup"><span data-stu-id="230ff-140">Type</span></span>                                              | <span data-ttu-id="230ff-141">Élément</span><span class="sxs-lookup"><span data-stu-id="230ff-141">Element</span></span>                        |
|---------------------------------------------------|--------------------------------|
| <span data-ttu-id="230ff-142">Interfaces toujours exposées par cet objet</span><span class="sxs-lookup"><span data-stu-id="230ff-142">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="230ff-143">**IVdsAsync**</span><span class="sxs-lookup"><span data-stu-id="230ff-143">**IVdsAsync**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsasync) |
| <span data-ttu-id="230ff-144">Énumérations associées</span><span class="sxs-lookup"><span data-stu-id="230ff-144">Associated enumerations</span></span>                           | <span data-ttu-id="230ff-145">Aucun</span><span class="sxs-lookup"><span data-stu-id="230ff-145">None.</span></span>                          |
| <span data-ttu-id="230ff-146">Structures associées</span><span class="sxs-lookup"><span data-stu-id="230ff-146">Associated structures</span></span>                             | <span data-ttu-id="230ff-147">Aucun</span><span class="sxs-lookup"><span data-stu-id="230ff-147">None.</span></span>                          |



 

## <a name="related-topics"></a><span data-ttu-id="230ff-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="230ff-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="230ff-149">Modèle d’objet VDS</span><span class="sxs-lookup"><span data-stu-id="230ff-149">VDS Object Model</span></span>](vds-object-model.md)
</dt> <dt>

[<span data-ttu-id="230ff-150">**IVdsAsync**</span><span class="sxs-lookup"><span data-stu-id="230ff-150">**IVdsAsync**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsasync)
</dt> <dt>

[<span data-ttu-id="230ff-151">Utilisation d’objets d’énumération</span><span class="sxs-lookup"><span data-stu-id="230ff-151">Working with Enumeration Objects</span></span>](working-with-enumeration-objects.md)
</dt> <dt>

[<span data-ttu-id="230ff-152">Gestion des opérations asynchrones</span><span class="sxs-lookup"><span data-stu-id="230ff-152">Managing Asynchronous Operations</span></span>](managing-asynchronous-operations.md)
</dt> </dl>

 

 
