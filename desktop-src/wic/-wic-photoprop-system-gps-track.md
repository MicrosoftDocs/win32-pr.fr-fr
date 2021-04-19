---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. Track.
ms.assetid: ac9e14a0-55f1-437e-9d27-df0fa09671c1
title: Stratégie de métadonnées de photo System. GPS. Track
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 773c65eec8b165c51456f3871309644638c1e2da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535676"
---
# <a name="systemgpstrack-photo-metadata-policy"></a><span data-ttu-id="a1b78-103">Stratégie de métadonnées de photo System. GPS. Track</span><span class="sxs-lookup"><span data-stu-id="a1b78-103">System.GPS.Track Photo Metadata Policy</span></span>

<span data-ttu-id="a1b78-104">Stratégie de métadonnées de la photo pour la propriété [System. GPS. Track](../properties/props-system-gps-track.md) .</span><span class="sxs-lookup"><span data-stu-id="a1b78-104">The photo metadata policy for the [System.GPS.Track](../properties/props-system-gps-track.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a1b78-105">A-la</span><span class="sxs-lookup"><span data-stu-id="a1b78-105">PKEY</span></span>

<span data-ttu-id="a1b78-106">Piste de la \_ balise GPS \_</span><span class="sxs-lookup"><span data-stu-id="a1b78-106">PKEY\_GPS\_Track</span></span>

### <a name="containers"></a><span data-ttu-id="a1b78-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="a1b78-107">Containers</span></span>

<span data-ttu-id="a1b78-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="a1b78-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a1b78-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a1b78-109">Read-Only</span></span>

<span data-ttu-id="a1b78-110">Oui</span><span class="sxs-lookup"><span data-stu-id="a1b78-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a1b78-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="a1b78-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a1b78-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="a1b78-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a1b78-113">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="a1b78-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="a1b78-114">Cette valeur est générée à partir de System. GPS. TrackNumerator et de System. GPS. TrackDenominator.</span><span class="sxs-lookup"><span data-stu-id="a1b78-114">This value is generated from System.GPS.TrackNumerator and System.GPS.TrackDenominator.</span></span> <span data-ttu-id="a1b78-115">Il ne peut pas être écrit directement.</span><span class="sxs-lookup"><span data-stu-id="a1b78-115">It cannot be written directly.</span></span> <span data-ttu-id="a1b78-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="a1b78-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="a1b78-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="a1b78-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="a1b78-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="a1b78-118">Read Paths</span></span>



| <span data-ttu-id="a1b78-119">Commande</span><span class="sxs-lookup"><span data-stu-id="a1b78-119">Order</span></span> | <span data-ttu-id="a1b78-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="a1b78-120">Path</span></span>                      | <span data-ttu-id="a1b78-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="a1b78-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="a1b78-122">1</span><span class="sxs-lookup"><span data-stu-id="a1b78-122">1</span></span>     | <span data-ttu-id="a1b78-123">/App1/IFD/GPS/{UShort = 15}</span><span class="sxs-lookup"><span data-stu-id="a1b78-123">/app1/ifd/gps/{ushort=15}</span></span> |             |
| <span data-ttu-id="a1b78-124">2</span><span class="sxs-lookup"><span data-stu-id="a1b78-124">2</span></span>     | <span data-ttu-id="a1b78-125">/xmp/exif:GPSTrack</span><span class="sxs-lookup"><span data-stu-id="a1b78-125">/xmp/exif:GPSTrack</span></span>        |             |



 

### <a name="write-paths"></a><span data-ttu-id="a1b78-126">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="a1b78-126">Write Paths</span></span>



| <span data-ttu-id="a1b78-127">Commande</span><span class="sxs-lookup"><span data-stu-id="a1b78-127">Order</span></span> | <span data-ttu-id="a1b78-128">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="a1b78-128">Path</span></span>                      | <span data-ttu-id="a1b78-129">Format de disque</span><span class="sxs-lookup"><span data-stu-id="a1b78-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="a1b78-130">1</span><span class="sxs-lookup"><span data-stu-id="a1b78-130">1</span></span>     | <span data-ttu-id="a1b78-131">/App1/IFD/GPS/{UShort = 15}</span><span class="sxs-lookup"><span data-stu-id="a1b78-131">/app1/ifd/gps/{ushort=15}</span></span> |             |
| <span data-ttu-id="a1b78-132">2</span><span class="sxs-lookup"><span data-stu-id="a1b78-132">2</span></span>     | <span data-ttu-id="a1b78-133">/xmp/exif:GPSTrack</span><span class="sxs-lookup"><span data-stu-id="a1b78-133">/xmp/exif:GPSTrack</span></span>        |             |



 

### <a name="remove-paths"></a><span data-ttu-id="a1b78-134">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="a1b78-134">Remove Paths</span></span>



| <span data-ttu-id="a1b78-135">Commande</span><span class="sxs-lookup"><span data-stu-id="a1b78-135">Order</span></span> | <span data-ttu-id="a1b78-136">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="a1b78-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="a1b78-137">1</span><span class="sxs-lookup"><span data-stu-id="a1b78-137">1</span></span>     | <span data-ttu-id="a1b78-138">/App1/IFD/GPS/{UShort = 15}</span><span class="sxs-lookup"><span data-stu-id="a1b78-138">/app1/ifd/gps/{ushort=15}</span></span> |
| <span data-ttu-id="a1b78-139">2</span><span class="sxs-lookup"><span data-stu-id="a1b78-139">2</span></span>     | <span data-ttu-id="a1b78-140">/xmp/exif:gpstrack</span><span class="sxs-lookup"><span data-stu-id="a1b78-140">/xmp/exif:gpstrack</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="a1b78-141">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="a1b78-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="a1b78-142">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="a1b78-142">Read Paths</span></span>



| <span data-ttu-id="a1b78-143">Commande</span><span class="sxs-lookup"><span data-stu-id="a1b78-143">Order</span></span> | <span data-ttu-id="a1b78-144">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="a1b78-144">Path</span></span>                   | <span data-ttu-id="a1b78-145">Format de disque</span><span class="sxs-lookup"><span data-stu-id="a1b78-145">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="a1b78-146">1</span><span class="sxs-lookup"><span data-stu-id="a1b78-146">1</span></span>     | <span data-ttu-id="a1b78-147">/IFD/GPS/{UShort = 15}</span><span class="sxs-lookup"><span data-stu-id="a1b78-147">/ifd/gps/{ushort=15}</span></span>   |             |
| <span data-ttu-id="a1b78-148">2</span><span class="sxs-lookup"><span data-stu-id="a1b78-148">2</span></span>     | <span data-ttu-id="a1b78-149">/ifd/xmp/exif:GPSTrack</span><span class="sxs-lookup"><span data-stu-id="a1b78-149">/ifd/xmp/exif:GPSTrack</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="a1b78-150">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="a1b78-150">Write Paths</span></span>



| <span data-ttu-id="a1b78-151">Commande</span><span class="sxs-lookup"><span data-stu-id="a1b78-151">Order</span></span> | <span data-ttu-id="a1b78-152">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="a1b78-152">Path</span></span>                   | <span data-ttu-id="a1b78-153">Format de disque</span><span class="sxs-lookup"><span data-stu-id="a1b78-153">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="a1b78-154">1</span><span class="sxs-lookup"><span data-stu-id="a1b78-154">1</span></span>     | <span data-ttu-id="a1b78-155">/IFD/GPS/{UShort = 15}</span><span class="sxs-lookup"><span data-stu-id="a1b78-155">/ifd/gps/{ushort=15}</span></span>   |             |
| <span data-ttu-id="a1b78-156">2</span><span class="sxs-lookup"><span data-stu-id="a1b78-156">2</span></span>     | <span data-ttu-id="a1b78-157">/ifd/xmp/exif:GPSTrack</span><span class="sxs-lookup"><span data-stu-id="a1b78-157">/ifd/xmp/exif:GPSTrack</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="a1b78-158">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="a1b78-158">Remove Paths</span></span>



| <span data-ttu-id="a1b78-159">Commande</span><span class="sxs-lookup"><span data-stu-id="a1b78-159">Order</span></span> | <span data-ttu-id="a1b78-160">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="a1b78-160">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="a1b78-161">1</span><span class="sxs-lookup"><span data-stu-id="a1b78-161">1</span></span>     | <span data-ttu-id="a1b78-162">/IFD/GPS/{UShort = 15}</span><span class="sxs-lookup"><span data-stu-id="a1b78-162">/ifd/gps/{ushort=15}</span></span>   |
| <span data-ttu-id="a1b78-163">2</span><span class="sxs-lookup"><span data-stu-id="a1b78-163">2</span></span>     | <span data-ttu-id="a1b78-164">/ifd/xmp/exif:gpstrack</span><span class="sxs-lookup"><span data-stu-id="a1b78-164">/ifd/xmp/exif:gpstrack</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a1b78-165">Notes</span><span class="sxs-lookup"><span data-stu-id="a1b78-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1b78-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a1b78-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1b78-167">System. GPS. Track</span><span class="sxs-lookup"><span data-stu-id="a1b78-167">System.GPS.Track</span></span>](../properties/props-system-gps-track.md)
</dt> </dl>

 

 
