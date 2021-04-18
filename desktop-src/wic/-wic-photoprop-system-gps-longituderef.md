---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. LongitudeRef.
ms.assetid: 6e7b3b87-70e5-4c6a-a9b3-959eab38f1f0
title: Stratégie de métadonnées de photo System. GPS. LongitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a93d37b59ca7c77bc05e049860cf4e2608eb60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534108"
---
# <a name="systemgpslongituderef-photo-metadata-policy"></a><span data-ttu-id="f6103-103">Stratégie de métadonnées de photo System. GPS. LongitudeRef</span><span class="sxs-lookup"><span data-stu-id="f6103-103">System.GPS.LongitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="f6103-104">Stratégie de métadonnées de la photo pour la propriété [System. GPS. LongitudeRef](../properties/props-system-gps-longituderef.md) .</span><span class="sxs-lookup"><span data-stu-id="f6103-104">The photo metadata policy for the [System.GPS.LongitudeRef](../properties/props-system-gps-longituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="f6103-105">A-la</span><span class="sxs-lookup"><span data-stu-id="f6103-105">PKEY</span></span>

<span data-ttu-id="f6103-106">\_LongitudeRef GPS \_</span><span class="sxs-lookup"><span data-stu-id="f6103-106">PKEY\_GPS\_LongitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="f6103-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="f6103-107">Containers</span></span>

<span data-ttu-id="f6103-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="f6103-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="f6103-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f6103-109">Read-Only</span></span>

<span data-ttu-id="f6103-110">Non</span><span class="sxs-lookup"><span data-stu-id="f6103-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="f6103-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="f6103-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="f6103-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="f6103-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="f6103-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="f6103-113">Input Type</span></span>

<span data-ttu-id="f6103-114">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="f6103-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="f6103-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="f6103-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="f6103-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="f6103-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="f6103-117">Priorité des chemins d’accès (JPEG)</span><span class="sxs-lookup"><span data-stu-id="f6103-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="f6103-118">Si le fichier est au format JPEG, le gestionnaire lit, écrit et supprime les données dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="f6103-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="f6103-119">Commande</span><span class="sxs-lookup"><span data-stu-id="f6103-119">Order</span></span> | <span data-ttu-id="f6103-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="f6103-120">Path</span></span>                         | <span data-ttu-id="f6103-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="f6103-121">Disk Format</span></span> | <span data-ttu-id="f6103-122">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f6103-122">Required</span></span> |
|-------|------------------------------|-------------|----------|
| <span data-ttu-id="f6103-123">1</span><span class="sxs-lookup"><span data-stu-id="f6103-123">1</span></span>     | <span data-ttu-id="f6103-124">/xmp/exif:GPSLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="f6103-124">/xmp/exif:GPSLongitudeRef</span></span>    | <span data-ttu-id="f6103-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="f6103-125">Unicode</span></span>     | <span data-ttu-id="f6103-126">Oui</span><span class="sxs-lookup"><span data-stu-id="f6103-126">Yes</span></span>      |
| <span data-ttu-id="f6103-127">2</span><span class="sxs-lookup"><span data-stu-id="f6103-127">2</span></span>     | <span data-ttu-id="f6103-128">/App1/IFD/GPS/ \\ {UShort = 3 \\ }</span><span class="sxs-lookup"><span data-stu-id="f6103-128">/app1/ifd/gps/\\{ushort=3\\}</span></span> | <span data-ttu-id="f6103-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="f6103-129">ASCII</span></span>       | <span data-ttu-id="f6103-130">Non</span><span class="sxs-lookup"><span data-stu-id="f6103-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="f6103-131">Priorité des chemins d’accès (TIFF)</span><span class="sxs-lookup"><span data-stu-id="f6103-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="f6103-132">Si le fichier est au format TIFF, le gestionnaire lit, écrit et supprime les données dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="f6103-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="f6103-133">Commande</span><span class="sxs-lookup"><span data-stu-id="f6103-133">Order</span></span> | <span data-ttu-id="f6103-134">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="f6103-134">Path</span></span>                          | <span data-ttu-id="f6103-135">Format de disque</span><span class="sxs-lookup"><span data-stu-id="f6103-135">Disk Format</span></span> | <span data-ttu-id="f6103-136">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f6103-136">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="f6103-137">1</span><span class="sxs-lookup"><span data-stu-id="f6103-137">1</span></span>     | <span data-ttu-id="f6103-138">/ifd/xmp/exif:GPSLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="f6103-138">/ifd/xmp/exif:GPSLongitudeRef</span></span> | <span data-ttu-id="f6103-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="f6103-139">Unicode</span></span>     | <span data-ttu-id="f6103-140">Oui</span><span class="sxs-lookup"><span data-stu-id="f6103-140">Yes</span></span>      |
| <span data-ttu-id="f6103-141">2</span><span class="sxs-lookup"><span data-stu-id="f6103-141">2</span></span>     | <span data-ttu-id="f6103-142">/IFD/GPS/ \\ {UShort = 3 \\ }</span><span class="sxs-lookup"><span data-stu-id="f6103-142">/ifd/gps/\\{ushort=3\\}</span></span>       | <span data-ttu-id="f6103-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="f6103-143">ASCII</span></span>       | <span data-ttu-id="f6103-144">Non</span><span class="sxs-lookup"><span data-stu-id="f6103-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="f6103-145">Notes</span><span class="sxs-lookup"><span data-stu-id="f6103-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6103-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f6103-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6103-147">System. GPS. LongitudeRef</span><span class="sxs-lookup"><span data-stu-id="f6103-147">System.GPS.LongitudeRef</span></span>](../properties/props-system-gps-longituderef.md)
</dt> </dl>

 

 
