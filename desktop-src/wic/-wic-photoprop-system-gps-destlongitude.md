---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. DestLongitude.
ms.assetid: 885a522d-e1bf-43fb-a996-97e725b6cf0c
title: Stratégie de métadonnées de photo System. GPS. DestLongitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e0a4f56e49dfbb3397b96cf7fae35a6065b7aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035034"
---
# <a name="systemgpsdestlongitude-photo-metadata-policy"></a><span data-ttu-id="66fb6-103">Stratégie de métadonnées de photo System. GPS. DestLongitude</span><span class="sxs-lookup"><span data-stu-id="66fb6-103">System.GPS.DestLongitude Photo Metadata Policy</span></span>

<span data-ttu-id="66fb6-104">Stratégie de métadonnées de la photo pour la propriété [System. GPS. DestLongitude](../properties/props-system-gps-destlongitude.md) .</span><span class="sxs-lookup"><span data-stu-id="66fb6-104">The photo metadata policy for the [System.GPS.DestLongitude](../properties/props-system-gps-destlongitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="66fb6-105">A-la</span><span class="sxs-lookup"><span data-stu-id="66fb6-105">PKEY</span></span>

<span data-ttu-id="66fb6-106">\_DestLongitude GPS \_</span><span class="sxs-lookup"><span data-stu-id="66fb6-106">PKEY\_GPS\_DestLongitude</span></span>

### <a name="containers"></a><span data-ttu-id="66fb6-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="66fb6-107">Containers</span></span>

<span data-ttu-id="66fb6-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="66fb6-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="66fb6-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66fb6-109">Read-Only</span></span>

<span data-ttu-id="66fb6-110">Oui</span><span class="sxs-lookup"><span data-stu-id="66fb6-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="66fb6-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="66fb6-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="66fb6-112">VT \_ Vector \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="66fb6-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="66fb6-113">Type de PROPVARIANT d’entrée</span><span class="sxs-lookup"><span data-stu-id="66fb6-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="66fb6-114">VT \_ Vector \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="66fb6-114">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="66fb6-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="66fb6-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="66fb6-116">Cette valeur est générée à partir de System. GPS. DestLongitudeNumerator et de System. GPS. DestLongitudeDenominator.</span><span class="sxs-lookup"><span data-stu-id="66fb6-116">This value is generated from System.GPS.DestLongitudeNumerator and System.GPS.DestLongitudeDenominator.</span></span> <span data-ttu-id="66fb6-117">Il ne peut pas être écrit directement.</span><span class="sxs-lookup"><span data-stu-id="66fb6-117">It cannot be written directly.</span></span> <span data-ttu-id="66fb6-118">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="66fb6-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="66fb6-119">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="66fb6-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="66fb6-120">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="66fb6-120">Read Paths</span></span>



| <span data-ttu-id="66fb6-121">Commande</span><span class="sxs-lookup"><span data-stu-id="66fb6-121">Order</span></span> | <span data-ttu-id="66fb6-122">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="66fb6-122">Path</span></span>                       | <span data-ttu-id="66fb6-123">Format de disque</span><span class="sxs-lookup"><span data-stu-id="66fb6-123">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="66fb6-124">1</span><span class="sxs-lookup"><span data-stu-id="66fb6-124">1</span></span>     | <span data-ttu-id="66fb6-125">/App1/IFD/GPS/{UShort = 22}</span><span class="sxs-lookup"><span data-stu-id="66fb6-125">/app1/ifd/gps/{ushort=22}</span></span>  |             |
| <span data-ttu-id="66fb6-126">2</span><span class="sxs-lookup"><span data-stu-id="66fb6-126">2</span></span>     | <span data-ttu-id="66fb6-127">/xmp/exif:GPSDestLongitude</span><span class="sxs-lookup"><span data-stu-id="66fb6-127">/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="66fb6-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="66fb6-128">Write Paths</span></span>



| <span data-ttu-id="66fb6-129">Commande</span><span class="sxs-lookup"><span data-stu-id="66fb6-129">Order</span></span> | <span data-ttu-id="66fb6-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="66fb6-130">Path</span></span>                       | <span data-ttu-id="66fb6-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="66fb6-131">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="66fb6-132">1</span><span class="sxs-lookup"><span data-stu-id="66fb6-132">1</span></span>     | <span data-ttu-id="66fb6-133">/App1/IFD/GPS/{UShort = 22}</span><span class="sxs-lookup"><span data-stu-id="66fb6-133">/app1/ifd/gps/{ushort=22}</span></span>  |             |
| <span data-ttu-id="66fb6-134">2</span><span class="sxs-lookup"><span data-stu-id="66fb6-134">2</span></span>     | <span data-ttu-id="66fb6-135">/xmp/exif:GPSDestLongitude</span><span class="sxs-lookup"><span data-stu-id="66fb6-135">/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="66fb6-136">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="66fb6-136">Remove Paths</span></span>



| <span data-ttu-id="66fb6-137">Commande</span><span class="sxs-lookup"><span data-stu-id="66fb6-137">Order</span></span> | <span data-ttu-id="66fb6-138">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="66fb6-138">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="66fb6-139">1</span><span class="sxs-lookup"><span data-stu-id="66fb6-139">1</span></span>     | <span data-ttu-id="66fb6-140">/App1/IFD/GPS/{UShort = 22}</span><span class="sxs-lookup"><span data-stu-id="66fb6-140">/app1/ifd/gps/{ushort=22}</span></span>  |
| <span data-ttu-id="66fb6-141">2</span><span class="sxs-lookup"><span data-stu-id="66fb6-141">2</span></span>     | <span data-ttu-id="66fb6-142">/xmp/exif:gpsdestlongitude</span><span class="sxs-lookup"><span data-stu-id="66fb6-142">/xmp/exif:gpsdestlongitude</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="66fb6-143">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="66fb6-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="66fb6-144">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="66fb6-144">Read Paths</span></span>



| <span data-ttu-id="66fb6-145">Commande</span><span class="sxs-lookup"><span data-stu-id="66fb6-145">Order</span></span> | <span data-ttu-id="66fb6-146">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="66fb6-146">Path</span></span>                           | <span data-ttu-id="66fb6-147">Format de disque</span><span class="sxs-lookup"><span data-stu-id="66fb6-147">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="66fb6-148">1</span><span class="sxs-lookup"><span data-stu-id="66fb6-148">1</span></span>     | <span data-ttu-id="66fb6-149">/IFD/GPS/{UShort = 22}</span><span class="sxs-lookup"><span data-stu-id="66fb6-149">/ifd/gps/{ushort=22}</span></span>           |             |
| <span data-ttu-id="66fb6-150">2</span><span class="sxs-lookup"><span data-stu-id="66fb6-150">2</span></span>     | <span data-ttu-id="66fb6-151">/ifd/xmp/exif:GPSDestLongitude</span><span class="sxs-lookup"><span data-stu-id="66fb6-151">/ifd/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="66fb6-152">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="66fb6-152">Write Paths</span></span>



| <span data-ttu-id="66fb6-153">Commande</span><span class="sxs-lookup"><span data-stu-id="66fb6-153">Order</span></span> | <span data-ttu-id="66fb6-154">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="66fb6-154">Path</span></span>                           | <span data-ttu-id="66fb6-155">Format de disque</span><span class="sxs-lookup"><span data-stu-id="66fb6-155">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="66fb6-156">1</span><span class="sxs-lookup"><span data-stu-id="66fb6-156">1</span></span>     | <span data-ttu-id="66fb6-157">/IFD/GPS/{UShort = 22}</span><span class="sxs-lookup"><span data-stu-id="66fb6-157">/ifd/gps/{ushort=22}</span></span>           |             |
| <span data-ttu-id="66fb6-158">2</span><span class="sxs-lookup"><span data-stu-id="66fb6-158">2</span></span>     | <span data-ttu-id="66fb6-159">/ifd/xmp/exif:GPSDestLongitude</span><span class="sxs-lookup"><span data-stu-id="66fb6-159">/ifd/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="66fb6-160">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="66fb6-160">Remove Paths</span></span>



| <span data-ttu-id="66fb6-161">Commande</span><span class="sxs-lookup"><span data-stu-id="66fb6-161">Order</span></span> | <span data-ttu-id="66fb6-162">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="66fb6-162">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="66fb6-163">1</span><span class="sxs-lookup"><span data-stu-id="66fb6-163">1</span></span>     | <span data-ttu-id="66fb6-164">/IFD/GPS/{UShort = 22}</span><span class="sxs-lookup"><span data-stu-id="66fb6-164">/ifd/gps/{ushort=22}</span></span>           |
| <span data-ttu-id="66fb6-165">2</span><span class="sxs-lookup"><span data-stu-id="66fb6-165">2</span></span>     | <span data-ttu-id="66fb6-166">/ifd/xmp/exif:gpsdestlongitude</span><span class="sxs-lookup"><span data-stu-id="66fb6-166">/ifd/xmp/exif:gpsdestlongitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="66fb6-167">Notes</span><span class="sxs-lookup"><span data-stu-id="66fb6-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="66fb6-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="66fb6-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66fb6-169">System. GPS. DestLongitude</span><span class="sxs-lookup"><span data-stu-id="66fb6-169">System.GPS.DestLongitude</span></span>](../properties/props-system-gps-destlongitude.md)
</dt> </dl>

 

 
