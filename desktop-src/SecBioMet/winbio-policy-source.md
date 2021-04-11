---
title: Énumération WINBIO_POLICY_SOURCE ( \_ types WINBIO. h)
description: Répertorie les sources possibles d’informations de stratégie pour la détection de l’usurpation d’identité pour les facteurs biométriques.
ms.assetid: 3DC3BB0B-1FD7-473C-8E0B-B7E0A4A44E9E
keywords:
- API Windows Biometric Framework de l’énumération WINBIO_POLICY_SOURCE
- API du pointeur d’énumération PWINBIO_POLICY_SOURCE Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_POLICY_SOURCE
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866d1d82d939f143c4385caa5d94c68ffe3758f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317482"
---
# <a name="winbio_policy_source-enumeration"></a><span data-ttu-id="05807-105">Énumération de la source de la \_ stratégie WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="05807-105">WINBIO\_POLICY\_SOURCE enumeration</span></span>

<span data-ttu-id="05807-106">Répertorie les sources possibles d’informations de stratégie pour la détection de l’usurpation d’identité pour les facteurs biométriques.</span><span class="sxs-lookup"><span data-stu-id="05807-106">Lists the possible sources of policy information for the detection of spoofing for biometric factors.</span></span>

## <a name="syntax"></a><span data-ttu-id="05807-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05807-107">Syntax</span></span>


```C++
typedef enum _WINBIO_POLICY_SOURCE { 
  WINBIO_POLICY_UNKNOWN  = 0x00000000,
  WINBIO_POLICY_DEFAULT  = 0x00000001,
  WINBIO_POLICY_LOCAL    = 0x00000002,
  WINBIO_POLICY_ADMIN    = 0x00000003
} WINBIO_POLICY_SOURCE, *PWINBIO_POLICY_SOURCE;
```



## <a name="constants"></a><span data-ttu-id="05807-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="05807-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="05807-109"><span id="WINBIO_POLICY_UNKNOWN"></span><span id="winbio_policy_unknown"></span>**\_stratégie WINBIO \_ inconnue**</span><span class="sxs-lookup"><span data-stu-id="05807-109"><span id="WINBIO_POLICY_UNKNOWN"></span><span id="winbio_policy_unknown"></span>**WINBIO\_POLICY\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="05807-110">La source de la stratégie est inconnue.</span><span class="sxs-lookup"><span data-stu-id="05807-110">The source of the policy is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="05807-111"><span id="WINBIO_POLICY_DEFAULT"></span><span id="winbio_policy_default"></span>**\_ \_ valeur par défaut de la stratégie WINBIO**</span><span class="sxs-lookup"><span data-stu-id="05807-111"><span id="WINBIO_POLICY_DEFAULT"></span><span id="winbio_policy_default"></span>**WINBIO\_POLICY\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="05807-112">La stratégie est la stratégie par défaut fournie par le Windows Biometric Framework.</span><span class="sxs-lookup"><span data-stu-id="05807-112">The policy is the default policy that the Windows Biometric Framework provides.</span></span>

</dd> <dt>

<span data-ttu-id="05807-113"><span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**\_stratégie WINBIO \_ locale**</span><span class="sxs-lookup"><span data-stu-id="05807-113"><span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**WINBIO\_POLICY\_LOCAL**</span></span>
</dt> <dd>

<span data-ttu-id="05807-114">Stratégie définie par l’utilisateur pour son compte à l’aide de l’application **paramètres** .</span><span class="sxs-lookup"><span data-stu-id="05807-114">The policy that the individual user set for their account by using the **Settings** app.</span></span> <span data-ttu-id="05807-115">Cette stratégie remplace la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="05807-115">This policy overrides the default policy.</span></span>

</dd> <dt>

<span data-ttu-id="05807-116"><span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**\_administrateur de stratégie WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="05807-116"><span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**WINBIO\_POLICY\_ADMIN**</span></span>
</dt> <dd>

<span data-ttu-id="05807-117">Stratégie de groupe définie par l’administrateur informatique pour l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="05807-117">A group policy that the IT administrator set for the enterprise.</span></span> <span data-ttu-id="05807-118">Les utilisateurs individuels ne peuvent pas remplacer cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="05807-118">Individual users cannot override this policy.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="05807-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05807-119">Requirements</span></span>



| <span data-ttu-id="05807-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05807-120">Requirement</span></span> | <span data-ttu-id="05807-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="05807-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05807-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05807-122">Minimum supported client</span></span><br/> | <span data-ttu-id="05807-123">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05807-123">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="05807-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05807-124">Minimum supported server</span></span><br/> | <span data-ttu-id="05807-125">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05807-125">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="05807-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="05807-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="05807-127"><dt>WinBio \_ types. h (inclure WinBio. h pour les applications clientes ou les \_ cartes WinBio. h pour les adaptateurs)</dt></span><span class="sxs-lookup"><span data-stu-id="05807-127"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05807-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05807-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05807-129">**\_action de stratégie anti- \_ usurpation WINBIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="05807-129">**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**</span></span>](winbio-anti-spoof-policy-action.md)
</dt> </dl>

 

 





