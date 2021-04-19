---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. longitude.
ms.assetid: 36539e20-d00c-4bbb-b9ee-1cf5e4b8df4b
title: Stratégie de métadonnées de photo System. GPS. Longitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25eb9869bc536f97adfc8f3c0f5b1f70c8bf030f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106537067"
---
# <a name="systemgpslongitude-photo-metadata-policy"></a><span data-ttu-id="0c2b5-103">Stratégie de métadonnées de photo System. GPS. Longitude</span><span class="sxs-lookup"><span data-stu-id="0c2b5-103">System.GPS.Longitude Photo Metadata Policy</span></span>

<span data-ttu-id="0c2b5-104">Stratégie de métadonnées de la photo pour la propriété [System. GPS. longitude](../properties/props-system-gps-longitude.md) .</span><span class="sxs-lookup"><span data-stu-id="0c2b5-104">The photo metadata policy for the [System.GPS.Longitude](../properties/props-system-gps-longitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="0c2b5-105">A-la</span><span class="sxs-lookup"><span data-stu-id="0c2b5-105">PKEY</span></span>

<span data-ttu-id="0c2b5-106">\_Longitude GPS \_</span><span class="sxs-lookup"><span data-stu-id="0c2b5-106">PKEY\_GPS\_Longitude</span></span>

### <a name="containers"></a><span data-ttu-id="0c2b5-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="0c2b5-107">Containers</span></span>

<span data-ttu-id="0c2b5-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="0c2b5-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="0c2b5-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0c2b5-109">Read-Only</span></span>

<span data-ttu-id="0c2b5-110">Oui</span><span class="sxs-lookup"><span data-stu-id="0c2b5-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="0c2b5-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="0c2b5-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="0c2b5-112">VT \_ Vector \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="0c2b5-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="0c2b5-113">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="0c2b5-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="0c2b5-114">Cette valeur peut être écrite en écrivant dans System. GPS. LongitudeNumerator et System. GPS. LongitudeDenominator.</span><span class="sxs-lookup"><span data-stu-id="0c2b5-114">This value can be written by writing to System.GPS.LongitudeNumerator and System.GPS.LongitudeDenominator.</span></span> <span data-ttu-id="0c2b5-115">Il ne peut pas être écrit directement.</span><span class="sxs-lookup"><span data-stu-id="0c2b5-115">It cannot be written directly.</span></span> <span data-ttu-id="0c2b5-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="0c2b5-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="0c2b5-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="0c2b5-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="0c2b5-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="0c2b5-118">Read Paths</span></span>



| <span data-ttu-id="0c2b5-119">Commande</span><span class="sxs-lookup"><span data-stu-id="0c2b5-119">Order</span></span> | <span data-ttu-id="0c2b5-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="0c2b5-120">Path</span></span>                     | <span data-ttu-id="0c2b5-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="0c2b5-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="0c2b5-122">1</span><span class="sxs-lookup"><span data-stu-id="0c2b5-122">1</span></span>     | <span data-ttu-id="0c2b5-123">/App1/IFD/GPS/{UShort = 4}</span><span class="sxs-lookup"><span data-stu-id="0c2b5-123">/app1/ifd/gps/{ushort=4}</span></span> |             |
| <span data-ttu-id="0c2b5-124">2</span><span class="sxs-lookup"><span data-stu-id="0c2b5-124">2</span></span>     | <span data-ttu-id="0c2b5-125">/xmp/exif:GPSLongitude</span><span class="sxs-lookup"><span data-stu-id="0c2b5-125">/xmp/exif:GPSLongitude</span></span>   |             |



 

### <a name="write-paths"></a><span data-ttu-id="0c2b5-126">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="0c2b5-126">Write Paths</span></span>



| <span data-ttu-id="0c2b5-127">Commande</span><span class="sxs-lookup"><span data-stu-id="0c2b5-127">Order</span></span> | <span data-ttu-id="0c2b5-128">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="0c2b5-128">Path</span></span>                     | <span data-ttu-id="0c2b5-129">Format de disque</span><span class="sxs-lookup"><span data-stu-id="0c2b5-129">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="0c2b5-130">1</span><span class="sxs-lookup"><span data-stu-id="0c2b5-130">1</span></span>     | <span data-ttu-id="0c2b5-131">/App1/IFD/GPS/{UShort = 4}</span><span class="sxs-lookup"><span data-stu-id="0c2b5-131">/app1/ifd/gps/{ushort=4}</span></span> |             |
| <span data-ttu-id="0c2b5-132">2</span><span class="sxs-lookup"><span data-stu-id="0c2b5-132">2</span></span>     | <span data-ttu-id="0c2b5-133">/xmp/exif:GPSLongitude</span><span class="sxs-lookup"><span data-stu-id="0c2b5-133">/xmp/exif:GPSLongitude</span></span>   |             |



 

### <a name="remove-paths"></a><span data-ttu-id="0c2b5-134">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="0c2b5-134">Remove Paths</span></span>



| <span data-ttu-id="0c2b5-135">Commande</span><span class="sxs-lookup"><span data-stu-id="0c2b5-135">Order</span></span> | <span data-ttu-id="0c2b5-136">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="0c2b5-136">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="0c2b5-137">1</span><span class="sxs-lookup"><span data-stu-id="0c2b5-137">1</span></span>     | <span data-ttu-id="0c2b5-138">/App1/IFD/GPS/{UShort = 4}</span><span class="sxs-lookup"><span data-stu-id="0c2b5-138">/app1/ifd/gps/{ushort=4}</span></span> |
| <span data-ttu-id="0c2b5-139">2</span><span class="sxs-lookup"><span data-stu-id="0c2b5-139">2</span></span>     | <span data-ttu-id="0c2b5-140">/xmp/exif:gpslongitude</span><span class="sxs-lookup"><span data-stu-id="0c2b5-140">/xmp/exif:gpslongitude</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="0c2b5-141">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="0c2b5-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="0c2b5-142">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="0c2b5-142">Read Paths</span></span>



| <span data-ttu-id="0c2b5-143">Commande</span><span class="sxs-lookup"><span data-stu-id="0c2b5-143">Order</span></span> | <span data-ttu-id="0c2b5-144">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="0c2b5-144">Path</span></span>                       | <span data-ttu-id="0c2b5-145">Format de disque</span><span class="sxs-lookup"><span data-stu-id="0c2b5-145">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="0c2b5-146">1</span><span class="sxs-lookup"><span data-stu-id="0c2b5-146">1</span></span>     | <span data-ttu-id="0c2b5-147">/IFD/GPS/{UShort = 4}</span><span class="sxs-lookup"><span data-stu-id="0c2b5-147">/ifd/gps/{ushort=4}</span></span>        |             |
| <span data-ttu-id="0c2b5-148">2</span><span class="sxs-lookup"><span data-stu-id="0c2b5-148">2</span></span>     | <span data-ttu-id="0c2b5-149">/ifd/xmp/exif:GPSLongitude</span><span class="sxs-lookup"><span data-stu-id="0c2b5-149">/ifd/xmp/exif:GPSLongitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="0c2b5-150">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="0c2b5-150">Write Paths</span></span>



| <span data-ttu-id="0c2b5-151">Commande</span><span class="sxs-lookup"><span data-stu-id="0c2b5-151">Order</span></span> | <span data-ttu-id="0c2b5-152">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="0c2b5-152">Path</span></span>                       | <span data-ttu-id="0c2b5-153">Format de disque</span><span class="sxs-lookup"><span data-stu-id="0c2b5-153">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="0c2b5-154">1</span><span class="sxs-lookup"><span data-stu-id="0c2b5-154">1</span></span>     | <span data-ttu-id="0c2b5-155">/IFD/GPS/{UShort = 4}</span><span class="sxs-lookup"><span data-stu-id="0c2b5-155">/ifd/gps/{ushort=4}</span></span>        |             |
| <span data-ttu-id="0c2b5-156">2</span><span class="sxs-lookup"><span data-stu-id="0c2b5-156">2</span></span>     | <span data-ttu-id="0c2b5-157">/ifd/xmp/exif:GPSLongitude</span><span class="sxs-lookup"><span data-stu-id="0c2b5-157">/ifd/xmp/exif:GPSLongitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="0c2b5-158">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="0c2b5-158">Remove Paths</span></span>



| <span data-ttu-id="0c2b5-159">Commande</span><span class="sxs-lookup"><span data-stu-id="0c2b5-159">Order</span></span> | <span data-ttu-id="0c2b5-160">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="0c2b5-160">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="0c2b5-161">1</span><span class="sxs-lookup"><span data-stu-id="0c2b5-161">1</span></span>     | <span data-ttu-id="0c2b5-162">/IFD/GPS/{UShort = 4}</span><span class="sxs-lookup"><span data-stu-id="0c2b5-162">/ifd/gps/{ushort=4}</span></span>        |
| <span data-ttu-id="0c2b5-163">2</span><span class="sxs-lookup"><span data-stu-id="0c2b5-163">2</span></span>     | <span data-ttu-id="0c2b5-164">/ifd/xmp/exif:gpslongitude</span><span class="sxs-lookup"><span data-stu-id="0c2b5-164">/ifd/xmp/exif:gpslongitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0c2b5-165">Notes</span><span class="sxs-lookup"><span data-stu-id="0c2b5-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c2b5-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0c2b5-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c2b5-167">System. GPS. Longitude</span><span class="sxs-lookup"><span data-stu-id="0c2b5-167">System.GPS.Longitude</span></span>](../properties/props-system-gps-longitude.md)
</dt> </dl>

 

 
