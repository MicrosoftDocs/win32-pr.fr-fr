---
description: Spécifie la qualité de la sortie.
ms.assetid: 7b45633b-7f1c-4951-a462-ad6240b9ca31
title: MFPKEY_WMRESAMP_FILTERQUALITY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4027d4bc3c0306240986cf632e171fa9a59ed18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201879"
---
# <a name="mfpkey_wmresamp_filterquality-property"></a><span data-ttu-id="1fa67-103">MFPKEY \_ WMRESAMP \_ FILTERQUALITY, propriété</span><span class="sxs-lookup"><span data-stu-id="1fa67-103">MFPKEY\_WMRESAMP\_FILTERQUALITY Property</span></span>

<span data-ttu-id="1fa67-104">Spécifie la qualité de la sortie.</span><span class="sxs-lookup"><span data-stu-id="1fa67-104">Specifies the quality of the output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1fa67-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="1fa67-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="1fa67-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="1fa67-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="1fa67-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="1fa67-107">Data Type</span></span>

<span data-ttu-id="1fa67-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="1fa67-108">VT\_I4</span></span>

## <a name="applies-to"></a><span data-ttu-id="1fa67-109">S'applique à</span><span class="sxs-lookup"><span data-stu-id="1fa67-109">Applies To</span></span>

-   [<span data-ttu-id="1fa67-110">Modèle de rééchantillonnage audio DSP</span><span class="sxs-lookup"><span data-stu-id="1fa67-110">Audio Resampler DSP</span></span>](audioresampler.md)

## <a name="remarks"></a><span data-ttu-id="1fa67-111">Notes</span><span class="sxs-lookup"><span data-stu-id="1fa67-111">Remarks</span></span>

<span data-ttu-id="1fa67-112">La plage valide de cette propriété est comprise entre 1 et 60 inclus.</span><span class="sxs-lookup"><span data-stu-id="1fa67-112">The valid range of this property is 1 to 60, inclusive.</span></span> <span data-ttu-id="1fa67-113">Des valeurs plus élevées produisent une sortie de qualité supérieure, mais introduisent plus de latence.</span><span class="sxs-lookup"><span data-stu-id="1fa67-113">Higher values produce higher-quality output, but introduce more latency.</span></span> <span data-ttu-id="1fa67-114">La valeur 1 est fondamentalement identique à l’interpolation linéaire.</span><span class="sxs-lookup"><span data-stu-id="1fa67-114">A value of 1 is essentially the same as linear interpolation.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fa67-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1fa67-115">Requirements</span></span>



| <span data-ttu-id="1fa67-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1fa67-116">Requirement</span></span> | <span data-ttu-id="1fa67-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fa67-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fa67-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fa67-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1fa67-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1fa67-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1fa67-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fa67-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1fa67-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1fa67-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1fa67-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="1fa67-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fa67-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fa67-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fa67-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fa67-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fa67-125">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1fa67-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
