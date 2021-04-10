---
description: Spécifie le mode de contrôle de plage dynamique qui sera utilisé par le décodeur audio.
ms.assetid: 0dbe0c40-39ac-4c1b-9da2-9b142b5bb0eb
title: MFPKEY_WMADEC_DRCMODE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb612e08ff8bd799ec94faae68763f04db8ad052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201883"
---
# <a name="mfpkey_wmadec_drcmode-property"></a><span data-ttu-id="dc273-103">MFPKEY \_ WMADEC \_ DRCMODE, propriété</span><span class="sxs-lookup"><span data-stu-id="dc273-103">MFPKEY\_WMADEC\_DRCMODE Property</span></span>

<span data-ttu-id="dc273-104">Spécifie le mode de contrôle de plage dynamique qui sera utilisé par le décodeur audio.</span><span class="sxs-lookup"><span data-stu-id="dc273-104">Specifies the dynamic range control mode that the audio decoder will use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="dc273-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="dc273-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="dc273-106">\_wszWMACDRCSetting g</span><span class="sxs-lookup"><span data-stu-id="dc273-106">g\_wszWMACDRCSetting</span></span>

## <a name="data-type"></a><span data-ttu-id="dc273-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="dc273-107">Data Type</span></span>

<span data-ttu-id="dc273-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="dc273-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="dc273-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="dc273-109">Default Value</span></span>

<span data-ttu-id="dc273-110">0</span><span class="sxs-lookup"><span data-stu-id="dc273-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="dc273-111">Notes</span><span class="sxs-lookup"><span data-stu-id="dc273-111">Remarks</span></span>

<span data-ttu-id="dc273-112">Cette valeur entière est comprise entre 0 et 2.</span><span class="sxs-lookup"><span data-stu-id="dc273-112">This integer value ranges from 0 to 2.</span></span> <span data-ttu-id="dc273-113">Plus la valeur est élevée, plus la plage dynamique de la sortie audio non compressée est petite.</span><span class="sxs-lookup"><span data-stu-id="dc273-113">The greater the value, the smaller the dynamic range of the uncompressed audio output.</span></span> <span data-ttu-id="dc273-114">La valeur 0 indique au codec qu’il n’exécute aucun contrôle de plage dynamique, autrement dit, le codec ne modifiera pas la plage dynamique inhérente du contenu encodé.</span><span class="sxs-lookup"><span data-stu-id="dc273-114">A value of 0 signals the codec to perform no dynamic range control, that is, the codec will not alter the inherent dynamic range of the encoded content.</span></span>

<span data-ttu-id="dc273-115">Si cette valeur est définie sur 1 ou 2, le codec utilise les propriétés suivantes pour déterminer le contrôle de plage dynamique nécessaire :</span><span class="sxs-lookup"><span data-stu-id="dc273-115">If this value is set to 1 or 2, the codec will use the following properties to determine the needed dynamic range control:</span></span>

-   [<span data-ttu-id="dc273-116">MFPKEY \_ WMADRC \_ AVGREF</span><span class="sxs-lookup"><span data-stu-id="dc273-116">MFPKEY\_WMADRC\_AVGREF</span></span>](mfpkey-wmadrc-avgrefproperty.md)
-   [<span data-ttu-id="dc273-117">MFPKEY \_ WMADRC \_ PEAKREF</span><span class="sxs-lookup"><span data-stu-id="dc273-117">MFPKEY\_WMADRC\_PEAKREF</span></span>](mfpkey-wmadrc-peakrefproperty.md)
-   [<span data-ttu-id="dc273-118">MFPKEY \_ WMADRC \_ AVGTARGET</span><span class="sxs-lookup"><span data-stu-id="dc273-118">MFPKEY\_WMADRC\_AVGTARGET</span></span>](mfpkey-wmadrc-avgtargetproperty.md)
-   [<span data-ttu-id="dc273-119">MFPKEY \_ WMADRC \_ PEAKTARGET</span><span class="sxs-lookup"><span data-stu-id="dc273-119">MFPKEY\_WMADRC\_PEAKTARGET</span></span>](mfpkey-wmadrc-peaktargetproperty.md)

<span data-ttu-id="dc273-120">Si vous ne fournissez pas de valeurs cibles, le codec fournira sa propre valeur.</span><span class="sxs-lookup"><span data-stu-id="dc273-120">If you do not provide target values, the codec will provide its own.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc273-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc273-121">Requirements</span></span>



| <span data-ttu-id="dc273-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc273-122">Requirement</span></span> | <span data-ttu-id="dc273-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc273-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc273-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc273-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dc273-125">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc273-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dc273-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc273-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dc273-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc273-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dc273-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc273-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc273-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc273-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc273-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc273-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc273-131">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dc273-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




