---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. FlashManufacturer.
ms.assetid: f62e85ec-2dc6-456b-a43b-7b76d162b608
title: Stratégie de métadonnées de photo System. photo. FlashManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa1e785dfd00662acf065021a3c80de5c587586c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035169"
---
# <a name="systemphotoflashmanufacturer-photo-metadata-policy"></a><span data-ttu-id="8c61f-103">Stratégie de métadonnées de photo System. photo. FlashManufacturer</span><span class="sxs-lookup"><span data-stu-id="8c61f-103">System.Photo.FlashManufacturer Photo Metadata Policy</span></span>

<span data-ttu-id="8c61f-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. FlashManufacturer](../properties/props-system-photo-flashmanufacturer.md) .</span><span class="sxs-lookup"><span data-stu-id="8c61f-104">The photo metadata policy for the [System.Photo.FlashManufacturer](../properties/props-system-photo-flashmanufacturer.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="8c61f-105">A-la</span><span class="sxs-lookup"><span data-stu-id="8c61f-105">PKEY</span></span>

<span data-ttu-id="8c61f-106">\_Photo \_ FlashManufacturer</span><span class="sxs-lookup"><span data-stu-id="8c61f-106">PKEY\_Photo\_FlashManufacturer</span></span>

### <a name="containers"></a><span data-ttu-id="8c61f-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="8c61f-107">Containers</span></span>

<span data-ttu-id="8c61f-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="8c61f-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="8c61f-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8c61f-109">Read-Only</span></span>

<span data-ttu-id="8c61f-110">Non</span><span class="sxs-lookup"><span data-stu-id="8c61f-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="8c61f-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="8c61f-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="8c61f-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="8c61f-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="8c61f-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="8c61f-113">Input Type</span></span>

<span data-ttu-id="8c61f-114">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="8c61f-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="8c61f-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="8c61f-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="8c61f-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="8c61f-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="8c61f-117">Priorité des chemins d’accès (JPEG)</span><span class="sxs-lookup"><span data-stu-id="8c61f-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="8c61f-118">Si le fichier est au format JPEG, le gestionnaire utilise le chemin d’accès suivant lors de la lecture ou de l’écriture des données.</span><span class="sxs-lookup"><span data-stu-id="8c61f-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="8c61f-119">Commande</span><span class="sxs-lookup"><span data-stu-id="8c61f-119">Order</span></span> | <span data-ttu-id="8c61f-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="8c61f-120">Path</span></span>                                  | <span data-ttu-id="8c61f-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="8c61f-121">Disk Format</span></span> | <span data-ttu-id="8c61f-122">Format de données</span><span class="sxs-lookup"><span data-stu-id="8c61f-122">Data Format</span></span> | <span data-ttu-id="8c61f-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8c61f-123">Required</span></span> |
|-------|---------------------------------------|-------------|-------------|----------|
| <span data-ttu-id="8c61f-124">1</span><span class="sxs-lookup"><span data-stu-id="8c61f-124">1</span></span>     | <span data-ttu-id="8c61f-125">/xmp/MicrosoftPhoto:FlashManufacturer</span><span class="sxs-lookup"><span data-stu-id="8c61f-125">/xmp/MicrosoftPhoto:FlashManufacturer</span></span> | <span data-ttu-id="8c61f-126">Unicode</span><span class="sxs-lookup"><span data-stu-id="8c61f-126">Unicode</span></span>     |             | <span data-ttu-id="8c61f-127">Oui</span><span class="sxs-lookup"><span data-stu-id="8c61f-127">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="8c61f-128">Priorité des chemins d’accès (TIFF)</span><span class="sxs-lookup"><span data-stu-id="8c61f-128">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="8c61f-129">Si le fichier est au format TIFF, le gestionnaire utilise l’ordre de priorité suivant lors de la lecture ou de l’écriture des données.</span><span class="sxs-lookup"><span data-stu-id="8c61f-129">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="8c61f-130">Commande</span><span class="sxs-lookup"><span data-stu-id="8c61f-130">Order</span></span> | <span data-ttu-id="8c61f-131">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="8c61f-131">Path</span></span>                                      | <span data-ttu-id="8c61f-132">Format de disque</span><span class="sxs-lookup"><span data-stu-id="8c61f-132">Disk Format</span></span> | <span data-ttu-id="8c61f-133">Format de données</span><span class="sxs-lookup"><span data-stu-id="8c61f-133">Data Format</span></span> | <span data-ttu-id="8c61f-134">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8c61f-134">Required</span></span> |
|-------|-------------------------------------------|-------------|-------------|----------|
| <span data-ttu-id="8c61f-135">1</span><span class="sxs-lookup"><span data-stu-id="8c61f-135">1</span></span>     | <span data-ttu-id="8c61f-136">/ifd/xmp/MicrosoftPhoto:FlashManufacturer</span><span class="sxs-lookup"><span data-stu-id="8c61f-136">/ifd/xmp/MicrosoftPhoto:FlashManufacturer</span></span> | <span data-ttu-id="8c61f-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="8c61f-137">Unicode</span></span>     |             | <span data-ttu-id="8c61f-138">Oui</span><span class="sxs-lookup"><span data-stu-id="8c61f-138">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="8c61f-139">Notes</span><span class="sxs-lookup"><span data-stu-id="8c61f-139">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c61f-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8c61f-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c61f-141">System. photo. FlashManufacturer</span><span class="sxs-lookup"><span data-stu-id="8c61f-141">System.Photo.FlashManufacturer</span></span>](../properties/props-system-photo-flashmanufacturer.md)
</dt> </dl>

 

 
