---
description: Stratégie de métadonnées de la photo pour la propriété System. image. ImageID.
ms.assetid: 2a092d16-e7b9-4ffe-9bdb-01ed328ca26f
title: Stratégie de métadonnées de photo System. image. ImageID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab812a8719c905002c91d33a65cc2b570d37cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529271"
---
# <a name="systemimageimageid-photo-metadata-policy"></a><span data-ttu-id="52caa-103">Stratégie de métadonnées de photo System. image. ImageID</span><span class="sxs-lookup"><span data-stu-id="52caa-103">System.Image.ImageID Photo Metadata Policy</span></span>

<span data-ttu-id="52caa-104">Stratégie de métadonnées de la photo pour la propriété [System. image. ImageID](../properties/props-system-image-imageid.md) .</span><span class="sxs-lookup"><span data-stu-id="52caa-104">The photo metadata policy for the [System.Image.ImageID](../properties/props-system-image-imageid.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="52caa-105">A-la</span><span class="sxs-lookup"><span data-stu-id="52caa-105">PKEY</span></span>

<span data-ttu-id="52caa-106">Image de la \_ \_ ImageID</span><span class="sxs-lookup"><span data-stu-id="52caa-106">PKEY\_Image\_ImageID</span></span>

### <a name="containers"></a><span data-ttu-id="52caa-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="52caa-107">Containers</span></span>

<span data-ttu-id="52caa-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="52caa-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="52caa-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52caa-109">Read-Only</span></span>

<span data-ttu-id="52caa-110">Non</span><span class="sxs-lookup"><span data-stu-id="52caa-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="52caa-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="52caa-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="52caa-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="52caa-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="52caa-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="52caa-113">Input Type</span></span>

<span data-ttu-id="52caa-114">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="52caa-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="52caa-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="52caa-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="52caa-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="52caa-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="52caa-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="52caa-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="52caa-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="52caa-118">Read Paths</span></span>



| <span data-ttu-id="52caa-119">Commande</span><span class="sxs-lookup"><span data-stu-id="52caa-119">Order</span></span> | <span data-ttu-id="52caa-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="52caa-120">Path</span></span>                          | <span data-ttu-id="52caa-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="52caa-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="52caa-122">1</span><span class="sxs-lookup"><span data-stu-id="52caa-122">1</span></span>     | <span data-ttu-id="52caa-123">/App1/IFD/EXIF/{UShort = 42016}</span><span class="sxs-lookup"><span data-stu-id="52caa-123">/app1/ifd/exif/{ushort=42016}</span></span> | <span data-ttu-id="52caa-124">ascii</span><span class="sxs-lookup"><span data-stu-id="52caa-124">ascii</span></span>       |
| <span data-ttu-id="52caa-125">2</span><span class="sxs-lookup"><span data-stu-id="52caa-125">2</span></span>     | <span data-ttu-id="52caa-126">/XMP/EXIF : ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="52caa-126">/xmp/exif:ImageUniqueID</span></span>       | <span data-ttu-id="52caa-127">unicode</span><span class="sxs-lookup"><span data-stu-id="52caa-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="52caa-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="52caa-128">Write Paths</span></span>



| <span data-ttu-id="52caa-129">Commande</span><span class="sxs-lookup"><span data-stu-id="52caa-129">Order</span></span> | <span data-ttu-id="52caa-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="52caa-130">Path</span></span>                          | <span data-ttu-id="52caa-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="52caa-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="52caa-132">1</span><span class="sxs-lookup"><span data-stu-id="52caa-132">1</span></span>     | <span data-ttu-id="52caa-133">/App1/IFD/EXIF/{UShort = 42016}</span><span class="sxs-lookup"><span data-stu-id="52caa-133">/app1/ifd/exif/{ushort=42016}</span></span> | <span data-ttu-id="52caa-134">ascii</span><span class="sxs-lookup"><span data-stu-id="52caa-134">ascii</span></span>       |
| <span data-ttu-id="52caa-135">2</span><span class="sxs-lookup"><span data-stu-id="52caa-135">2</span></span>     | <span data-ttu-id="52caa-136">/XMP/EXIF : ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="52caa-136">/xmp/exif:ImageUniqueID</span></span>       | <span data-ttu-id="52caa-137">unicode</span><span class="sxs-lookup"><span data-stu-id="52caa-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="52caa-138">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="52caa-138">Remove Paths</span></span>



| <span data-ttu-id="52caa-139">Commande</span><span class="sxs-lookup"><span data-stu-id="52caa-139">Order</span></span> | <span data-ttu-id="52caa-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="52caa-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="52caa-141">1</span><span class="sxs-lookup"><span data-stu-id="52caa-141">1</span></span>     | <span data-ttu-id="52caa-142">/App1/IFD/EXIF/{UShort = 42016}</span><span class="sxs-lookup"><span data-stu-id="52caa-142">/app1/ifd/exif/{ushort=42016}</span></span> |
| <span data-ttu-id="52caa-143">2</span><span class="sxs-lookup"><span data-stu-id="52caa-143">2</span></span>     | <span data-ttu-id="52caa-144">/XMP/EXIF : ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="52caa-144">/xmp/exif:ImageUniqueID</span></span>       |



 

### <a name="tiff-policy"></a><span data-ttu-id="52caa-145">Stratégie TIFF</span><span class="sxs-lookup"><span data-stu-id="52caa-145">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="52caa-146">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="52caa-146">Read Paths</span></span>



| <span data-ttu-id="52caa-147">Commande</span><span class="sxs-lookup"><span data-stu-id="52caa-147">Order</span></span> | <span data-ttu-id="52caa-148">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="52caa-148">Path</span></span>                        | <span data-ttu-id="52caa-149">Format de disque</span><span class="sxs-lookup"><span data-stu-id="52caa-149">Disk Format</span></span> |
|-------|-----------------------------|-------------|
|       | <span data-ttu-id="52caa-150">/IFD/EXIF/{UShort = 42016}</span><span class="sxs-lookup"><span data-stu-id="52caa-150">/ifd/exif/{ushort=42016}</span></span>    | <span data-ttu-id="52caa-151">ascii</span><span class="sxs-lookup"><span data-stu-id="52caa-151">ascii</span></span>       |
|       | <span data-ttu-id="52caa-152">/IFD/XMP/EXIF : ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="52caa-152">/ifd/xmp/exif:ImageUniqueID</span></span> | <span data-ttu-id="52caa-153">unicode</span><span class="sxs-lookup"><span data-stu-id="52caa-153">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="52caa-154">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="52caa-154">Write Paths</span></span>



| <span data-ttu-id="52caa-155">Commande</span><span class="sxs-lookup"><span data-stu-id="52caa-155">Order</span></span> | <span data-ttu-id="52caa-156">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="52caa-156">Path</span></span>                        | <span data-ttu-id="52caa-157">Format de disque</span><span class="sxs-lookup"><span data-stu-id="52caa-157">Disk Format</span></span> |
|-------|-----------------------------|-------------|
|       | <span data-ttu-id="52caa-158">/IFD/EXIF/{UShort = 42016}</span><span class="sxs-lookup"><span data-stu-id="52caa-158">/ifd/exif/{ushort=42016}</span></span>    | <span data-ttu-id="52caa-159">ascii</span><span class="sxs-lookup"><span data-stu-id="52caa-159">ascii</span></span>       |
|       | <span data-ttu-id="52caa-160">/IFD/XMP/EXIF : ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="52caa-160">/ifd/xmp/exif:ImageUniqueID</span></span> | <span data-ttu-id="52caa-161">unicode</span><span class="sxs-lookup"><span data-stu-id="52caa-161">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="52caa-162">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="52caa-162">Remove Paths</span></span>



| <span data-ttu-id="52caa-163">Commande</span><span class="sxs-lookup"><span data-stu-id="52caa-163">Order</span></span> | <span data-ttu-id="52caa-164">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="52caa-164">Path</span></span>                        |
|-------|-----------------------------|
|       | <span data-ttu-id="52caa-165">/IFD/EXIF/{UShort = 42016}</span><span class="sxs-lookup"><span data-stu-id="52caa-165">/ifd/exif/{ushort=42016}</span></span>    |
|       | <span data-ttu-id="52caa-166">/IFD/XMP/EXIF : ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="52caa-166">/ifd/xmp/exif:ImageUniqueID</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="52caa-167">Notes</span><span class="sxs-lookup"><span data-stu-id="52caa-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="52caa-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="52caa-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52caa-169">System. image. ImageID</span><span class="sxs-lookup"><span data-stu-id="52caa-169">System.Image.ImageID</span></span>](../properties/props-system-image-imageid.md)
</dt> </dl>

 

 
