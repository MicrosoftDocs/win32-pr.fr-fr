---
description: Spécifie le nombre maximal de QP pris en charge par l’encodeur.
ms.assetid: 2C02F82B-E645-4C5B-9526-5E130A6E2F67
title: CODECAPI_AVEncVideoMaxQP, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9bcf23866da5530d2edc1203be359071e5e33e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516596"
---
# <a name="codecapi_avencvideomaxqp-property"></a><span data-ttu-id="28e45-103">CODECAPI \_ propriété AVEncVideoMaxQP</span><span class="sxs-lookup"><span data-stu-id="28e45-103">CODECAPI\_AVEncVideoMaxQP property</span></span>

<span data-ttu-id="28e45-104">Spécifie le nombre maximal de QP pris en charge par l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="28e45-104">Specifies the maximum QP supported by the encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="28e45-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="28e45-105">Data type</span></span>

<span data-ttu-id="28e45-106">**ULong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="28e45-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="28e45-107">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="28e45-107">Property GUID</span></span>

<span data-ttu-id="28e45-108">**CODECAPI \_ AVEncVideoMaxQP**</span><span class="sxs-lookup"><span data-stu-id="28e45-108">**CODECAPI\_AVEncVideoMaxQP**</span></span>

## <a name="remarks"></a><span data-ttu-id="28e45-109">Notes</span><span class="sxs-lookup"><span data-stu-id="28e45-109">Remarks</span></span>

<span data-ttu-id="28e45-110">**Encodeurs H. 264/AVC :**</span><span class="sxs-lookup"><span data-stu-id="28e45-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="28e45-111">L’encodeur doit prendre en charge [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)et [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="28e45-111">The encoder shall support [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="28e45-112">Il s’agit d’une propriété statique, ce qui signifie qu’elle ne peut être définie que avant le démarrage de la session d’encodage.</span><span class="sxs-lookup"><span data-stu-id="28e45-112">This is a static property meaning that it can only be set before the encoding session starts.</span></span>

<span data-ttu-id="28e45-113">La valeur par défaut est le nombre maximal de QP autorisé par la norme de codage correspondante.</span><span class="sxs-lookup"><span data-stu-id="28e45-113">Default value shall be the max QP allowed by the corresponding coding standard.</span></span> <span data-ttu-id="28e45-114">Par exemple, les encodeurs H. 264 doivent avoir une valeur par défaut de 51.</span><span class="sxs-lookup"><span data-stu-id="28e45-114">For example, H.264 encoders shall have a default value of 51.</span></span>

## <a name="requirements"></a><span data-ttu-id="28e45-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28e45-115">Requirements</span></span>



| <span data-ttu-id="28e45-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28e45-116">Requirement</span></span> | <span data-ttu-id="28e45-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="28e45-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="28e45-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28e45-118">Minimum supported client</span></span><br/> | <span data-ttu-id="28e45-119">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="28e45-119">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="28e45-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28e45-120">Minimum supported server</span></span><br/> | <span data-ttu-id="28e45-121">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="28e45-121">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="28e45-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="28e45-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="28e45-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="28e45-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28e45-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28e45-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28e45-125">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="28e45-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="28e45-126">CODECAPI \_ AVEncVideoMinQP</span><span class="sxs-lookup"><span data-stu-id="28e45-126">CODECAPI\_AVEncVideoMinQP</span></span>](codecapi-avencvideominqp.md)
</dt> </dl>

 

