---
title: Structure DRM_OUTPUT_PROTECTION_EX (wmdrmsdk. h)
description: La \_ structure de protection de sortie DRM \_ \_ ex contient des informations sur une technologie de protection de sortie. Cette structure étend \_ \_ la protection de la sortie DRM en ajoutant un numéro de version.
ms.assetid: eeebf5da-172b-4781-8c44-00504a6961bf
keywords:
- Structure DRM_OUTPUT_PROTECTION_EX format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeadbb845dc115b1faff858fe3a6ba0064eb425e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533455"
---
# <a name="drm_output_protection_ex-structure"></a><span data-ttu-id="a0430-106">\_Protection de sortie DRM \_ \_ ex structure</span><span class="sxs-lookup"><span data-stu-id="a0430-106">DRM\_OUTPUT\_PROTECTION\_EX structure</span></span>

<span data-ttu-id="a0430-107">La structure de **\_ protection de sortie DRM \_ \_ ex** contient des informations sur une technologie de protection de sortie.</span><span class="sxs-lookup"><span data-stu-id="a0430-107">The **DRM\_OUTPUT\_PROTECTION\_EX** structure holds information about an output protection technology.</span></span> <span data-ttu-id="a0430-108">Cette structure étend **la \_ \_ protection de la sortie DRM** en ajoutant un numéro de version.</span><span class="sxs-lookup"><span data-stu-id="a0430-108">This structure extends **DRM\_OUTPUT\_PROTECTION** by adding a version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0430-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0430-109">Syntax</span></span>


```C++
typedef struct DRM_OUTPUT_PROTECTION_EX {
  DWORD dwVersion;
  GUID  guidId;
  DWORD dwConfigData;
} ;
```



## <a name="members"></a><span data-ttu-id="a0430-110">Membres</span><span class="sxs-lookup"><span data-stu-id="a0430-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="a0430-111">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="a0430-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="a0430-112">Numéro de version.</span><span class="sxs-lookup"><span data-stu-id="a0430-112">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="a0430-113">**Guidid ne**</span><span class="sxs-lookup"><span data-stu-id="a0430-113">**guidId**</span></span>
</dt> <dd>

<span data-ttu-id="a0430-114">GUID identifiant la technologie de protection de sortie.</span><span class="sxs-lookup"><span data-stu-id="a0430-114">GUID identifying the output protection technology.</span></span>

</dd> <dt>

<span data-ttu-id="a0430-115">**dwConfigData**</span><span class="sxs-lookup"><span data-stu-id="a0430-115">**dwConfigData**</span></span>
</dt> <dd>

<span data-ttu-id="a0430-116">Données de configuration pour la technologie.</span><span class="sxs-lookup"><span data-stu-id="a0430-116">Configuration data for the technology.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a0430-117">Notes</span><span class="sxs-lookup"><span data-stu-id="a0430-117">Remarks</span></span>

<span data-ttu-id="a0430-118">**DRM \_ La protection de sortie AUDIO par \_ \_ \_ exemple** et la **\_ \_ protection de sortie vidéo \_ \_ DRM** , par exemple, sont définies comme **\_ \_ protection de sortie DRM** dans les instructions **typedef** .</span><span class="sxs-lookup"><span data-stu-id="a0430-118">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_EX** and **DRM\_VIDEO\_OUTPUT\_PROTECTION\_EX** are both defined as **DRM\_OUTPUT\_PROTECTION** in **typedef** statements.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0430-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0430-119">Requirements</span></span>



| <span data-ttu-id="a0430-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0430-120">Requirement</span></span> | <span data-ttu-id="a0430-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0430-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0430-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="a0430-122">Header</span></span><br/> | <dl> <span data-ttu-id="a0430-123"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0430-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0430-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0430-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0430-125">**\_protection de sortie DRM \_**</span><span class="sxs-lookup"><span data-stu-id="a0430-125">**DRM\_OUTPUT\_PROTECTION**</span></span>](drm-output-protection.md)
</dt> <dt>

[<span data-ttu-id="a0430-126">**Structures**</span><span class="sxs-lookup"><span data-stu-id="a0430-126">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





