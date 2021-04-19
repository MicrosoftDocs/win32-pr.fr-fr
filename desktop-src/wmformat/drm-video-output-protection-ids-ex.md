---
title: Structure DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX (wmdrmsdk. h)
description: La \_ \_ \_ structure d’ID de protection de sortie vidéo DRM \_ \_ contient un tableau \_ de \_ structures de protection de sortie vidéo DRM \_ .
ms.assetid: 89de0ade-fa86-4081-b65b-9c84fb68cf3d
keywords:
- Structure DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2e7cc5ec0b4b14d88deb317e62e3e1cd4f92b57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539492"
---
# <a name="drm_video_output_protection_ids_ex-structure"></a><span data-ttu-id="8ec4a-105">\_ID de protection de sortie vidéo DRM \_ \_ \_ \_ ex structure</span><span class="sxs-lookup"><span data-stu-id="8ec4a-105">DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX structure</span></span>

<span data-ttu-id="8ec4a-106">La structure d' **\_ ID de \_ protection de sortie \_ \_ \_ vidéo DRM** contient un tableau de structures de **\_ \_ \_ protection de sortie vidéo DRM** .</span><span class="sxs-lookup"><span data-stu-id="8ec4a-106">The **DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX** structure holds an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ec4a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ec4a-107">Syntax</span></span>


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION_EX *rgVop;
} ;
```



## <a name="members"></a><span data-ttu-id="8ec4a-108">Membres</span><span class="sxs-lookup"><span data-stu-id="8ec4a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8ec4a-109">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="8ec4a-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="8ec4a-110">Numéro de version.</span><span class="sxs-lookup"><span data-stu-id="8ec4a-110">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="8ec4a-111">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="8ec4a-111">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="8ec4a-112">Nombre d’éléments dans le tableau référencé par **rgVop**.</span><span class="sxs-lookup"><span data-stu-id="8ec4a-112">Number of elements in the array referenced by **rgVop**.</span></span>

</dd> <dt>

<span data-ttu-id="8ec4a-113">**rgVop**</span><span class="sxs-lookup"><span data-stu-id="8ec4a-113">**rgVop**</span></span>
</dt> <dd>

<span data-ttu-id="8ec4a-114">Adresse d’un tableau de structures de **\_ protection de sortie vidéo DRM \_ \_ \_ ex** .</span><span class="sxs-lookup"><span data-stu-id="8ec4a-114">Address of an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION\_EX** structures.</span></span> <span data-ttu-id="8ec4a-115">**DRM \_ Protection de sortie vidéo par \_ \_ \_ ex** . est un type défini comme [**protection de sortie DRM, par \_ \_ \_ exemple**](drm-output-protection-ex.md).</span><span class="sxs-lookup"><span data-stu-id="8ec4a-115">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_EX** is a type defined as [**DRM\_OUTPUT\_PROTECTION\_EX**](drm-output-protection-ex.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ec4a-116">Notes</span><span class="sxs-lookup"><span data-stu-id="8ec4a-116">Remarks</span></span>

<span data-ttu-id="8ec4a-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="8ec4a-117">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ec4a-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ec4a-118">Requirements</span></span>



| <span data-ttu-id="8ec4a-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ec4a-119">Requirement</span></span> | <span data-ttu-id="8ec4a-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ec4a-120">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ec4a-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="8ec4a-121">Header</span></span><br/> | <dl> <span data-ttu-id="8ec4a-122"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ec4a-122"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ec4a-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ec4a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ec4a-124">**\_ID de \_ protection de sortie audio DRM \_ \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="8ec4a-124">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="8ec4a-125">**\_ID de \_ protection de sortie vidéo \_ DRM \_**</span><span class="sxs-lookup"><span data-stu-id="8ec4a-125">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="8ec4a-126">**Structures**</span><span class="sxs-lookup"><span data-stu-id="8ec4a-126">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





