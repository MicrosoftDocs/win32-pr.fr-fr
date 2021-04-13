---
description: Spécifie la structure de format héritée par défaut à utiliser lors de la conversion d’un type de média audio.
ms.assetid: 9bb045a2-be5b-468b-b30b-aedcb7849945
title: Attribut MF_MT_AUDIO_PREFER_WAVEFORMATEX (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be5f5ac0aadfb2a4d8d2b8394a06f270e1b4d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528245"
---
# <a name="mf_mt_audio_prefer_waveformatex-attribute"></a><span data-ttu-id="5ec7b-103">MF \_ MT \_ audio \_ préférer l' \_ attribut WAVEFORMATEX</span><span class="sxs-lookup"><span data-stu-id="5ec7b-103">MF\_MT\_AUDIO\_PREFER\_WAVEFORMATEX attribute</span></span>

<span data-ttu-id="5ec7b-104">Spécifie la structure de format héritée par défaut à utiliser lors de la conversion d’un type de média audio.</span><span class="sxs-lookup"><span data-stu-id="5ec7b-104">Specifies the preferred legacy format structure to use when converting an audio media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="5ec7b-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="5ec7b-105">Data type</span></span>

<span data-ttu-id="5ec7b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5ec7b-106">**UINT32**</span></span>

<span data-ttu-id="5ec7b-107">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="5ec7b-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ec7b-108">Notes</span><span class="sxs-lookup"><span data-stu-id="5ec7b-108">Remarks</span></span>

<span data-ttu-id="5ec7b-109">Cet attribut fournit un indicateur à la fonction [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="5ec7b-109">This attribute provides a hint to the [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype) function.</span></span> <span data-ttu-id="5ec7b-110">Si l’attribut a la **valeur true**, la fonction convertit le type de média audio en structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) chaque fois que cela est possible, au lieu de le convertir en une structure [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5ec7b-110">If the attribute is **TRUE**, the function converts the audio media type to a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure whenever possible, instead of converting it to a [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span>

<span data-ttu-id="5ec7b-111">La fonction [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) définit cet attribut.</span><span class="sxs-lookup"><span data-stu-id="5ec7b-111">The [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) function sets this attribute.</span></span> <span data-ttu-id="5ec7b-112">Vous pouvez remplacer la valeur de cet attribut, mais l’affectation de la valeur **true** à cet attribut ne garantit pas qu’un type de média audio peut être converti au format [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5ec7b-112">You can override the value of this attribute, but setting this attribute to **TRUE** does not guarantee that an audio media type can be converted to [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) form.</span></span>

<span data-ttu-id="5ec7b-113">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5ec7b-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ec7b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ec7b-114">Requirements</span></span>



| <span data-ttu-id="5ec7b-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ec7b-115">Requirement</span></span> | <span data-ttu-id="5ec7b-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ec7b-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec7b-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ec7b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5ec7b-118">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="5ec7b-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="5ec7b-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ec7b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5ec7b-120">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="5ec7b-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="5ec7b-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ec7b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ec7b-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ec7b-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ec7b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ec7b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ec7b-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5ec7b-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5ec7b-125">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5ec7b-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="5ec7b-126">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5ec7b-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="5ec7b-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="5ec7b-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="5ec7b-128">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="5ec7b-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
