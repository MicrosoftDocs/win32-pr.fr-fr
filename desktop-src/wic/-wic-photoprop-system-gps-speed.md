---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. Speed.
ms.assetid: 278826c2-3057-4da2-8c86-0e44471ad7b0
title: Stratégie de métadonnées de photo System. GPS. Speed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26d89f755114a73ab17388a1718d5ad0cbdf5a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521103"
---
# <a name="systemgpsspeed-photo-metadata-policy"></a><span data-ttu-id="8753d-103">Stratégie de métadonnées de photo System. GPS. Speed</span><span class="sxs-lookup"><span data-stu-id="8753d-103">System.GPS.Speed Photo Metadata Policy</span></span>

<span data-ttu-id="8753d-104">Stratégie de métadonnées de la photo pour la propriété [System. GPS. Speed](../properties/props-system-gps-speed.md) .</span><span class="sxs-lookup"><span data-stu-id="8753d-104">The photo metadata policy for the [System.GPS.Speed](../properties/props-system-gps-speed.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="8753d-105">A-la</span><span class="sxs-lookup"><span data-stu-id="8753d-105">PKEY</span></span>

<span data-ttu-id="8753d-106">\_Vitesse GPS \_</span><span class="sxs-lookup"><span data-stu-id="8753d-106">PKEY\_GPS\_Speed</span></span>

### <a name="containers"></a><span data-ttu-id="8753d-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="8753d-107">Containers</span></span>

<span data-ttu-id="8753d-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="8753d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="8753d-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8753d-109">Read-Only</span></span>

<span data-ttu-id="8753d-110">Oui</span><span class="sxs-lookup"><span data-stu-id="8753d-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="8753d-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="8753d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="8753d-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="8753d-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="8753d-113">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="8753d-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="8753d-114">Cette valeur est générée à partir de System. GPS. SpeedNumerator et de System. GPS. SpeedDenominator.</span><span class="sxs-lookup"><span data-stu-id="8753d-114">This value is generated from System.GPS.SpeedNumerator and System.GPS.SpeedDenominator.</span></span> <span data-ttu-id="8753d-115">Il ne peut pas être écrit directement.</span><span class="sxs-lookup"><span data-stu-id="8753d-115">It cannot be written directly.</span></span> <span data-ttu-id="8753d-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="8753d-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="8753d-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="8753d-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="8753d-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="8753d-118">Read Paths</span></span>



| <span data-ttu-id="8753d-119">Commande</span><span class="sxs-lookup"><span data-stu-id="8753d-119">Order</span></span> | <span data-ttu-id="8753d-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="8753d-120">Path</span></span>                      | <span data-ttu-id="8753d-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="8753d-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="8753d-122">1</span><span class="sxs-lookup"><span data-stu-id="8753d-122">1</span></span>     | <span data-ttu-id="8753d-123">/App1/IFD/GPS/{UShort = 13}</span><span class="sxs-lookup"><span data-stu-id="8753d-123">/app1/ifd/gps/{ushort=13}</span></span> |             |
| <span data-ttu-id="8753d-124">2</span><span class="sxs-lookup"><span data-stu-id="8753d-124">2</span></span>     | <span data-ttu-id="8753d-125">/xmp/exif:GPSSpeed</span><span class="sxs-lookup"><span data-stu-id="8753d-125">/xmp/exif:GPSSpeed</span></span>        |             |



 

### <a name="write-paths"></a><span data-ttu-id="8753d-126">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="8753d-126">Write Paths</span></span>



| <span data-ttu-id="8753d-127">Commande</span><span class="sxs-lookup"><span data-stu-id="8753d-127">Order</span></span> | <span data-ttu-id="8753d-128">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="8753d-128">Path</span></span>                      | <span data-ttu-id="8753d-129">Format de disque</span><span class="sxs-lookup"><span data-stu-id="8753d-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="8753d-130">1</span><span class="sxs-lookup"><span data-stu-id="8753d-130">1</span></span>     | <span data-ttu-id="8753d-131">/App1/IFD/GPS/{UShort = 13}</span><span class="sxs-lookup"><span data-stu-id="8753d-131">/app1/ifd/gps/{ushort=13}</span></span> |             |
| <span data-ttu-id="8753d-132">2</span><span class="sxs-lookup"><span data-stu-id="8753d-132">2</span></span>     | <span data-ttu-id="8753d-133">/xmp/exif:GPSSpeed</span><span class="sxs-lookup"><span data-stu-id="8753d-133">/xmp/exif:GPSSpeed</span></span>        |             |



 

### <a name="remove-paths"></a><span data-ttu-id="8753d-134">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="8753d-134">Remove Paths</span></span>



| <span data-ttu-id="8753d-135">Commande</span><span class="sxs-lookup"><span data-stu-id="8753d-135">Order</span></span> | <span data-ttu-id="8753d-136">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="8753d-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="8753d-137">1</span><span class="sxs-lookup"><span data-stu-id="8753d-137">1</span></span>     | <span data-ttu-id="8753d-138">/App1/IFD/GPS/{UShort = 13}</span><span class="sxs-lookup"><span data-stu-id="8753d-138">/app1/ifd/gps/{ushort=13}</span></span> |
| <span data-ttu-id="8753d-139">2</span><span class="sxs-lookup"><span data-stu-id="8753d-139">2</span></span>     | <span data-ttu-id="8753d-140">/xmp/exif:gpsspeed</span><span class="sxs-lookup"><span data-stu-id="8753d-140">/xmp/exif:gpsspeed</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="8753d-141">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="8753d-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="8753d-142">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="8753d-142">Read Paths</span></span>



| <span data-ttu-id="8753d-143">Commande</span><span class="sxs-lookup"><span data-stu-id="8753d-143">Order</span></span> | <span data-ttu-id="8753d-144">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="8753d-144">Path</span></span>                   | <span data-ttu-id="8753d-145">Format de disque</span><span class="sxs-lookup"><span data-stu-id="8753d-145">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="8753d-146">1</span><span class="sxs-lookup"><span data-stu-id="8753d-146">1</span></span>     | <span data-ttu-id="8753d-147">/IFD/GPS/{UShort = 13}</span><span class="sxs-lookup"><span data-stu-id="8753d-147">/ifd/gps/{ushort=13}</span></span>   |             |
| <span data-ttu-id="8753d-148">2</span><span class="sxs-lookup"><span data-stu-id="8753d-148">2</span></span>     | <span data-ttu-id="8753d-149">/ifd/xmp/exif:GPSSpeed</span><span class="sxs-lookup"><span data-stu-id="8753d-149">/ifd/xmp/exif:GPSSpeed</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="8753d-150">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="8753d-150">Write Paths</span></span>



| <span data-ttu-id="8753d-151">Commande</span><span class="sxs-lookup"><span data-stu-id="8753d-151">Order</span></span> | <span data-ttu-id="8753d-152">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="8753d-152">Path</span></span>                   | <span data-ttu-id="8753d-153">Format de disque</span><span class="sxs-lookup"><span data-stu-id="8753d-153">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="8753d-154">1</span><span class="sxs-lookup"><span data-stu-id="8753d-154">1</span></span>     | <span data-ttu-id="8753d-155">/IFD/GPS/{UShort = 13}</span><span class="sxs-lookup"><span data-stu-id="8753d-155">/ifd/gps/{ushort=13}</span></span>   |             |
| <span data-ttu-id="8753d-156">2</span><span class="sxs-lookup"><span data-stu-id="8753d-156">2</span></span>     | <span data-ttu-id="8753d-157">/ifd/xmp/exif:GPSSpeed</span><span class="sxs-lookup"><span data-stu-id="8753d-157">/ifd/xmp/exif:GPSSpeed</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="8753d-158">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="8753d-158">Remove Paths</span></span>



| <span data-ttu-id="8753d-159">Commande</span><span class="sxs-lookup"><span data-stu-id="8753d-159">Order</span></span> | <span data-ttu-id="8753d-160">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="8753d-160">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="8753d-161">1</span><span class="sxs-lookup"><span data-stu-id="8753d-161">1</span></span>     | <span data-ttu-id="8753d-162">/IFD/GPS/{UShort = 13}</span><span class="sxs-lookup"><span data-stu-id="8753d-162">/ifd/gps/{ushort=13}</span></span>   |
| <span data-ttu-id="8753d-163">2</span><span class="sxs-lookup"><span data-stu-id="8753d-163">2</span></span>     | <span data-ttu-id="8753d-164">/ifd/xmp/exif:gpsspeed</span><span class="sxs-lookup"><span data-stu-id="8753d-164">/ifd/xmp/exif:gpsspeed</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8753d-165">Notes</span><span class="sxs-lookup"><span data-stu-id="8753d-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="8753d-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8753d-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8753d-167">System. GPS. Speed</span><span class="sxs-lookup"><span data-stu-id="8753d-167">System.GPS.Speed</span></span>](../properties/props-system-gps-speed.md)
</dt> </dl>

 

 
