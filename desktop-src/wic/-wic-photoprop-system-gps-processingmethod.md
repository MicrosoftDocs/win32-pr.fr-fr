---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. ProcessingMethod.
ms.assetid: 840021a8-ec1d-4916-93b2-7cc1803e2d8c
title: Stratégie de métadonnées de photo System. GPS. ProcessingMethod
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02bf1484eb8e8a53c65a9cd43c54b076e418d4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532301"
---
# <a name="systemgpsprocessingmethod-photo-metadata-policy"></a><span data-ttu-id="1ab6a-103">Stratégie de métadonnées de photo System. GPS. ProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="1ab6a-103">System.GPS.ProcessingMethod Photo Metadata Policy</span></span>

<span data-ttu-id="1ab6a-104">Stratégie de métadonnées de la photo pour la propriété [System. GPS. ProcessingMethod](../properties/props-system-gps-processingmethod.md) .</span><span class="sxs-lookup"><span data-stu-id="1ab6a-104">The photo metadata policy for the [System.GPS.ProcessingMethod](../properties/props-system-gps-processingmethod.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="1ab6a-105">A-la</span><span class="sxs-lookup"><span data-stu-id="1ab6a-105">PKEY</span></span>

<span data-ttu-id="1ab6a-106">\_ProcessingMethod GPS \_</span><span class="sxs-lookup"><span data-stu-id="1ab6a-106">PKEY\_GPS\_ProcessingMethod</span></span>

### <a name="containers"></a><span data-ttu-id="1ab6a-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="1ab6a-107">Containers</span></span>

<span data-ttu-id="1ab6a-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="1ab6a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="1ab6a-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ab6a-109">Read-Only</span></span>

<span data-ttu-id="1ab6a-110">Non</span><span class="sxs-lookup"><span data-stu-id="1ab6a-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="1ab6a-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="1ab6a-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="1ab6a-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="1ab6a-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="1ab6a-113">Type de PROPVARIANT d’entrée</span><span class="sxs-lookup"><span data-stu-id="1ab6a-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="1ab6a-114">VT \_ LPWStr est préféré, mais VT \_ LPSTR est également accepté.</span><span class="sxs-lookup"><span data-stu-id="1ab6a-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="1ab6a-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="1ab6a-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="1ab6a-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="1ab6a-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="1ab6a-117">Stratégies JPEG</span><span class="sxs-lookup"><span data-stu-id="1ab6a-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="1ab6a-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="1ab6a-118">Read Paths</span></span>



| <span data-ttu-id="1ab6a-119">Commande</span><span class="sxs-lookup"><span data-stu-id="1ab6a-119">Order</span></span> | <span data-ttu-id="1ab6a-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1ab6a-120">Path</span></span>                          | <span data-ttu-id="1ab6a-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="1ab6a-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="1ab6a-122">1</span><span class="sxs-lookup"><span data-stu-id="1ab6a-122">1</span></span>     | <span data-ttu-id="1ab6a-123">/App1/IFD/GPS/{UShort = 27}</span><span class="sxs-lookup"><span data-stu-id="1ab6a-123">/app1/ifd/gps/{ushort=27}</span></span>     |             |
| <span data-ttu-id="1ab6a-124">2</span><span class="sxs-lookup"><span data-stu-id="1ab6a-124">2</span></span>     | <span data-ttu-id="1ab6a-125">/xmp/exif:GPSProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="1ab6a-125">/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="1ab6a-126">unicode</span><span class="sxs-lookup"><span data-stu-id="1ab6a-126">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="1ab6a-127">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="1ab6a-127">Write Paths</span></span>



| <span data-ttu-id="1ab6a-128">Commande</span><span class="sxs-lookup"><span data-stu-id="1ab6a-128">Order</span></span> | <span data-ttu-id="1ab6a-129">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1ab6a-129">Path</span></span>                          | <span data-ttu-id="1ab6a-130">Format de disque</span><span class="sxs-lookup"><span data-stu-id="1ab6a-130">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="1ab6a-131">1</span><span class="sxs-lookup"><span data-stu-id="1ab6a-131">1</span></span>     | <span data-ttu-id="1ab6a-132">/App1/IFD/GPS/{UShort = 27}</span><span class="sxs-lookup"><span data-stu-id="1ab6a-132">/app1/ifd/gps/{ushort=27}</span></span>     |             |
| <span data-ttu-id="1ab6a-133">2</span><span class="sxs-lookup"><span data-stu-id="1ab6a-133">2</span></span>     | <span data-ttu-id="1ab6a-134">/xmp/exif:GPSProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="1ab6a-134">/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="1ab6a-135">unicode</span><span class="sxs-lookup"><span data-stu-id="1ab6a-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="1ab6a-136">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="1ab6a-136">Remove Paths</span></span>



| <span data-ttu-id="1ab6a-137">Commande</span><span class="sxs-lookup"><span data-stu-id="1ab6a-137">Order</span></span> | <span data-ttu-id="1ab6a-138">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1ab6a-138">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="1ab6a-139">1</span><span class="sxs-lookup"><span data-stu-id="1ab6a-139">1</span></span>     | <span data-ttu-id="1ab6a-140">/App1/IFD/GPS/{UShort = 27}</span><span class="sxs-lookup"><span data-stu-id="1ab6a-140">/app1/ifd/gps/{ushort=27}</span></span>     |
| <span data-ttu-id="1ab6a-141">2</span><span class="sxs-lookup"><span data-stu-id="1ab6a-141">2</span></span>     | <span data-ttu-id="1ab6a-142">/xmp/exif:gpsprocessingmethod</span><span class="sxs-lookup"><span data-stu-id="1ab6a-142">/xmp/exif:gpsprocessingmethod</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="1ab6a-143">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="1ab6a-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="1ab6a-144">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="1ab6a-144">Read Paths</span></span>



| <span data-ttu-id="1ab6a-145">Commande</span><span class="sxs-lookup"><span data-stu-id="1ab6a-145">Order</span></span> | <span data-ttu-id="1ab6a-146">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1ab6a-146">Path</span></span>                              | <span data-ttu-id="1ab6a-147">Format de disque</span><span class="sxs-lookup"><span data-stu-id="1ab6a-147">Disk Format</span></span> |
|-------|-----------------------------------|-------------|
| <span data-ttu-id="1ab6a-148">1</span><span class="sxs-lookup"><span data-stu-id="1ab6a-148">1</span></span>     | <span data-ttu-id="1ab6a-149">/ifd/xmp/exif:GPSProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="1ab6a-149">/ifd/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="1ab6a-150">unicode</span><span class="sxs-lookup"><span data-stu-id="1ab6a-150">unicode</span></span>     |
| <span data-ttu-id="1ab6a-151">2</span><span class="sxs-lookup"><span data-stu-id="1ab6a-151">2</span></span>     | <span data-ttu-id="1ab6a-152">/IFD/GPS/{UShort = 27}</span><span class="sxs-lookup"><span data-stu-id="1ab6a-152">/ifd/gps/{ushort=27}</span></span>              |             |



 

### <a name="write-paths"></a><span data-ttu-id="1ab6a-153">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="1ab6a-153">Write Paths</span></span>



| <span data-ttu-id="1ab6a-154">Commande</span><span class="sxs-lookup"><span data-stu-id="1ab6a-154">Order</span></span> | <span data-ttu-id="1ab6a-155">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1ab6a-155">Path</span></span>                              | <span data-ttu-id="1ab6a-156">Format de disque</span><span class="sxs-lookup"><span data-stu-id="1ab6a-156">Disk Format</span></span> |
|-------|-----------------------------------|-------------|
| <span data-ttu-id="1ab6a-157">1</span><span class="sxs-lookup"><span data-stu-id="1ab6a-157">1</span></span>     | <span data-ttu-id="1ab6a-158">/ifd/xmp/exif:GPSProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="1ab6a-158">/ifd/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="1ab6a-159">unicode</span><span class="sxs-lookup"><span data-stu-id="1ab6a-159">unicode</span></span>     |
| <span data-ttu-id="1ab6a-160">2</span><span class="sxs-lookup"><span data-stu-id="1ab6a-160">2</span></span>     | <span data-ttu-id="1ab6a-161">/IFD/GPS/{UShort = 27}</span><span class="sxs-lookup"><span data-stu-id="1ab6a-161">/ifd/gps/{ushort=27}</span></span>              |             |



 

### <a name="remove-paths"></a><span data-ttu-id="1ab6a-162">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="1ab6a-162">Remove Paths</span></span>



| <span data-ttu-id="1ab6a-163">Commande</span><span class="sxs-lookup"><span data-stu-id="1ab6a-163">Order</span></span> | <span data-ttu-id="1ab6a-164">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1ab6a-164">Path</span></span>                              |
|-------|-----------------------------------|
| <span data-ttu-id="1ab6a-165">1</span><span class="sxs-lookup"><span data-stu-id="1ab6a-165">1</span></span>     | <span data-ttu-id="1ab6a-166">/ifd/xmp/exif:gpsprocessingmethod</span><span class="sxs-lookup"><span data-stu-id="1ab6a-166">/ifd/xmp/exif:gpsprocessingmethod</span></span> |
| <span data-ttu-id="1ab6a-167">2</span><span class="sxs-lookup"><span data-stu-id="1ab6a-167">2</span></span>     | <span data-ttu-id="1ab6a-168">/IFD/GPS/{UShort = 27}</span><span class="sxs-lookup"><span data-stu-id="1ab6a-168">/ifd/gps/{ushort=27}</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="1ab6a-169">Notes</span><span class="sxs-lookup"><span data-stu-id="1ab6a-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ab6a-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1ab6a-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ab6a-171">System. GPS. ProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="1ab6a-171">System.GPS.ProcessingMethod</span></span>](../properties/props-system-gps-processingmethod.md)
</dt> </dl>

 

 
