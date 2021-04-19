---
description: Stratégie de métadonnées de la photo pour la propriété System. Author.
ms.assetid: 2de9c452-93be-40a4-a72b-5da590534dfd
title: Stratégie de métadonnées de photos System. Author
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb90345257ef1623f7cda1ce4318af7a9f472df5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541981"
---
# <a name="systemauthor-photo-metadata-policy"></a><span data-ttu-id="13e5a-103">Stratégie de métadonnées de photos System. Author</span><span class="sxs-lookup"><span data-stu-id="13e5a-103">System.Author Photo Metadata Policy</span></span>

<span data-ttu-id="13e5a-104">Stratégie de métadonnées de la photo pour la propriété [System. Author](../properties/props-system-author.md) .</span><span class="sxs-lookup"><span data-stu-id="13e5a-104">The photo metadata policy for the [System.Author](../properties/props-system-author.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="13e5a-105">A-la</span><span class="sxs-lookup"><span data-stu-id="13e5a-105">PKEY</span></span>

<span data-ttu-id="13e5a-106">Auteur de la définition de l’écriture \_</span><span class="sxs-lookup"><span data-stu-id="13e5a-106">PKEY\_Author</span></span>

### <a name="containers"></a><span data-ttu-id="13e5a-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="13e5a-107">Containers</span></span>

<span data-ttu-id="13e5a-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="13e5a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="13e5a-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13e5a-109">Read-Only</span></span>

<span data-ttu-id="13e5a-110">Non</span><span class="sxs-lookup"><span data-stu-id="13e5a-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="13e5a-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="13e5a-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="13e5a-112">\_LPWStr VT Vector \| VT \_</span><span class="sxs-lookup"><span data-stu-id="13e5a-112">VT\_VECTOR \| VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="13e5a-113">Type de PROPVARIANT d’entrée</span><span class="sxs-lookup"><span data-stu-id="13e5a-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="13e5a-114">VT \_ Vector \| VT \_ LPWStr est préféré, mais VT \_ LPWStr est également accepté.</span><span class="sxs-lookup"><span data-stu-id="13e5a-114">VT\_VECTOR \| VT\_LPWSTR is preferred, but VT\_LPWSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="13e5a-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="13e5a-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="13e5a-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="13e5a-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="13e5a-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="13e5a-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="13e5a-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="13e5a-118">Read Paths</span></span>



| <span data-ttu-id="13e5a-119">Commande</span><span class="sxs-lookup"><span data-stu-id="13e5a-119">Order</span></span> | <span data-ttu-id="13e5a-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="13e5a-120">Path</span></span>                             | <span data-ttu-id="13e5a-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="13e5a-121">Disk Format</span></span>    |
|-------|----------------------------------|----------------|
| <span data-ttu-id="13e5a-122">1</span><span class="sxs-lookup"><span data-stu-id="13e5a-122">1</span></span>     | <span data-ttu-id="13e5a-123">/App1/IFD/{UShort = 315}</span><span class="sxs-lookup"><span data-stu-id="13e5a-123">/app1/ifd/{ushort=315}</span></span>           | <span data-ttu-id="13e5a-124">ascii</span><span class="sxs-lookup"><span data-stu-id="13e5a-124">ascii</span></span>          |
| <span data-ttu-id="13e5a-125">2</span><span class="sxs-lookup"><span data-stu-id="13e5a-125">2</span></span>     | <span data-ttu-id="13e5a-126">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="13e5a-126">/app13/irb/8bimiptc/iptc/by-line</span></span> |                |
| <span data-ttu-id="13e5a-127">3</span><span class="sxs-lookup"><span data-stu-id="13e5a-127">3</span></span>     | <span data-ttu-id="13e5a-128">/XMP/ <xmpseq> DC : Creator</span><span class="sxs-lookup"><span data-stu-id="13e5a-128">/xmp/<xmpseq>dc:creator</span></span>    | <span data-ttu-id="13e5a-129">unicode</span><span class="sxs-lookup"><span data-stu-id="13e5a-129">unicode</span></span>        |
| <span data-ttu-id="13e5a-130">4</span><span class="sxs-lookup"><span data-stu-id="13e5a-130">4</span></span>     | <span data-ttu-id="13e5a-131">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="13e5a-131">/app13/irb/8bimiptc/iptc/by-line</span></span> |                |
| <span data-ttu-id="13e5a-132">5</span><span class="sxs-lookup"><span data-stu-id="13e5a-132">5</span></span>     | <span data-ttu-id="13e5a-133">/App1/IFD/{UShort = 40093}</span><span class="sxs-lookup"><span data-stu-id="13e5a-133">/app1/ifd/{ushort=40093}</span></span>         | <span data-ttu-id="13e5a-134">\_octets Unicode</span><span class="sxs-lookup"><span data-stu-id="13e5a-134">unicode\_bytes</span></span> |
| <span data-ttu-id="13e5a-135">6</span><span class="sxs-lookup"><span data-stu-id="13e5a-135">6</span></span>     | <span data-ttu-id="13e5a-136">/XMP/TIFF : artiste</span><span class="sxs-lookup"><span data-stu-id="13e5a-136">/xmp/tiff:artist</span></span>                 | <span data-ttu-id="13e5a-137">unicode</span><span class="sxs-lookup"><span data-stu-id="13e5a-137">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="13e5a-138">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="13e5a-138">Write Paths</span></span>



| <span data-ttu-id="13e5a-139">Commande</span><span class="sxs-lookup"><span data-stu-id="13e5a-139">Order</span></span> | <span data-ttu-id="13e5a-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="13e5a-140">Path</span></span>                             | <span data-ttu-id="13e5a-141">Format de disque</span><span class="sxs-lookup"><span data-stu-id="13e5a-141">Disk Format</span></span>    |
|-------|----------------------------------|----------------|
| <span data-ttu-id="13e5a-142">1</span><span class="sxs-lookup"><span data-stu-id="13e5a-142">1</span></span>     | <span data-ttu-id="13e5a-143">/XMP/ <xmpseq> DC : Creator</span><span class="sxs-lookup"><span data-stu-id="13e5a-143">/xmp/<xmpseq>dc:creator</span></span>    | <span data-ttu-id="13e5a-144">unicode</span><span class="sxs-lookup"><span data-stu-id="13e5a-144">unicode</span></span>        |
| <span data-ttu-id="13e5a-145">2</span><span class="sxs-lookup"><span data-stu-id="13e5a-145">2</span></span>     | <span data-ttu-id="13e5a-146">/XMP/TIFF : artiste</span><span class="sxs-lookup"><span data-stu-id="13e5a-146">/xmp/tiff:artist</span></span>                 | <span data-ttu-id="13e5a-147">unicode</span><span class="sxs-lookup"><span data-stu-id="13e5a-147">unicode</span></span>        |
| <span data-ttu-id="13e5a-148">3</span><span class="sxs-lookup"><span data-stu-id="13e5a-148">3</span></span>     | <span data-ttu-id="13e5a-149">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="13e5a-149">/app13/irb/8bimiptc/iptc/by-line</span></span> |                |
| <span data-ttu-id="13e5a-150">4</span><span class="sxs-lookup"><span data-stu-id="13e5a-150">4</span></span>     | <span data-ttu-id="13e5a-151">/App1/IFD/{UShort = 315}</span><span class="sxs-lookup"><span data-stu-id="13e5a-151">/app1/ifd/{ushort=315}</span></span>           | <span data-ttu-id="13e5a-152">ascii</span><span class="sxs-lookup"><span data-stu-id="13e5a-152">ascii</span></span>          |
| <span data-ttu-id="13e5a-153">5</span><span class="sxs-lookup"><span data-stu-id="13e5a-153">5</span></span>     | <span data-ttu-id="13e5a-154">/App1/IFD/{UShort = 40093}</span><span class="sxs-lookup"><span data-stu-id="13e5a-154">/app1/ifd/{ushort=40093}</span></span>         | <span data-ttu-id="13e5a-155">\_octets Unicode</span><span class="sxs-lookup"><span data-stu-id="13e5a-155">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="13e5a-156">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="13e5a-156">Remove Paths</span></span>



| <span data-ttu-id="13e5a-157">Commande</span><span class="sxs-lookup"><span data-stu-id="13e5a-157">Order</span></span> | <span data-ttu-id="13e5a-158">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="13e5a-158">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="13e5a-159">1</span><span class="sxs-lookup"><span data-stu-id="13e5a-159">1</span></span>     | <span data-ttu-id="13e5a-160">/XMP/DC : Creator</span><span class="sxs-lookup"><span data-stu-id="13e5a-160">/xmp/dc:creator</span></span>                  |
| <span data-ttu-id="13e5a-161">2</span><span class="sxs-lookup"><span data-stu-id="13e5a-161">2</span></span>     | <span data-ttu-id="13e5a-162">/XMP/TIFF : artiste</span><span class="sxs-lookup"><span data-stu-id="13e5a-162">/xmp/tiff:artist</span></span>                 |
| <span data-ttu-id="13e5a-163">3</span><span class="sxs-lookup"><span data-stu-id="13e5a-163">3</span></span>     | <span data-ttu-id="13e5a-164">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="13e5a-164">/app13/irb/8bimiptc/iptc/by-line</span></span> |
| <span data-ttu-id="13e5a-165">4</span><span class="sxs-lookup"><span data-stu-id="13e5a-165">4</span></span>     | <span data-ttu-id="13e5a-166">/App1/IFD/{UShort = 315}</span><span class="sxs-lookup"><span data-stu-id="13e5a-166">/app1/ifd/{ushort=315}</span></span>           |
| <span data-ttu-id="13e5a-167">5</span><span class="sxs-lookup"><span data-stu-id="13e5a-167">5</span></span>     | <span data-ttu-id="13e5a-168">/App1/IFD/{UShort = 40093}</span><span class="sxs-lookup"><span data-stu-id="13e5a-168">/app1/ifd/{ushort=40093}</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="13e5a-169">Stratégie TIFF</span><span class="sxs-lookup"><span data-stu-id="13e5a-169">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="13e5a-170">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="13e5a-170">Read Paths</span></span>



| <span data-ttu-id="13e5a-171">Commande</span><span class="sxs-lookup"><span data-stu-id="13e5a-171">Order</span></span> | <span data-ttu-id="13e5a-172">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="13e5a-172">Path</span></span>                              | <span data-ttu-id="13e5a-173">Format de disque</span><span class="sxs-lookup"><span data-stu-id="13e5a-173">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="13e5a-174">1</span><span class="sxs-lookup"><span data-stu-id="13e5a-174">1</span></span>     | <span data-ttu-id="13e5a-175">/IFD/{UShort = 315}</span><span class="sxs-lookup"><span data-stu-id="13e5a-175">/ifd/{ushort=315}</span></span>                 | <span data-ttu-id="13e5a-176">ascii</span><span class="sxs-lookup"><span data-stu-id="13e5a-176">ascii</span></span>          |
| <span data-ttu-id="13e5a-177">2</span><span class="sxs-lookup"><span data-stu-id="13e5a-177">2</span></span>     | <span data-ttu-id="13e5a-178">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="13e5a-178">/ifd/iptc/by-line</span></span>                 |                |
| <span data-ttu-id="13e5a-179">3</span><span class="sxs-lookup"><span data-stu-id="13e5a-179">3</span></span>     | <span data-ttu-id="13e5a-180">/IFD/XMP/ <xmpseq> DC : Creator</span><span class="sxs-lookup"><span data-stu-id="13e5a-180">/ifd/xmp/<xmpseq>dc:creator</span></span> | <span data-ttu-id="13e5a-181">unicode</span><span class="sxs-lookup"><span data-stu-id="13e5a-181">unicode</span></span>        |
| <span data-ttu-id="13e5a-182">4</span><span class="sxs-lookup"><span data-stu-id="13e5a-182">4</span></span>     | <span data-ttu-id="13e5a-183">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="13e5a-183">/ifd/iptc/by-line</span></span>                 |                |
| <span data-ttu-id="13e5a-184">5</span><span class="sxs-lookup"><span data-stu-id="13e5a-184">5</span></span>     | <span data-ttu-id="13e5a-185">/IFD/{UShort = 40093}</span><span class="sxs-lookup"><span data-stu-id="13e5a-185">/ifd/{ushort=40093}</span></span>               | <span data-ttu-id="13e5a-186">\_octets Unicode</span><span class="sxs-lookup"><span data-stu-id="13e5a-186">unicode\_bytes</span></span> |
| <span data-ttu-id="13e5a-187">6</span><span class="sxs-lookup"><span data-stu-id="13e5a-187">6</span></span>     | <span data-ttu-id="13e5a-188">/ifd/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="13e5a-188">/ifd/irb/8bimiptc/iptc/by-line</span></span>    |                |
| <span data-ttu-id="13e5a-189">7</span><span class="sxs-lookup"><span data-stu-id="13e5a-189">7</span></span>     | <span data-ttu-id="13e5a-190">/IFD/XMP/TIFF : artiste</span><span class="sxs-lookup"><span data-stu-id="13e5a-190">/ifd/xmp/tiff:artist</span></span>              | <span data-ttu-id="13e5a-191">unicode</span><span class="sxs-lookup"><span data-stu-id="13e5a-191">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="13e5a-192">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="13e5a-192">Write Paths</span></span>



| <span data-ttu-id="13e5a-193">Commande</span><span class="sxs-lookup"><span data-stu-id="13e5a-193">Order</span></span> | <span data-ttu-id="13e5a-194">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="13e5a-194">Path</span></span>                              | <span data-ttu-id="13e5a-195">Format de disque</span><span class="sxs-lookup"><span data-stu-id="13e5a-195">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="13e5a-196">1</span><span class="sxs-lookup"><span data-stu-id="13e5a-196">1</span></span>     | <span data-ttu-id="13e5a-197">/IFD/XMP/ <xmpseq> DC : Creator</span><span class="sxs-lookup"><span data-stu-id="13e5a-197">/ifd/xmp/<xmpseq>dc:creator</span></span> | <span data-ttu-id="13e5a-198">unicode</span><span class="sxs-lookup"><span data-stu-id="13e5a-198">unicode</span></span>        |
| <span data-ttu-id="13e5a-199">2</span><span class="sxs-lookup"><span data-stu-id="13e5a-199">2</span></span>     | <span data-ttu-id="13e5a-200">/IFD/XMP/TIFF : artiste</span><span class="sxs-lookup"><span data-stu-id="13e5a-200">/ifd/xmp/tiff:artist</span></span>              | <span data-ttu-id="13e5a-201">unicode</span><span class="sxs-lookup"><span data-stu-id="13e5a-201">unicode</span></span>        |
| <span data-ttu-id="13e5a-202">3</span><span class="sxs-lookup"><span data-stu-id="13e5a-202">3</span></span>     | <span data-ttu-id="13e5a-203">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="13e5a-203">/ifd/iptc/by-line</span></span>                 |                |
| <span data-ttu-id="13e5a-204">4</span><span class="sxs-lookup"><span data-stu-id="13e5a-204">4</span></span>     | <span data-ttu-id="13e5a-205">/IFD/{UShort = 315}</span><span class="sxs-lookup"><span data-stu-id="13e5a-205">/ifd/{ushort=315}</span></span>                 | <span data-ttu-id="13e5a-206">\_vecteur ASCII</span><span class="sxs-lookup"><span data-stu-id="13e5a-206">ascii\_vector</span></span>  |
| <span data-ttu-id="13e5a-207">5</span><span class="sxs-lookup"><span data-stu-id="13e5a-207">5</span></span>     | <span data-ttu-id="13e5a-208">/IFD/{UShort = 40093}</span><span class="sxs-lookup"><span data-stu-id="13e5a-208">/ifd/{ushort=40093}</span></span>               | <span data-ttu-id="13e5a-209">\_octets Unicode</span><span class="sxs-lookup"><span data-stu-id="13e5a-209">unicode\_bytes</span></span> |
| <span data-ttu-id="13e5a-210">6</span><span class="sxs-lookup"><span data-stu-id="13e5a-210">6</span></span>     | <span data-ttu-id="13e5a-211">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="13e5a-211">/ifd/iptc/by-line</span></span>                 |                |



 

### <a name="remove-paths"></a><span data-ttu-id="13e5a-212">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="13e5a-212">Remove Paths</span></span>



| <span data-ttu-id="13e5a-213">Commande</span><span class="sxs-lookup"><span data-stu-id="13e5a-213">Order</span></span> | <span data-ttu-id="13e5a-214">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="13e5a-214">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="13e5a-215">1</span><span class="sxs-lookup"><span data-stu-id="13e5a-215">1</span></span>     | <span data-ttu-id="13e5a-216">/IFD/XMP/DC : Creator</span><span class="sxs-lookup"><span data-stu-id="13e5a-216">/ifd/xmp/dc:creator</span></span>            |
| <span data-ttu-id="13e5a-217">2</span><span class="sxs-lookup"><span data-stu-id="13e5a-217">2</span></span>     | <span data-ttu-id="13e5a-218">/IFD/XMP/TIFF : artiste</span><span class="sxs-lookup"><span data-stu-id="13e5a-218">/ifd/xmp/tiff:artist</span></span>           |
| <span data-ttu-id="13e5a-219">3</span><span class="sxs-lookup"><span data-stu-id="13e5a-219">3</span></span>     | <span data-ttu-id="13e5a-220">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="13e5a-220">/ifd/iptc/by-line</span></span>              |
| <span data-ttu-id="13e5a-221">4</span><span class="sxs-lookup"><span data-stu-id="13e5a-221">4</span></span>     | <span data-ttu-id="13e5a-222">/ifd/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="13e5a-222">/ifd/irb/8bimiptc/iptc/by-line</span></span> |
| <span data-ttu-id="13e5a-223">5</span><span class="sxs-lookup"><span data-stu-id="13e5a-223">5</span></span>     | <span data-ttu-id="13e5a-224">/IFD/{UShort = 315}</span><span class="sxs-lookup"><span data-stu-id="13e5a-224">/ifd/{ushort=315}</span></span>              |
| <span data-ttu-id="13e5a-225">6</span><span class="sxs-lookup"><span data-stu-id="13e5a-225">6</span></span>     | <span data-ttu-id="13e5a-226">/IFD/{UShort = 40093}</span><span class="sxs-lookup"><span data-stu-id="13e5a-226">/ifd/{ushort=40093}</span></span>            |



 

### <a name="remarks"></a><span data-ttu-id="13e5a-227">Notes</span><span class="sxs-lookup"><span data-stu-id="13e5a-227">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="13e5a-228">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="13e5a-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13e5a-229">System.Author</span><span class="sxs-lookup"><span data-stu-id="13e5a-229">System.Author</span></span>](../properties/props-system-author.md)
</dt> </dl>

 

 
