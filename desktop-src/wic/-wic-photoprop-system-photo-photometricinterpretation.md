---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. PhotometricInterpretation.
ms.assetid: ff36b2c3-8763-4640-a049-b5880fd26929
title: Stratégie de métadonnées de photo System. photo. PhotometricInterpretation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b371ce9257d526f941f3fdb33949e8788a7112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523338"
---
# <a name="systemphotophotometricinterpretation-photo-metadata-policy"></a><span data-ttu-id="51a98-103">Stratégie de métadonnées de photo System. photo. PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="51a98-103">System.Photo.PhotometricInterpretation Photo Metadata Policy</span></span>

<span data-ttu-id="51a98-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. PhotometricInterpretation](../properties/props-system-photo-photometricinterpretation.md) .</span><span class="sxs-lookup"><span data-stu-id="51a98-104">The photo metadata policy for the [System.Photo.PhotometricInterpretation](../properties/props-system-photo-photometricinterpretation.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="51a98-105">A-la</span><span class="sxs-lookup"><span data-stu-id="51a98-105">PKEY</span></span>

<span data-ttu-id="51a98-106">\_Photo \_ PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="51a98-106">PKEY\_Photo\_PhotometricInterpretation</span></span>

### <a name="containers"></a><span data-ttu-id="51a98-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="51a98-107">Containers</span></span>

<span data-ttu-id="51a98-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="51a98-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="51a98-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="51a98-109">Read-Only</span></span>

<span data-ttu-id="51a98-110">Oui</span><span class="sxs-lookup"><span data-stu-id="51a98-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="51a98-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="51a98-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="51a98-112">\_UI2 VT</span><span class="sxs-lookup"><span data-stu-id="51a98-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="51a98-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="51a98-113">Input Type</span></span>

<span data-ttu-id="51a98-114">UShort</span><span class="sxs-lookup"><span data-stu-id="51a98-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="51a98-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="51a98-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="51a98-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="51a98-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="51a98-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="51a98-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="51a98-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="51a98-118">Read Paths</span></span>



| <span data-ttu-id="51a98-119">Commande</span><span class="sxs-lookup"><span data-stu-id="51a98-119">Order</span></span> | <span data-ttu-id="51a98-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="51a98-120">Path</span></span>                                | <span data-ttu-id="51a98-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="51a98-121">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="51a98-122">1</span><span class="sxs-lookup"><span data-stu-id="51a98-122">1</span></span>     | <span data-ttu-id="51a98-123">/App1/IFD/{UShort = 262}</span><span class="sxs-lookup"><span data-stu-id="51a98-123">/app1/ifd/{ushort=262}</span></span>              | <span data-ttu-id="51a98-124">ushort</span><span class="sxs-lookup"><span data-stu-id="51a98-124">ushort</span></span>      |
| <span data-ttu-id="51a98-125">2</span><span class="sxs-lookup"><span data-stu-id="51a98-125">2</span></span>     | <span data-ttu-id="51a98-126">/xmp/tiff:PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="51a98-126">/xmp/tiff:PhotometricInterpretation</span></span> | <span data-ttu-id="51a98-127">unicode</span><span class="sxs-lookup"><span data-stu-id="51a98-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="51a98-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="51a98-128">Write Paths</span></span>



| <span data-ttu-id="51a98-129">Commande</span><span class="sxs-lookup"><span data-stu-id="51a98-129">Order</span></span> | <span data-ttu-id="51a98-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="51a98-130">Path</span></span>                                | <span data-ttu-id="51a98-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="51a98-131">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="51a98-132">1</span><span class="sxs-lookup"><span data-stu-id="51a98-132">1</span></span>     | <span data-ttu-id="51a98-133">/App1/IFD/{UShort = 262}</span><span class="sxs-lookup"><span data-stu-id="51a98-133">/app1/ifd/{ushort=262}</span></span>              | <span data-ttu-id="51a98-134">ushort</span><span class="sxs-lookup"><span data-stu-id="51a98-134">ushort</span></span>      |
| <span data-ttu-id="51a98-135">2</span><span class="sxs-lookup"><span data-stu-id="51a98-135">2</span></span>     | <span data-ttu-id="51a98-136">/xmp/tiff:PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="51a98-136">/xmp/tiff:PhotometricInterpretation</span></span> | <span data-ttu-id="51a98-137">unicode</span><span class="sxs-lookup"><span data-stu-id="51a98-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="51a98-138">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="51a98-138">Remove Paths</span></span>



| <span data-ttu-id="51a98-139">Commande</span><span class="sxs-lookup"><span data-stu-id="51a98-139">Order</span></span> | <span data-ttu-id="51a98-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="51a98-140">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="51a98-141">1</span><span class="sxs-lookup"><span data-stu-id="51a98-141">1</span></span>     | <span data-ttu-id="51a98-142">/App1/IFD/{UShort = 262}</span><span class="sxs-lookup"><span data-stu-id="51a98-142">/app1/ifd/{ushort=262}</span></span>              |
| <span data-ttu-id="51a98-143">2</span><span class="sxs-lookup"><span data-stu-id="51a98-143">2</span></span>     | <span data-ttu-id="51a98-144">/xmp/tiff:photometricinterpretation</span><span class="sxs-lookup"><span data-stu-id="51a98-144">/xmp/tiff:photometricinterpretation</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="51a98-145">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="51a98-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="51a98-146">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="51a98-146">Read Paths</span></span>



| <span data-ttu-id="51a98-147">Commande</span><span class="sxs-lookup"><span data-stu-id="51a98-147">Order</span></span> | <span data-ttu-id="51a98-148">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="51a98-148">Path</span></span>                                    | <span data-ttu-id="51a98-149">Format de disque</span><span class="sxs-lookup"><span data-stu-id="51a98-149">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="51a98-150">1</span><span class="sxs-lookup"><span data-stu-id="51a98-150">1</span></span>     | <span data-ttu-id="51a98-151">/IFD/{UShort = 262}</span><span class="sxs-lookup"><span data-stu-id="51a98-151">/ifd/{ushort=262}</span></span>                       | <span data-ttu-id="51a98-152">ushort</span><span class="sxs-lookup"><span data-stu-id="51a98-152">ushort</span></span>      |
| <span data-ttu-id="51a98-153">2</span><span class="sxs-lookup"><span data-stu-id="51a98-153">2</span></span>     | <span data-ttu-id="51a98-154">/ifd/xmp/tiff:PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="51a98-154">/ifd/xmp/tiff:PhotometricInterpretation</span></span> | <span data-ttu-id="51a98-155">unicode</span><span class="sxs-lookup"><span data-stu-id="51a98-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="51a98-156">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="51a98-156">Write Paths</span></span>



| <span data-ttu-id="51a98-157">Commande</span><span class="sxs-lookup"><span data-stu-id="51a98-157">Order</span></span> | <span data-ttu-id="51a98-158">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="51a98-158">Path</span></span>                                    | <span data-ttu-id="51a98-159">Format de disque</span><span class="sxs-lookup"><span data-stu-id="51a98-159">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="51a98-160">1</span><span class="sxs-lookup"><span data-stu-id="51a98-160">1</span></span>     | <span data-ttu-id="51a98-161">/IFD/{UShort = 262}</span><span class="sxs-lookup"><span data-stu-id="51a98-161">/ifd/{ushort=262}</span></span>                       | <span data-ttu-id="51a98-162">ushort</span><span class="sxs-lookup"><span data-stu-id="51a98-162">ushort</span></span>      |
| <span data-ttu-id="51a98-163">2</span><span class="sxs-lookup"><span data-stu-id="51a98-163">2</span></span>     | <span data-ttu-id="51a98-164">/ifd/xmp/tiff:PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="51a98-164">/ifd/xmp/tiff:PhotometricInterpretation</span></span> | <span data-ttu-id="51a98-165">unicode</span><span class="sxs-lookup"><span data-stu-id="51a98-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="51a98-166">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="51a98-166">Remove Paths</span></span>



| <span data-ttu-id="51a98-167">Commande</span><span class="sxs-lookup"><span data-stu-id="51a98-167">Order</span></span> | <span data-ttu-id="51a98-168">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="51a98-168">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="51a98-169">1</span><span class="sxs-lookup"><span data-stu-id="51a98-169">1</span></span>     | <span data-ttu-id="51a98-170">/IFD/{UShort = 262}</span><span class="sxs-lookup"><span data-stu-id="51a98-170">/ifd/{ushort=262}</span></span>                       |
| <span data-ttu-id="51a98-171">2</span><span class="sxs-lookup"><span data-stu-id="51a98-171">2</span></span>     | <span data-ttu-id="51a98-172">/ifd/xmp/tiff:photometricinterpretation</span><span class="sxs-lookup"><span data-stu-id="51a98-172">/ifd/xmp/tiff:photometricinterpretation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="51a98-173">Notes</span><span class="sxs-lookup"><span data-stu-id="51a98-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="51a98-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="51a98-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51a98-175">System. photo. PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="51a98-175">System.Photo.PhotometricInterpretation</span></span>](../properties/props-system-photo-photometricinterpretation.md)
</dt> </dl>

 

 
