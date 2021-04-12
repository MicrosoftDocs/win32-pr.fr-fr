---
description: Spécifie la complexité de l’algorithme d’encodeur.
ms.assetid: 1537e98b-d7ed-49e6-aa25-8f2f124c88eb
title: MFPKEY_COMPLEXITY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05325f3ab0cc1173924df9f6c551bf10fd0d5481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202365"
---
# <a name="mfpkey_complexity-property"></a><span data-ttu-id="e2e1f-103">\_Propriété de complexité MFPKEY</span><span class="sxs-lookup"><span data-stu-id="e2e1f-103">MFPKEY\_COMPLEXITY Property</span></span>

<span data-ttu-id="e2e1f-104">\[[**MFPKEY \_ La complexité**](mfpkey-complexityexproperty.md) est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="e2e1f-104">\[[**MFPKEY\_COMPLEXITY**](mfpkey-complexityexproperty.md) is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e2e1f-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e2e1f-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="e2e1f-106">Utilisez plutôt **MFPKEY \_ COMPLEXITYEX**.\]</span><span class="sxs-lookup"><span data-stu-id="e2e1f-106">Instead, use **MFPKEY\_COMPLEXITYEX**.\]</span></span>

<span data-ttu-id="e2e1f-107">Spécifie la complexité de l’algorithme d’encodeur.</span><span class="sxs-lookup"><span data-stu-id="e2e1f-107">Specifies the encoder algorithm complexity.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e2e1f-108">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="e2e1f-108">Constant for IPropertyBag</span></span>

<span data-ttu-id="e2e1f-109">\_wszWMVCComplexityMode g</span><span class="sxs-lookup"><span data-stu-id="e2e1f-109">g\_wszWMVCComplexityMode</span></span>

## <a name="data-type"></a><span data-ttu-id="e2e1f-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="e2e1f-110">Data Type</span></span>

<span data-ttu-id="e2e1f-111">VT \_</span><span class="sxs-lookup"><span data-stu-id="e2e1f-111">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="e2e1f-112">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="e2e1f-112">Default Value</span></span>

<span data-ttu-id="e2e1f-113">La valeur par défaut dépend de la version de l’encodeur vidéo, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e2e1f-113">The default value depends on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="e2e1f-114">Version de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="e2e1f-114">Encoder version</span></span>                 | <span data-ttu-id="e2e1f-115">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="e2e1f-115">Default value</span></span> |
|---------------------------------|---------------|
| <span data-ttu-id="e2e1f-116">Encodeur Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="e2e1f-116">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="e2e1f-117">3</span><span class="sxs-lookup"><span data-stu-id="e2e1f-117">3</span></span>             |
| <span data-ttu-id="e2e1f-118">Windows Media Video encodeur 7/8</span><span class="sxs-lookup"><span data-stu-id="e2e1f-118">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="e2e1f-119">1</span><span class="sxs-lookup"><span data-stu-id="e2e1f-119">1</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="e2e1f-120">Notes</span><span class="sxs-lookup"><span data-stu-id="e2e1f-120">Remarks</span></span>

<span data-ttu-id="e2e1f-121">Cette valeur entière est comprise entre 0 et 3.</span><span class="sxs-lookup"><span data-stu-id="e2e1f-121">This integer value ranges from 0 to 3.</span></span> <span data-ttu-id="e2e1f-122">Des valeurs inférieures obligent le codec à utiliser des algorithmes d’encodage moins compliqués.</span><span class="sxs-lookup"><span data-stu-id="e2e1f-122">Lower values cause the codec to use less complicated encoding algorithms.</span></span> <span data-ttu-id="e2e1f-123">Bien que les algorithmes plus simples produisent une sortie de qualité inférieure, le processus d’encodage est plus rapide et nécessite moins de puissance de traitement.</span><span class="sxs-lookup"><span data-stu-id="e2e1f-123">Although the simpler algorithms produce lower-quality output, the encoding process is faster and requires less processing power.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2e1f-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2e1f-124">Requirements</span></span>



| <span data-ttu-id="e2e1f-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2e1f-125">Requirement</span></span> | <span data-ttu-id="e2e1f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2e1f-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2e1f-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2e1f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e2e1f-128">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2e1f-128">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e2e1f-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2e1f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e2e1f-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2e1f-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e2e1f-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2e1f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2e1f-132"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2e1f-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2e1f-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2e1f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2e1f-134">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2e1f-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




