---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. TranscodedForSync.
ms.assetid: 1869d845-6264-425a-ab3e-e0a9f942961a
title: Stratégie de métadonnées de photo System. photo. TranscodedForSync
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5884ad469fcf7b5dffc8c4ad14f0ee5ff90cd07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867326"
---
# <a name="systemphototranscodedforsync-photo-metadata-policy"></a><span data-ttu-id="b9bc0-103">Stratégie de métadonnées de photo System. photo. TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="b9bc0-103">System.Photo.TranscodedForSync Photo Metadata Policy</span></span>

<span data-ttu-id="b9bc0-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. TranscodedForSync](../properties/props-system-photo-transcodedforsync.md) .</span><span class="sxs-lookup"><span data-stu-id="b9bc0-104">The photo metadata policy for the [System.Photo.TranscodedForSync](../properties/props-system-photo-transcodedforsync.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="b9bc0-105">A-la</span><span class="sxs-lookup"><span data-stu-id="b9bc0-105">PKEY</span></span>

<span data-ttu-id="b9bc0-106">\_Photo \_ TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="b9bc0-106">PKEY\_Photo\_TranscodedForSync</span></span>

### <a name="containers"></a><span data-ttu-id="b9bc0-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="b9bc0-107">Containers</span></span>

<span data-ttu-id="b9bc0-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="b9bc0-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="b9bc0-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b9bc0-109">Read-Only</span></span>

<span data-ttu-id="b9bc0-110">Non</span><span class="sxs-lookup"><span data-stu-id="b9bc0-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="b9bc0-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="b9bc0-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="b9bc0-112">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="b9bc0-112">VT\_BOOL</span></span>

### <a name="input-type"></a><span data-ttu-id="b9bc0-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="b9bc0-113">Input Type</span></span>

<span data-ttu-id="b9bc0-114">Propriété booléenne.</span><span class="sxs-lookup"><span data-stu-id="b9bc0-114">Boolean.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="b9bc0-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="b9bc0-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="b9bc0-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="b9bc0-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="b9bc0-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="b9bc0-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="b9bc0-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="b9bc0-118">Read Paths</span></span>



| <span data-ttu-id="b9bc0-119">Commande</span><span class="sxs-lookup"><span data-stu-id="b9bc0-119">Order</span></span> | <span data-ttu-id="b9bc0-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="b9bc0-120">Path</span></span>                                  | <span data-ttu-id="b9bc0-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="b9bc0-121">Disk Format</span></span>  |
|-------|---------------------------------------|--------------|
| <span data-ttu-id="b9bc0-122">1</span><span class="sxs-lookup"><span data-stu-id="b9bc0-122">1</span></span>     | <span data-ttu-id="b9bc0-123">/App1/IFD/{UShort = 18248}</span><span class="sxs-lookup"><span data-stu-id="b9bc0-123">/app1/ifd/{ushort=18248}</span></span>              | <span data-ttu-id="b9bc0-124">bool \_ UShort</span><span class="sxs-lookup"><span data-stu-id="b9bc0-124">bool\_ushort</span></span> |
| <span data-ttu-id="b9bc0-125">2</span><span class="sxs-lookup"><span data-stu-id="b9bc0-125">2</span></span>     | <span data-ttu-id="b9bc0-126">/xmp/MicrosoftPhoto:TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="b9bc0-126">/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="write-paths"></a><span data-ttu-id="b9bc0-127">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="b9bc0-127">Write Paths</span></span>



| <span data-ttu-id="b9bc0-128">Commande</span><span class="sxs-lookup"><span data-stu-id="b9bc0-128">Order</span></span> | <span data-ttu-id="b9bc0-129">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="b9bc0-129">Path</span></span>                                  | <span data-ttu-id="b9bc0-130">Format de disque</span><span class="sxs-lookup"><span data-stu-id="b9bc0-130">Disk Format</span></span>  |
|-------|---------------------------------------|--------------|
| <span data-ttu-id="b9bc0-131">1</span><span class="sxs-lookup"><span data-stu-id="b9bc0-131">1</span></span>     | <span data-ttu-id="b9bc0-132">/App1/IFD/{UShort = 18248}</span><span class="sxs-lookup"><span data-stu-id="b9bc0-132">/app1/ifd/{ushort=18248}</span></span>              | <span data-ttu-id="b9bc0-133">bool \_ UShort</span><span class="sxs-lookup"><span data-stu-id="b9bc0-133">bool\_ushort</span></span> |
| <span data-ttu-id="b9bc0-134">2</span><span class="sxs-lookup"><span data-stu-id="b9bc0-134">2</span></span>     | <span data-ttu-id="b9bc0-135">/xmp/MicrosoftPhoto:TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="b9bc0-135">/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="remove-paths"></a><span data-ttu-id="b9bc0-136">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="b9bc0-136">Remove Paths</span></span>



| <span data-ttu-id="b9bc0-137">Commande</span><span class="sxs-lookup"><span data-stu-id="b9bc0-137">Order</span></span> | <span data-ttu-id="b9bc0-138">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="b9bc0-138">Path</span></span>                                  |
|-------|---------------------------------------|
| <span data-ttu-id="b9bc0-139">1</span><span class="sxs-lookup"><span data-stu-id="b9bc0-139">1</span></span>     | <span data-ttu-id="b9bc0-140">/App1/IFD/{UShort = 18248}</span><span class="sxs-lookup"><span data-stu-id="b9bc0-140">/app1/ifd/{ushort=18248}</span></span>              |
| <span data-ttu-id="b9bc0-141">2</span><span class="sxs-lookup"><span data-stu-id="b9bc0-141">2</span></span>     | <span data-ttu-id="b9bc0-142">/xmp/microsoftphoto:transcodedforsync</span><span class="sxs-lookup"><span data-stu-id="b9bc0-142">/xmp/microsoftphoto:transcodedforsync</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="b9bc0-143">Stratégies TIFF</span><span class="sxs-lookup"><span data-stu-id="b9bc0-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="b9bc0-144">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="b9bc0-144">Read Paths</span></span>



| <span data-ttu-id="b9bc0-145">Commande</span><span class="sxs-lookup"><span data-stu-id="b9bc0-145">Order</span></span> | <span data-ttu-id="b9bc0-146">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="b9bc0-146">Path</span></span>                                      | <span data-ttu-id="b9bc0-147">Format de disque</span><span class="sxs-lookup"><span data-stu-id="b9bc0-147">Disk Format</span></span>  |
|-------|-------------------------------------------|--------------|
| <span data-ttu-id="b9bc0-148">1</span><span class="sxs-lookup"><span data-stu-id="b9bc0-148">1</span></span>     | <span data-ttu-id="b9bc0-149">/IFD/{UShort = 18248}</span><span class="sxs-lookup"><span data-stu-id="b9bc0-149">/ifd/{ushort=18248}</span></span>                       | <span data-ttu-id="b9bc0-150">bool \_ UShort</span><span class="sxs-lookup"><span data-stu-id="b9bc0-150">bool\_ushort</span></span> |
| <span data-ttu-id="b9bc0-151">2</span><span class="sxs-lookup"><span data-stu-id="b9bc0-151">2</span></span>     | <span data-ttu-id="b9bc0-152">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="b9bc0-152">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="write-paths"></a><span data-ttu-id="b9bc0-153">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="b9bc0-153">Write Paths</span></span>



| <span data-ttu-id="b9bc0-154">Commande</span><span class="sxs-lookup"><span data-stu-id="b9bc0-154">Order</span></span> | <span data-ttu-id="b9bc0-155">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="b9bc0-155">Path</span></span>                                      | <span data-ttu-id="b9bc0-156">Format de disque</span><span class="sxs-lookup"><span data-stu-id="b9bc0-156">Disk Format</span></span>  |
|-------|-------------------------------------------|--------------|
| <span data-ttu-id="b9bc0-157">1</span><span class="sxs-lookup"><span data-stu-id="b9bc0-157">1</span></span>     | <span data-ttu-id="b9bc0-158">/IFD/{UShort = 18248}</span><span class="sxs-lookup"><span data-stu-id="b9bc0-158">/ifd/{ushort=18248}</span></span>                       | <span data-ttu-id="b9bc0-159">bool \_ UShort</span><span class="sxs-lookup"><span data-stu-id="b9bc0-159">bool\_ushort</span></span> |
| <span data-ttu-id="b9bc0-160">2</span><span class="sxs-lookup"><span data-stu-id="b9bc0-160">2</span></span>     | <span data-ttu-id="b9bc0-161">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="b9bc0-161">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="remove-paths"></a><span data-ttu-id="b9bc0-162">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="b9bc0-162">Remove Paths</span></span>



| <span data-ttu-id="b9bc0-163">Commande</span><span class="sxs-lookup"><span data-stu-id="b9bc0-163">Order</span></span> | <span data-ttu-id="b9bc0-164">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="b9bc0-164">Path</span></span>                                      |
|-------|-------------------------------------------|
| <span data-ttu-id="b9bc0-165">1</span><span class="sxs-lookup"><span data-stu-id="b9bc0-165">1</span></span>     | <span data-ttu-id="b9bc0-166">/IFD/{UShort = 18248}</span><span class="sxs-lookup"><span data-stu-id="b9bc0-166">/ifd/{ushort=18248}</span></span>                       |
| <span data-ttu-id="b9bc0-167">2</span><span class="sxs-lookup"><span data-stu-id="b9bc0-167">2</span></span>     | <span data-ttu-id="b9bc0-168">/ifd/xmp/microsoftphoto:transcodedforsync</span><span class="sxs-lookup"><span data-stu-id="b9bc0-168">/ifd/xmp/microsoftphoto:transcodedforsync</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b9bc0-169">Notes</span><span class="sxs-lookup"><span data-stu-id="b9bc0-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9bc0-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b9bc0-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9bc0-171">System. photo. TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="b9bc0-171">System.Photo.TranscodedForSync</span></span>](../properties/props-system-photo-transcodedforsync.md)
</dt> </dl>

 

 
