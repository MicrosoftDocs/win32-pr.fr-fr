---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. FlashModel.
ms.assetid: ef322823-1b87-40ea-a5e3-e7551f14e44d
title: Stratégie de métadonnées de photo System. photo. FlashModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ade3769cb0d852239af84b769b85d5b3849589
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539111"
---
# <a name="systemphotoflashmodel-photo-metadata-policy"></a><span data-ttu-id="771c4-103">Stratégie de métadonnées de photo System. photo. FlashModel</span><span class="sxs-lookup"><span data-stu-id="771c4-103">System.Photo.FlashModel Photo Metadata Policy</span></span>

<span data-ttu-id="771c4-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. FlashModel](../properties/props-system-photo-flashmodel.md) .</span><span class="sxs-lookup"><span data-stu-id="771c4-104">The photo metadata policy for the [System.Photo.FlashModel](../properties/props-system-photo-flashmodel.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="771c4-105">A-la</span><span class="sxs-lookup"><span data-stu-id="771c4-105">PKEY</span></span>

<span data-ttu-id="771c4-106">\_Photo \_ FlashModel</span><span class="sxs-lookup"><span data-stu-id="771c4-106">PKEY\_Photo\_FlashModel</span></span>

### <a name="containers"></a><span data-ttu-id="771c4-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="771c4-107">Containers</span></span>

<span data-ttu-id="771c4-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="771c4-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="771c4-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="771c4-109">Read-Only</span></span>

<span data-ttu-id="771c4-110">Non</span><span class="sxs-lookup"><span data-stu-id="771c4-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="771c4-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="771c4-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="771c4-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="771c4-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="771c4-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="771c4-113">Input Type</span></span>

<span data-ttu-id="771c4-114">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="771c4-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="771c4-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="771c4-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="771c4-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="771c4-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="771c4-117">Priorité des chemins d’accès (JPEG)</span><span class="sxs-lookup"><span data-stu-id="771c4-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="771c4-118">Si le fichier est au format JPEG, le gestionnaire utilise le chemin d’accès suivant lors de la lecture ou de l’écriture des données.</span><span class="sxs-lookup"><span data-stu-id="771c4-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="771c4-119">Commande</span><span class="sxs-lookup"><span data-stu-id="771c4-119">Order</span></span> | <span data-ttu-id="771c4-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="771c4-120">Path</span></span>                           | <span data-ttu-id="771c4-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="771c4-121">Disk Format</span></span> | <span data-ttu-id="771c4-122">Format de données</span><span class="sxs-lookup"><span data-stu-id="771c4-122">Data Format</span></span> | <span data-ttu-id="771c4-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="771c4-123">Required</span></span> |
|-------|--------------------------------|-------------|-------------|----------|
| <span data-ttu-id="771c4-124">1</span><span class="sxs-lookup"><span data-stu-id="771c4-124">1</span></span>     | <span data-ttu-id="771c4-125">/xmp/MicrosoftPhoto:FlashModel</span><span class="sxs-lookup"><span data-stu-id="771c4-125">/xmp/MicrosoftPhoto:FlashModel</span></span> | <span data-ttu-id="771c4-126">Unicode</span><span class="sxs-lookup"><span data-stu-id="771c4-126">Unicode</span></span>     |             | <span data-ttu-id="771c4-127">Oui</span><span class="sxs-lookup"><span data-stu-id="771c4-127">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="771c4-128">Priorité des chemins d’accès (TIFF)</span><span class="sxs-lookup"><span data-stu-id="771c4-128">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="771c4-129">Si le fichier est au format TIFF, le gestionnaire utilise l’ordre de priorité suivant lors de la lecture ou de l’écriture des données.</span><span class="sxs-lookup"><span data-stu-id="771c4-129">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="771c4-130">Commande</span><span class="sxs-lookup"><span data-stu-id="771c4-130">Order</span></span> | <span data-ttu-id="771c4-131">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="771c4-131">Path</span></span>                               | <span data-ttu-id="771c4-132">Format de disque</span><span class="sxs-lookup"><span data-stu-id="771c4-132">Disk Format</span></span> | <span data-ttu-id="771c4-133">Format de données</span><span class="sxs-lookup"><span data-stu-id="771c4-133">Data Format</span></span> | <span data-ttu-id="771c4-134">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="771c4-134">Required</span></span> |
|-------|------------------------------------|-------------|-------------|----------|
| <span data-ttu-id="771c4-135">1</span><span class="sxs-lookup"><span data-stu-id="771c4-135">1</span></span>     | <span data-ttu-id="771c4-136">/ifd/xmp/MicrosoftPhoto:FlashModel</span><span class="sxs-lookup"><span data-stu-id="771c4-136">/ifd/xmp/MicrosoftPhoto:FlashModel</span></span> | <span data-ttu-id="771c4-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="771c4-137">Unicode</span></span>     |             | <span data-ttu-id="771c4-138">Oui</span><span class="sxs-lookup"><span data-stu-id="771c4-138">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="771c4-139">Notes</span><span class="sxs-lookup"><span data-stu-id="771c4-139">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="771c4-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="771c4-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="771c4-141">System. photo. FlashModel</span><span class="sxs-lookup"><span data-stu-id="771c4-141">System.Photo.FlashModel</span></span>](../properties/props-system-photo-flashmodel.md)
</dt> </dl>

 

 
