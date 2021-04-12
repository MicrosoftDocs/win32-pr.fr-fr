---
description: Niveau de volume maximal de référence d’un fichier Windows Media Audio.
ms.assetid: bb762f9c-cf08-4d32-991e-490eb7b1f579
title: Attribut MF_MT_AUDIO_WMADRC_PEAKREF (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0074046c79f532a4b63472f8ec22b588b2c4020a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528240"
---
# <a name="mf_mt_audio_wmadrc_peakref-attribute"></a><span data-ttu-id="44671-103">Attribut PEAKREF de l’WMADRC MF \_ MT \_ audio \_ \_</span><span class="sxs-lookup"><span data-stu-id="44671-103">MF\_MT\_AUDIO\_WMADRC\_PEAKREF attribute</span></span>

<span data-ttu-id="44671-104">Niveau de volume maximal de référence d’un fichier Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="44671-104">Reference peak volume level of a Windows Media Audio file.</span></span>

## <a name="data-type"></a><span data-ttu-id="44671-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="44671-105">Data type</span></span>

<span data-ttu-id="44671-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="44671-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="44671-107">Notes</span><span class="sxs-lookup"><span data-stu-id="44671-107">Remarks</span></span>

<span data-ttu-id="44671-108">Cet attribut s’applique aux types de média audio pour Windows Media Audio codecs.</span><span class="sxs-lookup"><span data-stu-id="44671-108">This attribute applies to audio media types for Windows Media Audio codecs.</span></span> <span data-ttu-id="44671-109">Il spécifie le niveau de volume maximal d’origine du contenu.</span><span class="sxs-lookup"><span data-stu-id="44671-109">It specifies the original peak volume level of the content.</span></span> <span data-ttu-id="44671-110">Le décodeur peut utiliser cette valeur pour effectuer un contrôle de plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="44671-110">The decoder can use this value to perform dynamic range control.</span></span>

<span data-ttu-id="44671-111">La méthode [**IMFASFContentInfo ::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) ajoute cet attribut au type de média si l’en-tête ASF contient l’attribut [**WM/WMADRCPeakReference**](../wmformat/wm-wmadrcpeakreference.md) .</span><span class="sxs-lookup"><span data-stu-id="44671-111">The [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method adds this attribute to the media type if the ASF header contains the [**WM/WMADRCPeakReference**](../wmformat/wm-wmadrcpeakreference.md) attribute.</span></span> <span data-ttu-id="44671-112">Cet attribut est documenté dans la documentation du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="44671-112">This attribute is documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="44671-113">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="44671-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="44671-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44671-114">Requirements</span></span>



| <span data-ttu-id="44671-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44671-115">Requirement</span></span> | <span data-ttu-id="44671-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="44671-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="44671-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44671-117">Minimum supported client</span></span><br/> | <span data-ttu-id="44671-118">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="44671-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="44671-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44671-119">Minimum supported server</span></span><br/> | <span data-ttu-id="44671-120">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="44671-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="44671-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="44671-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="44671-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="44671-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44671-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44671-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44671-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="44671-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="44671-125">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="44671-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="44671-126">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="44671-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="44671-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="44671-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="44671-128">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="44671-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
