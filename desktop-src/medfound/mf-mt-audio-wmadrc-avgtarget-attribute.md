---
description: Niveau de volume moyen cible d’un fichier Windows Media Audio.
ms.assetid: f81158c8-b341-4b39-8fa4-b510c93b89fc
title: Attribut MF_MT_AUDIO_WMADRC_AVGTARGET (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41956e2e9e6f14e969cade3628f1e88bce98796d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320629"
---
# <a name="mf_mt_audio_wmadrc_avgtarget-attribute"></a><span data-ttu-id="aa9b1-103">Attribut AVGTARGET de l’WMADRC MF \_ MT \_ audio \_ \_</span><span class="sxs-lookup"><span data-stu-id="aa9b1-103">MF\_MT\_AUDIO\_WMADRC\_AVGTARGET attribute</span></span>

<span data-ttu-id="aa9b1-104">Niveau de volume moyen cible d’un fichier Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="aa9b1-104">Target average volume level of a Windows Media Audio file.</span></span>

## <a name="data-type"></a><span data-ttu-id="aa9b1-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="aa9b1-105">Data type</span></span>

<span data-ttu-id="aa9b1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="aa9b1-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="aa9b1-107">Notes</span><span class="sxs-lookup"><span data-stu-id="aa9b1-107">Remarks</span></span>

<span data-ttu-id="aa9b1-108">Cet attribut s’applique aux types de média audio pour Windows Media Audio codecs.</span><span class="sxs-lookup"><span data-stu-id="aa9b1-108">This attribute applies to audio media types for Windows Media Audio codecs.</span></span> <span data-ttu-id="aa9b1-109">Il spécifie le niveau de volume moyen de la cible du contenu.</span><span class="sxs-lookup"><span data-stu-id="aa9b1-109">It specifies the target average volume level of the content.</span></span> <span data-ttu-id="aa9b1-110">Le décodeur peut utiliser cette valeur pour effectuer un contrôle de plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="aa9b1-110">The decoder can use this value to perform dynamic range control.</span></span>

<span data-ttu-id="aa9b1-111">La méthode [**IMFASFContentInfo ::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) ajoute cet attribut au type de média si l’en-tête ASF contient l’attribut [**WM/WMADRCAverageTarget**](../wmformat/wm-wmadrcaveragetarget.md) .</span><span class="sxs-lookup"><span data-stu-id="aa9b1-111">The [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method adds this attribute to the media type if the ASF header contains the [**WM/WMADRCAverageTarget**](../wmformat/wm-wmadrcaveragetarget.md) attribute.</span></span> <span data-ttu-id="aa9b1-112">Cet attribut est documenté dans la documentation du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="aa9b1-112">This attribute is documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="aa9b1-113">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="aa9b1-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa9b1-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa9b1-114">Requirements</span></span>



| <span data-ttu-id="aa9b1-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa9b1-115">Requirement</span></span> | <span data-ttu-id="aa9b1-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa9b1-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aa9b1-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa9b1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="aa9b1-118">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="aa9b1-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="aa9b1-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa9b1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="aa9b1-120">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="aa9b1-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="aa9b1-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="aa9b1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa9b1-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa9b1-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa9b1-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa9b1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa9b1-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aa9b1-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="aa9b1-125">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="aa9b1-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="aa9b1-126">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="aa9b1-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="aa9b1-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="aa9b1-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="aa9b1-128">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="aa9b1-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
