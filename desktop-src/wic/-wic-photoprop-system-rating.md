---
description: Stratégie de métadonnées de la photo pour la propriété System. Rating.
ms.assetid: e4d2c12e-617a-431e-9062-62acf6ef21c8
title: Stratégie de métadonnées de photo System. Rating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c4f7d89b1ff1ea8326c2d26fba0d331db1eab1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319846"
---
# <a name="systemrating-photo-metadata-policy"></a><span data-ttu-id="4378c-103">Stratégie de métadonnées de photo System. Rating</span><span class="sxs-lookup"><span data-stu-id="4378c-103">System.Rating Photo Metadata Policy</span></span>

<span data-ttu-id="4378c-104">Stratégie de métadonnées de la photo pour la propriété [System. Rating](../properties/props-system-rating.md) .</span><span class="sxs-lookup"><span data-stu-id="4378c-104">The photo metadata policy for the [System.Rating](../properties/props-system-rating.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="4378c-105">A-la</span><span class="sxs-lookup"><span data-stu-id="4378c-105">PKEY</span></span>

<span data-ttu-id="4378c-106">Notation de la- \_ catégorie</span><span class="sxs-lookup"><span data-stu-id="4378c-106">PKEY\_Rating</span></span>

### <a name="containers"></a><span data-ttu-id="4378c-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="4378c-107">Containers</span></span>

<span data-ttu-id="4378c-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="4378c-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="4378c-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4378c-109">Read-Only</span></span>

<span data-ttu-id="4378c-110">Non</span><span class="sxs-lookup"><span data-stu-id="4378c-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="4378c-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="4378c-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="4378c-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="4378c-112">VT\_UI4</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="4378c-113">Type de PROPVARIANT d’entrée</span><span class="sxs-lookup"><span data-stu-id="4378c-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="4378c-114">Peut être VT \_ UI1, VT \_ UI2 ou VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="4378c-114">May be VT\_UI1, VT\_UI2, or VT\_UI4.</span></span> <span data-ttu-id="4378c-115">La valeur peut être comprise entre 0 et 99.</span><span class="sxs-lookup"><span data-stu-id="4378c-115">The value may range from 0 to 99.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="4378c-116">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="4378c-116">Conflict Resolution Policy</span></span>

<span data-ttu-id="4378c-117">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="4378c-117">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="4378c-118">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="4378c-118">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="4378c-119">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="4378c-119">Read Paths</span></span>



| <span data-ttu-id="4378c-120">Commande</span><span class="sxs-lookup"><span data-stu-id="4378c-120">Order</span></span> | <span data-ttu-id="4378c-121">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="4378c-121">Path</span></span>                       | <span data-ttu-id="4378c-122">Format de disque</span><span class="sxs-lookup"><span data-stu-id="4378c-122">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="4378c-123">1</span><span class="sxs-lookup"><span data-stu-id="4378c-123">1</span></span>     | <span data-ttu-id="4378c-124">/App1/IFD/{UShort = 18249}</span><span class="sxs-lookup"><span data-stu-id="4378c-124">/app1/ifd/{ushort=18249}</span></span>   | <span data-ttu-id="4378c-125">ushort</span><span class="sxs-lookup"><span data-stu-id="4378c-125">ushort</span></span>      |
| <span data-ttu-id="4378c-126">2</span><span class="sxs-lookup"><span data-stu-id="4378c-126">2</span></span>     | <span data-ttu-id="4378c-127">/xmp/MicrosoftPhoto : évaluation</span><span class="sxs-lookup"><span data-stu-id="4378c-127">/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="4378c-128">unicode</span><span class="sxs-lookup"><span data-stu-id="4378c-128">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="4378c-129">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="4378c-129">Write Paths</span></span>



| <span data-ttu-id="4378c-130">Commande</span><span class="sxs-lookup"><span data-stu-id="4378c-130">Order</span></span> | <span data-ttu-id="4378c-131">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="4378c-131">Path</span></span>                       | <span data-ttu-id="4378c-132">Format de disque</span><span class="sxs-lookup"><span data-stu-id="4378c-132">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="4378c-133">1</span><span class="sxs-lookup"><span data-stu-id="4378c-133">1</span></span>     | <span data-ttu-id="4378c-134">/App1/IFD/{UShort = 18249}</span><span class="sxs-lookup"><span data-stu-id="4378c-134">/app1/ifd/{ushort=18249}</span></span>   | <span data-ttu-id="4378c-135">ushort</span><span class="sxs-lookup"><span data-stu-id="4378c-135">ushort</span></span>      |
| <span data-ttu-id="4378c-136">2</span><span class="sxs-lookup"><span data-stu-id="4378c-136">2</span></span>     | <span data-ttu-id="4378c-137">/xmp/MicrosoftPhoto : évaluation</span><span class="sxs-lookup"><span data-stu-id="4378c-137">/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="4378c-138">unicode</span><span class="sxs-lookup"><span data-stu-id="4378c-138">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="4378c-139">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="4378c-139">Remove Paths</span></span>



| <span data-ttu-id="4378c-140">Commande</span><span class="sxs-lookup"><span data-stu-id="4378c-140">Order</span></span> | <span data-ttu-id="4378c-141">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="4378c-141">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="4378c-142">1</span><span class="sxs-lookup"><span data-stu-id="4378c-142">1</span></span>     | <span data-ttu-id="4378c-143">/App1/IFD/{UShort = 18249}</span><span class="sxs-lookup"><span data-stu-id="4378c-143">/app1/ifd/{ushort=18249}</span></span>   |
| <span data-ttu-id="4378c-144">2</span><span class="sxs-lookup"><span data-stu-id="4378c-144">2</span></span>     | <span data-ttu-id="4378c-145">/XMP/microsoftphoto : évaluation</span><span class="sxs-lookup"><span data-stu-id="4378c-145">/xmp/microsoftphoto:rating</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="4378c-146">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="4378c-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="4378c-147">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="4378c-147">Read Paths</span></span>



| <span data-ttu-id="4378c-148">Commande</span><span class="sxs-lookup"><span data-stu-id="4378c-148">Order</span></span> | <span data-ttu-id="4378c-149">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="4378c-149">Path</span></span>                           | <span data-ttu-id="4378c-150">Format de disque</span><span class="sxs-lookup"><span data-stu-id="4378c-150">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="4378c-151">1</span><span class="sxs-lookup"><span data-stu-id="4378c-151">1</span></span>     | <span data-ttu-id="4378c-152">/IFD/{UShort = 18249}</span><span class="sxs-lookup"><span data-stu-id="4378c-152">/ifd/{ushort=18249}</span></span>            | <span data-ttu-id="4378c-153">ushort</span><span class="sxs-lookup"><span data-stu-id="4378c-153">ushort</span></span>      |
| <span data-ttu-id="4378c-154">2</span><span class="sxs-lookup"><span data-stu-id="4378c-154">2</span></span>     | <span data-ttu-id="4378c-155">/ifd/xmp/MicrosoftPhoto : évaluation</span><span class="sxs-lookup"><span data-stu-id="4378c-155">/ifd/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="4378c-156">unicode</span><span class="sxs-lookup"><span data-stu-id="4378c-156">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="4378c-157">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="4378c-157">Write Paths</span></span>



| <span data-ttu-id="4378c-158">Commande</span><span class="sxs-lookup"><span data-stu-id="4378c-158">Order</span></span> | <span data-ttu-id="4378c-159">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="4378c-159">Path</span></span>                           | <span data-ttu-id="4378c-160">Format de disque</span><span class="sxs-lookup"><span data-stu-id="4378c-160">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="4378c-161">1</span><span class="sxs-lookup"><span data-stu-id="4378c-161">1</span></span>     | <span data-ttu-id="4378c-162">/IFD/{UShort = 18249}</span><span class="sxs-lookup"><span data-stu-id="4378c-162">/ifd/{ushort=18249}</span></span>            | <span data-ttu-id="4378c-163">ushort</span><span class="sxs-lookup"><span data-stu-id="4378c-163">ushort</span></span>      |
| <span data-ttu-id="4378c-164">2</span><span class="sxs-lookup"><span data-stu-id="4378c-164">2</span></span>     | <span data-ttu-id="4378c-165">/ifd/xmp/MicrosoftPhoto : évaluation</span><span class="sxs-lookup"><span data-stu-id="4378c-165">/ifd/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="4378c-166">unicode</span><span class="sxs-lookup"><span data-stu-id="4378c-166">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="4378c-167">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="4378c-167">Remove Paths</span></span>



| <span data-ttu-id="4378c-168">Commande</span><span class="sxs-lookup"><span data-stu-id="4378c-168">Order</span></span> | <span data-ttu-id="4378c-169">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="4378c-169">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="4378c-170">1</span><span class="sxs-lookup"><span data-stu-id="4378c-170">1</span></span>     | <span data-ttu-id="4378c-171">/IFD/{UShort = 18249}</span><span class="sxs-lookup"><span data-stu-id="4378c-171">/ifd/{ushort=18249}</span></span>            |
| <span data-ttu-id="4378c-172">2</span><span class="sxs-lookup"><span data-stu-id="4378c-172">2</span></span>     | <span data-ttu-id="4378c-173">/IFD/XMP/microsoftphoto : évaluation</span><span class="sxs-lookup"><span data-stu-id="4378c-173">/ifd/xmp/microsoftphoto:rating</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4378c-174">Notes</span><span class="sxs-lookup"><span data-stu-id="4378c-174">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="4378c-175">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4378c-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4378c-176">System. Rating</span><span class="sxs-lookup"><span data-stu-id="4378c-176">System.Rating</span></span>](../properties/props-system-rating.md)
</dt> </dl>

 

 
