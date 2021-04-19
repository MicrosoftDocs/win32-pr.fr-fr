---
description: Stratégie de métadonnées de la photo pour la propriété System. image. ColorSpace.
ms.assetid: 10770f16-8db2-4719-bce3-452f578002ec
title: Stratégie de métadonnées de photo System. image. ColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6ef2003d05fa19b958b28950f71ec2d5f73027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521215"
---
# <a name="systemimagecolorspace-photo-metadata-policy"></a><span data-ttu-id="2c2d1-103">Stratégie de métadonnées de photo System. image. ColorSpace</span><span class="sxs-lookup"><span data-stu-id="2c2d1-103">System.Image.ColorSpace Photo Metadata Policy</span></span>

<span data-ttu-id="2c2d1-104">Stratégie de métadonnées de la photo pour la propriété [System. image. colorspace](../properties/props-system-image-colorspace.md) .</span><span class="sxs-lookup"><span data-stu-id="2c2d1-104">The photo metadata policy for the [System.Image.ColorSpace](../properties/props-system-image-colorspace.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="2c2d1-105">A-la</span><span class="sxs-lookup"><span data-stu-id="2c2d1-105">PKEY</span></span>

<span data-ttu-id="2c2d1-106">Image de la \_ \_ ColorSpace</span><span class="sxs-lookup"><span data-stu-id="2c2d1-106">PKEY\_Image\_ColorSpace</span></span>

### <a name="containers"></a><span data-ttu-id="2c2d1-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="2c2d1-107">Containers</span></span>

<span data-ttu-id="2c2d1-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="2c2d1-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="2c2d1-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c2d1-109">Read-Only</span></span>

<span data-ttu-id="2c2d1-110">Oui</span><span class="sxs-lookup"><span data-stu-id="2c2d1-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="2c2d1-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="2c2d1-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="2c2d1-112">\_UI2 VT</span><span class="sxs-lookup"><span data-stu-id="2c2d1-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="2c2d1-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="2c2d1-113">Input Type</span></span>

<span data-ttu-id="2c2d1-114">UShort</span><span class="sxs-lookup"><span data-stu-id="2c2d1-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="2c2d1-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="2c2d1-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="2c2d1-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="2c2d1-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="2c2d1-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="2c2d1-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="2c2d1-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="2c2d1-118">Read Paths</span></span>



| <span data-ttu-id="2c2d1-119">Commande</span><span class="sxs-lookup"><span data-stu-id="2c2d1-119">Order</span></span> | <span data-ttu-id="2c2d1-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="2c2d1-120">Path</span></span>                          | <span data-ttu-id="2c2d1-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="2c2d1-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="2c2d1-122">1</span><span class="sxs-lookup"><span data-stu-id="2c2d1-122">1</span></span>     | <span data-ttu-id="2c2d1-123">/App1/IFD/EXIF/{UShort = 40961}</span><span class="sxs-lookup"><span data-stu-id="2c2d1-123">/app1/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="2c2d1-124">ushort</span><span class="sxs-lookup"><span data-stu-id="2c2d1-124">ushort</span></span>      |
| <span data-ttu-id="2c2d1-125">2</span><span class="sxs-lookup"><span data-stu-id="2c2d1-125">2</span></span>     | <span data-ttu-id="2c2d1-126">/xmp/exif:ColorSpace</span><span class="sxs-lookup"><span data-stu-id="2c2d1-126">/xmp/exif:ColorSpace</span></span>          | <span data-ttu-id="2c2d1-127">unicode</span><span class="sxs-lookup"><span data-stu-id="2c2d1-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="2c2d1-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="2c2d1-128">Write Paths</span></span>



| <span data-ttu-id="2c2d1-129">Commande</span><span class="sxs-lookup"><span data-stu-id="2c2d1-129">Order</span></span> | <span data-ttu-id="2c2d1-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="2c2d1-130">Path</span></span>                          | <span data-ttu-id="2c2d1-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="2c2d1-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="2c2d1-132">1</span><span class="sxs-lookup"><span data-stu-id="2c2d1-132">1</span></span>     | <span data-ttu-id="2c2d1-133">/App1/IFD/EXIF/{UShort = 40961}</span><span class="sxs-lookup"><span data-stu-id="2c2d1-133">/app1/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="2c2d1-134">ushort</span><span class="sxs-lookup"><span data-stu-id="2c2d1-134">ushort</span></span>      |
| <span data-ttu-id="2c2d1-135">2</span><span class="sxs-lookup"><span data-stu-id="2c2d1-135">2</span></span>     | <span data-ttu-id="2c2d1-136">/xmp/exif:ColorSpace</span><span class="sxs-lookup"><span data-stu-id="2c2d1-136">/xmp/exif:ColorSpace</span></span>          | <span data-ttu-id="2c2d1-137">unicode</span><span class="sxs-lookup"><span data-stu-id="2c2d1-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="2c2d1-138">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="2c2d1-138">Remove Paths</span></span>



| <span data-ttu-id="2c2d1-139">Commande</span><span class="sxs-lookup"><span data-stu-id="2c2d1-139">Order</span></span> | <span data-ttu-id="2c2d1-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="2c2d1-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="2c2d1-141">1</span><span class="sxs-lookup"><span data-stu-id="2c2d1-141">1</span></span>     | <span data-ttu-id="2c2d1-142">/App1/IFD/EXIF/{UShort = 40961}</span><span class="sxs-lookup"><span data-stu-id="2c2d1-142">/app1/ifd/exif/{ushort=40961}</span></span> |
| <span data-ttu-id="2c2d1-143">2</span><span class="sxs-lookup"><span data-stu-id="2c2d1-143">2</span></span>     | <span data-ttu-id="2c2d1-144">/xmp/exif:colorspace</span><span class="sxs-lookup"><span data-stu-id="2c2d1-144">/xmp/exif:colorspace</span></span>          |



 

### <a name="tiff-policies"></a><span data-ttu-id="2c2d1-145">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="2c2d1-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="2c2d1-146">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="2c2d1-146">Read Paths</span></span>



| <span data-ttu-id="2c2d1-147">Commande</span><span class="sxs-lookup"><span data-stu-id="2c2d1-147">Order</span></span> | <span data-ttu-id="2c2d1-148">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="2c2d1-148">Path</span></span>                     | <span data-ttu-id="2c2d1-149">Format de disque</span><span class="sxs-lookup"><span data-stu-id="2c2d1-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="2c2d1-150">1</span><span class="sxs-lookup"><span data-stu-id="2c2d1-150">1</span></span>     | <span data-ttu-id="2c2d1-151">/IFD/EXIF/{UShort = 40961}</span><span class="sxs-lookup"><span data-stu-id="2c2d1-151">/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="2c2d1-152">ushort</span><span class="sxs-lookup"><span data-stu-id="2c2d1-152">ushort</span></span>      |
| <span data-ttu-id="2c2d1-153">2</span><span class="sxs-lookup"><span data-stu-id="2c2d1-153">2</span></span>     | <span data-ttu-id="2c2d1-154">/ifd/xmp/exif:ColorSpace</span><span class="sxs-lookup"><span data-stu-id="2c2d1-154">/ifd/xmp/exif:ColorSpace</span></span> | <span data-ttu-id="2c2d1-155">unicode</span><span class="sxs-lookup"><span data-stu-id="2c2d1-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="2c2d1-156">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="2c2d1-156">Write Paths</span></span>



| <span data-ttu-id="2c2d1-157">Commande</span><span class="sxs-lookup"><span data-stu-id="2c2d1-157">Order</span></span> | <span data-ttu-id="2c2d1-158">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="2c2d1-158">Path</span></span>                     | <span data-ttu-id="2c2d1-159">Format de disque</span><span class="sxs-lookup"><span data-stu-id="2c2d1-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="2c2d1-160">1</span><span class="sxs-lookup"><span data-stu-id="2c2d1-160">1</span></span>     | <span data-ttu-id="2c2d1-161">/IFD/EXIF/{UShort = 40961}</span><span class="sxs-lookup"><span data-stu-id="2c2d1-161">/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="2c2d1-162">ushort</span><span class="sxs-lookup"><span data-stu-id="2c2d1-162">ushort</span></span>      |
| <span data-ttu-id="2c2d1-163">2</span><span class="sxs-lookup"><span data-stu-id="2c2d1-163">2</span></span>     | <span data-ttu-id="2c2d1-164">/ifd/xmp/exif:ColorSpace</span><span class="sxs-lookup"><span data-stu-id="2c2d1-164">/ifd/xmp/exif:ColorSpace</span></span> | <span data-ttu-id="2c2d1-165">unicode</span><span class="sxs-lookup"><span data-stu-id="2c2d1-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="2c2d1-166">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="2c2d1-166">Remove Paths</span></span>



| <span data-ttu-id="2c2d1-167">Commande</span><span class="sxs-lookup"><span data-stu-id="2c2d1-167">Order</span></span> | <span data-ttu-id="2c2d1-168">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="2c2d1-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="2c2d1-169">1</span><span class="sxs-lookup"><span data-stu-id="2c2d1-169">1</span></span>     | <span data-ttu-id="2c2d1-170">/IFD/EXIF/{UShort = 40961}</span><span class="sxs-lookup"><span data-stu-id="2c2d1-170">/ifd/exif/{ushort=40961}</span></span> |
| <span data-ttu-id="2c2d1-171">2</span><span class="sxs-lookup"><span data-stu-id="2c2d1-171">2</span></span>     | <span data-ttu-id="2c2d1-172">/ifd/xmp/exif:colorspace</span><span class="sxs-lookup"><span data-stu-id="2c2d1-172">/ifd/xmp/exif:colorspace</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2c2d1-173">Notes</span><span class="sxs-lookup"><span data-stu-id="2c2d1-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c2d1-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2c2d1-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c2d1-175">System. image. ColorSpace</span><span class="sxs-lookup"><span data-stu-id="2c2d1-175">System.Image.ColorSpace</span></span>](../properties/props-system-image-colorspace.md)
</dt> </dl>

 

 
