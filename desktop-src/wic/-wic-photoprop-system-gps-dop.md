---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. DOP.
ms.assetid: 62efd1cc-a2ae-4e53-a0f2-4822b8c91c42
title: Stratégie de métadonnées de photo System. GPS. DOP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c33f3bfc6b958593748396124a8cfd1a7de73fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952908"
---
# <a name="systemgpsdop-photo-metadata-policy"></a><span data-ttu-id="73b6c-103">Stratégie de métadonnées de photo System. GPS. DOP</span><span class="sxs-lookup"><span data-stu-id="73b6c-103">System.GPS.DOP Photo Metadata Policy</span></span>

<span data-ttu-id="73b6c-104">Stratégie de métadonnées de la photo pour la propriété [System. GPS. DOP](../properties/props-system-gps-dop.md) .</span><span class="sxs-lookup"><span data-stu-id="73b6c-104">The photo metadata policy for the [System.GPS.DOP](../properties/props-system-gps-dop.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="73b6c-105">A-la</span><span class="sxs-lookup"><span data-stu-id="73b6c-105">PKEY</span></span>

<span data-ttu-id="73b6c-106">la \_ \_ DOP GPS</span><span class="sxs-lookup"><span data-stu-id="73b6c-106">PKEY\_GPS\_DOP</span></span>

### <a name="containers"></a><span data-ttu-id="73b6c-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="73b6c-107">Containers</span></span>

<span data-ttu-id="73b6c-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="73b6c-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="73b6c-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73b6c-109">Read-Only</span></span>

<span data-ttu-id="73b6c-110">Oui</span><span class="sxs-lookup"><span data-stu-id="73b6c-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="73b6c-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="73b6c-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="73b6c-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="73b6c-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="73b6c-113">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="73b6c-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="73b6c-114">Cette valeur peut être écrite en écrivant dans System. GPS. DOPNumerator et System. GPS. DOPDenominator.</span><span class="sxs-lookup"><span data-stu-id="73b6c-114">This value can be written by writing to System.GPS.DOPNumerator and System.GPS.DOPDenominator.</span></span> <span data-ttu-id="73b6c-115">Il ne peut pas être écrit directement.</span><span class="sxs-lookup"><span data-stu-id="73b6c-115">It cannot be written directly.</span></span> <span data-ttu-id="73b6c-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="73b6c-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="73b6c-117">Priorité des chemins d’accès (JPEG)</span><span class="sxs-lookup"><span data-stu-id="73b6c-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="73b6c-118">Si le fichier est au format JPEG, le gestionnaire lit, écrit et supprime les données dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="73b6c-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="73b6c-119">Commande</span><span class="sxs-lookup"><span data-stu-id="73b6c-119">Order</span></span> | <span data-ttu-id="73b6c-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="73b6c-120">Path</span></span>                          | <span data-ttu-id="73b6c-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="73b6c-121">Disk Format</span></span>   | <span data-ttu-id="73b6c-122">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="73b6c-122">Required</span></span> |
|-------|-------------------------------|---------------|----------|
| <span data-ttu-id="73b6c-123">1</span><span class="sxs-lookup"><span data-stu-id="73b6c-123">1</span></span>     | <span data-ttu-id="73b6c-124">/xmp/exif:GPSDOP</span><span class="sxs-lookup"><span data-stu-id="73b6c-124">/xmp/exif:GPSDOP</span></span>              | <span data-ttu-id="73b6c-125">XMP Rational</span><span class="sxs-lookup"><span data-stu-id="73b6c-125">XMP rational</span></span>  | <span data-ttu-id="73b6c-126">Oui</span><span class="sxs-lookup"><span data-stu-id="73b6c-126">Yes</span></span>      |
| <span data-ttu-id="73b6c-127">2</span><span class="sxs-lookup"><span data-stu-id="73b6c-127">2</span></span>     | <span data-ttu-id="73b6c-128">/App1/IFD/GPS/ \\ {UShort = 11 \\ }</span><span class="sxs-lookup"><span data-stu-id="73b6c-128">/app1/ifd/gps/\\{ushort=11\\}</span></span> | <span data-ttu-id="73b6c-129">EXIF (Rational)</span><span class="sxs-lookup"><span data-stu-id="73b6c-129">EXIF rational</span></span> | <span data-ttu-id="73b6c-130">Non</span><span class="sxs-lookup"><span data-stu-id="73b6c-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="73b6c-131">Priorité des chemins d’accès (TIFF)</span><span class="sxs-lookup"><span data-stu-id="73b6c-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="73b6c-132">Si le fichier est au format TIFF, le gestionnaire lit, écrit et supprime les données dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="73b6c-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="73b6c-133">Commande</span><span class="sxs-lookup"><span data-stu-id="73b6c-133">Order</span></span> | <span data-ttu-id="73b6c-134">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="73b6c-134">Path</span></span>                     | <span data-ttu-id="73b6c-135">Format de disque</span><span class="sxs-lookup"><span data-stu-id="73b6c-135">Disk Format</span></span>   | <span data-ttu-id="73b6c-136">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="73b6c-136">Required</span></span> |
|-------|--------------------------|---------------|----------|
| <span data-ttu-id="73b6c-137">1</span><span class="sxs-lookup"><span data-stu-id="73b6c-137">1</span></span>     | <span data-ttu-id="73b6c-138">/ifd/xmp/exif:GPSDop</span><span class="sxs-lookup"><span data-stu-id="73b6c-138">/ifd/xmp/exif:GPSDop</span></span>     | <span data-ttu-id="73b6c-139">XMP Rational</span><span class="sxs-lookup"><span data-stu-id="73b6c-139">XMP rational</span></span>  | <span data-ttu-id="73b6c-140">Oui</span><span class="sxs-lookup"><span data-stu-id="73b6c-140">Yes</span></span>      |
| <span data-ttu-id="73b6c-141">2</span><span class="sxs-lookup"><span data-stu-id="73b6c-141">2</span></span>     | <span data-ttu-id="73b6c-142">/IFD/GPS/ \\ {UShort = 11 \\ }</span><span class="sxs-lookup"><span data-stu-id="73b6c-142">/ifd/gps/\\{ushort=11\\}</span></span> | <span data-ttu-id="73b6c-143">EXIF (Rational)</span><span class="sxs-lookup"><span data-stu-id="73b6c-143">EXIF rational</span></span> | <span data-ttu-id="73b6c-144">Non</span><span class="sxs-lookup"><span data-stu-id="73b6c-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="73b6c-145">Notes</span><span class="sxs-lookup"><span data-stu-id="73b6c-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="73b6c-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="73b6c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73b6c-147">System. GPS. DOP</span><span class="sxs-lookup"><span data-stu-id="73b6c-147">System.GPS.DOP</span></span>](../properties/props-system-gps-dop.md)
</dt> </dl>

 

 
