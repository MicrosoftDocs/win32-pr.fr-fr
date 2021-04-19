---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. DestLongitudeRef.
ms.assetid: 2a0abb9b-41e3-49ba-a60b-3096d9c032bd
title: Stratégie de métadonnées de photo System. GPS. DestLongitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8139fcf5218d9863393888d7ab7b188a53e7f55f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541960"
---
# <a name="systemgpsdestlongituderef-photo-metadata-policy"></a><span data-ttu-id="4e2da-103">Stratégie de métadonnées de photo System. GPS. DestLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="4e2da-103">System.GPS.DestLongitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="4e2da-104">Stratégie de métadonnées de la photo pour la propriété [System. GPS. DestLongitudeRef](../properties/props-system-gps-destlongituderef.md) .</span><span class="sxs-lookup"><span data-stu-id="4e2da-104">The photo metadata policy for the [System.GPS.DestLongitudeRef](../properties/props-system-gps-destlongituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="4e2da-105">A-la</span><span class="sxs-lookup"><span data-stu-id="4e2da-105">PKEY</span></span>

<span data-ttu-id="4e2da-106">\_GPS. DestLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="4e2da-106">PKEY\_GPS.DestLongitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="4e2da-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="4e2da-107">Containers</span></span>

<span data-ttu-id="4e2da-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="4e2da-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="4e2da-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e2da-109">Read-Only</span></span>

<span data-ttu-id="4e2da-110">Non</span><span class="sxs-lookup"><span data-stu-id="4e2da-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="4e2da-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="4e2da-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="4e2da-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="4e2da-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="4e2da-113">Type de PROPVARIANT d’entrée</span><span class="sxs-lookup"><span data-stu-id="4e2da-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="4e2da-114">VT \_ LPWStr est préféré, mais VT \_ LPSTR est également accepté.</span><span class="sxs-lookup"><span data-stu-id="4e2da-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="4e2da-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="4e2da-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="4e2da-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="4e2da-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="4e2da-117">Priorité des chemins d’accès (JPEG)</span><span class="sxs-lookup"><span data-stu-id="4e2da-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="4e2da-118">Si le fichier est au format JPEG, le gestionnaire lit, écrit et supprime les données dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="4e2da-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="4e2da-119">Commande</span><span class="sxs-lookup"><span data-stu-id="4e2da-119">Order</span></span> | <span data-ttu-id="4e2da-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="4e2da-120">Path</span></span>                          | <span data-ttu-id="4e2da-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="4e2da-121">Disk Format</span></span> | <span data-ttu-id="4e2da-122">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="4e2da-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="4e2da-123">1</span><span class="sxs-lookup"><span data-stu-id="4e2da-123">1</span></span>     | <span data-ttu-id="4e2da-124">/xmp/exif:GPSDestLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="4e2da-124">/xmp/exif:GPSDestLongitudeRef</span></span> | <span data-ttu-id="4e2da-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="4e2da-125">Unicode</span></span>     | <span data-ttu-id="4e2da-126">Oui</span><span class="sxs-lookup"><span data-stu-id="4e2da-126">Yes</span></span>      |
| <span data-ttu-id="4e2da-127">2</span><span class="sxs-lookup"><span data-stu-id="4e2da-127">2</span></span>     | <span data-ttu-id="4e2da-128">/App1/IFD/GPS/ \\ {UShort = 21 \\ }</span><span class="sxs-lookup"><span data-stu-id="4e2da-128">/app1/ifd/gps/\\{ushort=21\\}</span></span> | <span data-ttu-id="4e2da-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="4e2da-129">ASCII</span></span>       | <span data-ttu-id="4e2da-130">Non</span><span class="sxs-lookup"><span data-stu-id="4e2da-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="4e2da-131">Priorité des chemins d’accès (TIFF)</span><span class="sxs-lookup"><span data-stu-id="4e2da-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="4e2da-132">Si le fichier est au format TIFF, le gestionnaire lit, écrit et supprime les données dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="4e2da-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="4e2da-133">Commande</span><span class="sxs-lookup"><span data-stu-id="4e2da-133">Order</span></span> | <span data-ttu-id="4e2da-134">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="4e2da-134">Path</span></span>                              | <span data-ttu-id="4e2da-135">Format de disque</span><span class="sxs-lookup"><span data-stu-id="4e2da-135">Disk Format</span></span> | <span data-ttu-id="4e2da-136">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="4e2da-136">Required</span></span> |
|-------|-----------------------------------|-------------|----------|
| <span data-ttu-id="4e2da-137">1</span><span class="sxs-lookup"><span data-stu-id="4e2da-137">1</span></span>     | <span data-ttu-id="4e2da-138">/ifd/xmp/exif:GPSDestLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="4e2da-138">/ifd/xmp/exif:GPSDestLongitudeRef</span></span> | <span data-ttu-id="4e2da-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="4e2da-139">Unicode</span></span>     | <span data-ttu-id="4e2da-140">Oui</span><span class="sxs-lookup"><span data-stu-id="4e2da-140">Yes</span></span>      |
| <span data-ttu-id="4e2da-141">2</span><span class="sxs-lookup"><span data-stu-id="4e2da-141">2</span></span>     | <span data-ttu-id="4e2da-142">/IFD/GPS/ \\ {UShort = 21 \\ }</span><span class="sxs-lookup"><span data-stu-id="4e2da-142">/ifd/gps/\\{ushort=21\\}</span></span>          | <span data-ttu-id="4e2da-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="4e2da-143">ASCII</span></span>       | <span data-ttu-id="4e2da-144">Non</span><span class="sxs-lookup"><span data-stu-id="4e2da-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="4e2da-145">Notes</span><span class="sxs-lookup"><span data-stu-id="4e2da-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e2da-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4e2da-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e2da-147">System. GPS. DestLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="4e2da-147">System.GPS.DestLongitudeRef</span></span>](../properties/props-system-gps-destlongituderef.md)
</dt> </dl>

 

 
