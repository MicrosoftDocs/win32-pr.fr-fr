---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. ImgDirectionRef.
ms.assetid: 74ae0989-6d53-4d72-abe9-84f40c0c884a
title: Stratégie de métadonnées de photo System. GPS. ImgDirectionRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80276ca8d1981935004dbec49fef588fcde330ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210279"
---
# <a name="systemgpsimgdirectionref-photo-metadata-policy"></a><span data-ttu-id="fcdea-103">Stratégie de métadonnées de photo System. GPS. ImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="fcdea-103">System.GPS.ImgDirectionRef Photo Metadata Policy</span></span>

<span data-ttu-id="fcdea-104">Stratégie de métadonnées de la photo pour la propriété [System. GPS. ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md) .</span><span class="sxs-lookup"><span data-stu-id="fcdea-104">The photo metadata policy for the [System.GPS.ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="fcdea-105">A-la</span><span class="sxs-lookup"><span data-stu-id="fcdea-105">PKEY</span></span>

<span data-ttu-id="fcdea-106">\_GPS. ImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="fcdea-106">PKEY\_GPS.ImgDirectionRef</span></span>

### <a name="containers"></a><span data-ttu-id="fcdea-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="fcdea-107">Containers</span></span>

<span data-ttu-id="fcdea-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="fcdea-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="fcdea-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fcdea-109">Read-Only</span></span>

<span data-ttu-id="fcdea-110">Non</span><span class="sxs-lookup"><span data-stu-id="fcdea-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="fcdea-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="fcdea-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="fcdea-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="fcdea-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="fcdea-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="fcdea-113">Input Type</span></span>

<span data-ttu-id="fcdea-114">VT \_ LPWStr est préféré, mais VT \_ LPSTR est également accepté.</span><span class="sxs-lookup"><span data-stu-id="fcdea-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="fcdea-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="fcdea-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="fcdea-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="fcdea-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="fcdea-117">Stratégies JPEG</span><span class="sxs-lookup"><span data-stu-id="fcdea-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="fcdea-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="fcdea-118">Read Paths</span></span>



| <span data-ttu-id="fcdea-119">Commande</span><span class="sxs-lookup"><span data-stu-id="fcdea-119">Order</span></span> | <span data-ttu-id="fcdea-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="fcdea-120">Path</span></span>                         | <span data-ttu-id="fcdea-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="fcdea-121">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="fcdea-122">1</span><span class="sxs-lookup"><span data-stu-id="fcdea-122">1</span></span>     | <span data-ttu-id="fcdea-123">/App1/IFD/GPS/{UShort = 16}</span><span class="sxs-lookup"><span data-stu-id="fcdea-123">/app1/ifd/gps/{ushort=16}</span></span>    | <span data-ttu-id="fcdea-124">ascii</span><span class="sxs-lookup"><span data-stu-id="fcdea-124">ascii</span></span>       |
| <span data-ttu-id="fcdea-125">2</span><span class="sxs-lookup"><span data-stu-id="fcdea-125">2</span></span>     | <span data-ttu-id="fcdea-126">/xmp/exif:GPSImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="fcdea-126">/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="fcdea-127">unicode</span><span class="sxs-lookup"><span data-stu-id="fcdea-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="fcdea-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="fcdea-128">Write Paths</span></span>



| <span data-ttu-id="fcdea-129">Commande</span><span class="sxs-lookup"><span data-stu-id="fcdea-129">Order</span></span> | <span data-ttu-id="fcdea-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="fcdea-130">Path</span></span>                         | <span data-ttu-id="fcdea-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="fcdea-131">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="fcdea-132">1</span><span class="sxs-lookup"><span data-stu-id="fcdea-132">1</span></span>     | <span data-ttu-id="fcdea-133">/App1/IFD/GPS/{UShort = 16}</span><span class="sxs-lookup"><span data-stu-id="fcdea-133">/app1/ifd/gps/{ushort=16}</span></span>    | <span data-ttu-id="fcdea-134">ascii</span><span class="sxs-lookup"><span data-stu-id="fcdea-134">ascii</span></span>       |
| <span data-ttu-id="fcdea-135">2</span><span class="sxs-lookup"><span data-stu-id="fcdea-135">2</span></span>     | <span data-ttu-id="fcdea-136">/xmp/exif:GPSImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="fcdea-136">/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="fcdea-137">unicode</span><span class="sxs-lookup"><span data-stu-id="fcdea-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="fcdea-138">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="fcdea-138">Remove Paths</span></span>



| <span data-ttu-id="fcdea-139">Commande</span><span class="sxs-lookup"><span data-stu-id="fcdea-139">Order</span></span> | <span data-ttu-id="fcdea-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="fcdea-140">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="fcdea-141">1</span><span class="sxs-lookup"><span data-stu-id="fcdea-141">1</span></span>     | <span data-ttu-id="fcdea-142">/App1/IFD/GPS/{UShort = 16}</span><span class="sxs-lookup"><span data-stu-id="fcdea-142">/app1/ifd/gps/{ushort=16}</span></span>    |
| <span data-ttu-id="fcdea-143">2</span><span class="sxs-lookup"><span data-stu-id="fcdea-143">2</span></span>     | <span data-ttu-id="fcdea-144">/xmp/exif:gpsimgdirectionref</span><span class="sxs-lookup"><span data-stu-id="fcdea-144">/xmp/exif:gpsimgdirectionref</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="fcdea-145">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="fcdea-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="fcdea-146">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="fcdea-146">Read Paths</span></span>



| <span data-ttu-id="fcdea-147">Commande</span><span class="sxs-lookup"><span data-stu-id="fcdea-147">Order</span></span> | <span data-ttu-id="fcdea-148">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="fcdea-148">Path</span></span>                             | <span data-ttu-id="fcdea-149">Format de disque</span><span class="sxs-lookup"><span data-stu-id="fcdea-149">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="fcdea-150">1</span><span class="sxs-lookup"><span data-stu-id="fcdea-150">1</span></span>     | <span data-ttu-id="fcdea-151">/IFD/GPS/{UShort = 16}</span><span class="sxs-lookup"><span data-stu-id="fcdea-151">/ifd/gps/{ushort=16}</span></span>             | <span data-ttu-id="fcdea-152">ascii</span><span class="sxs-lookup"><span data-stu-id="fcdea-152">ascii</span></span>       |
| <span data-ttu-id="fcdea-153">2</span><span class="sxs-lookup"><span data-stu-id="fcdea-153">2</span></span>     | <span data-ttu-id="fcdea-154">/ifd/xmp/exif:GPSImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="fcdea-154">/ifd/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="fcdea-155">unicode</span><span class="sxs-lookup"><span data-stu-id="fcdea-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="fcdea-156">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="fcdea-156">Write Paths</span></span>



| <span data-ttu-id="fcdea-157">Commande</span><span class="sxs-lookup"><span data-stu-id="fcdea-157">Order</span></span> | <span data-ttu-id="fcdea-158">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="fcdea-158">Path</span></span>                             | <span data-ttu-id="fcdea-159">Format de disque</span><span class="sxs-lookup"><span data-stu-id="fcdea-159">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="fcdea-160">1</span><span class="sxs-lookup"><span data-stu-id="fcdea-160">1</span></span>     | <span data-ttu-id="fcdea-161">/IFD/GPS/{UShort = 16}</span><span class="sxs-lookup"><span data-stu-id="fcdea-161">/ifd/gps/{ushort=16}</span></span>             | <span data-ttu-id="fcdea-162">ascii</span><span class="sxs-lookup"><span data-stu-id="fcdea-162">ascii</span></span>       |
| <span data-ttu-id="fcdea-163">2</span><span class="sxs-lookup"><span data-stu-id="fcdea-163">2</span></span>     | <span data-ttu-id="fcdea-164">/ifd/xmp/exif:GPSImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="fcdea-164">/ifd/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="fcdea-165">unicode</span><span class="sxs-lookup"><span data-stu-id="fcdea-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="fcdea-166">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="fcdea-166">Remove Paths</span></span>



| <span data-ttu-id="fcdea-167">Commande</span><span class="sxs-lookup"><span data-stu-id="fcdea-167">Order</span></span> | <span data-ttu-id="fcdea-168">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="fcdea-168">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="fcdea-169">1</span><span class="sxs-lookup"><span data-stu-id="fcdea-169">1</span></span>     | <span data-ttu-id="fcdea-170">/IFD/GPS/{UShort = 16}</span><span class="sxs-lookup"><span data-stu-id="fcdea-170">/ifd/gps/{ushort=16}</span></span>             |
| <span data-ttu-id="fcdea-171">2</span><span class="sxs-lookup"><span data-stu-id="fcdea-171">2</span></span>     | <span data-ttu-id="fcdea-172">/ifd/xmp/exif:gpsimgdirectionref</span><span class="sxs-lookup"><span data-stu-id="fcdea-172">/ifd/xmp/exif:gpsimgdirectionref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fcdea-173">Notes</span><span class="sxs-lookup"><span data-stu-id="fcdea-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="fcdea-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fcdea-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcdea-175">System. GPS. ImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="fcdea-175">System.GPS.ImgDirectionRef</span></span>](../properties/props-system-gps-imgdirectionref.md)
</dt> </dl>

 

 
