---
description: Définit des algorithmes pour le processeur vidéo qui est utilisé par \_ l' \_ algorithme de processeur vidéo MF \_ .
ms.assetid: 3BB0836E-39E6-40FA-9BA0-C986EB587CF1
title: Énumération MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
api_type:
- HeaderDef
api_location:
- mfidl.h
ms.openlocfilehash: 604fee61ae4b6a34d876de8c2863ee6dddad73d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516054"
---
# <a name="mf_video_processor_algorithm_type-enumeration"></a><span data-ttu-id="3d1d6-103">\_ \_ \_ Énumération des types d’algorithmes de processeur vidéo MF \_</span><span class="sxs-lookup"><span data-stu-id="3d1d6-103">MF\_VIDEO\_PROCESSOR\_ALGORITHM\_TYPE enumeration</span></span>

<span data-ttu-id="3d1d6-104">Définit des algorithmes pour le processeur vidéo qui est utilisé par l' [ \_ \_ \_ algorithme de processeur vidéo MF](mf-video-processor-algorithm.md).</span><span class="sxs-lookup"><span data-stu-id="3d1d6-104">Defines algorithms for the video processor which is use by [MF\_VIDEO\_PROCESSOR\_ALGORITHM](mf-video-processor-algorithm.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3d1d6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d1d6-105">Syntax</span></span>


```C++
typedef enum _MF_VIDEO_PROCESSOR_ALGORITHM_TYPE { 
  MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT      = 0,
  MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444  = 1
} MF_VIDEO_PROCESSOR_ALGORITHM_TYPE;
```



## <a name="constants"></a><span data-ttu-id="3d1d6-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="3d1d6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3d1d6-107"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT"></span><span id="mf_video_processor_algorithm_default"></span>**\_ \_ algorithme de processeur vidéo MF \_ \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="3d1d6-107"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT"></span><span id="mf_video_processor_algorithm_default"></span>**MF\_VIDEO\_PROCESSOR\_ALGORITHM\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="3d1d6-108">le mode par défaut favorise un équilibre entre qualité et vitesse</span><span class="sxs-lookup"><span data-stu-id="3d1d6-108">default mode favors a balance of quality and speed</span></span>

</dd> <dt>

<span data-ttu-id="3d1d6-109"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444"></span><span id="mf_video_processor_algorithm_mrf_crf_444"></span>**\_ \_ Algorithme de processeur vidéo MF \_ \_ MRF \_ CRF \_ 444**</span><span class="sxs-lookup"><span data-stu-id="3d1d6-109"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444"></span><span id="mf_video_processor_algorithm_mrf_crf_444"></span>**MF\_VIDEO\_PROCESSOR\_ALGORITHM\_MRF\_CRF\_444**</span></span>
</dt> <dd>

<span data-ttu-id="3d1d6-110">Le processeur vidéo est toujours traité en interne dans AYUV et utilise des filtres de haute qualité.</span><span class="sxs-lookup"><span data-stu-id="3d1d6-110">The video processor will always internally process in AYUV and use high quality filters.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3d1d6-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d1d6-111">Requirements</span></span>



| <span data-ttu-id="3d1d6-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d1d6-112">Requirement</span></span> | <span data-ttu-id="3d1d6-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d1d6-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3d1d6-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d1d6-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3d1d6-115">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3d1d6-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3d1d6-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d1d6-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3d1d6-117">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3d1d6-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3d1d6-118">MIDL</span><span class="sxs-lookup"><span data-stu-id="3d1d6-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3d1d6-119"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3d1d6-119"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d1d6-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d1d6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d1d6-121">Énumérations de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3d1d6-121">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




