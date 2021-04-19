---
description: Spécifie la méthode de coût utilisée par le codec pour déterminer le mode bloc macro à utiliser.
ms.assetid: 2ba9b943-0daa-40c1-87ea-2fa647fb7095
title: MFPKEY_MACROBLOCKMODECOSTMETHOD, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 289219300a79c67565891c48cec848851c17bd7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518426"
---
# <a name="mfpkey_macroblockmodecostmethod-property"></a><span data-ttu-id="35b3d-103">MFPKEY \_ propriété MACROBLOCKMODECOSTMETHOD</span><span class="sxs-lookup"><span data-stu-id="35b3d-103">MFPKEY\_MACROBLOCKMODECOSTMETHOD Property</span></span>

<span data-ttu-id="35b3d-104">Spécifie la méthode de coût utilisée par le codec pour déterminer le mode bloc macro à utiliser.</span><span class="sxs-lookup"><span data-stu-id="35b3d-104">Specifies the cost method used by the codec to determine which macroblock mode to use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="35b3d-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="35b3d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="35b3d-106">\_wszWMVCMacroblockModeCostMethod g</span><span class="sxs-lookup"><span data-stu-id="35b3d-106">g\_wszWMVCMacroblockModeCostMethod</span></span>

## <a name="data-type"></a><span data-ttu-id="35b3d-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="35b3d-107">Data Type</span></span>

<span data-ttu-id="35b3d-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="35b3d-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="35b3d-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="35b3d-109">Default Value</span></span>

<span data-ttu-id="35b3d-110">0</span><span class="sxs-lookup"><span data-stu-id="35b3d-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="35b3d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="35b3d-111">Remarks</span></span>

<span data-ttu-id="35b3d-112">Cette propriété peut être définie sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="35b3d-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="35b3d-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="35b3d-113">Value</span></span> | <span data-ttu-id="35b3d-114">Méthode utilisée</span><span class="sxs-lookup"><span data-stu-id="35b3d-114">Method used</span></span>                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35b3d-115">0</span><span class="sxs-lookup"><span data-stu-id="35b3d-115">0</span></span>     | <span data-ttu-id="35b3d-116">SAD/Hadarmard.</span><span class="sxs-lookup"><span data-stu-id="35b3d-116">SAD/Hadamard.</span></span> <span data-ttu-id="35b3d-117">Cette option configure le codec pour qu’il utilise uniquement la distorsion lorsque le calcul du coût.</span><span class="sxs-lookup"><span data-stu-id="35b3d-117">This option configures the codec to use only distortion when computing cost.</span></span>             |
| <span data-ttu-id="35b3d-118">1</span><span class="sxs-lookup"><span data-stu-id="35b3d-118">1</span></span>     | <span data-ttu-id="35b3d-119">Coût des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="35b3d-119">RD cost.</span></span> <span data-ttu-id="35b3d-120">Cette option configure le codec pour tenir compte du taux et de la distorsion lorsque vous calculez le coût.</span><span class="sxs-lookup"><span data-stu-id="35b3d-120">This option configures the codec to account for both rate and distortion when computing cost.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="35b3d-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35b3d-121">Requirements</span></span>



| <span data-ttu-id="35b3d-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35b3d-122">Requirement</span></span> | <span data-ttu-id="35b3d-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="35b3d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35b3d-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35b3d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="35b3d-125">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35b3d-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="35b3d-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35b3d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="35b3d-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35b3d-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="35b3d-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="35b3d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="35b3d-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="35b3d-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35b3d-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35b3d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35b3d-131">MFPKEY \_ MOTIONMATCHMETHOD</span><span class="sxs-lookup"><span data-stu-id="35b3d-131">MFPKEY\_MOTIONMATCHMETHOD</span></span>](mfpkey-motionmatchmethodproperty.md)
</dt> <dt>

[<span data-ttu-id="35b3d-132">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="35b3d-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




