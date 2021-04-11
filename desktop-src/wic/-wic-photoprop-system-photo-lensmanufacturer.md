---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. LensManufacturer.
ms.assetid: ee25da96-982f-475e-8957-e24ef7721b78
title: Stratégie de métadonnées de photo System. photo. LensManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6696e7113a14a9b5b26a26f38258f30a5ba82cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204220"
---
# <a name="systemphotolensmanufacturer-photo-metadata-policy"></a><span data-ttu-id="8dfe3-103">Stratégie de métadonnées de photo System. photo. LensManufacturer</span><span class="sxs-lookup"><span data-stu-id="8dfe3-103">System.Photo.LensManufacturer Photo Metadata Policy</span></span>

<span data-ttu-id="8dfe3-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. LensManufacturer](../properties/props-system-photo-lensmanufacturer.md) .</span><span class="sxs-lookup"><span data-stu-id="8dfe3-104">The photo metadata policy for the [System.Photo.LensManufacturer](../properties/props-system-photo-lensmanufacturer.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="8dfe3-105">A-la</span><span class="sxs-lookup"><span data-stu-id="8dfe3-105">PKEY</span></span>

<span data-ttu-id="8dfe3-106">\_Photo \_ LensManufacturer</span><span class="sxs-lookup"><span data-stu-id="8dfe3-106">PKEY\_Photo\_LensManufacturer</span></span>

### <a name="containers"></a><span data-ttu-id="8dfe3-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="8dfe3-107">Containers</span></span>

<span data-ttu-id="8dfe3-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="8dfe3-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="8dfe3-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8dfe3-109">Read-Only</span></span>

<span data-ttu-id="8dfe3-110">Non</span><span class="sxs-lookup"><span data-stu-id="8dfe3-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="8dfe3-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="8dfe3-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="8dfe3-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="8dfe3-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="8dfe3-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="8dfe3-113">Input Type</span></span>

<span data-ttu-id="8dfe3-114">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="8dfe3-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="8dfe3-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="8dfe3-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="8dfe3-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="8dfe3-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="8dfe3-117">Priorité des chemins d’accès (JPEG)</span><span class="sxs-lookup"><span data-stu-id="8dfe3-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="8dfe3-118">Si le fichier est au format JPEG, le gestionnaire utilise le chemin d’accès suivant lors de la lecture ou de l’écriture des données.</span><span class="sxs-lookup"><span data-stu-id="8dfe3-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="8dfe3-119">Commande</span><span class="sxs-lookup"><span data-stu-id="8dfe3-119">Order</span></span> | <span data-ttu-id="8dfe3-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="8dfe3-120">Path</span></span>                                 | <span data-ttu-id="8dfe3-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="8dfe3-121">Disk Format</span></span> | <span data-ttu-id="8dfe3-122">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8dfe3-122">Required</span></span> |
|-------|--------------------------------------|-------------|----------|
| <span data-ttu-id="8dfe3-123">1</span><span class="sxs-lookup"><span data-stu-id="8dfe3-123">1</span></span>     | <span data-ttu-id="8dfe3-124">/xmp/MicrosoftPhoto:LensManufacturer</span><span class="sxs-lookup"><span data-stu-id="8dfe3-124">/xmp/MicrosoftPhoto:LensManufacturer</span></span> | <span data-ttu-id="8dfe3-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="8dfe3-125">Unicode</span></span>     | <span data-ttu-id="8dfe3-126">Oui</span><span class="sxs-lookup"><span data-stu-id="8dfe3-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="8dfe3-127">Priorité des chemins d’accès (TIFF)</span><span class="sxs-lookup"><span data-stu-id="8dfe3-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="8dfe3-128">Si le fichier est au format TIFF, le gestionnaire utilise l’ordre de priorité suivant lors de la lecture ou de l’écriture des données.</span><span class="sxs-lookup"><span data-stu-id="8dfe3-128">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="8dfe3-129">Commande</span><span class="sxs-lookup"><span data-stu-id="8dfe3-129">Order</span></span> | <span data-ttu-id="8dfe3-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="8dfe3-130">Path</span></span>                                     | <span data-ttu-id="8dfe3-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="8dfe3-131">Disk Format</span></span> | <span data-ttu-id="8dfe3-132">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8dfe3-132">Required</span></span> |
|-------|------------------------------------------|-------------|----------|
| <span data-ttu-id="8dfe3-133">1</span><span class="sxs-lookup"><span data-stu-id="8dfe3-133">1</span></span>     | <span data-ttu-id="8dfe3-134">/ifd/xmp/MicrosoftPhoto:LensManufacturer</span><span class="sxs-lookup"><span data-stu-id="8dfe3-134">/ifd/xmp/MicrosoftPhoto:LensManufacturer</span></span> | <span data-ttu-id="8dfe3-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="8dfe3-135">Unicode</span></span>     | <span data-ttu-id="8dfe3-136">Oui</span><span class="sxs-lookup"><span data-stu-id="8dfe3-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="8dfe3-137">Notes</span><span class="sxs-lookup"><span data-stu-id="8dfe3-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="8dfe3-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8dfe3-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8dfe3-139">System. photo. LensManufacturer</span><span class="sxs-lookup"><span data-stu-id="8dfe3-139">System.Photo.LensManufacturer</span></span>](../properties/props-system-photo-lensmanufacturer.md)
</dt> </dl>

 

 
