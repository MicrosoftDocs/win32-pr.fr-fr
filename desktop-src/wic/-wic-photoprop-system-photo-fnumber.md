---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. FNumber.
ms.assetid: 434d52cb-c98d-4860-87f7-4aedab7f8188
title: Stratégie de métadonnées de photo System. photo. FNumber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85443b849d9f810709f3e75c3082738e5377092f
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443620"
---
# <a name="systemphotofnumber-photo-metadata-policy"></a><span data-ttu-id="f2a4b-103">Stratégie de métadonnées de photo System. photo. FNumber</span><span class="sxs-lookup"><span data-stu-id="f2a4b-103">System.Photo.FNumber Photo Metadata Policy</span></span>

<span data-ttu-id="f2a4b-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. FNumber](../properties/props-system-photo-fnumber.md) .</span><span class="sxs-lookup"><span data-stu-id="f2a4b-104">The photo metadata policy for the [System.Photo.FNumber](../properties/props-system-photo-fnumber.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="f2a4b-105">A-la</span><span class="sxs-lookup"><span data-stu-id="f2a4b-105">PKEY</span></span>

<span data-ttu-id="f2a4b-106">\_Photo \_ FNumber</span><span class="sxs-lookup"><span data-stu-id="f2a4b-106">PKEY\_Photo\_FNumber</span></span>

### <a name="containers"></a><span data-ttu-id="f2a4b-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="f2a4b-107">Containers</span></span>

<span data-ttu-id="f2a4b-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="f2a4b-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="f2a4b-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f2a4b-109">Read-Only</span></span>

<span data-ttu-id="f2a4b-110">Oui</span><span class="sxs-lookup"><span data-stu-id="f2a4b-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="f2a4b-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="f2a4b-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="f2a4b-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="f2a4b-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="f2a4b-113">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="f2a4b-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="f2a4b-114">Cette valeur est générée à partir de System. photo. FNumberNumerator et de System. photo. FNumberDenominator.</span><span class="sxs-lookup"><span data-stu-id="f2a4b-114">This value is generated from System.Photo.FNumberNumerator and System.Photo.FNumberDenominator.</span></span> <span data-ttu-id="f2a4b-115">Il ne peut pas être écrit directement.</span><span class="sxs-lookup"><span data-stu-id="f2a4b-115">It cannot be written directly.</span></span> <span data-ttu-id="f2a4b-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="f2a4b-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="f2a4b-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="f2a4b-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="f2a4b-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="f2a4b-118">Read Paths</span></span>



| <span data-ttu-id="f2a4b-119">Commande</span><span class="sxs-lookup"><span data-stu-id="f2a4b-119">Order</span></span> | <span data-ttu-id="f2a4b-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="f2a4b-120">Path</span></span>                          | <span data-ttu-id="f2a4b-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="f2a4b-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="f2a4b-122">1</span><span class="sxs-lookup"><span data-stu-id="f2a4b-122">1</span></span>     | <span data-ttu-id="f2a4b-123">/App1/IFD/EXIF/{UShort = 33437}</span><span class="sxs-lookup"><span data-stu-id="f2a4b-123">/app1/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="f2a4b-124">2</span><span class="sxs-lookup"><span data-stu-id="f2a4b-124">2</span></span>     | <span data-ttu-id="f2a4b-125">/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="f2a4b-125">/xmp/exif:FNumber</span></span>             |             |



 

### <a name="write-paths"></a><span data-ttu-id="f2a4b-126">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="f2a4b-126">Write Paths</span></span>



| <span data-ttu-id="f2a4b-127">Commande</span><span class="sxs-lookup"><span data-stu-id="f2a4b-127">Order</span></span> | <span data-ttu-id="f2a4b-128">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="f2a4b-128">Path</span></span>                          | <span data-ttu-id="f2a4b-129">Format de disque</span><span class="sxs-lookup"><span data-stu-id="f2a4b-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="f2a4b-130">1</span><span class="sxs-lookup"><span data-stu-id="f2a4b-130">1</span></span>     | <span data-ttu-id="f2a4b-131">/App1/IFD/EXIF/{UShort = 33437}</span><span class="sxs-lookup"><span data-stu-id="f2a4b-131">/app1/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="f2a4b-132">2</span><span class="sxs-lookup"><span data-stu-id="f2a4b-132">2</span></span>     | <span data-ttu-id="f2a4b-133">/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="f2a4b-133">/xmp/exif:FNumber</span></span>             |             | 
 

### <a name="remove-paths"></a><span data-ttu-id="f2a4b-134">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="f2a4b-134">Remove Paths</span></span>



| <span data-ttu-id="f2a4b-135">Commande</span><span class="sxs-lookup"><span data-stu-id="f2a4b-135">Order</span></span> | <span data-ttu-id="f2a4b-136">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="f2a4b-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="f2a4b-137">1</span><span class="sxs-lookup"><span data-stu-id="f2a4b-137">1</span></span>     | <span data-ttu-id="f2a4b-138">/App1/IFD/EXIF/{UShort = 33437}</span><span class="sxs-lookup"><span data-stu-id="f2a4b-138">/app1/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="f2a4b-139">2</span><span class="sxs-lookup"><span data-stu-id="f2a4b-139">2</span></span>     | <span data-ttu-id="f2a4b-140">/xmp/exif:fnumber</span><span class="sxs-lookup"><span data-stu-id="f2a4b-140">/xmp/exif:fnumber</span></span>             |



 

### <a name="tiff-policies"></a><span data-ttu-id="f2a4b-141">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="f2a4b-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="f2a4b-142">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="f2a4b-142">Read Paths</span></span>



| <span data-ttu-id="f2a4b-143">Commande</span><span class="sxs-lookup"><span data-stu-id="f2a4b-143">Order</span></span> | <span data-ttu-id="f2a4b-144">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="f2a4b-144">Path</span></span>                     | <span data-ttu-id="f2a4b-145">Format de disque</span><span class="sxs-lookup"><span data-stu-id="f2a4b-145">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="f2a4b-146">1</span><span class="sxs-lookup"><span data-stu-id="f2a4b-146">1</span></span>     | <span data-ttu-id="f2a4b-147">/IFD/EXIF/{UShort = 33437}</span><span class="sxs-lookup"><span data-stu-id="f2a4b-147">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="f2a4b-148">2</span><span class="sxs-lookup"><span data-stu-id="f2a4b-148">2</span></span>     | <span data-ttu-id="f2a4b-149">/ifd/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="f2a4b-149">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="f2a4b-150">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="f2a4b-150">Write Paths</span></span>



| <span data-ttu-id="f2a4b-151">Commande</span><span class="sxs-lookup"><span data-stu-id="f2a4b-151">Order</span></span> | <span data-ttu-id="f2a4b-152">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="f2a4b-152">Path</span></span>                     | <span data-ttu-id="f2a4b-153">Format de disque</span><span class="sxs-lookup"><span data-stu-id="f2a4b-153">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="f2a4b-154">1</span><span class="sxs-lookup"><span data-stu-id="f2a4b-154">1</span></span>     | <span data-ttu-id="f2a4b-155">/IFD/EXIF/{UShort = 33437}</span><span class="sxs-lookup"><span data-stu-id="f2a4b-155">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="f2a4b-156">2</span><span class="sxs-lookup"><span data-stu-id="f2a4b-156">2</span></span>     | <span data-ttu-id="f2a4b-157">/ifd/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="f2a4b-157">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="f2a4b-158">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="f2a4b-158">Remove Paths</span></span>



| <span data-ttu-id="f2a4b-159">Commande</span><span class="sxs-lookup"><span data-stu-id="f2a4b-159">Order</span></span> | <span data-ttu-id="f2a4b-160">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="f2a4b-160">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="f2a4b-161">1</span><span class="sxs-lookup"><span data-stu-id="f2a4b-161">1</span></span>     | <span data-ttu-id="f2a4b-162">/IFD/EXIF/{UShort = 33437}</span><span class="sxs-lookup"><span data-stu-id="f2a4b-162">/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="f2a4b-163">2</span><span class="sxs-lookup"><span data-stu-id="f2a4b-163">2</span></span>     | <span data-ttu-id="f2a4b-164">/ifd/xmp/exif:fnumber</span><span class="sxs-lookup"><span data-stu-id="f2a4b-164">/ifd/xmp/exif:fnumber</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="f2a4b-165">Remarques</span><span class="sxs-lookup"><span data-stu-id="f2a4b-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2a4b-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f2a4b-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2a4b-167">System. photo. FNumber</span><span class="sxs-lookup"><span data-stu-id="f2a4b-167">System.Photo.FNumber</span></span>](../properties/props-system-photo-fnumber.md)
</dt> </dl>

 

 
