---
description: La stratégie de métadonnées de la photo pour la propriété System. GPS. satellites.
ms.assetid: 5dbbbeaf-e67d-45f6-95b2-de3287202d41
title: Stratégie de métadonnées de photos System. GPS. satellites
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980393accdb1bee3d2a44dd539f3c9fb169c648b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519145"
---
# <a name="systemgpssatellites-photo-metadata-policy"></a><span data-ttu-id="1bf6c-103">Stratégie de métadonnées de photos System. GPS. satellites</span><span class="sxs-lookup"><span data-stu-id="1bf6c-103">System.GPS.Satellites Photo Metadata Policy</span></span>

<span data-ttu-id="1bf6c-104">La stratégie de métadonnées de la photo pour la propriété [System. GPS. satellites](../properties/props-system-gps-satellites.md) .</span><span class="sxs-lookup"><span data-stu-id="1bf6c-104">The photo metadata policy for the [System.GPS.Satellites](../properties/props-system-gps-satellites.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="1bf6c-105">A-la</span><span class="sxs-lookup"><span data-stu-id="1bf6c-105">PKEY</span></span>

<span data-ttu-id="1bf6c-106">\_Satellites GPS \_</span><span class="sxs-lookup"><span data-stu-id="1bf6c-106">PKEY\_GPS\_Satellites</span></span>

### <a name="containers"></a><span data-ttu-id="1bf6c-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="1bf6c-107">Containers</span></span>

<span data-ttu-id="1bf6c-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="1bf6c-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="1bf6c-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1bf6c-109">Read-Only</span></span>

<span data-ttu-id="1bf6c-110">Non</span><span class="sxs-lookup"><span data-stu-id="1bf6c-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="1bf6c-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="1bf6c-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="1bf6c-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="1bf6c-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="1bf6c-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="1bf6c-113">Input Type</span></span>

<span data-ttu-id="1bf6c-114">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="1bf6c-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="1bf6c-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="1bf6c-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="1bf6c-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="1bf6c-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="1bf6c-117">Stratégies JPEG</span><span class="sxs-lookup"><span data-stu-id="1bf6c-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="1bf6c-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="1bf6c-118">Read Paths</span></span>



| <span data-ttu-id="1bf6c-119">Commande</span><span class="sxs-lookup"><span data-stu-id="1bf6c-119">Order</span></span> | <span data-ttu-id="1bf6c-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1bf6c-120">Path</span></span>                     | <span data-ttu-id="1bf6c-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="1bf6c-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="1bf6c-122">1</span><span class="sxs-lookup"><span data-stu-id="1bf6c-122">1</span></span>     | <span data-ttu-id="1bf6c-123">/App1/IFD/GPS/{UShort = 8}</span><span class="sxs-lookup"><span data-stu-id="1bf6c-123">/app1/ifd/gps/{ushort=8}</span></span> | <span data-ttu-id="1bf6c-124">ascii</span><span class="sxs-lookup"><span data-stu-id="1bf6c-124">ascii</span></span>       |
| <span data-ttu-id="1bf6c-125">2</span><span class="sxs-lookup"><span data-stu-id="1bf6c-125">2</span></span>     | <span data-ttu-id="1bf6c-126">/xmp/exif:GPSSatellites</span><span class="sxs-lookup"><span data-stu-id="1bf6c-126">/xmp/exif:GPSSatellites</span></span>  | <span data-ttu-id="1bf6c-127">unicode</span><span class="sxs-lookup"><span data-stu-id="1bf6c-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="1bf6c-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="1bf6c-128">Write Paths</span></span>



| <span data-ttu-id="1bf6c-129">Commande</span><span class="sxs-lookup"><span data-stu-id="1bf6c-129">Order</span></span> | <span data-ttu-id="1bf6c-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1bf6c-130">Path</span></span>                     | <span data-ttu-id="1bf6c-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="1bf6c-131">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="1bf6c-132">1</span><span class="sxs-lookup"><span data-stu-id="1bf6c-132">1</span></span>     | <span data-ttu-id="1bf6c-133">/App1/IFD/GPS/{UShort = 8}</span><span class="sxs-lookup"><span data-stu-id="1bf6c-133">/app1/ifd/gps/{ushort=8}</span></span> | <span data-ttu-id="1bf6c-134">ascii</span><span class="sxs-lookup"><span data-stu-id="1bf6c-134">ascii</span></span>       |
| <span data-ttu-id="1bf6c-135">2</span><span class="sxs-lookup"><span data-stu-id="1bf6c-135">2</span></span>     | <span data-ttu-id="1bf6c-136">/xmp/exif:GPSSatellites</span><span class="sxs-lookup"><span data-stu-id="1bf6c-136">/xmp/exif:GPSSatellites</span></span>  | <span data-ttu-id="1bf6c-137">unicode</span><span class="sxs-lookup"><span data-stu-id="1bf6c-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="1bf6c-138">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="1bf6c-138">Remove Paths</span></span>



| <span data-ttu-id="1bf6c-139">Commande</span><span class="sxs-lookup"><span data-stu-id="1bf6c-139">Order</span></span> | <span data-ttu-id="1bf6c-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1bf6c-140">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="1bf6c-141">1</span><span class="sxs-lookup"><span data-stu-id="1bf6c-141">1</span></span>     | <span data-ttu-id="1bf6c-142">/App1/IFD/GPS/{UShort = 8}</span><span class="sxs-lookup"><span data-stu-id="1bf6c-142">/app1/ifd/gps/{ushort=8}</span></span> |
| <span data-ttu-id="1bf6c-143">2</span><span class="sxs-lookup"><span data-stu-id="1bf6c-143">2</span></span>     | <span data-ttu-id="1bf6c-144">/xmp/exif:gpssatellites</span><span class="sxs-lookup"><span data-stu-id="1bf6c-144">/xmp/exif:gpssatellites</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="1bf6c-145">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="1bf6c-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="1bf6c-146">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="1bf6c-146">Read Paths</span></span>



| <span data-ttu-id="1bf6c-147">Commande</span><span class="sxs-lookup"><span data-stu-id="1bf6c-147">Order</span></span> | <span data-ttu-id="1bf6c-148">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1bf6c-148">Path</span></span>                        | <span data-ttu-id="1bf6c-149">Format de disque</span><span class="sxs-lookup"><span data-stu-id="1bf6c-149">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="1bf6c-150">1</span><span class="sxs-lookup"><span data-stu-id="1bf6c-150">1</span></span>     | <span data-ttu-id="1bf6c-151">/IFD/GPS/{UShort = 8}</span><span class="sxs-lookup"><span data-stu-id="1bf6c-151">/ifd/gps/{ushort=8}</span></span>         | <span data-ttu-id="1bf6c-152">ascii</span><span class="sxs-lookup"><span data-stu-id="1bf6c-152">ascii</span></span>       |
| <span data-ttu-id="1bf6c-153">2</span><span class="sxs-lookup"><span data-stu-id="1bf6c-153">2</span></span>     | <span data-ttu-id="1bf6c-154">/ifd/xmp/exif:GPSSatellites</span><span class="sxs-lookup"><span data-stu-id="1bf6c-154">/ifd/xmp/exif:GPSSatellites</span></span> | <span data-ttu-id="1bf6c-155">unicode</span><span class="sxs-lookup"><span data-stu-id="1bf6c-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="1bf6c-156">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="1bf6c-156">Write Paths</span></span>



| <span data-ttu-id="1bf6c-157">Commande</span><span class="sxs-lookup"><span data-stu-id="1bf6c-157">Order</span></span> | <span data-ttu-id="1bf6c-158">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1bf6c-158">Path</span></span>                        | <span data-ttu-id="1bf6c-159">Format de disque</span><span class="sxs-lookup"><span data-stu-id="1bf6c-159">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="1bf6c-160">1</span><span class="sxs-lookup"><span data-stu-id="1bf6c-160">1</span></span>     | <span data-ttu-id="1bf6c-161">/IFD/GPS/{UShort = 8}</span><span class="sxs-lookup"><span data-stu-id="1bf6c-161">/ifd/gps/{ushort=8}</span></span>         | <span data-ttu-id="1bf6c-162">ascii</span><span class="sxs-lookup"><span data-stu-id="1bf6c-162">ascii</span></span>       |
| <span data-ttu-id="1bf6c-163">2</span><span class="sxs-lookup"><span data-stu-id="1bf6c-163">2</span></span>     | <span data-ttu-id="1bf6c-164">/ifd/xmp/exif:GPSSatellites</span><span class="sxs-lookup"><span data-stu-id="1bf6c-164">/ifd/xmp/exif:GPSSatellites</span></span> | <span data-ttu-id="1bf6c-165">unicode</span><span class="sxs-lookup"><span data-stu-id="1bf6c-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="1bf6c-166">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="1bf6c-166">Remove Paths</span></span>



| <span data-ttu-id="1bf6c-167">Commande</span><span class="sxs-lookup"><span data-stu-id="1bf6c-167">Order</span></span> | <span data-ttu-id="1bf6c-168">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1bf6c-168">Path</span></span>                        |
|-------|-----------------------------|
| <span data-ttu-id="1bf6c-169">1</span><span class="sxs-lookup"><span data-stu-id="1bf6c-169">1</span></span>     | <span data-ttu-id="1bf6c-170">/IFD/GPS/{UShort = 8}</span><span class="sxs-lookup"><span data-stu-id="1bf6c-170">/ifd/gps/{ushort=8}</span></span>         |
| <span data-ttu-id="1bf6c-171">2</span><span class="sxs-lookup"><span data-stu-id="1bf6c-171">2</span></span>     | <span data-ttu-id="1bf6c-172">/ifd/xmp/exif:gpssatellites</span><span class="sxs-lookup"><span data-stu-id="1bf6c-172">/ifd/xmp/exif:gpssatellites</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1bf6c-173">Notes</span><span class="sxs-lookup"><span data-stu-id="1bf6c-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="1bf6c-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1bf6c-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bf6c-175">System. GPS. satellites</span><span class="sxs-lookup"><span data-stu-id="1bf6c-175">System.GPS.Satellites</span></span>](../properties/props-system-gps-satellites.md)
</dt> </dl>

 

 
