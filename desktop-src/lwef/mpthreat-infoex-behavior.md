---
title: Structure MPTHREAT_INFOEX_BEHAVIOR (MpClient. h)
description: Contient des informations spécifiques à la modification du comportement.
ms.assetid: 762E755F-5BA1-476D-B395-6617093309C5
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPTHREAT_INFOEX_BEHAVIOR
- PMPTHREAT_INFOEX_BEHAVIOR des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_BEHAVIOR
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0bc00aeb56aec38b88f2590211c705079834f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743173"
---
# <a name="mpthreat_infoex_behavior-structure"></a><span data-ttu-id="29d7d-105">MPTHREAT \_ \_ structure de comportement INFOEX</span><span class="sxs-lookup"><span data-stu-id="29d7d-105">MPTHREAT\_INFOEX\_BEHAVIOR structure</span></span>

<span data-ttu-id="29d7d-106">Contient des informations spécifiques à la modification du comportement.</span><span class="sxs-lookup"><span data-stu-id="29d7d-106">Contains behavior modification-specific information.</span></span>

## <a name="syntax"></a><span data-ttu-id="29d7d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29d7d-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFOEX_BEHAVIOR {
  ULARGE_INTEGER         SignatureID;
  ULONGLONG              EngineVersion;
  ULONGLONG              ASDeltaSignatureVersion;
  ULONGLONG              AVDeltaSignatureVersion;
  MP_HASH_TYPE           HashType;
  DWORD                  FidelityValue;
  MP_MIDL_STRING  LPWSTR HashValue;
  MP_MIDL_STRING  LPWSTR TargetFileName;
  MP_MIDL_STRING  LPWSTR TargetFileHash;
} MPTHREAT_INFOEX_BEHAVIOR, *PMPTHREAT_INFOEX_BEHAVIOR;
```



## <a name="members"></a><span data-ttu-id="29d7d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="29d7d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="29d7d-109">**SignatureID**</span><span class="sxs-lookup"><span data-stu-id="29d7d-109">**SignatureID**</span></span>
</dt> <dd>

<span data-ttu-id="29d7d-110">Type : **\_ entier ULARGE**</span><span class="sxs-lookup"><span data-stu-id="29d7d-110">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="29d7d-111">ID de signature de modification de comportement fourni par le moteur au moment de la détection.</span><span class="sxs-lookup"><span data-stu-id="29d7d-111">Behavior modification signature ID given by the engine at the time of detection.</span></span>

</dd> <dt>

<span data-ttu-id="29d7d-112">**EngineVersion**</span><span class="sxs-lookup"><span data-stu-id="29d7d-112">**EngineVersion**</span></span>
</dt> <dd>

<span data-ttu-id="29d7d-113">Type : **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="29d7d-113">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="29d7d-114">Version du module moteur.</span><span class="sxs-lookup"><span data-stu-id="29d7d-114">Engine module version.</span></span>

</dd> <dt>

<span data-ttu-id="29d7d-115">**ASDeltaSignatureVersion**</span><span class="sxs-lookup"><span data-stu-id="29d7d-115">**ASDeltaSignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="29d7d-116">Type : **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="29d7d-116">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="29d7d-117">Version de signature du logiciel anti-espion.</span><span class="sxs-lookup"><span data-stu-id="29d7d-117">Antispyware signature version.</span></span>

</dd> <dt>

<span data-ttu-id="29d7d-118">**AVDeltaSignatureVersion**</span><span class="sxs-lookup"><span data-stu-id="29d7d-118">**AVDeltaSignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="29d7d-119">Type : **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="29d7d-119">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="29d7d-120">Version de signature de l’antivirus</span><span class="sxs-lookup"><span data-stu-id="29d7d-120">Antivirus signature version</span></span>

</dd> <dt>

<span data-ttu-id="29d7d-121">**HashType**</span><span class="sxs-lookup"><span data-stu-id="29d7d-121">**HashType**</span></span>
</dt> <dd>

<span data-ttu-id="29d7d-122">Type : **[ **\_ \_ type de hachage MP**](mp-hash-type.md)**</span><span class="sxs-lookup"><span data-stu-id="29d7d-122">Type: **[**MP\_HASH\_TYPE**](mp-hash-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="29d7d-123">Type de hachage utilisé.</span><span class="sxs-lookup"><span data-stu-id="29d7d-123">Hash type used.</span></span> <span data-ttu-id="29d7d-124">Consultez [**\_ \_ type de hachage MP**](mp-hash-type.md).</span><span class="sxs-lookup"><span data-stu-id="29d7d-124">See [**MP\_HASH\_TYPE**](mp-hash-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="29d7d-125">**FidelityValue**</span><span class="sxs-lookup"><span data-stu-id="29d7d-125">**FidelityValue**</span></span>
</dt> <dd>

<span data-ttu-id="29d7d-126">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="29d7d-126">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="29d7d-127">Valeur de fidélité.</span><span class="sxs-lookup"><span data-stu-id="29d7d-127">Fidelity value.</span></span>

</dd> <dt>

<span data-ttu-id="29d7d-128">**HashValue**</span><span class="sxs-lookup"><span data-stu-id="29d7d-128">**HashValue**</span></span>
</dt> <dd>

<span data-ttu-id="29d7d-129">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="29d7d-129">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="29d7d-130">Hachage du fichier.</span><span class="sxs-lookup"><span data-stu-id="29d7d-130">The hash of the file.</span></span>

</dd> <dt>

<span data-ttu-id="29d7d-131">**TargetFileName**</span><span class="sxs-lookup"><span data-stu-id="29d7d-131">**TargetFileName**</span></span>
</dt> <dd>

<span data-ttu-id="29d7d-132">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="29d7d-132">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="29d7d-133">Chemin d’accès et nom du fichier ciblé.</span><span class="sxs-lookup"><span data-stu-id="29d7d-133">The path and name of the targeted file.</span></span>

</dd> <dt>

<span data-ttu-id="29d7d-134">**TargetFileHash**</span><span class="sxs-lookup"><span data-stu-id="29d7d-134">**TargetFileHash**</span></span>
</dt> <dd>

<span data-ttu-id="29d7d-135">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="29d7d-135">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="29d7d-136">Hachage du fichier ciblé.</span><span class="sxs-lookup"><span data-stu-id="29d7d-136">The hash of the targeted file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29d7d-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29d7d-137">Requirements</span></span>



| <span data-ttu-id="29d7d-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29d7d-138">Requirement</span></span> | <span data-ttu-id="29d7d-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="29d7d-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="29d7d-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29d7d-140">Minimum supported client</span></span><br/> | <span data-ttu-id="29d7d-141">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="29d7d-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="29d7d-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29d7d-142">Minimum supported server</span></span><br/> | <span data-ttu-id="29d7d-143">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="29d7d-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="29d7d-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="29d7d-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="29d7d-145"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="29d7d-145"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29d7d-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29d7d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29d7d-147">**\_type de hachage MP \_**</span><span class="sxs-lookup"><span data-stu-id="29d7d-147">**MP\_HASH\_TYPE**</span></span>](mp-hash-type.md)
</dt> </dl>

 

 





