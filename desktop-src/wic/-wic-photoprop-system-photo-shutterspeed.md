---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. ShutterSpeed.
ms.assetid: f320944c-978d-4a3c-9bf8-5c5652123e29
title: Stratégie de métadonnées de photo System. photo. ShutterSpeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8df8c9e7fda5643fed022f67c3b6b7846e7a72f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536796"
---
# <a name="systemphotoshutterspeed-photo-metadata-policy"></a><span data-ttu-id="db11d-103">Stratégie de métadonnées de photo System. photo. ShutterSpeed</span><span class="sxs-lookup"><span data-stu-id="db11d-103">System.Photo.ShutterSpeed Photo Metadata Policy</span></span>

<span data-ttu-id="db11d-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. ShutterSpeed](../properties/props-system-photo-shutterspeed.md) .</span><span class="sxs-lookup"><span data-stu-id="db11d-104">The photo metadata policy for the [System.Photo.ShutterSpeed](../properties/props-system-photo-shutterspeed.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="db11d-105">A-la</span><span class="sxs-lookup"><span data-stu-id="db11d-105">PKEY</span></span>

<span data-ttu-id="db11d-106">\_Photo \_ ShutterSpeed</span><span class="sxs-lookup"><span data-stu-id="db11d-106">PKEY\_Photo\_ShutterSpeed</span></span>

### <a name="containers"></a><span data-ttu-id="db11d-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="db11d-107">Containers</span></span>

<span data-ttu-id="db11d-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="db11d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="db11d-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="db11d-109">Read-Only</span></span>

<span data-ttu-id="db11d-110">Oui</span><span class="sxs-lookup"><span data-stu-id="db11d-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="db11d-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="db11d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="db11d-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="db11d-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="db11d-113">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="db11d-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="db11d-114">Cette valeur est générée à partir de System. photo. ShutterSpeedNumerator et de System. photo. ShutterSpeedDenominator.</span><span class="sxs-lookup"><span data-stu-id="db11d-114">This value is generated from System.Photo.ShutterSpeedNumerator and System.Photo.ShutterSpeedDenominator.</span></span> <span data-ttu-id="db11d-115">Il ne peut pas être écrit directement.</span><span class="sxs-lookup"><span data-stu-id="db11d-115">It cannot be written directly.</span></span> <span data-ttu-id="db11d-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="db11d-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="db11d-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="db11d-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="db11d-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="db11d-118">Read Paths</span></span>



| <span data-ttu-id="db11d-119">Commande</span><span class="sxs-lookup"><span data-stu-id="db11d-119">Order</span></span> | <span data-ttu-id="db11d-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="db11d-120">Path</span></span>                          | <span data-ttu-id="db11d-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="db11d-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="db11d-122">1</span><span class="sxs-lookup"><span data-stu-id="db11d-122">1</span></span>     | <span data-ttu-id="db11d-123">/App1/IFD/EXIF/{UShort = 37377}</span><span class="sxs-lookup"><span data-stu-id="db11d-123">/app1/ifd/exif/{ushort=37377}</span></span> |             |
| <span data-ttu-id="db11d-124">2</span><span class="sxs-lookup"><span data-stu-id="db11d-124">2</span></span>     | <span data-ttu-id="db11d-125">/xmp/exif:ShutterSpeedValue</span><span class="sxs-lookup"><span data-stu-id="db11d-125">/xmp/exif:ShutterSpeedValue</span></span>   |             |



 

### <a name="write-paths"></a><span data-ttu-id="db11d-126">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="db11d-126">Write Paths</span></span>



| <span data-ttu-id="db11d-127">Commande</span><span class="sxs-lookup"><span data-stu-id="db11d-127">Order</span></span> | <span data-ttu-id="db11d-128">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="db11d-128">Path</span></span>                          | <span data-ttu-id="db11d-129">Format de disque</span><span class="sxs-lookup"><span data-stu-id="db11d-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="db11d-130">1</span><span class="sxs-lookup"><span data-stu-id="db11d-130">1</span></span>     | <span data-ttu-id="db11d-131">/App1/IFD/EXIF/{UShort = 37377}</span><span class="sxs-lookup"><span data-stu-id="db11d-131">/app1/ifd/exif/{ushort=37377}</span></span> |             |
| <span data-ttu-id="db11d-132">2</span><span class="sxs-lookup"><span data-stu-id="db11d-132">2</span></span>     | <span data-ttu-id="db11d-133">/xmp/exif:ShutterSpeedValue</span><span class="sxs-lookup"><span data-stu-id="db11d-133">/xmp/exif:ShutterSpeedValue</span></span>   |             |



 

### <a name="remove-paths"></a><span data-ttu-id="db11d-134">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="db11d-134">Remove Paths</span></span>



| <span data-ttu-id="db11d-135">Commande</span><span class="sxs-lookup"><span data-stu-id="db11d-135">Order</span></span> | <span data-ttu-id="db11d-136">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="db11d-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="db11d-137">1</span><span class="sxs-lookup"><span data-stu-id="db11d-137">1</span></span>     | <span data-ttu-id="db11d-138">/App1/IFD/EXIF/{UShort = 37377}</span><span class="sxs-lookup"><span data-stu-id="db11d-138">/app1/ifd/exif/{ushort=37377}</span></span> |
| <span data-ttu-id="db11d-139">2</span><span class="sxs-lookup"><span data-stu-id="db11d-139">2</span></span>     | <span data-ttu-id="db11d-140">/xmp/exif:shutterspeedvalue</span><span class="sxs-lookup"><span data-stu-id="db11d-140">/xmp/exif:shutterspeedvalue</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="db11d-141">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="db11d-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="db11d-142">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="db11d-142">Read Paths</span></span>



| <span data-ttu-id="db11d-143">Commande</span><span class="sxs-lookup"><span data-stu-id="db11d-143">Order</span></span> | <span data-ttu-id="db11d-144">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="db11d-144">Path</span></span>                            | <span data-ttu-id="db11d-145">Format de disque</span><span class="sxs-lookup"><span data-stu-id="db11d-145">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="db11d-146">1</span><span class="sxs-lookup"><span data-stu-id="db11d-146">1</span></span>     | <span data-ttu-id="db11d-147">/IFD/EXIF/{UShort = 37377}</span><span class="sxs-lookup"><span data-stu-id="db11d-147">/ifd/exif/{ushort=37377}</span></span>        |             |
| <span data-ttu-id="db11d-148">2</span><span class="sxs-lookup"><span data-stu-id="db11d-148">2</span></span>     | <span data-ttu-id="db11d-149">/ifd/xmp/exif:ShutterSpeedValue</span><span class="sxs-lookup"><span data-stu-id="db11d-149">/ifd/xmp/exif:ShutterSpeedValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="db11d-150">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="db11d-150">Write Paths</span></span>



| <span data-ttu-id="db11d-151">Commande</span><span class="sxs-lookup"><span data-stu-id="db11d-151">Order</span></span> | <span data-ttu-id="db11d-152">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="db11d-152">Path</span></span>                            | <span data-ttu-id="db11d-153">Format de disque</span><span class="sxs-lookup"><span data-stu-id="db11d-153">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="db11d-154">1</span><span class="sxs-lookup"><span data-stu-id="db11d-154">1</span></span>     | <span data-ttu-id="db11d-155">/IFD/EXIF/{UShort = 37377}</span><span class="sxs-lookup"><span data-stu-id="db11d-155">/ifd/exif/{ushort=37377}</span></span>        |             |
| <span data-ttu-id="db11d-156">2</span><span class="sxs-lookup"><span data-stu-id="db11d-156">2</span></span>     | <span data-ttu-id="db11d-157">/ifd/xmp/exif:ShutterSpeedValue</span><span class="sxs-lookup"><span data-stu-id="db11d-157">/ifd/xmp/exif:ShutterSpeedValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="db11d-158">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="db11d-158">Remove Paths</span></span>



| <span data-ttu-id="db11d-159">Commande</span><span class="sxs-lookup"><span data-stu-id="db11d-159">Order</span></span> | <span data-ttu-id="db11d-160">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="db11d-160">Path</span></span>                            |
|-------|---------------------------------|
| <span data-ttu-id="db11d-161">1</span><span class="sxs-lookup"><span data-stu-id="db11d-161">1</span></span>     | <span data-ttu-id="db11d-162">/IFD/EXIF/{UShort = 37377}</span><span class="sxs-lookup"><span data-stu-id="db11d-162">/ifd/exif/{ushort=37377}</span></span>        |
| <span data-ttu-id="db11d-163">2</span><span class="sxs-lookup"><span data-stu-id="db11d-163">2</span></span>     | <span data-ttu-id="db11d-164">/ifd/xmp/exif:shutterspeedvalue</span><span class="sxs-lookup"><span data-stu-id="db11d-164">/ifd/xmp/exif:shutterspeedvalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="db11d-165">Notes</span><span class="sxs-lookup"><span data-stu-id="db11d-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="db11d-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="db11d-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db11d-167">System. photo. ShutterSpeed</span><span class="sxs-lookup"><span data-stu-id="db11d-167">System.Photo.ShutterSpeed</span></span>](../properties/props-system-photo-shutterspeed.md)
</dt> </dl>

 

 
