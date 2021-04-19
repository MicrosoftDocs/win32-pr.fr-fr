---
title: Structure MPFASTPATH_DATA (MpClient. h)
description: Notification de mise à jour FastPath.
ms.assetid: E19F153D-DD46-4E27-9A4B-33586794DAC2
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPFASTPATH_DATA
- PMPFASTPATH_DATA des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPFASTPATH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2850a48074fee6984564550683c7fe595d0779ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513773"
---
# <a name="mpfastpath_data-structure"></a><span data-ttu-id="7ef18-105">\_Structure de données MPFASTPATH</span><span class="sxs-lookup"><span data-stu-id="7ef18-105">MPFASTPATH\_DATA structure</span></span>

<span data-ttu-id="7ef18-106">Notification de mise à jour FastPath.</span><span class="sxs-lookup"><span data-stu-id="7ef18-106">FastPath update notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ef18-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ef18-107">Syntax</span></span>


```C++
typedef struct tagMPFASTPATH_DATA {
  MP_SIGNATURE_TYPE         SignatureType;
  MP_FASTPATH_TYPE          FastPathSignatureType;
  MP_MIDL_STRING LPWSTR     FastPathSignatureVersion;
  ULARGE_INTEGER            CompilationTimestamp;
  MP_PERSISTENCE_LIMIT_TYPE PersistenceType;
  MP_MIDL_STRING LPWSTR     PersistenceValue;
  MP_MIDL_STRING LPWSTR     PersistencePath;
  MP_REMOVAL_REASON         Reason;
} MPFASTPATH_DATA, *PMPFASTPATH_DATA;
```



## <a name="members"></a><span data-ttu-id="7ef18-108">Membres</span><span class="sxs-lookup"><span data-stu-id="7ef18-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7ef18-109">**SignatureType**</span><span class="sxs-lookup"><span data-stu-id="7ef18-109">**SignatureType**</span></span>
</dt> <dd>

<span data-ttu-id="7ef18-110">Type : **[ **\_ \_ type de signature MP**](mp-signature-type.md)**</span><span class="sxs-lookup"><span data-stu-id="7ef18-110">Type: **[**MP\_SIGNATURE\_TYPE**](mp-signature-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7ef18-111">Type de signature.</span><span class="sxs-lookup"><span data-stu-id="7ef18-111">Signature type.</span></span>

</dd> <dt>

<span data-ttu-id="7ef18-112">**FastPathSignatureType**</span><span class="sxs-lookup"><span data-stu-id="7ef18-112">**FastPathSignatureType**</span></span>
</dt> <dd>

<span data-ttu-id="7ef18-113">Type : **[ **MP \_ FASTPATH \_ type**](mp-fastpath-type.md)**</span><span class="sxs-lookup"><span data-stu-id="7ef18-113">Type: **[**MP\_FASTPATH\_TYPE**](mp-fastpath-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7ef18-114">Type de signature FastPath.</span><span class="sxs-lookup"><span data-stu-id="7ef18-114">FastPath signature type.</span></span>

</dd> <dt>

<span data-ttu-id="7ef18-115">**FastPathSignatureVersion**</span><span class="sxs-lookup"><span data-stu-id="7ef18-115">**FastPathSignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="7ef18-116">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="7ef18-116">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="7ef18-117">Version de signature de FastPath (facultatif).</span><span class="sxs-lookup"><span data-stu-id="7ef18-117">FastPath signature version (optional).</span></span>

</dd> <dt>

<span data-ttu-id="7ef18-118">**CompilationTimestamp**</span><span class="sxs-lookup"><span data-stu-id="7ef18-118">**CompilationTimestamp**</span></span>
</dt> <dd>

<span data-ttu-id="7ef18-119">Type : **\_ entier ULARGE**</span><span class="sxs-lookup"><span data-stu-id="7ef18-119">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="7ef18-120">Horodatage de compilation (UTC).</span><span class="sxs-lookup"><span data-stu-id="7ef18-120">Compilation timestamp (UTC).</span></span>

</dd> <dt>

<span data-ttu-id="7ef18-121">**PersistenceType**</span><span class="sxs-lookup"><span data-stu-id="7ef18-121">**PersistenceType**</span></span>
</dt> <dd>

<span data-ttu-id="7ef18-122">Type : **[ **\_ \_ \_ type de limite de persistance MP**](mp-persistence-limit-type.md)**</span><span class="sxs-lookup"><span data-stu-id="7ef18-122">Type: **[**MP\_PERSISTENCE\_LIMIT\_TYPE**](mp-persistence-limit-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7ef18-123">Type de persistance (facultatif).</span><span class="sxs-lookup"><span data-stu-id="7ef18-123">Persistence type (optional).</span></span>

</dd> <dt>

<span data-ttu-id="7ef18-124">**PersistenceValue**</span><span class="sxs-lookup"><span data-stu-id="7ef18-124">**PersistenceValue**</span></span>
</dt> <dd>

<span data-ttu-id="7ef18-125">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="7ef18-125">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="7ef18-126">Valeur de persistance (facultatif).</span><span class="sxs-lookup"><span data-stu-id="7ef18-126">Persistence value (optional).</span></span>

</dd> <dt>

<span data-ttu-id="7ef18-127">**PersistencePath**</span><span class="sxs-lookup"><span data-stu-id="7ef18-127">**PersistencePath**</span></span>
</dt> <dd>

<span data-ttu-id="7ef18-128">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="7ef18-128">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="7ef18-129">Chemin de persistance (facultatif).</span><span class="sxs-lookup"><span data-stu-id="7ef18-129">Persistence path (optional).</span></span>

</dd> <dt>

<span data-ttu-id="7ef18-130">**Motif**</span><span class="sxs-lookup"><span data-stu-id="7ef18-130">**Reason**</span></span>
</dt> <dd>

<span data-ttu-id="7ef18-131">Type : raison de la **[ **suppression du pack d' \_ installation \_**](mp-removal-reason.md)**</span><span class="sxs-lookup"><span data-stu-id="7ef18-131">Type: **[**MP\_REMOVAL\_REASON**](mp-removal-reason.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7ef18-132">Raison de la suppression de la signature.</span><span class="sxs-lookup"><span data-stu-id="7ef18-132">Reason for signature removal.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7ef18-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ef18-133">Requirements</span></span>



| <span data-ttu-id="7ef18-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ef18-134">Requirement</span></span> | <span data-ttu-id="7ef18-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ef18-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ef18-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ef18-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7ef18-137">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ef18-137">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7ef18-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ef18-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7ef18-139">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ef18-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7ef18-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ef18-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ef18-141"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ef18-141"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ef18-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ef18-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ef18-143">**\_type de FASTPATH MP \_**</span><span class="sxs-lookup"><span data-stu-id="7ef18-143">**MP\_FASTPATH\_TYPE**</span></span>](mp-fastpath-type.md)
</dt> <dt>

[<span data-ttu-id="7ef18-144">**\_type de limite de persistance MP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ef18-144">**MP\_PERSISTENCE\_LIMIT\_TYPE**</span></span>](mp-persistence-limit-type.md)
</dt> <dt>

[<span data-ttu-id="7ef18-145">**\_type de signature MP \_**</span><span class="sxs-lookup"><span data-stu-id="7ef18-145">**MP\_SIGNATURE\_TYPE**</span></span>](mp-signature-type.md)
</dt> </dl>

 

 





