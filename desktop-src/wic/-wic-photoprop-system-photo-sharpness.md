---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. Sharpity.
ms.assetid: 0fda4832-940b-4b5a-bd20-7e48c7800925
title: Stratégie de métadonnées de photo System. photo. Sharpity
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d635691f0b0e0801c1e37a006faa686aff0a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541909"
---
# <a name="systemphotosharpness-photo-metadata-policy"></a><span data-ttu-id="80cdd-103">Stratégie de métadonnées de photo System. photo. Sharpity</span><span class="sxs-lookup"><span data-stu-id="80cdd-103">System.Photo.Sharpness Photo Metadata Policy</span></span>

<span data-ttu-id="80cdd-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. sharpity](../properties/props-system-photo-sharpness.md) .</span><span class="sxs-lookup"><span data-stu-id="80cdd-104">The photo metadata policy for the [System.Photo.Sharpness](../properties/props-system-photo-sharpness.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="80cdd-105">A-la</span><span class="sxs-lookup"><span data-stu-id="80cdd-105">PKEY</span></span>

<span data-ttu-id="80cdd-106">\_ \_ Netteté photo</span><span class="sxs-lookup"><span data-stu-id="80cdd-106">PKEY\_Photo\_Sharpness</span></span>

### <a name="containers"></a><span data-ttu-id="80cdd-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="80cdd-107">Containers</span></span>

<span data-ttu-id="80cdd-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="80cdd-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="80cdd-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80cdd-109">Read-Only</span></span>

<span data-ttu-id="80cdd-110">Non</span><span class="sxs-lookup"><span data-stu-id="80cdd-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="80cdd-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="80cdd-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="80cdd-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="80cdd-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="80cdd-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="80cdd-113">Input Type</span></span>

<span data-ttu-id="80cdd-114">UShort</span><span class="sxs-lookup"><span data-stu-id="80cdd-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="80cdd-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="80cdd-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="80cdd-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="80cdd-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="80cdd-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="80cdd-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="80cdd-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="80cdd-118">Read Paths</span></span>



| <span data-ttu-id="80cdd-119">Commande</span><span class="sxs-lookup"><span data-stu-id="80cdd-119">Order</span></span> | <span data-ttu-id="80cdd-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="80cdd-120">Path</span></span>                          | <span data-ttu-id="80cdd-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="80cdd-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="80cdd-122">1</span><span class="sxs-lookup"><span data-stu-id="80cdd-122">1</span></span>     | <span data-ttu-id="80cdd-123">/App1/IFD/EXIF/{UShort = 41994}</span><span class="sxs-lookup"><span data-stu-id="80cdd-123">/app1/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="80cdd-124">ushort</span><span class="sxs-lookup"><span data-stu-id="80cdd-124">ushort</span></span>      |
| <span data-ttu-id="80cdd-125">2</span><span class="sxs-lookup"><span data-stu-id="80cdd-125">2</span></span>     | <span data-ttu-id="80cdd-126">/XMP/EXIF : netteté</span><span class="sxs-lookup"><span data-stu-id="80cdd-126">/xmp/exif:Sharpness</span></span>           | <span data-ttu-id="80cdd-127">unicode</span><span class="sxs-lookup"><span data-stu-id="80cdd-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="80cdd-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="80cdd-128">Write Paths</span></span>



| <span data-ttu-id="80cdd-129">Commande</span><span class="sxs-lookup"><span data-stu-id="80cdd-129">Order</span></span> | <span data-ttu-id="80cdd-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="80cdd-130">Path</span></span>                          | <span data-ttu-id="80cdd-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="80cdd-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="80cdd-132">1</span><span class="sxs-lookup"><span data-stu-id="80cdd-132">1</span></span>     | <span data-ttu-id="80cdd-133">/App1/IFD/EXIF/{UShort = 41994}</span><span class="sxs-lookup"><span data-stu-id="80cdd-133">/app1/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="80cdd-134">ushort</span><span class="sxs-lookup"><span data-stu-id="80cdd-134">ushort</span></span>      |
| <span data-ttu-id="80cdd-135">2</span><span class="sxs-lookup"><span data-stu-id="80cdd-135">2</span></span>     | <span data-ttu-id="80cdd-136">/XMP/EXIF : netteté</span><span class="sxs-lookup"><span data-stu-id="80cdd-136">/xmp/exif:Sharpness</span></span>           | <span data-ttu-id="80cdd-137">unicode</span><span class="sxs-lookup"><span data-stu-id="80cdd-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="80cdd-138">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="80cdd-138">Remove Paths</span></span>



| <span data-ttu-id="80cdd-139">Commande</span><span class="sxs-lookup"><span data-stu-id="80cdd-139">Order</span></span> | <span data-ttu-id="80cdd-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="80cdd-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="80cdd-141">1</span><span class="sxs-lookup"><span data-stu-id="80cdd-141">1</span></span>     | <span data-ttu-id="80cdd-142">/App1/IFD/EXIF/{UShort = 41994}</span><span class="sxs-lookup"><span data-stu-id="80cdd-142">/app1/ifd/exif/{ushort=41994}</span></span> |
| <span data-ttu-id="80cdd-143">2</span><span class="sxs-lookup"><span data-stu-id="80cdd-143">2</span></span>     | <span data-ttu-id="80cdd-144">/XMP/EXIF : netteté</span><span class="sxs-lookup"><span data-stu-id="80cdd-144">/xmp/exif:sharpness</span></span>           |



 

### <a name="tiff-policies"></a><span data-ttu-id="80cdd-145">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="80cdd-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="80cdd-146">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="80cdd-146">Read Paths</span></span>



| <span data-ttu-id="80cdd-147">Commande</span><span class="sxs-lookup"><span data-stu-id="80cdd-147">Order</span></span> | <span data-ttu-id="80cdd-148">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="80cdd-148">Path</span></span>                     | <span data-ttu-id="80cdd-149">Format de disque</span><span class="sxs-lookup"><span data-stu-id="80cdd-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="80cdd-150">1</span><span class="sxs-lookup"><span data-stu-id="80cdd-150">1</span></span>     | <span data-ttu-id="80cdd-151">/IFD/EXIF/{UShort = 41994}</span><span class="sxs-lookup"><span data-stu-id="80cdd-151">/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="80cdd-152">ushort</span><span class="sxs-lookup"><span data-stu-id="80cdd-152">ushort</span></span>      |
| <span data-ttu-id="80cdd-153">2</span><span class="sxs-lookup"><span data-stu-id="80cdd-153">2</span></span>     | <span data-ttu-id="80cdd-154">/IFD/XMP/EXIF : netteté</span><span class="sxs-lookup"><span data-stu-id="80cdd-154">/ifd/xmp/exif:Sharpness</span></span>  | <span data-ttu-id="80cdd-155">unicode</span><span class="sxs-lookup"><span data-stu-id="80cdd-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="80cdd-156">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="80cdd-156">Write Paths</span></span>



| <span data-ttu-id="80cdd-157">Commande</span><span class="sxs-lookup"><span data-stu-id="80cdd-157">Order</span></span> | <span data-ttu-id="80cdd-158">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="80cdd-158">Path</span></span>                     | <span data-ttu-id="80cdd-159">Format de disque</span><span class="sxs-lookup"><span data-stu-id="80cdd-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="80cdd-160">1</span><span class="sxs-lookup"><span data-stu-id="80cdd-160">1</span></span>     | <span data-ttu-id="80cdd-161">/IFD/EXIF/{UShort = 41994}</span><span class="sxs-lookup"><span data-stu-id="80cdd-161">/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="80cdd-162">ushort</span><span class="sxs-lookup"><span data-stu-id="80cdd-162">ushort</span></span>      |
| <span data-ttu-id="80cdd-163">2</span><span class="sxs-lookup"><span data-stu-id="80cdd-163">2</span></span>     | <span data-ttu-id="80cdd-164">/IFD/XMP/EXIF : netteté</span><span class="sxs-lookup"><span data-stu-id="80cdd-164">/ifd/xmp/exif:Sharpness</span></span>  | <span data-ttu-id="80cdd-165">unicode</span><span class="sxs-lookup"><span data-stu-id="80cdd-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="80cdd-166">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="80cdd-166">Remove Paths</span></span>



| <span data-ttu-id="80cdd-167">Commande</span><span class="sxs-lookup"><span data-stu-id="80cdd-167">Order</span></span> | <span data-ttu-id="80cdd-168">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="80cdd-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="80cdd-169">1</span><span class="sxs-lookup"><span data-stu-id="80cdd-169">1</span></span>     | <span data-ttu-id="80cdd-170">/IFD/EXIF/{UShort = 41994}</span><span class="sxs-lookup"><span data-stu-id="80cdd-170">/ifd/exif/{ushort=41994}</span></span> |
| <span data-ttu-id="80cdd-171">2</span><span class="sxs-lookup"><span data-stu-id="80cdd-171">2</span></span>     | <span data-ttu-id="80cdd-172">/IFD/XMP/EXIF : netteté</span><span class="sxs-lookup"><span data-stu-id="80cdd-172">/ifd/xmp/exif:sharpness</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="80cdd-173">Notes</span><span class="sxs-lookup"><span data-stu-id="80cdd-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="80cdd-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="80cdd-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80cdd-175">System. photo. Sharpity</span><span class="sxs-lookup"><span data-stu-id="80cdd-175">System.Photo.Sharpness</span></span>](../properties/props-system-photo-sharpness.md)
</dt> </dl>

 

 
