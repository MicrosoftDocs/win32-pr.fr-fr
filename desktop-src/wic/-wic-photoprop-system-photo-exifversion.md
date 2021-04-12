---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. EXIFVersion.
ms.assetid: 0f9c5ea8-918f-4101-8492-3f408145a73e
title: Stratégie de métadonnées de photo System. photo. EXIFVersion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb823db41cb54a06fba235df5be4bb4acd55ea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210076"
---
# <a name="systemphotoexifversion-photo-metadata-policy"></a><span data-ttu-id="c5db8-103">Stratégie de métadonnées de photo System. photo. EXIFVersion</span><span class="sxs-lookup"><span data-stu-id="c5db8-103">System.Photo.EXIFVersion Photo Metadata Policy</span></span>

<span data-ttu-id="c5db8-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. EXIFVersion](../properties/props-system-photo-exifversion.md) .</span><span class="sxs-lookup"><span data-stu-id="c5db8-104">The photo metadata policy for the [System.Photo.EXIFVersion](../properties/props-system-photo-exifversion.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="c5db8-105">A-la</span><span class="sxs-lookup"><span data-stu-id="c5db8-105">PKEY</span></span>

<span data-ttu-id="c5db8-106">\_Photo \_ EXIFVersion</span><span class="sxs-lookup"><span data-stu-id="c5db8-106">PKEY\_Photo\_EXIFVersion</span></span>

### <a name="containers"></a><span data-ttu-id="c5db8-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="c5db8-107">Containers</span></span>

<span data-ttu-id="c5db8-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c5db8-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="c5db8-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c5db8-109">Read-Only</span></span>

<span data-ttu-id="c5db8-110">Non</span><span class="sxs-lookup"><span data-stu-id="c5db8-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="c5db8-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="c5db8-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="c5db8-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="c5db8-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="c5db8-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="c5db8-113">Input Type</span></span>

<span data-ttu-id="c5db8-114">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="c5db8-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="c5db8-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="c5db8-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="c5db8-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="c5db8-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="c5db8-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="c5db8-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="c5db8-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="c5db8-118">Read Paths</span></span>



| <span data-ttu-id="c5db8-119">Commande</span><span class="sxs-lookup"><span data-stu-id="c5db8-119">Order</span></span> | <span data-ttu-id="c5db8-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c5db8-120">Path</span></span>                          | <span data-ttu-id="c5db8-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="c5db8-121">Disk Format</span></span>   |
|-------|-------------------------------|---------------|
| <span data-ttu-id="c5db8-122">1</span><span class="sxs-lookup"><span data-stu-id="c5db8-122">1</span></span>     | <span data-ttu-id="c5db8-123">/App1/IFD/EXIF/{UShort = 36864}</span><span class="sxs-lookup"><span data-stu-id="c5db8-123">/app1/ifd/exif/{ushort=36864}</span></span> | <span data-ttu-id="c5db8-124">\_version EXIF</span><span class="sxs-lookup"><span data-stu-id="c5db8-124">exif\_version</span></span> |
| <span data-ttu-id="c5db8-125">2</span><span class="sxs-lookup"><span data-stu-id="c5db8-125">2</span></span>     | <span data-ttu-id="c5db8-126">/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="c5db8-126">/xmp/exif:ExifVersion</span></span>         | <span data-ttu-id="c5db8-127">unicode</span><span class="sxs-lookup"><span data-stu-id="c5db8-127">unicode</span></span>       |



 

### <a name="write-paths"></a><span data-ttu-id="c5db8-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="c5db8-128">Write Paths</span></span>



| <span data-ttu-id="c5db8-129">Commande</span><span class="sxs-lookup"><span data-stu-id="c5db8-129">Order</span></span> | <span data-ttu-id="c5db8-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c5db8-130">Path</span></span>                          | <span data-ttu-id="c5db8-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="c5db8-131">Disk Format</span></span>   |
|-------|-------------------------------|---------------|
| <span data-ttu-id="c5db8-132">1</span><span class="sxs-lookup"><span data-stu-id="c5db8-132">1</span></span>     | <span data-ttu-id="c5db8-133">/App1/IFD/EXIF/{UShort = 36864}</span><span class="sxs-lookup"><span data-stu-id="c5db8-133">/app1/ifd/exif/{ushort=36864}</span></span> | <span data-ttu-id="c5db8-134">\_version EXIF</span><span class="sxs-lookup"><span data-stu-id="c5db8-134">exif\_version</span></span> |
| <span data-ttu-id="c5db8-135">2</span><span class="sxs-lookup"><span data-stu-id="c5db8-135">2</span></span>     | <span data-ttu-id="c5db8-136">/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="c5db8-136">/xmp/exif:ExifVersion</span></span>         | <span data-ttu-id="c5db8-137">unicode</span><span class="sxs-lookup"><span data-stu-id="c5db8-137">unicode</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="c5db8-138">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="c5db8-138">Remove Paths</span></span>



| <span data-ttu-id="c5db8-139">Commande</span><span class="sxs-lookup"><span data-stu-id="c5db8-139">Order</span></span> | <span data-ttu-id="c5db8-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c5db8-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="c5db8-141">1</span><span class="sxs-lookup"><span data-stu-id="c5db8-141">1</span></span>     | <span data-ttu-id="c5db8-142">/App1/IFD/EXIF/{UShort = 36864}</span><span class="sxs-lookup"><span data-stu-id="c5db8-142">/app1/ifd/exif/{ushort=36864}</span></span> |
| <span data-ttu-id="c5db8-143">2</span><span class="sxs-lookup"><span data-stu-id="c5db8-143">2</span></span>     | <span data-ttu-id="c5db8-144">/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="c5db8-144">/xmp/exif:ExifVersion</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="c5db8-145">Stratégie TIFF</span><span class="sxs-lookup"><span data-stu-id="c5db8-145">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="c5db8-146">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="c5db8-146">Read Paths</span></span>



| <span data-ttu-id="c5db8-147">Commande</span><span class="sxs-lookup"><span data-stu-id="c5db8-147">Order</span></span> | <span data-ttu-id="c5db8-148">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c5db8-148">Path</span></span>                      | <span data-ttu-id="c5db8-149">Format de disque</span><span class="sxs-lookup"><span data-stu-id="c5db8-149">Disk Format</span></span>   |
|-------|---------------------------|---------------|
| <span data-ttu-id="c5db8-150">1</span><span class="sxs-lookup"><span data-stu-id="c5db8-150">1</span></span>     | <span data-ttu-id="c5db8-151">/IFD/EXIF/{UShort = 36864}</span><span class="sxs-lookup"><span data-stu-id="c5db8-151">/ifd/exif/{ushort=36864}</span></span>  | <span data-ttu-id="c5db8-152">\_version EXIF</span><span class="sxs-lookup"><span data-stu-id="c5db8-152">exif\_version</span></span> |
| <span data-ttu-id="c5db8-153">2</span><span class="sxs-lookup"><span data-stu-id="c5db8-153">2</span></span>     | <span data-ttu-id="c5db8-154">/ifd/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="c5db8-154">/ifd/xmp/exif:ExifVersion</span></span> | <span data-ttu-id="c5db8-155">unicode</span><span class="sxs-lookup"><span data-stu-id="c5db8-155">unicode</span></span>       |



 

### <a name="write-paths"></a><span data-ttu-id="c5db8-156">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="c5db8-156">Write Paths</span></span>



| <span data-ttu-id="c5db8-157">Commande</span><span class="sxs-lookup"><span data-stu-id="c5db8-157">Order</span></span> | <span data-ttu-id="c5db8-158">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c5db8-158">Path</span></span>                      | <span data-ttu-id="c5db8-159">Format de disque</span><span class="sxs-lookup"><span data-stu-id="c5db8-159">Disk Format</span></span>   |
|-------|---------------------------|---------------|
| <span data-ttu-id="c5db8-160">1</span><span class="sxs-lookup"><span data-stu-id="c5db8-160">1</span></span>     | <span data-ttu-id="c5db8-161">/IFD/EXIF/{UShort = 36864}</span><span class="sxs-lookup"><span data-stu-id="c5db8-161">/ifd/exif/{ushort=36864}</span></span>  | <span data-ttu-id="c5db8-162">\_version EXIF</span><span class="sxs-lookup"><span data-stu-id="c5db8-162">exif\_version</span></span> |
| <span data-ttu-id="c5db8-163">2</span><span class="sxs-lookup"><span data-stu-id="c5db8-163">2</span></span>     | <span data-ttu-id="c5db8-164">/ifd/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="c5db8-164">/ifd/xmp/exif:ExifVersion</span></span> | <span data-ttu-id="c5db8-165">unicode</span><span class="sxs-lookup"><span data-stu-id="c5db8-165">unicode</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="c5db8-166">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="c5db8-166">Remove Paths</span></span>



| <span data-ttu-id="c5db8-167">Commande</span><span class="sxs-lookup"><span data-stu-id="c5db8-167">Order</span></span> | <span data-ttu-id="c5db8-168">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c5db8-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="c5db8-169">1</span><span class="sxs-lookup"><span data-stu-id="c5db8-169">1</span></span>     | <span data-ttu-id="c5db8-170">/IFD/EXIF/{UShort = 36864}</span><span class="sxs-lookup"><span data-stu-id="c5db8-170">/ifd/exif/{ushort=36864}</span></span>  |
| <span data-ttu-id="c5db8-171">2</span><span class="sxs-lookup"><span data-stu-id="c5db8-171">2</span></span>     | <span data-ttu-id="c5db8-172">/ifd/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="c5db8-172">/ifd/xmp/exif:ExifVersion</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c5db8-173">Notes</span><span class="sxs-lookup"><span data-stu-id="c5db8-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5db8-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c5db8-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5db8-175">System. photo. EXIFVersion</span><span class="sxs-lookup"><span data-stu-id="c5db8-175">System.Photo.EXIFVersion</span></span>](../properties/props-system-photo-exifversion.md)
</dt> </dl>

 

 
