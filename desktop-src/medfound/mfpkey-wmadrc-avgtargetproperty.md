---
description: Spécifie le niveau de volume moyen souhaité de contenu audio de sortie.
ms.assetid: 2e59537f-ee14-4186-b312-297225e91120
title: MFPKEY_WMADRC_AVGTARGET, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4503161ac6e392a50fd7535592b84ea92d6136
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202260"
---
# <a name="mfpkey_wmadrc_avgtarget-property"></a><span data-ttu-id="4fd15-103">MFPKEY \_ WMADRC \_ AVGTARGET, propriété</span><span class="sxs-lookup"><span data-stu-id="4fd15-103">MFPKEY\_WMADRC\_AVGTARGET Property</span></span>

<span data-ttu-id="4fd15-104">Spécifie le niveau de volume moyen souhaité de contenu audio de sortie.</span><span class="sxs-lookup"><span data-stu-id="4fd15-104">Specifies the desired average volume level of output audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="4fd15-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="4fd15-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="4fd15-106">\_wszWMADRCAverageTarget g</span><span class="sxs-lookup"><span data-stu-id="4fd15-106">g\_wszWMADRCAverageTarget</span></span>

## <a name="data-type"></a><span data-ttu-id="4fd15-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="4fd15-107">Data Type</span></span>

<span data-ttu-id="4fd15-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="4fd15-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="4fd15-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="4fd15-109">Default Value</span></span>

<span data-ttu-id="4fd15-110">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="4fd15-110">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fd15-111">Notes</span><span class="sxs-lookup"><span data-stu-id="4fd15-111">Remarks</span></span>

<span data-ttu-id="4fd15-112">Vous pouvez définir cette valeur sur le décodeur à des fins de contrôle de plage dynamique, mais il n’aura d’effet que si la propriété [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) est définie.</span><span class="sxs-lookup"><span data-stu-id="4fd15-112">You can set this value on the decoder for the purpose of dynamic range control, but it will have an effect only if the [MFPKEY\_WMADEC\_DRCMODE](mfpkey-wmadec-drcmodeproperty.md) property is set.</span></span>

> [!Note]  
> <span data-ttu-id="4fd15-113">La définition de la valeur cible moyenne n’est pas recommandée.</span><span class="sxs-lookup"><span data-stu-id="4fd15-113">Setting the average target value is not recommended.</span></span> <span data-ttu-id="4fd15-114">L’ajustement de la valeur moyenne n’affecte pas la différence entre les sons forts et logiciels.</span><span class="sxs-lookup"><span data-stu-id="4fd15-114">Adjusting the average value does not affect the difference between loud and soft sounds.</span></span> <span data-ttu-id="4fd15-115">Au lieu de cela, il réduit ou augmente le volume moyen total, ce qui peut entraîner une déformation indésirable pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="4fd15-115">Instead, it cuts or boosts the overall average volume which may cause undesirable distortion during playback.</span></span>

 

<span data-ttu-id="4fd15-116">Si vous demandez un contrôle de plage dynamique à partir du décodeur lorsque cette propriété n’est pas définie, le codec calcule une valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="4fd15-116">If you request dynamic range control from the decoder when this property is not set, the codec will compute a default value.</span></span>

<span data-ttu-id="4fd15-117">Utilisez les propriétés [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) et [MFPKEY \_ WMADRC \_ ](mfpkey-wmadrc-peakrefproperty.md) PEAKREF pour calculer les valeurs appropriées pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="4fd15-117">Use the [MFPKEY\_WMADRC\_AVGREF](mfpkey-wmadrc-avgrefproperty.md) and [MFPKEY\_WMADRC\_PEAKREF](mfpkey-wmadrc-peakrefproperty.md) properties to compute appropriate values for this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fd15-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4fd15-118">Requirements</span></span>



| <span data-ttu-id="4fd15-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4fd15-119">Requirement</span></span> | <span data-ttu-id="4fd15-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="4fd15-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fd15-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4fd15-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4fd15-122">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4fd15-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4fd15-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4fd15-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4fd15-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4fd15-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4fd15-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="4fd15-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fd15-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fd15-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fd15-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fd15-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fd15-128">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4fd15-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




