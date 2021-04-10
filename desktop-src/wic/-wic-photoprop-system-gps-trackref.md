---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. TrackRef.
ms.assetid: e6912177-8add-4520-b396-c28060b359c7
title: Stratégie de métadonnées de photo System. GPS. TrackRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95fc63de6eaffd697798c08ff74a46c3d15c7818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210817"
---
# <a name="systemgpstrackref-photo-metadata-policy"></a><span data-ttu-id="3f4d4-103">Stratégie de métadonnées de photo System. GPS. TrackRef</span><span class="sxs-lookup"><span data-stu-id="3f4d4-103">System.GPS.TrackRef Photo Metadata Policy</span></span>

<span data-ttu-id="3f4d4-104">Stratégie de métadonnées de la photo pour la propriété [System. GPS. TrackRef](../properties/props-system-gps-trackref.md) .</span><span class="sxs-lookup"><span data-stu-id="3f4d4-104">The photo metadata policy for the [System.GPS.TrackRef](../properties/props-system-gps-trackref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="3f4d4-105">A-la</span><span class="sxs-lookup"><span data-stu-id="3f4d4-105">PKEY</span></span>

<span data-ttu-id="3f4d4-106">\_TrackRef GPS \_</span><span class="sxs-lookup"><span data-stu-id="3f4d4-106">PKEY\_GPS\_TrackRef</span></span>

### <a name="containers"></a><span data-ttu-id="3f4d4-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="3f4d4-107">Containers</span></span>

<span data-ttu-id="3f4d4-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="3f4d4-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="3f4d4-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f4d4-109">Read-Only</span></span>

<span data-ttu-id="3f4d4-110">Non</span><span class="sxs-lookup"><span data-stu-id="3f4d4-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="3f4d4-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="3f4d4-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="3f4d4-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="3f4d4-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="3f4d4-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="3f4d4-113">Input Type</span></span>

<span data-ttu-id="3f4d4-114">String</span><span class="sxs-lookup"><span data-stu-id="3f4d4-114">String</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="3f4d4-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="3f4d4-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="3f4d4-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="3f4d4-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="3f4d4-117">Stratégies JPEG</span><span class="sxs-lookup"><span data-stu-id="3f4d4-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="3f4d4-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="3f4d4-118">Read Paths</span></span>



| <span data-ttu-id="3f4d4-119">Commande</span><span class="sxs-lookup"><span data-stu-id="3f4d4-119">Order</span></span> | <span data-ttu-id="3f4d4-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="3f4d4-120">Path</span></span>                      | <span data-ttu-id="3f4d4-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="3f4d4-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="3f4d4-122">1</span><span class="sxs-lookup"><span data-stu-id="3f4d4-122">1</span></span>     | <span data-ttu-id="3f4d4-123">/App1/IFD/GPS/{UShort = 14}</span><span class="sxs-lookup"><span data-stu-id="3f4d4-123">/app1/ifd/gps/{ushort=14}</span></span> | <span data-ttu-id="3f4d4-124">ascii</span><span class="sxs-lookup"><span data-stu-id="3f4d4-124">ascii</span></span>       |
| <span data-ttu-id="3f4d4-125">2</span><span class="sxs-lookup"><span data-stu-id="3f4d4-125">2</span></span>     | <span data-ttu-id="3f4d4-126">/xmp/exif:GPSTrackRef</span><span class="sxs-lookup"><span data-stu-id="3f4d4-126">/xmp/exif:GPSTrackRef</span></span>     | <span data-ttu-id="3f4d4-127">unicode</span><span class="sxs-lookup"><span data-stu-id="3f4d4-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="3f4d4-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="3f4d4-128">Write Paths</span></span>



| <span data-ttu-id="3f4d4-129">Commande</span><span class="sxs-lookup"><span data-stu-id="3f4d4-129">Order</span></span> | <span data-ttu-id="3f4d4-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="3f4d4-130">Path</span></span>                      | <span data-ttu-id="3f4d4-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="3f4d4-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="3f4d4-132">1</span><span class="sxs-lookup"><span data-stu-id="3f4d4-132">1</span></span>     | <span data-ttu-id="3f4d4-133">/App1/IFD/GPS/{UShort = 14}</span><span class="sxs-lookup"><span data-stu-id="3f4d4-133">/app1/ifd/gps/{ushort=14}</span></span> | <span data-ttu-id="3f4d4-134">ascii</span><span class="sxs-lookup"><span data-stu-id="3f4d4-134">ascii</span></span>       |
| <span data-ttu-id="3f4d4-135">2</span><span class="sxs-lookup"><span data-stu-id="3f4d4-135">2</span></span>     | <span data-ttu-id="3f4d4-136">/xmp/exif:GPSTrackRef</span><span class="sxs-lookup"><span data-stu-id="3f4d4-136">/xmp/exif:GPSTrackRef</span></span>     | <span data-ttu-id="3f4d4-137">unicode</span><span class="sxs-lookup"><span data-stu-id="3f4d4-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="3f4d4-138">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="3f4d4-138">Remove Paths</span></span>



| <span data-ttu-id="3f4d4-139">Commande</span><span class="sxs-lookup"><span data-stu-id="3f4d4-139">Order</span></span> | <span data-ttu-id="3f4d4-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="3f4d4-140">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="3f4d4-141">1</span><span class="sxs-lookup"><span data-stu-id="3f4d4-141">1</span></span>     | <span data-ttu-id="3f4d4-142">/App1/IFD/GPS/{UShort = 14}</span><span class="sxs-lookup"><span data-stu-id="3f4d4-142">/app1/ifd/gps/{ushort=14}</span></span> |
| <span data-ttu-id="3f4d4-143">2</span><span class="sxs-lookup"><span data-stu-id="3f4d4-143">2</span></span>     | <span data-ttu-id="3f4d4-144">/xmp/exif:gpstrackref</span><span class="sxs-lookup"><span data-stu-id="3f4d4-144">/xmp/exif:gpstrackref</span></span>     |



 

### <a name="tiff-policies"></a><span data-ttu-id="3f4d4-145">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="3f4d4-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="3f4d4-146">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="3f4d4-146">Read Paths</span></span>



| <span data-ttu-id="3f4d4-147">Commande</span><span class="sxs-lookup"><span data-stu-id="3f4d4-147">Order</span></span> | <span data-ttu-id="3f4d4-148">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="3f4d4-148">Path</span></span>                      | <span data-ttu-id="3f4d4-149">Format de disque</span><span class="sxs-lookup"><span data-stu-id="3f4d4-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="3f4d4-150">1</span><span class="sxs-lookup"><span data-stu-id="3f4d4-150">1</span></span>     | <span data-ttu-id="3f4d4-151">/IFD/GPS/{UShort = 14}</span><span class="sxs-lookup"><span data-stu-id="3f4d4-151">/ifd/gps/{ushort=14}</span></span>      | <span data-ttu-id="3f4d4-152">ascii</span><span class="sxs-lookup"><span data-stu-id="3f4d4-152">ascii</span></span>       |
| <span data-ttu-id="3f4d4-153">2</span><span class="sxs-lookup"><span data-stu-id="3f4d4-153">2</span></span>     | <span data-ttu-id="3f4d4-154">/ifd/xmp/exif:GPSTrackRef</span><span class="sxs-lookup"><span data-stu-id="3f4d4-154">/ifd/xmp/exif:GPSTrackRef</span></span> | <span data-ttu-id="3f4d4-155">unicode</span><span class="sxs-lookup"><span data-stu-id="3f4d4-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="3f4d4-156">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="3f4d4-156">Write Paths</span></span>



| <span data-ttu-id="3f4d4-157">Commande</span><span class="sxs-lookup"><span data-stu-id="3f4d4-157">Order</span></span> | <span data-ttu-id="3f4d4-158">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="3f4d4-158">Path</span></span>                      | <span data-ttu-id="3f4d4-159">Format de disque</span><span class="sxs-lookup"><span data-stu-id="3f4d4-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="3f4d4-160">1</span><span class="sxs-lookup"><span data-stu-id="3f4d4-160">1</span></span>     | <span data-ttu-id="3f4d4-161">/IFD/GPS/{UShort = 14}</span><span class="sxs-lookup"><span data-stu-id="3f4d4-161">/ifd/gps/{ushort=14}</span></span>      | <span data-ttu-id="3f4d4-162">ascii</span><span class="sxs-lookup"><span data-stu-id="3f4d4-162">ascii</span></span>       |
| <span data-ttu-id="3f4d4-163">2</span><span class="sxs-lookup"><span data-stu-id="3f4d4-163">2</span></span>     | <span data-ttu-id="3f4d4-164">/ifd/xmp/exif:GPSTrackRef</span><span class="sxs-lookup"><span data-stu-id="3f4d4-164">/ifd/xmp/exif:GPSTrackRef</span></span> | <span data-ttu-id="3f4d4-165">unicode</span><span class="sxs-lookup"><span data-stu-id="3f4d4-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="3f4d4-166">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="3f4d4-166">Remove Paths</span></span>



| <span data-ttu-id="3f4d4-167">Commande</span><span class="sxs-lookup"><span data-stu-id="3f4d4-167">Order</span></span> | <span data-ttu-id="3f4d4-168">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="3f4d4-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="3f4d4-169">1</span><span class="sxs-lookup"><span data-stu-id="3f4d4-169">1</span></span>     | <span data-ttu-id="3f4d4-170">/IFD/GPS/{UShort = 14}</span><span class="sxs-lookup"><span data-stu-id="3f4d4-170">/ifd/gps/{ushort=14}</span></span>      |
| <span data-ttu-id="3f4d4-171">2</span><span class="sxs-lookup"><span data-stu-id="3f4d4-171">2</span></span>     | <span data-ttu-id="3f4d4-172">/ifd/xmp/exif:gpstrackref</span><span class="sxs-lookup"><span data-stu-id="3f4d4-172">/ifd/xmp/exif:gpstrackref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3f4d4-173">Notes</span><span class="sxs-lookup"><span data-stu-id="3f4d4-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f4d4-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3f4d4-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f4d4-175">System. GPS. TrackRef</span><span class="sxs-lookup"><span data-stu-id="3f4d4-175">System.GPS.TrackRef</span></span>](../properties/props-system-gps-trackref.md)
</dt> </dl>

 

 
