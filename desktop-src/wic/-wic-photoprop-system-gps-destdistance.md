---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. DestDistance.
ms.assetid: 1bd72acb-f462-454d-aec2-72d5b4517de3
title: Stratégie de métadonnées de photo System. GPS. DestDistance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc71c89ae6270f5babf08637f54baaf2cb57aae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520605"
---
# <a name="systemgpsdestdistance-photo-metadata-policy"></a><span data-ttu-id="d4a2a-103">Stratégie de métadonnées de photo System. GPS. DestDistance</span><span class="sxs-lookup"><span data-stu-id="d4a2a-103">System.GPS.DestDistance Photo Metadata Policy</span></span>

<span data-ttu-id="d4a2a-104">Stratégie de métadonnées de la photo pour la propriété [System. GPS. DestDistance](../properties/props-system-gps-destdistance.md) .</span><span class="sxs-lookup"><span data-stu-id="d4a2a-104">The photo metadata policy for the [System.GPS.DestDistance](../properties/props-system-gps-destdistance.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="d4a2a-105">A-la</span><span class="sxs-lookup"><span data-stu-id="d4a2a-105">PKEY</span></span>

<span data-ttu-id="d4a2a-106">\_DestDistance GPS \_</span><span class="sxs-lookup"><span data-stu-id="d4a2a-106">PKEY\_GPS\_DestDistance</span></span>

### <a name="containers"></a><span data-ttu-id="d4a2a-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="d4a2a-107">Containers</span></span>

<span data-ttu-id="d4a2a-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d4a2a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="d4a2a-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d4a2a-109">Read-Only</span></span>

<span data-ttu-id="d4a2a-110">Oui</span><span class="sxs-lookup"><span data-stu-id="d4a2a-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="d4a2a-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="d4a2a-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="d4a2a-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="d4a2a-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="d4a2a-113">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="d4a2a-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="d4a2a-114">Cette valeur est générée à partir de System. GPS. DestDistanceNumerator et de System. GPS. DestDistanceDenominator.</span><span class="sxs-lookup"><span data-stu-id="d4a2a-114">This value is generated from System.GPS.DestDistanceNumerator and System.GPS.DestDistanceDenominator.</span></span> <span data-ttu-id="d4a2a-115">Il ne peut pas être écrit directement.</span><span class="sxs-lookup"><span data-stu-id="d4a2a-115">It cannot be written directly.</span></span> <span data-ttu-id="d4a2a-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="d4a2a-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="d4a2a-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="d4a2a-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="d4a2a-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="d4a2a-118">Read Paths</span></span>



| <span data-ttu-id="d4a2a-119">Commande</span><span class="sxs-lookup"><span data-stu-id="d4a2a-119">Order</span></span> | <span data-ttu-id="d4a2a-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="d4a2a-120">Path</span></span>                      | <span data-ttu-id="d4a2a-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="d4a2a-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="d4a2a-122">1</span><span class="sxs-lookup"><span data-stu-id="d4a2a-122">1</span></span>     | <span data-ttu-id="d4a2a-123">/App1/IFD/GPS/{UShort = 26}</span><span class="sxs-lookup"><span data-stu-id="d4a2a-123">/app1/ifd/gps/{ushort=26}</span></span> |             |
| <span data-ttu-id="d4a2a-124">2</span><span class="sxs-lookup"><span data-stu-id="d4a2a-124">2</span></span>     | <span data-ttu-id="d4a2a-125">/xmp/exif:GPSDestDistance</span><span class="sxs-lookup"><span data-stu-id="d4a2a-125">/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="d4a2a-126">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="d4a2a-126">Write Paths</span></span>



| <span data-ttu-id="d4a2a-127">Commande</span><span class="sxs-lookup"><span data-stu-id="d4a2a-127">Order</span></span> | <span data-ttu-id="d4a2a-128">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="d4a2a-128">Path</span></span>                      | <span data-ttu-id="d4a2a-129">Format de disque</span><span class="sxs-lookup"><span data-stu-id="d4a2a-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="d4a2a-130">1</span><span class="sxs-lookup"><span data-stu-id="d4a2a-130">1</span></span>     | <span data-ttu-id="d4a2a-131">/App1/IFD/GPS/{UShort = 26}</span><span class="sxs-lookup"><span data-stu-id="d4a2a-131">/app1/ifd/gps/{ushort=26}</span></span> |             |
| <span data-ttu-id="d4a2a-132">2</span><span class="sxs-lookup"><span data-stu-id="d4a2a-132">2</span></span>     | <span data-ttu-id="d4a2a-133">/xmp/exif:GPSDestDistance</span><span class="sxs-lookup"><span data-stu-id="d4a2a-133">/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="d4a2a-134">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="d4a2a-134">Remove Paths</span></span>



| <span data-ttu-id="d4a2a-135">Commande</span><span class="sxs-lookup"><span data-stu-id="d4a2a-135">Order</span></span> | <span data-ttu-id="d4a2a-136">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="d4a2a-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="d4a2a-137">1</span><span class="sxs-lookup"><span data-stu-id="d4a2a-137">1</span></span>     | <span data-ttu-id="d4a2a-138">/App1/IFD/GPS/{UShort = 26}</span><span class="sxs-lookup"><span data-stu-id="d4a2a-138">/app1/ifd/gps/{ushort=26}</span></span> |
| <span data-ttu-id="d4a2a-139">2</span><span class="sxs-lookup"><span data-stu-id="d4a2a-139">2</span></span>     | <span data-ttu-id="d4a2a-140">/xmp/exif:gpsdestdistance</span><span class="sxs-lookup"><span data-stu-id="d4a2a-140">/xmp/exif:gpsdestdistance</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="d4a2a-141">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="d4a2a-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="d4a2a-142">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="d4a2a-142">Read Paths</span></span>



| <span data-ttu-id="d4a2a-143">Commande</span><span class="sxs-lookup"><span data-stu-id="d4a2a-143">Order</span></span> | <span data-ttu-id="d4a2a-144">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="d4a2a-144">Path</span></span>                          | <span data-ttu-id="d4a2a-145">Format de disque</span><span class="sxs-lookup"><span data-stu-id="d4a2a-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="d4a2a-146">1</span><span class="sxs-lookup"><span data-stu-id="d4a2a-146">1</span></span>     | <span data-ttu-id="d4a2a-147">/IFD/GPS/{UShort = 26}</span><span class="sxs-lookup"><span data-stu-id="d4a2a-147">/ifd/gps/{ushort=26}</span></span>          |             |
| <span data-ttu-id="d4a2a-148">2</span><span class="sxs-lookup"><span data-stu-id="d4a2a-148">2</span></span>     | <span data-ttu-id="d4a2a-149">/ifd/xmp/exif:GPSDestDistance</span><span class="sxs-lookup"><span data-stu-id="d4a2a-149">/ifd/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="d4a2a-150">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="d4a2a-150">Write Paths</span></span>



| <span data-ttu-id="d4a2a-151">Commande</span><span class="sxs-lookup"><span data-stu-id="d4a2a-151">Order</span></span> | <span data-ttu-id="d4a2a-152">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="d4a2a-152">Path</span></span>                          | <span data-ttu-id="d4a2a-153">Format de disque</span><span class="sxs-lookup"><span data-stu-id="d4a2a-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="d4a2a-154">1</span><span class="sxs-lookup"><span data-stu-id="d4a2a-154">1</span></span>     | <span data-ttu-id="d4a2a-155">/IFD/GPS/{UShort = 26}</span><span class="sxs-lookup"><span data-stu-id="d4a2a-155">/ifd/gps/{ushort=26}</span></span>          |             |
| <span data-ttu-id="d4a2a-156">2</span><span class="sxs-lookup"><span data-stu-id="d4a2a-156">2</span></span>     | <span data-ttu-id="d4a2a-157">/ifd/xmp/exif:GPSDestDistance</span><span class="sxs-lookup"><span data-stu-id="d4a2a-157">/ifd/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="d4a2a-158">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="d4a2a-158">Remove Paths</span></span>



| <span data-ttu-id="d4a2a-159">Commande</span><span class="sxs-lookup"><span data-stu-id="d4a2a-159">Order</span></span> | <span data-ttu-id="d4a2a-160">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="d4a2a-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="d4a2a-161">1</span><span class="sxs-lookup"><span data-stu-id="d4a2a-161">1</span></span>     | <span data-ttu-id="d4a2a-162">/IFD/GPS/{UShort = 26}</span><span class="sxs-lookup"><span data-stu-id="d4a2a-162">/ifd/gps/{ushort=26}</span></span>          |
| <span data-ttu-id="d4a2a-163">2</span><span class="sxs-lookup"><span data-stu-id="d4a2a-163">2</span></span>     | <span data-ttu-id="d4a2a-164">/ifd/xmp/exif:gpsdestdistance</span><span class="sxs-lookup"><span data-stu-id="d4a2a-164">/ifd/xmp/exif:gpsdestdistance</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d4a2a-165">Notes</span><span class="sxs-lookup"><span data-stu-id="d4a2a-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4a2a-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d4a2a-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4a2a-167">System. GPS. DestDistance</span><span class="sxs-lookup"><span data-stu-id="d4a2a-167">System.GPS.DestDistance</span></span>](../properties/props-system-gps-destdistance.md)
</dt> </dl>

 

 
