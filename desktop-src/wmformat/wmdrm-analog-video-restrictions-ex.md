---
title: Structure WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX (wmdrmsdk. h)
description: La \_ \_ \_ structure ex des restrictions de la vidéo analogique WMDRM \_ contient des informations étendues sur une restriction pour la diffusion de contenu sous forme de vidéo analogique.
ms.assetid: fe9092fe-a717-4377-9653-1cc07795319f
keywords:
- Structure WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59c9ca5f58cf2adadeb5a6a0618457472cde976c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545416"
---
# <a name="wmdrm_analog_video_restrictions_ex-structure"></a><span data-ttu-id="664b4-105">Limites de la \_ vidéo analogique WMDRM \_ \_ \_ ex structure</span><span class="sxs-lookup"><span data-stu-id="664b4-105">WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS\_EX structure</span></span>

<span data-ttu-id="664b4-106">La structure ex des restrictions de la **\_ \_ vidéo \_ \_ analogique WMDRM** contient des informations étendues sur une restriction pour la diffusion de contenu sous forme de vidéo analogique.</span><span class="sxs-lookup"><span data-stu-id="664b4-106">The **WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS\_EX** structure holds extended information about a restriction for playing back content as analog video.</span></span>

## <a name="syntax"></a><span data-ttu-id="664b4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="664b4-107">Syntax</span></span>


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX {
  DWORD dwVersion;
  GUID  guidRestrictionID;
  DWORD cbRestrictionData;
  BYTE  *pbRestrictionData;
} ;
```



## <a name="members"></a><span data-ttu-id="664b4-108">Membres</span><span class="sxs-lookup"><span data-stu-id="664b4-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="664b4-109">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="664b4-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="664b4-110">Numéro de version.</span><span class="sxs-lookup"><span data-stu-id="664b4-110">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="664b4-111">**guidRestrictionID**</span><span class="sxs-lookup"><span data-stu-id="664b4-111">**guidRestrictionID**</span></span>
</dt> <dd>

<span data-ttu-id="664b4-112">ID de restriction.</span><span class="sxs-lookup"><span data-stu-id="664b4-112">Restriction ID.</span></span>

</dd> <dt>

<span data-ttu-id="664b4-113">**cbRestrictionData**</span><span class="sxs-lookup"><span data-stu-id="664b4-113">**cbRestrictionData**</span></span>
</dt> <dd>

<span data-ttu-id="664b4-114">Taille des données de restriction en octets.</span><span class="sxs-lookup"><span data-stu-id="664b4-114">Size of restriction data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="664b4-115">**pbRestrictionData**</span><span class="sxs-lookup"><span data-stu-id="664b4-115">**pbRestrictionData**</span></span>
</dt> <dd>

<span data-ttu-id="664b4-116">Données de restriction.</span><span class="sxs-lookup"><span data-stu-id="664b4-116">Restriction data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="664b4-117">Notes</span><span class="sxs-lookup"><span data-stu-id="664b4-117">Remarks</span></span>

<span data-ttu-id="664b4-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="664b4-118">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="664b4-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="664b4-119">Requirements</span></span>



| <span data-ttu-id="664b4-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="664b4-120">Requirement</span></span> | <span data-ttu-id="664b4-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="664b4-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="664b4-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="664b4-122">Header</span></span><br/> | <dl> <span data-ttu-id="664b4-123"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="664b4-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="664b4-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="664b4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="664b4-125">**Structures**</span><span class="sxs-lookup"><span data-stu-id="664b4-125">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="664b4-126">**RESTRICTIONS de la \_ vidéo analogique WMDRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="664b4-126">**WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS**</span></span>](wmdrm-analog-video-restrictions.md)
</dt> </dl>

 

 





