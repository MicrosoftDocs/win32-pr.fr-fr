---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. MeteringMode.
ms.assetid: cb0bf0d5-eccf-4345-a242-76769c34e02d
title: Stratégie de métadonnées de photo System. photo. MeteringMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12a4443521c84113e4e2a6f4c2b9b2b3f822ae90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536797"
---
# <a name="systemphotometeringmode-photo-metadata-policy"></a><span data-ttu-id="9f0a4-103">Stratégie de métadonnées de photo System. photo. MeteringMode</span><span class="sxs-lookup"><span data-stu-id="9f0a4-103">System.Photo.MeteringMode Photo Metadata Policy</span></span>

<span data-ttu-id="9f0a4-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. MeteringMode](../properties/props-system-photo-meteringmode.md) .</span><span class="sxs-lookup"><span data-stu-id="9f0a4-104">The photo metadata policy for the [System.Photo.MeteringMode](../properties/props-system-photo-meteringmode.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="9f0a4-105">A-la</span><span class="sxs-lookup"><span data-stu-id="9f0a4-105">PKEY</span></span>

<span data-ttu-id="9f0a4-106">\_Photo \_ MeteringMode</span><span class="sxs-lookup"><span data-stu-id="9f0a4-106">PKEY\_Photo\_MeteringMode</span></span>

### <a name="containers"></a><span data-ttu-id="9f0a4-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="9f0a4-107">Containers</span></span>

<span data-ttu-id="9f0a4-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="9f0a4-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="9f0a4-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f0a4-109">Read-Only</span></span>

<span data-ttu-id="9f0a4-110">Non</span><span class="sxs-lookup"><span data-stu-id="9f0a4-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="9f0a4-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="9f0a4-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="9f0a4-112">\_UI2 VT</span><span class="sxs-lookup"><span data-stu-id="9f0a4-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="9f0a4-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="9f0a4-113">Input Type</span></span>

<span data-ttu-id="9f0a4-114">UShort</span><span class="sxs-lookup"><span data-stu-id="9f0a4-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="9f0a4-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="9f0a4-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="9f0a4-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="9f0a4-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="9f0a4-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="9f0a4-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="9f0a4-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="9f0a4-118">Read Paths</span></span>



| <span data-ttu-id="9f0a4-119">Commande</span><span class="sxs-lookup"><span data-stu-id="9f0a4-119">Order</span></span> | <span data-ttu-id="9f0a4-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="9f0a4-120">Path</span></span>                          | <span data-ttu-id="9f0a4-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="9f0a4-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="9f0a4-122">1</span><span class="sxs-lookup"><span data-stu-id="9f0a4-122">1</span></span>     | <span data-ttu-id="9f0a4-123">/App1/IFD/EXIF/{UShort = 37383}</span><span class="sxs-lookup"><span data-stu-id="9f0a4-123">/app1/ifd/exif/{ushort=37383}</span></span> | <span data-ttu-id="9f0a4-124">ushort</span><span class="sxs-lookup"><span data-stu-id="9f0a4-124">ushort</span></span>      |
| <span data-ttu-id="9f0a4-125">2</span><span class="sxs-lookup"><span data-stu-id="9f0a4-125">2</span></span>     | <span data-ttu-id="9f0a4-126">/xmp/exif:MeteringMode</span><span class="sxs-lookup"><span data-stu-id="9f0a4-126">/xmp/exif:MeteringMode</span></span>        | <span data-ttu-id="9f0a4-127">unicode</span><span class="sxs-lookup"><span data-stu-id="9f0a4-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="9f0a4-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="9f0a4-128">Write Paths</span></span>



| <span data-ttu-id="9f0a4-129">Commande</span><span class="sxs-lookup"><span data-stu-id="9f0a4-129">Order</span></span> | <span data-ttu-id="9f0a4-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="9f0a4-130">Path</span></span>                          | <span data-ttu-id="9f0a4-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="9f0a4-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="9f0a4-132">1</span><span class="sxs-lookup"><span data-stu-id="9f0a4-132">1</span></span>     | <span data-ttu-id="9f0a4-133">/App1/IFD/EXIF/{UShort = 37383}</span><span class="sxs-lookup"><span data-stu-id="9f0a4-133">/app1/ifd/exif/{ushort=37383}</span></span> | <span data-ttu-id="9f0a4-134">ushort</span><span class="sxs-lookup"><span data-stu-id="9f0a4-134">ushort</span></span>      |
| <span data-ttu-id="9f0a4-135">2</span><span class="sxs-lookup"><span data-stu-id="9f0a4-135">2</span></span>     | <span data-ttu-id="9f0a4-136">/xmp/exif:MeteringMode</span><span class="sxs-lookup"><span data-stu-id="9f0a4-136">/xmp/exif:MeteringMode</span></span>        | <span data-ttu-id="9f0a4-137">unicode</span><span class="sxs-lookup"><span data-stu-id="9f0a4-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="9f0a4-138">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="9f0a4-138">Remove Paths</span></span>



| <span data-ttu-id="9f0a4-139">Commande</span><span class="sxs-lookup"><span data-stu-id="9f0a4-139">Order</span></span> | <span data-ttu-id="9f0a4-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="9f0a4-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="9f0a4-141">1</span><span class="sxs-lookup"><span data-stu-id="9f0a4-141">1</span></span>     | <span data-ttu-id="9f0a4-142">/App1/IFD/EXIF/{UShort = 37383}</span><span class="sxs-lookup"><span data-stu-id="9f0a4-142">/app1/ifd/exif/{ushort=37383}</span></span> |
| <span data-ttu-id="9f0a4-143">2</span><span class="sxs-lookup"><span data-stu-id="9f0a4-143">2</span></span>     | <span data-ttu-id="9f0a4-144">/xmp/exif:meteringmode</span><span class="sxs-lookup"><span data-stu-id="9f0a4-144">/xmp/exif:meteringmode</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="9f0a4-145">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="9f0a4-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="9f0a4-146">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="9f0a4-146">Read Paths</span></span>



| <span data-ttu-id="9f0a4-147">Commande</span><span class="sxs-lookup"><span data-stu-id="9f0a4-147">Order</span></span> | <span data-ttu-id="9f0a4-148">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="9f0a4-148">Path</span></span>                       | <span data-ttu-id="9f0a4-149">Format de disque</span><span class="sxs-lookup"><span data-stu-id="9f0a4-149">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="9f0a4-150">1</span><span class="sxs-lookup"><span data-stu-id="9f0a4-150">1</span></span>     | <span data-ttu-id="9f0a4-151">/IFD/EXIF/{UShort = 37383}</span><span class="sxs-lookup"><span data-stu-id="9f0a4-151">/ifd/exif/{ushort=37383}</span></span>   | <span data-ttu-id="9f0a4-152">ushort</span><span class="sxs-lookup"><span data-stu-id="9f0a4-152">ushort</span></span>      |
| <span data-ttu-id="9f0a4-153">2</span><span class="sxs-lookup"><span data-stu-id="9f0a4-153">2</span></span>     | <span data-ttu-id="9f0a4-154">/ifd/xmp/exif:MeteringMode</span><span class="sxs-lookup"><span data-stu-id="9f0a4-154">/ifd/xmp/exif:MeteringMode</span></span> | <span data-ttu-id="9f0a4-155">unicode</span><span class="sxs-lookup"><span data-stu-id="9f0a4-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="9f0a4-156">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="9f0a4-156">Write Paths</span></span>



| <span data-ttu-id="9f0a4-157">Commande</span><span class="sxs-lookup"><span data-stu-id="9f0a4-157">Order</span></span> | <span data-ttu-id="9f0a4-158">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="9f0a4-158">Path</span></span>                       | <span data-ttu-id="9f0a4-159">Format de disque</span><span class="sxs-lookup"><span data-stu-id="9f0a4-159">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="9f0a4-160">1</span><span class="sxs-lookup"><span data-stu-id="9f0a4-160">1</span></span>     | <span data-ttu-id="9f0a4-161">/IFD/EXIF/{UShort = 37383}</span><span class="sxs-lookup"><span data-stu-id="9f0a4-161">/ifd/exif/{ushort=37383}</span></span>   | <span data-ttu-id="9f0a4-162">ushort</span><span class="sxs-lookup"><span data-stu-id="9f0a4-162">ushort</span></span>      |
| <span data-ttu-id="9f0a4-163">2</span><span class="sxs-lookup"><span data-stu-id="9f0a4-163">2</span></span>     | <span data-ttu-id="9f0a4-164">/ifd/xmp/exif:MeteringMode</span><span class="sxs-lookup"><span data-stu-id="9f0a4-164">/ifd/xmp/exif:MeteringMode</span></span> | <span data-ttu-id="9f0a4-165">unicode</span><span class="sxs-lookup"><span data-stu-id="9f0a4-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="9f0a4-166">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="9f0a4-166">Remove Paths</span></span>



| <span data-ttu-id="9f0a4-167">Commande</span><span class="sxs-lookup"><span data-stu-id="9f0a4-167">Order</span></span> | <span data-ttu-id="9f0a4-168">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="9f0a4-168">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="9f0a4-169">1</span><span class="sxs-lookup"><span data-stu-id="9f0a4-169">1</span></span>     | <span data-ttu-id="9f0a4-170">/IFD/EXIF/{UShort = 37383}</span><span class="sxs-lookup"><span data-stu-id="9f0a4-170">/ifd/exif/{ushort=37383}</span></span>   |
| <span data-ttu-id="9f0a4-171">2</span><span class="sxs-lookup"><span data-stu-id="9f0a4-171">2</span></span>     | <span data-ttu-id="9f0a4-172">/ifd/xmp/exif:meteringmode</span><span class="sxs-lookup"><span data-stu-id="9f0a4-172">/ifd/xmp/exif:meteringmode</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9f0a4-173">Notes</span><span class="sxs-lookup"><span data-stu-id="9f0a4-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f0a4-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9f0a4-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f0a4-175">System. photo. MeteringMode</span><span class="sxs-lookup"><span data-stu-id="9f0a4-175">System.Photo.MeteringMode</span></span>](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
