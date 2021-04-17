---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. LightSource.
ms.assetid: 051a49ad-bb4c-459f-ae52-dc359a03a14a
title: Stratégie de métadonnées de photo System. photo. LightSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec9b3d31f01cdd2bea8d3fabbbc730a41f1fb0da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529937"
---
# <a name="systemphotolightsource-photo-metadata-policy"></a><span data-ttu-id="27722-103">Stratégie de métadonnées de photo System. photo. LightSource</span><span class="sxs-lookup"><span data-stu-id="27722-103">System.Photo.LightSource Photo Metadata Policy</span></span>

<span data-ttu-id="27722-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. lightsource](../properties/props-system-photo-lightsource.md) .</span><span class="sxs-lookup"><span data-stu-id="27722-104">The photo metadata policy for the [System.Photo.LightSource](../properties/props-system-photo-lightsource.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="27722-105">A-la</span><span class="sxs-lookup"><span data-stu-id="27722-105">PKEY</span></span>

<span data-ttu-id="27722-106">Photo de la \_ \_</span><span class="sxs-lookup"><span data-stu-id="27722-106">PKEY\_Photo\_LightSource</span></span>

### <a name="containers"></a><span data-ttu-id="27722-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="27722-107">Containers</span></span>

<span data-ttu-id="27722-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="27722-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="27722-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="27722-109">Read-Only</span></span>

<span data-ttu-id="27722-110">Non</span><span class="sxs-lookup"><span data-stu-id="27722-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="27722-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="27722-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="27722-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="27722-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="27722-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="27722-113">Input Type</span></span>

<span data-ttu-id="27722-114">UShort</span><span class="sxs-lookup"><span data-stu-id="27722-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="27722-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="27722-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="27722-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="27722-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="27722-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="27722-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="27722-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="27722-118">Read Paths</span></span>



| <span data-ttu-id="27722-119">Commande</span><span class="sxs-lookup"><span data-stu-id="27722-119">Order</span></span> | <span data-ttu-id="27722-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="27722-120">Path</span></span>                          | <span data-ttu-id="27722-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="27722-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="27722-122">1</span><span class="sxs-lookup"><span data-stu-id="27722-122">1</span></span>     | <span data-ttu-id="27722-123">/App1/IFD/EXIF/{UShort = 37384}</span><span class="sxs-lookup"><span data-stu-id="27722-123">/app1/ifd/exif/{ushort=37384}</span></span> | <span data-ttu-id="27722-124">ushort</span><span class="sxs-lookup"><span data-stu-id="27722-124">ushort</span></span>      |
| <span data-ttu-id="27722-125">2</span><span class="sxs-lookup"><span data-stu-id="27722-125">2</span></span>     | <span data-ttu-id="27722-126">/XMP/EXIF : LightSource</span><span class="sxs-lookup"><span data-stu-id="27722-126">/xmp/exif:LightSource</span></span>         | <span data-ttu-id="27722-127">unicode</span><span class="sxs-lookup"><span data-stu-id="27722-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="27722-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="27722-128">Write Paths</span></span>



| <span data-ttu-id="27722-129">Commande</span><span class="sxs-lookup"><span data-stu-id="27722-129">Order</span></span> | <span data-ttu-id="27722-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="27722-130">Path</span></span>                          | <span data-ttu-id="27722-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="27722-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="27722-132">1</span><span class="sxs-lookup"><span data-stu-id="27722-132">1</span></span>     | <span data-ttu-id="27722-133">/App1/IFD/EXIF/{UShort = 37384}</span><span class="sxs-lookup"><span data-stu-id="27722-133">/app1/ifd/exif/{ushort=37384}</span></span> | <span data-ttu-id="27722-134">ushort</span><span class="sxs-lookup"><span data-stu-id="27722-134">ushort</span></span>      |
| <span data-ttu-id="27722-135">2</span><span class="sxs-lookup"><span data-stu-id="27722-135">2</span></span>     | <span data-ttu-id="27722-136">/XMP/EXIF : LightSource</span><span class="sxs-lookup"><span data-stu-id="27722-136">/xmp/exif:LightSource</span></span>         | <span data-ttu-id="27722-137">unicode</span><span class="sxs-lookup"><span data-stu-id="27722-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="27722-138">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="27722-138">Remove Paths</span></span>



| <span data-ttu-id="27722-139">Commande</span><span class="sxs-lookup"><span data-stu-id="27722-139">Order</span></span> | <span data-ttu-id="27722-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="27722-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="27722-141">1</span><span class="sxs-lookup"><span data-stu-id="27722-141">1</span></span>     | <span data-ttu-id="27722-142">/App1/IFD/EXIF/{UShort = 37384}</span><span class="sxs-lookup"><span data-stu-id="27722-142">/app1/ifd/exif/{ushort=37384}</span></span> |
| <span data-ttu-id="27722-143">2</span><span class="sxs-lookup"><span data-stu-id="27722-143">2</span></span>     | <span data-ttu-id="27722-144">/XMP/EXIF : lightsource</span><span class="sxs-lookup"><span data-stu-id="27722-144">/xmp/exif:lightsource</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="27722-145">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="27722-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="27722-146">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="27722-146">Read Paths</span></span>



| <span data-ttu-id="27722-147">Commande</span><span class="sxs-lookup"><span data-stu-id="27722-147">Order</span></span> | <span data-ttu-id="27722-148">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="27722-148">Path</span></span>                      | <span data-ttu-id="27722-149">Format de disque</span><span class="sxs-lookup"><span data-stu-id="27722-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="27722-150">1</span><span class="sxs-lookup"><span data-stu-id="27722-150">1</span></span>     | <span data-ttu-id="27722-151">/IFD/EXIF/{UShort = 37384}</span><span class="sxs-lookup"><span data-stu-id="27722-151">/ifd/exif/{ushort=37384}</span></span>  | <span data-ttu-id="27722-152">ushort</span><span class="sxs-lookup"><span data-stu-id="27722-152">ushort</span></span>      |
| <span data-ttu-id="27722-153">2</span><span class="sxs-lookup"><span data-stu-id="27722-153">2</span></span>     | <span data-ttu-id="27722-154">/IFD/XMP/EXIF : LightSource</span><span class="sxs-lookup"><span data-stu-id="27722-154">/ifd/xmp/exif:LightSource</span></span> | <span data-ttu-id="27722-155">unicode</span><span class="sxs-lookup"><span data-stu-id="27722-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="27722-156">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="27722-156">Write Paths</span></span>



| <span data-ttu-id="27722-157">Commande</span><span class="sxs-lookup"><span data-stu-id="27722-157">Order</span></span> | <span data-ttu-id="27722-158">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="27722-158">Path</span></span>                      | <span data-ttu-id="27722-159">Format de disque</span><span class="sxs-lookup"><span data-stu-id="27722-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="27722-160">1</span><span class="sxs-lookup"><span data-stu-id="27722-160">1</span></span>     | <span data-ttu-id="27722-161">/IFD/EXIF/{UShort = 37384}</span><span class="sxs-lookup"><span data-stu-id="27722-161">/ifd/exif/{ushort=37384}</span></span>  | <span data-ttu-id="27722-162">ushort</span><span class="sxs-lookup"><span data-stu-id="27722-162">ushort</span></span>      |
| <span data-ttu-id="27722-163">2</span><span class="sxs-lookup"><span data-stu-id="27722-163">2</span></span>     | <span data-ttu-id="27722-164">/IFD/XMP/EXIF : LightSource</span><span class="sxs-lookup"><span data-stu-id="27722-164">/ifd/xmp/exif:LightSource</span></span> | <span data-ttu-id="27722-165">unicode</span><span class="sxs-lookup"><span data-stu-id="27722-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="27722-166">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="27722-166">Remove Paths</span></span>



| <span data-ttu-id="27722-167">Commande</span><span class="sxs-lookup"><span data-stu-id="27722-167">Order</span></span> | <span data-ttu-id="27722-168">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="27722-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="27722-169">1</span><span class="sxs-lookup"><span data-stu-id="27722-169">1</span></span>     | <span data-ttu-id="27722-170">/IFD/EXIF/{UShort = 37384}</span><span class="sxs-lookup"><span data-stu-id="27722-170">/ifd/exif/{ushort=37384}</span></span>  |
| <span data-ttu-id="27722-171">2</span><span class="sxs-lookup"><span data-stu-id="27722-171">2</span></span>     | <span data-ttu-id="27722-172">/IFD/XMP/EXIF : lightsource</span><span class="sxs-lookup"><span data-stu-id="27722-172">/ifd/xmp/exif:lightsource</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="27722-173">Notes</span><span class="sxs-lookup"><span data-stu-id="27722-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="27722-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="27722-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27722-175">System. photo. LightSource</span><span class="sxs-lookup"><span data-stu-id="27722-175">System.Photo.LightSource</span></span>](../properties/props-system-photo-lightsource.md)
</dt> </dl>

 

 
