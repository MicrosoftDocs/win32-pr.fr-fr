---
description: Stratégie de métadonnées de la photo pour la propriété System. image. ResolutionUnit.
ms.assetid: b8b744bd-976b-4648-a04b-33607467d6ac
title: Stratégie de métadonnées de photo System. image. ResolutionUnit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d954df0b7efe9501cf25c33a54cd4296fb03f3c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521213"
---
# <a name="systemimageresolutionunit-photo-metadata-policy"></a><span data-ttu-id="c0e69-103">Stratégie de métadonnées de photo System. image. ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="c0e69-103">System.Image.ResolutionUnit Photo Metadata Policy</span></span>

<span data-ttu-id="c0e69-104">Stratégie de métadonnées de la photo pour la propriété [System. image. ResolutionUnit](../properties/props-system-image-resolutionunit.md) .</span><span class="sxs-lookup"><span data-stu-id="c0e69-104">The photo metadata policy for the [System.Image.ResolutionUnit](../properties/props-system-image-resolutionunit.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="c0e69-105">A-la</span><span class="sxs-lookup"><span data-stu-id="c0e69-105">PKEY</span></span>

<span data-ttu-id="c0e69-106">Image de la \_ \_ ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="c0e69-106">PKEY\_Image\_ResolutionUnit</span></span>

### <a name="containers"></a><span data-ttu-id="c0e69-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="c0e69-107">Containers</span></span>

<span data-ttu-id="c0e69-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c0e69-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="c0e69-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c0e69-109">Read-Only</span></span>

<span data-ttu-id="c0e69-110">Oui.</span><span class="sxs-lookup"><span data-stu-id="c0e69-110">Yes.</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="c0e69-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="c0e69-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="c0e69-112">VT \_ I2</span><span class="sxs-lookup"><span data-stu-id="c0e69-112">VT\_I2</span></span>

### <a name="input-type"></a><span data-ttu-id="c0e69-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="c0e69-113">Input Type</span></span>

<span data-ttu-id="c0e69-114">UShort</span><span class="sxs-lookup"><span data-stu-id="c0e69-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="c0e69-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="c0e69-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="c0e69-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="c0e69-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="c0e69-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="c0e69-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="c0e69-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="c0e69-118">Read Paths</span></span>



| <span data-ttu-id="c0e69-119">Commande</span><span class="sxs-lookup"><span data-stu-id="c0e69-119">Order</span></span> | <span data-ttu-id="c0e69-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c0e69-120">Path</span></span>                     | <span data-ttu-id="c0e69-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="c0e69-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="c0e69-122">1</span><span class="sxs-lookup"><span data-stu-id="c0e69-122">1</span></span>     | <span data-ttu-id="c0e69-123">/App1/IFD/{UShort = 296}</span><span class="sxs-lookup"><span data-stu-id="c0e69-123">/app1/ifd/{ushort=296}</span></span>   | <span data-ttu-id="c0e69-124">ushort</span><span class="sxs-lookup"><span data-stu-id="c0e69-124">ushort</span></span>      |
| <span data-ttu-id="c0e69-125">2</span><span class="sxs-lookup"><span data-stu-id="c0e69-125">2</span></span>     | <span data-ttu-id="c0e69-126">/xmp/tiff:ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="c0e69-126">/xmp/tiff:ResolutionUnit</span></span> | <span data-ttu-id="c0e69-127">unicode</span><span class="sxs-lookup"><span data-stu-id="c0e69-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c0e69-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="c0e69-128">Write Paths</span></span>



| <span data-ttu-id="c0e69-129">Commande</span><span class="sxs-lookup"><span data-stu-id="c0e69-129">Order</span></span> | <span data-ttu-id="c0e69-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c0e69-130">Path</span></span>                     | <span data-ttu-id="c0e69-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="c0e69-131">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="c0e69-132">1</span><span class="sxs-lookup"><span data-stu-id="c0e69-132">1</span></span>     | <span data-ttu-id="c0e69-133">/App1/IFD/{UShort = 296}</span><span class="sxs-lookup"><span data-stu-id="c0e69-133">/app1/ifd/{ushort=296}</span></span>   | <span data-ttu-id="c0e69-134">ushort</span><span class="sxs-lookup"><span data-stu-id="c0e69-134">ushort</span></span>      |
| <span data-ttu-id="c0e69-135">2</span><span class="sxs-lookup"><span data-stu-id="c0e69-135">2</span></span>     | <span data-ttu-id="c0e69-136">/xmp/tiff:ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="c0e69-136">/xmp/tiff:ResolutionUnit</span></span> | <span data-ttu-id="c0e69-137">unicode</span><span class="sxs-lookup"><span data-stu-id="c0e69-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c0e69-138">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="c0e69-138">Remove Paths</span></span>



| <span data-ttu-id="c0e69-139">Commande</span><span class="sxs-lookup"><span data-stu-id="c0e69-139">Order</span></span> | <span data-ttu-id="c0e69-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c0e69-140">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="c0e69-141">1</span><span class="sxs-lookup"><span data-stu-id="c0e69-141">1</span></span>     | <span data-ttu-id="c0e69-142">/App1/IFD/{UShort = 296}</span><span class="sxs-lookup"><span data-stu-id="c0e69-142">/app1/ifd/{ushort=296}</span></span>   |
| <span data-ttu-id="c0e69-143">2</span><span class="sxs-lookup"><span data-stu-id="c0e69-143">2</span></span>     | <span data-ttu-id="c0e69-144">/xmp/tiff:resolutionunit</span><span class="sxs-lookup"><span data-stu-id="c0e69-144">/xmp/tiff:resolutionunit</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="c0e69-145">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="c0e69-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="c0e69-146">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="c0e69-146">Read Paths</span></span>



| <span data-ttu-id="c0e69-147">Commande</span><span class="sxs-lookup"><span data-stu-id="c0e69-147">Order</span></span> | <span data-ttu-id="c0e69-148">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c0e69-148">Path</span></span>                         | <span data-ttu-id="c0e69-149">Format de disque</span><span class="sxs-lookup"><span data-stu-id="c0e69-149">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="c0e69-150">1</span><span class="sxs-lookup"><span data-stu-id="c0e69-150">1</span></span>     | <span data-ttu-id="c0e69-151">/IFD/{UShort = 296}</span><span class="sxs-lookup"><span data-stu-id="c0e69-151">/ifd/{ushort=296}</span></span>            | <span data-ttu-id="c0e69-152">ushort</span><span class="sxs-lookup"><span data-stu-id="c0e69-152">ushort</span></span>      |
| <span data-ttu-id="c0e69-153">2</span><span class="sxs-lookup"><span data-stu-id="c0e69-153">2</span></span>     | <span data-ttu-id="c0e69-154">/ifd/xmp/tiff:ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="c0e69-154">/ifd/xmp/tiff:ResolutionUnit</span></span> | <span data-ttu-id="c0e69-155">unicode</span><span class="sxs-lookup"><span data-stu-id="c0e69-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c0e69-156">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="c0e69-156">Write Paths</span></span>



| <span data-ttu-id="c0e69-157">Commande</span><span class="sxs-lookup"><span data-stu-id="c0e69-157">Order</span></span> | <span data-ttu-id="c0e69-158">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c0e69-158">Path</span></span>                         | <span data-ttu-id="c0e69-159">Format de disque</span><span class="sxs-lookup"><span data-stu-id="c0e69-159">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="c0e69-160">1</span><span class="sxs-lookup"><span data-stu-id="c0e69-160">1</span></span>     | <span data-ttu-id="c0e69-161">/IFD/{UShort = 296}</span><span class="sxs-lookup"><span data-stu-id="c0e69-161">/ifd/{ushort=296}</span></span>            | <span data-ttu-id="c0e69-162">ushort</span><span class="sxs-lookup"><span data-stu-id="c0e69-162">ushort</span></span>      |
| <span data-ttu-id="c0e69-163">2</span><span class="sxs-lookup"><span data-stu-id="c0e69-163">2</span></span>     | <span data-ttu-id="c0e69-164">/ifd/xmp/tiff:ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="c0e69-164">/ifd/xmp/tiff:ResolutionUnit</span></span> | <span data-ttu-id="c0e69-165">unicode</span><span class="sxs-lookup"><span data-stu-id="c0e69-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c0e69-166">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="c0e69-166">Remove Paths</span></span>



| <span data-ttu-id="c0e69-167">Commande</span><span class="sxs-lookup"><span data-stu-id="c0e69-167">Order</span></span> | <span data-ttu-id="c0e69-168">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c0e69-168">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="c0e69-169">1</span><span class="sxs-lookup"><span data-stu-id="c0e69-169">1</span></span>     | <span data-ttu-id="c0e69-170">/IFD/{UShort = 296}</span><span class="sxs-lookup"><span data-stu-id="c0e69-170">/ifd/{ushort=296}</span></span>            |
| <span data-ttu-id="c0e69-171">2</span><span class="sxs-lookup"><span data-stu-id="c0e69-171">2</span></span>     | <span data-ttu-id="c0e69-172">/ifd/xmp/tiff:resolutionunit</span><span class="sxs-lookup"><span data-stu-id="c0e69-172">/ifd/xmp/tiff:resolutionunit</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c0e69-173">Notes</span><span class="sxs-lookup"><span data-stu-id="c0e69-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0e69-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c0e69-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0e69-175">System. image. ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="c0e69-175">System.Image.ResolutionUnit</span></span>](../properties/props-system-image-resolutionunit.md)
</dt> </dl>

 

 
