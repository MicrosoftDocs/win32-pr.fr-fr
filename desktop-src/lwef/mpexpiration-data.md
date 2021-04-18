---
title: Structure MPEXPIRATION_DATA (MpClient. h)
description: Notification d’état d’expiration du produit.
ms.assetid: BF464FFD-16AE-4F46-83CD-E0355478180C
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPEXPIRATION_DATA
- PMPEXPIRATION_DATA des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPEXPIRATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df5e417b1ce6b1d1f4c15d646b44b0ea6c1fade2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512140"
---
# <a name="mpexpiration_data-structure"></a><span data-ttu-id="e4a4e-105">\_Structure de données MPEXPIRATION</span><span class="sxs-lookup"><span data-stu-id="e4a4e-105">MPEXPIRATION\_DATA structure</span></span>

<span data-ttu-id="e4a4e-106">Notification d’état d’expiration du produit.</span><span class="sxs-lookup"><span data-stu-id="e4a4e-106">Product expiration status notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4a4e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4a4e-107">Syntax</span></span>


```C++
typedef struct tagMPEXPIRATION_DATA {
  MP_EXPIRE_REASON       Reason;
  MP_EXPIRE_STATE_REPORT State;
} MPEXPIRATION_DATA, *PMPEXPIRATION_DATA;
```



## <a name="members"></a><span data-ttu-id="e4a4e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e4a4e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e4a4e-109">**Motif**</span><span class="sxs-lookup"><span data-stu-id="e4a4e-109">**Reason**</span></span>
</dt> <dd>

<span data-ttu-id="e4a4e-110">Type : **\_ \_ raison** de l’expiration du point de gestion</span><span class="sxs-lookup"><span data-stu-id="e4a4e-110">Type: **MP\_EXPIRE\_REASON**</span></span>

</dd> <dd>

<span data-ttu-id="e4a4e-111">Raison de l’expiration.</span><span class="sxs-lookup"><span data-stu-id="e4a4e-111">Expiration reason.</span></span> <span data-ttu-id="e4a4e-112">Il s’agit de l’une des valeurs possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="e4a4e-112">This is one of the following possible values:</span></span>



| <span data-ttu-id="e4a4e-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4a4e-113">Value</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="e4a4e-114">Signification</span><span class="sxs-lookup"><span data-stu-id="e4a4e-114">Meaning</span></span>                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|
| <span id="MP_EXPIRED_UNKNOWN"></span><span id="mp_expired_unknown"></span><dl> <span data-ttu-id="e4a4e-115">Pack d’e <dt>**\_ EXPIRÉ \_ inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e4a4e-115"><dt>**MP\_EXPIRED\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="e4a4e-116">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="e4a4e-116">Unknown.</span></span><br/>    |
| <span id="MP_EXPIRED_EVAL"></span><span id="mp_expired_eval"></span><dl> <span data-ttu-id="e4a4e-117">Pack d’e <dt>**\_ \_Eval expiré**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e4a4e-117"><dt>**MP\_EXPIRED\_EVAL**</dt> <dt>1</dt></span></span> </dl>          | <span data-ttu-id="e4a4e-118">Analyse.</span><span class="sxs-lookup"><span data-stu-id="e4a4e-118">Evaluation.</span></span><br/> |
| <span id="MP_EXPIRED_WAT"></span><span id="mp_expired_wat"></span><dl> <span data-ttu-id="e4a4e-119">Pack d’e <dt>**\_ \_Wat expirée**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e4a4e-119"><dt>**MP\_EXPIRED\_WAT**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="e4a4e-120">Wat.</span><span class="sxs-lookup"><span data-stu-id="e4a4e-120">WAT.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="e4a4e-121">**State**</span><span class="sxs-lookup"><span data-stu-id="e4a4e-121">**State**</span></span>
</dt> <dd>

<span data-ttu-id="e4a4e-122">Type : **\_ \_ \_ rapport d’état d’expiration** du point de gestion</span><span class="sxs-lookup"><span data-stu-id="e4a4e-122">Type: **MP\_EXPIRE\_STATE\_REPORT**</span></span>

</dd> <dd>

<span data-ttu-id="e4a4e-123">État d’expiration.</span><span class="sxs-lookup"><span data-stu-id="e4a4e-123">Expiration state.</span></span> <span data-ttu-id="e4a4e-124">Il s’agit de l’une des valeurs possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="e4a4e-124">This is one of the following possible values:</span></span>



| <span data-ttu-id="e4a4e-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4a4e-125">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="e4a4e-126">Signification</span><span class="sxs-lookup"><span data-stu-id="e4a4e-126">Meaning</span></span>                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| <span id="MP_EXPIRE_STATE_REPORT_UNKNOWN"></span><span id="mp_expire_state_report_unknown"></span><dl> <span data-ttu-id="e4a4e-127">Pack d’e <dt>**\_ Rapport d' \_ État d’expiration \_ \_ inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e4a4e-127"><dt>**MP\_EXPIRE\_STATE\_REPORT\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="e4a4e-128">État inconnu.</span><span class="sxs-lookup"><span data-stu-id="e4a4e-128">State unknown.</span></span><br/> |
| <span id="MP_EXPIRE_STATE_REPORT_VALID"></span><span id="mp_expire_state_report_valid"></span><dl> <span data-ttu-id="e4a4e-129">Pack d’e <dt>**\_ Rapport d' \_ État d’expiration \_ \_ valide**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e4a4e-129"><dt>**MP\_EXPIRE\_STATE\_REPORT\_VALID**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="e4a4e-130">Pas d’expiration.</span><span class="sxs-lookup"><span data-stu-id="e4a4e-130">No expiration.</span></span><br/> |
| <span id="MP_EXPIRE_STATE_REPORT_WARNING"></span><span id="mp_expire_state_report_warning"></span><dl> <span data-ttu-id="e4a4e-131">Pack d’e <dt>**\_ \_ \_ \_ Avertissement de rapport d’état d’expiration**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e4a4e-131"><dt>**MP\_EXPIRE\_STATE\_REPORT\_WARNING**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="e4a4e-132">Proche de l’expiration.</span><span class="sxs-lookup"><span data-stu-id="e4a4e-132">Near expired.</span></span><br/>  |
| <span id="MP_EXPIRE_STATE_REPORT_EXPIRED"></span><span id="mp_expire_state_report_expired"></span><dl> <span data-ttu-id="e4a4e-133">Pack d’e <dt>**\_ Le rapport d’état d’expiration \_ \_ \_ a expiré**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e4a4e-133"><dt>**MP\_EXPIRE\_STATE\_REPORT\_EXPIRED**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="e4a4e-134">Fin.</span><span class="sxs-lookup"><span data-stu-id="e4a4e-134">Expired.</span></span><br/>       |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e4a4e-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4a4e-135">Requirements</span></span>



| <span data-ttu-id="e4a4e-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4a4e-136">Requirement</span></span> | <span data-ttu-id="e4a4e-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4a4e-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4a4e-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4a4e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e4a4e-139">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4a4e-139">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e4a4e-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4a4e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e4a4e-141">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4a4e-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e4a4e-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="e4a4e-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4a4e-143"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4a4e-143"><dt>MpClient.h</dt></span></span> </dl> |



 

 





