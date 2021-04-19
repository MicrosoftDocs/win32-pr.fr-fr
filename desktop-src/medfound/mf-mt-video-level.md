---
description: Spécifie le niveau MPEG-2 ou H. 264 dans un type de média vidéo. Il s’agit d’un alias \_ du \_ niveau de MPEG2 MT MPEG2 \_ .
ms.assetid: 23786FC8-ACA4-4F6A-98BA-57A8C76BD4C6
title: Attribut MF_MT_VIDEO_LEVEL (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca2c5eb00390df1b5c18cab7e04a5f7449f84fc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521393"
---
# <a name="mf_mt_video_level-attribute"></a><span data-ttu-id="7f0f5-104">\_Attribut de \_ niveau vidéo MF MT \_</span><span class="sxs-lookup"><span data-stu-id="7f0f5-104">MF\_MT\_VIDEO\_LEVEL attribute</span></span>

<span data-ttu-id="7f0f5-105">Spécifie le niveau MPEG-2 ou H. 264 dans un type de média vidéo.</span><span class="sxs-lookup"><span data-stu-id="7f0f5-105">Specifies the MPEG-2 or H.264 level in a video media type.</span></span> <span data-ttu-id="7f0f5-106">Il s’agit d’un alias du [ \_ niveau de \_ MPEG2 MT MPEG2 \_ ](mf-mt-mpeg2-level-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="7f0f5-106">This is an alias of [MF\_MT\_MPEG2\_LEVEL](mf-mt-mpeg2-level-attribute.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="7f0f5-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="7f0f5-107">Data type</span></span>

<span data-ttu-id="7f0f5-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7f0f5-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="7f0f5-109">Notes</span><span class="sxs-lookup"><span data-stu-id="7f0f5-109">Remarks</span></span>

<span data-ttu-id="7f0f5-110">**Encodeurs H. 264 :**</span><span class="sxs-lookup"><span data-stu-id="7f0f5-110">**H.264 encoders:**</span></span>

<span data-ttu-id="7f0f5-111">Les niveaux pris en charge sont étendus pour inclure le [**eAVEncH264VLevel5 \_ 2**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel).</span><span class="sxs-lookup"><span data-stu-id="7f0f5-111">Supported levels are extended to include the [**eAVEncH264VLevel5\_2**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel).</span></span>

<span data-ttu-id="7f0f5-112">Par défaut : la valeur par défaut recommandée consiste à sélectionner le niveau minimal pour correspondre à la configuration de l’encodage vidéo, y compris la résolution, la fréquence d’images, etc.</span><span class="sxs-lookup"><span data-stu-id="7f0f5-112">Default : Recommended default is to select the minimum level to match video encoding configuration including resolution, frame rate etc.</span></span>

<span data-ttu-id="7f0f5-113">Valeur par défaut recommandée : sélectionnez le niveau minimum pour correspondre à la configuration de l’encodage vidéo, y compris la résolution, la fréquence d’images, etc.</span><span class="sxs-lookup"><span data-stu-id="7f0f5-113">Recommended default: select the minimum level to match video encoding configuration including resolution, frame rate, etc.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f0f5-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f0f5-114">Requirements</span></span>



| <span data-ttu-id="7f0f5-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f0f5-115">Requirement</span></span> | <span data-ttu-id="7f0f5-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f0f5-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7f0f5-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f0f5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7f0f5-118">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7f0f5-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7f0f5-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f0f5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7f0f5-120">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7f0f5-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="7f0f5-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f0f5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f0f5-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f0f5-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f0f5-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f0f5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f0f5-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7f0f5-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




