---
description: Spécifie le niveau de volume maximal souhaité pour le contenu audio de sortie.
ms.assetid: 231b7296-ca80-4918-bae6-674b976db24c
title: MFPKEY_WMADRC_PEAKTARGET, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c40fa68e2b580c5d3e8550d6e46c9f6b9fe4bfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517003"
---
# <a name="mfpkey_wmadrc_peaktarget-property"></a><span data-ttu-id="98e5e-103">MFPKEY \_ WMADRC \_ PEAKTARGET, propriété</span><span class="sxs-lookup"><span data-stu-id="98e5e-103">MFPKEY\_WMADRC\_PEAKTARGET Property</span></span>

<span data-ttu-id="98e5e-104">Spécifie le niveau de volume maximal souhaité pour le contenu audio de sortie.</span><span class="sxs-lookup"><span data-stu-id="98e5e-104">Specifies the desired maximum volume level of output audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="98e5e-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="98e5e-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="98e5e-106">\_wszWMADRCPeakTarget g</span><span class="sxs-lookup"><span data-stu-id="98e5e-106">g\_wszWMADRCPeakTarget</span></span>

## <a name="data-type"></a><span data-ttu-id="98e5e-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="98e5e-107">Data Type</span></span>

<span data-ttu-id="98e5e-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="98e5e-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="98e5e-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="98e5e-109">Default Value</span></span>

<span data-ttu-id="98e5e-110">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="98e5e-110">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="98e5e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="98e5e-111">Remarks</span></span>

<span data-ttu-id="98e5e-112">Vous pouvez définir cette valeur sur le décodeur à des fins de contrôle de plage dynamique, mais il n’aura d’effet que si la propriété [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) est définie.</span><span class="sxs-lookup"><span data-stu-id="98e5e-112">You can set this value on the decoder for the purpose of dynamic range control, but it will have an effect only if the [MFPKEY\_WMADEC\_DRCMODE](mfpkey-wmadec-drcmodeproperty.md) property is set.</span></span>

<span data-ttu-id="98e5e-113">Si vous demandez un contrôle de plage dynamique à partir du décodeur lorsque cette propriété n’est pas définie, le codec calcule une valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="98e5e-113">If you request dynamic range control from the decoder when this property is not set, the codec will compute a default value.</span></span>

<span data-ttu-id="98e5e-114">Utilisez les propriétés [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) et [MFPKEY \_ WMADRC \_ ](mfpkey-wmadrc-peakrefproperty.md) PEAKREF pour calculer les valeurs appropriées pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="98e5e-114">Use the [MFPKEY\_WMADRC\_AVGREF](mfpkey-wmadrc-avgrefproperty.md) and [MFPKEY\_WMADRC\_PEAKREF](mfpkey-wmadrc-peakrefproperty.md) properties to compute appropriate values for this property.</span></span>

<span data-ttu-id="98e5e-115">Pour plus d’informations sur le contrôle de plage dynamique, consultez l’article Web [Windows Media Audio fonctionnalités du codec professionnel](/previous-versions/ms867218(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="98e5e-115">For more information on dynamic range control, see the web article [Windows Media Audio Professional Codec Features](/previous-versions/ms867218(v=msdn.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="98e5e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98e5e-116">Requirements</span></span>



| <span data-ttu-id="98e5e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98e5e-117">Requirement</span></span> | <span data-ttu-id="98e5e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="98e5e-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98e5e-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98e5e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="98e5e-120">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98e5e-120">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="98e5e-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98e5e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="98e5e-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98e5e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="98e5e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="98e5e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="98e5e-124"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="98e5e-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98e5e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98e5e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98e5e-126">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="98e5e-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
