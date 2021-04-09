---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. SubjectDistance.
ms.assetid: 8d5acd7e-7227-4a79-890a-43e6dace3864
title: Stratégie de métadonnées de photo System. photo. SubjectDistance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3335b17f45cce7dc60881dc7ea8d9ffecc711016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867329"
---
# <a name="systemphotosubjectdistance-photo-metadata-policy"></a><span data-ttu-id="1d5a8-103">Stratégie de métadonnées de photo System. photo. SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="1d5a8-103">System.Photo.SubjectDistance Photo Metadata Policy</span></span>

<span data-ttu-id="1d5a8-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. SubjectDistance](../properties/props-system-photo-subjectdistance.md) .</span><span class="sxs-lookup"><span data-stu-id="1d5a8-104">The photo metadata policy for the [System.Photo.SubjectDistance](../properties/props-system-photo-subjectdistance.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="1d5a8-105">A-la</span><span class="sxs-lookup"><span data-stu-id="1d5a8-105">PKEY</span></span>

<span data-ttu-id="1d5a8-106">\_Photo \_ SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="1d5a8-106">PKEY\_Photo\_SubjectDistance</span></span>

### <a name="containers"></a><span data-ttu-id="1d5a8-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="1d5a8-107">Containers</span></span>

<span data-ttu-id="1d5a8-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="1d5a8-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="1d5a8-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d5a8-109">Read-Only</span></span>

<span data-ttu-id="1d5a8-110">Oui</span><span class="sxs-lookup"><span data-stu-id="1d5a8-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="1d5a8-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="1d5a8-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="1d5a8-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="1d5a8-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="1d5a8-113">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="1d5a8-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="1d5a8-114">Cette valeur est générée à partir de System. photo. SubjectDistanceNumerator et de System. photo. SubjectDistanceDenominator.</span><span class="sxs-lookup"><span data-stu-id="1d5a8-114">This value is generated from System.Photo.SubjectDistanceNumerator and System.Photo.SubjectDistanceDenominator.</span></span> <span data-ttu-id="1d5a8-115">Il ne peut pas être écrit directement.</span><span class="sxs-lookup"><span data-stu-id="1d5a8-115">It cannot be written directly.</span></span> <span data-ttu-id="1d5a8-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="1d5a8-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="1d5a8-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="1d5a8-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="1d5a8-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="1d5a8-118">Read Paths</span></span>



| <span data-ttu-id="1d5a8-119">Commande</span><span class="sxs-lookup"><span data-stu-id="1d5a8-119">Order</span></span> | <span data-ttu-id="1d5a8-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1d5a8-120">Path</span></span>                          | <span data-ttu-id="1d5a8-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="1d5a8-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="1d5a8-122">1</span><span class="sxs-lookup"><span data-stu-id="1d5a8-122">1</span></span>     | <span data-ttu-id="1d5a8-123">/App1/IFD/EXIF/{UShort = 37382}</span><span class="sxs-lookup"><span data-stu-id="1d5a8-123">/app1/ifd/exif/{ushort=37382}</span></span> |             |
| <span data-ttu-id="1d5a8-124">2</span><span class="sxs-lookup"><span data-stu-id="1d5a8-124">2</span></span>     | <span data-ttu-id="1d5a8-125">/xmp/exif:SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="1d5a8-125">/xmp/exif:SubjectDistance</span></span>     |             |



 

### <a name="write-paths"></a><span data-ttu-id="1d5a8-126">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="1d5a8-126">Write Paths</span></span>



| <span data-ttu-id="1d5a8-127">Commande</span><span class="sxs-lookup"><span data-stu-id="1d5a8-127">Order</span></span> | <span data-ttu-id="1d5a8-128">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1d5a8-128">Path</span></span>                          | <span data-ttu-id="1d5a8-129">Format de disque</span><span class="sxs-lookup"><span data-stu-id="1d5a8-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="1d5a8-130">1</span><span class="sxs-lookup"><span data-stu-id="1d5a8-130">1</span></span>     | <span data-ttu-id="1d5a8-131">/App1/IFD/EXIF/{UShort = 37382}</span><span class="sxs-lookup"><span data-stu-id="1d5a8-131">/app1/ifd/exif/{ushort=37382}</span></span> |             |
| <span data-ttu-id="1d5a8-132">2</span><span class="sxs-lookup"><span data-stu-id="1d5a8-132">2</span></span>     | <span data-ttu-id="1d5a8-133">/xmp/exif:SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="1d5a8-133">/xmp/exif:SubjectDistance</span></span>     |             |



 

### <a name="remove-paths"></a><span data-ttu-id="1d5a8-134">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="1d5a8-134">Remove Paths</span></span>



| <span data-ttu-id="1d5a8-135">Commande</span><span class="sxs-lookup"><span data-stu-id="1d5a8-135">Order</span></span> | <span data-ttu-id="1d5a8-136">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1d5a8-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="1d5a8-137">1</span><span class="sxs-lookup"><span data-stu-id="1d5a8-137">1</span></span>     | <span data-ttu-id="1d5a8-138">/App1/IFD/EXIF/{UShort = 37382}</span><span class="sxs-lookup"><span data-stu-id="1d5a8-138">/app1/ifd/exif/{ushort=37382}</span></span> |
| <span data-ttu-id="1d5a8-139">2</span><span class="sxs-lookup"><span data-stu-id="1d5a8-139">2</span></span>     | <span data-ttu-id="1d5a8-140">/xmp/exif:subjectdistance</span><span class="sxs-lookup"><span data-stu-id="1d5a8-140">/xmp/exif:subjectdistance</span></span>     |



 

### <a name="tiff-policies"></a><span data-ttu-id="1d5a8-141">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="1d5a8-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="1d5a8-142">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="1d5a8-142">Read Paths</span></span>



| <span data-ttu-id="1d5a8-143">Commande</span><span class="sxs-lookup"><span data-stu-id="1d5a8-143">Order</span></span> | <span data-ttu-id="1d5a8-144">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1d5a8-144">Path</span></span>                          | <span data-ttu-id="1d5a8-145">Format de disque</span><span class="sxs-lookup"><span data-stu-id="1d5a8-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="1d5a8-146">1</span><span class="sxs-lookup"><span data-stu-id="1d5a8-146">1</span></span>     | <span data-ttu-id="1d5a8-147">/IFD/EXIF/{UShort = 37382}</span><span class="sxs-lookup"><span data-stu-id="1d5a8-147">/ifd/exif/{ushort=37382}</span></span>      |             |
| <span data-ttu-id="1d5a8-148">2</span><span class="sxs-lookup"><span data-stu-id="1d5a8-148">2</span></span>     | <span data-ttu-id="1d5a8-149">/ifd/xmp/exif:SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="1d5a8-149">/ifd/xmp/exif:SubjectDistance</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="1d5a8-150">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="1d5a8-150">Write Paths</span></span>



| <span data-ttu-id="1d5a8-151">Commande</span><span class="sxs-lookup"><span data-stu-id="1d5a8-151">Order</span></span> | <span data-ttu-id="1d5a8-152">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1d5a8-152">Path</span></span>                          | <span data-ttu-id="1d5a8-153">Format de disque</span><span class="sxs-lookup"><span data-stu-id="1d5a8-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="1d5a8-154">1</span><span class="sxs-lookup"><span data-stu-id="1d5a8-154">1</span></span>     | <span data-ttu-id="1d5a8-155">/IFD/EXIF/{UShort = 37382}</span><span class="sxs-lookup"><span data-stu-id="1d5a8-155">/ifd/exif/{ushort=37382}</span></span>      |             |
| <span data-ttu-id="1d5a8-156">2</span><span class="sxs-lookup"><span data-stu-id="1d5a8-156">2</span></span>     | <span data-ttu-id="1d5a8-157">/ifd/xmp/exif:SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="1d5a8-157">/ifd/xmp/exif:SubjectDistance</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="1d5a8-158">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="1d5a8-158">Remove Paths</span></span>



| <span data-ttu-id="1d5a8-159">Commande</span><span class="sxs-lookup"><span data-stu-id="1d5a8-159">Order</span></span> | <span data-ttu-id="1d5a8-160">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1d5a8-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="1d5a8-161">1</span><span class="sxs-lookup"><span data-stu-id="1d5a8-161">1</span></span>     | <span data-ttu-id="1d5a8-162">/IFD/EXIF/{UShort = 37382}</span><span class="sxs-lookup"><span data-stu-id="1d5a8-162">/ifd/exif/{ushort=37382}</span></span>      |
| <span data-ttu-id="1d5a8-163">2</span><span class="sxs-lookup"><span data-stu-id="1d5a8-163">2</span></span>     | <span data-ttu-id="1d5a8-164">/ifd/xmp/exif:subjectdistance</span><span class="sxs-lookup"><span data-stu-id="1d5a8-164">/ifd/xmp/exif:subjectdistance</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1d5a8-165">Notes</span><span class="sxs-lookup"><span data-stu-id="1d5a8-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d5a8-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1d5a8-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d5a8-167">System. photo. SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="1d5a8-167">System.Photo.SubjectDistance</span></span>](../properties/props-system-photo-subjectdistance.md)
</dt> </dl>

 

 
