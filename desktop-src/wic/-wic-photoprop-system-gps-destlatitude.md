---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. DestLatitude.
ms.assetid: 05284291-977d-49b8-ad92-365f68384960
title: Stratégie de métadonnées de photo System. GPS. DestLatitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192db0f8efc868e9457e86d283d9967e4692c95b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536854"
---
# <a name="systemgpsdestlatitude-photo-metadata-policy"></a><span data-ttu-id="724a8-103">Stratégie de métadonnées de photo System. GPS. DestLatitude</span><span class="sxs-lookup"><span data-stu-id="724a8-103">System.GPS.DestLatitude Photo Metadata Policy</span></span>

<span data-ttu-id="724a8-104">Stratégie de métadonnées de la photo pour la propriété [System. GPS. DestLatitude](../properties/props-system-gps-destlatitude.md) .</span><span class="sxs-lookup"><span data-stu-id="724a8-104">The photo metadata policy for the [System.GPS.DestLatitude](../properties/props-system-gps-destlatitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="724a8-105">A-la</span><span class="sxs-lookup"><span data-stu-id="724a8-105">PKEY</span></span>

<span data-ttu-id="724a8-106">\_DestLatitude GPS \_</span><span class="sxs-lookup"><span data-stu-id="724a8-106">PKEY\_GPS\_DestLatitude</span></span>

### <a name="containers"></a><span data-ttu-id="724a8-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="724a8-107">Containers</span></span>

<span data-ttu-id="724a8-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="724a8-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="724a8-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="724a8-109">Read-Only</span></span>

<span data-ttu-id="724a8-110">Oui</span><span class="sxs-lookup"><span data-stu-id="724a8-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="724a8-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="724a8-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="724a8-112">VT \_ Vector \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="724a8-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="724a8-113">Type de PROPVARIANT d’entrée</span><span class="sxs-lookup"><span data-stu-id="724a8-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="724a8-114">VT \_ Vector \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="724a8-114">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="724a8-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="724a8-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="724a8-116">Cette valeur est générée à partir de System. GPS. DestLatitudeNumerator et de System. GPS. DestLatitudeDenominator.</span><span class="sxs-lookup"><span data-stu-id="724a8-116">This value is generated from System.GPS.DestLatitudeNumerator and System.GPS.DestLatitudeDenominator.</span></span> <span data-ttu-id="724a8-117">Il ne peut pas être écrit directement.</span><span class="sxs-lookup"><span data-stu-id="724a8-117">It cannot be written directly.</span></span> <span data-ttu-id="724a8-118">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="724a8-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="724a8-119">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="724a8-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="724a8-120">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="724a8-120">Read Paths</span></span>



| <span data-ttu-id="724a8-121">Commande</span><span class="sxs-lookup"><span data-stu-id="724a8-121">Order</span></span> | <span data-ttu-id="724a8-122">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="724a8-122">Path</span></span>                      | <span data-ttu-id="724a8-123">Format de disque</span><span class="sxs-lookup"><span data-stu-id="724a8-123">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="724a8-124">1</span><span class="sxs-lookup"><span data-stu-id="724a8-124">1</span></span>     | <span data-ttu-id="724a8-125">/App1/IFD/GPS/{UShort = 20}</span><span class="sxs-lookup"><span data-stu-id="724a8-125">/app1/ifd/gps/{ushort=20}</span></span> |             |
| <span data-ttu-id="724a8-126">2</span><span class="sxs-lookup"><span data-stu-id="724a8-126">2</span></span>     | <span data-ttu-id="724a8-127">/xmp/exif:GPSDestLatitude</span><span class="sxs-lookup"><span data-stu-id="724a8-127">/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="724a8-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="724a8-128">Write Paths</span></span>



| <span data-ttu-id="724a8-129">Commande</span><span class="sxs-lookup"><span data-stu-id="724a8-129">Order</span></span> | <span data-ttu-id="724a8-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="724a8-130">Path</span></span>                      | <span data-ttu-id="724a8-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="724a8-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="724a8-132">1</span><span class="sxs-lookup"><span data-stu-id="724a8-132">1</span></span>     | <span data-ttu-id="724a8-133">/App1/IFD/GPS/{UShort = 20}</span><span class="sxs-lookup"><span data-stu-id="724a8-133">/app1/ifd/gps/{ushort=20}</span></span> |             |
| <span data-ttu-id="724a8-134">2</span><span class="sxs-lookup"><span data-stu-id="724a8-134">2</span></span>     | <span data-ttu-id="724a8-135">/xmp/exif:GPSDestLatitude</span><span class="sxs-lookup"><span data-stu-id="724a8-135">/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="724a8-136">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="724a8-136">Remove Paths</span></span>



| <span data-ttu-id="724a8-137">Commande</span><span class="sxs-lookup"><span data-stu-id="724a8-137">Order</span></span> | <span data-ttu-id="724a8-138">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="724a8-138">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="724a8-139">1</span><span class="sxs-lookup"><span data-stu-id="724a8-139">1</span></span>     | <span data-ttu-id="724a8-140">/App1/IFD/GPS/{UShort = 20}</span><span class="sxs-lookup"><span data-stu-id="724a8-140">/app1/ifd/gps/{ushort=20}</span></span> |
| <span data-ttu-id="724a8-141">2</span><span class="sxs-lookup"><span data-stu-id="724a8-141">2</span></span>     | <span data-ttu-id="724a8-142">/xmp/exif:gpsdestlatitude</span><span class="sxs-lookup"><span data-stu-id="724a8-142">/xmp/exif:gpsdestlatitude</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="724a8-143">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="724a8-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="724a8-144">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="724a8-144">Read Paths</span></span>



| <span data-ttu-id="724a8-145">Commande</span><span class="sxs-lookup"><span data-stu-id="724a8-145">Order</span></span> | <span data-ttu-id="724a8-146">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="724a8-146">Path</span></span>                          | <span data-ttu-id="724a8-147">Format de disque</span><span class="sxs-lookup"><span data-stu-id="724a8-147">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="724a8-148">1</span><span class="sxs-lookup"><span data-stu-id="724a8-148">1</span></span>     | <span data-ttu-id="724a8-149">/IFD/GPS/{UShort = 20}</span><span class="sxs-lookup"><span data-stu-id="724a8-149">/ifd/gps/{ushort=20}</span></span>          |             |
| <span data-ttu-id="724a8-150">2</span><span class="sxs-lookup"><span data-stu-id="724a8-150">2</span></span>     | <span data-ttu-id="724a8-151">/ifd/xmp/exif:GPSDestLatitude</span><span class="sxs-lookup"><span data-stu-id="724a8-151">/ifd/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="724a8-152">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="724a8-152">Write Paths</span></span>



| <span data-ttu-id="724a8-153">Commande</span><span class="sxs-lookup"><span data-stu-id="724a8-153">Order</span></span> | <span data-ttu-id="724a8-154">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="724a8-154">Path</span></span>                          | <span data-ttu-id="724a8-155">Format de disque</span><span class="sxs-lookup"><span data-stu-id="724a8-155">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="724a8-156">1</span><span class="sxs-lookup"><span data-stu-id="724a8-156">1</span></span>     | <span data-ttu-id="724a8-157">/IFD/GPS/{UShort = 20}</span><span class="sxs-lookup"><span data-stu-id="724a8-157">/ifd/gps/{ushort=20}</span></span>          |             |
| <span data-ttu-id="724a8-158">2</span><span class="sxs-lookup"><span data-stu-id="724a8-158">2</span></span>     | <span data-ttu-id="724a8-159">/ifd/xmp/exif:GPSDestLatitude</span><span class="sxs-lookup"><span data-stu-id="724a8-159">/ifd/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="724a8-160">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="724a8-160">Remove Paths</span></span>



| <span data-ttu-id="724a8-161">Commande</span><span class="sxs-lookup"><span data-stu-id="724a8-161">Order</span></span> | <span data-ttu-id="724a8-162">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="724a8-162">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="724a8-163">1</span><span class="sxs-lookup"><span data-stu-id="724a8-163">1</span></span>     | <span data-ttu-id="724a8-164">/IFD/GPS/{UShort = 20}</span><span class="sxs-lookup"><span data-stu-id="724a8-164">/ifd/gps/{ushort=20}</span></span>          |
| <span data-ttu-id="724a8-165">2</span><span class="sxs-lookup"><span data-stu-id="724a8-165">2</span></span>     | <span data-ttu-id="724a8-166">/ifd/xmp/exif:gpsdestlatitude</span><span class="sxs-lookup"><span data-stu-id="724a8-166">/ifd/xmp/exif:gpsdestlatitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="724a8-167">Notes</span><span class="sxs-lookup"><span data-stu-id="724a8-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="724a8-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="724a8-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="724a8-169">System. GPS. DestLatitude</span><span class="sxs-lookup"><span data-stu-id="724a8-169">System.GPS.DestLatitude</span></span>](../properties/props-system-gps-destlatitude.md)
</dt> </dl>

 

 
