---
title: Structure DRM_VIDEO_OUTPUT_PROTECTION_IDS (wmdrmsdk. h)
description: La \_ \_ structure de l’ID de protection de la sortie vidéo DRM \_ \_ contient un tableau de \_ structures de protection de sortie vidéo DRM \_ \_ .
ms.assetid: 9f206a7e-c92b-4f29-a591-72784086d1db
keywords:
- Structure DRM_VIDEO_OUTPUT_PROTECTION_IDS format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51af3ccebec52ab6f6863aeb376ed27f8c8e2467
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530371"
---
# <a name="drm_video_output_protection_ids-structure"></a><span data-ttu-id="ee0c3-105">Structure des ID de protection de la \_ sortie vidéo DRM \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="ee0c3-105">DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS structure</span></span>

<span data-ttu-id="ee0c3-106">La structure de l’ID de protection de la **\_ \_ sortie \_ \_ vidéo DRM** contient un tableau de structures de **\_ \_ \_ protection de sortie vidéo DRM** .</span><span class="sxs-lookup"><span data-stu-id="ee0c3-106">The **DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS** structure holds an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee0c3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee0c3-107">Syntax</span></span>


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION *rgVop;
} ;
```



## <a name="members"></a><span data-ttu-id="ee0c3-108">Membres</span><span class="sxs-lookup"><span data-stu-id="ee0c3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ee0c3-109">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="ee0c3-109">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="ee0c3-110">Nombre d’éléments dans le tableau référencé par **rgVop**.</span><span class="sxs-lookup"><span data-stu-id="ee0c3-110">Number of elements in the array referenced by **rgVop**.</span></span>

</dd> <dt>

<span data-ttu-id="ee0c3-111">**rgVop**</span><span class="sxs-lookup"><span data-stu-id="ee0c3-111">**rgVop**</span></span>
</dt> <dd>

<span data-ttu-id="ee0c3-112">Adresse d’un tableau de structures de **\_ \_ \_ protection de sortie vidéo DRM** .</span><span class="sxs-lookup"><span data-stu-id="ee0c3-112">Address of an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION** structures.</span></span> <span data-ttu-id="ee0c3-113">**DRM \_ La \_ \_ protection de sortie vidéo** est un type défini comme [**\_ \_ protection de sortie DRM**](drm-output-protection.md).</span><span class="sxs-lookup"><span data-stu-id="ee0c3-113">**DRM\_VIDEO\_OUTPUT\_PROTECTION** is a type defined as [**DRM\_OUTPUT\_PROTECTION**](drm-output-protection.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee0c3-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ee0c3-114">Remarks</span></span>

<span data-ttu-id="ee0c3-115">Cette structure est utilisée en tant que membre de la structure de [**\_ lecture DRM \_ OPL**](drmdrm-play-opl.md) .</span><span class="sxs-lookup"><span data-stu-id="ee0c3-115">This structure is used as a member of the [**DRM\_PLAY\_OPL**](drmdrm-play-opl.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee0c3-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee0c3-116">Requirements</span></span>



| <span data-ttu-id="ee0c3-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee0c3-117">Requirement</span></span> | <span data-ttu-id="ee0c3-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee0c3-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee0c3-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="ee0c3-119">Header</span></span><br/> | <dl> <span data-ttu-id="ee0c3-120"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee0c3-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee0c3-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee0c3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee0c3-122">**\_ID de \_ protection de sortie audio \_ DRM \_**</span><span class="sxs-lookup"><span data-stu-id="ee0c3-122">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drm-audio-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="ee0c3-123">**\_ID de \_ protection de sortie vidéo DRM \_ \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="ee0c3-123">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="ee0c3-124">**Structures**</span><span class="sxs-lookup"><span data-stu-id="ee0c3-124">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





