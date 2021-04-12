---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. DigitalZoom.
ms.assetid: 22a69d3e-4ec3-4652-b4bb-dfcfffc2322b
title: Stratégie de métadonnées de photo System. photo. DigitalZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf440e92243eb2102ac6abaa349ea83e58d9a2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319946"
---
# <a name="systemphotodigitalzoom-photo-metadata-policy"></a><span data-ttu-id="37529-103">Stratégie de métadonnées de photo System. photo. DigitalZoom</span><span class="sxs-lookup"><span data-stu-id="37529-103">System.Photo.DigitalZoom Photo Metadata Policy</span></span>

<span data-ttu-id="37529-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. DigitalZoom](../properties/props-system-photo-digitalzoom.md) .</span><span class="sxs-lookup"><span data-stu-id="37529-104">The photo metadata policy for the [System.Photo.DigitalZoom](../properties/props-system-photo-digitalzoom.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="37529-105">A-la</span><span class="sxs-lookup"><span data-stu-id="37529-105">PKEY</span></span>

<span data-ttu-id="37529-106">\_Photo \_ DigitalZoom</span><span class="sxs-lookup"><span data-stu-id="37529-106">PKEY\_Photo\_DigitalZoom</span></span>

### <a name="containers"></a><span data-ttu-id="37529-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="37529-107">Containers</span></span>

<span data-ttu-id="37529-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="37529-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="37529-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37529-109">Read-Only</span></span>

<span data-ttu-id="37529-110">Oui</span><span class="sxs-lookup"><span data-stu-id="37529-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="37529-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="37529-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="37529-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="37529-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="37529-113">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="37529-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="37529-114">Cette valeur est générée à partir de System. photo. DigitalZoomNumerator et de System. photo. DigitalZoomDenominator.</span><span class="sxs-lookup"><span data-stu-id="37529-114">This value is generated from System.Photo.DigitalZoomNumerator and System.Photo.DigitalZoomDenominator.</span></span> <span data-ttu-id="37529-115">Il ne peut pas être écrit directement.</span><span class="sxs-lookup"><span data-stu-id="37529-115">It cannot be written directly.</span></span> <span data-ttu-id="37529-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="37529-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="37529-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="37529-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="37529-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="37529-118">Read Paths</span></span>



| <span data-ttu-id="37529-119">Commande</span><span class="sxs-lookup"><span data-stu-id="37529-119">Order</span></span> | <span data-ttu-id="37529-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="37529-120">Path</span></span>                          | <span data-ttu-id="37529-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="37529-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="37529-122">1</span><span class="sxs-lookup"><span data-stu-id="37529-122">1</span></span>     | <span data-ttu-id="37529-123">/App1/IFD/EXIF/{UShort = 41988}</span><span class="sxs-lookup"><span data-stu-id="37529-123">/app1/ifd/exif/{ushort=41988}</span></span> |             |
| <span data-ttu-id="37529-124">2</span><span class="sxs-lookup"><span data-stu-id="37529-124">2</span></span>     | <span data-ttu-id="37529-125">/xmp/exif:DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="37529-125">/xmp/exif:DigitalZoomRatio</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="37529-126">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="37529-126">Write Paths</span></span>



| <span data-ttu-id="37529-127">Commande</span><span class="sxs-lookup"><span data-stu-id="37529-127">Order</span></span> | <span data-ttu-id="37529-128">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="37529-128">Path</span></span>                          | <span data-ttu-id="37529-129">Format de disque</span><span class="sxs-lookup"><span data-stu-id="37529-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="37529-130">1</span><span class="sxs-lookup"><span data-stu-id="37529-130">1</span></span>     | <span data-ttu-id="37529-131">/App1/IFD/EXIF/{UShort = 41988}</span><span class="sxs-lookup"><span data-stu-id="37529-131">/app1/ifd/exif/{ushort=41988}</span></span> |             |
| <span data-ttu-id="37529-132">2</span><span class="sxs-lookup"><span data-stu-id="37529-132">2</span></span>     | <span data-ttu-id="37529-133">/xmp/exif:DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="37529-133">/xmp/exif:DigitalZoomRatio</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="37529-134">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="37529-134">Remove Paths</span></span>



| <span data-ttu-id="37529-135">Commande</span><span class="sxs-lookup"><span data-stu-id="37529-135">Order</span></span> | <span data-ttu-id="37529-136">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="37529-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="37529-137">1</span><span class="sxs-lookup"><span data-stu-id="37529-137">1</span></span>     | <span data-ttu-id="37529-138">/App1/IFD/EXIF/{UShort = 41988}</span><span class="sxs-lookup"><span data-stu-id="37529-138">/app1/ifd/exif/{ushort=41988}</span></span> |
| <span data-ttu-id="37529-139">2</span><span class="sxs-lookup"><span data-stu-id="37529-139">2</span></span>     | <span data-ttu-id="37529-140">/xmp/exif:digitalzoomratio</span><span class="sxs-lookup"><span data-stu-id="37529-140">/xmp/exif:digitalzoomratio</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="37529-141">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="37529-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="37529-142">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="37529-142">Read Paths</span></span>



| <span data-ttu-id="37529-143">Commande</span><span class="sxs-lookup"><span data-stu-id="37529-143">Order</span></span> | <span data-ttu-id="37529-144">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="37529-144">Path</span></span>                           | <span data-ttu-id="37529-145">Format de disque</span><span class="sxs-lookup"><span data-stu-id="37529-145">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="37529-146">1</span><span class="sxs-lookup"><span data-stu-id="37529-146">1</span></span>     | <span data-ttu-id="37529-147">/IFD/EXIF/{UShort = 41988}</span><span class="sxs-lookup"><span data-stu-id="37529-147">/ifd/exif/{ushort=41988}</span></span>       |             |
| <span data-ttu-id="37529-148">2</span><span class="sxs-lookup"><span data-stu-id="37529-148">2</span></span>     | <span data-ttu-id="37529-149">/ifd/xmp/exif:DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="37529-149">/ifd/xmp/exif:DigitalZoomRatio</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="37529-150">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="37529-150">Write Paths</span></span>



| <span data-ttu-id="37529-151">Commande</span><span class="sxs-lookup"><span data-stu-id="37529-151">Order</span></span> | <span data-ttu-id="37529-152">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="37529-152">Path</span></span>                           | <span data-ttu-id="37529-153">Format de disque</span><span class="sxs-lookup"><span data-stu-id="37529-153">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="37529-154">1</span><span class="sxs-lookup"><span data-stu-id="37529-154">1</span></span>     | <span data-ttu-id="37529-155">/IFD/EXIF/{UShort = 41988}</span><span class="sxs-lookup"><span data-stu-id="37529-155">/ifd/exif/{ushort=41988}</span></span>       |             |
| <span data-ttu-id="37529-156">2</span><span class="sxs-lookup"><span data-stu-id="37529-156">2</span></span>     | <span data-ttu-id="37529-157">/ifd/xmp/exif:DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="37529-157">/ifd/xmp/exif:DigitalZoomRatio</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="37529-158">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="37529-158">Remove Paths</span></span>



| <span data-ttu-id="37529-159">Commande</span><span class="sxs-lookup"><span data-stu-id="37529-159">Order</span></span> | <span data-ttu-id="37529-160">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="37529-160">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="37529-161">1</span><span class="sxs-lookup"><span data-stu-id="37529-161">1</span></span>     | <span data-ttu-id="37529-162">/IFD/EXIF/{UShort = 41988}</span><span class="sxs-lookup"><span data-stu-id="37529-162">/ifd/exif/{ushort=41988}</span></span>       |
| <span data-ttu-id="37529-163">2</span><span class="sxs-lookup"><span data-stu-id="37529-163">2</span></span>     | <span data-ttu-id="37529-164">/ifd/xmp/exif:digitalzoomratio</span><span class="sxs-lookup"><span data-stu-id="37529-164">/ifd/xmp/exif:digitalzoomratio</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="37529-165">Notes</span><span class="sxs-lookup"><span data-stu-id="37529-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="37529-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="37529-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37529-167">System. photo. DigitalZoom</span><span class="sxs-lookup"><span data-stu-id="37529-167">System.Photo.DigitalZoom</span></span>](../properties/props-system-photo-digitalzoom.md)
</dt> </dl>

 

 
