---
description: Pour un type de média vidéo, spécifie la manière dont les images vidéo 3D sont stockées en mémoire.
ms.assetid: 880DF017-5841-4C0A-82AF-F092DEF5406B
title: Attribut MF_MT_VIDEO_3D_FORMAT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f2b12f907edb2875b3b121607509288787c8e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524388"
---
# <a name="mf_mt_video_3d_format-attribute"></a><span data-ttu-id="d84e3-103">\_Attribut de \_ \_ format vidéo 3D \_ MF MT</span><span class="sxs-lookup"><span data-stu-id="d84e3-103">MF\_MT\_VIDEO\_3D\_FORMAT attribute</span></span>

<span data-ttu-id="d84e3-104">Pour un type de média vidéo, spécifie la manière dont les images vidéo 3D sont stockées en mémoire.</span><span class="sxs-lookup"><span data-stu-id="d84e3-104">For a video media type, specifies how 3D video frames are stored in memory.</span></span>

## <a name="data-type"></a><span data-ttu-id="d84e3-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="d84e3-105">Data type</span></span>

<span data-ttu-id="d84e3-106">**MFVideo3DFormat** stocké en tant que **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d84e3-106">**MFVideo3DFormat** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d84e3-107">Notes</span><span class="sxs-lookup"><span data-stu-id="d84e3-107">Remarks</span></span>

<span data-ttu-id="d84e3-108">La valeur de cet attribut est un membre de l’énumération [**MFVideo3DFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dformat) .</span><span class="sxs-lookup"><span data-stu-id="d84e3-108">The value of this attribute is a member of the [**MFVideo3DFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dformat) enumeration.</span></span> <span data-ttu-id="d84e3-109">L’attribut s’applique uniquement si l’attribut [ \_ \_ \_ 3D MF MT Video](mf-mt-video-3d.md) a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="d84e3-109">The attribute applies only if the [MF\_MT\_VIDEO\_3D](mf-mt-video-3d.md) attribute is **TRUE**.</span></span>

<span data-ttu-id="d84e3-110">Cet attribut est requis pour les formats vidéo 3D non compressés.</span><span class="sxs-lookup"><span data-stu-id="d84e3-110">This attribute is required for uncompressed 3D video formats.</span></span> <span data-ttu-id="d84e3-111">Elle est facultative pour la vidéo 3D compressée.</span><span class="sxs-lookup"><span data-stu-id="d84e3-111">It is optional for compressed 3D video.</span></span> <span data-ttu-id="d84e3-112">Une source de média qui fournit des frames encodés peut être en mesure de définir l’attribut, en fonction des informations contenues dans le conteneur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="d84e3-112">A media source that delivers encoded frames might be able to set the attribute, based on information in the file container.</span></span> <span data-ttu-id="d84e3-113">Dans le cas contraire, l’attribut doit être défini par le décodeur dans le type de média de sortie du décodeur.</span><span class="sxs-lookup"><span data-stu-id="d84e3-113">Otherwise, the attribute should be set by the decoder in the decoder's output media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="d84e3-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d84e3-114">Requirements</span></span>



| <span data-ttu-id="d84e3-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d84e3-115">Requirement</span></span> | <span data-ttu-id="d84e3-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d84e3-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d84e3-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d84e3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d84e3-118">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d84e3-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="d84e3-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d84e3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d84e3-120">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="d84e3-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="d84e3-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="d84e3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d84e3-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d84e3-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d84e3-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d84e3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d84e3-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d84e3-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




