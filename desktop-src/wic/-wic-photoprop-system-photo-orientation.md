---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. orientation.
ms.assetid: 27e6d4f5-39d5-4cb4-88bc-b0d61ccaa2f3
title: Stratégie de métadonnées de photo System. photo. orientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28f4f350cd1a4c24d71ec737b4679aea2f7cab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035029"
---
# <a name="systemphotoorientation-photo-metadata-policy"></a><span data-ttu-id="02d9c-103">Stratégie de métadonnées de photo System. photo. orientation</span><span class="sxs-lookup"><span data-stu-id="02d9c-103">System.Photo.Orientation Photo Metadata Policy</span></span>

<span data-ttu-id="02d9c-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. orientation](../properties/props-system-photo-meteringmode.md) .</span><span class="sxs-lookup"><span data-stu-id="02d9c-104">The photo metadata policy for the [System.Photo.Orientation](../properties/props-system-photo-meteringmode.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="02d9c-105">A-la</span><span class="sxs-lookup"><span data-stu-id="02d9c-105">PKEY</span></span>

<span data-ttu-id="02d9c-106">Orientation de photo de l' \_ hypergraphique \_</span><span class="sxs-lookup"><span data-stu-id="02d9c-106">PKEY\_Photo\_Orientation</span></span>

### <a name="containers"></a><span data-ttu-id="02d9c-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="02d9c-107">Containers</span></span>

<span data-ttu-id="02d9c-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="02d9c-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="02d9c-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02d9c-109">Read-Only</span></span>

<span data-ttu-id="02d9c-110">Non</span><span class="sxs-lookup"><span data-stu-id="02d9c-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="02d9c-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="02d9c-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="02d9c-112">\_UI2 VT</span><span class="sxs-lookup"><span data-stu-id="02d9c-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="02d9c-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="02d9c-113">Input Type</span></span>

<span data-ttu-id="02d9c-114">UShort</span><span class="sxs-lookup"><span data-stu-id="02d9c-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="02d9c-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="02d9c-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="02d9c-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="02d9c-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="02d9c-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="02d9c-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="02d9c-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="02d9c-118">Read Paths</span></span>



| <span data-ttu-id="02d9c-119">Commande</span><span class="sxs-lookup"><span data-stu-id="02d9c-119">Order</span></span> | <span data-ttu-id="02d9c-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="02d9c-120">Path</span></span>                   | <span data-ttu-id="02d9c-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="02d9c-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="02d9c-122">1</span><span class="sxs-lookup"><span data-stu-id="02d9c-122">1</span></span>     | <span data-ttu-id="02d9c-123">/App1/IFD/{UShort = 274}</span><span class="sxs-lookup"><span data-stu-id="02d9c-123">/app1/ifd/{ushort=274}</span></span> | <span data-ttu-id="02d9c-124">ushort</span><span class="sxs-lookup"><span data-stu-id="02d9c-124">ushort</span></span>      |
| <span data-ttu-id="02d9c-125">2</span><span class="sxs-lookup"><span data-stu-id="02d9c-125">2</span></span>     | <span data-ttu-id="02d9c-126">/XMP/TIFF : orientation</span><span class="sxs-lookup"><span data-stu-id="02d9c-126">/xmp/tiff:Orientation</span></span>  | <span data-ttu-id="02d9c-127">unicode</span><span class="sxs-lookup"><span data-stu-id="02d9c-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="02d9c-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="02d9c-128">Write Paths</span></span>



| <span data-ttu-id="02d9c-129">Commande</span><span class="sxs-lookup"><span data-stu-id="02d9c-129">Order</span></span> | <span data-ttu-id="02d9c-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="02d9c-130">Path</span></span>                   | <span data-ttu-id="02d9c-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="02d9c-131">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="02d9c-132">1</span><span class="sxs-lookup"><span data-stu-id="02d9c-132">1</span></span>     | <span data-ttu-id="02d9c-133">/App1/IFD/{UShort = 274}</span><span class="sxs-lookup"><span data-stu-id="02d9c-133">/app1/ifd/{ushort=274}</span></span> | <span data-ttu-id="02d9c-134">ushort</span><span class="sxs-lookup"><span data-stu-id="02d9c-134">ushort</span></span>      |
| <span data-ttu-id="02d9c-135">2</span><span class="sxs-lookup"><span data-stu-id="02d9c-135">2</span></span>     | <span data-ttu-id="02d9c-136">/XMP/TIFF : orientation</span><span class="sxs-lookup"><span data-stu-id="02d9c-136">/xmp/tiff:Orientation</span></span>  | <span data-ttu-id="02d9c-137">unicode</span><span class="sxs-lookup"><span data-stu-id="02d9c-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="02d9c-138">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="02d9c-138">Remove Paths</span></span>



| <span data-ttu-id="02d9c-139">Commande</span><span class="sxs-lookup"><span data-stu-id="02d9c-139">Order</span></span> | <span data-ttu-id="02d9c-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="02d9c-140">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="02d9c-141">1</span><span class="sxs-lookup"><span data-stu-id="02d9c-141">1</span></span>     | <span data-ttu-id="02d9c-142">/App1/IFD/{UShort = 274}</span><span class="sxs-lookup"><span data-stu-id="02d9c-142">/app1/ifd/{ushort=274}</span></span> |
| <span data-ttu-id="02d9c-143">2</span><span class="sxs-lookup"><span data-stu-id="02d9c-143">2</span></span>     | <span data-ttu-id="02d9c-144">/XMP/TIFF : orientation</span><span class="sxs-lookup"><span data-stu-id="02d9c-144">/xmp/tiff:orientation</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="02d9c-145">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="02d9c-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="02d9c-146">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="02d9c-146">Read Paths</span></span>



| <span data-ttu-id="02d9c-147">Commande</span><span class="sxs-lookup"><span data-stu-id="02d9c-147">Order</span></span> | <span data-ttu-id="02d9c-148">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="02d9c-148">Path</span></span>                      | <span data-ttu-id="02d9c-149">Format de disque</span><span class="sxs-lookup"><span data-stu-id="02d9c-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="02d9c-150">1</span><span class="sxs-lookup"><span data-stu-id="02d9c-150">1</span></span>     | <span data-ttu-id="02d9c-151">/IFD/{UShort = 274}</span><span class="sxs-lookup"><span data-stu-id="02d9c-151">/ifd/{ushort=274}</span></span>         | <span data-ttu-id="02d9c-152">ushort</span><span class="sxs-lookup"><span data-stu-id="02d9c-152">ushort</span></span>      |
| <span data-ttu-id="02d9c-153">2</span><span class="sxs-lookup"><span data-stu-id="02d9c-153">2</span></span>     | <span data-ttu-id="02d9c-154">/IFD/XMP/TIFF : orientation</span><span class="sxs-lookup"><span data-stu-id="02d9c-154">/ifd/xmp/tiff:Orientation</span></span> | <span data-ttu-id="02d9c-155">unicode</span><span class="sxs-lookup"><span data-stu-id="02d9c-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="02d9c-156">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="02d9c-156">Write Paths</span></span>



| <span data-ttu-id="02d9c-157">Commande</span><span class="sxs-lookup"><span data-stu-id="02d9c-157">Order</span></span> | <span data-ttu-id="02d9c-158">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="02d9c-158">Path</span></span>                      | <span data-ttu-id="02d9c-159">Format de disque</span><span class="sxs-lookup"><span data-stu-id="02d9c-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="02d9c-160">1</span><span class="sxs-lookup"><span data-stu-id="02d9c-160">1</span></span>     | <span data-ttu-id="02d9c-161">/IFD/{UShort = 274}</span><span class="sxs-lookup"><span data-stu-id="02d9c-161">/ifd/{ushort=274}</span></span>         | <span data-ttu-id="02d9c-162">ushort</span><span class="sxs-lookup"><span data-stu-id="02d9c-162">ushort</span></span>      |
| <span data-ttu-id="02d9c-163">2</span><span class="sxs-lookup"><span data-stu-id="02d9c-163">2</span></span>     | <span data-ttu-id="02d9c-164">/IFD/XMP/TIFF : orientation</span><span class="sxs-lookup"><span data-stu-id="02d9c-164">/ifd/xmp/tiff:Orientation</span></span> | <span data-ttu-id="02d9c-165">unicode</span><span class="sxs-lookup"><span data-stu-id="02d9c-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="02d9c-166">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="02d9c-166">Remove Paths</span></span>



| <span data-ttu-id="02d9c-167">Commande</span><span class="sxs-lookup"><span data-stu-id="02d9c-167">Order</span></span> | <span data-ttu-id="02d9c-168">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="02d9c-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="02d9c-169">1</span><span class="sxs-lookup"><span data-stu-id="02d9c-169">1</span></span>     | <span data-ttu-id="02d9c-170">/IFD/{UShort = 274}</span><span class="sxs-lookup"><span data-stu-id="02d9c-170">/ifd/{ushort=274}</span></span>         |
| <span data-ttu-id="02d9c-171">2</span><span class="sxs-lookup"><span data-stu-id="02d9c-171">2</span></span>     | <span data-ttu-id="02d9c-172">/IFD/XMP/TIFF : orientation</span><span class="sxs-lookup"><span data-stu-id="02d9c-172">/ifd/xmp/tiff:orientation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="02d9c-173">Notes</span><span class="sxs-lookup"><span data-stu-id="02d9c-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="02d9c-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="02d9c-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02d9c-175">System. photo. orientation</span><span class="sxs-lookup"><span data-stu-id="02d9c-175">System.Photo.Orientation</span></span>](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
