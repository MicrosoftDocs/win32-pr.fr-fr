---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. Differential.
ms.assetid: 330d1f88-5f54-4e29-b57f-eb7112203e04
title: Stratégie de métadonnées de photos System. GPS. Differential
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc3f114683d324a067fe4ce4034e2de5cfc88da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320406"
---
# <a name="systemgpsdifferential-photo-metadata-policy"></a><span data-ttu-id="b272b-103">Stratégie de métadonnées de photos System. GPS. Differential</span><span class="sxs-lookup"><span data-stu-id="b272b-103">System.GPS.Differential Photo Metadata Policy</span></span>

<span data-ttu-id="b272b-104">Stratégie de métadonnées de la photo pour la propriété [System. GPS. Differential](../properties/props-system-gps-differential.md) .</span><span class="sxs-lookup"><span data-stu-id="b272b-104">The photo metadata policy for the [System.GPS.Differential](../properties/props-system-gps-differential.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="b272b-105">A-la</span><span class="sxs-lookup"><span data-stu-id="b272b-105">PKEY</span></span>

<span data-ttu-id="b272b-106">\_Différentielle GPS \_</span><span class="sxs-lookup"><span data-stu-id="b272b-106">PKEY\_GPS\_Differential</span></span>

### <a name="containers"></a><span data-ttu-id="b272b-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="b272b-107">Containers</span></span>

<span data-ttu-id="b272b-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="b272b-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="b272b-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b272b-109">Read-Only</span></span>

<span data-ttu-id="b272b-110">Non</span><span class="sxs-lookup"><span data-stu-id="b272b-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="b272b-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="b272b-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="b272b-112">\_UI2 VT</span><span class="sxs-lookup"><span data-stu-id="b272b-112">VT\_UI2</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="b272b-113">Type de PROPVARIANT d’entrée</span><span class="sxs-lookup"><span data-stu-id="b272b-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="b272b-114">VT \_ UI1, VT \_ UI2 et VT \_ UI4 sont tous acceptés.</span><span class="sxs-lookup"><span data-stu-id="b272b-114">VT\_UI1, VT\_UI2, and VT\_UI4 are all accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="b272b-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="b272b-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="b272b-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="b272b-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="b272b-117">Stratégies JPEG</span><span class="sxs-lookup"><span data-stu-id="b272b-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="b272b-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="b272b-118">Read Paths</span></span>



| <span data-ttu-id="b272b-119">Commande</span><span class="sxs-lookup"><span data-stu-id="b272b-119">Order</span></span> | <span data-ttu-id="b272b-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="b272b-120">Path</span></span>                      | <span data-ttu-id="b272b-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="b272b-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="b272b-122">1</span><span class="sxs-lookup"><span data-stu-id="b272b-122">1</span></span>     | <span data-ttu-id="b272b-123">/App1/IFD/GPS/{UShort = 30}</span><span class="sxs-lookup"><span data-stu-id="b272b-123">/app1/ifd/gps/{ushort=30}</span></span> | <span data-ttu-id="b272b-124">ushort</span><span class="sxs-lookup"><span data-stu-id="b272b-124">ushort</span></span>      |
| <span data-ttu-id="b272b-125">2</span><span class="sxs-lookup"><span data-stu-id="b272b-125">2</span></span>     | <span data-ttu-id="b272b-126">/xmp/exif:GPSDifferential</span><span class="sxs-lookup"><span data-stu-id="b272b-126">/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="b272b-127">unicode</span><span class="sxs-lookup"><span data-stu-id="b272b-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="b272b-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="b272b-128">Write Paths</span></span>



| <span data-ttu-id="b272b-129">Commande</span><span class="sxs-lookup"><span data-stu-id="b272b-129">Order</span></span> | <span data-ttu-id="b272b-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="b272b-130">Path</span></span>                      | <span data-ttu-id="b272b-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="b272b-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="b272b-132">1</span><span class="sxs-lookup"><span data-stu-id="b272b-132">1</span></span>     | <span data-ttu-id="b272b-133">/App1/IFD/GPS/{UShort = 30}</span><span class="sxs-lookup"><span data-stu-id="b272b-133">/app1/ifd/gps/{ushort=30}</span></span> | <span data-ttu-id="b272b-134">ushort</span><span class="sxs-lookup"><span data-stu-id="b272b-134">ushort</span></span>      |
| <span data-ttu-id="b272b-135">2</span><span class="sxs-lookup"><span data-stu-id="b272b-135">2</span></span>     | <span data-ttu-id="b272b-136">/xmp/exif:GPSDifferential</span><span class="sxs-lookup"><span data-stu-id="b272b-136">/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="b272b-137">unicode</span><span class="sxs-lookup"><span data-stu-id="b272b-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="b272b-138">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="b272b-138">Remove Paths</span></span>



| <span data-ttu-id="b272b-139">Commande</span><span class="sxs-lookup"><span data-stu-id="b272b-139">Order</span></span> | <span data-ttu-id="b272b-140">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="b272b-140">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="b272b-141">1</span><span class="sxs-lookup"><span data-stu-id="b272b-141">1</span></span>     | <span data-ttu-id="b272b-142">/App1/IFD/GPS/{UShort = 30}</span><span class="sxs-lookup"><span data-stu-id="b272b-142">/app1/ifd/gps/{ushort=30}</span></span> |
| <span data-ttu-id="b272b-143">2</span><span class="sxs-lookup"><span data-stu-id="b272b-143">2</span></span>     | <span data-ttu-id="b272b-144">/xmp/exif:gpsdifferential</span><span class="sxs-lookup"><span data-stu-id="b272b-144">/xmp/exif:gpsdifferential</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="b272b-145">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="b272b-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="b272b-146">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="b272b-146">Read Paths</span></span>



| <span data-ttu-id="b272b-147">Commande</span><span class="sxs-lookup"><span data-stu-id="b272b-147">Order</span></span> | <span data-ttu-id="b272b-148">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="b272b-148">Path</span></span>                          | <span data-ttu-id="b272b-149">Format de disque</span><span class="sxs-lookup"><span data-stu-id="b272b-149">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="b272b-150">1</span><span class="sxs-lookup"><span data-stu-id="b272b-150">1</span></span>     | <span data-ttu-id="b272b-151">/IFD/GPS/{UShort = 30}</span><span class="sxs-lookup"><span data-stu-id="b272b-151">/ifd/gps/{ushort=30}</span></span>          | <span data-ttu-id="b272b-152">ushort</span><span class="sxs-lookup"><span data-stu-id="b272b-152">ushort</span></span>      |
| <span data-ttu-id="b272b-153">2</span><span class="sxs-lookup"><span data-stu-id="b272b-153">2</span></span>     | <span data-ttu-id="b272b-154">/ifd/xmp/exif:GPSDifferential</span><span class="sxs-lookup"><span data-stu-id="b272b-154">/ifd/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="b272b-155">unicode</span><span class="sxs-lookup"><span data-stu-id="b272b-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="b272b-156">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="b272b-156">Write Paths</span></span>



| <span data-ttu-id="b272b-157">Commande</span><span class="sxs-lookup"><span data-stu-id="b272b-157">Order</span></span> | <span data-ttu-id="b272b-158">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="b272b-158">Path</span></span>                          | <span data-ttu-id="b272b-159">Format de disque</span><span class="sxs-lookup"><span data-stu-id="b272b-159">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="b272b-160">1</span><span class="sxs-lookup"><span data-stu-id="b272b-160">1</span></span>     | <span data-ttu-id="b272b-161">/IFD/GPS/{UShort = 30}</span><span class="sxs-lookup"><span data-stu-id="b272b-161">/ifd/gps/{ushort=30}</span></span>          | <span data-ttu-id="b272b-162">ushort</span><span class="sxs-lookup"><span data-stu-id="b272b-162">ushort</span></span>      |
| <span data-ttu-id="b272b-163">2</span><span class="sxs-lookup"><span data-stu-id="b272b-163">2</span></span>     | <span data-ttu-id="b272b-164">/ifd/xmp/exif:GPSDifferential</span><span class="sxs-lookup"><span data-stu-id="b272b-164">/ifd/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="b272b-165">unicode</span><span class="sxs-lookup"><span data-stu-id="b272b-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="b272b-166">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="b272b-166">Remove Paths</span></span>



| <span data-ttu-id="b272b-167">Commande</span><span class="sxs-lookup"><span data-stu-id="b272b-167">Order</span></span> | <span data-ttu-id="b272b-168">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="b272b-168">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="b272b-169">1</span><span class="sxs-lookup"><span data-stu-id="b272b-169">1</span></span>     | <span data-ttu-id="b272b-170">/IFD/GPS/{UShort = 30}</span><span class="sxs-lookup"><span data-stu-id="b272b-170">/ifd/gps/{ushort=30}</span></span>          |
| <span data-ttu-id="b272b-171">2</span><span class="sxs-lookup"><span data-stu-id="b272b-171">2</span></span>     | <span data-ttu-id="b272b-172">/ifd/xmp/exif:gpsdifferential</span><span class="sxs-lookup"><span data-stu-id="b272b-172">/ifd/xmp/exif:gpsdifferential</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b272b-173">Notes</span><span class="sxs-lookup"><span data-stu-id="b272b-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b272b-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b272b-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b272b-175">System. GPS. Differential</span><span class="sxs-lookup"><span data-stu-id="b272b-175">System.GPS.Differential</span></span>](../properties/props-system-gps-differential.md)
</dt> </dl>

 

 
