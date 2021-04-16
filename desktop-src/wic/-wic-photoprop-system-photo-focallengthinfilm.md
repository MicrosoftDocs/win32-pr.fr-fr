---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. FocalLengthInFilm.
ms.assetid: 3ad63a7a-5ced-4e7f-a4a0-e1463f3d3fa3
title: Stratégie de métadonnées de photo System. photo. FocalLengthInFilm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df46f3e52c447cb7902fe3cce2da201dae16d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485704"
---
# <a name="systemphotofocallengthinfilm-photo-metadata-policy"></a><span data-ttu-id="d3c37-103">Stratégie de métadonnées de photo System. photo. FocalLengthInFilm</span><span class="sxs-lookup"><span data-stu-id="d3c37-103">System.Photo.FocalLengthInFilm Photo Metadata Policy</span></span>

<span data-ttu-id="d3c37-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. FocalLengthInFilm](../properties/props-system-photo-focallengthinfilm.md) .</span><span class="sxs-lookup"><span data-stu-id="d3c37-104">The photo metadata policy for the [System.Photo.FocalLengthInFilm](../properties/props-system-photo-focallengthinfilm.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="d3c37-105">A-la</span><span class="sxs-lookup"><span data-stu-id="d3c37-105">PKEY</span></span>

<span data-ttu-id="d3c37-106">FocalLengthInFilm de la \_</span><span class="sxs-lookup"><span data-stu-id="d3c37-106">PKEY\_FocalLengthInFilm</span></span>

### <a name="containers"></a><span data-ttu-id="d3c37-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="d3c37-107">Containers</span></span>

<span data-ttu-id="d3c37-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d3c37-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="d3c37-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d3c37-109">Read-Only</span></span>

<span data-ttu-id="d3c37-110">Non</span><span class="sxs-lookup"><span data-stu-id="d3c37-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="d3c37-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="d3c37-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="d3c37-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="d3c37-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="d3c37-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="d3c37-113">Input Type</span></span>

<span data-ttu-id="d3c37-114">UShort</span><span class="sxs-lookup"><span data-stu-id="d3c37-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="d3c37-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="d3c37-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="d3c37-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="d3c37-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="d3c37-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="d3c37-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="d3c37-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="d3c37-118">Read Paths</span></span>



| <span data-ttu-id="d3c37-119">Commande</span><span class="sxs-lookup"><span data-stu-id="d3c37-119">Order</span></span> | <span data-ttu-id="d3c37-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="d3c37-120">Path</span></span>                            | <span data-ttu-id="d3c37-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="d3c37-121">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="d3c37-122">1</span><span class="sxs-lookup"><span data-stu-id="d3c37-122">1</span></span>     | <span data-ttu-id="d3c37-123">/App1/IFD/EXIF/{UShort = 41989}</span><span class="sxs-lookup"><span data-stu-id="d3c37-123">/app1/ifd/exif/{ushort=41989}</span></span>   | <span data-ttu-id="d3c37-124">ushort</span><span class="sxs-lookup"><span data-stu-id="d3c37-124">ushort</span></span>      |
| <span data-ttu-id="d3c37-125">2</span><span class="sxs-lookup"><span data-stu-id="d3c37-125">2</span></span>     | <span data-ttu-id="d3c37-126">/xmp/exif:FocalLengthIn35mmFilm</span><span class="sxs-lookup"><span data-stu-id="d3c37-126">/xmp/exif:FocalLengthIn35mmFilm</span></span> | <span data-ttu-id="d3c37-127">unicode</span><span class="sxs-lookup"><span data-stu-id="d3c37-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="d3c37-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="d3c37-128">Write Paths</span></span>



| <span data-ttu-id="d3c37-129">Commande</span><span class="sxs-lookup"><span data-stu-id="d3c37-129">Order</span></span> | <span data-ttu-id="d3c37-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="d3c37-130">Path</span></span>                            | <span data-ttu-id="d3c37-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="d3c37-131">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="d3c37-132">1</span><span class="sxs-lookup"><span data-stu-id="d3c37-132">1</span></span>     | <span data-ttu-id="d3c37-133">/App1/IFD/EXIF/{UShort = 41989}</span><span class="sxs-lookup"><span data-stu-id="d3c37-133">/app1/ifd/exif/{ushort=41989}</span></span>   | <span data-ttu-id="d3c37-134">ushort</span><span class="sxs-lookup"><span data-stu-id="d3c37-134">ushort</span></span>      |
| <span data-ttu-id="d3c37-135">2</span><span class="sxs-lookup"><span data-stu-id="d3c37-135">2</span></span>     | <span data-ttu-id="d3c37-136">/xmp/exif:FocalLengthIn35mmFilm</span><span class="sxs-lookup"><span data-stu-id="d3c37-136">/xmp/exif:FocalLengthIn35mmFilm</span></span> | <span data-ttu-id="d3c37-137">unicode</span><span class="sxs-lookup"><span data-stu-id="d3c37-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="d3c37-138">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="d3c37-138">Remove Paths</span></span>



| <span data-ttu-id="d3c37-139">Commande</span><span class="sxs-lookup"><span data-stu-id="d3c37-139">Order</span></span> | <span data-ttu-id="d3c37-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="d3c37-140">Path</span></span>                            |
|-------|---------------------------------|
| <span data-ttu-id="d3c37-141">1</span><span class="sxs-lookup"><span data-stu-id="d3c37-141">1</span></span>     | <span data-ttu-id="d3c37-142">/App1/IFD/EXIF/{UShort = 41989}</span><span class="sxs-lookup"><span data-stu-id="d3c37-142">/app1/ifd/exif/{ushort=41989}</span></span>   |
| <span data-ttu-id="d3c37-143">2</span><span class="sxs-lookup"><span data-stu-id="d3c37-143">2</span></span>     | <span data-ttu-id="d3c37-144">/xmp/exif:focallengthin35mmfilm</span><span class="sxs-lookup"><span data-stu-id="d3c37-144">/xmp/exif:focallengthin35mmfilm</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="d3c37-145">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="d3c37-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="d3c37-146">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="d3c37-146">Read Paths</span></span>



| <span data-ttu-id="d3c37-147">Commande</span><span class="sxs-lookup"><span data-stu-id="d3c37-147">Order</span></span> | <span data-ttu-id="d3c37-148">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="d3c37-148">Path</span></span>                                | <span data-ttu-id="d3c37-149">Format de disque</span><span class="sxs-lookup"><span data-stu-id="d3c37-149">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="d3c37-150">1</span><span class="sxs-lookup"><span data-stu-id="d3c37-150">1</span></span>     | <span data-ttu-id="d3c37-151">/IFD/EXIF/{UShort = 41989}</span><span class="sxs-lookup"><span data-stu-id="d3c37-151">/ifd/exif/{ushort=41989}</span></span>            | <span data-ttu-id="d3c37-152">ushort</span><span class="sxs-lookup"><span data-stu-id="d3c37-152">ushort</span></span>      |
| <span data-ttu-id="d3c37-153">2</span><span class="sxs-lookup"><span data-stu-id="d3c37-153">2</span></span>     | <span data-ttu-id="d3c37-154">/ifd/xmp/exif:FocalLengthIn35mmFilm</span><span class="sxs-lookup"><span data-stu-id="d3c37-154">/ifd/xmp/exif:FocalLengthIn35mmFilm</span></span> | <span data-ttu-id="d3c37-155">unicode</span><span class="sxs-lookup"><span data-stu-id="d3c37-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="d3c37-156">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="d3c37-156">Write Paths</span></span>



| <span data-ttu-id="d3c37-157">Commande</span><span class="sxs-lookup"><span data-stu-id="d3c37-157">Order</span></span> | <span data-ttu-id="d3c37-158">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="d3c37-158">Path</span></span>                                | <span data-ttu-id="d3c37-159">Format de disque</span><span class="sxs-lookup"><span data-stu-id="d3c37-159">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="d3c37-160">1</span><span class="sxs-lookup"><span data-stu-id="d3c37-160">1</span></span>     | <span data-ttu-id="d3c37-161">/IFD/EXIF/{UShort = 41989}</span><span class="sxs-lookup"><span data-stu-id="d3c37-161">/ifd/exif/{ushort=41989}</span></span>            | <span data-ttu-id="d3c37-162">ushort</span><span class="sxs-lookup"><span data-stu-id="d3c37-162">ushort</span></span>      |
| <span data-ttu-id="d3c37-163">2</span><span class="sxs-lookup"><span data-stu-id="d3c37-163">2</span></span>     | <span data-ttu-id="d3c37-164">/ifd/xmp/exif:FocalLengthIn35mmFilm</span><span class="sxs-lookup"><span data-stu-id="d3c37-164">/ifd/xmp/exif:FocalLengthIn35mmFilm</span></span> | <span data-ttu-id="d3c37-165">unicode</span><span class="sxs-lookup"><span data-stu-id="d3c37-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="d3c37-166">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="d3c37-166">Remove Paths</span></span>



| <span data-ttu-id="d3c37-167">Commande</span><span class="sxs-lookup"><span data-stu-id="d3c37-167">Order</span></span> | <span data-ttu-id="d3c37-168">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="d3c37-168">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="d3c37-169">1</span><span class="sxs-lookup"><span data-stu-id="d3c37-169">1</span></span>     | <span data-ttu-id="d3c37-170">/IFD/EXIF/{UShort = 41989}</span><span class="sxs-lookup"><span data-stu-id="d3c37-170">/ifd/exif/{ushort=41989}</span></span>            |
| <span data-ttu-id="d3c37-171">2</span><span class="sxs-lookup"><span data-stu-id="d3c37-171">2</span></span>     | <span data-ttu-id="d3c37-172">/ifd/xmp/exif:focallengthin35mmfilm</span><span class="sxs-lookup"><span data-stu-id="d3c37-172">/ifd/xmp/exif:focallengthin35mmfilm</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d3c37-173">Notes</span><span class="sxs-lookup"><span data-stu-id="d3c37-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3c37-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d3c37-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3c37-175">System. photo. FocalLengthInFilm</span><span class="sxs-lookup"><span data-stu-id="d3c37-175">System.Photo.FocalLengthInFilm</span></span>](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
