---
title: Structure WINBIO_ANTI_SPOOF_POLICY ( \_ types WINBIO. h)
description: Représente la stratégie d’antiusurpation pour un utilisateur.
ms.assetid: 2B433AE8-21A0-4AF1-853C-9074527DB2E4
keywords:
- API de Windows Biometric Framework de structure de WINBIO_ANTI_SPOOF_POLICY
- API du pointeur de structure PWINBIO_ANTI_SPOOF_POLICY Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3da8b7811afb1de1ad464675125f125ef0ceab73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465830"
---
# <a name="winbio_anti_spoof_policy-structure"></a><span data-ttu-id="d6a97-105">\_Structure de stratégie anti- \_ usurpation WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="d6a97-105">WINBIO\_ANTI\_SPOOF\_POLICY structure</span></span>

<span data-ttu-id="d6a97-106">Représente la stratégie d’antiusurpation pour un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d6a97-106">Represents the antispoofing policy for a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6a97-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6a97-107">Syntax</span></span>


```C++
typedef struct _WINBIO_ANTI_SPOOF_POLICY {
  WINBIO_ANTI_SPOOF_POLICY_ACTION Action;
  WINBIO_POLICY_SOURCE            Source;
} WINBIO_ANTI_SPOOF_POLICY, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="members"></a><span data-ttu-id="d6a97-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d6a97-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d6a97-109">**Action**</span><span class="sxs-lookup"><span data-stu-id="d6a97-109">**Action**</span></span>
</dt> <dd>

<span data-ttu-id="d6a97-110">Type d’action à entreprendre pour la stratégie d’antiusurpation.</span><span class="sxs-lookup"><span data-stu-id="d6a97-110">The type of action to take for the antispoofing policy.</span></span>

</dd> <dt>

<span data-ttu-id="d6a97-111">**Source**</span><span class="sxs-lookup"><span data-stu-id="d6a97-111">**Source**</span></span>
</dt> <dd>

<span data-ttu-id="d6a97-112">Source de la stratégie d’antiusurpation.</span><span class="sxs-lookup"><span data-stu-id="d6a97-112">The source for the antispoofing policy.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d6a97-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6a97-113">Requirements</span></span>



| <span data-ttu-id="d6a97-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6a97-114">Requirement</span></span> | <span data-ttu-id="d6a97-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6a97-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6a97-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6a97-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d6a97-117">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6a97-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="d6a97-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6a97-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d6a97-119">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6a97-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="d6a97-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d6a97-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6a97-121"><dt>WinBio \_ types. h (inclure WinBio. h pour les applications clientes ou les \_ cartes WinBio. h pour les adaptateurs)</dt></span><span class="sxs-lookup"><span data-stu-id="d6a97-121"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6a97-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6a97-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6a97-123">**\_action de stratégie anti- \_ usurpation WINBIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d6a97-123">**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**</span></span>](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[<span data-ttu-id="d6a97-124">**SOURCE de la \_ stratégie WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="d6a97-124">**WINBIO\_POLICY\_SOURCE**</span></span>](winbio-policy-source.md)
</dt> <dt>

[<span data-ttu-id="d6a97-125">**\_Résultat asynchrone \_ WINBIO**</span><span class="sxs-lookup"><span data-stu-id="d6a97-125">**WINBIO\_ASYNC\_RESULT**</span></span>](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[<span data-ttu-id="d6a97-126">**WinBioGetProperty**</span><span class="sxs-lookup"><span data-stu-id="d6a97-126">**WinBioGetProperty**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> <dt>

[<span data-ttu-id="d6a97-127">**WinBioSetProperty**</span><span class="sxs-lookup"><span data-stu-id="d6a97-127">**WinBioSetProperty**</span></span>](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty)
</dt> </dl>

 

 





