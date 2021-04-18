---
description: Stratégie de métadonnées de la photo pour la propriété System. image. compression.
ms.assetid: 0fada41f-f6f8-43b3-ad65-79785e859c9c
title: Stratégie de métadonnées de photo System. image. compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32fdc55e2a6a962b1a3dfd9057ef25c89d942f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519734"
---
# <a name="systemimagecompression-photo-metadata-policy"></a><span data-ttu-id="03f78-103">Stratégie de métadonnées de photo System. image. compression</span><span class="sxs-lookup"><span data-stu-id="03f78-103">System.Image.Compression Photo Metadata Policy</span></span>

<span data-ttu-id="03f78-104">Stratégie de métadonnées de la photo pour la propriété [System. image. compression](../properties/props-system-image-compression.md) .</span><span class="sxs-lookup"><span data-stu-id="03f78-104">The photo metadata policy for the [System.Image.Compression](../properties/props-system-image-compression.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="03f78-105">A-la</span><span class="sxs-lookup"><span data-stu-id="03f78-105">PKEY</span></span>

<span data-ttu-id="03f78-106">Compression d’image de la \_ \_ prime</span><span class="sxs-lookup"><span data-stu-id="03f78-106">PKEY\_Image\_Compression</span></span>

### <a name="containers"></a><span data-ttu-id="03f78-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="03f78-107">Containers</span></span>

<span data-ttu-id="03f78-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="03f78-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="03f78-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="03f78-109">Read-Only</span></span>

<span data-ttu-id="03f78-110">Oui</span><span class="sxs-lookup"><span data-stu-id="03f78-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="03f78-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="03f78-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="03f78-112">\_UI2 VT</span><span class="sxs-lookup"><span data-stu-id="03f78-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="03f78-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="03f78-113">Input Type</span></span>

<span data-ttu-id="03f78-114">UShort</span><span class="sxs-lookup"><span data-stu-id="03f78-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="03f78-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="03f78-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="03f78-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="03f78-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="03f78-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="03f78-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="03f78-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="03f78-118">Read Paths</span></span>



| <span data-ttu-id="03f78-119">Commande</span><span class="sxs-lookup"><span data-stu-id="03f78-119">Order</span></span> | <span data-ttu-id="03f78-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="03f78-120">Path</span></span>                   | <span data-ttu-id="03f78-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="03f78-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="03f78-122">1</span><span class="sxs-lookup"><span data-stu-id="03f78-122">1</span></span>     | <span data-ttu-id="03f78-123">/App1/IFD/{UShort = 259}</span><span class="sxs-lookup"><span data-stu-id="03f78-123">/app1/ifd/{ushort=259}</span></span> | <span data-ttu-id="03f78-124">ushort</span><span class="sxs-lookup"><span data-stu-id="03f78-124">ushort</span></span>      |
| <span data-ttu-id="03f78-125">2</span><span class="sxs-lookup"><span data-stu-id="03f78-125">2</span></span>     | <span data-ttu-id="03f78-126">/XMP/TIFF : compression</span><span class="sxs-lookup"><span data-stu-id="03f78-126">/xmp/tiff:Compression</span></span>  | <span data-ttu-id="03f78-127">unicode</span><span class="sxs-lookup"><span data-stu-id="03f78-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="03f78-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="03f78-128">Write Paths</span></span>



| <span data-ttu-id="03f78-129">Commande</span><span class="sxs-lookup"><span data-stu-id="03f78-129">Order</span></span> | <span data-ttu-id="03f78-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="03f78-130">Path</span></span>                   | <span data-ttu-id="03f78-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="03f78-131">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="03f78-132">1</span><span class="sxs-lookup"><span data-stu-id="03f78-132">1</span></span>     | <span data-ttu-id="03f78-133">/App1/IFD/{UShort = 259}</span><span class="sxs-lookup"><span data-stu-id="03f78-133">/app1/ifd/{ushort=259}</span></span> | <span data-ttu-id="03f78-134">ushort</span><span class="sxs-lookup"><span data-stu-id="03f78-134">ushort</span></span>      |
| <span data-ttu-id="03f78-135">2</span><span class="sxs-lookup"><span data-stu-id="03f78-135">2</span></span>     | <span data-ttu-id="03f78-136">/XMP/TIFF : compression</span><span class="sxs-lookup"><span data-stu-id="03f78-136">/xmp/tiff:Compression</span></span>  | <span data-ttu-id="03f78-137">unicode</span><span class="sxs-lookup"><span data-stu-id="03f78-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="03f78-138">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="03f78-138">Remove Paths</span></span>



| <span data-ttu-id="03f78-139">Commande</span><span class="sxs-lookup"><span data-stu-id="03f78-139">Order</span></span> | <span data-ttu-id="03f78-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="03f78-140">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="03f78-141">1</span><span class="sxs-lookup"><span data-stu-id="03f78-141">1</span></span>     | <span data-ttu-id="03f78-142">/App1/IFD/{UShort = 259}</span><span class="sxs-lookup"><span data-stu-id="03f78-142">/app1/ifd/{ushort=259}</span></span> |
| <span data-ttu-id="03f78-143">2</span><span class="sxs-lookup"><span data-stu-id="03f78-143">2</span></span>     | <span data-ttu-id="03f78-144">/XMP/TIFF : compression</span><span class="sxs-lookup"><span data-stu-id="03f78-144">/xmp/tiff:compression</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="03f78-145">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="03f78-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="03f78-146">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="03f78-146">Read Paths</span></span>



| <span data-ttu-id="03f78-147">Commande</span><span class="sxs-lookup"><span data-stu-id="03f78-147">Order</span></span> | <span data-ttu-id="03f78-148">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="03f78-148">Path</span></span>                      | <span data-ttu-id="03f78-149">Format de disque</span><span class="sxs-lookup"><span data-stu-id="03f78-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="03f78-150">1</span><span class="sxs-lookup"><span data-stu-id="03f78-150">1</span></span>     | <span data-ttu-id="03f78-151">/IFD/{UShort = 259}</span><span class="sxs-lookup"><span data-stu-id="03f78-151">/ifd/{ushort=259}</span></span>         | <span data-ttu-id="03f78-152">ushort</span><span class="sxs-lookup"><span data-stu-id="03f78-152">ushort</span></span>      |
| <span data-ttu-id="03f78-153">2</span><span class="sxs-lookup"><span data-stu-id="03f78-153">2</span></span>     | <span data-ttu-id="03f78-154">/IFD/XMP/TIFF : compression</span><span class="sxs-lookup"><span data-stu-id="03f78-154">/ifd/xmp/tiff:Compression</span></span> | <span data-ttu-id="03f78-155">unicode</span><span class="sxs-lookup"><span data-stu-id="03f78-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="03f78-156">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="03f78-156">Write Paths</span></span>



| <span data-ttu-id="03f78-157">Commande</span><span class="sxs-lookup"><span data-stu-id="03f78-157">Order</span></span> | <span data-ttu-id="03f78-158">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="03f78-158">Path</span></span>                      | <span data-ttu-id="03f78-159">Format de disque</span><span class="sxs-lookup"><span data-stu-id="03f78-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="03f78-160">1</span><span class="sxs-lookup"><span data-stu-id="03f78-160">1</span></span>     | <span data-ttu-id="03f78-161">/IFD/{UShort = 259}</span><span class="sxs-lookup"><span data-stu-id="03f78-161">/ifd/{ushort=259}</span></span>         | <span data-ttu-id="03f78-162">ushort</span><span class="sxs-lookup"><span data-stu-id="03f78-162">ushort</span></span>      |
| <span data-ttu-id="03f78-163">2</span><span class="sxs-lookup"><span data-stu-id="03f78-163">2</span></span>     | <span data-ttu-id="03f78-164">/IFD/XMP/TIFF : compression</span><span class="sxs-lookup"><span data-stu-id="03f78-164">/ifd/xmp/tiff:Compression</span></span> | <span data-ttu-id="03f78-165">unicode</span><span class="sxs-lookup"><span data-stu-id="03f78-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="03f78-166">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="03f78-166">Remove Paths</span></span>



| <span data-ttu-id="03f78-167">Commande</span><span class="sxs-lookup"><span data-stu-id="03f78-167">Order</span></span> | <span data-ttu-id="03f78-168">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="03f78-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="03f78-169">1</span><span class="sxs-lookup"><span data-stu-id="03f78-169">1</span></span>     | <span data-ttu-id="03f78-170">/IFD/{UShort = 259}</span><span class="sxs-lookup"><span data-stu-id="03f78-170">/ifd/{ushort=259}</span></span>         |
| <span data-ttu-id="03f78-171">2</span><span class="sxs-lookup"><span data-stu-id="03f78-171">2</span></span>     | <span data-ttu-id="03f78-172">/IFD/XMP/TIFF : compression</span><span class="sxs-lookup"><span data-stu-id="03f78-172">/ifd/xmp/tiff:compression</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="03f78-173">Notes</span><span class="sxs-lookup"><span data-stu-id="03f78-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="03f78-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="03f78-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03f78-175">System. image. compression</span><span class="sxs-lookup"><span data-stu-id="03f78-175">System.Image.Compression</span></span>](../properties/props-system-image-compression.md)
</dt> </dl>

 

 
