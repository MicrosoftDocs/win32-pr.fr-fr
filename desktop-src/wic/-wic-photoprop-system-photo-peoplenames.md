---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. PeopleNames.
ms.assetid: 567d5542-fc7b-4d19-bc3c-b9d6e26e3387
title: Stratégie de métadonnées de photo System. photo. PeopleNames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c3de9f5adda67fcd0e555194500f109df078bdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535502"
---
# <a name="systemphotopeoplenames-photo-metadata-policy"></a><span data-ttu-id="3dc5f-103">Stratégie de métadonnées de photo System. photo. PeopleNames</span><span class="sxs-lookup"><span data-stu-id="3dc5f-103">System.Photo.PeopleNames Photo Metadata Policy</span></span>

<span data-ttu-id="3dc5f-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. PeopleNames](../properties/props-system-photo-peoplenames.md) .</span><span class="sxs-lookup"><span data-stu-id="3dc5f-104">The photo metadata policy for the [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="3dc5f-105">A-la</span><span class="sxs-lookup"><span data-stu-id="3dc5f-105">PKEY</span></span>

<span data-ttu-id="3dc5f-106">\_Photo \_ PeopleNames</span><span class="sxs-lookup"><span data-stu-id="3dc5f-106">PKEY\_Photo\_PeopleNames</span></span>

### <a name="containers"></a><span data-ttu-id="3dc5f-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="3dc5f-107">Containers</span></span>

<span data-ttu-id="3dc5f-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="3dc5f-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="3dc5f-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3dc5f-109">Read-Only</span></span>

<span data-ttu-id="3dc5f-110">Non</span><span class="sxs-lookup"><span data-stu-id="3dc5f-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="3dc5f-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="3dc5f-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="3dc5f-112">\_LPWStr VT Vector \| VT \_</span><span class="sxs-lookup"><span data-stu-id="3dc5f-112">VT\_VECTOR \| VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="3dc5f-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="3dc5f-113">Input Type</span></span>

<span data-ttu-id="3dc5f-114">StringMulti</span><span class="sxs-lookup"><span data-stu-id="3dc5f-114">StringMulti</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="3dc5f-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="3dc5f-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="3dc5f-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="3dc5f-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="3dc5f-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="3dc5f-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="3dc5f-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="3dc5f-118">Read Paths</span></span>



| <span data-ttu-id="3dc5f-119">Commande</span><span class="sxs-lookup"><span data-stu-id="3dc5f-119">Order</span></span> | <span data-ttu-id="3dc5f-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="3dc5f-120">Path</span></span>                                                           | <span data-ttu-id="3dc5f-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="3dc5f-121">Disk Format</span></span> |
|-------|----------------------------------------------------------------|-------------|
| <span data-ttu-id="3dc5f-122">1</span><span class="sxs-lookup"><span data-stu-id="3dc5f-122">1</span></span>     | <span data-ttu-id="3dc5f-123">/XMP/ <xmpstruct> MP : RegionInfo/ <xmpbag> MPRI : regions</span><span class="sxs-lookup"><span data-stu-id="3dc5f-123">/xmp/<xmpstruct>MP:RegionInfo/<xmpbag>MPRI:Regions</span></span> | <span data-ttu-id="3dc5f-124">ushort</span><span class="sxs-lookup"><span data-stu-id="3dc5f-124">ushort</span></span>      |



 

### <a name="write-paths"></a><span data-ttu-id="3dc5f-125">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="3dc5f-125">Write Paths</span></span>

<span data-ttu-id="3dc5f-126">Impossible d’écrire cette propriété à l’aide de la stratégie de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="3dc5f-126">This property cannot be written using the metadata policy.</span></span>

### <a name="remove-paths"></a><span data-ttu-id="3dc5f-127">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="3dc5f-127">Remove Paths</span></span>



| <span data-ttu-id="3dc5f-128">Commande</span><span class="sxs-lookup"><span data-stu-id="3dc5f-128">Order</span></span> | <span data-ttu-id="3dc5f-129">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="3dc5f-129">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="3dc5f-130">1</span><span class="sxs-lookup"><span data-stu-id="3dc5f-130">1</span></span>     | <span data-ttu-id="3dc5f-131">/XMP/ <xmpstruct> MP : RegionInfo</span><span class="sxs-lookup"><span data-stu-id="3dc5f-131">/xmp/<xmpstruct>MP:RegionInfo</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="3dc5f-132">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="3dc5f-132">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="3dc5f-133">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="3dc5f-133">Read Paths</span></span>



| <span data-ttu-id="3dc5f-134">Commande</span><span class="sxs-lookup"><span data-stu-id="3dc5f-134">Order</span></span> | <span data-ttu-id="3dc5f-135">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="3dc5f-135">Path</span></span>                                                               | <span data-ttu-id="3dc5f-136">Format de disque</span><span class="sxs-lookup"><span data-stu-id="3dc5f-136">Disk Format</span></span> |
|-------|--------------------------------------------------------------------|-------------|
| <span data-ttu-id="3dc5f-137">1</span><span class="sxs-lookup"><span data-stu-id="3dc5f-137">1</span></span>     | <span data-ttu-id="3dc5f-138">/IFD/XMP/ <xmpstruct> MP : RegionInfo/ <xmpbag> MPRI : regions</span><span class="sxs-lookup"><span data-stu-id="3dc5f-138">/ifd/xmp/<xmpstruct>MP:RegionInfo/<xmpbag>MPRI:Regions</span></span> | <span data-ttu-id="3dc5f-139">ushort</span><span class="sxs-lookup"><span data-stu-id="3dc5f-139">ushort</span></span>      |



 

### <a name="write-paths"></a><span data-ttu-id="3dc5f-140">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="3dc5f-140">Write Paths</span></span>

<span data-ttu-id="3dc5f-141">Impossible d’écrire cette propriété à l’aide de la stratégie de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="3dc5f-141">This property cannot be written using the metadata policy.</span></span>

### <a name="remove-paths"></a><span data-ttu-id="3dc5f-142">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="3dc5f-142">Remove Paths</span></span>



| <span data-ttu-id="3dc5f-143">Commande</span><span class="sxs-lookup"><span data-stu-id="3dc5f-143">Order</span></span> | <span data-ttu-id="3dc5f-144">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="3dc5f-144">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="3dc5f-145">1</span><span class="sxs-lookup"><span data-stu-id="3dc5f-145">1</span></span>     | <span data-ttu-id="3dc5f-146">/IFD/XMP/ <xmpstruct> MP : RegionInfo</span><span class="sxs-lookup"><span data-stu-id="3dc5f-146">/ifd/xmp/<xmpstruct>MP:RegionInfo</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3dc5f-147">Notes</span><span class="sxs-lookup"><span data-stu-id="3dc5f-147">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="3dc5f-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3dc5f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dc5f-149">System. photo. ProgramMode</span><span class="sxs-lookup"><span data-stu-id="3dc5f-149">System.Photo.ProgramMode</span></span>](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
