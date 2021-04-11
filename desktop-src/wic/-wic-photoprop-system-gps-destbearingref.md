---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. DestBearingRef.
ms.assetid: d1c8b3cc-ed52-43ca-a0ba-045a2c5fe274
title: Stratégie de métadonnées de photo System. GPS. DestBearingRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f00d3083459fe365fc54e81dc485ddd26887a46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203652"
---
# <a name="systemgpsdestbearingref-photo-metadata-policy"></a><span data-ttu-id="e0863-103">Stratégie de métadonnées de photo System. GPS. DestBearingRef</span><span class="sxs-lookup"><span data-stu-id="e0863-103">System.GPS.DestBearingRef Photo Metadata Policy</span></span>

<span data-ttu-id="e0863-104">Stratégie de métadonnées de la photo pour la propriété [System. GPS. DestBearingRef](../properties/props-system-gps-destbearingref.md) .</span><span class="sxs-lookup"><span data-stu-id="e0863-104">The photo metadata policy for the [System.GPS.DestBearingRef](../properties/props-system-gps-destbearingref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="e0863-105">A-la</span><span class="sxs-lookup"><span data-stu-id="e0863-105">PKEY</span></span>

<span data-ttu-id="e0863-106">\_DestBearingRef GPS \_</span><span class="sxs-lookup"><span data-stu-id="e0863-106">PKEY\_GPS\_DestBearingRef</span></span>

### <a name="containers"></a><span data-ttu-id="e0863-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="e0863-107">Containers</span></span>

<span data-ttu-id="e0863-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="e0863-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="e0863-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e0863-109">Read-Only</span></span>

<span data-ttu-id="e0863-110">Non</span><span class="sxs-lookup"><span data-stu-id="e0863-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="e0863-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="e0863-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="e0863-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="e0863-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="e0863-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="e0863-113">Input Type</span></span>

<span data-ttu-id="e0863-114">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="e0863-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="e0863-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="e0863-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="e0863-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="e0863-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="e0863-117">Stratégies JPEG</span><span class="sxs-lookup"><span data-stu-id="e0863-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="e0863-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="e0863-118">Read Paths</span></span>



| <span data-ttu-id="e0863-119">Commande</span><span class="sxs-lookup"><span data-stu-id="e0863-119">Order</span></span> | <span data-ttu-id="e0863-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="e0863-120">Path</span></span>                        | <span data-ttu-id="e0863-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="e0863-121">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="e0863-122">1</span><span class="sxs-lookup"><span data-stu-id="e0863-122">1</span></span>     | <span data-ttu-id="e0863-123">/App1/IFD/GPS/{UShort = 23}</span><span class="sxs-lookup"><span data-stu-id="e0863-123">/app1/ifd/gps/{ushort=23}</span></span>   | <span data-ttu-id="e0863-124">ascii</span><span class="sxs-lookup"><span data-stu-id="e0863-124">ascii</span></span>       |
| <span data-ttu-id="e0863-125">2</span><span class="sxs-lookup"><span data-stu-id="e0863-125">2</span></span>     | <span data-ttu-id="e0863-126">/xmp/exif:GPSDestBearingRef</span><span class="sxs-lookup"><span data-stu-id="e0863-126">/xmp/exif:GPSDestBearingRef</span></span> | <span data-ttu-id="e0863-127">unicode</span><span class="sxs-lookup"><span data-stu-id="e0863-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="e0863-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="e0863-128">Write Paths</span></span>



| <span data-ttu-id="e0863-129">Commande</span><span class="sxs-lookup"><span data-stu-id="e0863-129">Order</span></span> | <span data-ttu-id="e0863-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="e0863-130">Path</span></span>                        | <span data-ttu-id="e0863-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="e0863-131">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="e0863-132">1</span><span class="sxs-lookup"><span data-stu-id="e0863-132">1</span></span>     | <span data-ttu-id="e0863-133">/App1/IFD/GPS/{UShort = 23}</span><span class="sxs-lookup"><span data-stu-id="e0863-133">/app1/ifd/gps/{ushort=23}</span></span>   | <span data-ttu-id="e0863-134">ascii</span><span class="sxs-lookup"><span data-stu-id="e0863-134">ascii</span></span>       |
| <span data-ttu-id="e0863-135">2</span><span class="sxs-lookup"><span data-stu-id="e0863-135">2</span></span>     | <span data-ttu-id="e0863-136">/xmp/exif:GPSDestBearingRef</span><span class="sxs-lookup"><span data-stu-id="e0863-136">/xmp/exif:GPSDestBearingRef</span></span> | <span data-ttu-id="e0863-137">unicode</span><span class="sxs-lookup"><span data-stu-id="e0863-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="e0863-138">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="e0863-138">Remove Paths</span></span>



| <span data-ttu-id="e0863-139">Commande</span><span class="sxs-lookup"><span data-stu-id="e0863-139">Order</span></span> | <span data-ttu-id="e0863-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="e0863-140">Path</span></span>                        |
|-------|-----------------------------|
| <span data-ttu-id="e0863-141">1</span><span class="sxs-lookup"><span data-stu-id="e0863-141">1</span></span>     | <span data-ttu-id="e0863-142">/App1/IFD/GPS/{UShort = 23}</span><span class="sxs-lookup"><span data-stu-id="e0863-142">/app1/ifd/gps/{ushort=23}</span></span>   |
| <span data-ttu-id="e0863-143">2</span><span class="sxs-lookup"><span data-stu-id="e0863-143">2</span></span>     | <span data-ttu-id="e0863-144">/xmp/exif:gpsdestbearingref</span><span class="sxs-lookup"><span data-stu-id="e0863-144">/xmp/exif:gpsdestbearingref</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="e0863-145">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="e0863-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="e0863-146">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="e0863-146">Read Paths</span></span>



| <span data-ttu-id="e0863-147">Commande</span><span class="sxs-lookup"><span data-stu-id="e0863-147">Order</span></span> | <span data-ttu-id="e0863-148">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="e0863-148">Path</span></span>                            | <span data-ttu-id="e0863-149">Format de disque</span><span class="sxs-lookup"><span data-stu-id="e0863-149">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="e0863-150">1</span><span class="sxs-lookup"><span data-stu-id="e0863-150">1</span></span>     | <span data-ttu-id="e0863-151">/IFD/GPS/{UShort = 23}</span><span class="sxs-lookup"><span data-stu-id="e0863-151">/ifd/gps/{ushort=23}</span></span>            | <span data-ttu-id="e0863-152">ascii</span><span class="sxs-lookup"><span data-stu-id="e0863-152">ascii</span></span>       |
| <span data-ttu-id="e0863-153">2</span><span class="sxs-lookup"><span data-stu-id="e0863-153">2</span></span>     | <span data-ttu-id="e0863-154">/ifd/xmp/exif:GPSDestBearingRef</span><span class="sxs-lookup"><span data-stu-id="e0863-154">/ifd/xmp/exif:GPSDestBearingRef</span></span> | <span data-ttu-id="e0863-155">unicode</span><span class="sxs-lookup"><span data-stu-id="e0863-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="e0863-156">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="e0863-156">Write Paths</span></span>



| <span data-ttu-id="e0863-157">Commande</span><span class="sxs-lookup"><span data-stu-id="e0863-157">Order</span></span> | <span data-ttu-id="e0863-158">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="e0863-158">Path</span></span>                            | <span data-ttu-id="e0863-159">Format de disque</span><span class="sxs-lookup"><span data-stu-id="e0863-159">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="e0863-160">1</span><span class="sxs-lookup"><span data-stu-id="e0863-160">1</span></span>     | <span data-ttu-id="e0863-161">/IFD/GPS/{UShort = 23}</span><span class="sxs-lookup"><span data-stu-id="e0863-161">/ifd/gps/{ushort=23}</span></span>            | <span data-ttu-id="e0863-162">ascii</span><span class="sxs-lookup"><span data-stu-id="e0863-162">ascii</span></span>       |
| <span data-ttu-id="e0863-163">2</span><span class="sxs-lookup"><span data-stu-id="e0863-163">2</span></span>     | <span data-ttu-id="e0863-164">/ifd/xmp/exif:GPSDestBearingRef</span><span class="sxs-lookup"><span data-stu-id="e0863-164">/ifd/xmp/exif:GPSDestBearingRef</span></span> | <span data-ttu-id="e0863-165">unicode</span><span class="sxs-lookup"><span data-stu-id="e0863-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="e0863-166">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="e0863-166">Remove Paths</span></span>



| <span data-ttu-id="e0863-167">order</span><span class="sxs-lookup"><span data-stu-id="e0863-167">order</span></span> | <span data-ttu-id="e0863-168">path</span><span class="sxs-lookup"><span data-stu-id="e0863-168">path</span></span>                            |
|-------|---------------------------------|
| <span data-ttu-id="e0863-169">1</span><span class="sxs-lookup"><span data-stu-id="e0863-169">1</span></span>     | <span data-ttu-id="e0863-170">/IFD/GPS/{UShort = 23}</span><span class="sxs-lookup"><span data-stu-id="e0863-170">/ifd/gps/{ushort=23}</span></span>            |
| <span data-ttu-id="e0863-171">2</span><span class="sxs-lookup"><span data-stu-id="e0863-171">2</span></span>     | <span data-ttu-id="e0863-172">/ifd/xmp/exif:gpsdestbearingref</span><span class="sxs-lookup"><span data-stu-id="e0863-172">/ifd/xmp/exif:gpsdestbearingref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e0863-173">Notes</span><span class="sxs-lookup"><span data-stu-id="e0863-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0863-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e0863-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0863-175">System. GPS. DestBearingRef</span><span class="sxs-lookup"><span data-stu-id="e0863-175">System.GPS.DestBearingRef</span></span>](../properties/props-system-gps-destbearingref.md)
</dt> </dl>

 

 
