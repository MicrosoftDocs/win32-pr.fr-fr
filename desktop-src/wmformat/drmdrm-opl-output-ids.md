---
title: Structure DRM_OPL_OUTPUT_IDS (wmdrmsdk. h)
description: La \_ \_ \_ structure des ID de sortie DRM OPL contient un certain nombre d’identificateurs de sortie de niveau de protection de sortie (OPL).
ms.assetid: 3627f2a7-1cea-400b-82e7-678898ccc386
keywords:
- Structure DRM_OPL_OUTPUT_IDS format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_OPL_OUTPUT_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 802787c5e373c837d639e0225bf650d80c105970
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525536"
---
# <a name="drm_opl_output_ids-structure"></a><span data-ttu-id="45914-105">\_Structure des \_ ID de sortie DRM OPL \_</span><span class="sxs-lookup"><span data-stu-id="45914-105">DRM\_OPL\_OUTPUT\_IDS structure</span></span>

<span data-ttu-id="45914-106">La structure des **\_ ID de \_ sortie \_ DRM OPL** contient un certain nombre d’identificateurs de sortie de niveau de protection de sortie (OPL).</span><span class="sxs-lookup"><span data-stu-id="45914-106">The **DRM\_OPL\_OUTPUT\_IDS** structure holds a number of output protection level (OPL) output identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="45914-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45914-107">Syntax</span></span>


```C++
typedef struct DRM_OPL_OUTPUT_IDS {
  WORD cIds;
  GUID *rgIds;
} ;
```



## <a name="members"></a><span data-ttu-id="45914-108">Membres</span><span class="sxs-lookup"><span data-stu-id="45914-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="45914-109">**CID**</span><span class="sxs-lookup"><span data-stu-id="45914-109">**cIds**</span></span>
</dt> <dd>

<span data-ttu-id="45914-110">Nombre d’identificateurs dans le tableau référencé par **rgIds**.</span><span class="sxs-lookup"><span data-stu-id="45914-110">Number of identifiers in the array referenced by **rgIds**.</span></span>

</dd> <dt>

<span data-ttu-id="45914-111">**rgIds**</span><span class="sxs-lookup"><span data-stu-id="45914-111">**rgIds**</span></span>
</dt> <dd>

<span data-ttu-id="45914-112">Adresse d’un tableau de GUID.</span><span class="sxs-lookup"><span data-stu-id="45914-112">Address of an array of GUIDs.</span></span> <span data-ttu-id="45914-113">Chaque membre du tableau contient un identificateur de sortie OPL.</span><span class="sxs-lookup"><span data-stu-id="45914-113">Each member of the array contains an OPL output identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45914-114">Notes</span><span class="sxs-lookup"><span data-stu-id="45914-114">Remarks</span></span>

<span data-ttu-id="45914-115">Cette structure est utilisée en tant que membre des structures [**DRM \_ Copy \_ OPL**](drmdrm-copy-opl.md) et [**DRM \_ Play \_ OPL**](drmdrm-play-opl.md) pour identifier les groupes d’identificateurs de sortie.</span><span class="sxs-lookup"><span data-stu-id="45914-115">This structure is used as a member of the [**DRM\_COPY\_OPL**](drmdrm-copy-opl.md) and [**DRM\_PLAY\_OPL**](drmdrm-play-opl.md) structures to identify groups of output identifiers.</span></span>

## <a name="requirements"></a><span data-ttu-id="45914-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45914-116">Requirements</span></span>



| <span data-ttu-id="45914-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45914-117">Requirement</span></span> | <span data-ttu-id="45914-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="45914-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="45914-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="45914-119">Header</span></span><br/> | <dl> <span data-ttu-id="45914-120"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="45914-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45914-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45914-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45914-122">**Structures**</span><span class="sxs-lookup"><span data-stu-id="45914-122">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





