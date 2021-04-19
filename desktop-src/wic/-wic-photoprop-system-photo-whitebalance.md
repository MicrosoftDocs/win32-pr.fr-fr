---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. WhiteBalance.
ms.assetid: 7b3a31e6-a929-41e4-b7f0-c5b3beac2519
title: Stratégie de métadonnées de photo System. photo. WhiteBalance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc333cedcd4665ace37033452ec3c7f0336f13e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518820"
---
# <a name="systemphotowhitebalance-photo-metadata-policy"></a><span data-ttu-id="bc222-103">Stratégie de métadonnées de photo System. photo. WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="bc222-103">System.Photo.WhiteBalance Photo Metadata Policy</span></span>

<span data-ttu-id="bc222-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. WhiteBalance](../properties/props-system-photo-whitebalance.md) .</span><span class="sxs-lookup"><span data-stu-id="bc222-104">The photo metadata policy for the [System.Photo.WhiteBalance](../properties/props-system-photo-whitebalance.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="bc222-105">A-la</span><span class="sxs-lookup"><span data-stu-id="bc222-105">PKEY</span></span>

<span data-ttu-id="bc222-106">\_Photo \_ WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="bc222-106">PKEY\_Photo\_WhiteBalance</span></span>

### <a name="containers"></a><span data-ttu-id="bc222-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="bc222-107">Containers</span></span>

<span data-ttu-id="bc222-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="bc222-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="bc222-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bc222-109">Read-Only</span></span>

<span data-ttu-id="bc222-110">Non</span><span class="sxs-lookup"><span data-stu-id="bc222-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="bc222-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="bc222-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="bc222-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="bc222-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="bc222-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="bc222-113">Input Type</span></span>

<span data-ttu-id="bc222-114">UShort</span><span class="sxs-lookup"><span data-stu-id="bc222-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="bc222-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="bc222-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="bc222-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="bc222-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="bc222-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="bc222-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="bc222-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="bc222-118">Read Paths</span></span>



| <span data-ttu-id="bc222-119">Commande</span><span class="sxs-lookup"><span data-stu-id="bc222-119">Order</span></span> | <span data-ttu-id="bc222-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="bc222-120">Path</span></span>                          | <span data-ttu-id="bc222-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="bc222-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="bc222-122">1</span><span class="sxs-lookup"><span data-stu-id="bc222-122">1</span></span>     | <span data-ttu-id="bc222-123">/App1/IFD/EXIF/{UShort = 41987}</span><span class="sxs-lookup"><span data-stu-id="bc222-123">/app1/ifd/exif/{ushort=41987}</span></span> | <span data-ttu-id="bc222-124">ushort</span><span class="sxs-lookup"><span data-stu-id="bc222-124">ushort</span></span>      |
| <span data-ttu-id="bc222-125">2</span><span class="sxs-lookup"><span data-stu-id="bc222-125">2</span></span>     | <span data-ttu-id="bc222-126">/xmp/exif:WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="bc222-126">/xmp/exif:WhiteBalance</span></span>        | <span data-ttu-id="bc222-127">unicode</span><span class="sxs-lookup"><span data-stu-id="bc222-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="bc222-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="bc222-128">Write Paths</span></span>



| <span data-ttu-id="bc222-129">Commande</span><span class="sxs-lookup"><span data-stu-id="bc222-129">Order</span></span> | <span data-ttu-id="bc222-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="bc222-130">Path</span></span>                          | <span data-ttu-id="bc222-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="bc222-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="bc222-132">1</span><span class="sxs-lookup"><span data-stu-id="bc222-132">1</span></span>     | <span data-ttu-id="bc222-133">/App1/IFD/EXIF/{UShort = 41987}</span><span class="sxs-lookup"><span data-stu-id="bc222-133">/app1/ifd/exif/{ushort=41987}</span></span> | <span data-ttu-id="bc222-134">ushort</span><span class="sxs-lookup"><span data-stu-id="bc222-134">ushort</span></span>      |
| <span data-ttu-id="bc222-135">2</span><span class="sxs-lookup"><span data-stu-id="bc222-135">2</span></span>     | <span data-ttu-id="bc222-136">/xmp/exif:WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="bc222-136">/xmp/exif:WhiteBalance</span></span>        | <span data-ttu-id="bc222-137">unicode</span><span class="sxs-lookup"><span data-stu-id="bc222-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="bc222-138">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="bc222-138">Remove Paths</span></span>



| <span data-ttu-id="bc222-139">Commande</span><span class="sxs-lookup"><span data-stu-id="bc222-139">Order</span></span> | <span data-ttu-id="bc222-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="bc222-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="bc222-141">1</span><span class="sxs-lookup"><span data-stu-id="bc222-141">1</span></span>     | <span data-ttu-id="bc222-142">/App1/IFD/EXIF/{UShort = 41987}</span><span class="sxs-lookup"><span data-stu-id="bc222-142">/app1/ifd/exif/{ushort=41987}</span></span> |
| <span data-ttu-id="bc222-143">2</span><span class="sxs-lookup"><span data-stu-id="bc222-143">2</span></span>     | <span data-ttu-id="bc222-144">/xmp/exif:whitebalance</span><span class="sxs-lookup"><span data-stu-id="bc222-144">/xmp/exif:whitebalance</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="bc222-145">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="bc222-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="bc222-146">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="bc222-146">Read Paths</span></span>



| <span data-ttu-id="bc222-147">Commande</span><span class="sxs-lookup"><span data-stu-id="bc222-147">Order</span></span> | <span data-ttu-id="bc222-148">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="bc222-148">Path</span></span>                       | <span data-ttu-id="bc222-149">Format de disque</span><span class="sxs-lookup"><span data-stu-id="bc222-149">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="bc222-150">1</span><span class="sxs-lookup"><span data-stu-id="bc222-150">1</span></span>     | <span data-ttu-id="bc222-151">/IFD/EXIF/{UShort = 41987}</span><span class="sxs-lookup"><span data-stu-id="bc222-151">/ifd/exif/{ushort=41987}</span></span>   | <span data-ttu-id="bc222-152">ushort</span><span class="sxs-lookup"><span data-stu-id="bc222-152">ushort</span></span>      |
| <span data-ttu-id="bc222-153">2</span><span class="sxs-lookup"><span data-stu-id="bc222-153">2</span></span>     | <span data-ttu-id="bc222-154">/ifd/xmp/exif:WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="bc222-154">/ifd/xmp/exif:WhiteBalance</span></span> | <span data-ttu-id="bc222-155">unicode</span><span class="sxs-lookup"><span data-stu-id="bc222-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="bc222-156">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="bc222-156">Write Paths</span></span>



| <span data-ttu-id="bc222-157">Commande</span><span class="sxs-lookup"><span data-stu-id="bc222-157">Order</span></span> | <span data-ttu-id="bc222-158">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="bc222-158">Path</span></span>                       | <span data-ttu-id="bc222-159">Format de disque</span><span class="sxs-lookup"><span data-stu-id="bc222-159">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="bc222-160">1</span><span class="sxs-lookup"><span data-stu-id="bc222-160">1</span></span>     | <span data-ttu-id="bc222-161">/IFD/EXIF/{UShort = 41987}</span><span class="sxs-lookup"><span data-stu-id="bc222-161">/ifd/exif/{ushort=41987}</span></span>   | <span data-ttu-id="bc222-162">ushort</span><span class="sxs-lookup"><span data-stu-id="bc222-162">ushort</span></span>      |
| <span data-ttu-id="bc222-163">2</span><span class="sxs-lookup"><span data-stu-id="bc222-163">2</span></span>     | <span data-ttu-id="bc222-164">/ifd/xmp/exif:WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="bc222-164">/ifd/xmp/exif:WhiteBalance</span></span> | <span data-ttu-id="bc222-165">unicode</span><span class="sxs-lookup"><span data-stu-id="bc222-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="bc222-166">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="bc222-166">Remove Paths</span></span>



| <span data-ttu-id="bc222-167">Commande</span><span class="sxs-lookup"><span data-stu-id="bc222-167">Order</span></span> | <span data-ttu-id="bc222-168">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="bc222-168">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="bc222-169">1</span><span class="sxs-lookup"><span data-stu-id="bc222-169">1</span></span>     | <span data-ttu-id="bc222-170">/IFD/EXIF/{UShort = 41987}</span><span class="sxs-lookup"><span data-stu-id="bc222-170">/ifd/exif/{ushort=41987}</span></span>   |
| <span data-ttu-id="bc222-171">2</span><span class="sxs-lookup"><span data-stu-id="bc222-171">2</span></span>     | <span data-ttu-id="bc222-172">/ifd/xmp/exif:whitebalance</span><span class="sxs-lookup"><span data-stu-id="bc222-172">/ifd/xmp/exif:whitebalance</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="bc222-173">Notes</span><span class="sxs-lookup"><span data-stu-id="bc222-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc222-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc222-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc222-175">System. photo. WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="bc222-175">System.Photo.WhiteBalance</span></span>](../properties/props-system-photo-whitebalance.md)
</dt> </dl>

 

 
