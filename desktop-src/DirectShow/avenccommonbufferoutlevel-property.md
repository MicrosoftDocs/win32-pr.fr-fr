---
description: Spécifie le niveau final de la mémoire tampon d’encodage, en bits, à la fin du processus d’encodage. Cette propriété s’applique uniquement aux modes d’encodage à vitesse de transmission constante (CBR) et à vitesse de transmission variable (VBR).
ms.assetid: d5bcdf54-061a-436b-8b1a-61ef7d7c90bf
title: Propriété AVEncCommonBufferOutLevel (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d99cdea909a1fd1c3777aac4868a570161c3fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515757"
---
# <a name="avenccommonbufferoutlevel-property"></a><span data-ttu-id="0c8ab-104">Propriété AVEncCommonBufferOutLevel</span><span class="sxs-lookup"><span data-stu-id="0c8ab-104">AVEncCommonBufferOutLevel property</span></span>

<span data-ttu-id="0c8ab-105">Spécifie le niveau final de la mémoire tampon d’encodage, en bits, à la fin du processus d’encodage.</span><span class="sxs-lookup"><span data-stu-id="0c8ab-105">Specifies the final level of the encoding buffer, in bits, at the end of the encoding process.</span></span> <span data-ttu-id="0c8ab-106">Cette propriété s’applique uniquement aux modes d’encodage à vitesse de transmission constante (CBR) et à vitesse de transmission variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="0c8ab-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="0c8ab-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="0c8ab-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="0c8ab-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="0c8ab-108">Data type</span></span>

<span data-ttu-id="0c8ab-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="0c8ab-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="0c8ab-110">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="0c8ab-110">Property GUID</span></span>

<span data-ttu-id="0c8ab-111">**CODECAPI \_ AVEncCommonBufferOutLevel**</span><span class="sxs-lookup"><span data-stu-id="0c8ab-111">**CODECAPI\_AVEncCommonBufferOutLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="0c8ab-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0c8ab-112">Property value</span></span>

<span data-ttu-id="0c8ab-113">Cette propriété a une plage de valeurs linéaire.</span><span class="sxs-lookup"><span data-stu-id="0c8ab-113">This property has a linear range of values.</span></span> <span data-ttu-id="0c8ab-114">Pour accéder à la plage prise en charge, appelez [**ICodecAPI :: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="0c8ab-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="0c8ab-115">Notes</span><span class="sxs-lookup"><span data-stu-id="0c8ab-115">Remarks</span></span>

<span data-ttu-id="0c8ab-116">La propriété est disponible uniquement si la durée d’encodage est définie à l’avance, à l’aide de la propriété [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md) ou de la propriété [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md) .</span><span class="sxs-lookup"><span data-stu-id="0c8ab-116">The property is available only if the encoding duration is defined in advance, using the [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md) property or [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md) property.</span></span>

<span data-ttu-id="0c8ab-117">Pour la vidéo MPEG, cette propriété définit le remplissage du vérificateur de mémoire tampon vidéo (VBV) à la fin du processus d’encodage.</span><span class="sxs-lookup"><span data-stu-id="0c8ab-117">For MPEG video, this property defines the video buffer verifier (VBV) fullness at the end of the encoding process.</span></span> <span data-ttu-id="0c8ab-118">Il prend en charge la concaténation de flux pendant l’encodage.</span><span class="sxs-lookup"><span data-stu-id="0c8ab-118">It supports the concatenation of streams during encoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c8ab-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c8ab-119">Requirements</span></span>



| <span data-ttu-id="0c8ab-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c8ab-120">Requirement</span></span> | <span data-ttu-id="0c8ab-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c8ab-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c8ab-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c8ab-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0c8ab-123">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="0c8ab-123">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="0c8ab-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c8ab-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0c8ab-125">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="0c8ab-125">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="0c8ab-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="0c8ab-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c8ab-127"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c8ab-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c8ab-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c8ab-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c8ab-129">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="0c8ab-129">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="0c8ab-130">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="0c8ab-130">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




