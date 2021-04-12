---
description: Stratégie de métadonnées de la photo pour la propriété System. Keywords.
ms.assetid: bc9de56f-444c-45a2-9822-fba2fe618d38
title: Stratégie de métadonnées de photo System. Keywords
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5d25e7f1919527d474395397d6df62863f7b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210078"
---
# <a name="systemkeywords-photo-metadata-policy"></a><span data-ttu-id="6a98e-103">Stratégie de métadonnées de photo System. Keywords</span><span class="sxs-lookup"><span data-stu-id="6a98e-103">System.Keywords Photo Metadata Policy</span></span>

<span data-ttu-id="6a98e-104">Stratégie de métadonnées de la photo pour la propriété [System. Keywords](../properties/props-system-keywords.md) .</span><span class="sxs-lookup"><span data-stu-id="6a98e-104">The photo metadata policy for the [System.Keywords](../properties/props-system-keywords.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="6a98e-105">A-la</span><span class="sxs-lookup"><span data-stu-id="6a98e-105">PKEY</span></span>

<span data-ttu-id="6a98e-106">\_Mots clés de mot clé</span><span class="sxs-lookup"><span data-stu-id="6a98e-106">PKEY\_Keywords</span></span>

### <a name="containers"></a><span data-ttu-id="6a98e-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="6a98e-107">Containers</span></span>

<span data-ttu-id="6a98e-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="6a98e-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="6a98e-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a98e-109">Read-Only</span></span>

<span data-ttu-id="6a98e-110">Non</span><span class="sxs-lookup"><span data-stu-id="6a98e-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="6a98e-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="6a98e-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="6a98e-112">\_LPWStr VT Vector \| VT \_</span><span class="sxs-lookup"><span data-stu-id="6a98e-112">VT\_VECTOR \| VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="6a98e-113">Type de PROPVARIANT d’entrée</span><span class="sxs-lookup"><span data-stu-id="6a98e-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="6a98e-114">VT \_ Vector \| VT \_ LPWStr est préféré.</span><span class="sxs-lookup"><span data-stu-id="6a98e-114">VT\_VECTOR \| VT\_LPWSTR is preferred.</span></span> <span data-ttu-id="6a98e-115">Un \_ LPWStr VT contenant une chaîne délimitée par des points-virgules est également accepté.</span><span class="sxs-lookup"><span data-stu-id="6a98e-115">A VT\_LPWSTR containing a semicolon-delimited string is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="6a98e-116">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="6a98e-116">Conflict Resolution Policy</span></span>

<span data-ttu-id="6a98e-117">Les valeurs de différents schémas sont fusionnées.</span><span class="sxs-lookup"><span data-stu-id="6a98e-117">Values from different schemas are merged.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="6a98e-118">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="6a98e-118">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="6a98e-119">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="6a98e-119">Read Paths</span></span>



| <span data-ttu-id="6a98e-120">Commande</span><span class="sxs-lookup"><span data-stu-id="6a98e-120">Order</span></span> | <span data-ttu-id="6a98e-121">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="6a98e-121">Path</span></span>                              | <span data-ttu-id="6a98e-122">Format de disque</span><span class="sxs-lookup"><span data-stu-id="6a98e-122">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="6a98e-123">1</span><span class="sxs-lookup"><span data-stu-id="6a98e-123">1</span></span>     | <span data-ttu-id="6a98e-124">/XMP/ <xmpbag> contrôleur de domaine : objet</span><span class="sxs-lookup"><span data-stu-id="6a98e-124">/xmp/<xmpbag>dc:subject</span></span>     | <span data-ttu-id="6a98e-125">unicode</span><span class="sxs-lookup"><span data-stu-id="6a98e-125">unicode</span></span>        |
| <span data-ttu-id="6a98e-126">2</span><span class="sxs-lookup"><span data-stu-id="6a98e-126">2</span></span>     | <span data-ttu-id="6a98e-127">/app13/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="6a98e-127">/app13/irb/8bimiptc/iptc/keywords</span></span> |                |
| <span data-ttu-id="6a98e-128">3</span><span class="sxs-lookup"><span data-stu-id="6a98e-128">3</span></span>     | <span data-ttu-id="6a98e-129">/App1/IFD/{UShort = 18247}</span><span class="sxs-lookup"><span data-stu-id="6a98e-129">/app1/ifd/{ushort=18247}</span></span>          | <span data-ttu-id="6a98e-130">\_octets Unicode</span><span class="sxs-lookup"><span data-stu-id="6a98e-130">unicode\_bytes</span></span> |
| <span data-ttu-id="6a98e-131">4</span><span class="sxs-lookup"><span data-stu-id="6a98e-131">4</span></span>     | <span data-ttu-id="6a98e-132">/App1/IFD/{UShort = 40094}</span><span class="sxs-lookup"><span data-stu-id="6a98e-132">/app1/ifd/{ushort=40094}</span></span>          | <span data-ttu-id="6a98e-133">\_octets Unicode</span><span class="sxs-lookup"><span data-stu-id="6a98e-133">unicode\_bytes</span></span> |



 

### <a name="write-paths"></a><span data-ttu-id="6a98e-134">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="6a98e-134">Write Paths</span></span>



| <span data-ttu-id="6a98e-135">Commande</span><span class="sxs-lookup"><span data-stu-id="6a98e-135">Order</span></span> | <span data-ttu-id="6a98e-136">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="6a98e-136">Path</span></span>                                              | <span data-ttu-id="6a98e-137">Format de disque</span><span class="sxs-lookup"><span data-stu-id="6a98e-137">Disk Format</span></span>    |
|-------|---------------------------------------------------|----------------|
| <span data-ttu-id="6a98e-138">1</span><span class="sxs-lookup"><span data-stu-id="6a98e-138">1</span></span>     | <span data-ttu-id="6a98e-139">/XMP/ <xmpbag> contrôleur de domaine : objet</span><span class="sxs-lookup"><span data-stu-id="6a98e-139">/xmp/<xmpbag>dc:subject</span></span>                     | <span data-ttu-id="6a98e-140">unicode</span><span class="sxs-lookup"><span data-stu-id="6a98e-140">unicode</span></span>        |
| <span data-ttu-id="6a98e-141">2</span><span class="sxs-lookup"><span data-stu-id="6a98e-141">2</span></span>     | <span data-ttu-id="6a98e-142">/app13/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="6a98e-142">/app13/irb/8bimiptc/iptc/keywords</span></span>                 |                |
| <span data-ttu-id="6a98e-143">3</span><span class="sxs-lookup"><span data-stu-id="6a98e-143">3</span></span>     | <span data-ttu-id="6a98e-144">/App1/IFD/{UShort = 18247}</span><span class="sxs-lookup"><span data-stu-id="6a98e-144">/app1/ifd/{ushort=18247}</span></span>                          | <span data-ttu-id="6a98e-145">\_octets Unicode</span><span class="sxs-lookup"><span data-stu-id="6a98e-145">unicode\_bytes</span></span> |
| <span data-ttu-id="6a98e-146">4</span><span class="sxs-lookup"><span data-stu-id="6a98e-146">4</span></span>     | <span data-ttu-id="6a98e-147">/App1/IFD/{UShort = 40094}</span><span class="sxs-lookup"><span data-stu-id="6a98e-147">/app1/ifd/{ushort=40094}</span></span>                          | <span data-ttu-id="6a98e-148">\_octets Unicode</span><span class="sxs-lookup"><span data-stu-id="6a98e-148">unicode\_bytes</span></span> |
| <span data-ttu-id="6a98e-149">5</span><span class="sxs-lookup"><span data-stu-id="6a98e-149">5</span></span>     | <span data-ttu-id="6a98e-150">/XMP/ <xmpbag> MicrosoftPhoto : LastKeywordXMP</span><span class="sxs-lookup"><span data-stu-id="6a98e-150">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>  | <span data-ttu-id="6a98e-151">unicode</span><span class="sxs-lookup"><span data-stu-id="6a98e-151">unicode</span></span>        |
| <span data-ttu-id="6a98e-152">6</span><span class="sxs-lookup"><span data-stu-id="6a98e-152">6</span></span>     | <span data-ttu-id="6a98e-153">/XMP/ <xmpbag> MicrosoftPhoto : LastKeywordIPTC</span><span class="sxs-lookup"><span data-stu-id="6a98e-153">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span> | <span data-ttu-id="6a98e-154">unicode</span><span class="sxs-lookup"><span data-stu-id="6a98e-154">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="6a98e-155">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="6a98e-155">Remove Paths</span></span>



| <span data-ttu-id="6a98e-156">Commande</span><span class="sxs-lookup"><span data-stu-id="6a98e-156">Order</span></span> | <span data-ttu-id="6a98e-157">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="6a98e-157">Path</span></span>                                              |
|-------|---------------------------------------------------|
| <span data-ttu-id="6a98e-158">1</span><span class="sxs-lookup"><span data-stu-id="6a98e-158">1</span></span>     | <span data-ttu-id="6a98e-159">/XMP/DC : objet</span><span class="sxs-lookup"><span data-stu-id="6a98e-159">/xmp/dc:subject</span></span>                                   |
| <span data-ttu-id="6a98e-160">2</span><span class="sxs-lookup"><span data-stu-id="6a98e-160">2</span></span>     | <span data-ttu-id="6a98e-161">/app13/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="6a98e-161">/app13/irb/8bimiptc/iptc/keywords</span></span>                 |
| <span data-ttu-id="6a98e-162">3</span><span class="sxs-lookup"><span data-stu-id="6a98e-162">3</span></span>     | <span data-ttu-id="6a98e-163">/App1/IFD/{UShort = 18247}</span><span class="sxs-lookup"><span data-stu-id="6a98e-163">/app1/ifd/{ushort=18247}</span></span>                          |
| <span data-ttu-id="6a98e-164">4</span><span class="sxs-lookup"><span data-stu-id="6a98e-164">4</span></span>     | <span data-ttu-id="6a98e-165">/App1/IFD/{UShort = 40094}</span><span class="sxs-lookup"><span data-stu-id="6a98e-165">/app1/ifd/{ushort=40094}</span></span>                          |
| <span data-ttu-id="6a98e-166">5</span><span class="sxs-lookup"><span data-stu-id="6a98e-166">5</span></span>     | <span data-ttu-id="6a98e-167">/XMP/ <xmpbag> MicrosoftPhoto : LastKeywordXMP</span><span class="sxs-lookup"><span data-stu-id="6a98e-167">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>  |
| <span data-ttu-id="6a98e-168">6</span><span class="sxs-lookup"><span data-stu-id="6a98e-168">6</span></span>     | <span data-ttu-id="6a98e-169">/XMP/ <xmpbag> MicrosoftPhoto : LastKeywordIPTC</span><span class="sxs-lookup"><span data-stu-id="6a98e-169">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span> |



 

### <a name="tiff-policy"></a><span data-ttu-id="6a98e-170">Stratégie TIFF</span><span class="sxs-lookup"><span data-stu-id="6a98e-170">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="6a98e-171">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="6a98e-171">Read Paths</span></span>



| <span data-ttu-id="6a98e-172">Commande</span><span class="sxs-lookup"><span data-stu-id="6a98e-172">Order</span></span> | <span data-ttu-id="6a98e-173">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="6a98e-173">Path</span></span>                              | <span data-ttu-id="6a98e-174">Format de disque</span><span class="sxs-lookup"><span data-stu-id="6a98e-174">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="6a98e-175">1</span><span class="sxs-lookup"><span data-stu-id="6a98e-175">1</span></span>     | <span data-ttu-id="6a98e-176">/IFD/XMP/ <xmpbag> contrôleur de domaine : objet</span><span class="sxs-lookup"><span data-stu-id="6a98e-176">/ifd/xmp/<xmpbag>dc:subject</span></span> | <span data-ttu-id="6a98e-177">unicode</span><span class="sxs-lookup"><span data-stu-id="6a98e-177">unicode</span></span>        |
| <span data-ttu-id="6a98e-178">2</span><span class="sxs-lookup"><span data-stu-id="6a98e-178">2</span></span>     | <span data-ttu-id="6a98e-179">/ifd/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="6a98e-179">/ifd/iptc/keywords</span></span>                |                |
| <span data-ttu-id="6a98e-180">3</span><span class="sxs-lookup"><span data-stu-id="6a98e-180">3</span></span>     | <span data-ttu-id="6a98e-181">/IFD/{UShort = 18247}</span><span class="sxs-lookup"><span data-stu-id="6a98e-181">/ifd/{ushort=18247}</span></span>               | <span data-ttu-id="6a98e-182">\_octets Unicode</span><span class="sxs-lookup"><span data-stu-id="6a98e-182">unicode\_bytes</span></span> |
| <span data-ttu-id="6a98e-183">4</span><span class="sxs-lookup"><span data-stu-id="6a98e-183">4</span></span>     | <span data-ttu-id="6a98e-184">/IFD/{UShort = 40094}</span><span class="sxs-lookup"><span data-stu-id="6a98e-184">/ifd/{ushort=40094}</span></span>               | <span data-ttu-id="6a98e-185">\_octets Unicode</span><span class="sxs-lookup"><span data-stu-id="6a98e-185">unicode\_bytes</span></span> |
| <span data-ttu-id="6a98e-186">5</span><span class="sxs-lookup"><span data-stu-id="6a98e-186">5</span></span>     | <span data-ttu-id="6a98e-187">/ifd/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="6a98e-187">/ifd/irb/8bimiptc/iptc/keywords</span></span>   |                |



 

### <a name="write-paths"></a><span data-ttu-id="6a98e-188">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="6a98e-188">Write Paths</span></span>



| <span data-ttu-id="6a98e-189">Commande</span><span class="sxs-lookup"><span data-stu-id="6a98e-189">Order</span></span> | <span data-ttu-id="6a98e-190">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="6a98e-190">Path</span></span>                                                             | <span data-ttu-id="6a98e-191">Format de disque</span><span class="sxs-lookup"><span data-stu-id="6a98e-191">Disk Format</span></span>    |
|-------|------------------------------------------------------------------|----------------|
| <span data-ttu-id="6a98e-192">1</span><span class="sxs-lookup"><span data-stu-id="6a98e-192">1</span></span>     | <span data-ttu-id="6a98e-193">/IFD/XMP/ <xmpbag> contrôleur de domaine : objet</span><span class="sxs-lookup"><span data-stu-id="6a98e-193">/ifd/xmp/<xmpbag>dc:subject</span></span>                                | <span data-ttu-id="6a98e-194">unicode</span><span class="sxs-lookup"><span data-stu-id="6a98e-194">unicode</span></span>        |
| <span data-ttu-id="6a98e-195">2</span><span class="sxs-lookup"><span data-stu-id="6a98e-195">2</span></span>     | <span data-ttu-id="6a98e-196">/ifd/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="6a98e-196">/ifd/iptc/keywords</span></span>                                               |                |
| <span data-ttu-id="6a98e-197">3</span><span class="sxs-lookup"><span data-stu-id="6a98e-197">3</span></span>     | <span data-ttu-id="6a98e-198">/ifd/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="6a98e-198">/ifd/irb/8bimiptc/iptc/keywords</span></span>                                  |                |
| <span data-ttu-id="6a98e-199">4</span><span class="sxs-lookup"><span data-stu-id="6a98e-199">4</span></span>     | <span data-ttu-id="6a98e-200">/IFD/{UShort = 18247}</span><span class="sxs-lookup"><span data-stu-id="6a98e-200">/ifd/{ushort=18247}</span></span>                                              | <span data-ttu-id="6a98e-201">\_octets Unicode</span><span class="sxs-lookup"><span data-stu-id="6a98e-201">unicode\_bytes</span></span> |
| <span data-ttu-id="6a98e-202">5</span><span class="sxs-lookup"><span data-stu-id="6a98e-202">5</span></span>     | <span data-ttu-id="6a98e-203">/IFD/{UShort = 40094}</span><span class="sxs-lookup"><span data-stu-id="6a98e-203">/ifd/{ushort=40094}</span></span>                                              | <span data-ttu-id="6a98e-204">\_octets Unicode</span><span class="sxs-lookup"><span data-stu-id="6a98e-204">unicode\_bytes</span></span> |
| <span data-ttu-id="6a98e-205">6</span><span class="sxs-lookup"><span data-stu-id="6a98e-205">6</span></span>     | <span data-ttu-id="6a98e-206">/IFD/XMP/ <xmpbag> MicrosoftPhoto : LastKeywordXMP</span><span class="sxs-lookup"><span data-stu-id="6a98e-206">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>             | <span data-ttu-id="6a98e-207">unicode</span><span class="sxs-lookup"><span data-stu-id="6a98e-207">unicode</span></span>        |
| <span data-ttu-id="6a98e-208">7</span><span class="sxs-lookup"><span data-stu-id="6a98e-208">7</span></span>     | <span data-ttu-id="6a98e-209">/IFD/XMP/ <xmpbag> MicrosoftPhoto : LastKeywordIPTC</span><span class="sxs-lookup"><span data-stu-id="6a98e-209">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span>            | <span data-ttu-id="6a98e-210">unicode</span><span class="sxs-lookup"><span data-stu-id="6a98e-210">unicode</span></span>        |
| <span data-ttu-id="6a98e-211">8</span><span class="sxs-lookup"><span data-stu-id="6a98e-211">8</span></span>     | <span data-ttu-id="6a98e-212">/IFD/XMP/ <xmpbag> MicrosoftPhoto : LastKeywordIPTC \_ TIFF \_ IRB</span><span class="sxs-lookup"><span data-stu-id="6a98e-212">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC\_TIFF\_IRB</span></span> | <span data-ttu-id="6a98e-213">unicode</span><span class="sxs-lookup"><span data-stu-id="6a98e-213">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="6a98e-214">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="6a98e-214">Remove Paths</span></span>



| <span data-ttu-id="6a98e-215">Commande</span><span class="sxs-lookup"><span data-stu-id="6a98e-215">Order</span></span> | <span data-ttu-id="6a98e-216">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="6a98e-216">Path</span></span>                                                             |
|-------|------------------------------------------------------------------|
| <span data-ttu-id="6a98e-217">1</span><span class="sxs-lookup"><span data-stu-id="6a98e-217">1</span></span>     | <span data-ttu-id="6a98e-218">/IFD/XMP/DC : objet</span><span class="sxs-lookup"><span data-stu-id="6a98e-218">/ifd/xmp/dc:subject</span></span>                                              |
| <span data-ttu-id="6a98e-219">2</span><span class="sxs-lookup"><span data-stu-id="6a98e-219">2</span></span>     | <span data-ttu-id="6a98e-220">/ifd/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="6a98e-220">/ifd/iptc/keywords</span></span>                                               |
| <span data-ttu-id="6a98e-221">3</span><span class="sxs-lookup"><span data-stu-id="6a98e-221">3</span></span>     | <span data-ttu-id="6a98e-222">/ifd/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="6a98e-222">/ifd/irb/8bimiptc/iptc/keywords</span></span>                                  |
| <span data-ttu-id="6a98e-223">4</span><span class="sxs-lookup"><span data-stu-id="6a98e-223">4</span></span>     | <span data-ttu-id="6a98e-224">/IFD/{UShort = 18247}</span><span class="sxs-lookup"><span data-stu-id="6a98e-224">/ifd/{ushort=18247}</span></span>                                              |
| <span data-ttu-id="6a98e-225">5</span><span class="sxs-lookup"><span data-stu-id="6a98e-225">5</span></span>     | <span data-ttu-id="6a98e-226">/IFD/{UShort = 40094}</span><span class="sxs-lookup"><span data-stu-id="6a98e-226">/ifd/{ushort=40094}</span></span>                                              |
| <span data-ttu-id="6a98e-227">6</span><span class="sxs-lookup"><span data-stu-id="6a98e-227">6</span></span>     | <span data-ttu-id="6a98e-228">/IFD/XMP/ <xmpbag> MicrosoftPhoto : LastKeywordXMP</span><span class="sxs-lookup"><span data-stu-id="6a98e-228">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>             |
| <span data-ttu-id="6a98e-229">7</span><span class="sxs-lookup"><span data-stu-id="6a98e-229">7</span></span>     | <span data-ttu-id="6a98e-230">/IFD/XMP/ <xmpbag> MicrosoftPhoto : LastKeywordIPTC</span><span class="sxs-lookup"><span data-stu-id="6a98e-230">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span>            |
| <span data-ttu-id="6a98e-231">8</span><span class="sxs-lookup"><span data-stu-id="6a98e-231">8</span></span>     | <span data-ttu-id="6a98e-232">/IFD/XMP/ <xmpbag> MicrosoftPhoto : LastKeywordIPTC \_ TIFF \_ IRB</span><span class="sxs-lookup"><span data-stu-id="6a98e-232">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC\_TIFF\_IRB</span></span> |



 

### <a name="remarks"></a><span data-ttu-id="6a98e-233">Notes</span><span class="sxs-lookup"><span data-stu-id="6a98e-233">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a98e-234">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6a98e-234">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a98e-235">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="6a98e-235">System.Keywords</span></span>](../properties/props-system-keywords.md)
</dt> </dl>

 

 
