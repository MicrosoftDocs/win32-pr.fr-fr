---
title: Structure DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX (wmdrmsdk. h)
description: La \_ \_ \_ \_ \_ structure ex structure de protection des sorties audio DRM contient une liste d’identificateurs de protection de sortie audio. Cette structure étend les \_ \_ \_ ID de protection de sortie audio DRM \_ en ajoutant un numéro de version.
ms.assetid: e650ddeb-5e41-4ff8-b872-40c85ab519c1
keywords:
- Structure DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb687b5600e75f845c2d980f73f3b8c2eeda970a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545644"
---
# <a name="drm_audio_output_protection_ids_ex-structure"></a><span data-ttu-id="eed5e-106">\_ID de protection de sortie audio DRM \_ \_ \_ \_ ex structure</span><span class="sxs-lookup"><span data-stu-id="eed5e-106">DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX structure</span></span>

<span data-ttu-id="eed5e-107">La structure ex structure de **\_ \_ protection des sorties \_ \_ \_ audio DRM** contient une liste d’identificateurs de protection de sortie audio.</span><span class="sxs-lookup"><span data-stu-id="eed5e-107">The **DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX** structure contains a list of audio output protection identifiers.</span></span> <span data-ttu-id="eed5e-108">Cette structure étend **les \_ \_ ID de \_ protection \_ de sortie audio DRM** en ajoutant un numéro de version.</span><span class="sxs-lookup"><span data-stu-id="eed5e-108">This structure extends **DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS** by adding a version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="eed5e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eed5e-109">Syntax</span></span>


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION_EX *rgAop;
} ;
```



## <a name="members"></a><span data-ttu-id="eed5e-110">Membres</span><span class="sxs-lookup"><span data-stu-id="eed5e-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="eed5e-111">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="eed5e-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="eed5e-112">Numéro de version.</span><span class="sxs-lookup"><span data-stu-id="eed5e-112">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="eed5e-113">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="eed5e-113">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="eed5e-114">Nombre d’entrées dans le tableau **rgAop** .</span><span class="sxs-lookup"><span data-stu-id="eed5e-114">Number of entries in the **rgAop** array.</span></span>

</dd> <dt>

<span data-ttu-id="eed5e-115">**rgAop**</span><span class="sxs-lookup"><span data-stu-id="eed5e-115">**rgAop**</span></span>
</dt> <dd>

<span data-ttu-id="eed5e-116">Tableau des **structures \_ \_ ex de \_ protection \_ de sortie audio DRM** .</span><span class="sxs-lookup"><span data-stu-id="eed5e-116">Array of **DRM\_AUDIO\_OUTPUT\_PROTECTION\_EX** structures.</span></span> <span data-ttu-id="eed5e-117">**DRM \_ \_Protection de sortie audio \_ \_ ex** est un type défini comme [**protection de sortie DRM, par \_ \_ \_ exemple**](drm-output-protection-ex.md).</span><span class="sxs-lookup"><span data-stu-id="eed5e-117">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_EX** is a type defined as [**DRM\_OUTPUT\_PROTECTION\_EX**](drm-output-protection-ex.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eed5e-118">Notes</span><span class="sxs-lookup"><span data-stu-id="eed5e-118">Remarks</span></span>

<span data-ttu-id="eed5e-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="eed5e-119">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="eed5e-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eed5e-120">Requirements</span></span>



| <span data-ttu-id="eed5e-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eed5e-121">Requirement</span></span> | <span data-ttu-id="eed5e-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="eed5e-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eed5e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="eed5e-123">Header</span></span><br/> | <dl> <span data-ttu-id="eed5e-124"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="eed5e-124"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eed5e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eed5e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eed5e-126">**\_ID de \_ protection de sortie audio \_ DRM \_**</span><span class="sxs-lookup"><span data-stu-id="eed5e-126">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drm-audio-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="eed5e-127">**\_ID de \_ protection de sortie vidéo DRM \_ \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="eed5e-127">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="eed5e-128">**Structures**</span><span class="sxs-lookup"><span data-stu-id="eed5e-128">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





