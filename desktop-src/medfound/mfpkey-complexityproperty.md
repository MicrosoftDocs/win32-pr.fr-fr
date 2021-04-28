---
description: 'Propriété MFPKEY_COMPLEXITY : spécifie la complexité de l’algorithme de l’encodeur.'
ms.assetid: 1537e98b-d7ed-49e6-aa25-8f2f124c88eb
title: MFPKEY_COMPLEXITY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042e3158b43efb5a4a82542f000d137fa0c195e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092937"
---
# <a name="mfpkey_complexity-property"></a><span data-ttu-id="dd7dd-103">\_Propriété de complexité MFPKEY</span><span class="sxs-lookup"><span data-stu-id="dd7dd-103">MFPKEY\_COMPLEXITY Property</span></span>

<span data-ttu-id="dd7dd-104">\[[**MFPKEY \_ La complexité**](mfpkey-complexityexproperty.md) est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="dd7dd-104">\[[**MFPKEY\_COMPLEXITY**](mfpkey-complexityexproperty.md) is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dd7dd-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="dd7dd-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="dd7dd-106">Utilisez plutôt **MFPKEY \_ COMPLEXITYEX**.\]</span><span class="sxs-lookup"><span data-stu-id="dd7dd-106">Instead, use **MFPKEY\_COMPLEXITYEX**.\]</span></span>

<span data-ttu-id="dd7dd-107">Spécifie la complexité de l’algorithme d’encodeur.</span><span class="sxs-lookup"><span data-stu-id="dd7dd-107">Specifies the encoder algorithm complexity.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="dd7dd-108">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="dd7dd-108">Constant for IPropertyBag</span></span>

<span data-ttu-id="dd7dd-109">\_wszWMVCComplexityMode g</span><span class="sxs-lookup"><span data-stu-id="dd7dd-109">g\_wszWMVCComplexityMode</span></span>

## <a name="data-type"></a><span data-ttu-id="dd7dd-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="dd7dd-110">Data Type</span></span>

<span data-ttu-id="dd7dd-111">VT \_</span><span class="sxs-lookup"><span data-stu-id="dd7dd-111">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="dd7dd-112">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="dd7dd-112">Default Value</span></span>

<span data-ttu-id="dd7dd-113">La valeur par défaut dépend de la version de l’encodeur vidéo, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="dd7dd-113">The default value depends on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="dd7dd-114">Version de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="dd7dd-114">Encoder version</span></span>                 | <span data-ttu-id="dd7dd-115">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="dd7dd-115">Default value</span></span> |
|---------------------------------|---------------|
| <span data-ttu-id="dd7dd-116">Encodeur Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="dd7dd-116">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="dd7dd-117">3</span><span class="sxs-lookup"><span data-stu-id="dd7dd-117">3</span></span>             |
| <span data-ttu-id="dd7dd-118">Windows Media Video encodeur 7/8</span><span class="sxs-lookup"><span data-stu-id="dd7dd-118">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="dd7dd-119">1</span><span class="sxs-lookup"><span data-stu-id="dd7dd-119">1</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="dd7dd-120">Notes </span><span class="sxs-lookup"><span data-stu-id="dd7dd-120">Remarks</span></span>

<span data-ttu-id="dd7dd-121">Cette valeur entière est comprise entre 0 et 3.</span><span class="sxs-lookup"><span data-stu-id="dd7dd-121">This integer value ranges from 0 to 3.</span></span> <span data-ttu-id="dd7dd-122">Des valeurs inférieures obligent le codec à utiliser des algorithmes d’encodage moins compliqués.</span><span class="sxs-lookup"><span data-stu-id="dd7dd-122">Lower values cause the codec to use less complicated encoding algorithms.</span></span> <span data-ttu-id="dd7dd-123">Bien que les algorithmes plus simples produisent une sortie de qualité inférieure, le processus d’encodage est plus rapide et nécessite moins de puissance de traitement.</span><span class="sxs-lookup"><span data-stu-id="dd7dd-123">Although the simpler algorithms produce lower-quality output, the encoding process is faster and requires less processing power.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd7dd-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd7dd-124">Requirements</span></span>



| <span data-ttu-id="dd7dd-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd7dd-125">Requirement</span></span> | <span data-ttu-id="dd7dd-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd7dd-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd7dd-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd7dd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="dd7dd-128">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd7dd-128">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dd7dd-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd7dd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="dd7dd-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd7dd-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dd7dd-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd7dd-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd7dd-132"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd7dd-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd7dd-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd7dd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd7dd-134">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dd7dd-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




