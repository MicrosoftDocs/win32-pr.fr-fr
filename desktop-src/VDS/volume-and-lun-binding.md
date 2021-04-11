---
description: Liaison de volume et de numéro d’unité logique
ms.assetid: ae32b354-799e-4f9b-8989-02bd95968210
title: Liaison de volume et de numéro d’unité logique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9f62e599f5b5e457a1ce6dbf6a52524d1b80d1
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104211156"
---
# <a name="volume-and-lun-binding"></a><span data-ttu-id="8a6fc-103">Liaison de volume et de numéro d’unité logique</span><span class="sxs-lookup"><span data-stu-id="8a6fc-103">Volume and LUN Binding</span></span>

<span data-ttu-id="8a6fc-104">\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8a6fc-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="8a6fc-105">La liaison est la création de volumes ou de numéros d’unités logiques.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-105">Binding is the creation of volumes or LUNs.</span></span> <span data-ttu-id="8a6fc-106">Les volumes sont constitués d’étendues de disque et les numéros d’unités logiques sont constitués d’étendues de lecteurs.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-106">Volumes consist of disk extents and LUNs consist of drive extents.</span></span> <span data-ttu-id="8a6fc-107">La liaison sélectionne pour un ensemble de mappages aux ressources physiques et se produit dans un sous-système, dans un Pack, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-107">Binding selects for a set of mappings to physical resources and occurs within a subsystem, within a pack, or both.</span></span> <span data-ttu-id="8a6fc-108">Tous les programmes fournisseurs prennent en charge la liaison partiellement dirigée d’un modèle dans lequel l’appelant spécifie uniquement les attributs de liaison présentant un intérêt particulier, et permet au fournisseur de choisir le reste.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-108">All provider programs support partially directed binding a model in which the caller specifies only those binding attributes of particular interest, and allows the provider to choose the rest.</span></span> <span data-ttu-id="8a6fc-109">Les opérations dans VDS pour les volumes de liaison et les numéros d’unités logiques sont similaires, mais pas identiques.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-109">The operations in VDS for binding volumes and LUNs are similar but not identical.</span></span> <span data-ttu-id="8a6fc-110">Par exemple, les fournisseurs de matériel peuvent offrir des options de liaison supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-110">For example, hardware providers can offer additional binding options.</span></span>

<span data-ttu-id="8a6fc-111">VDS prend en charge les cinq types de liaison de volume et LUN suivants pour les configurations partiellement dirigées.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-111">VDS supports the following five volume and LUN binding types for partially directed configurations.</span></span> <span data-ttu-id="8a6fc-112">(Les fournisseurs de matériel peuvent et prennent en charge de nombreuses autres liaisons.)</span><span class="sxs-lookup"><span data-stu-id="8a6fc-112">(Hardware providers can and do support many other bindings.)</span></span>



| <span data-ttu-id="8a6fc-113">Terme</span><span class="sxs-lookup"><span data-stu-id="8a6fc-113">Term</span></span>                                                                                                                                             | <span data-ttu-id="8a6fc-114">Description</span><span class="sxs-lookup"><span data-stu-id="8a6fc-114">Description</span></span>                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a6fc-115"><span id="Simple"></span><span id="simple"></span><span id="SIMPLE"></span>Simple</span><span class="sxs-lookup"><span data-stu-id="8a6fc-115"><span id="Simple"></span><span id="simple"></span><span id="SIMPLE"></span>Simple</span></span><br/>                                                     | <span data-ttu-id="8a6fc-116">Mappage linéaire avec une seule étendue contiguë.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-116">Linear mapping with one and only one contiguous extent.</span></span><br/>                             |
| <span data-ttu-id="8a6fc-117"><span id="Spanned"></span><span id="spanned"></span><span id="SPANNED"></span>Fractionnés</span><span class="sxs-lookup"><span data-stu-id="8a6fc-117"><span id="Spanned"></span><span id="spanned"></span><span id="SPANNED"></span>Spanned</span></span><br/>                                                 | <span data-ttu-id="8a6fc-118">Mappage linéaire avec plusieurs extensions non contiguës sur plusieurs disques ou lecteurs.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-118">Linear mapping with multiple noncontiguous extents across multiple disks or drives.</span></span><br/> |
| <span data-ttu-id="8a6fc-119"><span id="Striped"></span><span id="striped"></span><span id="STRIPED"></span>Agrégés par bandes</span><span class="sxs-lookup"><span data-stu-id="8a6fc-119"><span id="Striped"></span><span id="striped"></span><span id="STRIPED"></span>Striped</span></span><br/>                                                 | <span data-ttu-id="8a6fc-120">Le mappage qui entrelace les extensions de volume contiguës sur plusieurs disques ou lecteurs.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-120">Mapping that interleaves contiguous volume extents across multiple disks or drives.</span></span><br/> |
| <span data-ttu-id="8a6fc-121"><span id="Mirrored"></span><span id="mirrored"></span><span id="MIRRORED"></span>Mise en miroir</span><span class="sxs-lookup"><span data-stu-id="8a6fc-121"><span id="Mirrored"></span><span id="mirrored"></span><span id="MIRRORED"></span>Mirrored</span></span><br/>                                             | <span data-ttu-id="8a6fc-122">Mappage qui gère au moins deux copies de données identiques.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-122">Mapping that maintains two or more identical data copies.</span></span><br/>                           |
| <span data-ttu-id="8a6fc-123"><span id="Striped_with_parity"></span><span id="striped_with_parity"></span><span id="STRIPED_WITH_PARITY"></span>Agrégé par bandes avec parité</span><span class="sxs-lookup"><span data-stu-id="8a6fc-123"><span id="Striped_with_parity"></span><span id="striped_with_parity"></span><span id="STRIPED_WITH_PARITY"></span>Striped with parity</span></span><br/> | <span data-ttu-id="8a6fc-124">Mappage qui distribue les informations de vérification de parité sur plusieurs disques ou lecteurs.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-124">Mapping that distributes parity check information across multiple disks or drives.</span></span><br/>  |



 

<span data-ttu-id="8a6fc-125">VDS crée des liaisons miroir, agrégées par bandes et agrégées par bandes à partir de plusieurs membres.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-125">VDS constructs mirrored, striped, and striped with parity bindings from more than one member.</span></span> <span data-ttu-id="8a6fc-126">Par exemple, un miroir bidirectionnel a deux membres.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-126">For example, a two-way mirror has two members.</span></span> <span data-ttu-id="8a6fc-127">Chaque membre peut occuper des étendues sur plusieurs disques ou lecteurs.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-127">Each member can occupy extents on more than one disk or drive.</span></span> <span data-ttu-id="8a6fc-128">VDS concatène les étendues pour former le membre, puis lie le volume ou le numéro d’unité logique sur les membres.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-128">VDS concatenates the extents to form the member and then binds the volume or LUN on the members.</span></span> <span data-ttu-id="8a6fc-129">Un fournisseur peut prendre en charge tous les types de liaison, ou n’importe quel sous-ensemble.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-129">A provider can support all binding types, or any subset.</span></span> <span data-ttu-id="8a6fc-130">Dans le modèle objet VDS, chaque membre d’un miroir est un objet indépendant appelé Plex.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-130">In the VDS object model, each member of a mirror is an independent object called a plex.</span></span>

<span data-ttu-id="8a6fc-131">Là encore, les types de volume et de LUN sont similaires, mais pas exacts.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-131">Again, volume and LUN types are similar, but not exact.</span></span> <span data-ttu-id="8a6fc-132">Pour obtenir une description des types de volumes, consultez l' [objet volume](volume-object.md). pour les types de LUN, consultez l' [objet lun](lun-object.md).</span><span class="sxs-lookup"><span data-stu-id="8a6fc-132">For a description of volume types, see the [Volume Object](volume-object.md); for LUN types, see the [LUN Object](lun-object.md).</span></span> <span data-ttu-id="8a6fc-133">Les types de liaison n’ont pas de tolérance de panne ou de tolérance de panne.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-133">Binding types are either non-fault tolerant or fault tolerant.</span></span>

### <a name="non-fault-tolerant-binding"></a><span data-ttu-id="8a6fc-134">Liaison non tolérante aux pannes</span><span class="sxs-lookup"><span data-stu-id="8a6fc-134">Non-Fault Tolerant Binding</span></span>

<span data-ttu-id="8a6fc-135">Les volumes non tolérants aux pannes et les numéros d’unités logiques n’offrent pas de récupération d’urgence.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-135">Non-fault tolerant volumes and LUNs do not offer disaster recovery.</span></span> <span data-ttu-id="8a6fc-136">Si l’un des piles qui contribue à un volume ou un numéro d’unité logique non tolérant aux pannes échoue, l’intégralité du volume ou de la LUN échoue.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-136">If one of the spindles that contributes to a non-fault tolerant volume or LUN fails, the entire volume or LUN fails.</span></span> <span data-ttu-id="8a6fc-137">En échange des risques de données, les volumes à tolérance de panne et les LUN offrent des performances d’entrée/sortie qui sont généralement supérieures à celles des volumes à tolérance de pannes et des numéros d’unités logiques.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-137">In exchange for the risk to data, non-fault tolerant volumes and LUNs offer input/output performance that is generally superior to that of fault tolerant volumes and LUNs.</span></span> <span data-ttu-id="8a6fc-138">VDS prend en charge les trois types suivants non tolérants aux pannes : simple, fractionné et agrégé par bandes.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-138">VDS supports the following three non-fault tolerant types: simple, spanned, and striped.</span></span>

<span data-ttu-id="8a6fc-139">Simple</span><span class="sxs-lookup"><span data-stu-id="8a6fc-139">Simple</span></span>

![Diagramme illustrant un type simple à tolérance de pannes avec 2 packs et 2 sous-systèmes.](images/vdssimplelunvol.png)

<span data-ttu-id="8a6fc-141">Réparti</span><span class="sxs-lookup"><span data-stu-id="8a6fc-141">Spanned</span></span>

![Diagramme qui montre un type non tolérant aux pannes avec 1 Pack et un sous-système.](images/vdsspanlunvol.png)

<span data-ttu-id="8a6fc-143">Agrégés par bandes</span><span class="sxs-lookup"><span data-stu-id="8a6fc-143">Striped</span></span>

![Diagramme qui montre un type entrelacé non tolérant aux pannes avec 1 Pack et 1 sous-système.](images/vdsstripelunvol.png)

### <a name="fault-tolerant-binding"></a><span data-ttu-id="8a6fc-145">Liaison à tolérance de panne</span><span class="sxs-lookup"><span data-stu-id="8a6fc-145">Fault Tolerant Binding</span></span>

<span data-ttu-id="8a6fc-146">Les volumes à tolérance de panne et les numéros d’unités logiques suivants offrent une récupération d’urgence.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-146">The following fault tolerant volumes and LUNs offer disaster recovery.</span></span> <span data-ttu-id="8a6fc-147">Si l’un des piles qui contribue à un volume à tolérance de panne ou à un numéro d’unité logique (LUN) tombe en panne, les données peuvent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-147">If one of the spindles that contributes to a fault tolerant volume or LUN fails, the data can be recovered.</span></span> <span data-ttu-id="8a6fc-148">Dans Exchange pour la sécurité des données, les performances d’entrée/sortie des volumes à tolérance de pannes et des numéros d’unités logiques sont généralement inférieures à celles des volumes et des numéros d’unités logiques non tolérants aux pannes.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-148">In exchange for data security, the input/output performance of fault tolerant volumes and LUNs is generally inferior to that of non-fault tolerant volumes and LUNs.</span></span> <span data-ttu-id="8a6fc-149">VDS prend en charge deux types de tolérance de panne : mis en miroir et agrégé par bandes avec parité.</span><span class="sxs-lookup"><span data-stu-id="8a6fc-149">VDS supports two fault tolerant types: mirrored and striped with parity.</span></span>

<span data-ttu-id="8a6fc-150">En miroir (miroir triple)</span><span class="sxs-lookup"><span data-stu-id="8a6fc-150">Mirrored (three-way mirror)</span></span>

![Diagramme illustrant un type de tolérance de panne en miroir (miroir 3-Way).](images/vdsmirrorlunvol.png)

<span data-ttu-id="8a6fc-152">Agrégé par bandes avec parité</span><span class="sxs-lookup"><span data-stu-id="8a6fc-152">Striped with parity</span></span>

![Diagramme qui montre un type de tolérance de panne de parité agrégé par bandes.](images/vdsstripeparitylunvol.png)

## <a name="related-topics"></a><span data-ttu-id="8a6fc-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8a6fc-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a6fc-155">Présentation de la configuration</span><span class="sxs-lookup"><span data-stu-id="8a6fc-155">Configuration Overview</span></span>](configuration.md)
</dt> <dt>

[<span data-ttu-id="8a6fc-156">Objet volume</span><span class="sxs-lookup"><span data-stu-id="8a6fc-156">Volume Object</span></span>](volume-object.md)
</dt> <dt>

[<span data-ttu-id="8a6fc-157">LUN (objet)</span><span class="sxs-lookup"><span data-stu-id="8a6fc-157">LUN Object</span></span>](lun-object.md)
</dt> </dl>

 

