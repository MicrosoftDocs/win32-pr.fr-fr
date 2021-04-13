---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. AreaInformation.
ms.assetid: d9ecb00b-1f97-4f53-909f-30231104d398
title: Stratégie de métadonnées de photo System. GPS. AreaInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e14837da9ffa8b688caf1a544e222043988cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319542"
---
# <a name="systemgpsareainformation-photo-metadata-policy"></a><span data-ttu-id="14b57-103">Stratégie de métadonnées de photo System. GPS. AreaInformation</span><span class="sxs-lookup"><span data-stu-id="14b57-103">System.GPS.AreaInformation Photo Metadata Policy</span></span>

<span data-ttu-id="14b57-104">Stratégie de métadonnées de la photo pour la propriété [System. GPS. AreaInformation](../properties/props-system-gps-areainformation.md) .</span><span class="sxs-lookup"><span data-stu-id="14b57-104">The photo metadata policy for the [System.GPS.AreaInformation](../properties/props-system-gps-areainformation.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="14b57-105">A-la</span><span class="sxs-lookup"><span data-stu-id="14b57-105">PKEY</span></span>

<span data-ttu-id="14b57-106">\_AreaInformation GPS \_</span><span class="sxs-lookup"><span data-stu-id="14b57-106">PKEY\_GPS\_AreaInformation</span></span>

### <a name="containers"></a><span data-ttu-id="14b57-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="14b57-107">Containers</span></span>

<span data-ttu-id="14b57-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="14b57-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="14b57-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14b57-109">Read-Only</span></span>

<span data-ttu-id="14b57-110">Non</span><span class="sxs-lookup"><span data-stu-id="14b57-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="14b57-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="14b57-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="14b57-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="14b57-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="14b57-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="14b57-113">Input Type</span></span>

<span data-ttu-id="14b57-114">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="14b57-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="14b57-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="14b57-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="14b57-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="14b57-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="14b57-117">Stratégies JPEG</span><span class="sxs-lookup"><span data-stu-id="14b57-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="14b57-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="14b57-118">Read Paths</span></span>



| <span data-ttu-id="14b57-119">Commande</span><span class="sxs-lookup"><span data-stu-id="14b57-119">Order</span></span> | <span data-ttu-id="14b57-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="14b57-120">Path</span></span>                         | <span data-ttu-id="14b57-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="14b57-121">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="14b57-122">1</span><span class="sxs-lookup"><span data-stu-id="14b57-122">1</span></span>     | <span data-ttu-id="14b57-123">/App1/IFD/GPS/{UShort = 28}</span><span class="sxs-lookup"><span data-stu-id="14b57-123">/app1/ifd/gps/{ushort=28}</span></span>    |             |
| <span data-ttu-id="14b57-124">2</span><span class="sxs-lookup"><span data-stu-id="14b57-124">2</span></span>     | <span data-ttu-id="14b57-125">/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="14b57-125">/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="14b57-126">unicode</span><span class="sxs-lookup"><span data-stu-id="14b57-126">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="14b57-127">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="14b57-127">Write Paths</span></span>



| <span data-ttu-id="14b57-128">Commande</span><span class="sxs-lookup"><span data-stu-id="14b57-128">Order</span></span> | <span data-ttu-id="14b57-129">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="14b57-129">Path</span></span>                         | <span data-ttu-id="14b57-130">Format de disque</span><span class="sxs-lookup"><span data-stu-id="14b57-130">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="14b57-131">1</span><span class="sxs-lookup"><span data-stu-id="14b57-131">1</span></span>     | <span data-ttu-id="14b57-132">/App1/IFD/GPS/{UShort = 28}</span><span class="sxs-lookup"><span data-stu-id="14b57-132">/app1/ifd/gps/{ushort=28}</span></span>    |             |
| <span data-ttu-id="14b57-133">2</span><span class="sxs-lookup"><span data-stu-id="14b57-133">2</span></span>     | <span data-ttu-id="14b57-134">/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="14b57-134">/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="14b57-135">unicode</span><span class="sxs-lookup"><span data-stu-id="14b57-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="14b57-136">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="14b57-136">Remove Paths</span></span>



| <span data-ttu-id="14b57-137">Commande</span><span class="sxs-lookup"><span data-stu-id="14b57-137">Order</span></span> | <span data-ttu-id="14b57-138">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="14b57-138">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="14b57-139">1</span><span class="sxs-lookup"><span data-stu-id="14b57-139">1</span></span>     | <span data-ttu-id="14b57-140">/App1/IFD/GPS/{UShort = 28}</span><span class="sxs-lookup"><span data-stu-id="14b57-140">/app1/ifd/gps/{ushort=28}</span></span>    |
| <span data-ttu-id="14b57-141">2</span><span class="sxs-lookup"><span data-stu-id="14b57-141">2</span></span>     | <span data-ttu-id="14b57-142">/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="14b57-142">/xmp/exif:GPSAreaInformation</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="14b57-143">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="14b57-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="14b57-144">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="14b57-144">Read Paths</span></span>



| <span data-ttu-id="14b57-145">Commande</span><span class="sxs-lookup"><span data-stu-id="14b57-145">Order</span></span> | <span data-ttu-id="14b57-146">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="14b57-146">Path</span></span>                             | <span data-ttu-id="14b57-147">Format de disque</span><span class="sxs-lookup"><span data-stu-id="14b57-147">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="14b57-148">1</span><span class="sxs-lookup"><span data-stu-id="14b57-148">1</span></span>     | <span data-ttu-id="14b57-149">/IFD/GPS/{UShort = 28}</span><span class="sxs-lookup"><span data-stu-id="14b57-149">/ifd/gps/{ushort=28}</span></span>             |             |
| <span data-ttu-id="14b57-150">2</span><span class="sxs-lookup"><span data-stu-id="14b57-150">2</span></span>     | <span data-ttu-id="14b57-151">/ifd/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="14b57-151">/ifd/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="14b57-152">unicode</span><span class="sxs-lookup"><span data-stu-id="14b57-152">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="14b57-153">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="14b57-153">Write Paths</span></span>



| <span data-ttu-id="14b57-154">Commande</span><span class="sxs-lookup"><span data-stu-id="14b57-154">Order</span></span> | <span data-ttu-id="14b57-155">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="14b57-155">Path</span></span>                             | <span data-ttu-id="14b57-156">Format de disque</span><span class="sxs-lookup"><span data-stu-id="14b57-156">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="14b57-157">1</span><span class="sxs-lookup"><span data-stu-id="14b57-157">1</span></span>     | <span data-ttu-id="14b57-158">/IFD/GPS/{UShort = 28}</span><span class="sxs-lookup"><span data-stu-id="14b57-158">/ifd/gps/{ushort=28}</span></span>             |             |
| <span data-ttu-id="14b57-159">2</span><span class="sxs-lookup"><span data-stu-id="14b57-159">2</span></span>     | <span data-ttu-id="14b57-160">/ifd/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="14b57-160">/ifd/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="14b57-161">unicode</span><span class="sxs-lookup"><span data-stu-id="14b57-161">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="14b57-162">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="14b57-162">Remove Paths</span></span>



| <span data-ttu-id="14b57-163">Commande</span><span class="sxs-lookup"><span data-stu-id="14b57-163">Order</span></span> | <span data-ttu-id="14b57-164">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="14b57-164">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="14b57-165">1</span><span class="sxs-lookup"><span data-stu-id="14b57-165">1</span></span>     | <span data-ttu-id="14b57-166">/IFD/GPS/{UShort = 28}</span><span class="sxs-lookup"><span data-stu-id="14b57-166">/ifd/gps/{ushort=28}</span></span>             |
| <span data-ttu-id="14b57-167">2</span><span class="sxs-lookup"><span data-stu-id="14b57-167">2</span></span>     | <span data-ttu-id="14b57-168">/ifd/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="14b57-168">/ifd/xmp/exif:GPSAreaInformation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="14b57-169">Notes</span><span class="sxs-lookup"><span data-stu-id="14b57-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="14b57-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="14b57-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14b57-171">System. GPS. AreaInformation</span><span class="sxs-lookup"><span data-stu-id="14b57-171">System.GPS.AreaInformation</span></span>](../properties/props-system-gps-areainformation.md)
</dt> </dl>

 

 
