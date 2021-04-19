---
title: Structure DRM_PLAY_OPL_EX (wmdrmsdk. h)
description: La \_ structure de lecture DRM \_ OPL \_ ex contient des informations sur les niveaux de protection de sortie (OPLs) spécifiés dans une licence pour les actions de lecture.
ms.assetid: 287f6681-f12e-4ef3-b802-24ee7b94bc7f
keywords:
- Structure DRM_PLAY_OPL_EX format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edf85ee664b33df9c63c390a870401b100327f53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539705"
---
# <a name="drm_play_opl_ex-structure"></a><span data-ttu-id="84f9e-105">\_Structure de lecture DRM \_ OPL \_ ex</span><span class="sxs-lookup"><span data-stu-id="84f9e-105">DRM\_PLAY\_OPL\_EX structure</span></span>

<span data-ttu-id="84f9e-106">La structure de **\_ lecture DRM \_ OPL \_ ex** contient des informations sur les niveaux de protection de sortie (OPLs) spécifiés dans une licence pour les actions de lecture.</span><span class="sxs-lookup"><span data-stu-id="84f9e-106">The **DRM\_PLAY\_OPL\_EX** structure holds information about the output protection levels (OPLs) specified in a license for play actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="84f9e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84f9e-107">Syntax</span></span>


```C++
typedef struct DRM_PLAY_OPL_EX {
  DWORD                                dwVersion;
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX   vopi;
} ;
```



## <a name="members"></a><span data-ttu-id="84f9e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="84f9e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="84f9e-109">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="84f9e-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="84f9e-110">Numéro de version.</span><span class="sxs-lookup"><span data-stu-id="84f9e-110">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="84f9e-111">**minOPL**</span><span class="sxs-lookup"><span data-stu-id="84f9e-111">**minOPL**</span></span>
</dt> <dd>

<span data-ttu-id="84f9e-112">[**DRM \_ Structure \_ des \_ \_ niveaux de protection de sortie minimum**](drmdrm-minimum-output-protection-levels.md) contenant le OPL minimal requis pour lire le contenu dans différents formats.</span><span class="sxs-lookup"><span data-stu-id="84f9e-112">[**DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS**](drmdrm-minimum-output-protection-levels.md) structure containing the minimum OPL required to play content in different formats.</span></span>

</dd> <dt>

<span data-ttu-id="84f9e-113">**oplIdReserved**</span><span class="sxs-lookup"><span data-stu-id="84f9e-113">**oplIdReserved**</span></span>
</dt> <dd>

<span data-ttu-id="84f9e-114">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="84f9e-114">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="84f9e-115">**vopi**</span><span class="sxs-lookup"><span data-stu-id="84f9e-115">**vopi**</span></span>
</dt> <dd>

<span data-ttu-id="84f9e-116">[**DRM \_ VIDEO \_ Output \_ \_ ID**](drmdrm-video-output-protection-ids.md) structure contenant les identificateurs de protection de sortie vidéo qui s’appliquent à la lecture du contenu.</span><span class="sxs-lookup"><span data-stu-id="84f9e-116">[**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**](drmdrm-video-output-protection-ids.md) structure containing the video output protection identifiers that apply to playback of the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84f9e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="84f9e-117">Remarks</span></span>

<span data-ttu-id="84f9e-118">Cette structure est identique à la **structure \_ \_ OPL de la lecture DRM** , à ceci près qu’elle comprend un numéro de version.</span><span class="sxs-lookup"><span data-stu-id="84f9e-118">This structure is identical to the **DRM\_PLAY\_OPL** structure, except that it includes a version number.</span></span>

## <a name="requirements"></a><span data-ttu-id="84f9e-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84f9e-119">Requirements</span></span>



| <span data-ttu-id="84f9e-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84f9e-120">Requirement</span></span> | <span data-ttu-id="84f9e-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="84f9e-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84f9e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="84f9e-122">Header</span></span><br/> | <dl> <span data-ttu-id="84f9e-123"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="84f9e-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84f9e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84f9e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84f9e-125">**\_OPL de lecture DRM \_**</span><span class="sxs-lookup"><span data-stu-id="84f9e-125">**DRM\_PLAY\_OPL**</span></span>](drmdrm-play-opl.md)
</dt> <dt>

[<span data-ttu-id="84f9e-126">**Structures**</span><span class="sxs-lookup"><span data-stu-id="84f9e-126">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





