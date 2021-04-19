---
description: Stratégie de métadonnées de la photo pour la propriété System. Subject.
ms.assetid: 5ab7c74b-8a5e-4329-8a49-291470d406cc
title: Stratégie de métadonnées de photo System. Subject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceabbab95a52a1155db949dbc60b4525dd5f9d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534676"
---
# <a name="systemsubject-photo-metadata-policy"></a><span data-ttu-id="4fbf2-103">Stratégie de métadonnées de photo System. Subject</span><span class="sxs-lookup"><span data-stu-id="4fbf2-103">System.Subject Photo Metadata Policy</span></span>

<span data-ttu-id="4fbf2-104">Stratégie de métadonnées de la photo pour la propriété [System. Subject](../properties/props-system-subject.md) .</span><span class="sxs-lookup"><span data-stu-id="4fbf2-104">The photo metadata policy for the [System.Subject](../properties/props-system-subject.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="4fbf2-105">A-la</span><span class="sxs-lookup"><span data-stu-id="4fbf2-105">PKEY</span></span>

<span data-ttu-id="4fbf2-106">Sujet de la \_ rubrique</span><span class="sxs-lookup"><span data-stu-id="4fbf2-106">PKEY\_Subject</span></span>

### <a name="containers"></a><span data-ttu-id="4fbf2-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="4fbf2-107">Containers</span></span>

<span data-ttu-id="4fbf2-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="4fbf2-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="4fbf2-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4fbf2-109">Read-Only</span></span>

<span data-ttu-id="4fbf2-110">Non</span><span class="sxs-lookup"><span data-stu-id="4fbf2-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="4fbf2-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="4fbf2-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="4fbf2-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="4fbf2-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="4fbf2-113">Type de PROPVARIANT d’entrée</span><span class="sxs-lookup"><span data-stu-id="4fbf2-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="4fbf2-114">VT \_ LPWStr ou VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="4fbf2-114">Either VT\_LPWSTR or VT\_LPWSTR</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="4fbf2-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="4fbf2-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="4fbf2-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="4fbf2-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="4fbf2-117">Stratégie JPEG</span><span class="sxs-lookup"><span data-stu-id="4fbf2-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="4fbf2-118">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="4fbf2-118">Read Paths</span></span>



| <span data-ttu-id="4fbf2-119">Commande</span><span class="sxs-lookup"><span data-stu-id="4fbf2-119">Order</span></span> | <span data-ttu-id="4fbf2-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="4fbf2-120">Path</span></span>                     | <span data-ttu-id="4fbf2-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="4fbf2-121">Disk Format</span></span>    |
|-------|--------------------------|----------------|
| <span data-ttu-id="4fbf2-122">1</span><span class="sxs-lookup"><span data-stu-id="4fbf2-122">1</span></span>     | <span data-ttu-id="4fbf2-123">/App1/IFD/{UShort = 40095}</span><span class="sxs-lookup"><span data-stu-id="4fbf2-123">/app1/ifd/{ushort=40095}</span></span> | <span data-ttu-id="4fbf2-124">\_octets Unicode</span><span class="sxs-lookup"><span data-stu-id="4fbf2-124">unicode\_bytes</span></span> |
| <span data-ttu-id="4fbf2-125">2</span><span class="sxs-lookup"><span data-stu-id="4fbf2-125">2</span></span>     | <span data-ttu-id="4fbf2-126">/App1/IFD/{UShort = 270}</span><span class="sxs-lookup"><span data-stu-id="4fbf2-126">/app1/ifd/{ushort=270}</span></span>   | <span data-ttu-id="4fbf2-127">ascii</span><span class="sxs-lookup"><span data-stu-id="4fbf2-127">ascii</span></span>          |



 

### <a name="write-paths"></a><span data-ttu-id="4fbf2-128">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="4fbf2-128">Write Paths</span></span>



| <span data-ttu-id="4fbf2-129">Commande</span><span class="sxs-lookup"><span data-stu-id="4fbf2-129">Order</span></span> | <span data-ttu-id="4fbf2-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="4fbf2-130">Path</span></span>                     | <span data-ttu-id="4fbf2-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="4fbf2-131">Disk Format</span></span>    |
|-------|--------------------------|----------------|
| <span data-ttu-id="4fbf2-132">1</span><span class="sxs-lookup"><span data-stu-id="4fbf2-132">1</span></span>     | <span data-ttu-id="4fbf2-133">/App1/IFD/{UShort = 40095}</span><span class="sxs-lookup"><span data-stu-id="4fbf2-133">/app1/ifd/{ushort=40095}</span></span> | <span data-ttu-id="4fbf2-134">\_octets Unicode</span><span class="sxs-lookup"><span data-stu-id="4fbf2-134">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="4fbf2-135">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="4fbf2-135">Remove Paths</span></span>



| <span data-ttu-id="4fbf2-136">Commande</span><span class="sxs-lookup"><span data-stu-id="4fbf2-136">Order</span></span> | <span data-ttu-id="4fbf2-137">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="4fbf2-137">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="4fbf2-138">1</span><span class="sxs-lookup"><span data-stu-id="4fbf2-138">1</span></span>     | <span data-ttu-id="4fbf2-139">/App1/IFD/{UShort = 40095}</span><span class="sxs-lookup"><span data-stu-id="4fbf2-139">/app1/ifd/{ushort=40095}</span></span> |
| <span data-ttu-id="4fbf2-140">2</span><span class="sxs-lookup"><span data-stu-id="4fbf2-140">2</span></span>     | <span data-ttu-id="4fbf2-141">/App1/IFD/{UShort = 270}</span><span class="sxs-lookup"><span data-stu-id="4fbf2-141">/app1/ifd/{ushort=270}</span></span>   |



 

### <a name="tiff-policy"></a><span data-ttu-id="4fbf2-142">Stratégie TIFF</span><span class="sxs-lookup"><span data-stu-id="4fbf2-142">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="4fbf2-143">Lire les chemins</span><span class="sxs-lookup"><span data-stu-id="4fbf2-143">Read Paths</span></span>



| <span data-ttu-id="4fbf2-144">Commande</span><span class="sxs-lookup"><span data-stu-id="4fbf2-144">Order</span></span> | <span data-ttu-id="4fbf2-145">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="4fbf2-145">Path</span></span>                | <span data-ttu-id="4fbf2-146">Format de disque</span><span class="sxs-lookup"><span data-stu-id="4fbf2-146">Disk Format</span></span>    |
|-------|---------------------|----------------|
| <span data-ttu-id="4fbf2-147">1</span><span class="sxs-lookup"><span data-stu-id="4fbf2-147">1</span></span>     | <span data-ttu-id="4fbf2-148">/IFD/{UShort = 40095}</span><span class="sxs-lookup"><span data-stu-id="4fbf2-148">/ifd/{ushort=40095}</span></span> | <span data-ttu-id="4fbf2-149">\_octets Unicode</span><span class="sxs-lookup"><span data-stu-id="4fbf2-149">unicode\_bytes</span></span> |
| <span data-ttu-id="4fbf2-150">2</span><span class="sxs-lookup"><span data-stu-id="4fbf2-150">2</span></span>     | <span data-ttu-id="4fbf2-151">/IFD/{UShort = 270}</span><span class="sxs-lookup"><span data-stu-id="4fbf2-151">/ifd/{ushort=270}</span></span>   | <span data-ttu-id="4fbf2-152">ascii</span><span class="sxs-lookup"><span data-stu-id="4fbf2-152">ascii</span></span>          |



 

### <a name="write-paths"></a><span data-ttu-id="4fbf2-153">Chemins d’accès en écriture</span><span class="sxs-lookup"><span data-stu-id="4fbf2-153">Write Paths</span></span>



| <span data-ttu-id="4fbf2-154">Commande</span><span class="sxs-lookup"><span data-stu-id="4fbf2-154">Order</span></span> | <span data-ttu-id="4fbf2-155">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="4fbf2-155">Path</span></span>                | <span data-ttu-id="4fbf2-156">Format de disque</span><span class="sxs-lookup"><span data-stu-id="4fbf2-156">Disk Format</span></span>    |
|-------|---------------------|----------------|
| <span data-ttu-id="4fbf2-157">1</span><span class="sxs-lookup"><span data-stu-id="4fbf2-157">1</span></span>     | <span data-ttu-id="4fbf2-158">/IFD/{UShort = 40095}</span><span class="sxs-lookup"><span data-stu-id="4fbf2-158">/ifd/{ushort=40095}</span></span> | <span data-ttu-id="4fbf2-159">\_octets Unicode</span><span class="sxs-lookup"><span data-stu-id="4fbf2-159">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="4fbf2-160">Supprimer les chemins</span><span class="sxs-lookup"><span data-stu-id="4fbf2-160">Remove Paths</span></span>



| <span data-ttu-id="4fbf2-161">Commande</span><span class="sxs-lookup"><span data-stu-id="4fbf2-161">Order</span></span> | <span data-ttu-id="4fbf2-162">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="4fbf2-162">Path</span></span>                |
|-------|---------------------|
| <span data-ttu-id="4fbf2-163">1</span><span class="sxs-lookup"><span data-stu-id="4fbf2-163">1</span></span>     | <span data-ttu-id="4fbf2-164">/IFD/{UShort = 40095}</span><span class="sxs-lookup"><span data-stu-id="4fbf2-164">/ifd/{ushort=40095}</span></span> |
| <span data-ttu-id="4fbf2-165">2</span><span class="sxs-lookup"><span data-stu-id="4fbf2-165">2</span></span>     | <span data-ttu-id="4fbf2-166">/IFD/{UShort = 270}</span><span class="sxs-lookup"><span data-stu-id="4fbf2-166">/ifd/{ushort=270}</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="4fbf2-167">Notes</span><span class="sxs-lookup"><span data-stu-id="4fbf2-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="4fbf2-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4fbf2-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fbf2-169">System. Subject</span><span class="sxs-lookup"><span data-stu-id="4fbf2-169">System.Subject</span></span>](../properties/props-system-subject.md)
</dt> </dl>

 

 
