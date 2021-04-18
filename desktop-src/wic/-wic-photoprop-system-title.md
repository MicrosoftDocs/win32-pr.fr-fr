---
description: Stratégie de métadonnées de la photo pour la propriété System. title.
ms.assetid: 84da345e-ec03-48fe-8fda-043b706e4e1c
title: Stratégie de métadonnées de photo System. title
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b02513f3f566576999e83b09c156d36ac480c17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526194"
---
# <a name="systemtitle-photo-metadata-policy"></a><span data-ttu-id="1a9ec-103">Stratégie de métadonnées de photo System. title</span><span class="sxs-lookup"><span data-stu-id="1a9ec-103">System.Title Photo Metadata Policy</span></span>

<span data-ttu-id="1a9ec-104">Stratégie de métadonnées de la photo pour la propriété [System. title](../properties/props-system-title.md) .</span><span class="sxs-lookup"><span data-stu-id="1a9ec-104">The photo metadata policy for the [System.Title](../properties/props-system-title.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="1a9ec-105">A-la</span><span class="sxs-lookup"><span data-stu-id="1a9ec-105">PKEY</span></span>

<span data-ttu-id="1a9ec-106">Titre de la \_ section</span><span class="sxs-lookup"><span data-stu-id="1a9ec-106">PKEY\_Title</span></span>

### <a name="containers"></a><span data-ttu-id="1a9ec-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="1a9ec-107">Containers</span></span>

<span data-ttu-id="1a9ec-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="1a9ec-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="1a9ec-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1a9ec-109">Read-Only</span></span>

<span data-ttu-id="1a9ec-110">Non</span><span class="sxs-lookup"><span data-stu-id="1a9ec-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="1a9ec-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="1a9ec-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="1a9ec-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="1a9ec-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="1a9ec-113">Type de PROPVARIANT d’entrée</span><span class="sxs-lookup"><span data-stu-id="1a9ec-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="1a9ec-114">VT \_ LPWStr ou VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="1a9ec-114">Either VT\_LPWSTR or VT\_LPSTR</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="1a9ec-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="1a9ec-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="1a9ec-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="1a9ec-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="1a9ec-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="1a9ec-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="1a9ec-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="1a9ec-118">Read Paths</span></span>



| <span data-ttu-id="1a9ec-119">Commande</span><span class="sxs-lookup"><span data-stu-id="1a9ec-119">Order</span></span> | <span data-ttu-id="1a9ec-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1a9ec-120">Path</span></span>                                | <span data-ttu-id="1a9ec-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="1a9ec-121">Disk Format</span></span>    |
|-------|-------------------------------------|----------------|
| <span data-ttu-id="1a9ec-122">1</span><span class="sxs-lookup"><span data-stu-id="1a9ec-122">1</span></span>     | <span data-ttu-id="1a9ec-123">/App1/IFD/{UShort = 40091}</span><span class="sxs-lookup"><span data-stu-id="1a9ec-123">/app1/ifd/{ushort=40091}</span></span>            | <span data-ttu-id="1a9ec-124">\_octets Unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-124">unicode\_bytes</span></span> |
| <span data-ttu-id="1a9ec-125">2</span><span class="sxs-lookup"><span data-stu-id="1a9ec-125">2</span></span>     | <span data-ttu-id="1a9ec-126">/XMP/ <xmpalt> DC : titre</span><span class="sxs-lookup"><span data-stu-id="1a9ec-126">/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="1a9ec-127">unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-127">unicode</span></span>        |
| <span data-ttu-id="1a9ec-128">3</span><span class="sxs-lookup"><span data-stu-id="1a9ec-128">3</span></span>     | <span data-ttu-id="1a9ec-129">/XMP/DC : titre</span><span class="sxs-lookup"><span data-stu-id="1a9ec-129">/xmp/dc:title</span></span>                       | <span data-ttu-id="1a9ec-130">unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-130">unicode</span></span>        |
| <span data-ttu-id="1a9ec-131">4</span><span class="sxs-lookup"><span data-stu-id="1a9ec-131">4</span></span>     | <span data-ttu-id="1a9ec-132">/App1/IFD/EXIF/{UShort = 37510}</span><span class="sxs-lookup"><span data-stu-id="1a9ec-132">/app1/ifd/exif/{ushort=37510}</span></span>       | <span data-ttu-id="1a9ec-133">unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-133">unicode</span></span>        |
| <span data-ttu-id="1a9ec-134">5</span><span class="sxs-lookup"><span data-stu-id="1a9ec-134">5</span></span>     | <span data-ttu-id="1a9ec-135">/App1/IFD/{UShort = 270}</span><span class="sxs-lookup"><span data-stu-id="1a9ec-135">/app1/ifd/{ushort=270}</span></span>              | <span data-ttu-id="1a9ec-136">ascii</span><span class="sxs-lookup"><span data-stu-id="1a9ec-136">ascii</span></span>          |
| <span data-ttu-id="1a9ec-137">6</span><span class="sxs-lookup"><span data-stu-id="1a9ec-137">6</span></span>     | <span data-ttu-id="1a9ec-138">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="1a9ec-138">/app13/irb/8bimiptc/iptc/caption</span></span>    |                |
| <span data-ttu-id="1a9ec-139">7</span><span class="sxs-lookup"><span data-stu-id="1a9ec-139">7</span></span>     | <span data-ttu-id="1a9ec-140">/XMP/ <xmpalt> DC : description</span><span class="sxs-lookup"><span data-stu-id="1a9ec-140">/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="1a9ec-141">unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-141">unicode</span></span>        |
| <span data-ttu-id="1a9ec-142">8</span><span class="sxs-lookup"><span data-stu-id="1a9ec-142">8</span></span>     | <span data-ttu-id="1a9ec-143">/XMP/DC : description</span><span class="sxs-lookup"><span data-stu-id="1a9ec-143">/xmp/dc:description</span></span>                 | <span data-ttu-id="1a9ec-144">unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-144">unicode</span></span>        |
| <span data-ttu-id="1a9ec-145">9</span><span class="sxs-lookup"><span data-stu-id="1a9ec-145">9</span></span>     | <span data-ttu-id="1a9ec-146">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="1a9ec-146">/app13/irb/8bimiptc/iptc/caption</span></span>    |                |
| <span data-ttu-id="1a9ec-147">10</span><span class="sxs-lookup"><span data-stu-id="1a9ec-147">10</span></span>    | <span data-ttu-id="1a9ec-148">/XMP/ <xmpalt> EXIF : UserComment</span><span class="sxs-lookup"><span data-stu-id="1a9ec-148">/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="1a9ec-149">unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-149">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="1a9ec-150">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="1a9ec-150">Write Paths</span></span>



| <span data-ttu-id="1a9ec-151">Commande</span><span class="sxs-lookup"><span data-stu-id="1a9ec-151">Order</span></span> | <span data-ttu-id="1a9ec-152">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1a9ec-152">Path</span></span>                                | <span data-ttu-id="1a9ec-153">Format de disque</span><span class="sxs-lookup"><span data-stu-id="1a9ec-153">Disk Format</span></span>    |
|-------|-------------------------------------|----------------|
| <span data-ttu-id="1a9ec-154">1</span><span class="sxs-lookup"><span data-stu-id="1a9ec-154">1</span></span>     | <span data-ttu-id="1a9ec-155">/App1/IFD/{UShort = 40091}</span><span class="sxs-lookup"><span data-stu-id="1a9ec-155">/app1/ifd/{ushort=40091}</span></span>            | <span data-ttu-id="1a9ec-156">\_octets Unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-156">unicode\_bytes</span></span> |
| <span data-ttu-id="1a9ec-157">2</span><span class="sxs-lookup"><span data-stu-id="1a9ec-157">2</span></span>     | <span data-ttu-id="1a9ec-158">/XMP/DC : titre</span><span class="sxs-lookup"><span data-stu-id="1a9ec-158">/xmp/dc:title</span></span>                       | <span data-ttu-id="1a9ec-159">unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-159">unicode</span></span>        |
| <span data-ttu-id="1a9ec-160">3</span><span class="sxs-lookup"><span data-stu-id="1a9ec-160">3</span></span>     | <span data-ttu-id="1a9ec-161">/XMP/ <xmpalt> DC : titre</span><span class="sxs-lookup"><span data-stu-id="1a9ec-161">/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="1a9ec-162">unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-162">unicode</span></span>        |
| <span data-ttu-id="1a9ec-163">4</span><span class="sxs-lookup"><span data-stu-id="1a9ec-163">4</span></span>     | <span data-ttu-id="1a9ec-164">/App1/IFD/EXIF/{UShort = 37510}</span><span class="sxs-lookup"><span data-stu-id="1a9ec-164">/app1/ifd/exif/{ushort=37510}</span></span>       | <span data-ttu-id="1a9ec-165">unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-165">unicode</span></span>        |
| <span data-ttu-id="1a9ec-166">5</span><span class="sxs-lookup"><span data-stu-id="1a9ec-166">5</span></span>     | <span data-ttu-id="1a9ec-167">/XMP/ <xmpalt> EXIF : UserComment</span><span class="sxs-lookup"><span data-stu-id="1a9ec-167">/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="1a9ec-168">unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-168">unicode</span></span>        |
| <span data-ttu-id="1a9ec-169">6</span><span class="sxs-lookup"><span data-stu-id="1a9ec-169">6</span></span>     | <span data-ttu-id="1a9ec-170">/App1/IFD/{UShort = 270}</span><span class="sxs-lookup"><span data-stu-id="1a9ec-170">/app1/ifd/{ushort=270}</span></span>              | <span data-ttu-id="1a9ec-171">ascii</span><span class="sxs-lookup"><span data-stu-id="1a9ec-171">ascii</span></span>          |
| <span data-ttu-id="1a9ec-172">7</span><span class="sxs-lookup"><span data-stu-id="1a9ec-172">7</span></span>     | <span data-ttu-id="1a9ec-173">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="1a9ec-173">/app13/irb/8bimiptc/iptc/caption</span></span>    |                |
| <span data-ttu-id="1a9ec-174">8</span><span class="sxs-lookup"><span data-stu-id="1a9ec-174">8</span></span>     | <span data-ttu-id="1a9ec-175">/XMP/DC : description</span><span class="sxs-lookup"><span data-stu-id="1a9ec-175">/xmp/dc:description</span></span>                 | <span data-ttu-id="1a9ec-176">unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-176">unicode</span></span>        |
| <span data-ttu-id="1a9ec-177">9</span><span class="sxs-lookup"><span data-stu-id="1a9ec-177">9</span></span>     | <span data-ttu-id="1a9ec-178">/XMP/ <xmpalt> DC : description</span><span class="sxs-lookup"><span data-stu-id="1a9ec-178">/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="1a9ec-179">unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-179">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="1a9ec-180">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="1a9ec-180">Remove Paths</span></span>



| <span data-ttu-id="1a9ec-181">Commande</span><span class="sxs-lookup"><span data-stu-id="1a9ec-181">Order</span></span> | <span data-ttu-id="1a9ec-182">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1a9ec-182">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="1a9ec-183">1</span><span class="sxs-lookup"><span data-stu-id="1a9ec-183">1</span></span>     | <span data-ttu-id="1a9ec-184">/App1/IFD/{UShort = 40091}</span><span class="sxs-lookup"><span data-stu-id="1a9ec-184">/app1/ifd/{ushort=40091}</span></span>            |
| <span data-ttu-id="1a9ec-185">2</span><span class="sxs-lookup"><span data-stu-id="1a9ec-185">2</span></span>     | <span data-ttu-id="1a9ec-186">/XMP/DC : titre</span><span class="sxs-lookup"><span data-stu-id="1a9ec-186">/xmp/dc:title</span></span>                       |
| <span data-ttu-id="1a9ec-187">3</span><span class="sxs-lookup"><span data-stu-id="1a9ec-187">3</span></span>     | <span data-ttu-id="1a9ec-188">/App1/IFD/EXIF/{UShort = 37510}</span><span class="sxs-lookup"><span data-stu-id="1a9ec-188">/app1/ifd/exif/{ushort=37510}</span></span>       |
| <span data-ttu-id="1a9ec-189">4</span><span class="sxs-lookup"><span data-stu-id="1a9ec-189">4</span></span>     | <span data-ttu-id="1a9ec-190">/XMP/ <xmpalt> EXIF : UserComment</span><span class="sxs-lookup"><span data-stu-id="1a9ec-190">/xmp/<xmpalt>exif:UserComment</span></span> |
| <span data-ttu-id="1a9ec-191">5</span><span class="sxs-lookup"><span data-stu-id="1a9ec-191">5</span></span>     | <span data-ttu-id="1a9ec-192">/App1/IFD/{UShort = 270}</span><span class="sxs-lookup"><span data-stu-id="1a9ec-192">/app1/ifd/{ushort=270}</span></span>              |
| <span data-ttu-id="1a9ec-193">6</span><span class="sxs-lookup"><span data-stu-id="1a9ec-193">6</span></span>     | <span data-ttu-id="1a9ec-194">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="1a9ec-194">/app13/irb/8bimiptc/iptc/caption</span></span>    |
| <span data-ttu-id="1a9ec-195">7</span><span class="sxs-lookup"><span data-stu-id="1a9ec-195">7</span></span>     | <span data-ttu-id="1a9ec-196">/XMP/DC : description</span><span class="sxs-lookup"><span data-stu-id="1a9ec-196">/xmp/dc:description</span></span>                 |



 

### <a name="tiff-policy"></a><span data-ttu-id="1a9ec-197">Stratégie TIFF</span><span class="sxs-lookup"><span data-stu-id="1a9ec-197">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="1a9ec-198">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="1a9ec-198">Read Paths</span></span>



| <span data-ttu-id="1a9ec-199">Commande</span><span class="sxs-lookup"><span data-stu-id="1a9ec-199">Order</span></span> | <span data-ttu-id="1a9ec-200">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1a9ec-200">Path</span></span>                                    | <span data-ttu-id="1a9ec-201">Format de disque</span><span class="sxs-lookup"><span data-stu-id="1a9ec-201">Disk Format</span></span>    |
|-------|-----------------------------------------|----------------|
| <span data-ttu-id="1a9ec-202">1</span><span class="sxs-lookup"><span data-stu-id="1a9ec-202">1</span></span>     | <span data-ttu-id="1a9ec-203">/IFD/{UShort = 40091}</span><span class="sxs-lookup"><span data-stu-id="1a9ec-203">/ifd/{ushort=40091}</span></span>                     | <span data-ttu-id="1a9ec-204">\_octets Unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-204">unicode\_bytes</span></span> |
| <span data-ttu-id="1a9ec-205">2</span><span class="sxs-lookup"><span data-stu-id="1a9ec-205">2</span></span>     | <span data-ttu-id="1a9ec-206">/IFD/XMP/ <xmpalt> DC : titre</span><span class="sxs-lookup"><span data-stu-id="1a9ec-206">/ifd/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="1a9ec-207">unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-207">unicode</span></span>        |
| <span data-ttu-id="1a9ec-208">3</span><span class="sxs-lookup"><span data-stu-id="1a9ec-208">3</span></span>     | <span data-ttu-id="1a9ec-209">/IFD/XMP/DC : titre</span><span class="sxs-lookup"><span data-stu-id="1a9ec-209">/ifd/xmp/dc:title</span></span>                       | <span data-ttu-id="1a9ec-210">unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-210">unicode</span></span>        |
| <span data-ttu-id="1a9ec-211">4</span><span class="sxs-lookup"><span data-stu-id="1a9ec-211">4</span></span>     | <span data-ttu-id="1a9ec-212">/IFD/EXIF/{UShort = 37510}</span><span class="sxs-lookup"><span data-stu-id="1a9ec-212">/ifd/exif/{ushort=37510}</span></span>                | <span data-ttu-id="1a9ec-213">unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-213">unicode</span></span>        |
| <span data-ttu-id="1a9ec-214">5</span><span class="sxs-lookup"><span data-stu-id="1a9ec-214">5</span></span>     | <span data-ttu-id="1a9ec-215">/IFD/{UShort = 270}</span><span class="sxs-lookup"><span data-stu-id="1a9ec-215">/ifd/{ushort=270}</span></span>                       | <span data-ttu-id="1a9ec-216">ascii</span><span class="sxs-lookup"><span data-stu-id="1a9ec-216">ascii</span></span>          |
| <span data-ttu-id="1a9ec-217">6</span><span class="sxs-lookup"><span data-stu-id="1a9ec-217">6</span></span>     | <span data-ttu-id="1a9ec-218">/ifd/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="1a9ec-218">/ifd/iptc/caption</span></span>                       |                |
| <span data-ttu-id="1a9ec-219">7</span><span class="sxs-lookup"><span data-stu-id="1a9ec-219">7</span></span>     | <span data-ttu-id="1a9ec-220">/IFD/XMP/ <xmpalt> DC : description</span><span class="sxs-lookup"><span data-stu-id="1a9ec-220">/ifd/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="1a9ec-221">unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-221">unicode</span></span>        |
| <span data-ttu-id="1a9ec-222">8</span><span class="sxs-lookup"><span data-stu-id="1a9ec-222">8</span></span>     | <span data-ttu-id="1a9ec-223">/IFD/XMP/DC : description</span><span class="sxs-lookup"><span data-stu-id="1a9ec-223">/ifd/xmp/dc:description</span></span>                 | <span data-ttu-id="1a9ec-224">unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-224">unicode</span></span>        |
| <span data-ttu-id="1a9ec-225">9</span><span class="sxs-lookup"><span data-stu-id="1a9ec-225">9</span></span>     | <span data-ttu-id="1a9ec-226">/ifd/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="1a9ec-226">/ifd/iptc/caption</span></span>                       |                |
| <span data-ttu-id="1a9ec-227">10</span><span class="sxs-lookup"><span data-stu-id="1a9ec-227">10</span></span>    | <span data-ttu-id="1a9ec-228">/ifd/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="1a9ec-228">/ifd/irb/8bimiptc/iptc/caption</span></span>          |                |
| <span data-ttu-id="1a9ec-229">11</span><span class="sxs-lookup"><span data-stu-id="1a9ec-229">11</span></span>    | <span data-ttu-id="1a9ec-230">/IFD/XMP/ <xmpalt> EXIF : UserComment</span><span class="sxs-lookup"><span data-stu-id="1a9ec-230">/ifd/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="1a9ec-231">unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-231">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="1a9ec-232">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="1a9ec-232">Write Paths</span></span>



| <span data-ttu-id="1a9ec-233">Commande</span><span class="sxs-lookup"><span data-stu-id="1a9ec-233">Order</span></span> | <span data-ttu-id="1a9ec-234">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1a9ec-234">Path</span></span>                                    | <span data-ttu-id="1a9ec-235">Format de disque</span><span class="sxs-lookup"><span data-stu-id="1a9ec-235">Disk Format</span></span>    |
|-------|-----------------------------------------|----------------|
| <span data-ttu-id="1a9ec-236">1</span><span class="sxs-lookup"><span data-stu-id="1a9ec-236">1</span></span>     | <span data-ttu-id="1a9ec-237">/IFD/{UShort = 40091}</span><span class="sxs-lookup"><span data-stu-id="1a9ec-237">/ifd/{ushort=40091}</span></span>                     | <span data-ttu-id="1a9ec-238">\_octets Unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-238">unicode\_bytes</span></span> |
| <span data-ttu-id="1a9ec-239">2</span><span class="sxs-lookup"><span data-stu-id="1a9ec-239">2</span></span>     | <span data-ttu-id="1a9ec-240">/IFD/XMP/DC : titre</span><span class="sxs-lookup"><span data-stu-id="1a9ec-240">/ifd/xmp/dc:title</span></span>                       | <span data-ttu-id="1a9ec-241">unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-241">unicode</span></span>        |
| <span data-ttu-id="1a9ec-242">3</span><span class="sxs-lookup"><span data-stu-id="1a9ec-242">3</span></span>     | <span data-ttu-id="1a9ec-243">/IFD/XMP/ <xmpalt> DC : titre</span><span class="sxs-lookup"><span data-stu-id="1a9ec-243">/ifd/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="1a9ec-244">unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-244">unicode</span></span>        |
| <span data-ttu-id="1a9ec-245">4</span><span class="sxs-lookup"><span data-stu-id="1a9ec-245">4</span></span>     | <span data-ttu-id="1a9ec-246">/IFD/EXIF/{UShort = 37510}</span><span class="sxs-lookup"><span data-stu-id="1a9ec-246">/ifd/exif/{ushort=37510}</span></span>                | <span data-ttu-id="1a9ec-247">unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-247">unicode</span></span>        |
| <span data-ttu-id="1a9ec-248">5</span><span class="sxs-lookup"><span data-stu-id="1a9ec-248">5</span></span>     | <span data-ttu-id="1a9ec-249">/IFD/XMP/ <xmpalt> EXIF : UserComment</span><span class="sxs-lookup"><span data-stu-id="1a9ec-249">/ifd/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="1a9ec-250">unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-250">unicode</span></span>        |
| <span data-ttu-id="1a9ec-251">6</span><span class="sxs-lookup"><span data-stu-id="1a9ec-251">6</span></span>     | <span data-ttu-id="1a9ec-252">/IFD/{UShort = 270}</span><span class="sxs-lookup"><span data-stu-id="1a9ec-252">/ifd/{ushort=270}</span></span>                       | <span data-ttu-id="1a9ec-253">ascii</span><span class="sxs-lookup"><span data-stu-id="1a9ec-253">ascii</span></span>          |
| <span data-ttu-id="1a9ec-254">7</span><span class="sxs-lookup"><span data-stu-id="1a9ec-254">7</span></span>     | <span data-ttu-id="1a9ec-255">/ifd/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="1a9ec-255">/ifd/iptc/caption</span></span>                       |                |
| <span data-ttu-id="1a9ec-256">8</span><span class="sxs-lookup"><span data-stu-id="1a9ec-256">8</span></span>     | <span data-ttu-id="1a9ec-257">/ifd/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="1a9ec-257">/ifd/irb/8bimiptc/iptc/caption</span></span>          |                |
| <span data-ttu-id="1a9ec-258">9</span><span class="sxs-lookup"><span data-stu-id="1a9ec-258">9</span></span>     | <span data-ttu-id="1a9ec-259">/IFD/XMP/DC : description</span><span class="sxs-lookup"><span data-stu-id="1a9ec-259">/ifd/xmp/dc:description</span></span>                 | <span data-ttu-id="1a9ec-260">unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-260">unicode</span></span>        |
| <span data-ttu-id="1a9ec-261">10</span><span class="sxs-lookup"><span data-stu-id="1a9ec-261">10</span></span>    | <span data-ttu-id="1a9ec-262">/IFD/XMP/ <xmpalt> DC : description</span><span class="sxs-lookup"><span data-stu-id="1a9ec-262">/ifd/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="1a9ec-263">unicode</span><span class="sxs-lookup"><span data-stu-id="1a9ec-263">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="1a9ec-264">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="1a9ec-264">Remove Paths</span></span>



| <span data-ttu-id="1a9ec-265">Commande</span><span class="sxs-lookup"><span data-stu-id="1a9ec-265">Order</span></span> | <span data-ttu-id="1a9ec-266">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1a9ec-266">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="1a9ec-267">1</span><span class="sxs-lookup"><span data-stu-id="1a9ec-267">1</span></span>     | <span data-ttu-id="1a9ec-268">/IFD/{UShort = 40091}</span><span class="sxs-lookup"><span data-stu-id="1a9ec-268">/ifd/{ushort=40091}</span></span>                     |
| <span data-ttu-id="1a9ec-269">2</span><span class="sxs-lookup"><span data-stu-id="1a9ec-269">2</span></span>     | <span data-ttu-id="1a9ec-270">/IFD/XMP/DC : titre</span><span class="sxs-lookup"><span data-stu-id="1a9ec-270">/ifd/xmp/dc:title</span></span>                       |
| <span data-ttu-id="1a9ec-271">3</span><span class="sxs-lookup"><span data-stu-id="1a9ec-271">3</span></span>     | <span data-ttu-id="1a9ec-272">/IFD/EXIF/{UShort = 37510}</span><span class="sxs-lookup"><span data-stu-id="1a9ec-272">/ifd/exif/{ushort=37510}</span></span>                |
| <span data-ttu-id="1a9ec-273">4</span><span class="sxs-lookup"><span data-stu-id="1a9ec-273">4</span></span>     | <span data-ttu-id="1a9ec-274">/IFD/XMP/ <xmpalt> EXIF : UserComment</span><span class="sxs-lookup"><span data-stu-id="1a9ec-274">/ifd/xmp/<xmpalt>exif:UserComment</span></span> |
| <span data-ttu-id="1a9ec-275">5</span><span class="sxs-lookup"><span data-stu-id="1a9ec-275">5</span></span>     | <span data-ttu-id="1a9ec-276">/IFD/{UShort = 270}</span><span class="sxs-lookup"><span data-stu-id="1a9ec-276">/ifd/{ushort=270}</span></span>                       |
| <span data-ttu-id="1a9ec-277">6</span><span class="sxs-lookup"><span data-stu-id="1a9ec-277">6</span></span>     | <span data-ttu-id="1a9ec-278">/ifd/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="1a9ec-278">/ifd/iptc/caption</span></span>                       |
| <span data-ttu-id="1a9ec-279">7</span><span class="sxs-lookup"><span data-stu-id="1a9ec-279">7</span></span>     | <span data-ttu-id="1a9ec-280">/ifd/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="1a9ec-280">/ifd/irb/8bimiptc/iptc/caption</span></span>          |
| <span data-ttu-id="1a9ec-281">8</span><span class="sxs-lookup"><span data-stu-id="1a9ec-281">8</span></span>     | <span data-ttu-id="1a9ec-282">/IFD/XMP/DC : description</span><span class="sxs-lookup"><span data-stu-id="1a9ec-282">/ifd/xmp/dc:description</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="1a9ec-283">Notes</span><span class="sxs-lookup"><span data-stu-id="1a9ec-283">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a9ec-284">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1a9ec-284">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a9ec-285">System.Title</span><span class="sxs-lookup"><span data-stu-id="1a9ec-285">System.Title</span></span>](../properties/props-system-title.md)
</dt> </dl>

 

 
