---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. LensModel.
ms.assetid: 39aeff17-e8d3-4ceb-86a1-1749d2ca98d6
title: Stratégie de métadonnées de photo System. photo. LensModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a5249136346407ab9fcd1e4802d6910d3e514a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035030"
---
# <a name="systemphotolensmodel-photo-metadata-policy"></a><span data-ttu-id="63397-103">Stratégie de métadonnées de photo System. photo. LensModel</span><span class="sxs-lookup"><span data-stu-id="63397-103">System.Photo.LensModel Photo Metadata Policy</span></span>

<span data-ttu-id="63397-104">Stratégie de métadonnées de la photo pour la propriété [System. photo. LensModel](../properties/props-system-photo-lensmodel.md) .</span><span class="sxs-lookup"><span data-stu-id="63397-104">The photo metadata policy for the [System.Photo.LensModel](../properties/props-system-photo-lensmodel.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="63397-105">A-la</span><span class="sxs-lookup"><span data-stu-id="63397-105">PKEY</span></span>

<span data-ttu-id="63397-106">\_Photo \_ LensModel</span><span class="sxs-lookup"><span data-stu-id="63397-106">PKEY\_Photo\_LensModel</span></span>

### <a name="containers"></a><span data-ttu-id="63397-107">Conteneurs</span><span class="sxs-lookup"><span data-stu-id="63397-107">Containers</span></span>

<span data-ttu-id="63397-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="63397-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="63397-109">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63397-109">Read-Only</span></span>

<span data-ttu-id="63397-110">Non</span><span class="sxs-lookup"><span data-stu-id="63397-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="63397-111">Type PROPVARIANT de sortie</span><span class="sxs-lookup"><span data-stu-id="63397-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="63397-112">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="63397-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="63397-113">Type d’entrée</span><span class="sxs-lookup"><span data-stu-id="63397-113">Input Type</span></span>

<span data-ttu-id="63397-114">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="63397-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="63397-115">Stratégie de résolution des conflits</span><span class="sxs-lookup"><span data-stu-id="63397-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="63397-116">Les valeurs de différents schémas sont conciliées.</span><span class="sxs-lookup"><span data-stu-id="63397-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="63397-117">Priorité des chemins d’accès (JPEG)</span><span class="sxs-lookup"><span data-stu-id="63397-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="63397-118">Si le fichier est au format JPEG, le gestionnaire utilise le chemin d’accès suivant lors de la lecture ou de l’écriture des données.</span><span class="sxs-lookup"><span data-stu-id="63397-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="63397-119">Commande</span><span class="sxs-lookup"><span data-stu-id="63397-119">Order</span></span> | <span data-ttu-id="63397-120">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="63397-120">Path</span></span>                          | <span data-ttu-id="63397-121">Format de disque</span><span class="sxs-lookup"><span data-stu-id="63397-121">Disk Format</span></span> | <span data-ttu-id="63397-122">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="63397-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="63397-123">1</span><span class="sxs-lookup"><span data-stu-id="63397-123">1</span></span>     | <span data-ttu-id="63397-124">/xmp/MicrosoftPhoto:LensModel</span><span class="sxs-lookup"><span data-stu-id="63397-124">/xmp/MicrosoftPhoto:LensModel</span></span> | <span data-ttu-id="63397-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="63397-125">Unicode</span></span>     | <span data-ttu-id="63397-126">Oui</span><span class="sxs-lookup"><span data-stu-id="63397-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="63397-127">Priorité des chemins d’accès (TIFF)</span><span class="sxs-lookup"><span data-stu-id="63397-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="63397-128">Si le fichier est au format TIFF, le gestionnaire utilise l’ordre de priorité suivant lors de la lecture ou de l’écriture des données.</span><span class="sxs-lookup"><span data-stu-id="63397-128">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="63397-129">Commande</span><span class="sxs-lookup"><span data-stu-id="63397-129">Order</span></span> | <span data-ttu-id="63397-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="63397-130">Path</span></span>                              | <span data-ttu-id="63397-131">Format de disque</span><span class="sxs-lookup"><span data-stu-id="63397-131">Disk Format</span></span> | <span data-ttu-id="63397-132">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="63397-132">Required</span></span> |
|-------|-----------------------------------|-------------|----------|
| <span data-ttu-id="63397-133">1</span><span class="sxs-lookup"><span data-stu-id="63397-133">1</span></span>     | <span data-ttu-id="63397-134">/ifd/xmp/MicrosoftPhoto:LensModel</span><span class="sxs-lookup"><span data-stu-id="63397-134">/ifd/xmp/MicrosoftPhoto:LensModel</span></span> | <span data-ttu-id="63397-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="63397-135">Unicode</span></span>     | <span data-ttu-id="63397-136">Oui</span><span class="sxs-lookup"><span data-stu-id="63397-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="63397-137">Notes</span><span class="sxs-lookup"><span data-stu-id="63397-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="63397-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="63397-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63397-139">System. photo. LensModel</span><span class="sxs-lookup"><span data-stu-id="63397-139">System.Photo.LensModel</span></span>](../properties/props-system-photo-lensmodel.md)
</dt> </dl>

 

 
