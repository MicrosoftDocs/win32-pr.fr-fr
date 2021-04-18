---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. VersionID.
ms.assetid: d3c88243-8744-4bb3-ab47-38b5354f6f7e
title: Stratégie de métadonnées de photo System. GPS. VersionID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ca5bd1885f0ac5c3dc14dbb5e859de3f8a26cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536375"
---
# <a name="systemgpsversionid-photo-metadata-policy"></a><span data-ttu-id="e29db-103">Stratégie de métadonnées de photo System. GPS. VersionID</span><span class="sxs-lookup"><span data-stu-id="e29db-103">System.GPS.VersionID Photo Metadata Policy</span></span>

<span data-ttu-id="e29db-104">Stratégie de métadonnées de la photo pour la propriété [System. GPS. VersionId](../properties/props-system-gps-versionid.md) .</span><span class="sxs-lookup"><span data-stu-id="e29db-104">The photo metadata policy for the [System.GPS.VersionID](../properties/props-system-gps-versionid.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="e29db-105">A-la</span><span class="sxs-lookup"><span data-stu-id="e29db-105">PKEY</span></span>

<span data-ttu-id="e29db-106">La \_ \_ VersionId GPS</span><span class="sxs-lookup"><span data-stu-id="e29db-106">PKEY\_GPS\_VersionID</span></span>

### <a name="containers"></a><span data-ttu-id="e29db-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="e29db-107">Containers</span></span>

<span data-ttu-id="e29db-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="e29db-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="e29db-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e29db-109">Read-Only</span></span>

<span data-ttu-id="e29db-110">Non</span><span class="sxs-lookup"><span data-stu-id="e29db-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="e29db-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="e29db-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="e29db-112">\_ \| interface utilisateur VT Vector VT \_</span><span class="sxs-lookup"><span data-stu-id="e29db-112">VT\_VECTOR \| VT\_UI</span></span>

### <a name="input-type"></a><span data-ttu-id="e29db-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="e29db-113">Input Type</span></span>

<span data-ttu-id="e29db-114">Buffer</span><span class="sxs-lookup"><span data-stu-id="e29db-114">Buffer</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="e29db-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="e29db-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="e29db-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="e29db-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="e29db-117">Stratégies JPEG</span><span class="sxs-lookup"><span data-stu-id="e29db-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="e29db-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="e29db-118">Read Paths</span></span>



| <span data-ttu-id="e29db-119">Commande</span><span class="sxs-lookup"><span data-stu-id="e29db-119">Order</span></span> | <span data-ttu-id="e29db-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="e29db-120">Path</span></span>                     | <span data-ttu-id="e29db-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="e29db-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="e29db-122">1</span><span class="sxs-lookup"><span data-stu-id="e29db-122">1</span></span>     | <span data-ttu-id="e29db-123">/App1/IFD/GPS/{UShort = 0}</span><span class="sxs-lookup"><span data-stu-id="e29db-123">/app1/ifd/gps/{ushort=0}</span></span> |             |
| <span data-ttu-id="e29db-124">2</span><span class="sxs-lookup"><span data-stu-id="e29db-124">2</span></span>     | <span data-ttu-id="e29db-125">/xmp/exif:GPSVersionID</span><span class="sxs-lookup"><span data-stu-id="e29db-125">/xmp/exif:GPSVersionID</span></span>   | <span data-ttu-id="e29db-126">unicode</span><span class="sxs-lookup"><span data-stu-id="e29db-126">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="e29db-127">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="e29db-127">Write Paths</span></span>



| <span data-ttu-id="e29db-128">Commande</span><span class="sxs-lookup"><span data-stu-id="e29db-128">Order</span></span> | <span data-ttu-id="e29db-129">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="e29db-129">Path</span></span>                     | <span data-ttu-id="e29db-130">Format de disque</span><span class="sxs-lookup"><span data-stu-id="e29db-130">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="e29db-131">1</span><span class="sxs-lookup"><span data-stu-id="e29db-131">1</span></span>     | <span data-ttu-id="e29db-132">/App1/IFD/GPS/{UShort = 0}</span><span class="sxs-lookup"><span data-stu-id="e29db-132">/app1/ifd/gps/{ushort=0}</span></span> |             |
| <span data-ttu-id="e29db-133">2</span><span class="sxs-lookup"><span data-stu-id="e29db-133">2</span></span>     | <span data-ttu-id="e29db-134">/xmp/exif:GPSVersionID</span><span class="sxs-lookup"><span data-stu-id="e29db-134">/xmp/exif:GPSVersionID</span></span>   | <span data-ttu-id="e29db-135">unicode</span><span class="sxs-lookup"><span data-stu-id="e29db-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="e29db-136">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="e29db-136">Remove Paths</span></span>



| <span data-ttu-id="e29db-137">Commande</span><span class="sxs-lookup"><span data-stu-id="e29db-137">Order</span></span> | <span data-ttu-id="e29db-138">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="e29db-138">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="e29db-139">1</span><span class="sxs-lookup"><span data-stu-id="e29db-139">1</span></span>     | <span data-ttu-id="e29db-140">/App1/IFD/GPS/{UShort = 0}</span><span class="sxs-lookup"><span data-stu-id="e29db-140">/app1/ifd/gps/{ushort=0}</span></span> |
| <span data-ttu-id="e29db-141">2</span><span class="sxs-lookup"><span data-stu-id="e29db-141">2</span></span>     | <span data-ttu-id="e29db-142">/xmp/exif:gpsversionid</span><span class="sxs-lookup"><span data-stu-id="e29db-142">/xmp/exif:gpsversionid</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="e29db-143">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="e29db-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="e29db-144">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="e29db-144">Read Paths</span></span>



| <span data-ttu-id="e29db-145">Commande</span><span class="sxs-lookup"><span data-stu-id="e29db-145">Order</span></span> | <span data-ttu-id="e29db-146">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="e29db-146">Path</span></span>                       | <span data-ttu-id="e29db-147">Format de disque</span><span class="sxs-lookup"><span data-stu-id="e29db-147">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="e29db-148">1</span><span class="sxs-lookup"><span data-stu-id="e29db-148">1</span></span>     | <span data-ttu-id="e29db-149">/IFD/GPS/{UShort = 0}</span><span class="sxs-lookup"><span data-stu-id="e29db-149">/ifd/gps/{ushort=0}</span></span>        |             |
| <span data-ttu-id="e29db-150">2</span><span class="sxs-lookup"><span data-stu-id="e29db-150">2</span></span>     | <span data-ttu-id="e29db-151">/ifd/xmp/exif:GPSVersionID</span><span class="sxs-lookup"><span data-stu-id="e29db-151">/ifd/xmp/exif:GPSVersionID</span></span> | <span data-ttu-id="e29db-152">unicode</span><span class="sxs-lookup"><span data-stu-id="e29db-152">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="e29db-153">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="e29db-153">Write Paths</span></span>



| <span data-ttu-id="e29db-154">Commande</span><span class="sxs-lookup"><span data-stu-id="e29db-154">Order</span></span> | <span data-ttu-id="e29db-155">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="e29db-155">Path</span></span>                       | <span data-ttu-id="e29db-156">Format de disque</span><span class="sxs-lookup"><span data-stu-id="e29db-156">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="e29db-157">1</span><span class="sxs-lookup"><span data-stu-id="e29db-157">1</span></span>     | <span data-ttu-id="e29db-158">/IFD/GPS/{UShort = 0}</span><span class="sxs-lookup"><span data-stu-id="e29db-158">/ifd/gps/{ushort=0}</span></span>        |             |
| <span data-ttu-id="e29db-159">2</span><span class="sxs-lookup"><span data-stu-id="e29db-159">2</span></span>     | <span data-ttu-id="e29db-160">/ifd/xmp/exif:GPSVersionID</span><span class="sxs-lookup"><span data-stu-id="e29db-160">/ifd/xmp/exif:GPSVersionID</span></span> | <span data-ttu-id="e29db-161">unicode</span><span class="sxs-lookup"><span data-stu-id="e29db-161">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="e29db-162">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="e29db-162">Remove Paths</span></span>



| <span data-ttu-id="e29db-163">Commande</span><span class="sxs-lookup"><span data-stu-id="e29db-163">Order</span></span> | <span data-ttu-id="e29db-164">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="e29db-164">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="e29db-165">1</span><span class="sxs-lookup"><span data-stu-id="e29db-165">1</span></span>     | <span data-ttu-id="e29db-166">/IFD/GPS/{UShort = 0}</span><span class="sxs-lookup"><span data-stu-id="e29db-166">/ifd/gps/{ushort=0}</span></span>        |
| <span data-ttu-id="e29db-167">2</span><span class="sxs-lookup"><span data-stu-id="e29db-167">2</span></span>     | <span data-ttu-id="e29db-168">/ifd/xmp/exif:gpsversionid</span><span class="sxs-lookup"><span data-stu-id="e29db-168">/ifd/xmp/exif:gpsversionid</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e29db-169">Notes</span><span class="sxs-lookup"><span data-stu-id="e29db-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="e29db-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e29db-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e29db-171">System. GPS. VersionID</span><span class="sxs-lookup"><span data-stu-id="e29db-171">System.GPS.VersionID</span></span>](../properties/props-system-gps-versionid.md)
</dt> </dl>

 

 
