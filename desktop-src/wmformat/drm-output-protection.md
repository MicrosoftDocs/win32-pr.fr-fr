---
title: Structure DRM_OUTPUT_PROTECTION (wmdrmsdk. h)
description: La \_ structure protection de la sortie DRM contient des \_ informations sur une technologie de protection de sortie.
ms.assetid: e458013d-b77e-4e03-bff9-e3ecfc72ebdb
keywords:
- Structure DRM_OUTPUT_PROTECTION format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a10428d86503e952dc82a7d45bddc11f5dd1286
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537537"
---
# <a name="drm_output_protection-structure"></a><span data-ttu-id="10147-105">Structure de protection de \_ sortie DRM \_</span><span class="sxs-lookup"><span data-stu-id="10147-105">DRM\_OUTPUT\_PROTECTION structure</span></span>

<span data-ttu-id="10147-106">La **structure \_ \_ protection de la sortie DRM** contient des informations sur une technologie de protection de sortie.</span><span class="sxs-lookup"><span data-stu-id="10147-106">The **DRM\_OUTPUT\_PROTECTION** structure holds information about an output protection technology.</span></span>

## <a name="syntax"></a><span data-ttu-id="10147-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10147-107">Syntax</span></span>


```C++
typedef struct DRM_OUTPUT_PROTECTION {
  GUID guidId;
  BYTE bConfigData;
} ;
```



## <a name="members"></a><span data-ttu-id="10147-108">Membres</span><span class="sxs-lookup"><span data-stu-id="10147-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="10147-109">**Guidid ne**</span><span class="sxs-lookup"><span data-stu-id="10147-109">**guidId**</span></span>
</dt> <dd>

<span data-ttu-id="10147-110">GUID identifiant la technologie de protection de sortie.</span><span class="sxs-lookup"><span data-stu-id="10147-110">GUID identifying the output protection technology.</span></span>

</dd> <dt>

<span data-ttu-id="10147-111">**bConfigData**</span><span class="sxs-lookup"><span data-stu-id="10147-111">**bConfigData**</span></span>
</dt> <dd>

<span data-ttu-id="10147-112">Données de configuration pour la technologie.</span><span class="sxs-lookup"><span data-stu-id="10147-112">Configuration data for the technology.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10147-113">Notes</span><span class="sxs-lookup"><span data-stu-id="10147-113">Remarks</span></span>

<span data-ttu-id="10147-114">**DRM \_ La \_ \_** protection de sortie audio et la protection de sortie de la **\_ vidéo \_ \_ DRM** sont toutes deux définies comme **\_ \_ protection de sortie DRM** dans les instructions **typedef** .</span><span class="sxs-lookup"><span data-stu-id="10147-114">**DRM\_AUDIO\_OUTPUT\_PROTECTION** and **DRM\_VIDEO\_OUTPUT\_PROTECTION** are both defined as **DRM\_OUTPUT\_PROTECTION** in **typedef** statements.</span></span>

## <a name="requirements"></a><span data-ttu-id="10147-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10147-115">Requirements</span></span>



| <span data-ttu-id="10147-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10147-116">Requirement</span></span> | <span data-ttu-id="10147-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="10147-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10147-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="10147-118">Header</span></span><br/> | <dl> <span data-ttu-id="10147-119"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="10147-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10147-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10147-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10147-121">**PROTECTION de la sortie DRM par \_ \_ \_ exemple**</span><span class="sxs-lookup"><span data-stu-id="10147-121">**DRM\_OUTPUT\_PROTECTION\_EX**</span></span>](drm-output-protection-ex.md)
</dt> <dt>

[<span data-ttu-id="10147-122">**Structures**</span><span class="sxs-lookup"><span data-stu-id="10147-122">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





