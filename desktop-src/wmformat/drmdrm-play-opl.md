---
title: Structure DRM_PLAY_OPL (wmdrmsdk. h)
description: La \_ structure OPL de la lecture DRM \_ contient des informations sur les niveaux de protection de sortie (OPLs) spécifiés dans une licence pour les actions de lecture.
ms.assetid: 10703893-630c-4cbe-a0b0-d2890905daba
keywords:
- Structure DRM_PLAY_OPL format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a40d8fe4e8b3c820f9d7bcb405b5c0806040182
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528564"
---
# <a name="drm_play_opl-structure"></a><span data-ttu-id="e4761-105">\_Structure OPL de lecture DRM \_</span><span class="sxs-lookup"><span data-stu-id="e4761-105">DRM\_PLAY\_OPL structure</span></span>

<span data-ttu-id="e4761-106">La **structure \_ \_ OPL de la lecture DRM** contient des informations sur les niveaux de protection de sortie (OPLs) spécifiés dans une licence pour les actions de lecture.</span><span class="sxs-lookup"><span data-stu-id="e4761-106">The **DRM\_PLAY\_OPL** structure holds information about the output protection levels (OPLs) specified in a license for play actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4761-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4761-107">Syntax</span></span>


```C++
typedef struct DRM_PLAY_OPL {
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS      vopi;
} ;
```



## <a name="members"></a><span data-ttu-id="e4761-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e4761-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e4761-109">**minOPL**</span><span class="sxs-lookup"><span data-stu-id="e4761-109">**minOPL**</span></span>
</dt> <dd>

<span data-ttu-id="e4761-110">[**DRM \_ Structure \_ des \_ \_ niveaux de protection de sortie minimum**](drmdrm-minimum-output-protection-levels.md) contenant le OPL minimal requis pour lire le contenu dans différents formats.</span><span class="sxs-lookup"><span data-stu-id="e4761-110">[**DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS**](drmdrm-minimum-output-protection-levels.md) structure containing the minimum OPL required to play content in different formats.</span></span>

</dd> <dt>

<span data-ttu-id="e4761-111">**oplIdReserved**</span><span class="sxs-lookup"><span data-stu-id="e4761-111">**oplIdReserved**</span></span>
</dt> <dd>

<span data-ttu-id="e4761-112">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="e4761-112">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="e4761-113">**vopi**</span><span class="sxs-lookup"><span data-stu-id="e4761-113">**vopi**</span></span>
</dt> <dd>

<span data-ttu-id="e4761-114">[**DRM \_ VIDEO \_ Output \_ \_ ID**](drmdrm-video-output-protection-ids.md) structure contenant les identificateurs de protection de sortie vidéo qui s’appliquent à la lecture du contenu.</span><span class="sxs-lookup"><span data-stu-id="e4761-114">[**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**](drmdrm-video-output-protection-ids.md) structure containing the video output protection identifiers that apply to playback of the content.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e4761-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4761-115">Requirements</span></span>



| <span data-ttu-id="e4761-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4761-116">Requirement</span></span> | <span data-ttu-id="e4761-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4761-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4761-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="e4761-118">Header</span></span><br/> | <dl> <span data-ttu-id="e4761-119"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4761-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4761-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4761-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4761-121">**\_OPL de copie DRM \_**</span><span class="sxs-lookup"><span data-stu-id="e4761-121">**DRM\_COPY\_OPL**</span></span>](drmdrm-copy-opl.md)
</dt> <dt>

[<span data-ttu-id="e4761-122">**\_OPL de lecture DRM \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="e4761-122">**DRM\_PLAY\_OPL\_EX**</span></span>](drm-play-opl-ex.md)
</dt> <dt>

[<span data-ttu-id="e4761-123">**Structures**</span><span class="sxs-lookup"><span data-stu-id="e4761-123">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





