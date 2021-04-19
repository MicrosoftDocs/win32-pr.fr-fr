---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. CameraManufacturer.
ms.assetid: 6710161c-4835-4385-9d4c-566acc000925
title: Stratégie de métadonnées de photo System. photo. CameraManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1d2765b6c787b7d7ad421300f1c3492669830b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530723"
---
# <a name="systemphotocameramanufacturer-photo-metadata-policy"></a><span data-ttu-id="4ef5c-103">Stratégie de métadonnées de photo System. photo. CameraManufacturer</span><span class="sxs-lookup"><span data-stu-id="4ef5c-103">System.Photo.CameraManufacturer Photo Metadata Policy</span></span>

<span data-ttu-id="4ef5c-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. CameraManufacturer](../properties/props-system-photo-cameramanufacturer.md) .</span><span class="sxs-lookup"><span data-stu-id="4ef5c-104">The photo metadata policy for the [System.Photo.CameraManufacturer](../properties/props-system-photo-cameramanufacturer.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="4ef5c-105">A-la</span><span class="sxs-lookup"><span data-stu-id="4ef5c-105">PKEY</span></span>

<span data-ttu-id="4ef5c-106">\_Photo \_ CameraManufacturer</span><span class="sxs-lookup"><span data-stu-id="4ef5c-106">PKEY\_Photo\_CameraManufacturer</span></span>

### <a name="containers"></a><span data-ttu-id="4ef5c-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="4ef5c-107">Containers</span></span>

<span data-ttu-id="4ef5c-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="4ef5c-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="4ef5c-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4ef5c-109">Read-Only</span></span>

<span data-ttu-id="4ef5c-110">Non</span><span class="sxs-lookup"><span data-stu-id="4ef5c-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="4ef5c-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="4ef5c-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="4ef5c-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="4ef5c-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="4ef5c-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="4ef5c-113">Input Type</span></span>

<span data-ttu-id="4ef5c-114">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="4ef5c-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="4ef5c-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="4ef5c-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="4ef5c-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="4ef5c-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="4ef5c-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="4ef5c-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="4ef5c-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="4ef5c-118">Read Paths</span></span>



| <span data-ttu-id="4ef5c-119">Commande</span><span class="sxs-lookup"><span data-stu-id="4ef5c-119">Order</span></span> | <span data-ttu-id="4ef5c-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="4ef5c-120">Path</span></span>                   | <span data-ttu-id="4ef5c-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="4ef5c-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="4ef5c-122">1</span><span class="sxs-lookup"><span data-stu-id="4ef5c-122">1</span></span>     | <span data-ttu-id="4ef5c-123">/App1/IFD/{UShort = 271}</span><span class="sxs-lookup"><span data-stu-id="4ef5c-123">/app1/ifd/{ushort=271}</span></span> | <span data-ttu-id="4ef5c-124">ascii</span><span class="sxs-lookup"><span data-stu-id="4ef5c-124">ascii</span></span>       |
| <span data-ttu-id="4ef5c-125">2</span><span class="sxs-lookup"><span data-stu-id="4ef5c-125">2</span></span>     | <span data-ttu-id="4ef5c-126">/XMP/TIFF : Make</span><span class="sxs-lookup"><span data-stu-id="4ef5c-126">/xmp/tiff:Make</span></span>         | <span data-ttu-id="4ef5c-127">unicode</span><span class="sxs-lookup"><span data-stu-id="4ef5c-127">unicode</span></span>     |
| <span data-ttu-id="4ef5c-128">3</span><span class="sxs-lookup"><span data-stu-id="4ef5c-128">3</span></span>     | <span data-ttu-id="4ef5c-129">/XMP/TIFF : Make</span><span class="sxs-lookup"><span data-stu-id="4ef5c-129">/xmp/tiff:make</span></span>         | <span data-ttu-id="4ef5c-130">unicode</span><span class="sxs-lookup"><span data-stu-id="4ef5c-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="4ef5c-131">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="4ef5c-131">Write Paths</span></span>



| <span data-ttu-id="4ef5c-132">Commande</span><span class="sxs-lookup"><span data-stu-id="4ef5c-132">Order</span></span> | <span data-ttu-id="4ef5c-133">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="4ef5c-133">Path</span></span>                   | <span data-ttu-id="4ef5c-134">Format de disque</span><span class="sxs-lookup"><span data-stu-id="4ef5c-134">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="4ef5c-135">1</span><span class="sxs-lookup"><span data-stu-id="4ef5c-135">1</span></span>     | <span data-ttu-id="4ef5c-136">/App1/IFD/{UShort = 271}</span><span class="sxs-lookup"><span data-stu-id="4ef5c-136">/app1/ifd/{ushort=271}</span></span> | <span data-ttu-id="4ef5c-137">ascii</span><span class="sxs-lookup"><span data-stu-id="4ef5c-137">ascii</span></span>       |
| <span data-ttu-id="4ef5c-138">2</span><span class="sxs-lookup"><span data-stu-id="4ef5c-138">2</span></span>     | <span data-ttu-id="4ef5c-139">/XMP/TIFF : Make</span><span class="sxs-lookup"><span data-stu-id="4ef5c-139">/xmp/tiff:Make</span></span>         | <span data-ttu-id="4ef5c-140">unicode</span><span class="sxs-lookup"><span data-stu-id="4ef5c-140">unicode</span></span>     |
| <span data-ttu-id="4ef5c-141">3</span><span class="sxs-lookup"><span data-stu-id="4ef5c-141">3</span></span>     | <span data-ttu-id="4ef5c-142">/XMP/TIFF : Make</span><span class="sxs-lookup"><span data-stu-id="4ef5c-142">/xmp/tiff:make</span></span>         | <span data-ttu-id="4ef5c-143">unicode</span><span class="sxs-lookup"><span data-stu-id="4ef5c-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="4ef5c-144">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="4ef5c-144">Remove Paths</span></span>



| <span data-ttu-id="4ef5c-145">Commande</span><span class="sxs-lookup"><span data-stu-id="4ef5c-145">Order</span></span> | <span data-ttu-id="4ef5c-146">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="4ef5c-146">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="4ef5c-147">1</span><span class="sxs-lookup"><span data-stu-id="4ef5c-147">1</span></span>     | <span data-ttu-id="4ef5c-148">/App1/IFD/{UShort = 271}</span><span class="sxs-lookup"><span data-stu-id="4ef5c-148">/app1/ifd/{ushort=271}</span></span> |
| <span data-ttu-id="4ef5c-149">2</span><span class="sxs-lookup"><span data-stu-id="4ef5c-149">2</span></span>     | <span data-ttu-id="4ef5c-150">/XMP/TIFF : Make</span><span class="sxs-lookup"><span data-stu-id="4ef5c-150">/xmp/tiff:Make</span></span>         |
| <span data-ttu-id="4ef5c-151">3</span><span class="sxs-lookup"><span data-stu-id="4ef5c-151">3</span></span>     | <span data-ttu-id="4ef5c-152">/XMP/TIFF : Make</span><span class="sxs-lookup"><span data-stu-id="4ef5c-152">/xmp/tiff:make</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="4ef5c-153">Stratégie TIFF</span><span class="sxs-lookup"><span data-stu-id="4ef5c-153">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="4ef5c-154">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="4ef5c-154">Read Paths</span></span>



| <span data-ttu-id="4ef5c-155">Commande</span><span class="sxs-lookup"><span data-stu-id="4ef5c-155">Order</span></span> | <span data-ttu-id="4ef5c-156">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="4ef5c-156">Path</span></span>               | <span data-ttu-id="4ef5c-157">Format de disque</span><span class="sxs-lookup"><span data-stu-id="4ef5c-157">Disk Format</span></span> |
|-------|--------------------|-------------|
| <span data-ttu-id="4ef5c-158">1</span><span class="sxs-lookup"><span data-stu-id="4ef5c-158">1</span></span>     | <span data-ttu-id="4ef5c-159">/IFD/{UShort = 271}</span><span class="sxs-lookup"><span data-stu-id="4ef5c-159">/ifd/{ushort=271}</span></span>  | <span data-ttu-id="4ef5c-160">ascii</span><span class="sxs-lookup"><span data-stu-id="4ef5c-160">ascii</span></span>       |
| <span data-ttu-id="4ef5c-161">2</span><span class="sxs-lookup"><span data-stu-id="4ef5c-161">2</span></span>     | <span data-ttu-id="4ef5c-162">/IFD/XMP/TIFF : Make</span><span class="sxs-lookup"><span data-stu-id="4ef5c-162">/ifd/xmp/tiff:Make</span></span> | <span data-ttu-id="4ef5c-163">unicode</span><span class="sxs-lookup"><span data-stu-id="4ef5c-163">unicode</span></span>     |
| <span data-ttu-id="4ef5c-164">3</span><span class="sxs-lookup"><span data-stu-id="4ef5c-164">3</span></span>     | <span data-ttu-id="4ef5c-165">/IFD/XMP/TIFF : Make</span><span class="sxs-lookup"><span data-stu-id="4ef5c-165">/ifd/xmp/tiff:make</span></span> | <span data-ttu-id="4ef5c-166">unicode</span><span class="sxs-lookup"><span data-stu-id="4ef5c-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="4ef5c-167">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="4ef5c-167">Write Paths</span></span>



| <span data-ttu-id="4ef5c-168">Commande</span><span class="sxs-lookup"><span data-stu-id="4ef5c-168">Order</span></span> | <span data-ttu-id="4ef5c-169">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="4ef5c-169">Path</span></span>               | <span data-ttu-id="4ef5c-170">Format de disque</span><span class="sxs-lookup"><span data-stu-id="4ef5c-170">Disk Format</span></span> |
|-------|--------------------|-------------|
| <span data-ttu-id="4ef5c-171">1</span><span class="sxs-lookup"><span data-stu-id="4ef5c-171">1</span></span>     | <span data-ttu-id="4ef5c-172">/IFD/{UShort = 271}</span><span class="sxs-lookup"><span data-stu-id="4ef5c-172">/ifd/{ushort=271}</span></span>  | <span data-ttu-id="4ef5c-173">ascii</span><span class="sxs-lookup"><span data-stu-id="4ef5c-173">ascii</span></span>       |
| <span data-ttu-id="4ef5c-174">2</span><span class="sxs-lookup"><span data-stu-id="4ef5c-174">2</span></span>     | <span data-ttu-id="4ef5c-175">/IFD/XMP/TIFF : Make</span><span class="sxs-lookup"><span data-stu-id="4ef5c-175">/ifd/xmp/tiff:Make</span></span> | <span data-ttu-id="4ef5c-176">unicode</span><span class="sxs-lookup"><span data-stu-id="4ef5c-176">unicode</span></span>     |
| <span data-ttu-id="4ef5c-177">3</span><span class="sxs-lookup"><span data-stu-id="4ef5c-177">3</span></span>     | <span data-ttu-id="4ef5c-178">/IFD/XMP/TIFF : Make</span><span class="sxs-lookup"><span data-stu-id="4ef5c-178">/ifd/xmp/tiff:make</span></span> | <span data-ttu-id="4ef5c-179">unicode</span><span class="sxs-lookup"><span data-stu-id="4ef5c-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="4ef5c-180">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="4ef5c-180">Remove Paths</span></span>



| <span data-ttu-id="4ef5c-181">Commande</span><span class="sxs-lookup"><span data-stu-id="4ef5c-181">Order</span></span> | <span data-ttu-id="4ef5c-182">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="4ef5c-182">Path</span></span>               |
|-------|--------------------|
| <span data-ttu-id="4ef5c-183">1</span><span class="sxs-lookup"><span data-stu-id="4ef5c-183">1</span></span>     | <span data-ttu-id="4ef5c-184">/IFD/{UShort = 271}</span><span class="sxs-lookup"><span data-stu-id="4ef5c-184">/ifd/{ushort=271}</span></span>  |
| <span data-ttu-id="4ef5c-185">2</span><span class="sxs-lookup"><span data-stu-id="4ef5c-185">2</span></span>     | <span data-ttu-id="4ef5c-186">/IFD/XMP/TIFF : Make</span><span class="sxs-lookup"><span data-stu-id="4ef5c-186">/ifd/xmp/tiff:Make</span></span> |
| <span data-ttu-id="4ef5c-187">3</span><span class="sxs-lookup"><span data-stu-id="4ef5c-187">3</span></span>     | <span data-ttu-id="4ef5c-188">/IFD/XMP/TIFF : Make</span><span class="sxs-lookup"><span data-stu-id="4ef5c-188">/ifd/xmp/tiff:make</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4ef5c-189">Notes</span><span class="sxs-lookup"><span data-stu-id="4ef5c-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ef5c-190">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4ef5c-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ef5c-191">System. photo. CameraManufacturer</span><span class="sxs-lookup"><span data-stu-id="4ef5c-191">System.Photo.CameraManufacturer</span></span>](../properties/props-system-photo-cameramanufacturer.md)
</dt> </dl>

 

 
