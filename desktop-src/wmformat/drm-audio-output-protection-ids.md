---
title: Structure DRM_AUDIO_OUTPUT_PROTECTION_IDS (wmdrmsdk. h)
description: La \_ \_ \_ structure des ID de protection de sortie audio DRM \_ contient une liste d’identificateurs de protection de sortie audio.
ms.assetid: 21972b18-334b-4a4d-812d-21cbfaf7cc58
keywords:
- Structure DRM_AUDIO_OUTPUT_PROTECTION_IDS format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d3c7142f5f575413f72885aa60a0ccb826ecfab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521719"
---
# <a name="drm_audio_output_protection_ids-structure"></a><span data-ttu-id="fdd5f-105">\_Structure des \_ \_ ID de protection de sortie audio DRM \_</span><span class="sxs-lookup"><span data-stu-id="fdd5f-105">DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS structure</span></span>

<span data-ttu-id="fdd5f-106">La structure des **\_ ID de \_ \_ protection \_ de sortie audio DRM** contient une liste d’identificateurs de protection de sortie audio.</span><span class="sxs-lookup"><span data-stu-id="fdd5f-106">The **DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS** structure contains a list of audio output protection identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdd5f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fdd5f-107">Syntax</span></span>


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION *rgAop;
} ;
```



## <a name="members"></a><span data-ttu-id="fdd5f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="fdd5f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="fdd5f-109">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="fdd5f-109">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="fdd5f-110">Nombre d’entrées dans le tableau **rgAop** .</span><span class="sxs-lookup"><span data-stu-id="fdd5f-110">Number of entries in the **rgAop** array.</span></span>

</dd> <dt>

<span data-ttu-id="fdd5f-111">**rgAop**</span><span class="sxs-lookup"><span data-stu-id="fdd5f-111">**rgAop**</span></span>
</dt> <dd>

<span data-ttu-id="fdd5f-112">Tableau de structures de **\_ \_ \_ protection de sortie audio DRM** .</span><span class="sxs-lookup"><span data-stu-id="fdd5f-112">Array of **DRM\_AUDIO\_OUTPUT\_PROTECTION** structures.</span></span> <span data-ttu-id="fdd5f-113">**DRM \_ La \_ \_ protection de sortie audio** est un type défini comme [**\_ \_ protection de sortie DRM**](drm-output-protection.md).</span><span class="sxs-lookup"><span data-stu-id="fdd5f-113">**DRM\_AUDIO\_OUTPUT\_PROTECTION** is a type defined as [**DRM\_OUTPUT\_PROTECTION**](drm-output-protection.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fdd5f-114">Notes</span><span class="sxs-lookup"><span data-stu-id="fdd5f-114">Remarks</span></span>

<span data-ttu-id="fdd5f-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fdd5f-115">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdd5f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fdd5f-116">Requirements</span></span>



| <span data-ttu-id="fdd5f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fdd5f-117">Requirement</span></span> | <span data-ttu-id="fdd5f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="fdd5f-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fdd5f-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="fdd5f-119">Header</span></span><br/> | <dl> <span data-ttu-id="fdd5f-120"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdd5f-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdd5f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fdd5f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdd5f-122">**\_ID de \_ protection de sortie audio DRM \_ \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="fdd5f-122">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="fdd5f-123">**\_ID de \_ protection de sortie vidéo \_ DRM \_**</span><span class="sxs-lookup"><span data-stu-id="fdd5f-123">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="fdd5f-124">**Structures**</span><span class="sxs-lookup"><span data-stu-id="fdd5f-124">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





