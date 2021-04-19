---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. altitude.
ms.assetid: 63d59aa3-52a6-4b6f-b6ec-a1c4abcee83f
title: Stratégie de métadonnées de photo System. GPS. altitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003d39d135c625a01035c023b5d7dc8d890b3b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520747"
---
# <a name="systemgpsaltitude-photo-metadata-policy"></a><span data-ttu-id="6a98e-103">Stratégie de métadonnées de photo System. GPS. altitude</span><span class="sxs-lookup"><span data-stu-id="6a98e-103">System.GPS.Altitude Photo Metadata Policy</span></span>

<span data-ttu-id="6a98e-104">Stratégie de métadonnées de la photo pour la propriété [System. GPS. altitude](../properties/props-system-gps-altitude.md) .</span><span class="sxs-lookup"><span data-stu-id="6a98e-104">The photo metadata policy for the [System.GPS.Altitude](../properties/props-system-gps-altitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="6a98e-105">A-la</span><span class="sxs-lookup"><span data-stu-id="6a98e-105">PKEY</span></span>

<span data-ttu-id="6a98e-106">\_Altitude GPS \_</span><span class="sxs-lookup"><span data-stu-id="6a98e-106">PKEY\_GPS\_Altitude</span></span>

### <a name="description"></a><span data-ttu-id="6a98e-107">Description</span><span class="sxs-lookup"><span data-stu-id="6a98e-107">Description</span></span>

<span data-ttu-id="6a98e-108">L’altitude est indiquée sous la forme d’une valeur absolue référencée en mètres.</span><span class="sxs-lookup"><span data-stu-id="6a98e-108">The altitude is indicated as an absolute value referenced in meters.</span></span>

### <a name="containers"></a><span data-ttu-id="6a98e-109">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="6a98e-109">Containers</span></span>

<span data-ttu-id="6a98e-110">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="6a98e-110">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="6a98e-111">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a98e-111">Read-Only</span></span>

<span data-ttu-id="6a98e-112">Oui</span><span class="sxs-lookup"><span data-stu-id="6a98e-112">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="6a98e-113">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="6a98e-113">Output PROPVARIANT Type</span></span>

<span data-ttu-id="6a98e-114">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="6a98e-114">VT\_R8</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="6a98e-115">Type de PROPVARIANT d’entrée</span><span class="sxs-lookup"><span data-stu-id="6a98e-115">Input PROPVARIANT Type</span></span>

<span data-ttu-id="6a98e-116">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="6a98e-116">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="6a98e-117">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="6a98e-117">Conflict Resolution Policy</span></span>

<span data-ttu-id="6a98e-118">Cette valeur peut être écrite en écrivant dans System. GPS. altitude. numérateur et System. GPS. altitude. dénominateur.</span><span class="sxs-lookup"><span data-stu-id="6a98e-118">This value can be written by writing to System.GPS.Altitude.Numerator and System.GPS.Altitude.Denominator.</span></span> <span data-ttu-id="6a98e-119">Il ne peut pas être écrit directement.</span><span class="sxs-lookup"><span data-stu-id="6a98e-119">It cannot be written directly.</span></span> <span data-ttu-id="6a98e-120">Les chemins d’accès en écriture dans les tableaux suivants indiquent où la valeur peut être enregistrée lors de sa génération, et non lors de son écriture directe.</span><span class="sxs-lookup"><span data-stu-id="6a98e-120">The write paths in the following tables indicate where the value may be saved when it is generated, not when it is written directly.</span></span> <span data-ttu-id="6a98e-121">Lorsque la valeur est lue, les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="6a98e-121">When the value is read, values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="6a98e-122">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="6a98e-122">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="6a98e-123">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="6a98e-123">Read Paths</span></span>



| <span data-ttu-id="6a98e-124">Commande</span><span class="sxs-lookup"><span data-stu-id="6a98e-124">Order</span></span> | <span data-ttu-id="6a98e-125">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="6a98e-125">Path</span></span>                     | <span data-ttu-id="6a98e-126">Format de disque</span><span class="sxs-lookup"><span data-stu-id="6a98e-126">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="6a98e-127">1</span><span class="sxs-lookup"><span data-stu-id="6a98e-127">1</span></span>     | <span data-ttu-id="6a98e-128">/App1/IFD/GPS/{UShort = 6}</span><span class="sxs-lookup"><span data-stu-id="6a98e-128">/app1/ifd/gps/{ushort=6}</span></span> |             |
| <span data-ttu-id="6a98e-129">2</span><span class="sxs-lookup"><span data-stu-id="6a98e-129">2</span></span>     | <span data-ttu-id="6a98e-130">/xmp/exif:GPSAltitude</span><span class="sxs-lookup"><span data-stu-id="6a98e-130">/xmp/exif:GPSAltitude</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="6a98e-131">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="6a98e-131">Write Paths</span></span>



| <span data-ttu-id="6a98e-132">Commande</span><span class="sxs-lookup"><span data-stu-id="6a98e-132">Order</span></span> | <span data-ttu-id="6a98e-133">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="6a98e-133">Path</span></span>                     | <span data-ttu-id="6a98e-134">Format de disque</span><span class="sxs-lookup"><span data-stu-id="6a98e-134">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="6a98e-135">1</span><span class="sxs-lookup"><span data-stu-id="6a98e-135">1</span></span>     | <span data-ttu-id="6a98e-136">/App1/IFD/GPS/{UShort = 6}</span><span class="sxs-lookup"><span data-stu-id="6a98e-136">/app1/ifd/gps/{ushort=6}</span></span> |             |
| <span data-ttu-id="6a98e-137">2</span><span class="sxs-lookup"><span data-stu-id="6a98e-137">2</span></span>     | <span data-ttu-id="6a98e-138">/xmp/exif:GPSAltitude</span><span class="sxs-lookup"><span data-stu-id="6a98e-138">/xmp/exif:GPSAltitude</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="6a98e-139">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="6a98e-139">Remove Paths</span></span>



| <span data-ttu-id="6a98e-140">Commande</span><span class="sxs-lookup"><span data-stu-id="6a98e-140">Order</span></span> | <span data-ttu-id="6a98e-141">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="6a98e-141">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="6a98e-142">1</span><span class="sxs-lookup"><span data-stu-id="6a98e-142">1</span></span>     | <span data-ttu-id="6a98e-143">/App1/IFD/GPS/{UShort = 6}</span><span class="sxs-lookup"><span data-stu-id="6a98e-143">/app1/ifd/gps/{ushort=6}</span></span> |
| <span data-ttu-id="6a98e-144">2</span><span class="sxs-lookup"><span data-stu-id="6a98e-144">2</span></span>     | <span data-ttu-id="6a98e-145">/xmp/exif:gpsaltitude</span><span class="sxs-lookup"><span data-stu-id="6a98e-145">/xmp/exif:gpsaltitude</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="6a98e-146">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="6a98e-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="6a98e-147">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="6a98e-147">Read Paths</span></span>



| <span data-ttu-id="6a98e-148">Commande</span><span class="sxs-lookup"><span data-stu-id="6a98e-148">Order</span></span> | <span data-ttu-id="6a98e-149">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="6a98e-149">Path</span></span>                      | <span data-ttu-id="6a98e-150">Format de disque</span><span class="sxs-lookup"><span data-stu-id="6a98e-150">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="6a98e-151">1</span><span class="sxs-lookup"><span data-stu-id="6a98e-151">1</span></span>     | <span data-ttu-id="6a98e-152">/IFD/GPS/{UShort = 6}</span><span class="sxs-lookup"><span data-stu-id="6a98e-152">/ifd/gps/{ushort=6}</span></span>       |             |
| <span data-ttu-id="6a98e-153">2</span><span class="sxs-lookup"><span data-stu-id="6a98e-153">2</span></span>     | <span data-ttu-id="6a98e-154">/ifd/xmp/exif:GPSAltitude</span><span class="sxs-lookup"><span data-stu-id="6a98e-154">/ifd/xmp/exif:GPSAltitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="6a98e-155">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="6a98e-155">Write Paths</span></span>



| <span data-ttu-id="6a98e-156">Commande</span><span class="sxs-lookup"><span data-stu-id="6a98e-156">Order</span></span> | <span data-ttu-id="6a98e-157">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="6a98e-157">Path</span></span>                      | <span data-ttu-id="6a98e-158">Format de disque</span><span class="sxs-lookup"><span data-stu-id="6a98e-158">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="6a98e-159">1</span><span class="sxs-lookup"><span data-stu-id="6a98e-159">1</span></span>     | <span data-ttu-id="6a98e-160">/IFD/GPS/{UShort = 6}</span><span class="sxs-lookup"><span data-stu-id="6a98e-160">/ifd/gps/{ushort=6}</span></span>       |             |
| <span data-ttu-id="6a98e-161">2</span><span class="sxs-lookup"><span data-stu-id="6a98e-161">2</span></span>     | <span data-ttu-id="6a98e-162">/ifd/xmp/exif:GPSAltitude</span><span class="sxs-lookup"><span data-stu-id="6a98e-162">/ifd/xmp/exif:GPSAltitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="6a98e-163">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="6a98e-163">Remove Paths</span></span>



| <span data-ttu-id="6a98e-164">Commande</span><span class="sxs-lookup"><span data-stu-id="6a98e-164">Order</span></span> | <span data-ttu-id="6a98e-165">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="6a98e-165">Path</span></span>                      |     |
|-------|---------------------------|-----|
| <span data-ttu-id="6a98e-166">1</span><span class="sxs-lookup"><span data-stu-id="6a98e-166">1</span></span>     | <span data-ttu-id="6a98e-167">/IFD/GPS/{UShort = 6}</span><span class="sxs-lookup"><span data-stu-id="6a98e-167">/ifd/gps/{ushort=6}</span></span>       |     |
| <span data-ttu-id="6a98e-168">2</span><span class="sxs-lookup"><span data-stu-id="6a98e-168">2</span></span>     | <span data-ttu-id="6a98e-169">/ifd/xmp/exif:gpsaltitude</span><span class="sxs-lookup"><span data-stu-id="6a98e-169">/ifd/xmp/exif:gpsaltitude</span></span> |     |



 

## <a name="remarks"></a><span data-ttu-id="6a98e-170">Notes</span><span class="sxs-lookup"><span data-stu-id="6a98e-170">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a98e-171">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6a98e-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a98e-172">System. GPS. altitude</span><span class="sxs-lookup"><span data-stu-id="6a98e-172">System.GPS.Altitude</span></span>](../properties/props-system-gps-altitude.md)
</dt> </dl>

 

 
