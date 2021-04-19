---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. MaxAperture.
ms.assetid: 9d12d265-0b0a-44d9-bbf6-ca7d748382ee
title: Stratégie de métadonnées de photo System. photo. MaxAperture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f3dab4d5ebf89033de03dfce887a7cea10fa11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530085"
---
# <a name="systemphotomaxaperture-photo-metadata-policy"></a><span data-ttu-id="5eb34-103">Stratégie de métadonnées de photo System. photo. MaxAperture</span><span class="sxs-lookup"><span data-stu-id="5eb34-103">System.Photo.MaxAperture Photo Metadata Policy</span></span>

<span data-ttu-id="5eb34-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. MaxAperture](../properties/props-system-photo-maxaperture.md) .</span><span class="sxs-lookup"><span data-stu-id="5eb34-104">The photo metadata policy for the [System.Photo.MaxAperture](../properties/props-system-photo-maxaperture.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="5eb34-105">A-la</span><span class="sxs-lookup"><span data-stu-id="5eb34-105">PKEY</span></span>

<span data-ttu-id="5eb34-106">\_Photo \_ MaxAperture</span><span class="sxs-lookup"><span data-stu-id="5eb34-106">PKEY\_Photo\_MaxAperture</span></span>

### <a name="containers"></a><span data-ttu-id="5eb34-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="5eb34-107">Containers</span></span>

<span data-ttu-id="5eb34-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="5eb34-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="5eb34-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5eb34-109">Read-Only</span></span>

<span data-ttu-id="5eb34-110">Oui</span><span class="sxs-lookup"><span data-stu-id="5eb34-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="5eb34-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="5eb34-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="5eb34-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="5eb34-112">VT\_R8</span></span>

### <a name="input-type"></a><span data-ttu-id="5eb34-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="5eb34-113">Input Type</span></span>

<span data-ttu-id="5eb34-114">Double</span><span class="sxs-lookup"><span data-stu-id="5eb34-114">Double</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="5eb34-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="5eb34-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="5eb34-116">Cette valeur est générée à partir de System. photo. MaxApertureNumerator et de System. photo. MaxApertureDenominator.</span><span class="sxs-lookup"><span data-stu-id="5eb34-116">This value is generated from System.Photo.MaxApertureNumerator and System.Photo.MaxApertureDenominator.</span></span> <span data-ttu-id="5eb34-117">Il ne peut pas être écrit directement.</span><span class="sxs-lookup"><span data-stu-id="5eb34-117">It cannot be written directly.</span></span> <span data-ttu-id="5eb34-118">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="5eb34-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="5eb34-119">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="5eb34-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="5eb34-120">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="5eb34-120">Read Paths</span></span>



| <span data-ttu-id="5eb34-121">Commande</span><span class="sxs-lookup"><span data-stu-id="5eb34-121">Order</span></span> | <span data-ttu-id="5eb34-122">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="5eb34-122">Path</span></span>                          | <span data-ttu-id="5eb34-123">Format de disque</span><span class="sxs-lookup"><span data-stu-id="5eb34-123">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="5eb34-124">1</span><span class="sxs-lookup"><span data-stu-id="5eb34-124">1</span></span>     | <span data-ttu-id="5eb34-125">/App1/IFD/EXIF/{UShort = 37381}</span><span class="sxs-lookup"><span data-stu-id="5eb34-125">/app1/ifd/exif/{ushort=37381}</span></span> |             |
| <span data-ttu-id="5eb34-126">2</span><span class="sxs-lookup"><span data-stu-id="5eb34-126">2</span></span>     | <span data-ttu-id="5eb34-127">/xmp/exif:MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="5eb34-127">/xmp/exif:MaxApertureValue</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="5eb34-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="5eb34-128">Write Paths</span></span>



| <span data-ttu-id="5eb34-129">Commande</span><span class="sxs-lookup"><span data-stu-id="5eb34-129">Order</span></span> | <span data-ttu-id="5eb34-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="5eb34-130">Path</span></span>                          | <span data-ttu-id="5eb34-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="5eb34-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="5eb34-132">1</span><span class="sxs-lookup"><span data-stu-id="5eb34-132">1</span></span>     | <span data-ttu-id="5eb34-133">/App1/IFD/EXIF/{UShort = 37381}</span><span class="sxs-lookup"><span data-stu-id="5eb34-133">/app1/ifd/exif/{ushort=37381}</span></span> |             |
| <span data-ttu-id="5eb34-134">2</span><span class="sxs-lookup"><span data-stu-id="5eb34-134">2</span></span>     | <span data-ttu-id="5eb34-135">/xmp/exif:MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="5eb34-135">/xmp/exif:MaxApertureValue</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="5eb34-136">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="5eb34-136">Remove Paths</span></span>



| <span data-ttu-id="5eb34-137">Commande</span><span class="sxs-lookup"><span data-stu-id="5eb34-137">Order</span></span> | <span data-ttu-id="5eb34-138">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="5eb34-138">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="5eb34-139">1</span><span class="sxs-lookup"><span data-stu-id="5eb34-139">1</span></span>     | <span data-ttu-id="5eb34-140">/App1/IFD/EXIF/{UShort = 37381}</span><span class="sxs-lookup"><span data-stu-id="5eb34-140">/app1/ifd/exif/{ushort=37381}</span></span> |
| <span data-ttu-id="5eb34-141">2</span><span class="sxs-lookup"><span data-stu-id="5eb34-141">2</span></span>     | <span data-ttu-id="5eb34-142">/xmp/exif:maxaperturevalue</span><span class="sxs-lookup"><span data-stu-id="5eb34-142">/xmp/exif:maxaperturevalue</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="5eb34-143">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="5eb34-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="5eb34-144">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="5eb34-144">Read Paths</span></span>



| <span data-ttu-id="5eb34-145">Commande</span><span class="sxs-lookup"><span data-stu-id="5eb34-145">Order</span></span> | <span data-ttu-id="5eb34-146">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="5eb34-146">Path</span></span>                           | <span data-ttu-id="5eb34-147">Format de disque</span><span class="sxs-lookup"><span data-stu-id="5eb34-147">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="5eb34-148">1</span><span class="sxs-lookup"><span data-stu-id="5eb34-148">1</span></span>     | <span data-ttu-id="5eb34-149">/IFD/EXIF/{UShort = 37381}</span><span class="sxs-lookup"><span data-stu-id="5eb34-149">/ifd/exif/{ushort=37381}</span></span>       |             |
| <span data-ttu-id="5eb34-150">2</span><span class="sxs-lookup"><span data-stu-id="5eb34-150">2</span></span>     | <span data-ttu-id="5eb34-151">/ifd/xmp/exif:MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="5eb34-151">/ifd/xmp/exif:MaxApertureValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="5eb34-152">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="5eb34-152">Write Paths</span></span>



| <span data-ttu-id="5eb34-153">Commande</span><span class="sxs-lookup"><span data-stu-id="5eb34-153">Order</span></span> | <span data-ttu-id="5eb34-154">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="5eb34-154">Path</span></span>                           | <span data-ttu-id="5eb34-155">Format de disque</span><span class="sxs-lookup"><span data-stu-id="5eb34-155">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="5eb34-156">1</span><span class="sxs-lookup"><span data-stu-id="5eb34-156">1</span></span>     | <span data-ttu-id="5eb34-157">/IFD/EXIF/{UShort = 37381}</span><span class="sxs-lookup"><span data-stu-id="5eb34-157">/ifd/exif/{ushort=37381}</span></span>       |             |
| <span data-ttu-id="5eb34-158">2</span><span class="sxs-lookup"><span data-stu-id="5eb34-158">2</span></span>     | <span data-ttu-id="5eb34-159">/ifd/xmp/exif:MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="5eb34-159">/ifd/xmp/exif:MaxApertureValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="5eb34-160">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="5eb34-160">Remove Paths</span></span>



| <span data-ttu-id="5eb34-161">Commande</span><span class="sxs-lookup"><span data-stu-id="5eb34-161">Order</span></span> | <span data-ttu-id="5eb34-162">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="5eb34-162">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="5eb34-163">1</span><span class="sxs-lookup"><span data-stu-id="5eb34-163">1</span></span>     | <span data-ttu-id="5eb34-164">/IFD/EXIF/{UShort = 37381}</span><span class="sxs-lookup"><span data-stu-id="5eb34-164">/ifd/exif/{ushort=37381}</span></span>       |
| <span data-ttu-id="5eb34-165">2</span><span class="sxs-lookup"><span data-stu-id="5eb34-165">2</span></span>     | <span data-ttu-id="5eb34-166">/ifd/xmp/exif:maxaperturevalue</span><span class="sxs-lookup"><span data-stu-id="5eb34-166">/ifd/xmp/exif:maxaperturevalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5eb34-167">Notes</span><span class="sxs-lookup"><span data-stu-id="5eb34-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="5eb34-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5eb34-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5eb34-169">System. photo. MaxAperture</span><span class="sxs-lookup"><span data-stu-id="5eb34-169">System.Photo.MaxAperture</span></span>](../properties/props-system-photo-maxaperture.md)
</dt> </dl>

 

 
