---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. MapDatum.
ms.assetid: be31e98f-5114-4693-a9ef-37fea334875b
title: Stratégie de métadonnées de photo System. GPS. MapDatum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb7a279c79da3d2b1dd20563af35bd34233a1a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522197"
---
# <a name="systemgpsmapdatum-photo-metadata-policy"></a><span data-ttu-id="99202-103">Stratégie de métadonnées de photo System. GPS. MapDatum</span><span class="sxs-lookup"><span data-stu-id="99202-103">System.GPS.MapDatum Photo Metadata Policy</span></span>

<span data-ttu-id="99202-104">Stratégie de métadonnées de la photo pour la propriété [System. GPS. MapDatum](../properties/props-system-gps-mapdatum.md) .</span><span class="sxs-lookup"><span data-stu-id="99202-104">The photo metadata policy for the [System.GPS.MapDatum](../properties/props-system-gps-mapdatum.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="99202-105">A-la</span><span class="sxs-lookup"><span data-stu-id="99202-105">PKEY</span></span>

<span data-ttu-id="99202-106">\_MapDatum GPS \_</span><span class="sxs-lookup"><span data-stu-id="99202-106">PKEY\_GPS\_MapDatum</span></span>

### <a name="containers"></a><span data-ttu-id="99202-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="99202-107">Containers</span></span>

<span data-ttu-id="99202-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="99202-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="99202-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="99202-109">Read-Only</span></span>

<span data-ttu-id="99202-110">Non</span><span class="sxs-lookup"><span data-stu-id="99202-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="99202-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="99202-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="99202-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="99202-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="99202-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="99202-113">Input Type</span></span>

<span data-ttu-id="99202-114">VT \_ LPWStr est préféré, mais VT \_ LPSTR est également accepté</span><span class="sxs-lookup"><span data-stu-id="99202-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="99202-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="99202-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="99202-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="99202-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="99202-117">Priorité des chemins d’accès (JPEG)</span><span class="sxs-lookup"><span data-stu-id="99202-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="99202-118">Si le fichier est au format JPEG, le gestionnaire lit, écrit et supprime les données dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="99202-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="99202-119">Commande</span><span class="sxs-lookup"><span data-stu-id="99202-119">Order</span></span> | <span data-ttu-id="99202-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="99202-120">Path</span></span>                          | <span data-ttu-id="99202-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="99202-121">Disk Format</span></span> | <span data-ttu-id="99202-122">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="99202-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="99202-123">1</span><span class="sxs-lookup"><span data-stu-id="99202-123">1</span></span>     | <span data-ttu-id="99202-124">/xmp/exif:GPSMapDatum</span><span class="sxs-lookup"><span data-stu-id="99202-124">/xmp/exif:GPSMapDatum</span></span>         | <span data-ttu-id="99202-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="99202-125">Unicode</span></span>     | <span data-ttu-id="99202-126">Oui</span><span class="sxs-lookup"><span data-stu-id="99202-126">Yes</span></span>      |
| <span data-ttu-id="99202-127">2</span><span class="sxs-lookup"><span data-stu-id="99202-127">2</span></span>     | <span data-ttu-id="99202-128">/App1/IFD/GPS/ \\ {UShort = 18 \\ }</span><span class="sxs-lookup"><span data-stu-id="99202-128">/app1/ifd/gps/\\{ushort=18\\}</span></span> | <span data-ttu-id="99202-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="99202-129">ASCII</span></span>       | <span data-ttu-id="99202-130">Non</span><span class="sxs-lookup"><span data-stu-id="99202-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="99202-131">Priorité des chemins d’accès (TIFF)</span><span class="sxs-lookup"><span data-stu-id="99202-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="99202-132">Si le fichier est au format TIFF, le gestionnaire lit, écrit et supprime les données dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="99202-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="99202-133">Commande</span><span class="sxs-lookup"><span data-stu-id="99202-133">Order</span></span> | <span data-ttu-id="99202-134">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="99202-134">Path</span></span>                      | <span data-ttu-id="99202-135">Format de disque</span><span class="sxs-lookup"><span data-stu-id="99202-135">Disk Format</span></span> | <span data-ttu-id="99202-136">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="99202-136">Required</span></span> |
|-------|---------------------------|-------------|----------|
| <span data-ttu-id="99202-137">1</span><span class="sxs-lookup"><span data-stu-id="99202-137">1</span></span>     | <span data-ttu-id="99202-138">/ifd/xmp/exif:GPSMapDatum</span><span class="sxs-lookup"><span data-stu-id="99202-138">/ifd/xmp/exif:GPSMapDatum</span></span> | <span data-ttu-id="99202-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="99202-139">Unicode</span></span>     | <span data-ttu-id="99202-140">Oui</span><span class="sxs-lookup"><span data-stu-id="99202-140">Yes</span></span>      |
| <span data-ttu-id="99202-141">2</span><span class="sxs-lookup"><span data-stu-id="99202-141">2</span></span>     | <span data-ttu-id="99202-142">/IFD/GPS/ \\ {UShort = 18 \\ }</span><span class="sxs-lookup"><span data-stu-id="99202-142">/ifd/gps/\\{ushort=18\\}</span></span>  | <span data-ttu-id="99202-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="99202-143">ASCII</span></span>       | <span data-ttu-id="99202-144">Non</span><span class="sxs-lookup"><span data-stu-id="99202-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="99202-145">Notes</span><span class="sxs-lookup"><span data-stu-id="99202-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="99202-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="99202-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99202-147">System. GPS. MapDatum</span><span class="sxs-lookup"><span data-stu-id="99202-147">System.GPS.MapDatum</span></span>](../properties/props-system-gps-mapdatum.md)
</dt> </dl>

 

 
