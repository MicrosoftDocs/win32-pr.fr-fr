---
title: WINBIO_ACCOUNT_POLICY structure (WinBio \_ adapter. h)
description: Contient une stratégie d’antiusurpation propre à la valeur par défaut ou spécifique au compte.
ms.assetid: 7098FC53-E487-42B2-8B4B-EB7E2D296CB6
keywords:
- API de Windows Biometric Framework de structure de WINBIO_ACCOUNT_POLICY
- API du pointeur de structure PWINBIO_ACCOUNT_POLICY Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_ACCOUNT_POLICY
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c734fa6d98615b7708a65ebad1dddc47cdc77cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942123"
---
# <a name="winbio_account_policy-structure"></a><span data-ttu-id="a71aa-105">Structure de stratégie de \_ compte WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="a71aa-105">WINBIO\_ACCOUNT\_POLICY structure</span></span>

<span data-ttu-id="a71aa-106">La structure de la **\_ \_ stratégie de compte WINBIO** contient une stratégie de lutte contre l’usurpation d’identité spécifique au compte ou à la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="a71aa-106">The **WINBIO\_ACCOUNT\_POLICY** structure contains either a default or account-specific antispoofing policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="a71aa-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a71aa-107">Syntax</span></span>


```C++
typedef struct _WINBIO_ACCOUNT_POLICY {
  WINBIO_IDENTITY                 Identity;
  WINBIO_ANTI_SPOOF_POLICY_ACTION AntiSpoofBehavior;
} WINBIO_ACCOUNT_POLICY, *PWINBIO_ACCOUNT_POLICY;
```



## <a name="members"></a><span data-ttu-id="a71aa-108">Membres</span><span class="sxs-lookup"><span data-stu-id="a71aa-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a71aa-109">**Identité**</span><span class="sxs-lookup"><span data-stu-id="a71aa-109">**Identity**</span></span>
</dt> <dd>

<span data-ttu-id="a71aa-110">Structure [**d' \_ identité WINBIO**](winbio-identity.md) qui spécifie les informations de compte.</span><span class="sxs-lookup"><span data-stu-id="a71aa-110">A [**WINBIO\_IDENTITY**](winbio-identity.md) structure that specifies the account information.</span></span>

</dd> <dt>

<span data-ttu-id="a71aa-111">**AntiSpoofBehavior**</span><span class="sxs-lookup"><span data-stu-id="a71aa-111">**AntiSpoofBehavior**</span></span>
</dt> <dd>

<span data-ttu-id="a71aa-112">L’une des valeurs d’énumération d' [**\_ \_ action de \_ stratégie \_ anti-usurpation WINBIO**](winbio-anti-spoof-policy-action.md) qui spécifie l’action de stratégie d’usurpation d’identité à utiliser pour le compte.</span><span class="sxs-lookup"><span data-stu-id="a71aa-112">One of the [**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**](winbio-anti-spoof-policy-action.md) enumeration values that specifies what antispoofing policy action to use for the account.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a71aa-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a71aa-113">Remarks</span></span>

<span data-ttu-id="a71aa-114">Pour obtenir une description de l’utilisation de cette structure, consultez la rubrique relative à la méthode [**EngineAdapterSetAccountPolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) .</span><span class="sxs-lookup"><span data-stu-id="a71aa-114">See the discussion of the [**EngineAdapterSetAccountPolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) method for a description of how this structure is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="a71aa-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a71aa-115">Requirements</span></span>



| <span data-ttu-id="a71aa-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a71aa-116">Requirement</span></span> | <span data-ttu-id="a71aa-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a71aa-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a71aa-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a71aa-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a71aa-119">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a71aa-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="a71aa-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a71aa-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a71aa-121">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a71aa-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="a71aa-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="a71aa-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a71aa-123"><dt>WinBio \_ adaptateur. h (include WinBio \_ adapter. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a71aa-123"><dt>Winbio\_adapter.h (include Winbio\_adapter.h)</dt></span></span> </dl> |



 

 





