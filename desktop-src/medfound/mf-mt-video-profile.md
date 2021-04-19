---
description: Spécifie le profil d’encodage vidéo sur le type de média de sortie. Il s’agit d’un alias de l' \_ \_ attribut de profil MPEG2 MT \_ .
ms.assetid: 29D1CCCA-CC11-46F1-A094-8BA8F74F7EE9
title: Attribut MF_MT_VIDEO_PROFILE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6dbf8d324c7a451c1d2affb9f348a3ef2e1806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544318"
---
# <a name="mf_mt_video_profile-attribute"></a><span data-ttu-id="b10b5-104">\_Attribut de \_ Profil vidéo MF MT \_</span><span class="sxs-lookup"><span data-stu-id="b10b5-104">MF\_MT\_VIDEO\_PROFILE attribute</span></span>

<span data-ttu-id="b10b5-105">Spécifie le profil d’encodage vidéo sur le type de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="b10b5-105">Specifies the profile of video encoding on the output media type.</span></span> <span data-ttu-id="b10b5-106">Il s’agit d’un alias de l’attribut de [ \_ \_ \_ Profil MPEG2 MT](mf-mt-mpeg2-profile-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="b10b5-106">This is an alias of [MF\_MT\_MPEG2\_PROFILE](mf-mt-mpeg2-profile-attribute.md) attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="b10b5-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="b10b5-107">Data type</span></span>

<span data-ttu-id="b10b5-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b10b5-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b10b5-109">Notes</span><span class="sxs-lookup"><span data-stu-id="b10b5-109">Remarks</span></span>

<span data-ttu-id="b10b5-110">**Encodeurs H. 264 :**</span><span class="sxs-lookup"><span data-stu-id="b10b5-110">**H.264 encoders:**</span></span>

<span data-ttu-id="b10b5-111">Les profils pris en charge sont dépassés pour inclure [**eAVEncH264VProfile \_ ConstrainedBase**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) et **eAVEncH264VProfile \_ ConstrainedHigh**.</span><span class="sxs-lookup"><span data-stu-id="b10b5-111">Supported profiles are exceeded to include [**eAVEncH264VProfile\_ConstrainedBase**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) and **eAVEncH264VProfile\_ConstrainedHigh**.</span></span>

<span data-ttu-id="b10b5-112">Les encodeurs doivent prendre en charge les paramètres [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) et [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) pour cet attribut.</span><span class="sxs-lookup"><span data-stu-id="b10b5-112">Encoders shall support both [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) and [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) for this attribute.</span></span>

<span data-ttu-id="b10b5-113">Cela est statique, les encodeurs vidéo doivent donc être configurés avant le démarrage de la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="b10b5-113">This is static, so video encoders must be configured before the streaming starts.</span></span> <span data-ttu-id="b10b5-114">Si l’application définit un profil que l’encodeur ne prend pas en charge, l’encodeur doit rejeter le type de média.</span><span class="sxs-lookup"><span data-stu-id="b10b5-114">If the application sets a profile which the encoder does not support, the encoder shall reject the media type.</span></span>

<span data-ttu-id="b10b5-115">Valeur par défaut recommandée : [**eAVEncH264VProfile \_ main**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) Profile.</span><span class="sxs-lookup"><span data-stu-id="b10b5-115">Recommended default: [**eAVEncH264VProfile\_Main**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) profile.</span></span>

## <a name="requirements"></a><span data-ttu-id="b10b5-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b10b5-116">Requirements</span></span>



| <span data-ttu-id="b10b5-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b10b5-117">Requirement</span></span> | <span data-ttu-id="b10b5-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b10b5-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b10b5-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b10b5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b10b5-120">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b10b5-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b10b5-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b10b5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b10b5-122">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b10b5-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b10b5-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b10b5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b10b5-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b10b5-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b10b5-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b10b5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b10b5-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b10b5-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
