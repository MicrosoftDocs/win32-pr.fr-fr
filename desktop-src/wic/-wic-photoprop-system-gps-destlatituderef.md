---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. DestLatitudeRef.
ms.assetid: 8a13642a-0d29-4193-9784-f716bc428c72
title: Stratégie de métadonnées de photo System. GPS. DestLatitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838e4688f0c3342091e5995885689a44fab38739
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524307"
---
# <a name="systemgpsdestlatituderef-photo-metadata-policy"></a><span data-ttu-id="b7e87-103">Stratégie de métadonnées de photo System. GPS. DestLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="b7e87-103">System.GPS.DestLatitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="b7e87-104">Stratégie de métadonnées de la photo pour la propriété [System. GPS. DestLatitudeRef](../properties/props-system-gps-destlatituderef.md) .</span><span class="sxs-lookup"><span data-stu-id="b7e87-104">The photo metadata policy for the [System.GPS.DestLatitudeRef](../properties/props-system-gps-destlatituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="b7e87-105">A-la</span><span class="sxs-lookup"><span data-stu-id="b7e87-105">PKEY</span></span>

<span data-ttu-id="b7e87-106">\_DestLatitudeRef GPS \_</span><span class="sxs-lookup"><span data-stu-id="b7e87-106">PKEY\_GPS\_DestLatitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="b7e87-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="b7e87-107">Containers</span></span>

<span data-ttu-id="b7e87-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="b7e87-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="b7e87-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b7e87-109">Read-Only</span></span>

<span data-ttu-id="b7e87-110">Non</span><span class="sxs-lookup"><span data-stu-id="b7e87-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="b7e87-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="b7e87-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="b7e87-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="b7e87-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="b7e87-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="b7e87-113">Input Type</span></span>

<span data-ttu-id="b7e87-114">VT \_ LPWStr est préféré, mais VT \_ LPSTR est accepté.</span><span class="sxs-lookup"><span data-stu-id="b7e87-114">VT\_LPWSTR is preferred, but VT\_LPSTR is accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="b7e87-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="b7e87-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="b7e87-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="b7e87-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="b7e87-117">Priorité des chemins d’accès (JPEG)</span><span class="sxs-lookup"><span data-stu-id="b7e87-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="b7e87-118">Si le fichier est au format JPEG, le gestionnaire lit, écrit et supprime les données dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="b7e87-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="b7e87-119">Commande</span><span class="sxs-lookup"><span data-stu-id="b7e87-119">Order</span></span> | <span data-ttu-id="b7e87-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="b7e87-120">Path</span></span>                          | <span data-ttu-id="b7e87-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="b7e87-121">Disk Format</span></span> | <span data-ttu-id="b7e87-122">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b7e87-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="b7e87-123">1</span><span class="sxs-lookup"><span data-stu-id="b7e87-123">1</span></span>     | <span data-ttu-id="b7e87-124">/xmp/exif:GPSDestLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="b7e87-124">/xmp/exif:GPSDestLatitudeRef</span></span>  | <span data-ttu-id="b7e87-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="b7e87-125">Unicode</span></span>     | <span data-ttu-id="b7e87-126">Oui</span><span class="sxs-lookup"><span data-stu-id="b7e87-126">Yes</span></span>      |
| <span data-ttu-id="b7e87-127">2</span><span class="sxs-lookup"><span data-stu-id="b7e87-127">2</span></span>     | <span data-ttu-id="b7e87-128">/App1/IFD/GPS/ \\ {UShort = 19 \\ }</span><span class="sxs-lookup"><span data-stu-id="b7e87-128">/app1/ifd/gps/\\{ushort=19\\}</span></span> | <span data-ttu-id="b7e87-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="b7e87-129">ASCII</span></span>       | <span data-ttu-id="b7e87-130">Non</span><span class="sxs-lookup"><span data-stu-id="b7e87-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="b7e87-131">Priorité des chemins d’accès (TIFF)</span><span class="sxs-lookup"><span data-stu-id="b7e87-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="b7e87-132">Si le fichier est au format TIFF, le gestionnaire lit, écrit et supprime les données dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="b7e87-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="b7e87-133">Commande</span><span class="sxs-lookup"><span data-stu-id="b7e87-133">Order</span></span> | <span data-ttu-id="b7e87-134">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="b7e87-134">Path</span></span>                             | <span data-ttu-id="b7e87-135">Format de disque</span><span class="sxs-lookup"><span data-stu-id="b7e87-135">Disk Format</span></span> | <span data-ttu-id="b7e87-136">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b7e87-136">Required</span></span> |
|-------|----------------------------------|-------------|----------|
| <span data-ttu-id="b7e87-137">1</span><span class="sxs-lookup"><span data-stu-id="b7e87-137">1</span></span>     | <span data-ttu-id="b7e87-138">/ifd/xmp/exif:GPSDestLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="b7e87-138">/ifd/xmp/exif:GPSDestLatitudeRef</span></span> | <span data-ttu-id="b7e87-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="b7e87-139">Unicode</span></span>     | <span data-ttu-id="b7e87-140">Oui</span><span class="sxs-lookup"><span data-stu-id="b7e87-140">Yes</span></span>      |
| <span data-ttu-id="b7e87-141">2</span><span class="sxs-lookup"><span data-stu-id="b7e87-141">2</span></span>     | <span data-ttu-id="b7e87-142">/IFD/GPS/ \\ {UShort = 19 \\ }</span><span class="sxs-lookup"><span data-stu-id="b7e87-142">/ifd/gps/\\{ushort=19\\}</span></span>         | <span data-ttu-id="b7e87-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="b7e87-143">ASCII</span></span>       | <span data-ttu-id="b7e87-144">Non</span><span class="sxs-lookup"><span data-stu-id="b7e87-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="b7e87-145">Notes</span><span class="sxs-lookup"><span data-stu-id="b7e87-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7e87-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7e87-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7e87-147">System. GPS. DestLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="b7e87-147">System.GPS.DestLatitudeRef</span></span>](../properties/props-system-gps-destlatituderef.md)
</dt> </dl>

 

 
