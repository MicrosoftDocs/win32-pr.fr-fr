---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. Brightness.
ms.assetid: 3fd73845-f1d9-468c-abf8-081109880974
title: Stratégie de métadonnées de photo System. photo. Brightness
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd7328b4d40b8d1582dcc17b317b706b2695c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952828"
---
# <a name="systemphotobrightness-photo-metadata-policy"></a><span data-ttu-id="c157a-103">Stratégie de métadonnées de photo System. photo. Brightness</span><span class="sxs-lookup"><span data-stu-id="c157a-103">System.Photo.Brightness Photo Metadata Policy</span></span>

<span data-ttu-id="c157a-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. Brightness](../properties/props-system-photo-aperture.md) .</span><span class="sxs-lookup"><span data-stu-id="c157a-104">The photo metadata policy for the [System.Photo.Brightness](../properties/props-system-photo-aperture.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="c157a-105">A-la</span><span class="sxs-lookup"><span data-stu-id="c157a-105">PKEY</span></span>

<span data-ttu-id="c157a-106">Luminosité de la photo de la \_ \_</span><span class="sxs-lookup"><span data-stu-id="c157a-106">PKEY\_Photo\_Brightness</span></span>

### <a name="containers"></a><span data-ttu-id="c157a-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="c157a-107">Containers</span></span>

<span data-ttu-id="c157a-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c157a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="c157a-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c157a-109">Read-Only</span></span>

<span data-ttu-id="c157a-110">Oui</span><span class="sxs-lookup"><span data-stu-id="c157a-110">Yes</span></span>

### <a name="input-type"></a><span data-ttu-id="c157a-111">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="c157a-111">Input Type</span></span>

<span data-ttu-id="c157a-112">Double</span><span class="sxs-lookup"><span data-stu-id="c157a-112">Double</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="c157a-113">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="c157a-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="c157a-114">Cette valeur est générée à partir de System. photo. ApertureNumerator et de System. photo. ApertureDenominator.</span><span class="sxs-lookup"><span data-stu-id="c157a-114">This value is generated from System.Photo.ApertureNumerator and System.Photo.ApertureDenominator.</span></span> <span data-ttu-id="c157a-115">Il ne peut pas être écrit directement.</span><span class="sxs-lookup"><span data-stu-id="c157a-115">It cannot be written directly.</span></span> <span data-ttu-id="c157a-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="c157a-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="c157a-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="c157a-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="c157a-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="c157a-118">Read Paths</span></span>



| <span data-ttu-id="c157a-119">Commande</span><span class="sxs-lookup"><span data-stu-id="c157a-119">Order</span></span> | <span data-ttu-id="c157a-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c157a-120">Path</span></span>                          | <span data-ttu-id="c157a-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="c157a-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="c157a-122">1</span><span class="sxs-lookup"><span data-stu-id="c157a-122">1</span></span>     | <span data-ttu-id="c157a-123">/App1/IFD/EXIF/{UShort = 37379}</span><span class="sxs-lookup"><span data-stu-id="c157a-123">/app1/ifd/exif/{ushort=37379}</span></span> |             |
| <span data-ttu-id="c157a-124">2</span><span class="sxs-lookup"><span data-stu-id="c157a-124">2</span></span>     | <span data-ttu-id="c157a-125">/xmp/exif:BrightnessValue</span><span class="sxs-lookup"><span data-stu-id="c157a-125">/xmp/exif:BrightnessValue</span></span>     |             |



 

### <a name="write-paths"></a><span data-ttu-id="c157a-126">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="c157a-126">Write Paths</span></span>



| <span data-ttu-id="c157a-127">Commande</span><span class="sxs-lookup"><span data-stu-id="c157a-127">Order</span></span> | <span data-ttu-id="c157a-128">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c157a-128">Path</span></span>                          | <span data-ttu-id="c157a-129">Format de disque</span><span class="sxs-lookup"><span data-stu-id="c157a-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="c157a-130">1</span><span class="sxs-lookup"><span data-stu-id="c157a-130">1</span></span>     | <span data-ttu-id="c157a-131">/App1/IFD/EXIF/{UShort = 37379}</span><span class="sxs-lookup"><span data-stu-id="c157a-131">/app1/ifd/exif/{ushort=37379}</span></span> |             |
| <span data-ttu-id="c157a-132">2</span><span class="sxs-lookup"><span data-stu-id="c157a-132">2</span></span>     | <span data-ttu-id="c157a-133">/xmp/exif:BrightnessValue</span><span class="sxs-lookup"><span data-stu-id="c157a-133">/xmp/exif:BrightnessValue</span></span>     |             |



 

### <a name="remove-paths"></a><span data-ttu-id="c157a-134">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="c157a-134">Remove Paths</span></span>



| <span data-ttu-id="c157a-135">Commande</span><span class="sxs-lookup"><span data-stu-id="c157a-135">Order</span></span> | <span data-ttu-id="c157a-136">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c157a-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="c157a-137">1</span><span class="sxs-lookup"><span data-stu-id="c157a-137">1</span></span>     | <span data-ttu-id="c157a-138">/App1/IFD/EXIF/{UShort = 37379}</span><span class="sxs-lookup"><span data-stu-id="c157a-138">/app1/ifd/exif/{ushort=37379}</span></span> |
| <span data-ttu-id="c157a-139">2</span><span class="sxs-lookup"><span data-stu-id="c157a-139">2</span></span>     | <span data-ttu-id="c157a-140">/xmp/exif:brightnessvalue</span><span class="sxs-lookup"><span data-stu-id="c157a-140">/xmp/exif:brightnessvalue</span></span>     |



 

### <a name="tiff-policies"></a><span data-ttu-id="c157a-141">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="c157a-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="c157a-142">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="c157a-142">Read Paths</span></span>



| <span data-ttu-id="c157a-143">Commande</span><span class="sxs-lookup"><span data-stu-id="c157a-143">Order</span></span> | <span data-ttu-id="c157a-144">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c157a-144">Path</span></span>                          | <span data-ttu-id="c157a-145">Format de disque</span><span class="sxs-lookup"><span data-stu-id="c157a-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="c157a-146">1</span><span class="sxs-lookup"><span data-stu-id="c157a-146">1</span></span>     | <span data-ttu-id="c157a-147">/IFD/EXIF/{UShort = 37379}</span><span class="sxs-lookup"><span data-stu-id="c157a-147">/ifd/exif/{ushort=37379}</span></span>      |             |
| <span data-ttu-id="c157a-148">2</span><span class="sxs-lookup"><span data-stu-id="c157a-148">2</span></span>     | <span data-ttu-id="c157a-149">/ifd/xmp/exif:BrightnessValue</span><span class="sxs-lookup"><span data-stu-id="c157a-149">/ifd/xmp/exif:BrightnessValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="c157a-150">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="c157a-150">Write Paths</span></span>



| <span data-ttu-id="c157a-151">Commande</span><span class="sxs-lookup"><span data-stu-id="c157a-151">Order</span></span> | <span data-ttu-id="c157a-152">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c157a-152">Path</span></span>                          | <span data-ttu-id="c157a-153">Format de disque</span><span class="sxs-lookup"><span data-stu-id="c157a-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="c157a-154">1</span><span class="sxs-lookup"><span data-stu-id="c157a-154">1</span></span>     | <span data-ttu-id="c157a-155">/IFD/EXIF/{UShort = 37379}</span><span class="sxs-lookup"><span data-stu-id="c157a-155">/ifd/exif/{ushort=37379}</span></span>      |             |
| <span data-ttu-id="c157a-156">2</span><span class="sxs-lookup"><span data-stu-id="c157a-156">2</span></span>     | <span data-ttu-id="c157a-157">/ifd/xmp/exif:BrightnessValue</span><span class="sxs-lookup"><span data-stu-id="c157a-157">/ifd/xmp/exif:BrightnessValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="c157a-158">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="c157a-158">Remove Paths</span></span>



| <span data-ttu-id="c157a-159">Commande</span><span class="sxs-lookup"><span data-stu-id="c157a-159">Order</span></span> | <span data-ttu-id="c157a-160">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c157a-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="c157a-161">1</span><span class="sxs-lookup"><span data-stu-id="c157a-161">1</span></span>     | <span data-ttu-id="c157a-162">/IFD/EXIF/{UShort = 37379}</span><span class="sxs-lookup"><span data-stu-id="c157a-162">/ifd/exif/{ushort=37379}</span></span>      |
| <span data-ttu-id="c157a-163">2</span><span class="sxs-lookup"><span data-stu-id="c157a-163">2</span></span>     | <span data-ttu-id="c157a-164">/ifd/xmp/exif:brightnessvalue</span><span class="sxs-lookup"><span data-stu-id="c157a-164">/ifd/xmp/exif:brightnessvalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c157a-165">Notes</span><span class="sxs-lookup"><span data-stu-id="c157a-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="c157a-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c157a-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c157a-167">System. photo. Brightness</span><span class="sxs-lookup"><span data-stu-id="c157a-167">System.Photo.Brightness</span></span>](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
