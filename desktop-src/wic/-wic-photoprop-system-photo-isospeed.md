---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. ISOSpeed.
ms.assetid: 22b5552c-41b1-4090-a827-b920dcbba5e9
title: Stratégie de métadonnées de photo System. photo. ISOSpeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2988f774f70721ab1817ffaf605098ab1164316a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319617"
---
# <a name="systemphotoisospeed-photo-metadata-policy"></a><span data-ttu-id="2c6f4-103">Stratégie de métadonnées de photo System. photo. ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="2c6f4-103">System.Photo.ISOSpeed Photo Metadata Policy</span></span>

<span data-ttu-id="2c6f4-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. ISOSpeed](../properties/props-system-photo-focallengthinfilm.md) .</span><span class="sxs-lookup"><span data-stu-id="2c6f4-104">The photo metadata policy for the [System.Photo.ISOSpeed](../properties/props-system-photo-focallengthinfilm.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="2c6f4-105">A-la</span><span class="sxs-lookup"><span data-stu-id="2c6f4-105">PKEY</span></span>

<span data-ttu-id="2c6f4-106">\_Photo \_ ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="2c6f4-106">PKEY\_Photo\_ISOSpeed</span></span>

### <a name="containers"></a><span data-ttu-id="2c6f4-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="2c6f4-107">Containers</span></span>

<span data-ttu-id="2c6f4-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="2c6f4-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="2c6f4-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c6f4-109">Read-Only</span></span>

<span data-ttu-id="2c6f4-110">Non</span><span class="sxs-lookup"><span data-stu-id="2c6f4-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="2c6f4-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="2c6f4-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="2c6f4-112">\_UI2 VT</span><span class="sxs-lookup"><span data-stu-id="2c6f4-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="2c6f4-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="2c6f4-113">Input Type</span></span>

<span data-ttu-id="2c6f4-114">UShort</span><span class="sxs-lookup"><span data-stu-id="2c6f4-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="2c6f4-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="2c6f4-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="2c6f4-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="2c6f4-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="2c6f4-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="2c6f4-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="2c6f4-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="2c6f4-118">Read Paths</span></span>



| <span data-ttu-id="2c6f4-119">Commande</span><span class="sxs-lookup"><span data-stu-id="2c6f4-119">Order</span></span> | <span data-ttu-id="2c6f4-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="2c6f4-120">Path</span></span>                                    | <span data-ttu-id="2c6f4-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="2c6f4-121">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="2c6f4-122">1</span><span class="sxs-lookup"><span data-stu-id="2c6f4-122">1</span></span>     | <span data-ttu-id="2c6f4-123">/App1/IFD/EXIF/{UShort = 34855}</span><span class="sxs-lookup"><span data-stu-id="2c6f4-123">/app1/ifd/exif/{ushort=34855}</span></span>           | <span data-ttu-id="2c6f4-124">ushort</span><span class="sxs-lookup"><span data-stu-id="2c6f4-124">ushort</span></span>      |
| <span data-ttu-id="2c6f4-125">2</span><span class="sxs-lookup"><span data-stu-id="2c6f4-125">2</span></span>     | <span data-ttu-id="2c6f4-126">/XMP/ <xmpseq> EXIF : ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="2c6f4-126">/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="2c6f4-127">unicode</span><span class="sxs-lookup"><span data-stu-id="2c6f4-127">unicode</span></span>     |
| <span data-ttu-id="2c6f4-128">3</span><span class="sxs-lookup"><span data-stu-id="2c6f4-128">3</span></span>     | <span data-ttu-id="2c6f4-129">/xmp/exif:ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="2c6f4-129">/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="2c6f4-130">unicode</span><span class="sxs-lookup"><span data-stu-id="2c6f4-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="2c6f4-131">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="2c6f4-131">Write Paths</span></span>



| <span data-ttu-id="2c6f4-132">Commande</span><span class="sxs-lookup"><span data-stu-id="2c6f4-132">Order</span></span> | <span data-ttu-id="2c6f4-133">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="2c6f4-133">Path</span></span>                                    | <span data-ttu-id="2c6f4-134">Format de disque</span><span class="sxs-lookup"><span data-stu-id="2c6f4-134">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="2c6f4-135">1</span><span class="sxs-lookup"><span data-stu-id="2c6f4-135">1</span></span>     | <span data-ttu-id="2c6f4-136">/App1/IFD/EXIF/{UShort = 34855}</span><span class="sxs-lookup"><span data-stu-id="2c6f4-136">/app1/ifd/exif/{ushort=34855}</span></span>           | <span data-ttu-id="2c6f4-137">ushort</span><span class="sxs-lookup"><span data-stu-id="2c6f4-137">ushort</span></span>      |
| <span data-ttu-id="2c6f4-138">2</span><span class="sxs-lookup"><span data-stu-id="2c6f4-138">2</span></span>     | <span data-ttu-id="2c6f4-139">/XMP/ <xmpseq> EXIF : ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="2c6f4-139">/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="2c6f4-140">unicode</span><span class="sxs-lookup"><span data-stu-id="2c6f4-140">unicode</span></span>     |
| <span data-ttu-id="2c6f4-141">3</span><span class="sxs-lookup"><span data-stu-id="2c6f4-141">3</span></span>     | <span data-ttu-id="2c6f4-142">/xmp/exif:ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="2c6f4-142">/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="2c6f4-143">unicode</span><span class="sxs-lookup"><span data-stu-id="2c6f4-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="2c6f4-144">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="2c6f4-144">Remove Paths</span></span>



| <span data-ttu-id="2c6f4-145">Commande</span><span class="sxs-lookup"><span data-stu-id="2c6f4-145">Order</span></span> | <span data-ttu-id="2c6f4-146">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="2c6f4-146">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="2c6f4-147">1</span><span class="sxs-lookup"><span data-stu-id="2c6f4-147">1</span></span>     | <span data-ttu-id="2c6f4-148">/App1/IFD/EXIF/{UShort = 34855}</span><span class="sxs-lookup"><span data-stu-id="2c6f4-148">/app1/ifd/exif/{ushort=34855}</span></span>           |
| <span data-ttu-id="2c6f4-149">2</span><span class="sxs-lookup"><span data-stu-id="2c6f4-149">2</span></span>     | <span data-ttu-id="2c6f4-150">/XMP/ <xmpseq> EXIF : ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="2c6f4-150">/xmp/<xmpseq>exif:isospeedratings</span></span> |
| <span data-ttu-id="2c6f4-151">3</span><span class="sxs-lookup"><span data-stu-id="2c6f4-151">3</span></span>     | <span data-ttu-id="2c6f4-152">/xmp/exif:isospeed</span><span class="sxs-lookup"><span data-stu-id="2c6f4-152">/xmp/exif:isospeed</span></span>                      |



 

### <a name="tiff-policies"></a><span data-ttu-id="2c6f4-153">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="2c6f4-153">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="2c6f4-154">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="2c6f4-154">Read Paths</span></span>



| <span data-ttu-id="2c6f4-155">Commande</span><span class="sxs-lookup"><span data-stu-id="2c6f4-155">Order</span></span> | <span data-ttu-id="2c6f4-156">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="2c6f4-156">Path</span></span>                                        | <span data-ttu-id="2c6f4-157">Format de disque</span><span class="sxs-lookup"><span data-stu-id="2c6f4-157">Disk Format</span></span> |
|-------|---------------------------------------------|-------------|
| <span data-ttu-id="2c6f4-158">1</span><span class="sxs-lookup"><span data-stu-id="2c6f4-158">1</span></span>     | <span data-ttu-id="2c6f4-159">/IFD/EXIF/{UShort = 34855}</span><span class="sxs-lookup"><span data-stu-id="2c6f4-159">/ifd/exif/{ushort=34855}</span></span>                    | <span data-ttu-id="2c6f4-160">ushort</span><span class="sxs-lookup"><span data-stu-id="2c6f4-160">ushort</span></span>      |
| <span data-ttu-id="2c6f4-161">2</span><span class="sxs-lookup"><span data-stu-id="2c6f4-161">2</span></span>     | <span data-ttu-id="2c6f4-162">/IFD/XMP/ <xmpseq> EXIF : ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="2c6f4-162">/ifd/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="2c6f4-163">unicode</span><span class="sxs-lookup"><span data-stu-id="2c6f4-163">unicode</span></span>     |
| <span data-ttu-id="2c6f4-164">3</span><span class="sxs-lookup"><span data-stu-id="2c6f4-164">3</span></span>     | <span data-ttu-id="2c6f4-165">/ifd/xmp/exif:ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="2c6f4-165">/ifd/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="2c6f4-166">unicode</span><span class="sxs-lookup"><span data-stu-id="2c6f4-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="2c6f4-167">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="2c6f4-167">Write Paths</span></span>



| <span data-ttu-id="2c6f4-168">Commande</span><span class="sxs-lookup"><span data-stu-id="2c6f4-168">Order</span></span> | <span data-ttu-id="2c6f4-169">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="2c6f4-169">Path</span></span>                                        | <span data-ttu-id="2c6f4-170">Format de disque</span><span class="sxs-lookup"><span data-stu-id="2c6f4-170">Disk Format</span></span> |
|-------|---------------------------------------------|-------------|
| <span data-ttu-id="2c6f4-171">1</span><span class="sxs-lookup"><span data-stu-id="2c6f4-171">1</span></span>     | <span data-ttu-id="2c6f4-172">/IFD/EXIF/{UShort = 34855}</span><span class="sxs-lookup"><span data-stu-id="2c6f4-172">/ifd/exif/{ushort=34855}</span></span>                    | <span data-ttu-id="2c6f4-173">ushort</span><span class="sxs-lookup"><span data-stu-id="2c6f4-173">ushort</span></span>      |
| <span data-ttu-id="2c6f4-174">2</span><span class="sxs-lookup"><span data-stu-id="2c6f4-174">2</span></span>     | <span data-ttu-id="2c6f4-175">/IFD/XMP/ <xmpseq> EXIF : ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="2c6f4-175">/ifd/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="2c6f4-176">unicode</span><span class="sxs-lookup"><span data-stu-id="2c6f4-176">unicode</span></span>     |
| <span data-ttu-id="2c6f4-177">3</span><span class="sxs-lookup"><span data-stu-id="2c6f4-177">3</span></span>     | <span data-ttu-id="2c6f4-178">/ifd/xmp/exif:ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="2c6f4-178">/ifd/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="2c6f4-179">unicode</span><span class="sxs-lookup"><span data-stu-id="2c6f4-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="2c6f4-180">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="2c6f4-180">Remove Paths</span></span>



| <span data-ttu-id="2c6f4-181">Commande</span><span class="sxs-lookup"><span data-stu-id="2c6f4-181">Order</span></span> | <span data-ttu-id="2c6f4-182">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="2c6f4-182">Path</span></span>                                        |
|-------|---------------------------------------------|
| <span data-ttu-id="2c6f4-183">1</span><span class="sxs-lookup"><span data-stu-id="2c6f4-183">1</span></span>     | <span data-ttu-id="2c6f4-184">/IFD/EXIF/{UShort = 34855}</span><span class="sxs-lookup"><span data-stu-id="2c6f4-184">/ifd/exif/{ushort=34855}</span></span>                    |
| <span data-ttu-id="2c6f4-185">2</span><span class="sxs-lookup"><span data-stu-id="2c6f4-185">2</span></span>     | <span data-ttu-id="2c6f4-186">/IFD/XMP/ <xmpseq> EXIF : ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="2c6f4-186">/ifd/xmp/<xmpseq>exif:isospeedratings</span></span> |
| <span data-ttu-id="2c6f4-187">3</span><span class="sxs-lookup"><span data-stu-id="2c6f4-187">3</span></span>     | <span data-ttu-id="2c6f4-188">/ifd/xmp/exif:isospeed</span><span class="sxs-lookup"><span data-stu-id="2c6f4-188">/ifd/xmp/exif:isospeed</span></span>                      |



 

## <a name="remarks"></a><span data-ttu-id="2c6f4-189">Notes</span><span class="sxs-lookup"><span data-stu-id="2c6f4-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c6f4-190">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2c6f4-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c6f4-191">System. photo. ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="2c6f4-191">System.Photo.ISOSpeed</span></span>](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
