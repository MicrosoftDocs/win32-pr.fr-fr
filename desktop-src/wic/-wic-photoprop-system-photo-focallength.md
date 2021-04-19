---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. FocalLength.
ms.assetid: a282c31f-00dd-4df5-9b93-300bb9bc8f2d
title: Stratégie de métadonnées de photo System. photo. FocalLength
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7b36240713782c98d52e4fbf4dae5c0c06082
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521058"
---
# <a name="systemphotofocallength-photo-metadata-policy"></a><span data-ttu-id="c92a9-103">Stratégie de métadonnées de photo System. photo. FocalLength</span><span class="sxs-lookup"><span data-stu-id="c92a9-103">System.Photo.FocalLength Photo Metadata Policy</span></span>

<span data-ttu-id="c92a9-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. focalLength](../properties/props-system-photo-focallength.md) .</span><span class="sxs-lookup"><span data-stu-id="c92a9-104">The photo metadata policy for the [System.Photo.FocalLength](../properties/props-system-photo-focallength.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="c92a9-105">A-la</span><span class="sxs-lookup"><span data-stu-id="c92a9-105">PKEY</span></span>

<span data-ttu-id="c92a9-106">\_Photo \_ focalLength</span><span class="sxs-lookup"><span data-stu-id="c92a9-106">PKEY\_Photo\_FocalLength</span></span>

### <a name="containers"></a><span data-ttu-id="c92a9-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="c92a9-107">Containers</span></span>

<span data-ttu-id="c92a9-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c92a9-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="c92a9-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c92a9-109">Read-Only</span></span>

<span data-ttu-id="c92a9-110">Oui</span><span class="sxs-lookup"><span data-stu-id="c92a9-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="c92a9-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="c92a9-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="c92a9-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="c92a9-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="c92a9-113">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="c92a9-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="c92a9-114">Cette valeur est générée à partir de System. photo. FocalLengthNumerator et de System. photo. FocalLengthDenominator.</span><span class="sxs-lookup"><span data-stu-id="c92a9-114">This value is generated from System.Photo.FocalLengthNumerator and System.Photo.FocalLengthDenominator.</span></span> <span data-ttu-id="c92a9-115">Il ne peut pas être écrit directement.</span><span class="sxs-lookup"><span data-stu-id="c92a9-115">It cannot be written directly.</span></span> <span data-ttu-id="c92a9-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="c92a9-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="c92a9-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="c92a9-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="c92a9-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="c92a9-118">Read Paths</span></span>



| <span data-ttu-id="c92a9-119">Commande</span><span class="sxs-lookup"><span data-stu-id="c92a9-119">Order</span></span> | <span data-ttu-id="c92a9-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c92a9-120">Path</span></span>                          | <span data-ttu-id="c92a9-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="c92a9-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="c92a9-122">1</span><span class="sxs-lookup"><span data-stu-id="c92a9-122">1</span></span>     | <span data-ttu-id="c92a9-123">/App1/IFD/EXIF/{UShort = 37386}</span><span class="sxs-lookup"><span data-stu-id="c92a9-123">/app1/ifd/exif/{ushort=37386}</span></span> |             |
| <span data-ttu-id="c92a9-124">2</span><span class="sxs-lookup"><span data-stu-id="c92a9-124">2</span></span>     | <span data-ttu-id="c92a9-125">/xmp/exif:FocalLength</span><span class="sxs-lookup"><span data-stu-id="c92a9-125">/xmp/exif:FocalLength</span></span>         |             |



 

### <a name="write-paths"></a><span data-ttu-id="c92a9-126">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="c92a9-126">Write Paths</span></span>



| <span data-ttu-id="c92a9-127">Commande</span><span class="sxs-lookup"><span data-stu-id="c92a9-127">Order</span></span> | <span data-ttu-id="c92a9-128">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c92a9-128">Path</span></span>                          | <span data-ttu-id="c92a9-129">Format de disque</span><span class="sxs-lookup"><span data-stu-id="c92a9-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="c92a9-130">1</span><span class="sxs-lookup"><span data-stu-id="c92a9-130">1</span></span>     | <span data-ttu-id="c92a9-131">/App1/IFD/EXIF/{UShort = 37386}</span><span class="sxs-lookup"><span data-stu-id="c92a9-131">/app1/ifd/exif/{ushort=37386}</span></span> |             |
| <span data-ttu-id="c92a9-132">2</span><span class="sxs-lookup"><span data-stu-id="c92a9-132">2</span></span>     | <span data-ttu-id="c92a9-133">/xmp/exif:FocalLength</span><span class="sxs-lookup"><span data-stu-id="c92a9-133">/xmp/exif:FocalLength</span></span>         |             |



 

### <a name="remove-paths"></a><span data-ttu-id="c92a9-134">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="c92a9-134">Remove Paths</span></span>



| <span data-ttu-id="c92a9-135">Commande</span><span class="sxs-lookup"><span data-stu-id="c92a9-135">Order</span></span> | <span data-ttu-id="c92a9-136">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c92a9-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="c92a9-137">1</span><span class="sxs-lookup"><span data-stu-id="c92a9-137">1</span></span>     | <span data-ttu-id="c92a9-138">/App1/IFD/EXIF/{UShort = 37386}</span><span class="sxs-lookup"><span data-stu-id="c92a9-138">/app1/ifd/exif/{ushort=37386}</span></span> |
| <span data-ttu-id="c92a9-139">2</span><span class="sxs-lookup"><span data-stu-id="c92a9-139">2</span></span>     | <span data-ttu-id="c92a9-140">/xmp/exif:focallength</span><span class="sxs-lookup"><span data-stu-id="c92a9-140">/xmp/exif:focallength</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="c92a9-141">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="c92a9-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="c92a9-142">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="c92a9-142">Read Paths</span></span>



| <span data-ttu-id="c92a9-143">Commande</span><span class="sxs-lookup"><span data-stu-id="c92a9-143">Order</span></span> | <span data-ttu-id="c92a9-144">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c92a9-144">Path</span></span>                      | <span data-ttu-id="c92a9-145">Format de disque</span><span class="sxs-lookup"><span data-stu-id="c92a9-145">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="c92a9-146">1</span><span class="sxs-lookup"><span data-stu-id="c92a9-146">1</span></span>     | <span data-ttu-id="c92a9-147">/IFD/EXIF/{UShort = 37386}</span><span class="sxs-lookup"><span data-stu-id="c92a9-147">/ifd/exif/{ushort=37386}</span></span>  |             |
| <span data-ttu-id="c92a9-148">2</span><span class="sxs-lookup"><span data-stu-id="c92a9-148">2</span></span>     | <span data-ttu-id="c92a9-149">/ifd/xmp/exif:FocalLength</span><span class="sxs-lookup"><span data-stu-id="c92a9-149">/ifd/xmp/exif:FocalLength</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="c92a9-150">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="c92a9-150">Write Paths</span></span>



| <span data-ttu-id="c92a9-151">Commande</span><span class="sxs-lookup"><span data-stu-id="c92a9-151">Order</span></span> | <span data-ttu-id="c92a9-152">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c92a9-152">Path</span></span>                      | <span data-ttu-id="c92a9-153">Format de disque</span><span class="sxs-lookup"><span data-stu-id="c92a9-153">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="c92a9-154">1</span><span class="sxs-lookup"><span data-stu-id="c92a9-154">1</span></span>     | <span data-ttu-id="c92a9-155">/IFD/EXIF/{UShort = 37386}</span><span class="sxs-lookup"><span data-stu-id="c92a9-155">/ifd/exif/{ushort=37386}</span></span>  |             |
| <span data-ttu-id="c92a9-156">2</span><span class="sxs-lookup"><span data-stu-id="c92a9-156">2</span></span>     | <span data-ttu-id="c92a9-157">/ifd/xmp/exif:FocalLength</span><span class="sxs-lookup"><span data-stu-id="c92a9-157">/ifd/xmp/exif:FocalLength</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="c92a9-158">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="c92a9-158">Remove Paths</span></span>



| <span data-ttu-id="c92a9-159">Commande</span><span class="sxs-lookup"><span data-stu-id="c92a9-159">Order</span></span> | <span data-ttu-id="c92a9-160">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c92a9-160">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="c92a9-161">1</span><span class="sxs-lookup"><span data-stu-id="c92a9-161">1</span></span>     | <span data-ttu-id="c92a9-162">/IFD/EXIF/{UShort = 37386}</span><span class="sxs-lookup"><span data-stu-id="c92a9-162">/ifd/exif/{ushort=37386}</span></span>  |
| <span data-ttu-id="c92a9-163">2</span><span class="sxs-lookup"><span data-stu-id="c92a9-163">2</span></span>     | <span data-ttu-id="c92a9-164">/ifd/xmp/exif:focallength</span><span class="sxs-lookup"><span data-stu-id="c92a9-164">/ifd/xmp/exif:focallength</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c92a9-165">Notes</span><span class="sxs-lookup"><span data-stu-id="c92a9-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="c92a9-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c92a9-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c92a9-167">System. photo. FocalLength</span><span class="sxs-lookup"><span data-stu-id="c92a9-167">System.Photo.FocalLength</span></span>](../properties/props-system-photo-focallength.md)
</dt> </dl>

 

 
