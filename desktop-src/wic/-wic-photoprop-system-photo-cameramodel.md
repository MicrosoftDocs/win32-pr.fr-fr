---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. CameraModel.
ms.assetid: ff85e6ee-dc75-45bc-a406-2290b012c22d
title: Stratégie de métadonnées de photo System. photo. CameraModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cf9cbb2906f15d02e8d72219862c607d0f515a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868005"
---
# <a name="systemphotocameramodel-photo-metadata-policy"></a><span data-ttu-id="1e374-103">Stratégie de métadonnées de photo System. photo. CameraModel</span><span class="sxs-lookup"><span data-stu-id="1e374-103">System.Photo.CameraModel Photo Metadata Policy</span></span>

<span data-ttu-id="1e374-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. CameraModel](../properties/props-system-photo-cameramodel.md) .</span><span class="sxs-lookup"><span data-stu-id="1e374-104">The photo metadata policy for the [System.Photo.CameraModel](../properties/props-system-photo-cameramodel.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="1e374-105">A-la</span><span class="sxs-lookup"><span data-stu-id="1e374-105">PKEY</span></span>

<span data-ttu-id="1e374-106">\_Photo \_ CameraModel</span><span class="sxs-lookup"><span data-stu-id="1e374-106">PKEY\_Photo\_CameraModel</span></span>

### <a name="containers"></a><span data-ttu-id="1e374-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="1e374-107">Containers</span></span>

<span data-ttu-id="1e374-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="1e374-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="1e374-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e374-109">Read-Only</span></span>

<span data-ttu-id="1e374-110">Non</span><span class="sxs-lookup"><span data-stu-id="1e374-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="1e374-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="1e374-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="1e374-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="1e374-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="1e374-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="1e374-113">Input Type</span></span>

<span data-ttu-id="1e374-114">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="1e374-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="1e374-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="1e374-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="1e374-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="1e374-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="1e374-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="1e374-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="1e374-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="1e374-118">Read Paths</span></span>



| <span data-ttu-id="1e374-119">Commande</span><span class="sxs-lookup"><span data-stu-id="1e374-119">Order</span></span> | <span data-ttu-id="1e374-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1e374-120">Path</span></span>                   | <span data-ttu-id="1e374-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="1e374-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="1e374-122">1</span><span class="sxs-lookup"><span data-stu-id="1e374-122">1</span></span>     | <span data-ttu-id="1e374-123">/App1/IFD/{UShort = 272}</span><span class="sxs-lookup"><span data-stu-id="1e374-123">/app1/ifd/{ushort=272}</span></span> | <span data-ttu-id="1e374-124">ascii</span><span class="sxs-lookup"><span data-stu-id="1e374-124">ascii</span></span>       |
| <span data-ttu-id="1e374-125">2</span><span class="sxs-lookup"><span data-stu-id="1e374-125">2</span></span>     | <span data-ttu-id="1e374-126">/XMP/TIFF : modèle</span><span class="sxs-lookup"><span data-stu-id="1e374-126">/xmp/tiff:Model</span></span>        | <span data-ttu-id="1e374-127">unicode</span><span class="sxs-lookup"><span data-stu-id="1e374-127">unicode</span></span>     |
| <span data-ttu-id="1e374-128">3</span><span class="sxs-lookup"><span data-stu-id="1e374-128">3</span></span>     | <span data-ttu-id="1e374-129">/XMP/TIFF : modèle</span><span class="sxs-lookup"><span data-stu-id="1e374-129">/xmp/tiff:model</span></span>        | <span data-ttu-id="1e374-130">unicode</span><span class="sxs-lookup"><span data-stu-id="1e374-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="1e374-131">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="1e374-131">Write Paths</span></span>



| <span data-ttu-id="1e374-132">Commande</span><span class="sxs-lookup"><span data-stu-id="1e374-132">Order</span></span> | <span data-ttu-id="1e374-133">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1e374-133">Path</span></span>                   | <span data-ttu-id="1e374-134">Format de disque</span><span class="sxs-lookup"><span data-stu-id="1e374-134">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="1e374-135">1</span><span class="sxs-lookup"><span data-stu-id="1e374-135">1</span></span>     | <span data-ttu-id="1e374-136">/App1/IFD/{UShort = 272}</span><span class="sxs-lookup"><span data-stu-id="1e374-136">/app1/ifd/{ushort=272}</span></span> | <span data-ttu-id="1e374-137">ascii</span><span class="sxs-lookup"><span data-stu-id="1e374-137">ascii</span></span>       |
| <span data-ttu-id="1e374-138">2</span><span class="sxs-lookup"><span data-stu-id="1e374-138">2</span></span>     | <span data-ttu-id="1e374-139">/XMP/TIFF : modèle</span><span class="sxs-lookup"><span data-stu-id="1e374-139">/xmp/tiff:Model</span></span>        | <span data-ttu-id="1e374-140">unicode</span><span class="sxs-lookup"><span data-stu-id="1e374-140">unicode</span></span>     |
| <span data-ttu-id="1e374-141">3</span><span class="sxs-lookup"><span data-stu-id="1e374-141">3</span></span>     | <span data-ttu-id="1e374-142">/XMP/TIFF : modèle</span><span class="sxs-lookup"><span data-stu-id="1e374-142">/xmp/tiff:model</span></span>        | <span data-ttu-id="1e374-143">unicode</span><span class="sxs-lookup"><span data-stu-id="1e374-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="1e374-144">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="1e374-144">Remove Paths</span></span>



| <span data-ttu-id="1e374-145">Commande</span><span class="sxs-lookup"><span data-stu-id="1e374-145">Order</span></span> | <span data-ttu-id="1e374-146">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1e374-146">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="1e374-147">1</span><span class="sxs-lookup"><span data-stu-id="1e374-147">1</span></span>     | <span data-ttu-id="1e374-148">/App1/IFD/{UShort = 272}</span><span class="sxs-lookup"><span data-stu-id="1e374-148">/app1/ifd/{ushort=272}</span></span> |
| <span data-ttu-id="1e374-149">2</span><span class="sxs-lookup"><span data-stu-id="1e374-149">2</span></span>     | <span data-ttu-id="1e374-150">/XMP/TIFF : modèle</span><span class="sxs-lookup"><span data-stu-id="1e374-150">/xmp/tiff:Model</span></span>        |
| <span data-ttu-id="1e374-151">3</span><span class="sxs-lookup"><span data-stu-id="1e374-151">3</span></span>     | <span data-ttu-id="1e374-152">/XMP/TIFF : modèle</span><span class="sxs-lookup"><span data-stu-id="1e374-152">/xmp/tiff:model</span></span>        |



 

### <a name="tiff-policy"></a><span data-ttu-id="1e374-153">Stratégie TIFF</span><span class="sxs-lookup"><span data-stu-id="1e374-153">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="1e374-154">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="1e374-154">Read Paths</span></span>



| <span data-ttu-id="1e374-155">Commande</span><span class="sxs-lookup"><span data-stu-id="1e374-155">Order</span></span> | <span data-ttu-id="1e374-156">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1e374-156">Path</span></span>                | <span data-ttu-id="1e374-157">Format de disque</span><span class="sxs-lookup"><span data-stu-id="1e374-157">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="1e374-158">1</span><span class="sxs-lookup"><span data-stu-id="1e374-158">1</span></span>     | <span data-ttu-id="1e374-159">/IFD/{UShort = 272}</span><span class="sxs-lookup"><span data-stu-id="1e374-159">/ifd/{ushort=272}</span></span>   | <span data-ttu-id="1e374-160">ascii</span><span class="sxs-lookup"><span data-stu-id="1e374-160">ascii</span></span>       |
| <span data-ttu-id="1e374-161">2</span><span class="sxs-lookup"><span data-stu-id="1e374-161">2</span></span>     | <span data-ttu-id="1e374-162">/IFD/XMP/TIFF : modèle</span><span class="sxs-lookup"><span data-stu-id="1e374-162">/ifd/xmp/tiff:Model</span></span> | <span data-ttu-id="1e374-163">unicode</span><span class="sxs-lookup"><span data-stu-id="1e374-163">unicode</span></span>     |
| <span data-ttu-id="1e374-164">3</span><span class="sxs-lookup"><span data-stu-id="1e374-164">3</span></span>     | <span data-ttu-id="1e374-165">/IFD/XMP/TIFF : modèle</span><span class="sxs-lookup"><span data-stu-id="1e374-165">/ifd/xmp/tiff:model</span></span> | <span data-ttu-id="1e374-166">unicode</span><span class="sxs-lookup"><span data-stu-id="1e374-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="1e374-167">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="1e374-167">Write Paths</span></span>



| <span data-ttu-id="1e374-168">Commande</span><span class="sxs-lookup"><span data-stu-id="1e374-168">Order</span></span> | <span data-ttu-id="1e374-169">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1e374-169">Path</span></span>                | <span data-ttu-id="1e374-170">Format de disque</span><span class="sxs-lookup"><span data-stu-id="1e374-170">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="1e374-171">1</span><span class="sxs-lookup"><span data-stu-id="1e374-171">1</span></span>     | <span data-ttu-id="1e374-172">/IFD/{UShort = 272}</span><span class="sxs-lookup"><span data-stu-id="1e374-172">/ifd/{ushort=272}</span></span>   | <span data-ttu-id="1e374-173">ascii</span><span class="sxs-lookup"><span data-stu-id="1e374-173">ascii</span></span>       |
| <span data-ttu-id="1e374-174">2</span><span class="sxs-lookup"><span data-stu-id="1e374-174">2</span></span>     | <span data-ttu-id="1e374-175">/IFD/XMP/TIFF : modèle</span><span class="sxs-lookup"><span data-stu-id="1e374-175">/ifd/xmp/tiff:Model</span></span> | <span data-ttu-id="1e374-176">unicode</span><span class="sxs-lookup"><span data-stu-id="1e374-176">unicode</span></span>     |
| <span data-ttu-id="1e374-177">3</span><span class="sxs-lookup"><span data-stu-id="1e374-177">3</span></span>     | <span data-ttu-id="1e374-178">/IFD/XMP/TIFF : modèle</span><span class="sxs-lookup"><span data-stu-id="1e374-178">/ifd/xmp/tiff:model</span></span> | <span data-ttu-id="1e374-179">unicode</span><span class="sxs-lookup"><span data-stu-id="1e374-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="1e374-180">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="1e374-180">Remove Paths</span></span>



| <span data-ttu-id="1e374-181">Commande</span><span class="sxs-lookup"><span data-stu-id="1e374-181">Order</span></span> | <span data-ttu-id="1e374-182">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1e374-182">Path</span></span>                |
|-------|---------------------|
| <span data-ttu-id="1e374-183">1</span><span class="sxs-lookup"><span data-stu-id="1e374-183">1</span></span>     | <span data-ttu-id="1e374-184">/IFD/{UShort = 272}</span><span class="sxs-lookup"><span data-stu-id="1e374-184">/ifd/{ushort=272}</span></span>   |
| <span data-ttu-id="1e374-185">2</span><span class="sxs-lookup"><span data-stu-id="1e374-185">2</span></span>     | <span data-ttu-id="1e374-186">/IFD/XMP/TIFF : modèle</span><span class="sxs-lookup"><span data-stu-id="1e374-186">/ifd/xmp/tiff:Model</span></span> |
| <span data-ttu-id="1e374-187">3</span><span class="sxs-lookup"><span data-stu-id="1e374-187">3</span></span>     | <span data-ttu-id="1e374-188">/IFD/XMP/TIFF : modèle</span><span class="sxs-lookup"><span data-stu-id="1e374-188">/ifd/xmp/tiff:model</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1e374-189">Notes</span><span class="sxs-lookup"><span data-stu-id="1e374-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e374-190">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1e374-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e374-191">System. photo. CameraModel</span><span class="sxs-lookup"><span data-stu-id="1e374-191">System.Photo.CameraModel</span></span>](../properties/props-system-photo-cameramodel.md)
</dt> </dl>

 

 
