---
description: Stratégie de métadonnées de la photo pour la propriété System. SimpleRating.
ms.assetid: d932a251-f238-4582-a1c4-cf4855f26fb3
title: Stratégie de métadonnées de photo System. SimpleRating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b91e41a0684c8e395992683e0a1d4fe43306a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035024"
---
# <a name="systemsimplerating-photo-metadata-policy"></a><span data-ttu-id="c67a5-103">Stratégie de métadonnées de photo System. SimpleRating</span><span class="sxs-lookup"><span data-stu-id="c67a5-103">System.SimpleRating Photo Metadata Policy</span></span>

<span data-ttu-id="c67a5-104">Stratégie de métadonnées de la photo pour la propriété [System. SimpleRating](../properties/props-system-simplerating.md) .</span><span class="sxs-lookup"><span data-stu-id="c67a5-104">The photo metadata policy for the [System.SimpleRating](../properties/props-system-simplerating.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="c67a5-105">A-la</span><span class="sxs-lookup"><span data-stu-id="c67a5-105">PKEY</span></span>

<span data-ttu-id="c67a5-106">SimpleRating de la \_</span><span class="sxs-lookup"><span data-stu-id="c67a5-106">PKEY\_SimpleRating</span></span>

### <a name="containers"></a><span data-ttu-id="c67a5-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="c67a5-107">Containers</span></span>

<span data-ttu-id="c67a5-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c67a5-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="c67a5-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c67a5-109">Read-Only</span></span>

<span data-ttu-id="c67a5-110">Non</span><span class="sxs-lookup"><span data-stu-id="c67a5-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="c67a5-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="c67a5-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="c67a5-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="c67a5-112">VT\_UI4</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="c67a5-113">Type de PROPVARIANT d’entrée</span><span class="sxs-lookup"><span data-stu-id="c67a5-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="c67a5-114">Peut être VT \_ UI1, VT \_ UI2 ou VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="c67a5-114">May be VT\_UI1, VT\_UI2, or VT\_UI4.</span></span> <span data-ttu-id="c67a5-115">La valeur entière peut être comprise entre 0 et 5.</span><span class="sxs-lookup"><span data-stu-id="c67a5-115">The integer value may range from 0 to 5.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="c67a5-116">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="c67a5-116">Conflict Resolution Policy</span></span>

<span data-ttu-id="c67a5-117">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="c67a5-117">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="c67a5-118">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="c67a5-118">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="c67a5-119">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="c67a5-119">Read Paths</span></span>



| <span data-ttu-id="c67a5-120">Commande</span><span class="sxs-lookup"><span data-stu-id="c67a5-120">Order</span></span> | <span data-ttu-id="c67a5-121">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c67a5-121">Path</span></span>                     | <span data-ttu-id="c67a5-122">Format de disque</span><span class="sxs-lookup"><span data-stu-id="c67a5-122">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="c67a5-123">1</span><span class="sxs-lookup"><span data-stu-id="c67a5-123">1</span></span>     | <span data-ttu-id="c67a5-124">/App1/IFD/{UShort = 18246}</span><span class="sxs-lookup"><span data-stu-id="c67a5-124">/app1/ifd/{ushort=18246}</span></span> | <span data-ttu-id="c67a5-125">ushort</span><span class="sxs-lookup"><span data-stu-id="c67a5-125">ushort</span></span>      |
| <span data-ttu-id="c67a5-126">2</span><span class="sxs-lookup"><span data-stu-id="c67a5-126">2</span></span>     | <span data-ttu-id="c67a5-127">/XMP/XMP : évaluation</span><span class="sxs-lookup"><span data-stu-id="c67a5-127">/xmp/xmp:Rating</span></span>          | <span data-ttu-id="c67a5-128">unicode</span><span class="sxs-lookup"><span data-stu-id="c67a5-128">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c67a5-129">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="c67a5-129">Write Paths</span></span>



| <span data-ttu-id="c67a5-130">Commande</span><span class="sxs-lookup"><span data-stu-id="c67a5-130">Order</span></span> | <span data-ttu-id="c67a5-131">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c67a5-131">Path</span></span>                     | <span data-ttu-id="c67a5-132">Format de disque</span><span class="sxs-lookup"><span data-stu-id="c67a5-132">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="c67a5-133">1</span><span class="sxs-lookup"><span data-stu-id="c67a5-133">1</span></span>     | <span data-ttu-id="c67a5-134">/App1/IFD/{UShort = 18246}</span><span class="sxs-lookup"><span data-stu-id="c67a5-134">/app1/ifd/{ushort=18246}</span></span> | <span data-ttu-id="c67a5-135">ushort</span><span class="sxs-lookup"><span data-stu-id="c67a5-135">ushort</span></span>      |
| <span data-ttu-id="c67a5-136">2</span><span class="sxs-lookup"><span data-stu-id="c67a5-136">2</span></span>     | <span data-ttu-id="c67a5-137">/XMP/XMP : évaluation</span><span class="sxs-lookup"><span data-stu-id="c67a5-137">/xmp/xmp:Rating</span></span>          | <span data-ttu-id="c67a5-138">unicode</span><span class="sxs-lookup"><span data-stu-id="c67a5-138">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c67a5-139">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="c67a5-139">Remove Paths</span></span>



| <span data-ttu-id="c67a5-140">Commande</span><span class="sxs-lookup"><span data-stu-id="c67a5-140">Order</span></span> | <span data-ttu-id="c67a5-141">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c67a5-141">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="c67a5-142">1</span><span class="sxs-lookup"><span data-stu-id="c67a5-142">1</span></span>     | <span data-ttu-id="c67a5-143">/App1/IFD/{UShort = 18246}</span><span class="sxs-lookup"><span data-stu-id="c67a5-143">/app1/ifd/{ushort=18246}</span></span> |
| <span data-ttu-id="c67a5-144">2</span><span class="sxs-lookup"><span data-stu-id="c67a5-144">2</span></span>     | <span data-ttu-id="c67a5-145">/XMP/XMP : évaluation</span><span class="sxs-lookup"><span data-stu-id="c67a5-145">/xmp/xmp:rating</span></span>          |



 

### <a name="tiff-policies"></a><span data-ttu-id="c67a5-146">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="c67a5-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="c67a5-147">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="c67a5-147">Read Paths</span></span>



| <span data-ttu-id="c67a5-148">Commande</span><span class="sxs-lookup"><span data-stu-id="c67a5-148">Order</span></span> | <span data-ttu-id="c67a5-149">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c67a5-149">Path</span></span>                | <span data-ttu-id="c67a5-150">Format de disque</span><span class="sxs-lookup"><span data-stu-id="c67a5-150">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="c67a5-151">1</span><span class="sxs-lookup"><span data-stu-id="c67a5-151">1</span></span>     | <span data-ttu-id="c67a5-152">/IFD/{UShort = 18246}</span><span class="sxs-lookup"><span data-stu-id="c67a5-152">/ifd/{ushort=18246}</span></span> | <span data-ttu-id="c67a5-153">ushort</span><span class="sxs-lookup"><span data-stu-id="c67a5-153">ushort</span></span>      |
| <span data-ttu-id="c67a5-154">2</span><span class="sxs-lookup"><span data-stu-id="c67a5-154">2</span></span>     | <span data-ttu-id="c67a5-155">/IFD/XMP/XMP : évaluation</span><span class="sxs-lookup"><span data-stu-id="c67a5-155">/ifd/xmp/xmp:Rating</span></span> | <span data-ttu-id="c67a5-156">unicode</span><span class="sxs-lookup"><span data-stu-id="c67a5-156">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c67a5-157">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="c67a5-157">Write Paths</span></span>



| <span data-ttu-id="c67a5-158">Commande</span><span class="sxs-lookup"><span data-stu-id="c67a5-158">Order</span></span> | <span data-ttu-id="c67a5-159">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c67a5-159">Path</span></span>                | <span data-ttu-id="c67a5-160">Format de disque</span><span class="sxs-lookup"><span data-stu-id="c67a5-160">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="c67a5-161">1</span><span class="sxs-lookup"><span data-stu-id="c67a5-161">1</span></span>     | <span data-ttu-id="c67a5-162">/IFD/{UShort = 18246}</span><span class="sxs-lookup"><span data-stu-id="c67a5-162">/ifd/{ushort=18246}</span></span> | <span data-ttu-id="c67a5-163">ushort</span><span class="sxs-lookup"><span data-stu-id="c67a5-163">ushort</span></span>      |
| <span data-ttu-id="c67a5-164">2</span><span class="sxs-lookup"><span data-stu-id="c67a5-164">2</span></span>     | <span data-ttu-id="c67a5-165">/IFD/XMP/XMP : évaluation</span><span class="sxs-lookup"><span data-stu-id="c67a5-165">/ifd/xmp/xmp:Rating</span></span> | <span data-ttu-id="c67a5-166">unicode</span><span class="sxs-lookup"><span data-stu-id="c67a5-166">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c67a5-167">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="c67a5-167">Remove Paths</span></span>



| <span data-ttu-id="c67a5-168">Commande</span><span class="sxs-lookup"><span data-stu-id="c67a5-168">Order</span></span> | <span data-ttu-id="c67a5-169">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c67a5-169">Path</span></span>                |
|-------|---------------------|
| <span data-ttu-id="c67a5-170">1</span><span class="sxs-lookup"><span data-stu-id="c67a5-170">1</span></span>     | <span data-ttu-id="c67a5-171">/IFD/{UShort = 18246}</span><span class="sxs-lookup"><span data-stu-id="c67a5-171">/ifd/{ushort=18246}</span></span> |
| <span data-ttu-id="c67a5-172">2</span><span class="sxs-lookup"><span data-stu-id="c67a5-172">2</span></span>     | <span data-ttu-id="c67a5-173">/IFD/XMP/XMP : évaluation</span><span class="sxs-lookup"><span data-stu-id="c67a5-173">/ifd/xmp/xmp:rating</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c67a5-174">Notes</span><span class="sxs-lookup"><span data-stu-id="c67a5-174">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="c67a5-175">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c67a5-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c67a5-176">System. SimpleRating</span><span class="sxs-lookup"><span data-stu-id="c67a5-176">System.SimpleRating</span></span>](../properties/props-system-simplerating.md)
</dt> </dl>

 

 
