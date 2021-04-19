---
description: La stratégie de métadonnées de la photo pour la propriété System. GPS. Latitude.
ms.assetid: 0f8cea07-da96-4d2a-8444-6073b51e1236
title: Stratégie de métadonnées de photo System. GPS. Latitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5320869c1e8fd0d4b17bb17da455fc939bf44b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523351"
---
# <a name="systemgpslatitude-photo-metadata-policy"></a><span data-ttu-id="f700d-103">Stratégie de métadonnées de photo System. GPS. Latitude</span><span class="sxs-lookup"><span data-stu-id="f700d-103">System.GPS.Latitude Photo Metadata Policy</span></span>

<span data-ttu-id="f700d-104">La stratégie de métadonnées de la photo pour la propriété [System. GPS. Latitude](../properties/props-system-gps-latitude.md) .</span><span class="sxs-lookup"><span data-stu-id="f700d-104">The photo metadata policy for the [System.GPS.Latitude](../properties/props-system-gps-latitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="f700d-105">A-la</span><span class="sxs-lookup"><span data-stu-id="f700d-105">PKEY</span></span>

<span data-ttu-id="f700d-106">Latitude de la \_ balise GPS \_</span><span class="sxs-lookup"><span data-stu-id="f700d-106">PKEY\_GPS\_Latitude</span></span>

### <a name="containers"></a><span data-ttu-id="f700d-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="f700d-107">Containers</span></span>

<span data-ttu-id="f700d-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="f700d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="f700d-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f700d-109">Read-Only</span></span>

<span data-ttu-id="f700d-110">Oui</span><span class="sxs-lookup"><span data-stu-id="f700d-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="f700d-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="f700d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="f700d-112">VT \_ Vector \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="f700d-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="f700d-113">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="f700d-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="f700d-114">Cette valeur peut être écrite en écrivant dans System. GPS. LatitudeNumerator et System. GPS. LatitudeDenominator.</span><span class="sxs-lookup"><span data-stu-id="f700d-114">This value can be written by writing to System.GPS.LatitudeNumerator and System.GPS.LatitudeDenominator.</span></span> <span data-ttu-id="f700d-115">Il ne peut pas être écrit directement.</span><span class="sxs-lookup"><span data-stu-id="f700d-115">It cannot be written directly.</span></span> <span data-ttu-id="f700d-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="f700d-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="f700d-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="f700d-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="f700d-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="f700d-118">Read Paths</span></span>



| <span data-ttu-id="f700d-119">Commande</span><span class="sxs-lookup"><span data-stu-id="f700d-119">Order</span></span> | <span data-ttu-id="f700d-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="f700d-120">Path</span></span>                     | <span data-ttu-id="f700d-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="f700d-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="f700d-122">1</span><span class="sxs-lookup"><span data-stu-id="f700d-122">1</span></span>     | <span data-ttu-id="f700d-123">/App1/IFD/GPS/{UShort = 2}</span><span class="sxs-lookup"><span data-stu-id="f700d-123">/app1/ifd/gps/{ushort=2}</span></span> |             |
| <span data-ttu-id="f700d-124">2</span><span class="sxs-lookup"><span data-stu-id="f700d-124">2</span></span>     | <span data-ttu-id="f700d-125">/xmp/exif:GPSLatitude</span><span class="sxs-lookup"><span data-stu-id="f700d-125">/xmp/exif:GPSLatitude</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="f700d-126">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="f700d-126">Write Paths</span></span>



| <span data-ttu-id="f700d-127">Commande</span><span class="sxs-lookup"><span data-stu-id="f700d-127">Order</span></span> | <span data-ttu-id="f700d-128">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="f700d-128">Path</span></span>                     | <span data-ttu-id="f700d-129">Format de disque</span><span class="sxs-lookup"><span data-stu-id="f700d-129">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="f700d-130">1</span><span class="sxs-lookup"><span data-stu-id="f700d-130">1</span></span>     | <span data-ttu-id="f700d-131">/App1/IFD/GPS/{UShort = 2}</span><span class="sxs-lookup"><span data-stu-id="f700d-131">/app1/ifd/gps/{ushort=2}</span></span> |             |
| <span data-ttu-id="f700d-132">2</span><span class="sxs-lookup"><span data-stu-id="f700d-132">2</span></span>     | <span data-ttu-id="f700d-133">/xmp/exif:GPSLatitude</span><span class="sxs-lookup"><span data-stu-id="f700d-133">/xmp/exif:GPSLatitude</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="f700d-134">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="f700d-134">Remove Paths</span></span>



| <span data-ttu-id="f700d-135">Commande</span><span class="sxs-lookup"><span data-stu-id="f700d-135">Order</span></span> | <span data-ttu-id="f700d-136">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="f700d-136">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="f700d-137">1</span><span class="sxs-lookup"><span data-stu-id="f700d-137">1</span></span>     | <span data-ttu-id="f700d-138">/App1/IFD/GPS/{UShort = 2}</span><span class="sxs-lookup"><span data-stu-id="f700d-138">/app1/ifd/gps/{ushort=2}</span></span> |
| <span data-ttu-id="f700d-139">2</span><span class="sxs-lookup"><span data-stu-id="f700d-139">2</span></span>     | <span data-ttu-id="f700d-140">/xmp/exif:gpslatitude</span><span class="sxs-lookup"><span data-stu-id="f700d-140">/xmp/exif:gpslatitude</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="f700d-141">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="f700d-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="f700d-142">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="f700d-142">Read Paths</span></span>



| <span data-ttu-id="f700d-143">Commande</span><span class="sxs-lookup"><span data-stu-id="f700d-143">Order</span></span> | <span data-ttu-id="f700d-144">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="f700d-144">Path</span></span>                      | <span data-ttu-id="f700d-145">Format de disque</span><span class="sxs-lookup"><span data-stu-id="f700d-145">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="f700d-146">1</span><span class="sxs-lookup"><span data-stu-id="f700d-146">1</span></span>     | <span data-ttu-id="f700d-147">/IFD/GPS/{UShort = 2}</span><span class="sxs-lookup"><span data-stu-id="f700d-147">/ifd/gps/{ushort=2}</span></span>       |             |
| <span data-ttu-id="f700d-148">2</span><span class="sxs-lookup"><span data-stu-id="f700d-148">2</span></span>     | <span data-ttu-id="f700d-149">/ifd/xmp/exif:GPSLatitude</span><span class="sxs-lookup"><span data-stu-id="f700d-149">/ifd/xmp/exif:GPSLatitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="f700d-150">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="f700d-150">Write Paths</span></span>



| <span data-ttu-id="f700d-151">Commande</span><span class="sxs-lookup"><span data-stu-id="f700d-151">Order</span></span> | <span data-ttu-id="f700d-152">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="f700d-152">Path</span></span>                      | <span data-ttu-id="f700d-153">Format de disque</span><span class="sxs-lookup"><span data-stu-id="f700d-153">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="f700d-154">1</span><span class="sxs-lookup"><span data-stu-id="f700d-154">1</span></span>     | <span data-ttu-id="f700d-155">/IFD/GPS/{UShort = 2}</span><span class="sxs-lookup"><span data-stu-id="f700d-155">/ifd/gps/{ushort=2}</span></span>       |             |
| <span data-ttu-id="f700d-156">2</span><span class="sxs-lookup"><span data-stu-id="f700d-156">2</span></span>     | <span data-ttu-id="f700d-157">/ifd/xmp/exif:GPSLatitude</span><span class="sxs-lookup"><span data-stu-id="f700d-157">/ifd/xmp/exif:GPSLatitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="f700d-158">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="f700d-158">Remove Paths</span></span>



| <span data-ttu-id="f700d-159">Commande</span><span class="sxs-lookup"><span data-stu-id="f700d-159">Order</span></span> | <span data-ttu-id="f700d-160">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="f700d-160">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="f700d-161">1</span><span class="sxs-lookup"><span data-stu-id="f700d-161">1</span></span>     | <span data-ttu-id="f700d-162">/IFD/GPS/{UShort = 2}</span><span class="sxs-lookup"><span data-stu-id="f700d-162">/ifd/gps/{ushort=2}</span></span>       |
| <span data-ttu-id="f700d-163">2</span><span class="sxs-lookup"><span data-stu-id="f700d-163">2</span></span>     | <span data-ttu-id="f700d-164">/ifd/xmp/exif:gpslatitude</span><span class="sxs-lookup"><span data-stu-id="f700d-164">/ifd/xmp/exif:gpslatitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f700d-165">Notes</span><span class="sxs-lookup"><span data-stu-id="f700d-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="f700d-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f700d-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f700d-167">System. GPS. Latitude</span><span class="sxs-lookup"><span data-stu-id="f700d-167">System.GPS.Latitude</span></span>](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
