---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. Flash.
ms.assetid: 24b400a4-f4c7-4b59-a9e3-8a20144cd52e
title: Stratégie de métadonnées de photo System. photo. Flash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0302e0f310d2f9a6a4390b0d4856578cc2f43e93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536491"
---
# <a name="systemphotoflash-photo-metadata-policy"></a><span data-ttu-id="040ae-103">Stratégie de métadonnées de photo System. photo. Flash</span><span class="sxs-lookup"><span data-stu-id="040ae-103">System.Photo.Flash Photo Metadata Policy</span></span>

<span data-ttu-id="040ae-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. Flash](../properties/props-system-photo-exposuretime.md) .</span><span class="sxs-lookup"><span data-stu-id="040ae-104">The photo metadata policy for the [System.Photo.Flash](../properties/props-system-photo-exposuretime.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="040ae-105">A-la</span><span class="sxs-lookup"><span data-stu-id="040ae-105">PKEY</span></span>

<span data-ttu-id="040ae-106">Flash de la \_ photo \_</span><span class="sxs-lookup"><span data-stu-id="040ae-106">PKEY\_Photo\_Flash</span></span>

### <a name="containers"></a><span data-ttu-id="040ae-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="040ae-107">Containers</span></span>

<span data-ttu-id="040ae-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="040ae-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="040ae-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="040ae-109">Read-Only</span></span>

<span data-ttu-id="040ae-110">Non</span><span class="sxs-lookup"><span data-stu-id="040ae-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="040ae-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="040ae-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="040ae-112">VT \_ UI1 (si le schéma source était XMP) ou VT \_ UI2 (si le schéma source était EXIF)</span><span class="sxs-lookup"><span data-stu-id="040ae-112">VT\_UI1 (if the source schema was XMP), or VT\_UI2 (if the source schema was EXIF)</span></span>

<span data-ttu-id="040ae-113">\\lang1036</span><span class="sxs-lookup"><span data-stu-id="040ae-113">\\lang1036</span></span>

### <a name="input-type"></a><span data-ttu-id="040ae-114">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="040ae-114">Input Type</span></span>

<span data-ttu-id="040ae-115">VT \_ UI1, VTUI2, VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="040ae-115">VT\_UI1, VTUI2, VT\_UI4</span></span>

<span data-ttu-id="040ae-116">\\lang1033</span><span class="sxs-lookup"><span data-stu-id="040ae-116">\\lang1033</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="040ae-117">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="040ae-117">Conflict Resolution Policy</span></span>

<span data-ttu-id="040ae-118">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="040ae-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="040ae-119">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="040ae-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="040ae-120">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="040ae-120">Read Paths</span></span>



| <span data-ttu-id="040ae-121">Commande</span><span class="sxs-lookup"><span data-stu-id="040ae-121">Order</span></span> | <span data-ttu-id="040ae-122">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="040ae-122">Path</span></span>                             | <span data-ttu-id="040ae-123">Format de disque</span><span class="sxs-lookup"><span data-stu-id="040ae-123">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="040ae-124">1</span><span class="sxs-lookup"><span data-stu-id="040ae-124">1</span></span>     | <span data-ttu-id="040ae-125">/App1/IFD/EXIF/{UShort = 37385}</span><span class="sxs-lookup"><span data-stu-id="040ae-125">/app1/ifd/exif/{ushort=37385}</span></span>    | <span data-ttu-id="040ae-126">ushort</span><span class="sxs-lookup"><span data-stu-id="040ae-126">ushort</span></span>      |
| <span data-ttu-id="040ae-127">2</span><span class="sxs-lookup"><span data-stu-id="040ae-127">2</span></span>     | <span data-ttu-id="040ae-128">/XMP/ <xmpstruct> EXIF : Flash</span><span class="sxs-lookup"><span data-stu-id="040ae-128">/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="040ae-129">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="040ae-129">Write Paths</span></span>



| <span data-ttu-id="040ae-130">Commande</span><span class="sxs-lookup"><span data-stu-id="040ae-130">Order</span></span> | <span data-ttu-id="040ae-131">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="040ae-131">Path</span></span>                             | <span data-ttu-id="040ae-132">Format de disque</span><span class="sxs-lookup"><span data-stu-id="040ae-132">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="040ae-133">1</span><span class="sxs-lookup"><span data-stu-id="040ae-133">1</span></span>     | <span data-ttu-id="040ae-134">/App1/IFD/EXIF/{UShort = 37385}</span><span class="sxs-lookup"><span data-stu-id="040ae-134">/app1/ifd/exif/{ushort=37385}</span></span>    | <span data-ttu-id="040ae-135">ushort</span><span class="sxs-lookup"><span data-stu-id="040ae-135">ushort</span></span>      |
| <span data-ttu-id="040ae-136">2</span><span class="sxs-lookup"><span data-stu-id="040ae-136">2</span></span>     | <span data-ttu-id="040ae-137">/XMP/ <xmpstruct> EXIF : Flash</span><span class="sxs-lookup"><span data-stu-id="040ae-137">/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="040ae-138">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="040ae-138">Remove Paths</span></span>



| <span data-ttu-id="040ae-139">Commande</span><span class="sxs-lookup"><span data-stu-id="040ae-139">Order</span></span> | <span data-ttu-id="040ae-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="040ae-140">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="040ae-141">1</span><span class="sxs-lookup"><span data-stu-id="040ae-141">1</span></span>     | <span data-ttu-id="040ae-142">/App1/IFD/EXIF/{UShort = 37385}</span><span class="sxs-lookup"><span data-stu-id="040ae-142">/app1/ifd/exif/{ushort=37385}</span></span>    |
| <span data-ttu-id="040ae-143">2</span><span class="sxs-lookup"><span data-stu-id="040ae-143">2</span></span>     | <span data-ttu-id="040ae-144">/XMP/ <xmpstruct> EXIF : Flash</span><span class="sxs-lookup"><span data-stu-id="040ae-144">/xmp/<xmpstruct>exif:flash</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="040ae-145">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="040ae-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="040ae-146">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="040ae-146">Read Paths</span></span>



| <span data-ttu-id="040ae-147">Commande</span><span class="sxs-lookup"><span data-stu-id="040ae-147">Order</span></span> | <span data-ttu-id="040ae-148">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="040ae-148">Path</span></span>                                 | <span data-ttu-id="040ae-149">Format de disque</span><span class="sxs-lookup"><span data-stu-id="040ae-149">Disk Format</span></span> |
|-------|--------------------------------------|-------------|
| <span data-ttu-id="040ae-150">1</span><span class="sxs-lookup"><span data-stu-id="040ae-150">1</span></span>     | <span data-ttu-id="040ae-151">/IFD/EXIF/{UShort = 37385}</span><span class="sxs-lookup"><span data-stu-id="040ae-151">/ifd/exif/{ushort=37385}</span></span>             | <span data-ttu-id="040ae-152">ushort</span><span class="sxs-lookup"><span data-stu-id="040ae-152">ushort</span></span>      |
| <span data-ttu-id="040ae-153">2</span><span class="sxs-lookup"><span data-stu-id="040ae-153">2</span></span>     | <span data-ttu-id="040ae-154">/IFD/XMP/ <xmpstruct> EXIF : Flash</span><span class="sxs-lookup"><span data-stu-id="040ae-154">/ifd/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="040ae-155">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="040ae-155">Write Paths</span></span>



| <span data-ttu-id="040ae-156">Commande</span><span class="sxs-lookup"><span data-stu-id="040ae-156">Order</span></span> | <span data-ttu-id="040ae-157">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="040ae-157">Path</span></span>                                 | <span data-ttu-id="040ae-158">Format de disque</span><span class="sxs-lookup"><span data-stu-id="040ae-158">Disk Format</span></span> |
|-------|--------------------------------------|-------------|
| <span data-ttu-id="040ae-159">1</span><span class="sxs-lookup"><span data-stu-id="040ae-159">1</span></span>     | <span data-ttu-id="040ae-160">/IFD/EXIF/{UShort = 37385}</span><span class="sxs-lookup"><span data-stu-id="040ae-160">/ifd/exif/{ushort=37385}</span></span>             | <span data-ttu-id="040ae-161">ushort</span><span class="sxs-lookup"><span data-stu-id="040ae-161">ushort</span></span>      |
| <span data-ttu-id="040ae-162">2</span><span class="sxs-lookup"><span data-stu-id="040ae-162">2</span></span>     | <span data-ttu-id="040ae-163">/IFD/XMP/ <xmpstruct> EXIF : Flash</span><span class="sxs-lookup"><span data-stu-id="040ae-163">/ifd/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="040ae-164">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="040ae-164">Remove Paths</span></span>



| <span data-ttu-id="040ae-165">Commande</span><span class="sxs-lookup"><span data-stu-id="040ae-165">Order</span></span> | <span data-ttu-id="040ae-166">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="040ae-166">Path</span></span>                                 |
|-------|--------------------------------------|
| <span data-ttu-id="040ae-167">1</span><span class="sxs-lookup"><span data-stu-id="040ae-167">1</span></span>     | <span data-ttu-id="040ae-168">/IFD/EXIF/{UShort = 37385}</span><span class="sxs-lookup"><span data-stu-id="040ae-168">/ifd/exif/{ushort=37385}</span></span>             |
| <span data-ttu-id="040ae-169">2</span><span class="sxs-lookup"><span data-stu-id="040ae-169">2</span></span>     | <span data-ttu-id="040ae-170">/IFD/XMP/ <xmpstruct> EXIF : Flash</span><span class="sxs-lookup"><span data-stu-id="040ae-170">/ifd/xmp/<xmpstruct>exif:flash</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="040ae-171">Notes</span><span class="sxs-lookup"><span data-stu-id="040ae-171">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="040ae-172">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="040ae-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="040ae-173">System. photo. Flash</span><span class="sxs-lookup"><span data-stu-id="040ae-173">System.Photo.Flash</span></span>](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
