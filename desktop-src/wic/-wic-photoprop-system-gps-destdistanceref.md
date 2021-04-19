---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. DestDistanceRef.
ms.assetid: eb671f34-7366-4182-b72e-0dd7830751e0
title: Stratégie de métadonnées de photo System. GPS. DestDistanceRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bba6e04bee00aaed868fcc02059403fe479f8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529213"
---
# <a name="systemgpsdestdistanceref-photo-metadata-policy"></a><span data-ttu-id="0069a-103">Stratégie de métadonnées de photo System. GPS. DestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="0069a-103">System.GPS.DestDistanceRef Photo Metadata Policy</span></span>

<span data-ttu-id="0069a-104">Stratégie de métadonnées de la photo pour la propriété [System. GPS. DestDistanceRef](../properties/props-system-gps-destdistanceref.md) .</span><span class="sxs-lookup"><span data-stu-id="0069a-104">The photo metadata policy for the [System.GPS.DestDistanceRef](../properties/props-system-gps-destdistanceref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="0069a-105">A-la</span><span class="sxs-lookup"><span data-stu-id="0069a-105">PKEY</span></span>

<span data-ttu-id="0069a-106">DestDistanceRef de la \_</span><span class="sxs-lookup"><span data-stu-id="0069a-106">PKEY\_DestDistanceRef</span></span>

### <a name="containers"></a><span data-ttu-id="0069a-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="0069a-107">Containers</span></span>

<span data-ttu-id="0069a-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="0069a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="0069a-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0069a-109">Read-Only</span></span>

<span data-ttu-id="0069a-110">Non</span><span class="sxs-lookup"><span data-stu-id="0069a-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="0069a-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="0069a-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="0069a-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="0069a-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="0069a-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="0069a-113">Input Type</span></span>

<span data-ttu-id="0069a-114">VT \_ LPWStr ou VT \_ LPSTR sont acceptés.</span><span class="sxs-lookup"><span data-stu-id="0069a-114">VT\_LPWSTR or VT\_LPSTR are accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="0069a-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="0069a-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="0069a-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="0069a-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="0069a-117">Stratégies JPEG</span><span class="sxs-lookup"><span data-stu-id="0069a-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="0069a-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="0069a-118">Read Paths</span></span>



| <span data-ttu-id="0069a-119">Commande</span><span class="sxs-lookup"><span data-stu-id="0069a-119">Order</span></span> | <span data-ttu-id="0069a-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="0069a-120">Path</span></span>                         | <span data-ttu-id="0069a-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="0069a-121">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="0069a-122">1</span><span class="sxs-lookup"><span data-stu-id="0069a-122">1</span></span>     | <span data-ttu-id="0069a-123">/App1/IFD/GPS/{UShort = 25}</span><span class="sxs-lookup"><span data-stu-id="0069a-123">/app1/ifd/gps/{ushort=25}</span></span>    | <span data-ttu-id="0069a-124">ascii</span><span class="sxs-lookup"><span data-stu-id="0069a-124">ascii</span></span>       |
| <span data-ttu-id="0069a-125">2</span><span class="sxs-lookup"><span data-stu-id="0069a-125">2</span></span>     | <span data-ttu-id="0069a-126">/xmp/exif:GPSDestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="0069a-126">/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="0069a-127">unicode</span><span class="sxs-lookup"><span data-stu-id="0069a-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="0069a-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="0069a-128">Write Paths</span></span>



| <span data-ttu-id="0069a-129">Commande</span><span class="sxs-lookup"><span data-stu-id="0069a-129">Order</span></span> | <span data-ttu-id="0069a-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="0069a-130">Path</span></span>                         | <span data-ttu-id="0069a-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="0069a-131">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="0069a-132">1</span><span class="sxs-lookup"><span data-stu-id="0069a-132">1</span></span>     | <span data-ttu-id="0069a-133">/App1/IFD/GPS/{UShort = 25}</span><span class="sxs-lookup"><span data-stu-id="0069a-133">/app1/ifd/gps/{ushort=25}</span></span>    | <span data-ttu-id="0069a-134">ascii</span><span class="sxs-lookup"><span data-stu-id="0069a-134">ascii</span></span>       |
| <span data-ttu-id="0069a-135">2</span><span class="sxs-lookup"><span data-stu-id="0069a-135">2</span></span>     | <span data-ttu-id="0069a-136">/xmp/exif:GPSDestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="0069a-136">/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="0069a-137">unicode</span><span class="sxs-lookup"><span data-stu-id="0069a-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="0069a-138">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="0069a-138">Remove Paths</span></span>



| <span data-ttu-id="0069a-139">Commande</span><span class="sxs-lookup"><span data-stu-id="0069a-139">Order</span></span> | <span data-ttu-id="0069a-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="0069a-140">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="0069a-141">1</span><span class="sxs-lookup"><span data-stu-id="0069a-141">1</span></span>     | <span data-ttu-id="0069a-142">/App1/IFD/GPS/{UShort = 25}</span><span class="sxs-lookup"><span data-stu-id="0069a-142">/app1/ifd/gps/{ushort=25}</span></span>    |
| <span data-ttu-id="0069a-143">2</span><span class="sxs-lookup"><span data-stu-id="0069a-143">2</span></span>     | <span data-ttu-id="0069a-144">/xmp/exif:gpsdestdistanceref</span><span class="sxs-lookup"><span data-stu-id="0069a-144">/xmp/exif:gpsdestdistanceref</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="0069a-145">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="0069a-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="0069a-146">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="0069a-146">Read Paths</span></span>



| <span data-ttu-id="0069a-147">Commande</span><span class="sxs-lookup"><span data-stu-id="0069a-147">Order</span></span> | <span data-ttu-id="0069a-148">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="0069a-148">Path</span></span>                             | <span data-ttu-id="0069a-149">Format de disque</span><span class="sxs-lookup"><span data-stu-id="0069a-149">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="0069a-150">1</span><span class="sxs-lookup"><span data-stu-id="0069a-150">1</span></span>     | <span data-ttu-id="0069a-151">/IFD/GPS/{UShort = 25}</span><span class="sxs-lookup"><span data-stu-id="0069a-151">/ifd/gps/{ushort=25}</span></span>             | <span data-ttu-id="0069a-152">ascii</span><span class="sxs-lookup"><span data-stu-id="0069a-152">ascii</span></span>       |
| <span data-ttu-id="0069a-153">2</span><span class="sxs-lookup"><span data-stu-id="0069a-153">2</span></span>     | <span data-ttu-id="0069a-154">/ifd/xmp/exif:GPSDestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="0069a-154">/ifd/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="0069a-155">unicode</span><span class="sxs-lookup"><span data-stu-id="0069a-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="0069a-156">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="0069a-156">Write Paths</span></span>



| <span data-ttu-id="0069a-157">Commande</span><span class="sxs-lookup"><span data-stu-id="0069a-157">Order</span></span> | <span data-ttu-id="0069a-158">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="0069a-158">Path</span></span>                             | <span data-ttu-id="0069a-159">Format de disque</span><span class="sxs-lookup"><span data-stu-id="0069a-159">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="0069a-160">1</span><span class="sxs-lookup"><span data-stu-id="0069a-160">1</span></span>     | <span data-ttu-id="0069a-161">/IFD/GPS/{UShort = 25}</span><span class="sxs-lookup"><span data-stu-id="0069a-161">/ifd/gps/{ushort=25}</span></span>             | <span data-ttu-id="0069a-162">ascii</span><span class="sxs-lookup"><span data-stu-id="0069a-162">ascii</span></span>       |
| <span data-ttu-id="0069a-163">2</span><span class="sxs-lookup"><span data-stu-id="0069a-163">2</span></span>     | <span data-ttu-id="0069a-164">/ifd/xmp/exif:GPSDestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="0069a-164">/ifd/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="0069a-165">unicode</span><span class="sxs-lookup"><span data-stu-id="0069a-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="0069a-166">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="0069a-166">Remove Paths</span></span>



| <span data-ttu-id="0069a-167">Commande</span><span class="sxs-lookup"><span data-stu-id="0069a-167">Order</span></span> | <span data-ttu-id="0069a-168">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="0069a-168">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="0069a-169">1</span><span class="sxs-lookup"><span data-stu-id="0069a-169">1</span></span>     | <span data-ttu-id="0069a-170">/IFD/GPS/{UShort = 25}</span><span class="sxs-lookup"><span data-stu-id="0069a-170">/ifd/gps/{ushort=25}</span></span>             |
| <span data-ttu-id="0069a-171">2</span><span class="sxs-lookup"><span data-stu-id="0069a-171">2</span></span>     | <span data-ttu-id="0069a-172">/ifd/xmp/exif:gpsdestdistanceref</span><span class="sxs-lookup"><span data-stu-id="0069a-172">/ifd/xmp/exif:gpsdestdistanceref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0069a-173">Notes</span><span class="sxs-lookup"><span data-stu-id="0069a-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="0069a-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0069a-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0069a-175">System. GPS. DestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="0069a-175">System.GPS.DestDistanceRef</span></span>](../properties/props-system-gps-destdistanceref.md)
</dt> </dl>

 

 
