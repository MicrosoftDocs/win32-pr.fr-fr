---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. orifice.
ms.assetid: 3048eb9d-4ed4-4b5b-960e-9d0fd6704041
title: Stratégie de métadonnées de photo System. photo. orifice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc02826b0602d0052f129640901ac3564a0eadb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524425"
---
# <a name="systemphotoaperture-photo-metadata-policy"></a><span data-ttu-id="1a4e7-103">Stratégie de métadonnées de photo System. photo. orifice</span><span class="sxs-lookup"><span data-stu-id="1a4e7-103">System.Photo.Aperture Photo Metadata Policy</span></span>

<span data-ttu-id="1a4e7-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. orifice](../properties/props-system-photo-aperture.md) .</span><span class="sxs-lookup"><span data-stu-id="1a4e7-104">The photo metadata policy for the [System.Photo.Aperture](../properties/props-system-photo-aperture.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="1a4e7-105">A-la</span><span class="sxs-lookup"><span data-stu-id="1a4e7-105">PKEY</span></span>

<span data-ttu-id="1a4e7-106">Ouverture de photo de l' \_ hypergraphique \_</span><span class="sxs-lookup"><span data-stu-id="1a4e7-106">PKEY\_Photo\_Aperture</span></span>

### <a name="containers"></a><span data-ttu-id="1a4e7-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="1a4e7-107">Containers</span></span>

<span data-ttu-id="1a4e7-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="1a4e7-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="1a4e7-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1a4e7-109">Read-Only</span></span>

<span data-ttu-id="1a4e7-110">Oui</span><span class="sxs-lookup"><span data-stu-id="1a4e7-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="1a4e7-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="1a4e7-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="1a4e7-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="1a4e7-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="1a4e7-113">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="1a4e7-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="1a4e7-114">Cette valeur est générée à partir de System. photo. ApertureNumerator et de System. photo. ApertureDenominator.</span><span class="sxs-lookup"><span data-stu-id="1a4e7-114">This value is generated from System.Photo.ApertureNumerator and System.Photo.ApertureDenominator.</span></span> <span data-ttu-id="1a4e7-115">Il ne peut pas être écrit directement.</span><span class="sxs-lookup"><span data-stu-id="1a4e7-115">It cannot be written directly.</span></span> <span data-ttu-id="1a4e7-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="1a4e7-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="1a4e7-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="1a4e7-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="1a4e7-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="1a4e7-118">Read Paths</span></span>



| <span data-ttu-id="1a4e7-119">Commande</span><span class="sxs-lookup"><span data-stu-id="1a4e7-119">Order</span></span> | <span data-ttu-id="1a4e7-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1a4e7-120">Path</span></span>                          | <span data-ttu-id="1a4e7-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="1a4e7-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="1a4e7-122">1</span><span class="sxs-lookup"><span data-stu-id="1a4e7-122">1</span></span>     | <span data-ttu-id="1a4e7-123">/App1/IFD/EXIF/{UShort = 37378}</span><span class="sxs-lookup"><span data-stu-id="1a4e7-123">/app1/ifd/exif/{ushort=37378}</span></span> |             |
| <span data-ttu-id="1a4e7-124">2</span><span class="sxs-lookup"><span data-stu-id="1a4e7-124">2</span></span>     | <span data-ttu-id="1a4e7-125">/xmp/exif:ApertureValue</span><span class="sxs-lookup"><span data-stu-id="1a4e7-125">/xmp/exif:ApertureValue</span></span>       |             |



 

### <a name="write-paths"></a><span data-ttu-id="1a4e7-126">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="1a4e7-126">Write Paths</span></span>



| <span data-ttu-id="1a4e7-127">Commande</span><span class="sxs-lookup"><span data-stu-id="1a4e7-127">Order</span></span> | <span data-ttu-id="1a4e7-128">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1a4e7-128">Path</span></span>                          | <span data-ttu-id="1a4e7-129">Format de disque</span><span class="sxs-lookup"><span data-stu-id="1a4e7-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="1a4e7-130">1</span><span class="sxs-lookup"><span data-stu-id="1a4e7-130">1</span></span>     | <span data-ttu-id="1a4e7-131">/App1/IFD/EXIF/{UShort = 37378}</span><span class="sxs-lookup"><span data-stu-id="1a4e7-131">/app1/ifd/exif/{ushort=37378}</span></span> |             |
| <span data-ttu-id="1a4e7-132">2</span><span class="sxs-lookup"><span data-stu-id="1a4e7-132">2</span></span>     | <span data-ttu-id="1a4e7-133">/xmp/exif:ApertureValue</span><span class="sxs-lookup"><span data-stu-id="1a4e7-133">/xmp/exif:ApertureValue</span></span>       |             |



 

### <a name="remove-paths"></a><span data-ttu-id="1a4e7-134">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="1a4e7-134">Remove Paths</span></span>



| <span data-ttu-id="1a4e7-135">Commande</span><span class="sxs-lookup"><span data-stu-id="1a4e7-135">Order</span></span> | <span data-ttu-id="1a4e7-136">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1a4e7-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="1a4e7-137">1</span><span class="sxs-lookup"><span data-stu-id="1a4e7-137">1</span></span>     | <span data-ttu-id="1a4e7-138">/App1/IFD/EXIF/{UShort = 37378}</span><span class="sxs-lookup"><span data-stu-id="1a4e7-138">/app1/ifd/exif/{ushort=37378}</span></span> |
| <span data-ttu-id="1a4e7-139">2</span><span class="sxs-lookup"><span data-stu-id="1a4e7-139">2</span></span>     | <span data-ttu-id="1a4e7-140">/xmp/exif:aperturevalue</span><span class="sxs-lookup"><span data-stu-id="1a4e7-140">/xmp/exif:aperturevalue</span></span>       |



 

### <a name="tiff-policies"></a><span data-ttu-id="1a4e7-141">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="1a4e7-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="1a4e7-142">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="1a4e7-142">Read Paths</span></span>



| <span data-ttu-id="1a4e7-143">Commande</span><span class="sxs-lookup"><span data-stu-id="1a4e7-143">Order</span></span> | <span data-ttu-id="1a4e7-144">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1a4e7-144">Path</span></span>                        | <span data-ttu-id="1a4e7-145">Format de disque</span><span class="sxs-lookup"><span data-stu-id="1a4e7-145">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="1a4e7-146">1</span><span class="sxs-lookup"><span data-stu-id="1a4e7-146">1</span></span>     | <span data-ttu-id="1a4e7-147">/IFD/EXIF/{UShort = 37378}</span><span class="sxs-lookup"><span data-stu-id="1a4e7-147">/ifd/exif/{ushort=37378}</span></span>    |             |
| <span data-ttu-id="1a4e7-148">2</span><span class="sxs-lookup"><span data-stu-id="1a4e7-148">2</span></span>     | <span data-ttu-id="1a4e7-149">/ifd/xmp/exif:ApertureValue</span><span class="sxs-lookup"><span data-stu-id="1a4e7-149">/ifd/xmp/exif:ApertureValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="1a4e7-150">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="1a4e7-150">Write Paths</span></span>



| <span data-ttu-id="1a4e7-151">Commande</span><span class="sxs-lookup"><span data-stu-id="1a4e7-151">Order</span></span> | <span data-ttu-id="1a4e7-152">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1a4e7-152">Path</span></span>                        | <span data-ttu-id="1a4e7-153">Format de disque</span><span class="sxs-lookup"><span data-stu-id="1a4e7-153">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="1a4e7-154">1</span><span class="sxs-lookup"><span data-stu-id="1a4e7-154">1</span></span>     | <span data-ttu-id="1a4e7-155">/IFD/EXIF/{UShort = 37378}</span><span class="sxs-lookup"><span data-stu-id="1a4e7-155">/ifd/exif/{ushort=37378}</span></span>    |             |
| <span data-ttu-id="1a4e7-156">2</span><span class="sxs-lookup"><span data-stu-id="1a4e7-156">2</span></span>     | <span data-ttu-id="1a4e7-157">/ifd/xmp/exif:ApertureValue</span><span class="sxs-lookup"><span data-stu-id="1a4e7-157">/ifd/xmp/exif:ApertureValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="1a4e7-158">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="1a4e7-158">Remove Paths</span></span>



| <span data-ttu-id="1a4e7-159">Commande</span><span class="sxs-lookup"><span data-stu-id="1a4e7-159">Order</span></span> | <span data-ttu-id="1a4e7-160">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1a4e7-160">Path</span></span>                        |
|-------|-----------------------------|
| <span data-ttu-id="1a4e7-161">1</span><span class="sxs-lookup"><span data-stu-id="1a4e7-161">1</span></span>     | <span data-ttu-id="1a4e7-162">/IFD/EXIF/{UShort = 37378}</span><span class="sxs-lookup"><span data-stu-id="1a4e7-162">/ifd/exif/{ushort=37378}</span></span>    |
| <span data-ttu-id="1a4e7-163">2</span><span class="sxs-lookup"><span data-stu-id="1a4e7-163">2</span></span>     | <span data-ttu-id="1a4e7-164">/ifd/xmp/exif:aperturevalue</span><span class="sxs-lookup"><span data-stu-id="1a4e7-164">/ifd/xmp/exif:aperturevalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1a4e7-165">Notes</span><span class="sxs-lookup"><span data-stu-id="1a4e7-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a4e7-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1a4e7-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a4e7-167">System. photo. ouverture</span><span class="sxs-lookup"><span data-stu-id="1a4e7-167">System.Photo.Aperture</span></span>](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
