---
title: Structure WMDRM_ANALOG_VIDEO_RESTRICTIONS (wmdrmsdk. h)
description: La \_ \_ \_ structure des restrictions de la vidéo de l’entrée WMDRM contient des informations sur une restriction pour la diffusion de contenu en tant que vidéo analogique.
ms.assetid: 13b38115-bd18-45b9-a1d5-542e043a4bde
keywords:
- Structure WMDRM_ANALOG_VIDEO_RESTRICTIONS format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3d6b8fe957468baebb6da06f45ba7b37756413c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539613"
---
# <a name="wmdrm_analog_video_restrictions-structure"></a><span data-ttu-id="3ab6b-105">Structure des restrictions de la \_ vidéo analogique WMDRM \_ \_</span><span class="sxs-lookup"><span data-stu-id="3ab6b-105">WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS structure</span></span>

<span data-ttu-id="3ab6b-106">La structure des **\_ \_ \_ restrictions** de la vidéo de l’entrée WMDRM contient des informations sur une restriction pour la diffusion de contenu en tant que vidéo analogique.</span><span class="sxs-lookup"><span data-stu-id="3ab6b-106">The **WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS** structure holds information about a restriction for playing back content as analog video.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ab6b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ab6b-107">Syntax</span></span>


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS {
  GUID  guidRestrictionID;
  DWORD dwRestrictionData;
} ;
```



## <a name="members"></a><span data-ttu-id="3ab6b-108">Membres</span><span class="sxs-lookup"><span data-stu-id="3ab6b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3ab6b-109">**guidRestrictionID**</span><span class="sxs-lookup"><span data-stu-id="3ab6b-109">**guidRestrictionID**</span></span>
</dt> <dd>

<span data-ttu-id="3ab6b-110">Identificateur de restriction.</span><span class="sxs-lookup"><span data-stu-id="3ab6b-110">Restriction identifier.</span></span>

</dd> <dt>

<span data-ttu-id="3ab6b-111">**dwRestrictionData**</span><span class="sxs-lookup"><span data-stu-id="3ab6b-111">**dwRestrictionData**</span></span>
</dt> <dd>

<span data-ttu-id="3ab6b-112">Données de restriction.</span><span class="sxs-lookup"><span data-stu-id="3ab6b-112">Restriction data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ab6b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="3ab6b-113">Remarks</span></span>

<span data-ttu-id="3ab6b-114">Cette structure est reçue quand vous appelez [**IWMDRMLicense :: GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md).</span><span class="sxs-lookup"><span data-stu-id="3ab6b-114">This structure is received when you call [**IWMDRMLicense::GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ab6b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ab6b-115">Requirements</span></span>



| <span data-ttu-id="3ab6b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ab6b-116">Requirement</span></span> | <span data-ttu-id="3ab6b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ab6b-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ab6b-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="3ab6b-118">Header</span></span><br/> | <dl> <span data-ttu-id="3ab6b-119"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ab6b-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ab6b-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ab6b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ab6b-121">**Structures**</span><span class="sxs-lookup"><span data-stu-id="3ab6b-121">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="3ab6b-122">**RESTRICTIONS de la \_ vidéo analogique WMDRM \_ \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="3ab6b-122">**WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS\_EX**</span></span>](wmdrm-analog-video-restrictions-ex.md)
</dt> </dl>

 

 





