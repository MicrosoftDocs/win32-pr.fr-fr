---
description: La stratégie de métadonnées de la photo pour la propriété System. GPS. Status.
ms.assetid: 74ea0384-3b1f-4d5e-8713-7b3936813a3a
title: Stratégie de métadonnées de photo System. GPS. Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac08139a267052f8d6dd3dc463e2a2768309a41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522026"
---
# <a name="systemgpsstatus-photo-metadata-policy"></a><span data-ttu-id="aa125-103">Stratégie de métadonnées de photo System. GPS. Status</span><span class="sxs-lookup"><span data-stu-id="aa125-103">System.GPS.Status Photo Metadata Policy</span></span>

<span data-ttu-id="aa125-104">La stratégie de métadonnées de la photo pour la propriété [System. GPS. Status](../properties/props-system-gps-status.md) .</span><span class="sxs-lookup"><span data-stu-id="aa125-104">The photo metadata policy for the [System.GPS.Status](../properties/props-system-gps-status.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="aa125-105">A-la</span><span class="sxs-lookup"><span data-stu-id="aa125-105">PKEY</span></span>

<span data-ttu-id="aa125-106">\_État du GPS \_</span><span class="sxs-lookup"><span data-stu-id="aa125-106">PKEY\_GPS\_Status</span></span>

### <a name="containers"></a><span data-ttu-id="aa125-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="aa125-107">Containers</span></span>

<span data-ttu-id="aa125-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="aa125-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="aa125-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aa125-109">Read-Only</span></span>

<span data-ttu-id="aa125-110">Non</span><span class="sxs-lookup"><span data-stu-id="aa125-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="aa125-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="aa125-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="aa125-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="aa125-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="aa125-113">Type de PROPVARIANT d’entrée</span><span class="sxs-lookup"><span data-stu-id="aa125-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="aa125-114">VT \_ LPWStr est préféré, mais VT \_ LPSTR est également accepté.</span><span class="sxs-lookup"><span data-stu-id="aa125-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="aa125-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="aa125-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="aa125-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="aa125-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="aa125-117">Stratégies JPEG</span><span class="sxs-lookup"><span data-stu-id="aa125-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="aa125-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="aa125-118">Read Paths</span></span>



| <span data-ttu-id="aa125-119">Commande</span><span class="sxs-lookup"><span data-stu-id="aa125-119">Order</span></span> | <span data-ttu-id="aa125-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="aa125-120">Path</span></span>                     | <span data-ttu-id="aa125-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="aa125-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="aa125-122">1</span><span class="sxs-lookup"><span data-stu-id="aa125-122">1</span></span>     | <span data-ttu-id="aa125-123">/App1/IFD/GPS/{UShort = 9}</span><span class="sxs-lookup"><span data-stu-id="aa125-123">/app1/ifd/gps/{ushort=9}</span></span> | <span data-ttu-id="aa125-124">ascii</span><span class="sxs-lookup"><span data-stu-id="aa125-124">ascii</span></span>       |
| <span data-ttu-id="aa125-125">2</span><span class="sxs-lookup"><span data-stu-id="aa125-125">2</span></span>     | <span data-ttu-id="aa125-126">/xmp/exif:GPSStatus</span><span class="sxs-lookup"><span data-stu-id="aa125-126">/xmp/exif:GPSStatus</span></span>      | <span data-ttu-id="aa125-127">unicode</span><span class="sxs-lookup"><span data-stu-id="aa125-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="aa125-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="aa125-128">Write Paths</span></span>



| <span data-ttu-id="aa125-129">Commande</span><span class="sxs-lookup"><span data-stu-id="aa125-129">Order</span></span> | <span data-ttu-id="aa125-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="aa125-130">Path</span></span>                     | <span data-ttu-id="aa125-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="aa125-131">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="aa125-132">1</span><span class="sxs-lookup"><span data-stu-id="aa125-132">1</span></span>     | <span data-ttu-id="aa125-133">/App1/IFD/GPS/{UShort = 9}</span><span class="sxs-lookup"><span data-stu-id="aa125-133">/app1/ifd/gps/{ushort=9}</span></span> | <span data-ttu-id="aa125-134">ascii</span><span class="sxs-lookup"><span data-stu-id="aa125-134">ascii</span></span>       |
| <span data-ttu-id="aa125-135">2</span><span class="sxs-lookup"><span data-stu-id="aa125-135">2</span></span>     | <span data-ttu-id="aa125-136">/xmp/exif:GPSStatus</span><span class="sxs-lookup"><span data-stu-id="aa125-136">/xmp/exif:GPSStatus</span></span>      | <span data-ttu-id="aa125-137">unicode</span><span class="sxs-lookup"><span data-stu-id="aa125-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="aa125-138">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="aa125-138">Remove Paths</span></span>



| <span data-ttu-id="aa125-139">Commande</span><span class="sxs-lookup"><span data-stu-id="aa125-139">Order</span></span> | <span data-ttu-id="aa125-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="aa125-140">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="aa125-141">1</span><span class="sxs-lookup"><span data-stu-id="aa125-141">1</span></span>     | <span data-ttu-id="aa125-142">/App1/IFD/GPS/{UShort = 9}</span><span class="sxs-lookup"><span data-stu-id="aa125-142">/app1/ifd/gps/{ushort=9}</span></span> |
| <span data-ttu-id="aa125-143">2</span><span class="sxs-lookup"><span data-stu-id="aa125-143">2</span></span>     | <span data-ttu-id="aa125-144">/xmp/exif:gpsstatus</span><span class="sxs-lookup"><span data-stu-id="aa125-144">/xmp/exif:gpsstatus</span></span>      |



 

### <a name="tiff-policies"></a><span data-ttu-id="aa125-145">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="aa125-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="aa125-146">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="aa125-146">Read Paths</span></span>



| <span data-ttu-id="aa125-147">Commande</span><span class="sxs-lookup"><span data-stu-id="aa125-147">Order</span></span> | <span data-ttu-id="aa125-148">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="aa125-148">Path</span></span>                    | <span data-ttu-id="aa125-149">Format de disque</span><span class="sxs-lookup"><span data-stu-id="aa125-149">Disk Format</span></span> |
|-------|-------------------------|-------------|
| <span data-ttu-id="aa125-150">1</span><span class="sxs-lookup"><span data-stu-id="aa125-150">1</span></span>     | <span data-ttu-id="aa125-151">/IFD/GPS/{UShort = 9}</span><span class="sxs-lookup"><span data-stu-id="aa125-151">/ifd/gps/{ushort=9}</span></span>     | <span data-ttu-id="aa125-152">ascii</span><span class="sxs-lookup"><span data-stu-id="aa125-152">ascii</span></span>       |
| <span data-ttu-id="aa125-153">2</span><span class="sxs-lookup"><span data-stu-id="aa125-153">2</span></span>     | <span data-ttu-id="aa125-154">/ifd/xmp/exif:GPSStatus</span><span class="sxs-lookup"><span data-stu-id="aa125-154">/ifd/xmp/exif:GPSStatus</span></span> | <span data-ttu-id="aa125-155">unicode</span><span class="sxs-lookup"><span data-stu-id="aa125-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="aa125-156">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="aa125-156">Write Paths</span></span>



| <span data-ttu-id="aa125-157">Commande</span><span class="sxs-lookup"><span data-stu-id="aa125-157">Order</span></span> | <span data-ttu-id="aa125-158">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="aa125-158">Path</span></span>                    | <span data-ttu-id="aa125-159">Format de disque</span><span class="sxs-lookup"><span data-stu-id="aa125-159">Disk Format</span></span> |
|-------|-------------------------|-------------|
| <span data-ttu-id="aa125-160">1</span><span class="sxs-lookup"><span data-stu-id="aa125-160">1</span></span>     | <span data-ttu-id="aa125-161">/IFD/GPS/{UShort = 9}</span><span class="sxs-lookup"><span data-stu-id="aa125-161">/ifd/gps/{ushort=9}</span></span>     | <span data-ttu-id="aa125-162">ascii</span><span class="sxs-lookup"><span data-stu-id="aa125-162">ascii</span></span>       |
| <span data-ttu-id="aa125-163">2</span><span class="sxs-lookup"><span data-stu-id="aa125-163">2</span></span>     | <span data-ttu-id="aa125-164">/ifd/xmp/exif:GPSStatus</span><span class="sxs-lookup"><span data-stu-id="aa125-164">/ifd/xmp/exif:GPSStatus</span></span> | <span data-ttu-id="aa125-165">unicode</span><span class="sxs-lookup"><span data-stu-id="aa125-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="aa125-166">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="aa125-166">Remove Paths</span></span>



| <span data-ttu-id="aa125-167">Commande</span><span class="sxs-lookup"><span data-stu-id="aa125-167">Order</span></span> | <span data-ttu-id="aa125-168">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="aa125-168">Path</span></span>                    |
|-------|-------------------------|
| <span data-ttu-id="aa125-169">1</span><span class="sxs-lookup"><span data-stu-id="aa125-169">1</span></span>     | <span data-ttu-id="aa125-170">/IFD/GPS/{UShort = 9}</span><span class="sxs-lookup"><span data-stu-id="aa125-170">/ifd/gps/{ushort=9}</span></span>     |
| <span data-ttu-id="aa125-171">2</span><span class="sxs-lookup"><span data-stu-id="aa125-171">2</span></span>     | <span data-ttu-id="aa125-172">/ifd/xmp/exif:gpsstatus</span><span class="sxs-lookup"><span data-stu-id="aa125-172">/ifd/xmp/exif:gpsstatus</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="aa125-173">Notes</span><span class="sxs-lookup"><span data-stu-id="aa125-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa125-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aa125-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa125-175">System. GPS. Status</span><span class="sxs-lookup"><span data-stu-id="aa125-175">System.GPS.Status</span></span>](../properties/props-system-gps-status.md)
</dt> </dl>

 

 
