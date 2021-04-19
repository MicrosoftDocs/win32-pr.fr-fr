---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. AltitudeRef.
ms.assetid: abbb2441-25ca-484b-a744-620ff2794221
title: Stratégie de métadonnées de photo System. GPS. AltitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db600d218d72014c49fd3f0a8b5eb11dd4c467d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523416"
---
# <a name="systemgpsaltituderef-photo-metadata-policy"></a><span data-ttu-id="5632d-103">Stratégie de métadonnées de photo System. GPS. AltitudeRef</span><span class="sxs-lookup"><span data-stu-id="5632d-103">System.GPS.AltitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="5632d-104">Stratégie de métadonnées de la photo pour la propriété [System. GPS. AltitudeRef](../properties/props-system-gps-altituderef.md) .</span><span class="sxs-lookup"><span data-stu-id="5632d-104">The photo metadata policy for the [System.GPS.AltitudeRef](../properties/props-system-gps-altituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="5632d-105">A-la</span><span class="sxs-lookup"><span data-stu-id="5632d-105">PKEY</span></span>

<span data-ttu-id="5632d-106">\_AltitudeRef GPS \_</span><span class="sxs-lookup"><span data-stu-id="5632d-106">PKEY\_GPS\_AltitudeRef</span></span>

### <a name="description"></a><span data-ttu-id="5632d-107">Description</span><span class="sxs-lookup"><span data-stu-id="5632d-107">Description</span></span>

<span data-ttu-id="5632d-108">Indique l’altitude utilisée comme altitude de référence.</span><span class="sxs-lookup"><span data-stu-id="5632d-108">Indicates the altitude used as the reference altitude.</span></span> <span data-ttu-id="5632d-109">La valeur 0 indique que l’altitude est au-dessus de la mer.</span><span class="sxs-lookup"><span data-stu-id="5632d-109">A value of 0 indicates the altitude is above sea level.</span></span> <span data-ttu-id="5632d-110">La valeur 1 indique une altitude inférieure au niveau de la mer.</span><span class="sxs-lookup"><span data-stu-id="5632d-110">A value of 1 indicates an altitude below sea level.</span></span>

### <a name="containers"></a><span data-ttu-id="5632d-111">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="5632d-111">Containers</span></span>

<span data-ttu-id="5632d-112">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="5632d-112">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="5632d-113">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5632d-113">Read-Only</span></span>

<span data-ttu-id="5632d-114">Non</span><span class="sxs-lookup"><span data-stu-id="5632d-114">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="5632d-115">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="5632d-115">Output PROPVARIANT Type</span></span>

<span data-ttu-id="5632d-116">\_UI1 VT</span><span class="sxs-lookup"><span data-stu-id="5632d-116">VT\_UI1</span></span>

### <a name="input-type"></a><span data-ttu-id="5632d-117">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="5632d-117">Input Type</span></span>

<span data-ttu-id="5632d-118">Poids.</span><span class="sxs-lookup"><span data-stu-id="5632d-118">Byte.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="5632d-119">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="5632d-119">Conflict Resolution Policy</span></span>

<span data-ttu-id="5632d-120">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="5632d-120">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="5632d-121">Stratégies JPEG</span><span class="sxs-lookup"><span data-stu-id="5632d-121">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="5632d-122">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="5632d-122">Read Paths</span></span>



| <span data-ttu-id="5632d-123">Commande</span><span class="sxs-lookup"><span data-stu-id="5632d-123">Order</span></span> | <span data-ttu-id="5632d-124">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="5632d-124">Path</span></span>                     | <span data-ttu-id="5632d-125">Format de disque</span><span class="sxs-lookup"><span data-stu-id="5632d-125">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="5632d-126">1</span><span class="sxs-lookup"><span data-stu-id="5632d-126">1</span></span>     | <span data-ttu-id="5632d-127">/App1/IFD/GPS/{UShort = 5}</span><span class="sxs-lookup"><span data-stu-id="5632d-127">/app1/ifd/gps/{ushort=5}</span></span> | <span data-ttu-id="5632d-128">byte</span><span class="sxs-lookup"><span data-stu-id="5632d-128">byte</span></span>        |
| <span data-ttu-id="5632d-129">2</span><span class="sxs-lookup"><span data-stu-id="5632d-129">2</span></span>     | <span data-ttu-id="5632d-130">/xmp/exif:GPSAltitudeRef</span><span class="sxs-lookup"><span data-stu-id="5632d-130">/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="5632d-131">unicode</span><span class="sxs-lookup"><span data-stu-id="5632d-131">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="5632d-132">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="5632d-132">Write Paths</span></span>



| <span data-ttu-id="5632d-133">Commande</span><span class="sxs-lookup"><span data-stu-id="5632d-133">Order</span></span> | <span data-ttu-id="5632d-134">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="5632d-134">Path</span></span>                     | <span data-ttu-id="5632d-135">Format de disque</span><span class="sxs-lookup"><span data-stu-id="5632d-135">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="5632d-136">1</span><span class="sxs-lookup"><span data-stu-id="5632d-136">1</span></span>     | <span data-ttu-id="5632d-137">/App1/IFD/GPS/{UShort = 5}</span><span class="sxs-lookup"><span data-stu-id="5632d-137">/app1/ifd/gps/{ushort=5}</span></span> | <span data-ttu-id="5632d-138">byte</span><span class="sxs-lookup"><span data-stu-id="5632d-138">byte</span></span>        |
| <span data-ttu-id="5632d-139">2</span><span class="sxs-lookup"><span data-stu-id="5632d-139">2</span></span>     | <span data-ttu-id="5632d-140">/xmp/exif:GPSAltitudeRef</span><span class="sxs-lookup"><span data-stu-id="5632d-140">/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="5632d-141">unicode</span><span class="sxs-lookup"><span data-stu-id="5632d-141">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="5632d-142">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="5632d-142">Remove Paths</span></span>



| <span data-ttu-id="5632d-143">Commande</span><span class="sxs-lookup"><span data-stu-id="5632d-143">Order</span></span> | <span data-ttu-id="5632d-144">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="5632d-144">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="5632d-145">1</span><span class="sxs-lookup"><span data-stu-id="5632d-145">1</span></span>     | <span data-ttu-id="5632d-146">/App1/IFD/GPS/{UShort = 5}</span><span class="sxs-lookup"><span data-stu-id="5632d-146">/app1/ifd/gps/{ushort=5}</span></span> |
| <span data-ttu-id="5632d-147">2</span><span class="sxs-lookup"><span data-stu-id="5632d-147">2</span></span>     | <span data-ttu-id="5632d-148">/xmp/exif:gpsaltituderef</span><span class="sxs-lookup"><span data-stu-id="5632d-148">/xmp/exif:gpsaltituderef</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="5632d-149">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="5632d-149">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="5632d-150">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="5632d-150">Read Paths</span></span>



| <span data-ttu-id="5632d-151">Commande</span><span class="sxs-lookup"><span data-stu-id="5632d-151">Order</span></span> | <span data-ttu-id="5632d-152">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="5632d-152">Path</span></span>                         | <span data-ttu-id="5632d-153">Format de disque</span><span class="sxs-lookup"><span data-stu-id="5632d-153">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="5632d-154">1</span><span class="sxs-lookup"><span data-stu-id="5632d-154">1</span></span>     | <span data-ttu-id="5632d-155">/IFD/GPS/{UShort = 5}</span><span class="sxs-lookup"><span data-stu-id="5632d-155">/ifd/gps/{ushort=5}</span></span>          | <span data-ttu-id="5632d-156">byte</span><span class="sxs-lookup"><span data-stu-id="5632d-156">byte</span></span>        |
| <span data-ttu-id="5632d-157">2</span><span class="sxs-lookup"><span data-stu-id="5632d-157">2</span></span>     | <span data-ttu-id="5632d-158">/ifd/xmp/exif:GPSAltitudeRef</span><span class="sxs-lookup"><span data-stu-id="5632d-158">/ifd/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="5632d-159">unicode</span><span class="sxs-lookup"><span data-stu-id="5632d-159">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="5632d-160">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="5632d-160">Write Paths</span></span>



| <span data-ttu-id="5632d-161">Commande</span><span class="sxs-lookup"><span data-stu-id="5632d-161">Order</span></span> | <span data-ttu-id="5632d-162">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="5632d-162">Path</span></span>                         | <span data-ttu-id="5632d-163">Format de disque</span><span class="sxs-lookup"><span data-stu-id="5632d-163">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="5632d-164">1</span><span class="sxs-lookup"><span data-stu-id="5632d-164">1</span></span>     | <span data-ttu-id="5632d-165">/IFD/GPS/{UShort = 5}</span><span class="sxs-lookup"><span data-stu-id="5632d-165">/ifd/gps/{ushort=5}</span></span>          | <span data-ttu-id="5632d-166">byte</span><span class="sxs-lookup"><span data-stu-id="5632d-166">byte</span></span>        |
| <span data-ttu-id="5632d-167">2</span><span class="sxs-lookup"><span data-stu-id="5632d-167">2</span></span>     | <span data-ttu-id="5632d-168">/ifd/xmp/exif:GPSAltitudeRef</span><span class="sxs-lookup"><span data-stu-id="5632d-168">/ifd/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="5632d-169">unicode</span><span class="sxs-lookup"><span data-stu-id="5632d-169">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="5632d-170">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="5632d-170">Remove Paths</span></span>



| <span data-ttu-id="5632d-171">Commande</span><span class="sxs-lookup"><span data-stu-id="5632d-171">Order</span></span> | <span data-ttu-id="5632d-172">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="5632d-172">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="5632d-173">1</span><span class="sxs-lookup"><span data-stu-id="5632d-173">1</span></span>     | <span data-ttu-id="5632d-174">/IFD/GPS/{UShort = 5}</span><span class="sxs-lookup"><span data-stu-id="5632d-174">/ifd/gps/{ushort=5}</span></span>          |
| <span data-ttu-id="5632d-175">2</span><span class="sxs-lookup"><span data-stu-id="5632d-175">2</span></span>     | <span data-ttu-id="5632d-176">/ifd/xmp/exif:gpsaltituderef</span><span class="sxs-lookup"><span data-stu-id="5632d-176">/ifd/xmp/exif:gpsaltituderef</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5632d-177">Notes</span><span class="sxs-lookup"><span data-stu-id="5632d-177">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="5632d-178">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5632d-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5632d-179">System. GPS. AltitudeRef</span><span class="sxs-lookup"><span data-stu-id="5632d-179">System.GPS.AltitudeRef</span></span>](../properties/props-system-gps-altituderef.md)
</dt> </dl>

 

 
