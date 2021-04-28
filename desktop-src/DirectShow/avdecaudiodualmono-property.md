---
description: 'Propriété AVDecAudioDualMono : spécifie si l’audio à 2 canaux est encodé en stéréo ou double mono.'
ms.assetid: 96cb9e17-588c-4a1a-a7ba-7f8439d5b79a
title: Propriété AVDecAudioDualMono (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adc84e19d41840b358e3e79576152dbc8527e2bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096567"
---
# <a name="avdecaudiodualmono-property"></a><span data-ttu-id="683bc-103">Propriété AVDecAudioDualMono</span><span class="sxs-lookup"><span data-stu-id="683bc-103">AVDecAudioDualMono property</span></span>

<span data-ttu-id="683bc-104">Spécifie si le contenu audio à 2 canaux est encodé en stéréo ou en double mono.</span><span class="sxs-lookup"><span data-stu-id="683bc-104">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span>

<span data-ttu-id="683bc-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="683bc-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="683bc-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="683bc-106">Data type</span></span>

<span data-ttu-id="683bc-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="683bc-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="683bc-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="683bc-108">Property GUID</span></span>

<span data-ttu-id="683bc-109">**CODECAPI \_ AVDecAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="683bc-109">**CODECAPI\_AVDecAudioDualMono**</span></span>

## <a name="property-value"></a><span data-ttu-id="683bc-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="683bc-110">Property value</span></span>

<span data-ttu-id="683bc-111">La valeur de cette propriété est un membre de l’énumération [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono) .</span><span class="sxs-lookup"><span data-stu-id="683bc-111">The value of this property is a member of the [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="683bc-112">Notes </span><span class="sxs-lookup"><span data-stu-id="683bc-112">Remarks</span></span>

<span data-ttu-id="683bc-113">Cette propriété s’applique uniquement lorsque le flux de bits d’entrée du décodeur contient du son de deux canaux.</span><span class="sxs-lookup"><span data-stu-id="683bc-113">This property applies only when the decoder's input bit stream contains two-channel audio.</span></span> <span data-ttu-id="683bc-114">Un flux audio à deux canaux peut être encodé en stéréo ou en double mono.</span><span class="sxs-lookup"><span data-stu-id="683bc-114">A two-channel audio stream might be encoded as stereo or as dual mono.</span></span> <span data-ttu-id="683bc-115">Si le son est double mono, vous pouvez définir la propriété [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md) pour configurer la façon dont le décodeur reproduit l’audio.</span><span class="sxs-lookup"><span data-stu-id="683bc-115">If the audio is dual mono, you can set the [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md) property to configure how the decoder reproduces the audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="683bc-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="683bc-116">Requirements</span></span>



| <span data-ttu-id="683bc-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="683bc-117">Requirement</span></span> | <span data-ttu-id="683bc-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="683bc-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="683bc-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="683bc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="683bc-120">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="683bc-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="683bc-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="683bc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="683bc-122">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="683bc-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="683bc-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="683bc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="683bc-124"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="683bc-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="683bc-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="683bc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="683bc-126">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="683bc-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="683bc-127">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="683bc-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




