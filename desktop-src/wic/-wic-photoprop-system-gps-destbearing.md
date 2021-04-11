---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. DestBearing.
ms.assetid: ccc31b3d-27fd-4a8c-a304-852cf6114ec5
title: Stratégie de métadonnées de photo System. GPS. DestBearing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a084a0633579afe646403fb4dcad0ca8a1b9ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320410"
---
# <a name="systemgpsdestbearing-photo-metadata-policy"></a><span data-ttu-id="edfd8-103">Stratégie de métadonnées de photo System. GPS. DestBearing</span><span class="sxs-lookup"><span data-stu-id="edfd8-103">System.GPS.DestBearing Photo Metadata Policy</span></span>

<span data-ttu-id="edfd8-104">Stratégie de métadonnées de la photo pour la propriété [System. GPS. DestBearing](../properties/props-system-gps-destbearing.md) .</span><span class="sxs-lookup"><span data-stu-id="edfd8-104">The photo metadata policy for the [System.GPS.DestBearing](../properties/props-system-gps-destbearing.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="edfd8-105">A-la</span><span class="sxs-lookup"><span data-stu-id="edfd8-105">PKEY</span></span>

<span data-ttu-id="edfd8-106">\_DestBearing GPS \_</span><span class="sxs-lookup"><span data-stu-id="edfd8-106">PKEY\_GPS\_DestBearing</span></span>

### <a name="containers"></a><span data-ttu-id="edfd8-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="edfd8-107">Containers</span></span>

<span data-ttu-id="edfd8-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="edfd8-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="edfd8-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="edfd8-109">Read-Only</span></span>

<span data-ttu-id="edfd8-110">Oui</span><span class="sxs-lookup"><span data-stu-id="edfd8-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="edfd8-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="edfd8-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="edfd8-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="edfd8-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="edfd8-113">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="edfd8-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="edfd8-114">Cette valeur peut être écrite en écrivant dans System. GPS. DestBearingNumerator et System. GPS. DestBearingDenominator.</span><span class="sxs-lookup"><span data-stu-id="edfd8-114">This value can be written by writing to System.GPS.DestBearingNumerator and System.GPS.DestBearingDenominator.</span></span> <span data-ttu-id="edfd8-115">Il ne peut pas être écrit directement.</span><span class="sxs-lookup"><span data-stu-id="edfd8-115">It cannot be written directly.</span></span> <span data-ttu-id="edfd8-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="edfd8-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="edfd8-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="edfd8-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="edfd8-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="edfd8-118">Read Paths</span></span>



| <span data-ttu-id="edfd8-119">Commande</span><span class="sxs-lookup"><span data-stu-id="edfd8-119">Order</span></span> | <span data-ttu-id="edfd8-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="edfd8-120">Path</span></span>                      | <span data-ttu-id="edfd8-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="edfd8-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="edfd8-122">1</span><span class="sxs-lookup"><span data-stu-id="edfd8-122">1</span></span>     | <span data-ttu-id="edfd8-123">/App1/IFD/GPS/{UShort = 24}</span><span class="sxs-lookup"><span data-stu-id="edfd8-123">/app1/ifd/gps/{ushort=24}</span></span> |             |
| <span data-ttu-id="edfd8-124">2</span><span class="sxs-lookup"><span data-stu-id="edfd8-124">2</span></span>     | <span data-ttu-id="edfd8-125">/xmp/exif:GPSDestBearing</span><span class="sxs-lookup"><span data-stu-id="edfd8-125">/xmp/exif:GPSDestBearing</span></span>  |             |



 

### <a name="write-paths"></a><span data-ttu-id="edfd8-126">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="edfd8-126">Write Paths</span></span>



| <span data-ttu-id="edfd8-127">Commande</span><span class="sxs-lookup"><span data-stu-id="edfd8-127">Order</span></span> | <span data-ttu-id="edfd8-128">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="edfd8-128">Path</span></span>                      | <span data-ttu-id="edfd8-129">Format de disque</span><span class="sxs-lookup"><span data-stu-id="edfd8-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="edfd8-130">1</span><span class="sxs-lookup"><span data-stu-id="edfd8-130">1</span></span>     | <span data-ttu-id="edfd8-131">/App1/IFD/GPS/{UShort = 24}</span><span class="sxs-lookup"><span data-stu-id="edfd8-131">/app1/ifd/gps/{ushort=24}</span></span> |             |
| <span data-ttu-id="edfd8-132">2</span><span class="sxs-lookup"><span data-stu-id="edfd8-132">2</span></span>     | <span data-ttu-id="edfd8-133">/xmp/exif:GPSDestBearing</span><span class="sxs-lookup"><span data-stu-id="edfd8-133">/xmp/exif:GPSDestBearing</span></span>  |             |



 

### <a name="remove-paths"></a><span data-ttu-id="edfd8-134">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="edfd8-134">Remove Paths</span></span>



| <span data-ttu-id="edfd8-135">Commande</span><span class="sxs-lookup"><span data-stu-id="edfd8-135">Order</span></span> | <span data-ttu-id="edfd8-136">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="edfd8-136">Path</span></span>                      | <span data-ttu-id="edfd8-137">Format de disque</span><span class="sxs-lookup"><span data-stu-id="edfd8-137">Disk format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="edfd8-138">1</span><span class="sxs-lookup"><span data-stu-id="edfd8-138">1</span></span>     | <span data-ttu-id="edfd8-139">/App1/IFD/GPS/{UShort = 24}</span><span class="sxs-lookup"><span data-stu-id="edfd8-139">/app1/ifd/gps/{ushort=24}</span></span> |             |
| <span data-ttu-id="edfd8-140">2</span><span class="sxs-lookup"><span data-stu-id="edfd8-140">2</span></span>     | <span data-ttu-id="edfd8-141">/xmp/exif:gpsdestbearing</span><span class="sxs-lookup"><span data-stu-id="edfd8-141">/xmp/exif:gpsdestbearing</span></span>  |             |



 

### <a name="tiff-policies"></a><span data-ttu-id="edfd8-142">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="edfd8-142">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="edfd8-143">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="edfd8-143">Read Paths</span></span>



| <span data-ttu-id="edfd8-144">Commande</span><span class="sxs-lookup"><span data-stu-id="edfd8-144">Order</span></span> | <span data-ttu-id="edfd8-145">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="edfd8-145">Path</span></span>                         | <span data-ttu-id="edfd8-146">Format de disque</span><span class="sxs-lookup"><span data-stu-id="edfd8-146">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="edfd8-147">1</span><span class="sxs-lookup"><span data-stu-id="edfd8-147">1</span></span>     | <span data-ttu-id="edfd8-148">/IFD/GPS/{UShort = 24}</span><span class="sxs-lookup"><span data-stu-id="edfd8-148">/ifd/gps/{ushort=24}</span></span>         |             |
| <span data-ttu-id="edfd8-149">2</span><span class="sxs-lookup"><span data-stu-id="edfd8-149">2</span></span>     | <span data-ttu-id="edfd8-150">/ifd/xmp/exif:GPSDestBearing</span><span class="sxs-lookup"><span data-stu-id="edfd8-150">/ifd/xmp/exif:GPSDestBearing</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="edfd8-151">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="edfd8-151">Write Paths</span></span>



| <span data-ttu-id="edfd8-152">Commande</span><span class="sxs-lookup"><span data-stu-id="edfd8-152">Order</span></span> | <span data-ttu-id="edfd8-153">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="edfd8-153">Path</span></span>                         | <span data-ttu-id="edfd8-154">Format de disque</span><span class="sxs-lookup"><span data-stu-id="edfd8-154">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="edfd8-155">1</span><span class="sxs-lookup"><span data-stu-id="edfd8-155">1</span></span>     | <span data-ttu-id="edfd8-156">/IFD/GPS/{UShort = 24}</span><span class="sxs-lookup"><span data-stu-id="edfd8-156">/ifd/gps/{ushort=24}</span></span>         |             |
| <span data-ttu-id="edfd8-157">2</span><span class="sxs-lookup"><span data-stu-id="edfd8-157">2</span></span>     | <span data-ttu-id="edfd8-158">/ifd/xmp/exif:GPSDestBearing</span><span class="sxs-lookup"><span data-stu-id="edfd8-158">/ifd/xmp/exif:GPSDestBearing</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="edfd8-159">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="edfd8-159">Remove Paths</span></span>



| <span data-ttu-id="edfd8-160">Commande</span><span class="sxs-lookup"><span data-stu-id="edfd8-160">Order</span></span> | <span data-ttu-id="edfd8-161">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="edfd8-161">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="edfd8-162">1</span><span class="sxs-lookup"><span data-stu-id="edfd8-162">1</span></span>     | <span data-ttu-id="edfd8-163">/IFD/GPS/{UShort = 24}</span><span class="sxs-lookup"><span data-stu-id="edfd8-163">/ifd/gps/{ushort=24}</span></span>         |
| <span data-ttu-id="edfd8-164">2</span><span class="sxs-lookup"><span data-stu-id="edfd8-164">2</span></span>     | <span data-ttu-id="edfd8-165">/ifd/xmp/exif:gpsdestbearing</span><span class="sxs-lookup"><span data-stu-id="edfd8-165">/ifd/xmp/exif:gpsdestbearing</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="edfd8-166">Notes</span><span class="sxs-lookup"><span data-stu-id="edfd8-166">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="edfd8-167">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="edfd8-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edfd8-168">System. GPS. DestBearing</span><span class="sxs-lookup"><span data-stu-id="edfd8-168">System.GPS.DestBearing</span></span>](../properties/props-system-gps-destbearing.md)
</dt> </dl>

 

 
