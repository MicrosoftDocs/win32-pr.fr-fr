---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. Contrast.
ms.assetid: c5e2589d-507c-4b92-9ada-7d64e7c45dd8
title: Stratégie de métadonnées de photo System. photo. Contrast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d6ed34854b525e9eaac2ff5ac7339a75ad10e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530262"
---
# <a name="systemphotocontrast-photo-metadata-policy"></a><span data-ttu-id="42e4a-103">Stratégie de métadonnées de photo System. photo. Contrast</span><span class="sxs-lookup"><span data-stu-id="42e4a-103">System.Photo.Contrast Photo Metadata Policy</span></span>

<span data-ttu-id="42e4a-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. Contrast](../properties/props-system-photo-contrast.md) .</span><span class="sxs-lookup"><span data-stu-id="42e4a-104">The photo metadata policy for the [System.Photo.Contrast](../properties/props-system-photo-contrast.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="42e4a-105">A-la</span><span class="sxs-lookup"><span data-stu-id="42e4a-105">PKEY</span></span>

<span data-ttu-id="42e4a-106">\_Contraste de photo de la \_</span><span class="sxs-lookup"><span data-stu-id="42e4a-106">PKEY\_Photo\_Contrast</span></span>

### <a name="containers"></a><span data-ttu-id="42e4a-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="42e4a-107">Containers</span></span>

<span data-ttu-id="42e4a-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="42e4a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="42e4a-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="42e4a-109">Read-Only</span></span>

<span data-ttu-id="42e4a-110">Non</span><span class="sxs-lookup"><span data-stu-id="42e4a-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="42e4a-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="42e4a-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="42e4a-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="42e4a-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="42e4a-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="42e4a-113">Input Type</span></span>

<span data-ttu-id="42e4a-114">UShort</span><span class="sxs-lookup"><span data-stu-id="42e4a-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="42e4a-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="42e4a-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="42e4a-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="42e4a-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="42e4a-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="42e4a-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="42e4a-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="42e4a-118">Read Paths</span></span>



| <span data-ttu-id="42e4a-119">Commande</span><span class="sxs-lookup"><span data-stu-id="42e4a-119">Order</span></span> | <span data-ttu-id="42e4a-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="42e4a-120">Path</span></span>                          | <span data-ttu-id="42e4a-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="42e4a-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="42e4a-122">1</span><span class="sxs-lookup"><span data-stu-id="42e4a-122">1</span></span>     | <span data-ttu-id="42e4a-123">/App1/IFD/EXIF/{UShort = 41992}</span><span class="sxs-lookup"><span data-stu-id="42e4a-123">/app1/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="42e4a-124">ushort</span><span class="sxs-lookup"><span data-stu-id="42e4a-124">ushort</span></span>      |
| <span data-ttu-id="42e4a-125">2</span><span class="sxs-lookup"><span data-stu-id="42e4a-125">2</span></span>     | <span data-ttu-id="42e4a-126">/XMP/EXIF : contraste</span><span class="sxs-lookup"><span data-stu-id="42e4a-126">/xmp/exif:Contrast</span></span>            | <span data-ttu-id="42e4a-127">unicode</span><span class="sxs-lookup"><span data-stu-id="42e4a-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="42e4a-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="42e4a-128">Write Paths</span></span>



| <span data-ttu-id="42e4a-129">Commande</span><span class="sxs-lookup"><span data-stu-id="42e4a-129">Order</span></span> | <span data-ttu-id="42e4a-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="42e4a-130">Path</span></span>                          | <span data-ttu-id="42e4a-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="42e4a-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="42e4a-132">1</span><span class="sxs-lookup"><span data-stu-id="42e4a-132">1</span></span>     | <span data-ttu-id="42e4a-133">/App1/IFD/EXIF/{UShort = 41992}</span><span class="sxs-lookup"><span data-stu-id="42e4a-133">/app1/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="42e4a-134">ushort</span><span class="sxs-lookup"><span data-stu-id="42e4a-134">ushort</span></span>      |
| <span data-ttu-id="42e4a-135">2</span><span class="sxs-lookup"><span data-stu-id="42e4a-135">2</span></span>     | <span data-ttu-id="42e4a-136">/XMP/EXIF : contraste</span><span class="sxs-lookup"><span data-stu-id="42e4a-136">/xmp/exif:Contrast</span></span>            | <span data-ttu-id="42e4a-137">unicode</span><span class="sxs-lookup"><span data-stu-id="42e4a-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="42e4a-138">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="42e4a-138">Remove Paths</span></span>



| <span data-ttu-id="42e4a-139">Commande</span><span class="sxs-lookup"><span data-stu-id="42e4a-139">Order</span></span> | <span data-ttu-id="42e4a-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="42e4a-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="42e4a-141">1</span><span class="sxs-lookup"><span data-stu-id="42e4a-141">1</span></span>     | <span data-ttu-id="42e4a-142">/App1/IFD/EXIF/{UShort = 41992}</span><span class="sxs-lookup"><span data-stu-id="42e4a-142">/app1/ifd/exif/{ushort=41992}</span></span> |
| <span data-ttu-id="42e4a-143">2</span><span class="sxs-lookup"><span data-stu-id="42e4a-143">2</span></span>     | <span data-ttu-id="42e4a-144">/XMP/EXIF : contraste</span><span class="sxs-lookup"><span data-stu-id="42e4a-144">/xmp/exif:contrast</span></span>            |



 

### <a name="tiff-policies"></a><span data-ttu-id="42e4a-145">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="42e4a-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="42e4a-146">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="42e4a-146">Read Paths</span></span>



| <span data-ttu-id="42e4a-147">Commande</span><span class="sxs-lookup"><span data-stu-id="42e4a-147">Order</span></span> | <span data-ttu-id="42e4a-148">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="42e4a-148">Path</span></span>                     | <span data-ttu-id="42e4a-149">Format de disque</span><span class="sxs-lookup"><span data-stu-id="42e4a-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="42e4a-150">1</span><span class="sxs-lookup"><span data-stu-id="42e4a-150">1</span></span>     | <span data-ttu-id="42e4a-151">/IFD/EXIF/{UShort = 41992}</span><span class="sxs-lookup"><span data-stu-id="42e4a-151">/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="42e4a-152">ushort</span><span class="sxs-lookup"><span data-stu-id="42e4a-152">ushort</span></span>      |
| <span data-ttu-id="42e4a-153">2</span><span class="sxs-lookup"><span data-stu-id="42e4a-153">2</span></span>     | <span data-ttu-id="42e4a-154">/IFD/XMP/EXIF : contraste</span><span class="sxs-lookup"><span data-stu-id="42e4a-154">/ifd/xmp/exif:Contrast</span></span>   | <span data-ttu-id="42e4a-155">unicode</span><span class="sxs-lookup"><span data-stu-id="42e4a-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="42e4a-156">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="42e4a-156">Write Paths</span></span>



| <span data-ttu-id="42e4a-157">Commande</span><span class="sxs-lookup"><span data-stu-id="42e4a-157">Order</span></span> | <span data-ttu-id="42e4a-158">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="42e4a-158">Path</span></span>                     | <span data-ttu-id="42e4a-159">Format de disque</span><span class="sxs-lookup"><span data-stu-id="42e4a-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="42e4a-160">1</span><span class="sxs-lookup"><span data-stu-id="42e4a-160">1</span></span>     | <span data-ttu-id="42e4a-161">/IFD/EXIF/{UShort = 41992}</span><span class="sxs-lookup"><span data-stu-id="42e4a-161">/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="42e4a-162">ushort</span><span class="sxs-lookup"><span data-stu-id="42e4a-162">ushort</span></span>      |
| <span data-ttu-id="42e4a-163">2</span><span class="sxs-lookup"><span data-stu-id="42e4a-163">2</span></span>     | <span data-ttu-id="42e4a-164">/IFD/XMP/EXIF : contraste</span><span class="sxs-lookup"><span data-stu-id="42e4a-164">/ifd/xmp/exif:Contrast</span></span>   | <span data-ttu-id="42e4a-165">unicode</span><span class="sxs-lookup"><span data-stu-id="42e4a-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="42e4a-166">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="42e4a-166">Remove Paths</span></span>



| <span data-ttu-id="42e4a-167">Commande</span><span class="sxs-lookup"><span data-stu-id="42e4a-167">Order</span></span> | <span data-ttu-id="42e4a-168">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="42e4a-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="42e4a-169">1</span><span class="sxs-lookup"><span data-stu-id="42e4a-169">1</span></span>     | <span data-ttu-id="42e4a-170">/IFD/EXIF/{UShort = 41992}</span><span class="sxs-lookup"><span data-stu-id="42e4a-170">/ifd/exif/{ushort=41992}</span></span> |
| <span data-ttu-id="42e4a-171">2</span><span class="sxs-lookup"><span data-stu-id="42e4a-171">2</span></span>     | <span data-ttu-id="42e4a-172">/IFD/XMP/EXIF : contraste</span><span class="sxs-lookup"><span data-stu-id="42e4a-172">/ifd/xmp/exif:contrast</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="42e4a-173">Notes</span><span class="sxs-lookup"><span data-stu-id="42e4a-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="42e4a-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="42e4a-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42e4a-175">System. photo. Contrast</span><span class="sxs-lookup"><span data-stu-id="42e4a-175">System.Photo.Contrast</span></span>](../properties/props-system-photo-contrast.md)
</dt> </dl>

 

 
