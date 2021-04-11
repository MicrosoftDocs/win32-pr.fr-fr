---
description: Spécifie la complexité de l’algorithme d’encodeur.
ms.assetid: abfc84d5-954f-4524-b3cb-5c5b9cfc7fa0
title: MFPKEY_COMPLEXITYEX, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34b935f41ce14a77a135d0bbc8ad6dec2933b570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202366"
---
# <a name="mfpkey_complexityex-property"></a><span data-ttu-id="fee56-103">MFPKEY \_ propriété COMPLEXITYEX</span><span class="sxs-lookup"><span data-stu-id="fee56-103">MFPKEY\_COMPLEXITYEX Property</span></span>

<span data-ttu-id="fee56-104">Spécifie la complexité de l’algorithme d’encodeur.</span><span class="sxs-lookup"><span data-stu-id="fee56-104">Specifies the encoder algorithm complexity.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="fee56-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="fee56-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="fee56-106">\_wszWMVCComplexityEx g</span><span class="sxs-lookup"><span data-stu-id="fee56-106">g\_wszWMVCComplexityEx</span></span>

## <a name="data-type"></a><span data-ttu-id="fee56-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="fee56-107">Data Type</span></span>

<span data-ttu-id="fee56-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="fee56-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="fee56-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="fee56-109">Default Value</span></span>

<span data-ttu-id="fee56-110">La valeur par défaut dépend de la version de l’encodeur vidéo, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fee56-110">The default value depends on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="fee56-111">Version de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="fee56-111">Encoder version</span></span>                 | <span data-ttu-id="fee56-112">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="fee56-112">Default value</span></span> |
|---------------------------------|---------------|
| <span data-ttu-id="fee56-113">Encodeur Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="fee56-113">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="fee56-114">3</span><span class="sxs-lookup"><span data-stu-id="fee56-114">3</span></span>             |
| <span data-ttu-id="fee56-115">Windows Media Video encodeur 7/8</span><span class="sxs-lookup"><span data-stu-id="fee56-115">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="fee56-116">1</span><span class="sxs-lookup"><span data-stu-id="fee56-116">1</span></span>             |



 

## <a name="possible-values"></a><span data-ttu-id="fee56-117">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="fee56-117">Possible Values</span></span>

<span data-ttu-id="fee56-118">Les valeurs possibles dépendent de la version de l’encodeur vidéo, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fee56-118">The possible values depend on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="fee56-119">Version de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="fee56-119">Encoder version</span></span>                 | <span data-ttu-id="fee56-120">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="fee56-120">Possible values</span></span>  |
|---------------------------------|------------------|
| <span data-ttu-id="fee56-121">Encodeur Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="fee56-121">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="fee56-122">0, 1, 2, 3, 4, 5</span><span class="sxs-lookup"><span data-stu-id="fee56-122">0, 1, 2, 3, 4, 5</span></span> |
| <span data-ttu-id="fee56-123">Windows Media Video encodeur 7/8</span><span class="sxs-lookup"><span data-stu-id="fee56-123">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="fee56-124">0, 1</span><span class="sxs-lookup"><span data-stu-id="fee56-124">0, 1</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="fee56-125">Notes</span><span class="sxs-lookup"><span data-stu-id="fee56-125">Remarks</span></span>

<span data-ttu-id="fee56-126">Des valeurs inférieures obligent le codec à utiliser des algorithmes d’encodage moins compliqués.</span><span class="sxs-lookup"><span data-stu-id="fee56-126">Lower values cause the codec to use less complicated encoding algorithms.</span></span> <span data-ttu-id="fee56-127">Bien que les algorithmes plus simples produisent une sortie de qualité inférieure, le processus d’encodage est plus rapide et nécessite moins de puissance de traitement.</span><span class="sxs-lookup"><span data-stu-id="fee56-127">Although the simpler algorithms produce lower-quality output, the encoding process is faster and requires less processing power.</span></span> <span data-ttu-id="fee56-128">Cela peut être important lorsque vous encodez du contenu à partir d’une source Live, car l’encodeur doit traiter les entrées suffisamment rapidement pour suivre la source.</span><span class="sxs-lookup"><span data-stu-id="fee56-128">This can be important when encoding content from a live source because the encoder must process inputs fast enough to keep up with the source.</span></span>

<span data-ttu-id="fee56-129">Toute valeur assignée à cette propriété sera ignorée si la propriété [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) est définie sur 1.</span><span class="sxs-lookup"><span data-stu-id="fee56-129">Any value assigned to this property will be ignored if the [MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) property is set to 1.</span></span> <span data-ttu-id="fee56-130">Dans ce cas, MFPKEY \_ COMPLEXITYEX a automatiquement la valeur 3.</span><span class="sxs-lookup"><span data-stu-id="fee56-130">In that case, MFPKEY\_COMPLEXITYEX is automatically set to 3.</span></span>

## <a name="requirements"></a><span data-ttu-id="fee56-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fee56-131">Requirements</span></span>



| <span data-ttu-id="fee56-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fee56-132">Requirement</span></span> | <span data-ttu-id="fee56-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="fee56-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fee56-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fee56-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fee56-135">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fee56-135">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="fee56-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fee56-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fee56-137">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fee56-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fee56-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="fee56-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="fee56-139"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fee56-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fee56-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fee56-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fee56-141">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fee56-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




