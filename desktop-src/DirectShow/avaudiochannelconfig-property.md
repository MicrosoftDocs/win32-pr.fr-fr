---
description: Obtient la configuration de l’orateur pour les canaux audio dans le flux de bits audio.
ms.assetid: ec13bb55-47af-4d79-9560-d297bce8e236
title: Propriété AVAudioChannelConfig (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52ee1bc7897d92f7efa1b6d351d2f73c32867529
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033440"
---
# <a name="avaudiochannelconfig-property"></a><span data-ttu-id="b6300-103">Propriété AVAudioChannelConfig</span><span class="sxs-lookup"><span data-stu-id="b6300-103">AVAudioChannelConfig property</span></span>

<span data-ttu-id="b6300-104">Obtient la configuration de l’orateur pour les canaux audio dans le flux de bits audio.</span><span class="sxs-lookup"><span data-stu-id="b6300-104">Gets the speaker configuration for the audio channels in the audio bit stream.</span></span>

<span data-ttu-id="b6300-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b6300-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="b6300-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="b6300-106">Data type</span></span>

<span data-ttu-id="b6300-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="b6300-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="b6300-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="b6300-108">Property GUID</span></span>

<span data-ttu-id="b6300-109">**CODECAPI \_ AVAudioChannelConfig**</span><span class="sxs-lookup"><span data-stu-id="b6300-109">**CODECAPI\_AVAudioChannelConfig**</span></span>

## <a name="property-value"></a><span data-ttu-id="b6300-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b6300-110">Property value</span></span>

<span data-ttu-id="b6300-111">La valeur de cette propriété est une opération or au niveau du bit de l’énumération [**eAVAudioChannelConfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig) .</span><span class="sxs-lookup"><span data-stu-id="b6300-111">The value of this property is a bitwise OR of members of the [**eAVAudioChannelConfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6300-112">Notes</span><span class="sxs-lookup"><span data-stu-id="b6300-112">Remarks</span></span>

<span data-ttu-id="b6300-113">Le nombre de canaux comprend le canal de l’effet de fréquence faible (LFE), le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="b6300-113">The number of channels includes the low frequency effect (LFE) channel, if present.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6300-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6300-114">Requirements</span></span>



| <span data-ttu-id="b6300-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6300-115">Requirement</span></span> | <span data-ttu-id="b6300-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6300-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6300-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6300-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b6300-118">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="b6300-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="b6300-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6300-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b6300-120">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="b6300-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b6300-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6300-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6300-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6300-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6300-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6300-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6300-124">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="b6300-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="b6300-125">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="b6300-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




