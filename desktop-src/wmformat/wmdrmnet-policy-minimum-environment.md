---
title: Structure WMDRMNET_POLICY_MINIMUM_ENVIRONMENT (wmdrmsdk. h)
description: La \_ structure d’environnement minimale de la stratégie WMDRMNET \_ \_ contient les exigences de sécurité minimales pour Windows Media DRM pour les périphériques réseau.
ms.assetid: b1bc9a8d-197e-45fe-a152-0b81add977eb
keywords:
- Structure WMDRMNET_POLICY_MINIMUM_ENVIRONMENT format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_MINIMUM_ENVIRONMENT
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf53fdec186a44eff375dd2e9cf9badfe0ba715
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538139"
---
# <a name="wmdrmnet_policy_minimum_environment-structure"></a><span data-ttu-id="7f6a4-105">\_Structure d' \_ \_ environnement minimale de la stratégie WMDRMNET</span><span class="sxs-lookup"><span data-stu-id="7f6a4-105">WMDRMNET\_POLICY\_MINIMUM\_ENVIRONMENT structure</span></span>

<span data-ttu-id="7f6a4-106">La structure d' **\_ \_ \_ environnement minimale de la stratégie WMDRMNET** contient les exigences de sécurité minimales pour Windows Media DRM pour les périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="7f6a4-106">The **WMDRMNET\_POLICY\_MINIMUM\_ENVIRONMENT** structure contains the minimum security requirements for Windows Media DRM for Network Devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f6a4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f6a4-107">Syntax</span></span>


```C++
typedef struct WMDRMNET_POLICY_MINIMUM_ENVIRONMENT {
  WORD  wMinimumSecurityLevel;
  DWORD dwMinimumAppRevocationListVersion;
  DWORD dwMinimumDeviceRevocationListVersion;
} ;
```



## <a name="members"></a><span data-ttu-id="7f6a4-108">Membres</span><span class="sxs-lookup"><span data-stu-id="7f6a4-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7f6a4-109">**wMinimumSecurityLevel**</span><span class="sxs-lookup"><span data-stu-id="7f6a4-109">**wMinimumSecurityLevel**</span></span>
</dt> <dd>

<span data-ttu-id="7f6a4-110">Niveau de sécurité d’application minimal requis.</span><span class="sxs-lookup"><span data-stu-id="7f6a4-110">Minimum application security level required.</span></span>

</dd> <dt>

<span data-ttu-id="7f6a4-111">**dwMinimumAppRevocationListVersion**</span><span class="sxs-lookup"><span data-stu-id="7f6a4-111">**dwMinimumAppRevocationListVersion**</span></span>
</dt> <dd>

<span data-ttu-id="7f6a4-112">Version minimale de la liste de révocation des certificats d’application requise.</span><span class="sxs-lookup"><span data-stu-id="7f6a4-112">Minimum application certificate revocation list version required.</span></span>

</dd> <dt>

<span data-ttu-id="7f6a4-113">**dwMinimumDeviceRevocationListVersion**</span><span class="sxs-lookup"><span data-stu-id="7f6a4-113">**dwMinimumDeviceRevocationListVersion**</span></span>
</dt> <dd>

<span data-ttu-id="7f6a4-114">Configuration minimale requise pour la liste de révocation des certificats d’appareil.</span><span class="sxs-lookup"><span data-stu-id="7f6a4-114">Minimum device certificate revocation list required.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f6a4-115">Notes</span><span class="sxs-lookup"><span data-stu-id="7f6a4-115">Remarks</span></span>

<span data-ttu-id="7f6a4-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7f6a4-116">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f6a4-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f6a4-117">Requirements</span></span>



| <span data-ttu-id="7f6a4-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f6a4-118">Requirement</span></span> | <span data-ttu-id="7f6a4-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f6a4-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7f6a4-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f6a4-120">Header</span></span><br/> | <dl> <span data-ttu-id="7f6a4-121"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f6a4-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f6a4-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f6a4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f6a4-123">**Structures**</span><span class="sxs-lookup"><span data-stu-id="7f6a4-123">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="7f6a4-124">**\_stratégie WMDRMNET**</span><span class="sxs-lookup"><span data-stu-id="7f6a4-124">**WMDRMNET\_POLICY**</span></span>](wmdrmnet-policy.md)
</dt> </dl>

 

 





