---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. ImgDirection.
ms.assetid: c9a0f5de-4010-4251-a5d5-8728b7ae6d33
title: Stratégie de métadonnées de photo System. GPS. ImgDirection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013edd632f98f1359c4f3c04856b0409c70eaa56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521175"
---
# <a name="systemgpsimgdirection-photo-metadata-policy"></a><span data-ttu-id="07b20-103">Stratégie de métadonnées de photo System. GPS. ImgDirection</span><span class="sxs-lookup"><span data-stu-id="07b20-103">System.GPS.ImgDirection Photo Metadata Policy</span></span>

<span data-ttu-id="07b20-104">Stratégie de métadonnées de la photo pour la propriété [System. GPS. ImgDirection](../properties/props-system-gps-imgdirection.md) .</span><span class="sxs-lookup"><span data-stu-id="07b20-104">The photo metadata policy for the [System.GPS.ImgDirection](../properties/props-system-gps-imgdirection.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="07b20-105">A-la</span><span class="sxs-lookup"><span data-stu-id="07b20-105">PKEY</span></span>

<span data-ttu-id="07b20-106">\_ImgDirection GPS \_</span><span class="sxs-lookup"><span data-stu-id="07b20-106">PKEY\_GPS\_ImgDirection</span></span>

### <a name="containers"></a><span data-ttu-id="07b20-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="07b20-107">Containers</span></span>

<span data-ttu-id="07b20-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="07b20-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="07b20-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="07b20-109">Read-Only</span></span>

<span data-ttu-id="07b20-110">Oui</span><span class="sxs-lookup"><span data-stu-id="07b20-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="07b20-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="07b20-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="07b20-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="07b20-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="07b20-113">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="07b20-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="07b20-114">Cette valeur peut être écrite en écrivant dans System. GPS. ImgDirectionNumerator et System. GPS. ImgDirectionDenominator.</span><span class="sxs-lookup"><span data-stu-id="07b20-114">This value can be written by writing to System.GPS.ImgDirectionNumerator and System.GPS.ImgDirectionDenominator.</span></span> <span data-ttu-id="07b20-115">Il ne peut pas être écrit directement.</span><span class="sxs-lookup"><span data-stu-id="07b20-115">It cannot be written directly.</span></span> <span data-ttu-id="07b20-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="07b20-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="07b20-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="07b20-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="07b20-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="07b20-118">Read Paths</span></span>



| <span data-ttu-id="07b20-119">Commande</span><span class="sxs-lookup"><span data-stu-id="07b20-119">Order</span></span> | <span data-ttu-id="07b20-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="07b20-120">Path</span></span>                      | <span data-ttu-id="07b20-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="07b20-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="07b20-122">1</span><span class="sxs-lookup"><span data-stu-id="07b20-122">1</span></span>     | <span data-ttu-id="07b20-123">/App1/IFD/GPS/{UShort = 17}</span><span class="sxs-lookup"><span data-stu-id="07b20-123">/app1/ifd/gps/{ushort=17}</span></span> |             |
| <span data-ttu-id="07b20-124">2</span><span class="sxs-lookup"><span data-stu-id="07b20-124">2</span></span>     | <span data-ttu-id="07b20-125">/xmp/exif:GPSImgDirection</span><span class="sxs-lookup"><span data-stu-id="07b20-125">/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="07b20-126">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="07b20-126">Write Paths</span></span>



| <span data-ttu-id="07b20-127">Commande</span><span class="sxs-lookup"><span data-stu-id="07b20-127">Order</span></span> | <span data-ttu-id="07b20-128">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="07b20-128">Path</span></span>                      | <span data-ttu-id="07b20-129">Format de disque</span><span class="sxs-lookup"><span data-stu-id="07b20-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="07b20-130">1</span><span class="sxs-lookup"><span data-stu-id="07b20-130">1</span></span>     | <span data-ttu-id="07b20-131">/App1/IFD/GPS/{UShort = 17}</span><span class="sxs-lookup"><span data-stu-id="07b20-131">/app1/ifd/gps/{ushort=17}</span></span> |             |
| <span data-ttu-id="07b20-132">2</span><span class="sxs-lookup"><span data-stu-id="07b20-132">2</span></span>     | <span data-ttu-id="07b20-133">/xmp/exif:GPSImgDirection</span><span class="sxs-lookup"><span data-stu-id="07b20-133">/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="07b20-134">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="07b20-134">Remove Paths</span></span>



| <span data-ttu-id="07b20-135">Commande</span><span class="sxs-lookup"><span data-stu-id="07b20-135">Order</span></span> | <span data-ttu-id="07b20-136">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="07b20-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="07b20-137">1</span><span class="sxs-lookup"><span data-stu-id="07b20-137">1</span></span>     | <span data-ttu-id="07b20-138">/App1/IFD/GPS/{UShort = 17}</span><span class="sxs-lookup"><span data-stu-id="07b20-138">/app1/ifd/gps/{ushort=17}</span></span> |
| <span data-ttu-id="07b20-139">2</span><span class="sxs-lookup"><span data-stu-id="07b20-139">2</span></span>     | <span data-ttu-id="07b20-140">/xmp/exif:gpsimgdirection</span><span class="sxs-lookup"><span data-stu-id="07b20-140">/xmp/exif:gpsimgdirection</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="07b20-141">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="07b20-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="07b20-142">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="07b20-142">Read Paths</span></span>



| <span data-ttu-id="07b20-143">Commande</span><span class="sxs-lookup"><span data-stu-id="07b20-143">Order</span></span> | <span data-ttu-id="07b20-144">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="07b20-144">Path</span></span>                          | <span data-ttu-id="07b20-145">Format de disque</span><span class="sxs-lookup"><span data-stu-id="07b20-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="07b20-146">1</span><span class="sxs-lookup"><span data-stu-id="07b20-146">1</span></span>     | <span data-ttu-id="07b20-147">/IFD/GPS/{UShort = 17}</span><span class="sxs-lookup"><span data-stu-id="07b20-147">/ifd/gps/{ushort=17}</span></span>          |             |
| <span data-ttu-id="07b20-148">2</span><span class="sxs-lookup"><span data-stu-id="07b20-148">2</span></span>     | <span data-ttu-id="07b20-149">/ifd/xmp/exif:GPSImgDirection</span><span class="sxs-lookup"><span data-stu-id="07b20-149">/ifd/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="07b20-150">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="07b20-150">Write Paths</span></span>



| <span data-ttu-id="07b20-151">Commande</span><span class="sxs-lookup"><span data-stu-id="07b20-151">Order</span></span> | <span data-ttu-id="07b20-152">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="07b20-152">Path</span></span>                          | <span data-ttu-id="07b20-153">Format de disque</span><span class="sxs-lookup"><span data-stu-id="07b20-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="07b20-154">1</span><span class="sxs-lookup"><span data-stu-id="07b20-154">1</span></span>     | <span data-ttu-id="07b20-155">/IFD/GPS/{UShort = 17}</span><span class="sxs-lookup"><span data-stu-id="07b20-155">/ifd/gps/{ushort=17}</span></span>          |             |
| <span data-ttu-id="07b20-156">2</span><span class="sxs-lookup"><span data-stu-id="07b20-156">2</span></span>     | <span data-ttu-id="07b20-157">/ifd/xmp/exif:GPSImgDirection</span><span class="sxs-lookup"><span data-stu-id="07b20-157">/ifd/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="07b20-158">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="07b20-158">Remove Paths</span></span>



| <span data-ttu-id="07b20-159">Commande</span><span class="sxs-lookup"><span data-stu-id="07b20-159">Order</span></span> | <span data-ttu-id="07b20-160">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="07b20-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="07b20-161">1</span><span class="sxs-lookup"><span data-stu-id="07b20-161">1</span></span>     | <span data-ttu-id="07b20-162">/IFD/GPS/{UShort = 17}</span><span class="sxs-lookup"><span data-stu-id="07b20-162">/ifd/gps/{ushort=17}</span></span>          |
| <span data-ttu-id="07b20-163">2</span><span class="sxs-lookup"><span data-stu-id="07b20-163">2</span></span>     | <span data-ttu-id="07b20-164">/ifd/xmp/exif:gpsimgdirection</span><span class="sxs-lookup"><span data-stu-id="07b20-164">/ifd/xmp/exif:gpsimgdirection</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="07b20-165">Notes</span><span class="sxs-lookup"><span data-stu-id="07b20-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="07b20-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="07b20-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07b20-167">System. GPS. ImgDirection</span><span class="sxs-lookup"><span data-stu-id="07b20-167">System.GPS.ImgDirection</span></span>](../properties/props-system-gps-imgdirection.md)
</dt> </dl>

 

 
