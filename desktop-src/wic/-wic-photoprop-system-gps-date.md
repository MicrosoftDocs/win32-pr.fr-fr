---
description: La stratégie de métadonnées de la photo pour la propriété System. GPS. date.
ms.assetid: 75047658-b6f3-454e-961a-89016c244bf6
title: Stratégie de métadonnées de photo System. GPS. date
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c736c79cd76d2d070d727dc024925717b386cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210281"
---
# <a name="systemgpsdate-photo-metadata-policy"></a><span data-ttu-id="ca4ab-103">Stratégie de métadonnées de photo System. GPS. date</span><span class="sxs-lookup"><span data-stu-id="ca4ab-103">System.GPS.Date Photo Metadata Policy</span></span>

<span data-ttu-id="ca4ab-104">La stratégie de métadonnées de la photo pour la propriété [System. GPS. date](../properties/props-system-gps-date.md) .</span><span class="sxs-lookup"><span data-stu-id="ca4ab-104">The photo metadata policy for the [System.GPS.Date](../properties/props-system-gps-date.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="ca4ab-105">A-la</span><span class="sxs-lookup"><span data-stu-id="ca4ab-105">PKEY</span></span>

<span data-ttu-id="ca4ab-106">Date de la \_ balise GPS \_</span><span class="sxs-lookup"><span data-stu-id="ca4ab-106">PKEY\_GPS\_Date</span></span>

### <a name="containers"></a><span data-ttu-id="ca4ab-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="ca4ab-107">Containers</span></span>

<span data-ttu-id="ca4ab-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="ca4ab-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="ca4ab-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ca4ab-109">Read-Only</span></span>

<span data-ttu-id="ca4ab-110">Non</span><span class="sxs-lookup"><span data-stu-id="ca4ab-110">No</span></span>

### <a name="input-type"></a><span data-ttu-id="ca4ab-111">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="ca4ab-111">Input Type</span></span>

<span data-ttu-id="ca4ab-112">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="ca4ab-112">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="ca4ab-113">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="ca4ab-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="ca4ab-114">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="ca4ab-114">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="ca4ab-115">Stratégies JPEG</span><span class="sxs-lookup"><span data-stu-id="ca4ab-115">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="ca4ab-116">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="ca4ab-116">Read Paths</span></span>



| <span data-ttu-id="ca4ab-117">Commande</span><span class="sxs-lookup"><span data-stu-id="ca4ab-117">Order</span></span> | <span data-ttu-id="ca4ab-118">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="ca4ab-118">Path</span></span>                      | <span data-ttu-id="ca4ab-119">Format de disque</span><span class="sxs-lookup"><span data-stu-id="ca4ab-119">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="ca4ab-120">1</span><span class="sxs-lookup"><span data-stu-id="ca4ab-120">1</span></span>     | <span data-ttu-id="ca4ab-121">/App1/IFD/GPS/{UShort = 29}</span><span class="sxs-lookup"><span data-stu-id="ca4ab-121">/app1/ifd/gps/{ushort=29}</span></span> | <span data-ttu-id="ca4ab-122">ascii</span><span class="sxs-lookup"><span data-stu-id="ca4ab-122">ascii</span></span>       |
| <span data-ttu-id="ca4ab-123">2</span><span class="sxs-lookup"><span data-stu-id="ca4ab-123">2</span></span>     | <span data-ttu-id="ca4ab-124">/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="ca4ab-124">/xmp/exif:GPSTimeStamp</span></span>    | <span data-ttu-id="ca4ab-125">unicode</span><span class="sxs-lookup"><span data-stu-id="ca4ab-125">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="ca4ab-126">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="ca4ab-126">Write Paths</span></span>



| <span data-ttu-id="ca4ab-127">Commande</span><span class="sxs-lookup"><span data-stu-id="ca4ab-127">Order</span></span> | <span data-ttu-id="ca4ab-128">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="ca4ab-128">Path</span></span>                      | <span data-ttu-id="ca4ab-129">Format de disque</span><span class="sxs-lookup"><span data-stu-id="ca4ab-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="ca4ab-130">1</span><span class="sxs-lookup"><span data-stu-id="ca4ab-130">1</span></span>     | <span data-ttu-id="ca4ab-131">/App1/IFD/GPS/{UShort = 29}</span><span class="sxs-lookup"><span data-stu-id="ca4ab-131">/app1/ifd/gps/{ushort=29}</span></span> | <span data-ttu-id="ca4ab-132">ascii</span><span class="sxs-lookup"><span data-stu-id="ca4ab-132">ascii</span></span>       |
| <span data-ttu-id="ca4ab-133">2</span><span class="sxs-lookup"><span data-stu-id="ca4ab-133">2</span></span>     | <span data-ttu-id="ca4ab-134">/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="ca4ab-134">/xmp/exif:GPSTimeStamp</span></span>    | <span data-ttu-id="ca4ab-135">unicode</span><span class="sxs-lookup"><span data-stu-id="ca4ab-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="ca4ab-136">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="ca4ab-136">Remove Paths</span></span>



| <span data-ttu-id="ca4ab-137">Commande</span><span class="sxs-lookup"><span data-stu-id="ca4ab-137">Order</span></span> | <span data-ttu-id="ca4ab-138">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="ca4ab-138">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="ca4ab-139">1</span><span class="sxs-lookup"><span data-stu-id="ca4ab-139">1</span></span>     | <span data-ttu-id="ca4ab-140">/App1/IFD/GPS/{UShort = 29}</span><span class="sxs-lookup"><span data-stu-id="ca4ab-140">/app1/ifd/gps/{ushort=29}</span></span> |
| <span data-ttu-id="ca4ab-141">2</span><span class="sxs-lookup"><span data-stu-id="ca4ab-141">2</span></span>     | <span data-ttu-id="ca4ab-142">/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="ca4ab-142">/xmp/exif:GPSTimeStamp</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="ca4ab-143">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="ca4ab-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="ca4ab-144">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="ca4ab-144">Read Paths</span></span>



| <span data-ttu-id="ca4ab-145">Commande</span><span class="sxs-lookup"><span data-stu-id="ca4ab-145">Order</span></span> | <span data-ttu-id="ca4ab-146">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="ca4ab-146">Path</span></span>                       | <span data-ttu-id="ca4ab-147">Format de disque</span><span class="sxs-lookup"><span data-stu-id="ca4ab-147">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="ca4ab-148">1</span><span class="sxs-lookup"><span data-stu-id="ca4ab-148">1</span></span>     | <span data-ttu-id="ca4ab-149">/IFD/GPS/{UShort = 29}</span><span class="sxs-lookup"><span data-stu-id="ca4ab-149">/ifd/gps/{ushort=29}</span></span>       | <span data-ttu-id="ca4ab-150">ascii</span><span class="sxs-lookup"><span data-stu-id="ca4ab-150">ascii</span></span>       |
| <span data-ttu-id="ca4ab-151">2</span><span class="sxs-lookup"><span data-stu-id="ca4ab-151">2</span></span>     | <span data-ttu-id="ca4ab-152">/ifd/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="ca4ab-152">/ifd/xmp/exif:GPSTimeStamp</span></span> | <span data-ttu-id="ca4ab-153">unicode</span><span class="sxs-lookup"><span data-stu-id="ca4ab-153">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="ca4ab-154">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="ca4ab-154">Write Paths</span></span>



| <span data-ttu-id="ca4ab-155">Commande</span><span class="sxs-lookup"><span data-stu-id="ca4ab-155">Order</span></span> | <span data-ttu-id="ca4ab-156">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="ca4ab-156">Path</span></span>                       | <span data-ttu-id="ca4ab-157">Format de disque</span><span class="sxs-lookup"><span data-stu-id="ca4ab-157">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="ca4ab-158">1</span><span class="sxs-lookup"><span data-stu-id="ca4ab-158">1</span></span>     | <span data-ttu-id="ca4ab-159">/IFD/GPS/{UShort = 29}</span><span class="sxs-lookup"><span data-stu-id="ca4ab-159">/ifd/gps/{ushort=29}</span></span>       | <span data-ttu-id="ca4ab-160">ascii</span><span class="sxs-lookup"><span data-stu-id="ca4ab-160">ascii</span></span>       |
| <span data-ttu-id="ca4ab-161">2</span><span class="sxs-lookup"><span data-stu-id="ca4ab-161">2</span></span>     | <span data-ttu-id="ca4ab-162">/ifd/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="ca4ab-162">/ifd/xmp/exif:GPSTimeStamp</span></span> | <span data-ttu-id="ca4ab-163">unicode</span><span class="sxs-lookup"><span data-stu-id="ca4ab-163">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="ca4ab-164">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="ca4ab-164">Remove Paths</span></span>



| <span data-ttu-id="ca4ab-165">Commande</span><span class="sxs-lookup"><span data-stu-id="ca4ab-165">Order</span></span> | <span data-ttu-id="ca4ab-166">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="ca4ab-166">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="ca4ab-167">1</span><span class="sxs-lookup"><span data-stu-id="ca4ab-167">1</span></span>     | <span data-ttu-id="ca4ab-168">/IFD/GPS/{UShort = 29}</span><span class="sxs-lookup"><span data-stu-id="ca4ab-168">/ifd/gps/{ushort=29}</span></span>       |
| <span data-ttu-id="ca4ab-169">2</span><span class="sxs-lookup"><span data-stu-id="ca4ab-169">2</span></span>     | <span data-ttu-id="ca4ab-170">/ifd/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="ca4ab-170">/ifd/xmp/exif:GPSTimeStamp</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ca4ab-171">Notes</span><span class="sxs-lookup"><span data-stu-id="ca4ab-171">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca4ab-172">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ca4ab-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca4ab-173">System. GPS. date</span><span class="sxs-lookup"><span data-stu-id="ca4ab-173">System.GPS.Date</span></span>](../properties/props-system-gps-date.md)
</dt> </dl>

 

 
