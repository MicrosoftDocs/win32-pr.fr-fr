---
description: Spécifie la méthode à utiliser pour la correspondance de mouvement.
ms.assetid: 75bbc189-3092-4813-9f45-54e8e48b05cd
title: MFPKEY_MOTIONMATCHMETHOD, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09496e714633dd394f55122b7461f29a2daa3656
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951664"
---
# <a name="mfpkey_motionmatchmethod-property"></a><span data-ttu-id="323f1-103">MFPKEY \_ propriété MOTIONMATCHMETHOD</span><span class="sxs-lookup"><span data-stu-id="323f1-103">MFPKEY\_MOTIONMATCHMETHOD Property</span></span>

<span data-ttu-id="323f1-104">Spécifie la méthode à utiliser pour la correspondance de mouvement.</span><span class="sxs-lookup"><span data-stu-id="323f1-104">Specifies the method to use for motion matching.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="323f1-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="323f1-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="323f1-106">\_wszWMVCMotionMatchMethod g</span><span class="sxs-lookup"><span data-stu-id="323f1-106">g\_wszWMVCMotionMatchMethod</span></span>

## <a name="data-type"></a><span data-ttu-id="323f1-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="323f1-107">Data Type</span></span>

<span data-ttu-id="323f1-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="323f1-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="323f1-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="323f1-109">Default Value</span></span>

<span data-ttu-id="323f1-110">0</span><span class="sxs-lookup"><span data-stu-id="323f1-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="323f1-111">Notes</span><span class="sxs-lookup"><span data-stu-id="323f1-111">Remarks</span></span>

<span data-ttu-id="323f1-112">Cette propriété peut être définie sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="323f1-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="323f1-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="323f1-113">Value</span></span> | <span data-ttu-id="323f1-114">Méthode utilisée</span><span class="sxs-lookup"><span data-stu-id="323f1-114">Method used</span></span>                       |
|-------|-----------------------------------|
| <span data-ttu-id="323f1-115">0</span><span class="sxs-lookup"><span data-stu-id="323f1-115">0</span></span>     | <span data-ttu-id="323f1-116">somme des différences absolues (SAD)</span><span class="sxs-lookup"><span data-stu-id="323f1-116">sum of absolute differences (SAD)</span></span> |
| <span data-ttu-id="323f1-117">1</span><span class="sxs-lookup"><span data-stu-id="323f1-117">1</span></span>     | <span data-ttu-id="323f1-118">Hadamard</span><span class="sxs-lookup"><span data-stu-id="323f1-118">Hadamard</span></span>                          |
| <span data-ttu-id="323f1-119">-1</span><span class="sxs-lookup"><span data-stu-id="323f1-119">-1</span></span>    | <span data-ttu-id="323f1-120">Bloc macro-adaptative.</span><span class="sxs-lookup"><span data-stu-id="323f1-120">Macroblock-adaptive.</span></span>              |



 

<span data-ttu-id="323f1-121">La somme des différences absolues (SAD) est une méthode plus rapide mais moins précise que la transformation Hadarmard.</span><span class="sxs-lookup"><span data-stu-id="323f1-121">The sum of absolute differences (SAD) is a faster but less accurate method than the Hadamard transform.</span></span> <span data-ttu-id="323f1-122">La transformation Hadarmard est plus précise, mais exigeante en calcul.</span><span class="sxs-lookup"><span data-stu-id="323f1-122">The Hadamard transform is more accurate but computationally intensive.</span></span> <span data-ttu-id="323f1-123">Le mode bloc macro-Adaptive constitue un compromis raisonnable entre les deux méthodes en choisissant dynamiquement entre les deux transformations, en sélectionnant la transformation Hadarmard uniquement lorsque cela est approprié.</span><span class="sxs-lookup"><span data-stu-id="323f1-123">The macroblock-adaptive mode provides a reasonable compromise between the two methods by dynamically choosing between the two transforms, selecting the Hadamard transform only when appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="323f1-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="323f1-124">Requirements</span></span>



| <span data-ttu-id="323f1-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="323f1-125">Requirement</span></span> | <span data-ttu-id="323f1-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="323f1-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="323f1-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="323f1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="323f1-128">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="323f1-128">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="323f1-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="323f1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="323f1-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="323f1-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="323f1-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="323f1-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="323f1-132"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="323f1-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="323f1-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="323f1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="323f1-134">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="323f1-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




