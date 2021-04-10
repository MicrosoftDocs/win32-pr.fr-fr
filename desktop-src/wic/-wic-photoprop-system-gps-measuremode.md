---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. MeasureMode.
ms.assetid: 911a0d81-bd12-4155-b45a-ae1a18f2dd07
title: Stratégie de métadonnées de photo System. GPS. MeasureMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a9449ca9a7d1ee5ef213c37562392be2842a09f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952131"
---
# <a name="systemgpsmeasuremode-photo-metadata-policy"></a><span data-ttu-id="83c6b-103">Stratégie de métadonnées de photo System. GPS. MeasureMode</span><span class="sxs-lookup"><span data-stu-id="83c6b-103">System.GPS.MeasureMode Photo Metadata Policy</span></span>

<span data-ttu-id="83c6b-104">Stratégie de métadonnées de la photo pour la propriété [System. GPS. MeasureMode](../properties/props-system-gps-measuremode.md) .</span><span class="sxs-lookup"><span data-stu-id="83c6b-104">The photo metadata policy for the [System.GPS.MeasureMode](../properties/props-system-gps-measuremode.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="83c6b-105">A-la</span><span class="sxs-lookup"><span data-stu-id="83c6b-105">PKEY</span></span>

<span data-ttu-id="83c6b-106">\_MeasureMode GPS \_</span><span class="sxs-lookup"><span data-stu-id="83c6b-106">PKEY\_GPS\_MeasureMode</span></span>

### <a name="containers"></a><span data-ttu-id="83c6b-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="83c6b-107">Containers</span></span>

<span data-ttu-id="83c6b-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="83c6b-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="83c6b-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83c6b-109">Read-Only</span></span>

<span data-ttu-id="83c6b-110">Non</span><span class="sxs-lookup"><span data-stu-id="83c6b-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="83c6b-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="83c6b-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="83c6b-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="83c6b-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="83c6b-113">Type de PROPVARIANT d’entrée</span><span class="sxs-lookup"><span data-stu-id="83c6b-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="83c6b-114">VT \_ LPWStr est préféré, mais VT \_ LPSTR est également accepté.</span><span class="sxs-lookup"><span data-stu-id="83c6b-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="83c6b-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="83c6b-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="83c6b-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="83c6b-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="83c6b-117">Stratégies JPEG</span><span class="sxs-lookup"><span data-stu-id="83c6b-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="83c6b-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="83c6b-118">Read Paths</span></span>



| <span data-ttu-id="83c6b-119">Commande</span><span class="sxs-lookup"><span data-stu-id="83c6b-119">Order</span></span> | <span data-ttu-id="83c6b-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="83c6b-120">Path</span></span>                      | <span data-ttu-id="83c6b-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="83c6b-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="83c6b-122">1</span><span class="sxs-lookup"><span data-stu-id="83c6b-122">1</span></span>     | <span data-ttu-id="83c6b-123">/App1/IFD/GPS/{UShort = 10}</span><span class="sxs-lookup"><span data-stu-id="83c6b-123">/app1/ifd/gps/{ushort=10}</span></span> | <span data-ttu-id="83c6b-124">ascii</span><span class="sxs-lookup"><span data-stu-id="83c6b-124">ascii</span></span>       |
| <span data-ttu-id="83c6b-125">2</span><span class="sxs-lookup"><span data-stu-id="83c6b-125">2</span></span>     | <span data-ttu-id="83c6b-126">/xmp/exif:GPSMeasureMode</span><span class="sxs-lookup"><span data-stu-id="83c6b-126">/xmp/exif:GPSMeasureMode</span></span>  | <span data-ttu-id="83c6b-127">unicode</span><span class="sxs-lookup"><span data-stu-id="83c6b-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="83c6b-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="83c6b-128">Write Paths</span></span>



| <span data-ttu-id="83c6b-129">Commande</span><span class="sxs-lookup"><span data-stu-id="83c6b-129">Order</span></span> | <span data-ttu-id="83c6b-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="83c6b-130">Path</span></span>                      | <span data-ttu-id="83c6b-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="83c6b-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="83c6b-132">1</span><span class="sxs-lookup"><span data-stu-id="83c6b-132">1</span></span>     | <span data-ttu-id="83c6b-133">/App1/IFD/GPS/{UShort = 10}</span><span class="sxs-lookup"><span data-stu-id="83c6b-133">/app1/ifd/gps/{ushort=10}</span></span> | <span data-ttu-id="83c6b-134">ascii</span><span class="sxs-lookup"><span data-stu-id="83c6b-134">ascii</span></span>       |
| <span data-ttu-id="83c6b-135">2</span><span class="sxs-lookup"><span data-stu-id="83c6b-135">2</span></span>     | <span data-ttu-id="83c6b-136">/xmp/exif:GPSMeasureMode</span><span class="sxs-lookup"><span data-stu-id="83c6b-136">/xmp/exif:GPSMeasureMode</span></span>  | <span data-ttu-id="83c6b-137">unicode</span><span class="sxs-lookup"><span data-stu-id="83c6b-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="83c6b-138">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="83c6b-138">Remove Paths</span></span>



| <span data-ttu-id="83c6b-139">Commande</span><span class="sxs-lookup"><span data-stu-id="83c6b-139">Order</span></span> | <span data-ttu-id="83c6b-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="83c6b-140">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="83c6b-141">1</span><span class="sxs-lookup"><span data-stu-id="83c6b-141">1</span></span>     | <span data-ttu-id="83c6b-142">/App1/IFD/GPS/{UShort = 10}</span><span class="sxs-lookup"><span data-stu-id="83c6b-142">/app1/ifd/gps/{ushort=10}</span></span> |
| <span data-ttu-id="83c6b-143">2</span><span class="sxs-lookup"><span data-stu-id="83c6b-143">2</span></span>     | <span data-ttu-id="83c6b-144">/xmp/exif:gpsmeasuremode</span><span class="sxs-lookup"><span data-stu-id="83c6b-144">/xmp/exif:gpsmeasuremode</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="83c6b-145">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="83c6b-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="83c6b-146">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="83c6b-146">Read Paths</span></span>



| <span data-ttu-id="83c6b-147">Commande</span><span class="sxs-lookup"><span data-stu-id="83c6b-147">Order</span></span> | <span data-ttu-id="83c6b-148">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="83c6b-148">Path</span></span>                         | <span data-ttu-id="83c6b-149">Format de disque</span><span class="sxs-lookup"><span data-stu-id="83c6b-149">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="83c6b-150">1</span><span class="sxs-lookup"><span data-stu-id="83c6b-150">1</span></span>     | <span data-ttu-id="83c6b-151">/IFD/GPS/{UShort = 10}</span><span class="sxs-lookup"><span data-stu-id="83c6b-151">/ifd/gps/{ushort=10}</span></span>         | <span data-ttu-id="83c6b-152">ascii</span><span class="sxs-lookup"><span data-stu-id="83c6b-152">ascii</span></span>       |
| <span data-ttu-id="83c6b-153">2</span><span class="sxs-lookup"><span data-stu-id="83c6b-153">2</span></span>     | <span data-ttu-id="83c6b-154">/ifd/xmp/exif:GPSMeasureMode</span><span class="sxs-lookup"><span data-stu-id="83c6b-154">/ifd/xmp/exif:GPSMeasureMode</span></span> | <span data-ttu-id="83c6b-155">unicode</span><span class="sxs-lookup"><span data-stu-id="83c6b-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="83c6b-156">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="83c6b-156">Write Paths</span></span>



| <span data-ttu-id="83c6b-157">Commande</span><span class="sxs-lookup"><span data-stu-id="83c6b-157">Order</span></span> | <span data-ttu-id="83c6b-158">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="83c6b-158">Path</span></span>                         | <span data-ttu-id="83c6b-159">Format de disque</span><span class="sxs-lookup"><span data-stu-id="83c6b-159">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="83c6b-160">1</span><span class="sxs-lookup"><span data-stu-id="83c6b-160">1</span></span>     | <span data-ttu-id="83c6b-161">/IFD/GPS/{UShort = 10}</span><span class="sxs-lookup"><span data-stu-id="83c6b-161">/ifd/gps/{ushort=10}</span></span>         | <span data-ttu-id="83c6b-162">ascii</span><span class="sxs-lookup"><span data-stu-id="83c6b-162">ascii</span></span>       |
| <span data-ttu-id="83c6b-163">2</span><span class="sxs-lookup"><span data-stu-id="83c6b-163">2</span></span>     | <span data-ttu-id="83c6b-164">/ifd/xmp/exif:GPSMeasureMode</span><span class="sxs-lookup"><span data-stu-id="83c6b-164">/ifd/xmp/exif:GPSMeasureMode</span></span> | <span data-ttu-id="83c6b-165">unicode</span><span class="sxs-lookup"><span data-stu-id="83c6b-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="83c6b-166">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="83c6b-166">Remove Paths</span></span>



| <span data-ttu-id="83c6b-167">Commande</span><span class="sxs-lookup"><span data-stu-id="83c6b-167">Order</span></span> | <span data-ttu-id="83c6b-168">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="83c6b-168">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="83c6b-169">1</span><span class="sxs-lookup"><span data-stu-id="83c6b-169">1</span></span>     | <span data-ttu-id="83c6b-170">/IFD/GPS/{UShort = 10}</span><span class="sxs-lookup"><span data-stu-id="83c6b-170">/ifd/gps/{ushort=10}</span></span>         |
| <span data-ttu-id="83c6b-171">2</span><span class="sxs-lookup"><span data-stu-id="83c6b-171">2</span></span>     | <span data-ttu-id="83c6b-172">/ifd/xmp/exif:gpsmeasuremode</span><span class="sxs-lookup"><span data-stu-id="83c6b-172">/ifd/xmp/exif:gpsmeasuremode</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="83c6b-173">Notes</span><span class="sxs-lookup"><span data-stu-id="83c6b-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="83c6b-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="83c6b-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83c6b-175">System. GPS. MeasureMode</span><span class="sxs-lookup"><span data-stu-id="83c6b-175">System.GPS.MeasureMode</span></span>](../properties/props-system-gps-measuremode.md)
</dt> </dl>

 

 
