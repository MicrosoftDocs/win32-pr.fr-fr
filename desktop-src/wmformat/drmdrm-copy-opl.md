---
title: Structure DRM_COPY_OPL (wmdrmsdk. h)
description: La \_ \_ structure OPL de la copie DRM contient des informations sur les niveaux de protection de sortie (OPLs) spécifiés dans une licence pour les actions de copie.
ms.assetid: 439cbd56-05c1-46f8-86b9-ac1341902a40
keywords:
- Structure DRM_COPY_OPL format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_COPY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28655e220588bb704567de033e1117dd569d3ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521653"
---
# <a name="drm_copy_opl-structure"></a><span data-ttu-id="a1bf9-105">\_ \_ Structure OPL de la copie DRM</span><span class="sxs-lookup"><span data-stu-id="a1bf9-105">DRM\_COPY\_OPL structure</span></span>

<span data-ttu-id="a1bf9-106">La **structure \_ \_ OPL de la copie DRM** contient des informations sur les niveaux de protection de sortie (OPLs) spécifiés dans une licence pour les actions de copie.</span><span class="sxs-lookup"><span data-stu-id="a1bf9-106">The **DRM\_COPY\_OPL** structure holds information about the output protection levels (OPLs) specified in a license for copy actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1bf9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1bf9-107">Syntax</span></span>


```C++
typedef struct DRM_COPY_OPL {
  WORD               wMinimumCopyLevel;
  DRM_OPL_OUTPUT_IDS oplIdIncludes;
  DRM_OPL_OUTPUT_IDS oplIdExcludes;
} ;
```



## <a name="members"></a><span data-ttu-id="a1bf9-108">Membres</span><span class="sxs-lookup"><span data-stu-id="a1bf9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a1bf9-109">**wMinimumCopyLevel**</span><span class="sxs-lookup"><span data-stu-id="a1bf9-109">**wMinimumCopyLevel**</span></span>
</dt> <dd>

<span data-ttu-id="a1bf9-110">OPL minimal pour les actions de copie.</span><span class="sxs-lookup"><span data-stu-id="a1bf9-110">Minimum OPL for copy actions.</span></span>

</dd> <dt>

<span data-ttu-id="a1bf9-111">**oplIdIncludes**</span><span class="sxs-lookup"><span data-stu-id="a1bf9-111">**oplIdIncludes**</span></span>
</dt> <dd>

<span data-ttu-id="a1bf9-112">[**DRM \_ OPL \_ structure \_ ID de sortie**](drmdrm-opl-output-ids.md) contenant les identificateurs des technologies à autoriser.</span><span class="sxs-lookup"><span data-stu-id="a1bf9-112">[**DRM\_OPL\_OUTPUT\_IDS**](drmdrm-opl-output-ids.md) structure containing the identifiers of technologies to allow.</span></span> <span data-ttu-id="a1bf9-113">Ce membre est utilisé pour les technologies de sortie qui sont affectées OPLs inférieur au niveau de copie minimal, mais sur lequel le contenu peut être copié.</span><span class="sxs-lookup"><span data-stu-id="a1bf9-113">This member is used for output technologies that are assigned OPLs lower than the minimum copy level, but to which the content may be copied.</span></span>

</dd> <dt>

<span data-ttu-id="a1bf9-114">**oplIdExcludes**</span><span class="sxs-lookup"><span data-stu-id="a1bf9-114">**oplIdExcludes**</span></span>
</dt> <dd>

<span data-ttu-id="a1bf9-115">[**DRM \_ OPL \_ structure \_ ID de sortie**](drmdrm-opl-output-ids.md) contenant les identificateurs de sortie des technologies à restreindre.</span><span class="sxs-lookup"><span data-stu-id="a1bf9-115">[**DRM\_OPL\_OUTPUT\_IDS**](drmdrm-opl-output-ids.md) structure containing the output identifiers of technologies to restrict.</span></span> <span data-ttu-id="a1bf9-116">Ce membre est utilisé pour les technologies de sortie auxquelles sont affectées des OPLs qui dépassent le niveau de copie minimal, mais que l’émetteur de licence n’accorde pas de droits pour la copie vers.</span><span class="sxs-lookup"><span data-stu-id="a1bf9-116">This member is used for output technologies that are assigned OPLs that exceed the minimum copy level, but that the license issuer does not grant rights for copying to.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1bf9-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1bf9-117">Requirements</span></span>



| <span data-ttu-id="a1bf9-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1bf9-118">Requirement</span></span> | <span data-ttu-id="a1bf9-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1bf9-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1bf9-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="a1bf9-120">Header</span></span><br/> | <dl> <span data-ttu-id="a1bf9-121"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1bf9-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1bf9-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1bf9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1bf9-123">**\_OPL de lecture DRM \_**</span><span class="sxs-lookup"><span data-stu-id="a1bf9-123">**DRM\_PLAY\_OPL**</span></span>](drmdrm-play-opl.md)
</dt> <dt>

[<span data-ttu-id="a1bf9-124">**Structures**</span><span class="sxs-lookup"><span data-stu-id="a1bf9-124">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





