---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. ExposureTime.
ms.assetid: 26f6ff27-b326-46f8-b4be-b091acbec575
title: Stratégie de métadonnées de photo System. photo. ExposureTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea9078befd0cbc26272ff14ae023b1b22cb4f0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536492"
---
# <a name="systemphotoexposuretime-photo-metadata-policy"></a><span data-ttu-id="9bafe-103">Stratégie de métadonnées de photo System. photo. ExposureTime</span><span class="sxs-lookup"><span data-stu-id="9bafe-103">System.Photo.ExposureTime Photo Metadata Policy</span></span>

<span data-ttu-id="9bafe-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. exposuretime](../properties/props-system-photo-exposuretime.md) .</span><span class="sxs-lookup"><span data-stu-id="9bafe-104">The photo metadata policy for the [System.Photo.ExposureTime](../properties/props-system-photo-exposuretime.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="9bafe-105">A-la</span><span class="sxs-lookup"><span data-stu-id="9bafe-105">PKEY</span></span>

<span data-ttu-id="9bafe-106">\_Photo \_ exposuretime</span><span class="sxs-lookup"><span data-stu-id="9bafe-106">PKEY\_Photo\_ExposureTime</span></span>

### <a name="containers"></a><span data-ttu-id="9bafe-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="9bafe-107">Containers</span></span>

<span data-ttu-id="9bafe-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="9bafe-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="9bafe-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9bafe-109">Read-Only</span></span>

<span data-ttu-id="9bafe-110">Oui</span><span class="sxs-lookup"><span data-stu-id="9bafe-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="9bafe-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="9bafe-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="9bafe-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="9bafe-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="9bafe-113">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="9bafe-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="9bafe-114">Cette valeur est générée à partir de System. photo. ExposureTimeNumerator et de System. photo. ExposureTimeDenominator.</span><span class="sxs-lookup"><span data-stu-id="9bafe-114">This value is generated from System.Photo.ExposureTimeNumerator and System.Photo.ExposureTimeDenominator.</span></span> <span data-ttu-id="9bafe-115">Il ne peut pas être écrit directement.</span><span class="sxs-lookup"><span data-stu-id="9bafe-115">It cannot be written directly.</span></span> <span data-ttu-id="9bafe-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="9bafe-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="9bafe-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="9bafe-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="9bafe-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="9bafe-118">Read Paths</span></span>



| <span data-ttu-id="9bafe-119">Commande</span><span class="sxs-lookup"><span data-stu-id="9bafe-119">Order</span></span> | <span data-ttu-id="9bafe-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="9bafe-120">Path</span></span>                          | <span data-ttu-id="9bafe-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="9bafe-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="9bafe-122">1</span><span class="sxs-lookup"><span data-stu-id="9bafe-122">1</span></span>     | <span data-ttu-id="9bafe-123">/App1/IFD/EXIF/{UShort = 33434}</span><span class="sxs-lookup"><span data-stu-id="9bafe-123">/app1/ifd/exif/{ushort=33434}</span></span> |             |
| <span data-ttu-id="9bafe-124">2</span><span class="sxs-lookup"><span data-stu-id="9bafe-124">2</span></span>     | <span data-ttu-id="9bafe-125">/xmp/exif:ExposureTime</span><span class="sxs-lookup"><span data-stu-id="9bafe-125">/xmp/exif:ExposureTime</span></span>        |             |



 

### <a name="write-paths"></a><span data-ttu-id="9bafe-126">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="9bafe-126">Write Paths</span></span>



| <span data-ttu-id="9bafe-127">Commande</span><span class="sxs-lookup"><span data-stu-id="9bafe-127">Order</span></span> | <span data-ttu-id="9bafe-128">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="9bafe-128">Path</span></span>                          | <span data-ttu-id="9bafe-129">Format de disque</span><span class="sxs-lookup"><span data-stu-id="9bafe-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="9bafe-130">1</span><span class="sxs-lookup"><span data-stu-id="9bafe-130">1</span></span>     | <span data-ttu-id="9bafe-131">/App1/IFD/EXIF/{UShort = 33434}</span><span class="sxs-lookup"><span data-stu-id="9bafe-131">/app1/ifd/exif/{ushort=33434}</span></span> |             |
| <span data-ttu-id="9bafe-132">2</span><span class="sxs-lookup"><span data-stu-id="9bafe-132">2</span></span>     | <span data-ttu-id="9bafe-133">/xmp/exif:ExposureTime</span><span class="sxs-lookup"><span data-stu-id="9bafe-133">/xmp/exif:ExposureTime</span></span>        |             |



 

### <a name="remove-paths"></a><span data-ttu-id="9bafe-134">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="9bafe-134">Remove Paths</span></span>



| <span data-ttu-id="9bafe-135">Commande</span><span class="sxs-lookup"><span data-stu-id="9bafe-135">Order</span></span> | <span data-ttu-id="9bafe-136">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="9bafe-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="9bafe-137">1</span><span class="sxs-lookup"><span data-stu-id="9bafe-137">1</span></span>     | <span data-ttu-id="9bafe-138">/App1/IFD/EXIF/{UShort = 33434}</span><span class="sxs-lookup"><span data-stu-id="9bafe-138">/app1/ifd/exif/{ushort=33434}</span></span> |
| <span data-ttu-id="9bafe-139">2</span><span class="sxs-lookup"><span data-stu-id="9bafe-139">2</span></span>     | <span data-ttu-id="9bafe-140">/xmp/exif:exposuretime</span><span class="sxs-lookup"><span data-stu-id="9bafe-140">/xmp/exif:exposuretime</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="9bafe-141">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="9bafe-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="9bafe-142">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="9bafe-142">Read Paths</span></span>



| <span data-ttu-id="9bafe-143">Commande</span><span class="sxs-lookup"><span data-stu-id="9bafe-143">Order</span></span> | <span data-ttu-id="9bafe-144">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="9bafe-144">Path</span></span>                       | <span data-ttu-id="9bafe-145">Format de disque</span><span class="sxs-lookup"><span data-stu-id="9bafe-145">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="9bafe-146">1</span><span class="sxs-lookup"><span data-stu-id="9bafe-146">1</span></span>     | <span data-ttu-id="9bafe-147">/IFD/EXIF/{UShort = 33434}</span><span class="sxs-lookup"><span data-stu-id="9bafe-147">/ifd/exif/{ushort=33434}</span></span>   |             |
| <span data-ttu-id="9bafe-148">2</span><span class="sxs-lookup"><span data-stu-id="9bafe-148">2</span></span>     | <span data-ttu-id="9bafe-149">/ifd/xmp/exif:ExposureTime</span><span class="sxs-lookup"><span data-stu-id="9bafe-149">/ifd/xmp/exif:ExposureTime</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="9bafe-150">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="9bafe-150">Write Paths</span></span>



| <span data-ttu-id="9bafe-151">Commande</span><span class="sxs-lookup"><span data-stu-id="9bafe-151">Order</span></span> | <span data-ttu-id="9bafe-152">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="9bafe-152">Path</span></span>                       | <span data-ttu-id="9bafe-153">Format de disque</span><span class="sxs-lookup"><span data-stu-id="9bafe-153">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="9bafe-154">1</span><span class="sxs-lookup"><span data-stu-id="9bafe-154">1</span></span>     | <span data-ttu-id="9bafe-155">/IFD/EXIF/{UShort = 33434}</span><span class="sxs-lookup"><span data-stu-id="9bafe-155">/ifd/exif/{ushort=33434}</span></span>   |             |
| <span data-ttu-id="9bafe-156">2</span><span class="sxs-lookup"><span data-stu-id="9bafe-156">2</span></span>     | <span data-ttu-id="9bafe-157">/ifd/xmp/exif:ExposureTime</span><span class="sxs-lookup"><span data-stu-id="9bafe-157">/ifd/xmp/exif:ExposureTime</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="9bafe-158">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="9bafe-158">Remove Paths</span></span>



| <span data-ttu-id="9bafe-159">Commande</span><span class="sxs-lookup"><span data-stu-id="9bafe-159">Order</span></span> | <span data-ttu-id="9bafe-160">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="9bafe-160">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="9bafe-161">1</span><span class="sxs-lookup"><span data-stu-id="9bafe-161">1</span></span>     | <span data-ttu-id="9bafe-162">/IFD/EXIF/{UShort = 33434}</span><span class="sxs-lookup"><span data-stu-id="9bafe-162">/ifd/exif/{ushort=33434}</span></span>   |
| <span data-ttu-id="9bafe-163">2</span><span class="sxs-lookup"><span data-stu-id="9bafe-163">2</span></span>     | <span data-ttu-id="9bafe-164">/ifd/xmp/exif:exposuretime</span><span class="sxs-lookup"><span data-stu-id="9bafe-164">/ifd/xmp/exif:exposuretime</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9bafe-165">Notes</span><span class="sxs-lookup"><span data-stu-id="9bafe-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="9bafe-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9bafe-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bafe-167">System. photo. ExposureTime</span><span class="sxs-lookup"><span data-stu-id="9bafe-167">System.Photo.ExposureTime</span></span>](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
