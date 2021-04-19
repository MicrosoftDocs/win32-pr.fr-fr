---
title: Énumération WMDRMNET_POLICY_TYPE (wmdrmsdk. h)
description: Le \_ \_ type d’énumération de type de stratégie WMDRMNET répertorie les types de stratégies qui sont disponibles pour les opérations DRM Windows Media pour les périphériques réseau.
ms.assetid: 83e9e247-3bd8-4857-97b6-95b3cd5ad25c
keywords:
- Format Windows Media d’énumération WMDRMNET_POLICY_TYPE
- Format Windows Media d’énumération
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 964a3e938caa312f02f21074f046f3cf88d72de6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539992"
---
# <a name="wmdrmnet_policy_type-enumeration"></a><span data-ttu-id="e28e8-105">\_Énumération des types de stratégie WMDRMNET \_</span><span class="sxs-lookup"><span data-stu-id="e28e8-105">WMDRMNET\_POLICY\_TYPE enumeration</span></span>

<span data-ttu-id="e28e8-106">Le type d’énumération de **\_ \_ type de stratégie WMDRMNET** répertorie les types de stratégies qui sont disponibles pour les opérations DRM Windows Media pour les périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="e28e8-106">The **WMDRMNET\_POLICY\_TYPE** enumeration type lists the types of policies that are available for Windows Media DRM for Network Devices operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="e28e8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e28e8-107">Syntax</span></span>


```C++
typedef enum WMDRMNET_POLICY_TYPE { 
  WMDRMNET_POLICY_TYPE_UNDEFINED       = 0x0000,
  WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY  = 0x0001
} ;
```



## <a name="constants"></a><span data-ttu-id="e28e8-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="e28e8-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e28e8-109"><span id="WMDRMNET_POLICY_TYPE_UNDEFINED"></span><span id="wmdrmnet_policy_type_undefined"></span>**\_type de stratégie WMDRMNET \_ \_ non défini**</span><span class="sxs-lookup"><span data-stu-id="e28e8-109"><span id="WMDRMNET_POLICY_TYPE_UNDEFINED"></span><span id="wmdrmnet_policy_type_undefined"></span>**WMDRMNET\_POLICY\_TYPE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="e28e8-110">Les types de stratégie non définis ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e28e8-110">Undefined policy types are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="e28e8-111"><span id="WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY"></span><span id="wmdrmnet_policy_type_transcryptplay"></span>**WMDRMNET \_ type de stratégie \_ \_ TRANSCRYPTPLAY**</span><span class="sxs-lookup"><span data-stu-id="e28e8-111"><span id="WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY"></span><span id="wmdrmnet_policy_type_transcryptplay"></span>**WMDRMNET\_POLICY\_TYPE\_TRANSCRYPTPLAY**</span></span>
</dt> <dd>

<span data-ttu-id="e28e8-112">La stratégie régit la possibilité de convertir le contenu protégé par Windows Media DRM en Windows Media DRM protégé pour les données des périphériques réseau et de le lire sur un appareil en réseau.</span><span class="sxs-lookup"><span data-stu-id="e28e8-112">The policy governs the ability to convert content protected by Windows Media DRM into protected Windows Media DRM for Network Devices data and play it back on a networked device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e28e8-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e28e8-113">Remarks</span></span>

<span data-ttu-id="e28e8-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e28e8-114">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="e28e8-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e28e8-115">Requirements</span></span>



| <span data-ttu-id="e28e8-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e28e8-116">Requirement</span></span> | <span data-ttu-id="e28e8-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e28e8-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e28e8-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="e28e8-118">Header</span></span><br/> | <dl> <span data-ttu-id="e28e8-119"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="e28e8-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e28e8-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e28e8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e28e8-121">**Types énumération**</span><span class="sxs-lookup"><span data-stu-id="e28e8-121">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> <dt>

[<span data-ttu-id="e28e8-122">**\_stratégie WMDRMNET**</span><span class="sxs-lookup"><span data-stu-id="e28e8-122">**WMDRMNET\_POLICY**</span></span>](wmdrmnet-policy.md)
</dt> </dl>

 

 





