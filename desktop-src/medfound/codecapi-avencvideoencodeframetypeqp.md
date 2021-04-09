---
description: Spécifie les types de frames (I, P ou B) auxquels le paramètre de quantification (QP) est appliqué.
ms.assetid: 6331033F-7EEB-41B3-B166-29686D4AADB6
title: CODECAPI_AVEncVideoEncodeFrameTypeQP, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76e68e0cb6cbdc076dbf523f3ae9dfd7b5870f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111859"
---
# <a name="codecapi_avencvideoencodeframetypeqp-property"></a><span data-ttu-id="e4471-103">CODECAPI \_ propriété AVEncVideoEncodeFrameTypeQP</span><span class="sxs-lookup"><span data-stu-id="e4471-103">CODECAPI\_AVEncVideoEncodeFrameTypeQP property</span></span>

<span data-ttu-id="e4471-104">Spécifie les types de frames (I, P ou B) auxquels le paramètre de quantification (QP) est appliqué.</span><span class="sxs-lookup"><span data-stu-id="e4471-104">Specifies the frame types (I, P, or B) that the quantization parameter (QP) is applied to.</span></span>

## <a name="data-type"></a><span data-ttu-id="e4471-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="e4471-105">Data type</span></span>

<span data-ttu-id="e4471-106">**ULONGULONG** (VT \_ UI8)</span><span class="sxs-lookup"><span data-stu-id="e4471-106">**ULONGULONG** (VT\_UI8)</span></span>

## <a name="property-guid"></a><span data-ttu-id="e4471-107">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="e4471-107">Property GUID</span></span>

<span data-ttu-id="e4471-108">**CODECAPI \_ AVEncVideoEncodeFrameTypeQP**</span><span class="sxs-lookup"><span data-stu-id="e4471-108">**CODECAPI\_AVEncVideoEncodeFrameTypeQP**</span></span>

## <a name="remarks"></a><span data-ttu-id="e4471-109">Notes</span><span class="sxs-lookup"><span data-stu-id="e4471-109">Remarks</span></span>

<span data-ttu-id="e4471-110">Pour les encodeurs qui prennent en charge la définition d’un paramètre de quantification (QP) pour différents types de trames (I, P, B), ils exposent cette API en plus de [CODECAPI \_ AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md).</span><span class="sxs-lookup"><span data-stu-id="e4471-110">For encoders which support setting a quantization parameter (QP) for different frame types (I, P, B), they shall expose this API in addition to [CODECAPI\_AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md).</span></span> <span data-ttu-id="e4471-111">Si un encodeur ne prend en charge qu’un seul QP pour tous les types de frame, ils prennent en charge uniquement CODECAPI \_ AVEncVideoEncodeQP.</span><span class="sxs-lookup"><span data-stu-id="e4471-111">If an encoder supports only a single QP for all frame types, they shall support only CODECAPI\_AVEncVideoEncodeQP.</span></span>

<span data-ttu-id="e4471-112">Il s’agit d’une propriété d’encodage dynamique qui signifie qu’une nouvelle valeur peut être définie à tout moment pendant la session d’encodage.</span><span class="sxs-lookup"><span data-stu-id="e4471-112">This is a dynamic encoding property meaning that a new value can be set any time during the encoding session.</span></span>

<span data-ttu-id="e4471-113">**Encodeurs H. 264/AVC :**</span><span class="sxs-lookup"><span data-stu-id="e4471-113">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="e4471-114">L’encodeur doit prendre en charge [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)et [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="e4471-114">Encoder shall support [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="e4471-115">Un ensemble de champs 4 16 bits est utilisé pour spécifier le cadre RPS dans l’encodage Fixed-QP.</span><span class="sxs-lookup"><span data-stu-id="e4471-115">A set of four 16-bit fields are used to specify the frame QPs in fixed-QP encoding.</span></span> <span data-ttu-id="e4471-116">Les champs sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="e4471-116">The fields are:</span></span>

-   <span data-ttu-id="e4471-117">**Bits 0-15 :** QP utilisé pour les trames I, plage valide \[ 0, 51 \] .</span><span class="sxs-lookup"><span data-stu-id="e4471-117">**Bits 0-15:** QP used for I frames, valid range \[0, 51\].</span></span>
-   <span data-ttu-id="e4471-118">**Bits 16-31 :** QP utilisé pour les frames P, plage valide \[ 0, 51 \] .</span><span class="sxs-lookup"><span data-stu-id="e4471-118">**Bits 16-31:** QP used for P frames, valid range \[0, 51\].</span></span>
-   <span data-ttu-id="e4471-119">**Bits 32-47 :** QP utilisé pour les frames B, plage valide \[ 0, 51\]</span><span class="sxs-lookup"><span data-stu-id="e4471-119">**Bits 32-47:** QP used for B frames, valid range \[0, 51\]</span></span>
-   <span data-ttu-id="e4471-120">**Bits 48-63 :** réservé</span><span class="sxs-lookup"><span data-stu-id="e4471-120">**Bits 48-63:** reserved</span></span>

<span data-ttu-id="e4471-121">Quand ce CodecAPI est pris en charge, les encodeurs prennent en charge le paramètre QP sur le type de trame I, P et B.</span><span class="sxs-lookup"><span data-stu-id="e4471-121">When this CodecAPI is supported, encoders shall support QP setting on frame type of I, P, and B.</span></span>

<span data-ttu-id="e4471-122">La valeur par défaut est 0x0000001a001a001a.</span><span class="sxs-lookup"><span data-stu-id="e4471-122">Default value shall be 0x0000001a001a001a.</span></span> <span data-ttu-id="e4471-123">QP égal à 26 pour I, P et B.</span><span class="sxs-lookup"><span data-stu-id="e4471-123">QP equal to 26 for I, P and B.</span></span>

<span data-ttu-id="e4471-124">Quand [CODECAPI \_ AVEncVideoSelectLayer](codecapi-avencvideoselectlayer.md) sélectionne une couche temporelle spécifique, [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) de CODECAPI \_ AVEncVideoEncodeFrameTypeQP doit définir QP pour les images I, P et B sur cette couche temporelle.</span><span class="sxs-lookup"><span data-stu-id="e4471-124">When [CODECAPI\_AVEncVideoSelectLayer](codecapi-avencvideoselectlayer.md) selects a specific temporal layer, [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) of CODECAPI\_AVEncVideoEncodeFrameTypeQP shall set QP for I, P, and B frames on that temporal layer.</span></span> <span data-ttu-id="e4471-125">Par défaut, il définit QP pour les images I, P et B sur la couche temporelle de base de la couche temporelle 0.</span><span class="sxs-lookup"><span data-stu-id="e4471-125">By default, it sets QP for I, P, and B frames on base temporal layer temporal layer 0.</span></span>

<span data-ttu-id="e4471-126">[CODECAPI \_ AVEncVideoMaxQP](codecapi-avencvideomaxqp.md) et [CODECAPI \_ AVEncVideoMinQP](codecapi-avencvideominqp.md) doivent être utilisés pour définir et limiter la plage de QP pour RPS de tous les types d’images, I, P et B.</span><span class="sxs-lookup"><span data-stu-id="e4471-126">[CODECAPI\_AVEncVideoMaxQP](codecapi-avencvideomaxqp.md) and [CODECAPI\_AVEncVideoMinQP](codecapi-avencvideominqp.md) shall be used to define and limit the QP range for QPs of all picture types, I, P and B.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4471-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4471-127">Requirements</span></span>



| <span data-ttu-id="e4471-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4471-128">Requirement</span></span> | <span data-ttu-id="e4471-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4471-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4471-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4471-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e4471-131">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e4471-131">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="e4471-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4471-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e4471-133">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e4471-133">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="e4471-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="e4471-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4471-135"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4471-135"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4471-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4471-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4471-137">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e4471-137">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

