---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. ProgramMode.
ms.assetid: f1954dc7-d4df-4675-ab3b-a65f2354e57a
title: Stratégie de métadonnées de photo System. photo. ProgramMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f5dffa822454509134c485e4792f4be4270912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952612"
---
# <a name="systemphotoprogrammode-photo-metadata-policy"></a><span data-ttu-id="895e3-103">Stratégie de métadonnées de photo System. photo. ProgramMode</span><span class="sxs-lookup"><span data-stu-id="895e3-103">System.Photo.ProgramMode Photo Metadata Policy</span></span>

<span data-ttu-id="895e3-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. ProgramMode](../properties/props-system-photo-programmode.md) .</span><span class="sxs-lookup"><span data-stu-id="895e3-104">The photo metadata policy for the [System.Photo.ProgramMode](../properties/props-system-photo-programmode.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="895e3-105">A-la</span><span class="sxs-lookup"><span data-stu-id="895e3-105">PKEY</span></span>

<span data-ttu-id="895e3-106">\_Photo \_ ProgramMode</span><span class="sxs-lookup"><span data-stu-id="895e3-106">PKEY\_Photo\_ProgramMode</span></span>

### <a name="containers"></a><span data-ttu-id="895e3-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="895e3-107">Containers</span></span>

<span data-ttu-id="895e3-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="895e3-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="895e3-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="895e3-109">Read-Only</span></span>

<span data-ttu-id="895e3-110">Non</span><span class="sxs-lookup"><span data-stu-id="895e3-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="895e3-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="895e3-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="895e3-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="895e3-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="895e3-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="895e3-113">Input Type</span></span>

<span data-ttu-id="895e3-114">UShort</span><span class="sxs-lookup"><span data-stu-id="895e3-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="895e3-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="895e3-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="895e3-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="895e3-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="895e3-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="895e3-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="895e3-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="895e3-118">Read Paths</span></span>



| <span data-ttu-id="895e3-119">Commande</span><span class="sxs-lookup"><span data-stu-id="895e3-119">Order</span></span> | <span data-ttu-id="895e3-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="895e3-120">Path</span></span>                          | <span data-ttu-id="895e3-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="895e3-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="895e3-122">1</span><span class="sxs-lookup"><span data-stu-id="895e3-122">1</span></span>     | <span data-ttu-id="895e3-123">/App1/IFD/EXIF/{UShort = 34850}</span><span class="sxs-lookup"><span data-stu-id="895e3-123">/app1/ifd/exif/{ushort=34850}</span></span> | <span data-ttu-id="895e3-124">ushort</span><span class="sxs-lookup"><span data-stu-id="895e3-124">ushort</span></span>      |
| <span data-ttu-id="895e3-125">2</span><span class="sxs-lookup"><span data-stu-id="895e3-125">2</span></span>     | <span data-ttu-id="895e3-126">/xmp/exif:ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="895e3-126">/xmp/exif:ExposureProgram</span></span>     | <span data-ttu-id="895e3-127">unicode</span><span class="sxs-lookup"><span data-stu-id="895e3-127">unicode</span></span>     |
| <span data-ttu-id="895e3-128">3</span><span class="sxs-lookup"><span data-stu-id="895e3-128">3</span></span>     | <span data-ttu-id="895e3-129">/xmp/exif:ProgramMode</span><span class="sxs-lookup"><span data-stu-id="895e3-129">/xmp/exif:ProgramMode</span></span>         | <span data-ttu-id="895e3-130">unicode</span><span class="sxs-lookup"><span data-stu-id="895e3-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="895e3-131">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="895e3-131">Write Paths</span></span>



| <span data-ttu-id="895e3-132">Commande</span><span class="sxs-lookup"><span data-stu-id="895e3-132">Order</span></span> | <span data-ttu-id="895e3-133">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="895e3-133">Path</span></span>                          | <span data-ttu-id="895e3-134">Format de disque</span><span class="sxs-lookup"><span data-stu-id="895e3-134">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="895e3-135">1</span><span class="sxs-lookup"><span data-stu-id="895e3-135">1</span></span>     | <span data-ttu-id="895e3-136">/App1/IFD/EXIF/{UShort = 34850}</span><span class="sxs-lookup"><span data-stu-id="895e3-136">/app1/ifd/exif/{ushort=34850}</span></span> | <span data-ttu-id="895e3-137">ushort</span><span class="sxs-lookup"><span data-stu-id="895e3-137">ushort</span></span>      |
| <span data-ttu-id="895e3-138">2</span><span class="sxs-lookup"><span data-stu-id="895e3-138">2</span></span>     | <span data-ttu-id="895e3-139">/xmp/exif:ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="895e3-139">/xmp/exif:ExposureProgram</span></span>     | <span data-ttu-id="895e3-140">unicode</span><span class="sxs-lookup"><span data-stu-id="895e3-140">unicode</span></span>     |
| <span data-ttu-id="895e3-141">3</span><span class="sxs-lookup"><span data-stu-id="895e3-141">3</span></span>     | <span data-ttu-id="895e3-142">/xmp/exif:ProgramMode</span><span class="sxs-lookup"><span data-stu-id="895e3-142">/xmp/exif:ProgramMode</span></span>         | <span data-ttu-id="895e3-143">unicode</span><span class="sxs-lookup"><span data-stu-id="895e3-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="895e3-144">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="895e3-144">Remove Paths</span></span>



| <span data-ttu-id="895e3-145">Commande</span><span class="sxs-lookup"><span data-stu-id="895e3-145">Order</span></span> | <span data-ttu-id="895e3-146">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="895e3-146">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="895e3-147">1</span><span class="sxs-lookup"><span data-stu-id="895e3-147">1</span></span>     | <span data-ttu-id="895e3-148">/App1/IFD/EXIF/{UShort = 34850}</span><span class="sxs-lookup"><span data-stu-id="895e3-148">/app1/ifd/exif/{ushort=34850}</span></span> |
| <span data-ttu-id="895e3-149">2</span><span class="sxs-lookup"><span data-stu-id="895e3-149">2</span></span>     | <span data-ttu-id="895e3-150">/xmp/exif:exposureprogram</span><span class="sxs-lookup"><span data-stu-id="895e3-150">/xmp/exif:exposureprogram</span></span>     |
| <span data-ttu-id="895e3-151">3</span><span class="sxs-lookup"><span data-stu-id="895e3-151">3</span></span>     | <span data-ttu-id="895e3-152">/xmp/exif:programmode</span><span class="sxs-lookup"><span data-stu-id="895e3-152">/xmp/exif:programmode</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="895e3-153">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="895e3-153">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="895e3-154">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="895e3-154">Read Paths</span></span>



| <span data-ttu-id="895e3-155">Commande</span><span class="sxs-lookup"><span data-stu-id="895e3-155">Order</span></span> | <span data-ttu-id="895e3-156">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="895e3-156">Path</span></span>                          | <span data-ttu-id="895e3-157">Format de disque</span><span class="sxs-lookup"><span data-stu-id="895e3-157">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="895e3-158">1</span><span class="sxs-lookup"><span data-stu-id="895e3-158">1</span></span>     | <span data-ttu-id="895e3-159">/IFD/EXIF/{UShort = 34850}</span><span class="sxs-lookup"><span data-stu-id="895e3-159">/ifd/exif/{ushort=34850}</span></span>      | <span data-ttu-id="895e3-160">ushort</span><span class="sxs-lookup"><span data-stu-id="895e3-160">ushort</span></span>      |
| <span data-ttu-id="895e3-161">2</span><span class="sxs-lookup"><span data-stu-id="895e3-161">2</span></span>     | <span data-ttu-id="895e3-162">/ifd/xmp/exif:ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="895e3-162">/ifd/xmp/exif:ExposureProgram</span></span> | <span data-ttu-id="895e3-163">unicode</span><span class="sxs-lookup"><span data-stu-id="895e3-163">unicode</span></span>     |
| <span data-ttu-id="895e3-164">3</span><span class="sxs-lookup"><span data-stu-id="895e3-164">3</span></span>     | <span data-ttu-id="895e3-165">/ifd/xmp/exif:ProgramMode</span><span class="sxs-lookup"><span data-stu-id="895e3-165">/ifd/xmp/exif:ProgramMode</span></span>     | <span data-ttu-id="895e3-166">unicode</span><span class="sxs-lookup"><span data-stu-id="895e3-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="895e3-167">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="895e3-167">Write Paths</span></span>



| <span data-ttu-id="895e3-168">Commande</span><span class="sxs-lookup"><span data-stu-id="895e3-168">Order</span></span> | <span data-ttu-id="895e3-169">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="895e3-169">Path</span></span>                          | <span data-ttu-id="895e3-170">Format de disque</span><span class="sxs-lookup"><span data-stu-id="895e3-170">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="895e3-171">1</span><span class="sxs-lookup"><span data-stu-id="895e3-171">1</span></span>     | <span data-ttu-id="895e3-172">/IFD/EXIF/{UShort = 34850}</span><span class="sxs-lookup"><span data-stu-id="895e3-172">/ifd/exif/{ushort=34850}</span></span>      | <span data-ttu-id="895e3-173">ushort</span><span class="sxs-lookup"><span data-stu-id="895e3-173">ushort</span></span>      |
| <span data-ttu-id="895e3-174">2</span><span class="sxs-lookup"><span data-stu-id="895e3-174">2</span></span>     | <span data-ttu-id="895e3-175">/ifd/xmp/exif:ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="895e3-175">/ifd/xmp/exif:ExposureProgram</span></span> | <span data-ttu-id="895e3-176">unicode</span><span class="sxs-lookup"><span data-stu-id="895e3-176">unicode</span></span>     |
| <span data-ttu-id="895e3-177">3</span><span class="sxs-lookup"><span data-stu-id="895e3-177">3</span></span>     | <span data-ttu-id="895e3-178">/ifd/xmp/exif:ProgramMode</span><span class="sxs-lookup"><span data-stu-id="895e3-178">/ifd/xmp/exif:ProgramMode</span></span>     | <span data-ttu-id="895e3-179">unicode</span><span class="sxs-lookup"><span data-stu-id="895e3-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="895e3-180">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="895e3-180">Remove Paths</span></span>



| <span data-ttu-id="895e3-181">Commande</span><span class="sxs-lookup"><span data-stu-id="895e3-181">Order</span></span> | <span data-ttu-id="895e3-182">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="895e3-182">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="895e3-183">1</span><span class="sxs-lookup"><span data-stu-id="895e3-183">1</span></span>     | <span data-ttu-id="895e3-184">/IFD/EXIF/{UShort = 34850}</span><span class="sxs-lookup"><span data-stu-id="895e3-184">/ifd/exif/{ushort=34850}</span></span>      |
| <span data-ttu-id="895e3-185">2</span><span class="sxs-lookup"><span data-stu-id="895e3-185">2</span></span>     | <span data-ttu-id="895e3-186">/ifd/xmp/exif:exposureprogram</span><span class="sxs-lookup"><span data-stu-id="895e3-186">/ifd/xmp/exif:exposureprogram</span></span> |
| <span data-ttu-id="895e3-187">3</span><span class="sxs-lookup"><span data-stu-id="895e3-187">3</span></span>     | <span data-ttu-id="895e3-188">/ifd/xmp/exif:programmode</span><span class="sxs-lookup"><span data-stu-id="895e3-188">/ifd/xmp/exif:programmode</span></span>     |



 

## <a name="remarks"></a><span data-ttu-id="895e3-189">Notes</span><span class="sxs-lookup"><span data-stu-id="895e3-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="895e3-190">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="895e3-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="895e3-191">System. photo. ProgramMode</span><span class="sxs-lookup"><span data-stu-id="895e3-191">System.Photo.ProgramMode</span></span>](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
