---
description: Stratégie de métadonnées de la photo pour la propriété System. Comment.
ms.assetid: 02a6ac18-ad69-4880-a267-8330d648c0d9
title: Stratégie de métadonnées de la photo System. Comment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9d7526e05a72b073ac32bd8286a621b33ee62a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320414"
---
# <a name="systemcomment-photo-metadata-policy"></a><span data-ttu-id="cd1a6-103">Stratégie de métadonnées de la photo System. Comment</span><span class="sxs-lookup"><span data-stu-id="cd1a6-103">System.Comment Photo Metadata Policy</span></span>

<span data-ttu-id="cd1a6-104">Stratégie de métadonnées de la photo pour la propriété [System. Comment](../properties/props-system-comment.md) .</span><span class="sxs-lookup"><span data-stu-id="cd1a6-104">The photo metadata policy for the [System.Comment](../properties/props-system-comment.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="cd1a6-105">A-la</span><span class="sxs-lookup"><span data-stu-id="cd1a6-105">PKEY</span></span>

<span data-ttu-id="cd1a6-106">Commentaire de la barre d’ajout \_</span><span class="sxs-lookup"><span data-stu-id="cd1a6-106">PKEY\_Comment</span></span>

### <a name="containers"></a><span data-ttu-id="cd1a6-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="cd1a6-107">Containers</span></span>

<span data-ttu-id="cd1a6-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="cd1a6-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="cd1a6-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd1a6-109">Read-Only</span></span>

<span data-ttu-id="cd1a6-110">Non</span><span class="sxs-lookup"><span data-stu-id="cd1a6-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="cd1a6-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="cd1a6-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="cd1a6-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="cd1a6-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="cd1a6-113">Type de PROPVARIANT d’entrée</span><span class="sxs-lookup"><span data-stu-id="cd1a6-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="cd1a6-114">VT \_ LPWStr ou VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="cd1a6-114">VT\_LPWSTR or VT\_LPSTR</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="cd1a6-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="cd1a6-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="cd1a6-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="cd1a6-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="cd1a6-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="cd1a6-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="cd1a6-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="cd1a6-118">Read Paths</span></span>



| <span data-ttu-id="cd1a6-119">Commande</span><span class="sxs-lookup"><span data-stu-id="cd1a6-119">Order</span></span> | <span data-ttu-id="cd1a6-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="cd1a6-120">Path</span></span>                                | <span data-ttu-id="cd1a6-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="cd1a6-121">Disk Format</span></span>    |
|-------|-------------------------------------|----------------|
| <span data-ttu-id="cd1a6-122">1</span><span class="sxs-lookup"><span data-stu-id="cd1a6-122">1</span></span>     | <span data-ttu-id="cd1a6-123">/App1/IFD/{UShort = 40092}</span><span class="sxs-lookup"><span data-stu-id="cd1a6-123">/app1/ifd/{ushort=40092}</span></span>            | <span data-ttu-id="cd1a6-124">\_octets Unicode</span><span class="sxs-lookup"><span data-stu-id="cd1a6-124">unicode\_bytes</span></span> |
| <span data-ttu-id="cd1a6-125">2</span><span class="sxs-lookup"><span data-stu-id="cd1a6-125">2</span></span>     | <span data-ttu-id="cd1a6-126">/App1/IFD/{UShort = 37510}</span><span class="sxs-lookup"><span data-stu-id="cd1a6-126">/app1/ifd/{ushort=37510}</span></span>            | <span data-ttu-id="cd1a6-127">unicode</span><span class="sxs-lookup"><span data-stu-id="cd1a6-127">unicode</span></span>        |
| <span data-ttu-id="cd1a6-128">3</span><span class="sxs-lookup"><span data-stu-id="cd1a6-128">3</span></span>     | <span data-ttu-id="cd1a6-129">/XMP/ <xmpalt> EXIF : UserComment</span><span class="sxs-lookup"><span data-stu-id="cd1a6-129">/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="cd1a6-130">unicode</span><span class="sxs-lookup"><span data-stu-id="cd1a6-130">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="cd1a6-131">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="cd1a6-131">Write Paths</span></span>



| <span data-ttu-id="cd1a6-132">Commande</span><span class="sxs-lookup"><span data-stu-id="cd1a6-132">Order</span></span> | <span data-ttu-id="cd1a6-133">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="cd1a6-133">Path</span></span>                     | <span data-ttu-id="cd1a6-134">Format de disque</span><span class="sxs-lookup"><span data-stu-id="cd1a6-134">Disk Format</span></span>    |
|-------|--------------------------|----------------|
| <span data-ttu-id="cd1a6-135">1</span><span class="sxs-lookup"><span data-stu-id="cd1a6-135">1</span></span>     | <span data-ttu-id="cd1a6-136">/App1/IFD/{UShort = 40092}</span><span class="sxs-lookup"><span data-stu-id="cd1a6-136">/app1/ifd/{ushort=40092}</span></span> | <span data-ttu-id="cd1a6-137">\_octets Unicode</span><span class="sxs-lookup"><span data-stu-id="cd1a6-137">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="cd1a6-138">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="cd1a6-138">Remove Paths</span></span>



| <span data-ttu-id="cd1a6-139">Commande</span><span class="sxs-lookup"><span data-stu-id="cd1a6-139">Order</span></span> | <span data-ttu-id="cd1a6-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="cd1a6-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="cd1a6-141">1</span><span class="sxs-lookup"><span data-stu-id="cd1a6-141">1</span></span>     | <span data-ttu-id="cd1a6-142">/App1/IFD/{UShort = 40092}</span><span class="sxs-lookup"><span data-stu-id="cd1a6-142">/app1/ifd/{ushort=40092}</span></span>      |
| <span data-ttu-id="cd1a6-143">2</span><span class="sxs-lookup"><span data-stu-id="cd1a6-143">2</span></span>     | <span data-ttu-id="cd1a6-144">/App1/IFD/EXIF/{UShort = 37510}</span><span class="sxs-lookup"><span data-stu-id="cd1a6-144">/app1/ifd/exif/{ushort=37510}</span></span> |
| <span data-ttu-id="cd1a6-145">3</span><span class="sxs-lookup"><span data-stu-id="cd1a6-145">3</span></span>     | <span data-ttu-id="cd1a6-146">/xmp/exif:UserComment</span><span class="sxs-lookup"><span data-stu-id="cd1a6-146">/xmp/exif:UserComment</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="cd1a6-147">Stratégie TIFF</span><span class="sxs-lookup"><span data-stu-id="cd1a6-147">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="cd1a6-148">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="cd1a6-148">Read Paths</span></span>



| <span data-ttu-id="cd1a6-149">Commande</span><span class="sxs-lookup"><span data-stu-id="cd1a6-149">Order</span></span> | <span data-ttu-id="cd1a6-150">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="cd1a6-150">Path</span></span>                                    | <span data-ttu-id="cd1a6-151">Format de disque</span><span class="sxs-lookup"><span data-stu-id="cd1a6-151">Disk Format</span></span>    |
|-------|-----------------------------------------|----------------|
| <span data-ttu-id="cd1a6-152">1</span><span class="sxs-lookup"><span data-stu-id="cd1a6-152">1</span></span>     | <span data-ttu-id="cd1a6-153">/IFD/{UShort = 40092}</span><span class="sxs-lookup"><span data-stu-id="cd1a6-153">/ifd/{ushort=40092}</span></span>                     | <span data-ttu-id="cd1a6-154">\_octets Unicode</span><span class="sxs-lookup"><span data-stu-id="cd1a6-154">unicode\_bytes</span></span> |
| <span data-ttu-id="cd1a6-155">2</span><span class="sxs-lookup"><span data-stu-id="cd1a6-155">2</span></span>     | <span data-ttu-id="cd1a6-156">/IFD/{UShort = 37510}</span><span class="sxs-lookup"><span data-stu-id="cd1a6-156">/ifd/{ushort=37510}</span></span>                     | <span data-ttu-id="cd1a6-157">unicode</span><span class="sxs-lookup"><span data-stu-id="cd1a6-157">unicode</span></span>        |
| <span data-ttu-id="cd1a6-158">3</span><span class="sxs-lookup"><span data-stu-id="cd1a6-158">3</span></span>     | <span data-ttu-id="cd1a6-159">/IFD/XMP/ <xmpalt> EXIF : UserComment</span><span class="sxs-lookup"><span data-stu-id="cd1a6-159">/ifd/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="cd1a6-160">unicode</span><span class="sxs-lookup"><span data-stu-id="cd1a6-160">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="cd1a6-161">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="cd1a6-161">Write Paths</span></span>



| <span data-ttu-id="cd1a6-162">Commande</span><span class="sxs-lookup"><span data-stu-id="cd1a6-162">Order</span></span> | <span data-ttu-id="cd1a6-163">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="cd1a6-163">Path</span></span>                | <span data-ttu-id="cd1a6-164">Format de disque</span><span class="sxs-lookup"><span data-stu-id="cd1a6-164">Disk Format</span></span>    |
|-------|---------------------|----------------|
| <span data-ttu-id="cd1a6-165">1</span><span class="sxs-lookup"><span data-stu-id="cd1a6-165">1</span></span>     | <span data-ttu-id="cd1a6-166">/IFD/{UShort = 40092}</span><span class="sxs-lookup"><span data-stu-id="cd1a6-166">/ifd/{ushort=40092}</span></span> | <span data-ttu-id="cd1a6-167">\_octets Unicode</span><span class="sxs-lookup"><span data-stu-id="cd1a6-167">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="cd1a6-168">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="cd1a6-168">Remove Paths</span></span>



| <span data-ttu-id="cd1a6-169">Commande</span><span class="sxs-lookup"><span data-stu-id="cd1a6-169">Order</span></span> | <span data-ttu-id="cd1a6-170">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="cd1a6-170">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="cd1a6-171">1</span><span class="sxs-lookup"><span data-stu-id="cd1a6-171">1</span></span>     | <span data-ttu-id="cd1a6-172">/IFD/{UShort = 40092}</span><span class="sxs-lookup"><span data-stu-id="cd1a6-172">/ifd/{ushort=40092}</span></span>       |
| <span data-ttu-id="cd1a6-173">2</span><span class="sxs-lookup"><span data-stu-id="cd1a6-173">2</span></span>     | <span data-ttu-id="cd1a6-174">/IFD/{UShort = 37510}</span><span class="sxs-lookup"><span data-stu-id="cd1a6-174">/ifd/{ushort=37510}</span></span>       |
| <span data-ttu-id="cd1a6-175">3</span><span class="sxs-lookup"><span data-stu-id="cd1a6-175">3</span></span>     | <span data-ttu-id="cd1a6-176">/ifd/xmp/exif:UserComment</span><span class="sxs-lookup"><span data-stu-id="cd1a6-176">/ifd/xmp/exif:UserComment</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="cd1a6-177">Notes</span><span class="sxs-lookup"><span data-stu-id="cd1a6-177">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd1a6-178">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cd1a6-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd1a6-179">System. Comment</span><span class="sxs-lookup"><span data-stu-id="cd1a6-179">System.Comment</span></span>](../properties/props-system-comment.md)
</dt> </dl>

 

 
