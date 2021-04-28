---
description: 'Propriété AVEncAudioDualMono : spécifie si l’audio à 2 canaux est encodé en stéréo ou double mono.'
ms.assetid: 37f25590-69c2-43bd-a5d4-2262457cb39d
title: Propriété AVEncAudioDualMono (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b58cbd901079d8f4dede1efae140791ae99c7fed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096577"
---
# <a name="avencaudiodualmono-property"></a><span data-ttu-id="bded0-103">Propriété AVEncAudioDualMono</span><span class="sxs-lookup"><span data-stu-id="bded0-103">AVEncAudioDualMono property</span></span>

<span data-ttu-id="bded0-104">Spécifie si le contenu audio à 2 canaux est encodé en stéréo ou en double mono.</span><span class="sxs-lookup"><span data-stu-id="bded0-104">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span>

<span data-ttu-id="bded0-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="bded0-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="bded0-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="bded0-106">Data type</span></span>

<span data-ttu-id="bded0-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="bded0-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="bded0-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="bded0-108">Property GUID</span></span>

<span data-ttu-id="bded0-109">**CODECAPI \_ AVEncAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="bded0-109">**CODECAPI\_AVEncAudioDualMono**</span></span>

## <a name="property-value"></a><span data-ttu-id="bded0-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="bded0-110">Property value</span></span>

<span data-ttu-id="bded0-111">La valeur de cette propriété est un membre de l’énumération [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono) .</span><span class="sxs-lookup"><span data-stu-id="bded0-111">The value of this property is a member of the [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="bded0-112">Notes </span><span class="sxs-lookup"><span data-stu-id="bded0-112">Remarks</span></span>

<span data-ttu-id="bded0-113">Cette propriété ne s’applique pas aux encodeurs audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="bded0-113">This property does not apply to MPEG audio encoders.</span></span> <span data-ttu-id="bded0-114">Pour l’audio MPEG, utilisez la propriété [**AVEncMPACodingMode**](avencmpacodingmode-property.md) .</span><span class="sxs-lookup"><span data-stu-id="bded0-114">For MPEG audio, use the [**AVEncMPACodingMode**](avencmpacodingmode-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="bded0-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bded0-115">Requirements</span></span>



| <span data-ttu-id="bded0-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bded0-116">Requirement</span></span> | <span data-ttu-id="bded0-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="bded0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bded0-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bded0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bded0-119">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="bded0-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="bded0-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bded0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bded0-121">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="bded0-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="bded0-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="bded0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bded0-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bded0-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bded0-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bded0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bded0-125">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="bded0-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="bded0-126">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="bded0-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

