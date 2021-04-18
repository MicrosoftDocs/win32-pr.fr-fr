---
description: Spécifie le mode stéréo downmix pour un décodeur audio Dolby Digital.
ms.assetid: 270893C6-8B44-4A4D-AE2B-2E58E260F649
title: CODECAPI_AVDecDDStereoDownMixMode, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de7caaed1af804e22b3ec6085241746bdf01eb7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393303"
---
# <a name="codecapi_avdecddstereodownmixmode-property"></a><span data-ttu-id="3c983-103">CODECAPI \_ propriété AVDecDDStereoDownMixMode</span><span class="sxs-lookup"><span data-stu-id="3c983-103">CODECAPI\_AVDecDDStereoDownMixMode property</span></span>

<span data-ttu-id="3c983-104">Spécifie le mode stéréo downmix pour un décodeur audio Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="3c983-104">Specifies the stereo downmix mode for a Dolby Digital audio decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="3c983-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="3c983-105">Data type</span></span>

<span data-ttu-id="3c983-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3c983-106">**UINT32**</span></span>

## <a name="property-guid"></a><span data-ttu-id="3c983-107">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="3c983-107">Property GUID</span></span>

<span data-ttu-id="3c983-108">**CODECAPI \_ AVDecDDStereoDownMixMode**</span><span class="sxs-lookup"><span data-stu-id="3c983-108">**CODECAPI\_AVDecDDStereoDownMixMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="3c983-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3c983-109">Property value</span></span>

<span data-ttu-id="3c983-110">La valeur de cette propriété est un membre de l’énumération [**eAVDecDDStereoDownMixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecddstereodownmixmode) .</span><span class="sxs-lookup"><span data-stu-id="3c983-110">The value of this property is a member of the [**eAVDecDDStereoDownMixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecddstereodownmixmode) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c983-111">Notes</span><span class="sxs-lookup"><span data-stu-id="3c983-111">Remarks</span></span>

<span data-ttu-id="3c983-112">Cet attribut s’applique lorsque l’entrée dans le décodeur est un fichier audio PCM Multichannel, et la sortie est de l’audio stéréo.</span><span class="sxs-lookup"><span data-stu-id="3c983-112">This attribute applies when the input to the decoder is multichannel PCM audio, and the output is stereo audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c983-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c983-113">Requirements</span></span>



| <span data-ttu-id="3c983-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c983-114">Requirement</span></span> | <span data-ttu-id="3c983-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c983-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c983-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c983-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3c983-117">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3c983-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="3c983-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c983-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3c983-119">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="3c983-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="3c983-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c983-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c983-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c983-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c983-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c983-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c983-123">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3c983-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="3c983-124">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="3c983-124">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

