---
title: Énumération MPSOURCE (MpClient. h)
description: Catégorie possible de la source.
ms.assetid: 1AD12D67-C74B-481A-AC9B-D119AABDB6E9
keywords:
- MPSOURCE, énumération des fonctionnalités d’environnement Windows héritées
- Pointeur d’énumération PMPSOURCE fonctionnalités d’environnement Windows héritées
topic_type:
- apiref
api_name:
- MPSOURCE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e9255029512499a0e2948a44701ef4482aff4b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942394"
---
# <a name="mpsource-enumeration"></a><span data-ttu-id="ce341-105">Énumération MPSOURCE</span><span class="sxs-lookup"><span data-stu-id="ce341-105">MPSOURCE enumeration</span></span>

<span data-ttu-id="ce341-106">Catégorie possible de la source.</span><span class="sxs-lookup"><span data-stu-id="ce341-106">Possible category of source.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce341-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce341-107">Syntax</span></span>


```C++
typedef enum tagMPSOURCE { 
  MPSOURCE_UNKNOWN             = 0,
  MPSOURCE_USER                = 1,
  MPSOURCE_SYSTEM              = 2,
  MPSOURCE_REALTIME            = 3,
  MPSOURCE_IOAV                = 4,
  MPSOURCE_NIS                 = 5,
  MPSOURCE_BHO                 = 6,
  MPSOURCE_IEPROTECT           = 6,
  MPSOURCE_ELAM                = 7,
  MPSOURCE_LOCAL_ATTESTATION   = 8,
  MPSOURCE_REMOTE_ATTESTATION  = 9,
  MPSOURCE_AMSI                = 10,
  MP_SOURCE_MAXVALUE           = 10
} MPSOURCE, *PMPSOURCE;
```



## <a name="constants"></a><span data-ttu-id="ce341-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="ce341-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ce341-109"><span id="MPSOURCE_UNKNOWN"></span><span id="mpsource_unknown"></span>**MPSOURCE \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="ce341-109"><span id="MPSOURCE_UNKNOWN"></span><span id="mpsource_unknown"></span>**MPSOURCE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="ce341-110">Source inconnue.</span><span class="sxs-lookup"><span data-stu-id="ce341-110">Source unknown.</span></span>

</dd> <dt>

<span data-ttu-id="ce341-111"><span id="MPSOURCE_USER"></span><span id="mpsource_user"></span>**\_utilisateur MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="ce341-111"><span id="MPSOURCE_USER"></span><span id="mpsource_user"></span>**MPSOURCE\_USER**</span></span>
</dt> <dd>

<span data-ttu-id="ce341-112">Initié par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ce341-112">User initiated.</span></span>

</dd> <dt>

<span data-ttu-id="ce341-113"><span id="MPSOURCE_SYSTEM"></span><span id="mpsource_system"></span>**\_système MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="ce341-113"><span id="MPSOURCE_SYSTEM"></span><span id="mpsource_system"></span>**MPSOURCE\_SYSTEM**</span></span>
</dt> <dd>

<span data-ttu-id="ce341-114">initié par le système.</span><span class="sxs-lookup"><span data-stu-id="ce341-114">system initiated.</span></span>

</dd> <dt>

<span data-ttu-id="ce341-115"><span id="MPSOURCE_REALTIME"></span><span id="mpsource_realtime"></span>**\_temps réel MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="ce341-115"><span id="MPSOURCE_REALTIME"></span><span id="mpsource_realtime"></span>**MPSOURCE\_REALTIME**</span></span>
</dt> <dd>

<span data-ttu-id="ce341-116">Le composant en temps réel a démarré.</span><span class="sxs-lookup"><span data-stu-id="ce341-116">Realtime component initiated.</span></span>

</dd> <dt>

<span data-ttu-id="ce341-117"><span id="MPSOURCE_IOAV"></span><span id="mpsource_ioav"></span>**MPSOURCE \_ IOAV**</span><span class="sxs-lookup"><span data-stu-id="ce341-117"><span id="MPSOURCE_IOAV"></span><span id="mpsource_ioav"></span>**MPSOURCE\_IOAV**</span></span>
</dt> <dd>

<span data-ttu-id="ce341-118">Les téléchargements IE et les pièces jointes Outlook Express sont initiés.</span><span class="sxs-lookup"><span data-stu-id="ce341-118">IE Downloads and Outlook Express Attachments initiated.</span></span>

</dd> <dt>

<span data-ttu-id="ce341-119"><span id="MPSOURCE_NIS"></span><span id="mpsource_nis"></span>**MPSOURCE \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="ce341-119"><span id="MPSOURCE_NIS"></span><span id="mpsource_nis"></span>**MPSOURCE\_NIS**</span></span>
</dt> <dd>

<span data-ttu-id="ce341-120">Système NIS (Network Inspection System).</span><span class="sxs-lookup"><span data-stu-id="ce341-120">Network inspection system.</span></span>

</dd> <dt>

<span data-ttu-id="ce341-121"><span id="MPSOURCE_BHO"></span><span id="mpsource_bho"></span>**MPSOURCE \_ BHO**</span><span class="sxs-lookup"><span data-stu-id="ce341-121"><span id="MPSOURCE_BHO"></span><span id="mpsource_bho"></span>**MPSOURCE\_BHO**</span></span>
</dt> <dd>

<span data-ttu-id="ce341-122">BHO-script Web (déconseillé).</span><span class="sxs-lookup"><span data-stu-id="ce341-122">BHO - web script (deprecated).</span></span>

</dd> <dt>

<span data-ttu-id="ce341-123"><span id="MPSOURCE_IEPROTECT"></span><span id="mpsource_ieprotect"></span>**MPSOURCE \_ IEPROTECT**</span><span class="sxs-lookup"><span data-stu-id="ce341-123"><span id="MPSOURCE_IEPROTECT"></span><span id="mpsource_ieprotect"></span>**MPSOURCE\_IEPROTECT**</span></span>
</dt> <dd>

<span data-ttu-id="ce341-124">IE-IExtensionValidation.</span><span class="sxs-lookup"><span data-stu-id="ce341-124">IE - IExtensionValidation.</span></span>

</dd> <dt>

<span data-ttu-id="ce341-125"><span id="MPSOURCE_ELAM"></span><span id="mpsource_elam"></span>**MPSOURCE \_ Elam**</span><span class="sxs-lookup"><span data-stu-id="ce341-125"><span id="MPSOURCE_ELAM"></span><span id="mpsource_elam"></span>**MPSOURCE\_ELAM**</span></span>
</dt> <dd>

<span data-ttu-id="ce341-126">Logiciel anti-programme malveillant à lancement anticipé</span><span class="sxs-lookup"><span data-stu-id="ce341-126">ELAM</span></span>

</dd> <dt>

<span data-ttu-id="ce341-127"><span id="MPSOURCE_LOCAL_ATTESTATION"></span><span id="mpsource_local_attestation"></span>**\_attestation locale \_ MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="ce341-127"><span id="MPSOURCE_LOCAL_ATTESTATION"></span><span id="mpsource_local_attestation"></span>**MPSOURCE\_LOCAL\_ATTESTATION**</span></span>
</dt> <dd>

<span data-ttu-id="ce341-128">Attestation locale.</span><span class="sxs-lookup"><span data-stu-id="ce341-128">Local attestation.</span></span>

</dd> <dt>

<span data-ttu-id="ce341-129"><span id="MPSOURCE_REMOTE_ATTESTATION"></span><span id="mpsource_remote_attestation"></span>**\_attestation distante MPSOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="ce341-129"><span id="MPSOURCE_REMOTE_ATTESTATION"></span><span id="mpsource_remote_attestation"></span>**MPSOURCE\_REMOTE\_ATTESTATION**</span></span>
</dt> <dd>

<span data-ttu-id="ce341-130">Attestation distante.</span><span class="sxs-lookup"><span data-stu-id="ce341-130">Remote attestation.</span></span>

</dd> <dt>

<span data-ttu-id="ce341-131"><span id="MPSOURCE_AMSI"></span><span id="mpsource_amsi"></span>**MPSOURCE \_ AMSI**</span><span class="sxs-lookup"><span data-stu-id="ce341-131"><span id="MPSOURCE_AMSI"></span><span id="mpsource_amsi"></span>**MPSOURCE\_AMSI**</span></span>
</dt> <dd>

<span data-ttu-id="ce341-132">AMSI</span><span class="sxs-lookup"><span data-stu-id="ce341-132">AMSI</span></span>

</dd> <dt>

<span data-ttu-id="ce341-133"><span id="MP_SOURCE_MAXVALUE"></span><span id="mp_source_maxvalue"></span>**\_source MP \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="ce341-133"><span id="MP_SOURCE_MAXVALUE"></span><span id="mp_source_maxvalue"></span>**MP\_SOURCE\_MAXVALUE**</span></span>
</dt> <dd>

<span data-ttu-id="ce341-134">Valeur maximale possible.</span><span class="sxs-lookup"><span data-stu-id="ce341-134">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce341-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce341-135">Requirements</span></span>



| <span data-ttu-id="ce341-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce341-136">Requirement</span></span> | <span data-ttu-id="ce341-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce341-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce341-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce341-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ce341-139">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce341-139">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ce341-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce341-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ce341-141">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce341-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce341-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce341-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce341-143"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce341-143"><dt>MpClient.h</dt></span></span> </dl> |



 

 





