---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. DateTaken.
ms.assetid: 800aa01b-6064-45df-a40e-6537819df4d7
title: Stratégie de métadonnées de photo System. photo. DateTaken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc1d3fb50a9a94e4bb13b35a0a5726572d78429f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522222"
---
# <a name="systemphotodatetaken-photo-metadata-policy"></a><span data-ttu-id="3e7ba-103">Stratégie de métadonnées de photo System. photo. DateTaken</span><span class="sxs-lookup"><span data-stu-id="3e7ba-103">System.Photo.DateTaken Photo Metadata Policy</span></span>

<span data-ttu-id="3e7ba-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. DateTaken](../properties/props-system-photo-datetaken.md) .</span><span class="sxs-lookup"><span data-stu-id="3e7ba-104">The photo metadata policy for the [System.Photo.DateTaken](../properties/props-system-photo-datetaken.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="3e7ba-105">A-la</span><span class="sxs-lookup"><span data-stu-id="3e7ba-105">PKEY</span></span>

<span data-ttu-id="3e7ba-106">\_Photo \_ DateTaken</span><span class="sxs-lookup"><span data-stu-id="3e7ba-106">PKEY\_Photo\_DateTaken</span></span>

### <a name="containers"></a><span data-ttu-id="3e7ba-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="3e7ba-107">Containers</span></span>

<span data-ttu-id="3e7ba-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="3e7ba-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="3e7ba-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3e7ba-109">Read-Only</span></span>

<span data-ttu-id="3e7ba-110">Non</span><span class="sxs-lookup"><span data-stu-id="3e7ba-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="3e7ba-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="3e7ba-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="3e7ba-112">de VT \_ fileTime</span><span class="sxs-lookup"><span data-stu-id="3e7ba-112">VT\_FILETIME</span></span>

### <a name="input-type"></a><span data-ttu-id="3e7ba-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="3e7ba-113">Input Type</span></span>

<span data-ttu-id="3e7ba-114">DateTime</span><span class="sxs-lookup"><span data-stu-id="3e7ba-114">DateTime</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="3e7ba-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="3e7ba-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="3e7ba-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="3e7ba-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="3e7ba-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="3e7ba-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="3e7ba-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="3e7ba-118">Read Paths</span></span>



| <span data-ttu-id="3e7ba-119">Commande</span><span class="sxs-lookup"><span data-stu-id="3e7ba-119">Order</span></span> | <span data-ttu-id="3e7ba-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="3e7ba-120">Path</span></span>                                  | <span data-ttu-id="3e7ba-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="3e7ba-121">Disk Format</span></span> |
|-------|---------------------------------------|-------------|
| <span data-ttu-id="3e7ba-122">1</span><span class="sxs-lookup"><span data-stu-id="3e7ba-122">1</span></span>     | <span data-ttu-id="3e7ba-123">/App1/IFD/EXIF/{UShort = 36867}</span><span class="sxs-lookup"><span data-stu-id="3e7ba-123">/app1/ifd/exif/{ushort=36867}</span></span>         | <span data-ttu-id="3e7ba-124">ascii</span><span class="sxs-lookup"><span data-stu-id="3e7ba-124">ascii</span></span>       |
| <span data-ttu-id="3e7ba-125">2</span><span class="sxs-lookup"><span data-stu-id="3e7ba-125">2</span></span>     | <span data-ttu-id="3e7ba-126">/APP13/IRB/8bimiptc/IPTC/Date créé</span><span class="sxs-lookup"><span data-stu-id="3e7ba-126">/app13/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="3e7ba-127">unicode</span><span class="sxs-lookup"><span data-stu-id="3e7ba-127">unicode</span></span>     |
| <span data-ttu-id="3e7ba-128">3</span><span class="sxs-lookup"><span data-stu-id="3e7ba-128">3</span></span>     | <span data-ttu-id="3e7ba-129">/XMP/XMP : CreateD</span><span class="sxs-lookup"><span data-stu-id="3e7ba-129">/xmp/xmp:CreateDate</span></span>                   | <span data-ttu-id="3e7ba-130">unicode</span><span class="sxs-lookup"><span data-stu-id="3e7ba-130">unicode</span></span>     |
| <span data-ttu-id="3e7ba-131">4</span><span class="sxs-lookup"><span data-stu-id="3e7ba-131">4</span></span>     | <span data-ttu-id="3e7ba-132">/App1/IFD/EXIF/{UShort = 36868}</span><span class="sxs-lookup"><span data-stu-id="3e7ba-132">/app1/ifd/exif/{ushort=36868}</span></span>         | <span data-ttu-id="3e7ba-133">ascii</span><span class="sxs-lookup"><span data-stu-id="3e7ba-133">ascii</span></span>       |
| <span data-ttu-id="3e7ba-134">5</span><span class="sxs-lookup"><span data-stu-id="3e7ba-134">5</span></span>     | <span data-ttu-id="3e7ba-135">/APP13/IRB/8bimiptc/IPTC/Date créé</span><span class="sxs-lookup"><span data-stu-id="3e7ba-135">/app13/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="3e7ba-136">unicode</span><span class="sxs-lookup"><span data-stu-id="3e7ba-136">unicode</span></span>     |
| <span data-ttu-id="3e7ba-137">6</span><span class="sxs-lookup"><span data-stu-id="3e7ba-137">6</span></span>     | <span data-ttu-id="3e7ba-138">/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="3e7ba-138">/xmp/exif:DateTimeOriginal</span></span>            | <span data-ttu-id="3e7ba-139">unicode</span><span class="sxs-lookup"><span data-stu-id="3e7ba-139">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="3e7ba-140">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="3e7ba-140">Write Paths</span></span>



| <span data-ttu-id="3e7ba-141">Commande</span><span class="sxs-lookup"><span data-stu-id="3e7ba-141">Order</span></span> | <span data-ttu-id="3e7ba-142">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="3e7ba-142">Path</span></span>                                  | <span data-ttu-id="3e7ba-143">Format de disque</span><span class="sxs-lookup"><span data-stu-id="3e7ba-143">Disk Format</span></span> |
|-------|---------------------------------------|-------------|
| <span data-ttu-id="3e7ba-144">1</span><span class="sxs-lookup"><span data-stu-id="3e7ba-144">1</span></span>     | <span data-ttu-id="3e7ba-145">/App1/IFD/EXIF/{UShort = 36867}</span><span class="sxs-lookup"><span data-stu-id="3e7ba-145">/app1/ifd/exif/{ushort=36867}</span></span>         | <span data-ttu-id="3e7ba-146">ascii</span><span class="sxs-lookup"><span data-stu-id="3e7ba-146">ascii</span></span>       |
| <span data-ttu-id="3e7ba-147">2</span><span class="sxs-lookup"><span data-stu-id="3e7ba-147">2</span></span>     | <span data-ttu-id="3e7ba-148">/APP13/IRB/8bimiptc/IPTC/Date créé</span><span class="sxs-lookup"><span data-stu-id="3e7ba-148">/app13/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="3e7ba-149">unicode</span><span class="sxs-lookup"><span data-stu-id="3e7ba-149">unicode</span></span>     |
| <span data-ttu-id="3e7ba-150">3</span><span class="sxs-lookup"><span data-stu-id="3e7ba-150">3</span></span>     | <span data-ttu-id="3e7ba-151">/XMP/XMP : CreateD</span><span class="sxs-lookup"><span data-stu-id="3e7ba-151">/xmp/xmp:CreateDate</span></span>                   | <span data-ttu-id="3e7ba-152">unicode</span><span class="sxs-lookup"><span data-stu-id="3e7ba-152">unicode</span></span>     |
| <span data-ttu-id="3e7ba-153">4</span><span class="sxs-lookup"><span data-stu-id="3e7ba-153">4</span></span>     | <span data-ttu-id="3e7ba-154">/App1/IFD/EXIF/{UShort = 36868}</span><span class="sxs-lookup"><span data-stu-id="3e7ba-154">/app1/ifd/exif/{ushort=36868}</span></span>         | <span data-ttu-id="3e7ba-155">ascii</span><span class="sxs-lookup"><span data-stu-id="3e7ba-155">ascii</span></span>       |
| <span data-ttu-id="3e7ba-156">5</span><span class="sxs-lookup"><span data-stu-id="3e7ba-156">5</span></span>     | <span data-ttu-id="3e7ba-157">/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="3e7ba-157">/xmp/exif:DateTimeOriginal</span></span>            | <span data-ttu-id="3e7ba-158">unicode</span><span class="sxs-lookup"><span data-stu-id="3e7ba-158">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="3e7ba-159">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="3e7ba-159">Remove Paths</span></span>



| <span data-ttu-id="3e7ba-160">Commande</span><span class="sxs-lookup"><span data-stu-id="3e7ba-160">Order</span></span> | <span data-ttu-id="3e7ba-161">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="3e7ba-161">Path</span></span>                                  |
|-------|---------------------------------------|
| <span data-ttu-id="3e7ba-162">1</span><span class="sxs-lookup"><span data-stu-id="3e7ba-162">1</span></span>     | <span data-ttu-id="3e7ba-163">/App1/IFD/EXIF/{UShort = 36867}</span><span class="sxs-lookup"><span data-stu-id="3e7ba-163">/app1/ifd/exif/{ushort=36867}</span></span>         |
| <span data-ttu-id="3e7ba-164">2</span><span class="sxs-lookup"><span data-stu-id="3e7ba-164">2</span></span>     | <span data-ttu-id="3e7ba-165">/App1/IFD/EXIF/{UShort = 37521}</span><span class="sxs-lookup"><span data-stu-id="3e7ba-165">/app1/ifd/exif/{ushort=37521}</span></span>         |
| <span data-ttu-id="3e7ba-166">3</span><span class="sxs-lookup"><span data-stu-id="3e7ba-166">3</span></span>     | <span data-ttu-id="3e7ba-167">/App1/IFD/EXIF/{UShort = 36868}</span><span class="sxs-lookup"><span data-stu-id="3e7ba-167">/app1/ifd/exif/{ushort=36868}</span></span>         |
| <span data-ttu-id="3e7ba-168">4</span><span class="sxs-lookup"><span data-stu-id="3e7ba-168">4</span></span>     | <span data-ttu-id="3e7ba-169">/App1/IFD/EXIF/{UShort = 37522}</span><span class="sxs-lookup"><span data-stu-id="3e7ba-169">/app1/ifd/exif/{ushort=37522}</span></span>         |
| <span data-ttu-id="3e7ba-170">5</span><span class="sxs-lookup"><span data-stu-id="3e7ba-170">5</span></span>     | <span data-ttu-id="3e7ba-171">/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="3e7ba-171">/xmp/exif:DateTimeOriginal</span></span>            |
| <span data-ttu-id="3e7ba-172">6</span><span class="sxs-lookup"><span data-stu-id="3e7ba-172">6</span></span>     | <span data-ttu-id="3e7ba-173">/XMP/XMP : CreateD</span><span class="sxs-lookup"><span data-stu-id="3e7ba-173">/xmp/xmp:CreateDate</span></span>                   |
| <span data-ttu-id="3e7ba-174">7</span><span class="sxs-lookup"><span data-stu-id="3e7ba-174">7</span></span>     | <span data-ttu-id="3e7ba-175">/APP13/IRB/8bimiptc/IPTC/Date créé</span><span class="sxs-lookup"><span data-stu-id="3e7ba-175">/app13/irb/8bimiptc/iptc/date created</span></span> |
| <span data-ttu-id="3e7ba-176">8</span><span class="sxs-lookup"><span data-stu-id="3e7ba-176">8</span></span>     | <span data-ttu-id="3e7ba-177">/APP13/IRB/8bimiptc/IPTC/Time créé</span><span class="sxs-lookup"><span data-stu-id="3e7ba-177">/app13/irb/8bimiptc/iptc/time created</span></span> |



 

### <a name="tiff-policy"></a><span data-ttu-id="3e7ba-178">Stratégie TIFF</span><span class="sxs-lookup"><span data-stu-id="3e7ba-178">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="3e7ba-179">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="3e7ba-179">Read Paths</span></span>



| <span data-ttu-id="3e7ba-180">Commande</span><span class="sxs-lookup"><span data-stu-id="3e7ba-180">Order</span></span> | <span data-ttu-id="3e7ba-181">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="3e7ba-181">Path</span></span>                                | <span data-ttu-id="3e7ba-182">Format de disque</span><span class="sxs-lookup"><span data-stu-id="3e7ba-182">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="3e7ba-183">1</span><span class="sxs-lookup"><span data-stu-id="3e7ba-183">1</span></span>     | <span data-ttu-id="3e7ba-184">/IFD/EXIF/{UShort = 36867}</span><span class="sxs-lookup"><span data-stu-id="3e7ba-184">/ifd/exif/{ushort=36867}</span></span>            | <span data-ttu-id="3e7ba-185">ascii</span><span class="sxs-lookup"><span data-stu-id="3e7ba-185">ascii</span></span>       |
| <span data-ttu-id="3e7ba-186">2</span><span class="sxs-lookup"><span data-stu-id="3e7ba-186">2</span></span>     | <span data-ttu-id="3e7ba-187">/IFD/IPTC/Date créé</span><span class="sxs-lookup"><span data-stu-id="3e7ba-187">/ifd/iptc/date created</span></span>              | <span data-ttu-id="3e7ba-188">unicode</span><span class="sxs-lookup"><span data-stu-id="3e7ba-188">unicode</span></span>     |
| <span data-ttu-id="3e7ba-189">3</span><span class="sxs-lookup"><span data-stu-id="3e7ba-189">3</span></span>     | <span data-ttu-id="3e7ba-190">/IFD/XMP/XMP : CreateD</span><span class="sxs-lookup"><span data-stu-id="3e7ba-190">/ifd/xmp/xmp:CreateDate</span></span>             | <span data-ttu-id="3e7ba-191">unicode</span><span class="sxs-lookup"><span data-stu-id="3e7ba-191">unicode</span></span>     |
| <span data-ttu-id="3e7ba-192">4</span><span class="sxs-lookup"><span data-stu-id="3e7ba-192">4</span></span>     | <span data-ttu-id="3e7ba-193">/IFD/EXIF/{UShort = 36868}</span><span class="sxs-lookup"><span data-stu-id="3e7ba-193">/ifd/exif/{ushort=36868}</span></span>            | <span data-ttu-id="3e7ba-194">ascii</span><span class="sxs-lookup"><span data-stu-id="3e7ba-194">ascii</span></span>       |
| <span data-ttu-id="3e7ba-195">5</span><span class="sxs-lookup"><span data-stu-id="3e7ba-195">5</span></span>     | <span data-ttu-id="3e7ba-196">/IFD/IPTC/Date créé</span><span class="sxs-lookup"><span data-stu-id="3e7ba-196">/ifd/iptc/date created</span></span>              | <span data-ttu-id="3e7ba-197">unicode</span><span class="sxs-lookup"><span data-stu-id="3e7ba-197">unicode</span></span>     |
| <span data-ttu-id="3e7ba-198">6</span><span class="sxs-lookup"><span data-stu-id="3e7ba-198">6</span></span>     | <span data-ttu-id="3e7ba-199">/IFD/IRB/8bimiptc/IPTC/Date créé</span><span class="sxs-lookup"><span data-stu-id="3e7ba-199">/ifd/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="3e7ba-200">unicode</span><span class="sxs-lookup"><span data-stu-id="3e7ba-200">unicode</span></span>     |
| <span data-ttu-id="3e7ba-201">7</span><span class="sxs-lookup"><span data-stu-id="3e7ba-201">7</span></span>     | <span data-ttu-id="3e7ba-202">/ifd/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="3e7ba-202">/ifd/xmp/exif:DateTimeOriginal</span></span>      | <span data-ttu-id="3e7ba-203">unicode</span><span class="sxs-lookup"><span data-stu-id="3e7ba-203">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="3e7ba-204">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="3e7ba-204">Write Paths</span></span>



| <span data-ttu-id="3e7ba-205">Commande</span><span class="sxs-lookup"><span data-stu-id="3e7ba-205">Order</span></span> | <span data-ttu-id="3e7ba-206">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="3e7ba-206">Path</span></span>                                | <span data-ttu-id="3e7ba-207">Format de disque</span><span class="sxs-lookup"><span data-stu-id="3e7ba-207">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="3e7ba-208">1</span><span class="sxs-lookup"><span data-stu-id="3e7ba-208">1</span></span>     | <span data-ttu-id="3e7ba-209">/IFD/EXIF/{UShort = 36867}</span><span class="sxs-lookup"><span data-stu-id="3e7ba-209">/ifd/exif/{ushort=36867}</span></span>            | <span data-ttu-id="3e7ba-210">ascii</span><span class="sxs-lookup"><span data-stu-id="3e7ba-210">ascii</span></span>       |
| <span data-ttu-id="3e7ba-211">2</span><span class="sxs-lookup"><span data-stu-id="3e7ba-211">2</span></span>     | <span data-ttu-id="3e7ba-212">/IFD/IPTC/Date créé</span><span class="sxs-lookup"><span data-stu-id="3e7ba-212">/ifd/iptc/date created</span></span>              | <span data-ttu-id="3e7ba-213">unicode</span><span class="sxs-lookup"><span data-stu-id="3e7ba-213">unicode</span></span>     |
| <span data-ttu-id="3e7ba-214">3</span><span class="sxs-lookup"><span data-stu-id="3e7ba-214">3</span></span>     | <span data-ttu-id="3e7ba-215">/IFD/XMP/XMP : CreateD</span><span class="sxs-lookup"><span data-stu-id="3e7ba-215">/ifd/xmp/xmp:CreateDate</span></span>             | <span data-ttu-id="3e7ba-216">unicode</span><span class="sxs-lookup"><span data-stu-id="3e7ba-216">unicode</span></span>     |
| <span data-ttu-id="3e7ba-217">4</span><span class="sxs-lookup"><span data-stu-id="3e7ba-217">4</span></span>     | <span data-ttu-id="3e7ba-218">/IFD/EXIF/{UShort = 36868}</span><span class="sxs-lookup"><span data-stu-id="3e7ba-218">/ifd/exif/{ushort=36868}</span></span>            | <span data-ttu-id="3e7ba-219">ascii</span><span class="sxs-lookup"><span data-stu-id="3e7ba-219">ascii</span></span>       |
| <span data-ttu-id="3e7ba-220">5</span><span class="sxs-lookup"><span data-stu-id="3e7ba-220">5</span></span>     | <span data-ttu-id="3e7ba-221">/IFD/IRB/8bimiptc/IPTC/Date créé</span><span class="sxs-lookup"><span data-stu-id="3e7ba-221">/ifd/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="3e7ba-222">unicode</span><span class="sxs-lookup"><span data-stu-id="3e7ba-222">unicode</span></span>     |
| <span data-ttu-id="3e7ba-223">6</span><span class="sxs-lookup"><span data-stu-id="3e7ba-223">6</span></span>     | <span data-ttu-id="3e7ba-224">/ifd/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="3e7ba-224">/ifd/xmp/exif:DateTimeOriginal</span></span>      | <span data-ttu-id="3e7ba-225">unicode</span><span class="sxs-lookup"><span data-stu-id="3e7ba-225">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="3e7ba-226">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="3e7ba-226">Remove Paths</span></span>



| <span data-ttu-id="3e7ba-227">Commande</span><span class="sxs-lookup"><span data-stu-id="3e7ba-227">Order</span></span> | <span data-ttu-id="3e7ba-228">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="3e7ba-228">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="3e7ba-229">1</span><span class="sxs-lookup"><span data-stu-id="3e7ba-229">1</span></span>     | <span data-ttu-id="3e7ba-230">/IFD/EXIF/{UShort = 36867}</span><span class="sxs-lookup"><span data-stu-id="3e7ba-230">/ifd/exif/{ushort=36867}</span></span>            |
| <span data-ttu-id="3e7ba-231">2</span><span class="sxs-lookup"><span data-stu-id="3e7ba-231">2</span></span>     | <span data-ttu-id="3e7ba-232">/IFD/EXIF/{UShort = 37521}</span><span class="sxs-lookup"><span data-stu-id="3e7ba-232">/ifd/exif/{ushort=37521}</span></span>            |
| <span data-ttu-id="3e7ba-233">3</span><span class="sxs-lookup"><span data-stu-id="3e7ba-233">3</span></span>     | <span data-ttu-id="3e7ba-234">/IFD/EXIF/{UShort = 36868}</span><span class="sxs-lookup"><span data-stu-id="3e7ba-234">/ifd/exif/{ushort=36868}</span></span>            |
| <span data-ttu-id="3e7ba-235">4</span><span class="sxs-lookup"><span data-stu-id="3e7ba-235">4</span></span>     | <span data-ttu-id="3e7ba-236">/IFD/EXIF/{UShort = 37522}</span><span class="sxs-lookup"><span data-stu-id="3e7ba-236">/ifd/exif/{ushort=37522}</span></span>            |
| <span data-ttu-id="3e7ba-237">5</span><span class="sxs-lookup"><span data-stu-id="3e7ba-237">5</span></span>     | <span data-ttu-id="3e7ba-238">/ifd/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="3e7ba-238">/ifd/xmp/exif:DateTimeOriginal</span></span>      |
| <span data-ttu-id="3e7ba-239">6</span><span class="sxs-lookup"><span data-stu-id="3e7ba-239">6</span></span>     | <span data-ttu-id="3e7ba-240">/IFD/XMP/XMP : CreateD</span><span class="sxs-lookup"><span data-stu-id="3e7ba-240">/ifd/xmp/xmp:CreateDate</span></span>             |
| <span data-ttu-id="3e7ba-241">7</span><span class="sxs-lookup"><span data-stu-id="3e7ba-241">7</span></span>     | <span data-ttu-id="3e7ba-242">/IFD/IPTC/Date créé</span><span class="sxs-lookup"><span data-stu-id="3e7ba-242">/ifd/iptc/date created</span></span>              |
| <span data-ttu-id="3e7ba-243">8</span><span class="sxs-lookup"><span data-stu-id="3e7ba-243">8</span></span>     | <span data-ttu-id="3e7ba-244">/IFD/IPTC/Time créé</span><span class="sxs-lookup"><span data-stu-id="3e7ba-244">/ifd/iptc/time created</span></span>              |
| <span data-ttu-id="3e7ba-245">9</span><span class="sxs-lookup"><span data-stu-id="3e7ba-245">9</span></span>     | <span data-ttu-id="3e7ba-246">/IFD/IRB/8bimiptc/IPTC/Date créé</span><span class="sxs-lookup"><span data-stu-id="3e7ba-246">/ifd/irb/8bimiptc/iptc/date created</span></span> |
| <span data-ttu-id="3e7ba-247">10</span><span class="sxs-lookup"><span data-stu-id="3e7ba-247">10</span></span>    | <span data-ttu-id="3e7ba-248">/IFD/IRB/8bimiptc/IPTC/Time créé</span><span class="sxs-lookup"><span data-stu-id="3e7ba-248">/ifd/irb/8bimiptc/iptc/time created</span></span> |



 

### <a name="png-policy"></a><span data-ttu-id="3e7ba-249">Stratégie PNG</span><span class="sxs-lookup"><span data-stu-id="3e7ba-249">PNG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="3e7ba-250">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="3e7ba-250">Read Paths</span></span>



| <span data-ttu-id="3e7ba-251">Commande</span><span class="sxs-lookup"><span data-stu-id="3e7ba-251">Order</span></span> | <span data-ttu-id="3e7ba-252">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="3e7ba-252">Path</span></span>                      | <span data-ttu-id="3e7ba-253">Format de disque</span><span class="sxs-lookup"><span data-stu-id="3e7ba-253">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="3e7ba-254">1</span><span class="sxs-lookup"><span data-stu-id="3e7ba-254">1</span></span>     | <span data-ttu-id="3e7ba-255">/\[\*\]Texte/heure de création</span><span class="sxs-lookup"><span data-stu-id="3e7ba-255">/\[\*\]tEXt/Creation Time</span></span> | <span data-ttu-id="3e7ba-256">ascii</span><span class="sxs-lookup"><span data-stu-id="3e7ba-256">ascii</span></span>       |



 

### <a name="write-paths"></a><span data-ttu-id="3e7ba-257">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="3e7ba-257">Write Paths</span></span>



| <span data-ttu-id="3e7ba-258">Commande</span><span class="sxs-lookup"><span data-stu-id="3e7ba-258">Order</span></span> | <span data-ttu-id="3e7ba-259">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="3e7ba-259">Path</span></span>                      | <span data-ttu-id="3e7ba-260">Format de disque</span><span class="sxs-lookup"><span data-stu-id="3e7ba-260">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="3e7ba-261">2</span><span class="sxs-lookup"><span data-stu-id="3e7ba-261">2</span></span>     | <span data-ttu-id="3e7ba-262">/\[\*\]Texte/heure de création</span><span class="sxs-lookup"><span data-stu-id="3e7ba-262">/\[\*\]tEXt/Creation Time</span></span> | <span data-ttu-id="3e7ba-263">ascii</span><span class="sxs-lookup"><span data-stu-id="3e7ba-263">ascii</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="3e7ba-264">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="3e7ba-264">Remove Paths</span></span>



| <span data-ttu-id="3e7ba-265">Commande</span><span class="sxs-lookup"><span data-stu-id="3e7ba-265">Order</span></span> | <span data-ttu-id="3e7ba-266">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="3e7ba-266">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="3e7ba-267">3</span><span class="sxs-lookup"><span data-stu-id="3e7ba-267">3</span></span>     | <span data-ttu-id="3e7ba-268">/\[\*\]Texte/heure de création</span><span class="sxs-lookup"><span data-stu-id="3e7ba-268">/\[\*\]tEXt/Creation Time</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3e7ba-269">Notes</span><span class="sxs-lookup"><span data-stu-id="3e7ba-269">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e7ba-270">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3e7ba-270">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e7ba-271">System. photo. DateTaken</span><span class="sxs-lookup"><span data-stu-id="3e7ba-271">System.Photo.DateTaken</span></span>](../properties/props-system-photo-datetaken.md)
</dt> </dl>

 

 
