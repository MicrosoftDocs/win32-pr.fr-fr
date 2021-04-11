---
title: Énumération WINBIO_ANTI_SPOOF_POLICY_ACTION ( \_ types WINBIO. h)
description: Spécifie les types d’actions que vous effectuez pour la stratégie d’antiusurpation d’un utilisateur.
ms.assetid: 846C0725-1796-49E4-883C-44AC7D618317
keywords:
- API Windows Biometric Framework de l’énumération WINBIO_ANTI_SPOOF_POLICY_ACTION
- API du pointeur d’énumération PWINBIO_ANTI_SPOOF_POLICY Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY_ACTION
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5905624bad252475cdde12c003f31a734e64dd2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942351"
---
# <a name="winbio_anti_spoof_policy_action-enumeration"></a><span data-ttu-id="fa5f0-105">\_ \_ \_ Énumération des actions de stratégie anti-usurpation WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="fa5f0-105">WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION enumeration</span></span>

<span data-ttu-id="fa5f0-106">Spécifie les types d’actions que vous effectuez pour la stratégie d’antiusurpation d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fa5f0-106">Specifies the types of actions you take for the antispoofing policy of a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa5f0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa5f0-107">Syntax</span></span>


```C++
typedef enum _WINBIO_ANTI_SPOOF_POLICY_ACTION { 
  WINBIO_ANTI_SPOOF_DISABLE  = 0x00000000,
  WINBIO_ANTI_SPOOF_ENABLE   = 0x00000001,
  WINBIO_ANTI_SPOOF_REMOVE   = 0x00000002
} WINBIO_ANTI_SPOOF_POLICY_ACTION, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="constants"></a><span data-ttu-id="fa5f0-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="fa5f0-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fa5f0-109"><span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**désactivation de la \_ protection contre l' \_ usurpation WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="fa5f0-109"><span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**WINBIO\_ANTI\_SPOOF\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="fa5f0-110">Désactive la détection de l’usurpation d’identité pour un facteur biométrique.</span><span class="sxs-lookup"><span data-stu-id="fa5f0-110">Turns off the detection of spoofing for a biometric factor.</span></span>

</dd> <dt>

<span data-ttu-id="fa5f0-111"><span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**WINBIO \_ anti- \_ usurpation \_ activée**</span><span class="sxs-lookup"><span data-stu-id="fa5f0-111"><span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**WINBIO\_ANTI\_SPOOF\_ENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="fa5f0-112">Active la détection de l’usurpation d’identité pour un facteur biométrique.</span><span class="sxs-lookup"><span data-stu-id="fa5f0-112">Turns on the detection of spoofing for a biometric factor.</span></span>

</dd> <dt>

<span data-ttu-id="fa5f0-113"><span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**WINBIO \_ anti- \_ usurpation \_**</span><span class="sxs-lookup"><span data-stu-id="fa5f0-113"><span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**WINBIO\_ANTI\_SPOOF\_REMOVE**</span></span>
</dt> <dd>

<span data-ttu-id="fa5f0-114">Supprime l’intégralité de la stratégie d’antiusurpation pour le facteur biométrique du compte.</span><span class="sxs-lookup"><span data-stu-id="fa5f0-114">Removes the entire antispoofing policy for the biometric factor from the account.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa5f0-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa5f0-115">Requirements</span></span>



| <span data-ttu-id="fa5f0-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa5f0-116">Requirement</span></span> | <span data-ttu-id="fa5f0-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa5f0-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa5f0-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa5f0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fa5f0-119">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa5f0-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="fa5f0-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa5f0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fa5f0-121">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa5f0-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="fa5f0-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="fa5f0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa5f0-123"><dt>WinBio \_ types. h (inclure WinBio. h pour les applications clientes ou les \_ cartes WinBio. h pour les adaptateurs)</dt></span><span class="sxs-lookup"><span data-stu-id="fa5f0-123"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa5f0-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa5f0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa5f0-125">**\_action de stratégie anti- \_ usurpation WINBIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fa5f0-125">**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**</span></span>](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[<span data-ttu-id="fa5f0-126">**SOURCE de la \_ stratégie WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="fa5f0-126">**WINBIO\_POLICY\_SOURCE**</span></span>](winbio-policy-source.md)
</dt> </dl>

 

 





