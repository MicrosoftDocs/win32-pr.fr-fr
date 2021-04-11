---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. FNumber.
ms.assetid: 434d52cb-c98d-4860-87f7-4aedab7f8188
title: Stratégie de métadonnées de photo System. photo. FNumber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c518ef2a05dde8fd7e812d1d76a79cbe3efb4217
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203648"
---
# <a name="systemphotofnumber-photo-metadata-policy"></a><span data-ttu-id="6cdc1-103">Stratégie de métadonnées de photo System. photo. FNumber</span><span class="sxs-lookup"><span data-stu-id="6cdc1-103">System.Photo.FNumber Photo Metadata Policy</span></span>

<span data-ttu-id="6cdc1-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. FNumber](../properties/props-system-photo-fnumber.md) .</span><span class="sxs-lookup"><span data-stu-id="6cdc1-104">The photo metadata policy for the [System.Photo.FNumber](../properties/props-system-photo-fnumber.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="6cdc1-105">A-la</span><span class="sxs-lookup"><span data-stu-id="6cdc1-105">PKEY</span></span>

<span data-ttu-id="6cdc1-106">\_Photo \_ FNumber</span><span class="sxs-lookup"><span data-stu-id="6cdc1-106">PKEY\_Photo\_FNumber</span></span>

### <a name="containers"></a><span data-ttu-id="6cdc1-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="6cdc1-107">Containers</span></span>

<span data-ttu-id="6cdc1-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="6cdc1-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="6cdc1-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6cdc1-109">Read-Only</span></span>

<span data-ttu-id="6cdc1-110">Oui</span><span class="sxs-lookup"><span data-stu-id="6cdc1-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="6cdc1-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="6cdc1-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="6cdc1-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="6cdc1-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="6cdc1-113">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="6cdc1-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="6cdc1-114">Cette valeur est générée à partir de System. photo. FNumberNumerator et de System. photo. FNumberDenominator.</span><span class="sxs-lookup"><span data-stu-id="6cdc1-114">This value is generated from System.Photo.FNumberNumerator and System.Photo.FNumberDenominator.</span></span> <span data-ttu-id="6cdc1-115">Il ne peut pas être écrit directement.</span><span class="sxs-lookup"><span data-stu-id="6cdc1-115">It cannot be written directly.</span></span> <span data-ttu-id="6cdc1-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="6cdc1-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="6cdc1-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="6cdc1-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="6cdc1-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="6cdc1-118">Read Paths</span></span>



| <span data-ttu-id="6cdc1-119">Commande</span><span class="sxs-lookup"><span data-stu-id="6cdc1-119">Order</span></span> | <span data-ttu-id="6cdc1-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="6cdc1-120">Path</span></span>                          | <span data-ttu-id="6cdc1-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="6cdc1-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="6cdc1-122">1</span><span class="sxs-lookup"><span data-stu-id="6cdc1-122">1</span></span>     | <span data-ttu-id="6cdc1-123">/App1/IFD/EXIF/{UShort = 33437}</span><span class="sxs-lookup"><span data-stu-id="6cdc1-123">/app1/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="6cdc1-124">2</span><span class="sxs-lookup"><span data-stu-id="6cdc1-124">2</span></span>     | <span data-ttu-id="6cdc1-125">/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="6cdc1-125">/xmp/exif:FNumber</span></span>             |             |



 

### <a name="write-paths"></a><span data-ttu-id="6cdc1-126">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="6cdc1-126">Write Paths</span></span>



|       |                               |             |     |
|-------|-------------------------------|-------------|-----|
| <span data-ttu-id="6cdc1-127">Commande</span><span class="sxs-lookup"><span data-stu-id="6cdc1-127">Order</span></span> | <span data-ttu-id="6cdc1-128">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="6cdc1-128">Path</span></span>                          | <span data-ttu-id="6cdc1-129">Format de disque</span><span class="sxs-lookup"><span data-stu-id="6cdc1-129">Disk Format</span></span> |     |
| <span data-ttu-id="6cdc1-130">1</span><span class="sxs-lookup"><span data-stu-id="6cdc1-130">1</span></span>     | <span data-ttu-id="6cdc1-131">/App1/IFD/EXIF/{UShort = 33437}</span><span class="sxs-lookup"><span data-stu-id="6cdc1-131">/app1/ifd/exif/{ushort=33437}</span></span> |             |     |
| <span data-ttu-id="6cdc1-132">2</span><span class="sxs-lookup"><span data-stu-id="6cdc1-132">2</span></span>     | <span data-ttu-id="6cdc1-133">/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="6cdc1-133">/xmp/exif:FNumber</span></span>             |             |     |



 

### <a name="remove-paths"></a><span data-ttu-id="6cdc1-134">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="6cdc1-134">Remove Paths</span></span>



| <span data-ttu-id="6cdc1-135">Commande</span><span class="sxs-lookup"><span data-stu-id="6cdc1-135">Order</span></span> | <span data-ttu-id="6cdc1-136">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="6cdc1-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="6cdc1-137">1</span><span class="sxs-lookup"><span data-stu-id="6cdc1-137">1</span></span>     | <span data-ttu-id="6cdc1-138">/App1/IFD/EXIF/{UShort = 33437}</span><span class="sxs-lookup"><span data-stu-id="6cdc1-138">/app1/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="6cdc1-139">2</span><span class="sxs-lookup"><span data-stu-id="6cdc1-139">2</span></span>     | <span data-ttu-id="6cdc1-140">/xmp/exif:fnumber</span><span class="sxs-lookup"><span data-stu-id="6cdc1-140">/xmp/exif:fnumber</span></span>             |



 

### <a name="tiff-policies"></a><span data-ttu-id="6cdc1-141">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="6cdc1-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="6cdc1-142">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="6cdc1-142">Read Paths</span></span>



| <span data-ttu-id="6cdc1-143">Commande</span><span class="sxs-lookup"><span data-stu-id="6cdc1-143">Order</span></span> | <span data-ttu-id="6cdc1-144">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="6cdc1-144">Path</span></span>                     | <span data-ttu-id="6cdc1-145">Format de disque</span><span class="sxs-lookup"><span data-stu-id="6cdc1-145">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="6cdc1-146">1</span><span class="sxs-lookup"><span data-stu-id="6cdc1-146">1</span></span>     | <span data-ttu-id="6cdc1-147">/IFD/EXIF/{UShort = 33437}</span><span class="sxs-lookup"><span data-stu-id="6cdc1-147">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="6cdc1-148">2</span><span class="sxs-lookup"><span data-stu-id="6cdc1-148">2</span></span>     | <span data-ttu-id="6cdc1-149">/ifd/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="6cdc1-149">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="6cdc1-150">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="6cdc1-150">Write Paths</span></span>



| <span data-ttu-id="6cdc1-151">Commande</span><span class="sxs-lookup"><span data-stu-id="6cdc1-151">Order</span></span> | <span data-ttu-id="6cdc1-152">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="6cdc1-152">Path</span></span>                     | <span data-ttu-id="6cdc1-153">Format de disque</span><span class="sxs-lookup"><span data-stu-id="6cdc1-153">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="6cdc1-154">1</span><span class="sxs-lookup"><span data-stu-id="6cdc1-154">1</span></span>     | <span data-ttu-id="6cdc1-155">/IFD/EXIF/{UShort = 33437}</span><span class="sxs-lookup"><span data-stu-id="6cdc1-155">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="6cdc1-156">2</span><span class="sxs-lookup"><span data-stu-id="6cdc1-156">2</span></span>     | <span data-ttu-id="6cdc1-157">/ifd/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="6cdc1-157">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="6cdc1-158">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="6cdc1-158">Remove Paths</span></span>



| <span data-ttu-id="6cdc1-159">Commande</span><span class="sxs-lookup"><span data-stu-id="6cdc1-159">Order</span></span> | <span data-ttu-id="6cdc1-160">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="6cdc1-160">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="6cdc1-161">1</span><span class="sxs-lookup"><span data-stu-id="6cdc1-161">1</span></span>     | <span data-ttu-id="6cdc1-162">/IFD/EXIF/{UShort = 33437}</span><span class="sxs-lookup"><span data-stu-id="6cdc1-162">/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="6cdc1-163">2</span><span class="sxs-lookup"><span data-stu-id="6cdc1-163">2</span></span>     | <span data-ttu-id="6cdc1-164">/ifd/xmp/exif:fnumber</span><span class="sxs-lookup"><span data-stu-id="6cdc1-164">/ifd/xmp/exif:fnumber</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="6cdc1-165">Notes</span><span class="sxs-lookup"><span data-stu-id="6cdc1-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="6cdc1-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6cdc1-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cdc1-167">System. photo. FNumber</span><span class="sxs-lookup"><span data-stu-id="6cdc1-167">System.Photo.FNumber</span></span>](../properties/props-system-photo-fnumber.md)
</dt> </dl>

 

 
