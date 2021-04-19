---
title: Structure WMDRMNET_POLICY (wmdrmsdk. h)
description: La structure de la \_ stratégie WMDRMNET contient la stratégie à utiliser pour les opérations DRM Windows Media pour les périphériques réseau.
ms.assetid: 11eaaeb2-3470-4f58-ae1c-53ee0f60bdce
keywords:
- Structure WMDRMNET_POLICY format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574e37a8c5ee7f68291012b86cda3a89e25949ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540941"
---
# <a name="wmdrmnet_policy-structure"></a><span data-ttu-id="120ff-105">Structure de la \_ stratégie WMDRMNET</span><span class="sxs-lookup"><span data-stu-id="120ff-105">WMDRMNET\_POLICY structure</span></span>

<span data-ttu-id="120ff-106">La structure de la **\_ stratégie WMDRMNET** contient la stratégie à utiliser pour les opérations DRM Windows Media pour les périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="120ff-106">The **WMDRMNET\_POLICY** structure contains the policy to be used for Windows Media DRM for Network Devices operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="120ff-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="120ff-107">Syntax</span></span>


```C++
typedef struct WMDRMNET_POLICY {
  WMDRMNET_POLICY_TYPE ePolicyType;
  BYTE                 *pbPolicy;
} ;
```



## <a name="members"></a><span data-ttu-id="120ff-108">Membres</span><span class="sxs-lookup"><span data-stu-id="120ff-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="120ff-109">**ePolicyType**</span><span class="sxs-lookup"><span data-stu-id="120ff-109">**ePolicyType**</span></span>
</dt> <dd>

<span data-ttu-id="120ff-110">Membre de l’énumération de [**\_ \_ type de stratégie WMDRMNET**](wmdrmnet-policy-type.md) qui spécifie le type de stratégie.</span><span class="sxs-lookup"><span data-stu-id="120ff-110">Member of the [**WMDRMNET\_POLICY\_TYPE**](wmdrmnet-policy-type.md) enumeration that specifies the type of policy.</span></span>

</dd> <dt>

<span data-ttu-id="120ff-111">**pbPolicy**</span><span class="sxs-lookup"><span data-stu-id="120ff-111">**pbPolicy**</span></span>
</dt> <dd>

<span data-ttu-id="120ff-112">Mémoire tampon contenant la stratégie.</span><span class="sxs-lookup"><span data-stu-id="120ff-112">Buffer containing the policy.</span></span> <span data-ttu-id="120ff-113">Le seul type de stratégie actuellement pris en charge est le **\_ type de stratégie WMDRMNET \_ \_ TRANSCRYPTPLAY**.</span><span class="sxs-lookup"><span data-stu-id="120ff-113">The only type of policy currently supported is **WMDRMNET\_POLICY\_TYPE\_TRANSCRYPTPLAY**.</span></span> <span data-ttu-id="120ff-114">Ce membre est un pointeur vers une structure de **\_ \_ TRANSCRYPTPLAY de stratégie WMDRMNET** .</span><span class="sxs-lookup"><span data-stu-id="120ff-114">This member is a pointer to a **WMDRMNET\_POLICY\_TRANSCRYPTPLAY** structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="120ff-115">Notes</span><span class="sxs-lookup"><span data-stu-id="120ff-115">Remarks</span></span>

<span data-ttu-id="120ff-116">Cette structure est utilisée en tant que paramètre pour la méthode [**IWMDRMNetTransmitter :: GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="120ff-116">This structure is used as a parameter for the [**IWMDRMNetTransmitter::GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="120ff-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="120ff-117">Requirements</span></span>



| <span data-ttu-id="120ff-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="120ff-118">Requirement</span></span> | <span data-ttu-id="120ff-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="120ff-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="120ff-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="120ff-120">Header</span></span><br/> | <dl> <span data-ttu-id="120ff-121"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="120ff-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="120ff-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="120ff-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="120ff-123">**Structures**</span><span class="sxs-lookup"><span data-stu-id="120ff-123">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="120ff-124">**\_ \_ exigences globales de la stratégie WMDRMNET \_**</span><span class="sxs-lookup"><span data-stu-id="120ff-124">**WMDRMNET\_POLICY\_GLOBAL\_REQUIREMENTS**</span></span>](wmdrmnet-policy-global-requirements.md)
</dt> <dt>

[<span data-ttu-id="120ff-125">**\_ \_ environnement minimal de la stratégie WMDRMNET \_**</span><span class="sxs-lookup"><span data-stu-id="120ff-125">**WMDRMNET\_POLICY\_MINIMUM\_ENVIRONMENT**</span></span>](wmdrmnet-policy-minimum-environment.md)
</dt> <dt>

[<span data-ttu-id="120ff-126">**\_stratégie WMDRMNET \_ TRANSCRYPTPLAY**</span><span class="sxs-lookup"><span data-stu-id="120ff-126">**WMDRMNET\_POLICY\_TRANSCRYPTPLAY**</span></span>](wmdrmnet-policy-transcryptplay.md)
</dt> <dt>

[<span data-ttu-id="120ff-127">**\_type de stratégie WMDRMNET \_**</span><span class="sxs-lookup"><span data-stu-id="120ff-127">**WMDRMNET\_POLICY\_TYPE**</span></span>](wmdrmnet-policy-type.md)
</dt> </dl>

 

 





