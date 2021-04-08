---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. FlashEnergy.
ms.assetid: d10a4de9-16fe-4920-aa7f-b2f95fb23045
title: Stratégie de métadonnées de photo System. photo. FlashEnergy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c272b4d6d14bf2f2e81d0964a3dc4395ba62dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035170"
---
# <a name="systemphotoflashenergy-photo-metadata-policy"></a><span data-ttu-id="9159a-103">Stratégie de métadonnées de photo System. photo. FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="9159a-103">System.Photo.FlashEnergy Photo Metadata Policy</span></span>

<span data-ttu-id="9159a-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. FlashEnergy](../properties/props-system-photo-flashenergy.md) .</span><span class="sxs-lookup"><span data-stu-id="9159a-104">The photo metadata policy for the [System.Photo.FlashEnergy](../properties/props-system-photo-flashenergy.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="9159a-105">A-la</span><span class="sxs-lookup"><span data-stu-id="9159a-105">PKEY</span></span>

<span data-ttu-id="9159a-106">\_Photo \_ FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="9159a-106">PKEY\_Photo\_FlashEnergy</span></span>

### <a name="containers"></a><span data-ttu-id="9159a-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="9159a-107">Containers</span></span>

<span data-ttu-id="9159a-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="9159a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="9159a-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9159a-109">Read-Only</span></span>

<span data-ttu-id="9159a-110">Oui</span><span class="sxs-lookup"><span data-stu-id="9159a-110">Yes</span></span>

### <a name="input-type"></a><span data-ttu-id="9159a-111">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="9159a-111">Input Type</span></span>

<span data-ttu-id="9159a-112">Double</span><span class="sxs-lookup"><span data-stu-id="9159a-112">Double</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="9159a-113">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="9159a-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="9159a-114">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="9159a-114">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="9159a-115">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="9159a-115">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="9159a-116">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="9159a-116">Read Paths</span></span>



| <span data-ttu-id="9159a-117">Commande</span><span class="sxs-lookup"><span data-stu-id="9159a-117">Order</span></span> | <span data-ttu-id="9159a-118">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="9159a-118">Path</span></span>                          | <span data-ttu-id="9159a-119">Format de disque</span><span class="sxs-lookup"><span data-stu-id="9159a-119">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="9159a-120">1</span><span class="sxs-lookup"><span data-stu-id="9159a-120">1</span></span>     | <span data-ttu-id="9159a-121">/App1/IFD/EXIF/{UShort = 41483}</span><span class="sxs-lookup"><span data-stu-id="9159a-121">/app1/ifd/exif/{ushort=41483}</span></span> |             |
| <span data-ttu-id="9159a-122">2</span><span class="sxs-lookup"><span data-stu-id="9159a-122">2</span></span>     | <span data-ttu-id="9159a-123">/xmp/exif:FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="9159a-123">/xmp/exif:FlashEnergy</span></span>         |             |



 

### <a name="write-paths"></a><span data-ttu-id="9159a-124">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="9159a-124">Write Paths</span></span>



| <span data-ttu-id="9159a-125">Commande</span><span class="sxs-lookup"><span data-stu-id="9159a-125">Order</span></span> | <span data-ttu-id="9159a-126">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="9159a-126">Path</span></span>                          | <span data-ttu-id="9159a-127">Format de disque</span><span class="sxs-lookup"><span data-stu-id="9159a-127">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="9159a-128">1</span><span class="sxs-lookup"><span data-stu-id="9159a-128">1</span></span>     | <span data-ttu-id="9159a-129">/App1/IFD/EXIF/{UShort = 41483}</span><span class="sxs-lookup"><span data-stu-id="9159a-129">/app1/ifd/exif/{ushort=41483}</span></span> |             |
| <span data-ttu-id="9159a-130">2</span><span class="sxs-lookup"><span data-stu-id="9159a-130">2</span></span>     | <span data-ttu-id="9159a-131">/xmp/exif:FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="9159a-131">/xmp/exif:FlashEnergy</span></span>         |             |



 

### <a name="remove-paths"></a><span data-ttu-id="9159a-132">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="9159a-132">Remove Paths</span></span>



| <span data-ttu-id="9159a-133">Commande</span><span class="sxs-lookup"><span data-stu-id="9159a-133">Order</span></span> | <span data-ttu-id="9159a-134">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="9159a-134">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="9159a-135">1</span><span class="sxs-lookup"><span data-stu-id="9159a-135">1</span></span>     | <span data-ttu-id="9159a-136">/App1/IFD/EXIF/{UShort = 41483}</span><span class="sxs-lookup"><span data-stu-id="9159a-136">/app1/ifd/exif/{ushort=41483}</span></span> |
| <span data-ttu-id="9159a-137">2</span><span class="sxs-lookup"><span data-stu-id="9159a-137">2</span></span>     | <span data-ttu-id="9159a-138">/xmp/exif:flashenergy</span><span class="sxs-lookup"><span data-stu-id="9159a-138">/xmp/exif:flashenergy</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="9159a-139">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="9159a-139">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="9159a-140">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="9159a-140">Read Paths</span></span>



| <span data-ttu-id="9159a-141">Commande</span><span class="sxs-lookup"><span data-stu-id="9159a-141">Order</span></span> | <span data-ttu-id="9159a-142">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="9159a-142">Path</span></span>                      | <span data-ttu-id="9159a-143">Format de disque</span><span class="sxs-lookup"><span data-stu-id="9159a-143">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="9159a-144">1</span><span class="sxs-lookup"><span data-stu-id="9159a-144">1</span></span>     | <span data-ttu-id="9159a-145">/IFD/EXIF/{UShort = 41483}</span><span class="sxs-lookup"><span data-stu-id="9159a-145">/ifd/exif/{ushort=41483}</span></span>  |             |
| <span data-ttu-id="9159a-146">2</span><span class="sxs-lookup"><span data-stu-id="9159a-146">2</span></span>     | <span data-ttu-id="9159a-147">/ifd/xmp/exif:FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="9159a-147">/ifd/xmp/exif:FlashEnergy</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="9159a-148">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="9159a-148">Write Paths</span></span>



| <span data-ttu-id="9159a-149">Commande</span><span class="sxs-lookup"><span data-stu-id="9159a-149">Order</span></span> | <span data-ttu-id="9159a-150">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="9159a-150">Path</span></span>                      | <span data-ttu-id="9159a-151">Format de disque</span><span class="sxs-lookup"><span data-stu-id="9159a-151">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="9159a-152">1</span><span class="sxs-lookup"><span data-stu-id="9159a-152">1</span></span>     | <span data-ttu-id="9159a-153">/IFD/EXIF/{UShort = 41483}</span><span class="sxs-lookup"><span data-stu-id="9159a-153">/ifd/exif/{ushort=41483}</span></span>  |             |
| <span data-ttu-id="9159a-154">2</span><span class="sxs-lookup"><span data-stu-id="9159a-154">2</span></span>     | <span data-ttu-id="9159a-155">/ifd/xmp/exif:FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="9159a-155">/ifd/xmp/exif:FlashEnergy</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="9159a-156">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="9159a-156">Remove Paths</span></span>



| <span data-ttu-id="9159a-157">Commande</span><span class="sxs-lookup"><span data-stu-id="9159a-157">Order</span></span> | <span data-ttu-id="9159a-158">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="9159a-158">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="9159a-159">1</span><span class="sxs-lookup"><span data-stu-id="9159a-159">1</span></span>     | <span data-ttu-id="9159a-160">/IFD/EXIF/{UShort = 41483}</span><span class="sxs-lookup"><span data-stu-id="9159a-160">/ifd/exif/{ushort=41483}</span></span>  |
| <span data-ttu-id="9159a-161">2</span><span class="sxs-lookup"><span data-stu-id="9159a-161">2</span></span>     | <span data-ttu-id="9159a-162">/ifd/xmp/exif:flashenergy</span><span class="sxs-lookup"><span data-stu-id="9159a-162">/ifd/xmp/exif:flashenergy</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9159a-163">Notes</span><span class="sxs-lookup"><span data-stu-id="9159a-163">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="9159a-164">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9159a-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9159a-165">System. photo. FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="9159a-165">System.Photo.FlashEnergy</span></span>](../properties/props-system-photo-flashenergy.md)
</dt> </dl>

 

 
