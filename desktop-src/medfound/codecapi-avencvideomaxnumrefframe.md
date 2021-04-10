---
description: Spécifie le nombre maximal de frames de référence pris en charge par l’encodeur.
ms.assetid: 023FD791-BD43-41F6-95D0-8BE800F51579
title: CODECAPI_AVEncVideoMaxNumRefFrame, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e8f5a7794410012bd1a025e794e1fd23f4b332
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104116046"
---
# <a name="codecapi_avencvideomaxnumrefframe-property"></a><span data-ttu-id="1b58d-103">CODECAPI \_ propriété AVEncVideoMaxNumRefFrame</span><span class="sxs-lookup"><span data-stu-id="1b58d-103">CODECAPI\_AVEncVideoMaxNumRefFrame property</span></span>

<span data-ttu-id="1b58d-104">Spécifie le nombre maximal de frames de référence pris en charge par l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="1b58d-104">Specifies the maximum reference frames supported by the encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="1b58d-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="1b58d-105">Data type</span></span>

<span data-ttu-id="1b58d-106">**ULong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="1b58d-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="1b58d-107">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="1b58d-107">Property GUID</span></span>

<span data-ttu-id="1b58d-108">**CODECAPI \_ AVEncVideoMaxNumRefFrame**</span><span class="sxs-lookup"><span data-stu-id="1b58d-108">**CODECAPI\_AVEncVideoMaxNumRefFrame**</span></span>

## <a name="remarks"></a><span data-ttu-id="1b58d-109">Notes</span><span class="sxs-lookup"><span data-stu-id="1b58d-109">Remarks</span></span>

<span data-ttu-id="1b58d-110">Pour H. 264, cela est mappé aux images du paramètre de séquence Set **Max \_ num \_ Ref \_ frames** comme défini dans la spécification H. 264.</span><span class="sxs-lookup"><span data-stu-id="1b58d-110">For H.264, this maps to the Sequence Parameter Set variable **max\_num\_ref\_frames** as defined in H.264 specification.</span></span>

<span data-ttu-id="1b58d-111">**Encodeurs H. 264/AVC :**</span><span class="sxs-lookup"><span data-stu-id="1b58d-111">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="1b58d-112">Les encodeurs peuvent utiliser moins de frames de référence pour respecter le niveau spécifié dans le flux binaire.</span><span class="sxs-lookup"><span data-stu-id="1b58d-112">Encoders may use fewer reference frames in order to obey the level specified in the bitstream.</span></span>

<span data-ttu-id="1b58d-113">Les encodeurs prennent en charge [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)et [**GetParameterRangee**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="1b58d-113">Encoders shall support [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRangee**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="1b58d-114">Il s’agit d’une propriété statique, ce qui signifie qu’elle ne peut être définie que avant le démarrage de la session d’encodage.</span><span class="sxs-lookup"><span data-stu-id="1b58d-114">This is a static property meaning that it can only be set before the encoding session starts.</span></span>

<span data-ttu-id="1b58d-115">La valeur par défaut recommandée est 2.</span><span class="sxs-lookup"><span data-stu-id="1b58d-115">Recommended default value is 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b58d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b58d-116">Requirements</span></span>



| <span data-ttu-id="1b58d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b58d-117">Requirement</span></span> | <span data-ttu-id="1b58d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b58d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b58d-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b58d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1b58d-120">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1b58d-120">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="1b58d-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b58d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1b58d-122">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1b58d-122">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="1b58d-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b58d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b58d-124"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b58d-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b58d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b58d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b58d-126">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1b58d-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

