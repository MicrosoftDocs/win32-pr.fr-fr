---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. saturation.
ms.assetid: 1dbb7515-7022-404c-928a-9eb09e43e7a7
title: Stratégie de métadonnées de photo System. photo. saturation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcb2b199458f063f2c28d7f6780a6ea907f76f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035028"
---
# <a name="systemphotosaturation-photo-metadata-policy"></a><span data-ttu-id="b0099-103">Stratégie de métadonnées de photo System. photo. saturation</span><span class="sxs-lookup"><span data-stu-id="b0099-103">System.Photo.Saturation Photo Metadata Policy</span></span>

<span data-ttu-id="b0099-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. saturation](../properties/props-system-photo-saturation.md) .</span><span class="sxs-lookup"><span data-stu-id="b0099-104">The photo metadata policy for the [System.Photo.Saturation](../properties/props-system-photo-saturation.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="b0099-105">A-la</span><span class="sxs-lookup"><span data-stu-id="b0099-105">PKEY</span></span>

<span data-ttu-id="b0099-106">Saturation de la photo de la \_ \_</span><span class="sxs-lookup"><span data-stu-id="b0099-106">PKEY\_Photo\_Saturation</span></span>

### <a name="containers"></a><span data-ttu-id="b0099-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="b0099-107">Containers</span></span>

<span data-ttu-id="b0099-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="b0099-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="b0099-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b0099-109">Read-Only</span></span>

<span data-ttu-id="b0099-110">Non</span><span class="sxs-lookup"><span data-stu-id="b0099-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="b0099-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="b0099-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="b0099-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="b0099-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="b0099-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="b0099-113">Input Type</span></span>

<span data-ttu-id="b0099-114">UShort</span><span class="sxs-lookup"><span data-stu-id="b0099-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="b0099-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="b0099-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="b0099-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="b0099-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="b0099-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="b0099-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="b0099-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="b0099-118">Read Paths</span></span>



| <span data-ttu-id="b0099-119">Commande</span><span class="sxs-lookup"><span data-stu-id="b0099-119">Order</span></span> | <span data-ttu-id="b0099-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="b0099-120">Path</span></span>                          | <span data-ttu-id="b0099-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="b0099-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="b0099-122">1</span><span class="sxs-lookup"><span data-stu-id="b0099-122">1</span></span>     | <span data-ttu-id="b0099-123">/App1/IFD/EXIF/{UShort = 41993}</span><span class="sxs-lookup"><span data-stu-id="b0099-123">/app1/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="b0099-124">ushort</span><span class="sxs-lookup"><span data-stu-id="b0099-124">ushort</span></span>      |
| <span data-ttu-id="b0099-125">2</span><span class="sxs-lookup"><span data-stu-id="b0099-125">2</span></span>     | <span data-ttu-id="b0099-126">/XMP/EXIF : saturation</span><span class="sxs-lookup"><span data-stu-id="b0099-126">/xmp/exif:Saturation</span></span>          | <span data-ttu-id="b0099-127">unicode</span><span class="sxs-lookup"><span data-stu-id="b0099-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="b0099-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="b0099-128">Write Paths</span></span>



| <span data-ttu-id="b0099-129">Commande</span><span class="sxs-lookup"><span data-stu-id="b0099-129">Order</span></span> | <span data-ttu-id="b0099-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="b0099-130">Path</span></span>                          | <span data-ttu-id="b0099-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="b0099-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="b0099-132">1</span><span class="sxs-lookup"><span data-stu-id="b0099-132">1</span></span>     | <span data-ttu-id="b0099-133">/App1/IFD/EXIF/{UShort = 41993}</span><span class="sxs-lookup"><span data-stu-id="b0099-133">/app1/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="b0099-134">ushort</span><span class="sxs-lookup"><span data-stu-id="b0099-134">ushort</span></span>      |
| <span data-ttu-id="b0099-135">2</span><span class="sxs-lookup"><span data-stu-id="b0099-135">2</span></span>     | <span data-ttu-id="b0099-136">/XMP/EXIF : saturation</span><span class="sxs-lookup"><span data-stu-id="b0099-136">/xmp/exif:Saturation</span></span>          | <span data-ttu-id="b0099-137">unicode</span><span class="sxs-lookup"><span data-stu-id="b0099-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="b0099-138">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="b0099-138">Remove Paths</span></span>



| <span data-ttu-id="b0099-139">Commande</span><span class="sxs-lookup"><span data-stu-id="b0099-139">Order</span></span> | <span data-ttu-id="b0099-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="b0099-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="b0099-141">1</span><span class="sxs-lookup"><span data-stu-id="b0099-141">1</span></span>     | <span data-ttu-id="b0099-142">/App1/IFD/EXIF/{UShort = 41993}</span><span class="sxs-lookup"><span data-stu-id="b0099-142">/app1/ifd/exif/{ushort=41993}</span></span> |
| <span data-ttu-id="b0099-143">2</span><span class="sxs-lookup"><span data-stu-id="b0099-143">2</span></span>     | <span data-ttu-id="b0099-144">/XMP/EXIF : saturation</span><span class="sxs-lookup"><span data-stu-id="b0099-144">/xmp/exif:saturation</span></span>          |



 

### <a name="tiff-policies"></a><span data-ttu-id="b0099-145">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="b0099-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="b0099-146">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="b0099-146">Read Paths</span></span>



| <span data-ttu-id="b0099-147">Commande</span><span class="sxs-lookup"><span data-stu-id="b0099-147">Order</span></span> | <span data-ttu-id="b0099-148">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="b0099-148">Path</span></span>                     | <span data-ttu-id="b0099-149">Format de disque</span><span class="sxs-lookup"><span data-stu-id="b0099-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="b0099-150">1</span><span class="sxs-lookup"><span data-stu-id="b0099-150">1</span></span>     | <span data-ttu-id="b0099-151">/IFD/EXIF/{UShort = 41993}</span><span class="sxs-lookup"><span data-stu-id="b0099-151">/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="b0099-152">ushort</span><span class="sxs-lookup"><span data-stu-id="b0099-152">ushort</span></span>      |
| <span data-ttu-id="b0099-153">2</span><span class="sxs-lookup"><span data-stu-id="b0099-153">2</span></span>     | <span data-ttu-id="b0099-154">/IFD/XMP/EXIF : saturation</span><span class="sxs-lookup"><span data-stu-id="b0099-154">/ifd/xmp/exif:Saturation</span></span> | <span data-ttu-id="b0099-155">unicode</span><span class="sxs-lookup"><span data-stu-id="b0099-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="b0099-156">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="b0099-156">Write Paths</span></span>



| <span data-ttu-id="b0099-157">Commande</span><span class="sxs-lookup"><span data-stu-id="b0099-157">Order</span></span> | <span data-ttu-id="b0099-158">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="b0099-158">Path</span></span>                     | <span data-ttu-id="b0099-159">Format de disque</span><span class="sxs-lookup"><span data-stu-id="b0099-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="b0099-160">1</span><span class="sxs-lookup"><span data-stu-id="b0099-160">1</span></span>     | <span data-ttu-id="b0099-161">/IFD/EXIF/{UShort = 41993}</span><span class="sxs-lookup"><span data-stu-id="b0099-161">/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="b0099-162">ushort</span><span class="sxs-lookup"><span data-stu-id="b0099-162">ushort</span></span>      |
| <span data-ttu-id="b0099-163">2</span><span class="sxs-lookup"><span data-stu-id="b0099-163">2</span></span>     | <span data-ttu-id="b0099-164">/IFD/XMP/EXIF : saturation</span><span class="sxs-lookup"><span data-stu-id="b0099-164">/ifd/xmp/exif:Saturation</span></span> | <span data-ttu-id="b0099-165">unicode</span><span class="sxs-lookup"><span data-stu-id="b0099-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="b0099-166">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="b0099-166">Remove Paths</span></span>



| <span data-ttu-id="b0099-167">Commande</span><span class="sxs-lookup"><span data-stu-id="b0099-167">Order</span></span> | <span data-ttu-id="b0099-168">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="b0099-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="b0099-169">1</span><span class="sxs-lookup"><span data-stu-id="b0099-169">1</span></span>     | <span data-ttu-id="b0099-170">/IFD/EXIF/{UShort = 41993}</span><span class="sxs-lookup"><span data-stu-id="b0099-170">/ifd/exif/{ushort=41993}</span></span> |
| <span data-ttu-id="b0099-171">2</span><span class="sxs-lookup"><span data-stu-id="b0099-171">2</span></span>     | <span data-ttu-id="b0099-172">/IFD/XMP/EXIF : saturation</span><span class="sxs-lookup"><span data-stu-id="b0099-172">/ifd/xmp/exif:saturation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b0099-173">Notes</span><span class="sxs-lookup"><span data-stu-id="b0099-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0099-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b0099-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0099-175">System. photo. saturation</span><span class="sxs-lookup"><span data-stu-id="b0099-175">System.Photo.Saturation</span></span>](../properties/props-system-photo-saturation.md)
</dt> </dl>

 

 
