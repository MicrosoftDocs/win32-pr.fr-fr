---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. SpeedRef.
ms.assetid: 45fea6be-1e63-4244-a93d-d446e315ddd4
title: Stratégie de métadonnées de photo System. GPS. SpeedRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c454a016dd77345c0a85e0ca3df1ae52694bd81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527679"
---
# <a name="systemgpsspeedref-photo-metadata-policy"></a><span data-ttu-id="eb672-103">Stratégie de métadonnées de photo System. GPS. SpeedRef</span><span class="sxs-lookup"><span data-stu-id="eb672-103">System.GPS.SpeedRef Photo Metadata Policy</span></span>

<span data-ttu-id="eb672-104">Stratégie de métadonnées de la photo pour la propriété [System. GPS. SpeedRef](../properties/props-system-gps-speedref.md) .</span><span class="sxs-lookup"><span data-stu-id="eb672-104">The photo metadata policy for the [System.GPS.SpeedRef](../properties/props-system-gps-speedref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="eb672-105">A-la</span><span class="sxs-lookup"><span data-stu-id="eb672-105">PKEY</span></span>

<span data-ttu-id="eb672-106">\_SpeedRef GPS \_</span><span class="sxs-lookup"><span data-stu-id="eb672-106">PKEY\_GPS\_SpeedRef</span></span>

### <a name="containers"></a><span data-ttu-id="eb672-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="eb672-107">Containers</span></span>

<span data-ttu-id="eb672-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="eb672-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="eb672-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb672-109">Read-Only</span></span>

<span data-ttu-id="eb672-110">Non</span><span class="sxs-lookup"><span data-stu-id="eb672-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="eb672-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="eb672-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="eb672-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="eb672-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="eb672-113">Type de PROPVARIANT d’entrée</span><span class="sxs-lookup"><span data-stu-id="eb672-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="eb672-114">VT \_ LPWStr est préféré, mais VT \_ LPSTR est également accepté.</span><span class="sxs-lookup"><span data-stu-id="eb672-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted..</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="eb672-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="eb672-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="eb672-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="eb672-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="eb672-117">Stratégies JPEG</span><span class="sxs-lookup"><span data-stu-id="eb672-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="eb672-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="eb672-118">Read Paths</span></span>



| <span data-ttu-id="eb672-119">Commande</span><span class="sxs-lookup"><span data-stu-id="eb672-119">Order</span></span> | <span data-ttu-id="eb672-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="eb672-120">Path</span></span>                      | <span data-ttu-id="eb672-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="eb672-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="eb672-122">1</span><span class="sxs-lookup"><span data-stu-id="eb672-122">1</span></span>     | <span data-ttu-id="eb672-123">/App1/IFD/GPS/{UShort = 12}</span><span class="sxs-lookup"><span data-stu-id="eb672-123">/app1/ifd/gps/{ushort=12}</span></span> | <span data-ttu-id="eb672-124">ascii</span><span class="sxs-lookup"><span data-stu-id="eb672-124">ascii</span></span>       |
| <span data-ttu-id="eb672-125">2</span><span class="sxs-lookup"><span data-stu-id="eb672-125">2</span></span>     | <span data-ttu-id="eb672-126">/xmp/exif:GPSSpeedRef</span><span class="sxs-lookup"><span data-stu-id="eb672-126">/xmp/exif:GPSSpeedRef</span></span>     | <span data-ttu-id="eb672-127">unicode</span><span class="sxs-lookup"><span data-stu-id="eb672-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="eb672-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="eb672-128">Write Paths</span></span>



| <span data-ttu-id="eb672-129">Commande</span><span class="sxs-lookup"><span data-stu-id="eb672-129">Order</span></span> | <span data-ttu-id="eb672-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="eb672-130">Path</span></span>                      | <span data-ttu-id="eb672-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="eb672-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="eb672-132">1</span><span class="sxs-lookup"><span data-stu-id="eb672-132">1</span></span>     | <span data-ttu-id="eb672-133">/App1/IFD/GPS/{UShort = 12}</span><span class="sxs-lookup"><span data-stu-id="eb672-133">/app1/ifd/gps/{ushort=12}</span></span> | <span data-ttu-id="eb672-134">ascii</span><span class="sxs-lookup"><span data-stu-id="eb672-134">ascii</span></span>       |
| <span data-ttu-id="eb672-135">2</span><span class="sxs-lookup"><span data-stu-id="eb672-135">2</span></span>     | <span data-ttu-id="eb672-136">/xmp/exif:GPSSpeedRef</span><span class="sxs-lookup"><span data-stu-id="eb672-136">/xmp/exif:GPSSpeedRef</span></span>     | <span data-ttu-id="eb672-137">unicode</span><span class="sxs-lookup"><span data-stu-id="eb672-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="eb672-138">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="eb672-138">Remove Paths</span></span>



| <span data-ttu-id="eb672-139">Commande</span><span class="sxs-lookup"><span data-stu-id="eb672-139">Order</span></span> | <span data-ttu-id="eb672-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="eb672-140">Path</span></span>                      | <span data-ttu-id="eb672-141">Format de disque</span><span class="sxs-lookup"><span data-stu-id="eb672-141">Disk format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="eb672-142">1</span><span class="sxs-lookup"><span data-stu-id="eb672-142">1</span></span>     | <span data-ttu-id="eb672-143">/App1/IFD/GPS/{UShort = 12}</span><span class="sxs-lookup"><span data-stu-id="eb672-143">/app1/ifd/gps/{ushort=12}</span></span> |             |
| <span data-ttu-id="eb672-144">2</span><span class="sxs-lookup"><span data-stu-id="eb672-144">2</span></span>     | <span data-ttu-id="eb672-145">/xmp/exif:gpsspeedref</span><span class="sxs-lookup"><span data-stu-id="eb672-145">/xmp/exif:gpsspeedref</span></span>     |             |



 

### <a name="tiff-policies"></a><span data-ttu-id="eb672-146">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="eb672-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="eb672-147">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="eb672-147">Read Paths</span></span>



| <span data-ttu-id="eb672-148">Commande</span><span class="sxs-lookup"><span data-stu-id="eb672-148">Order</span></span> | <span data-ttu-id="eb672-149">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="eb672-149">Path</span></span>                      |         |
|-------|---------------------------|---------|
| <span data-ttu-id="eb672-150">1</span><span class="sxs-lookup"><span data-stu-id="eb672-150">1</span></span>     | <span data-ttu-id="eb672-151">/IFD/GPS/{UShort = 12}</span><span class="sxs-lookup"><span data-stu-id="eb672-151">/ifd/gps/{ushort=12}</span></span>      | <span data-ttu-id="eb672-152">ascii</span><span class="sxs-lookup"><span data-stu-id="eb672-152">ascii</span></span>   |
| <span data-ttu-id="eb672-153">2</span><span class="sxs-lookup"><span data-stu-id="eb672-153">2</span></span>     | <span data-ttu-id="eb672-154">/ifd/xmp/exif:GPSSpeedRef</span><span class="sxs-lookup"><span data-stu-id="eb672-154">/ifd/xmp/exif:GPSSpeedRef</span></span> | <span data-ttu-id="eb672-155">unicode</span><span class="sxs-lookup"><span data-stu-id="eb672-155">unicode</span></span> |



 

### <a name="write-paths"></a><span data-ttu-id="eb672-156">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="eb672-156">Write Paths</span></span>



| <span data-ttu-id="eb672-157">Commande</span><span class="sxs-lookup"><span data-stu-id="eb672-157">Order</span></span> | <span data-ttu-id="eb672-158">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="eb672-158">Path</span></span>                      | <span data-ttu-id="eb672-159">Format de disque</span><span class="sxs-lookup"><span data-stu-id="eb672-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="eb672-160">1</span><span class="sxs-lookup"><span data-stu-id="eb672-160">1</span></span>     | <span data-ttu-id="eb672-161">/IFD/GPS/{UShort = 12}</span><span class="sxs-lookup"><span data-stu-id="eb672-161">/ifd/gps/{ushort=12}</span></span>      | <span data-ttu-id="eb672-162">ascii</span><span class="sxs-lookup"><span data-stu-id="eb672-162">ascii</span></span>       |
| <span data-ttu-id="eb672-163">2</span><span class="sxs-lookup"><span data-stu-id="eb672-163">2</span></span>     | <span data-ttu-id="eb672-164">/ifd/xmp/exif:GPSSpeedRef</span><span class="sxs-lookup"><span data-stu-id="eb672-164">/ifd/xmp/exif:GPSSpeedRef</span></span> | <span data-ttu-id="eb672-165">unicode</span><span class="sxs-lookup"><span data-stu-id="eb672-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="eb672-166">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="eb672-166">Remove Paths</span></span>



| <span data-ttu-id="eb672-167">Commande</span><span class="sxs-lookup"><span data-stu-id="eb672-167">Order</span></span> | <span data-ttu-id="eb672-168">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="eb672-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="eb672-169">1</span><span class="sxs-lookup"><span data-stu-id="eb672-169">1</span></span>     | <span data-ttu-id="eb672-170">/IFD/GPS/{UShort = 12}</span><span class="sxs-lookup"><span data-stu-id="eb672-170">/ifd/gps/{ushort=12}</span></span>      |
| <span data-ttu-id="eb672-171">2</span><span class="sxs-lookup"><span data-stu-id="eb672-171">2</span></span>     | <span data-ttu-id="eb672-172">/ifd/xmp/exif:gpsspeedref</span><span class="sxs-lookup"><span data-stu-id="eb672-172">/ifd/xmp/exif:gpsspeedref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="eb672-173">Notes</span><span class="sxs-lookup"><span data-stu-id="eb672-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb672-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eb672-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb672-175">System. GPS. SpeedRef</span><span class="sxs-lookup"><span data-stu-id="eb672-175">System.GPS.SpeedRef</span></span>](../properties/props-system-gps-speedref.md)
</dt> </dl>

 

 
