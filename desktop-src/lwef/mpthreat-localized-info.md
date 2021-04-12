---
title: Structure MPTHREAT_LOCALIZED_INFO (MpClient. h)
description: Informations localisées pour une menace.
ms.assetid: 99DC9737-9A61-4407-B544-A7A979C5B556
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPTHREAT_LOCALIZED_INFO
- PMPTHREAT_LOCALIZED_INFO des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPTHREAT_LOCALIZED_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87ea0bee7c8cae15389b40b64038aad92a56dd5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384600"
---
# <a name="mpthreat_localized_info-structure"></a><span data-ttu-id="cc75b-105">MPTHREAT \_ structure des \_ informations localisées</span><span class="sxs-lookup"><span data-stu-id="cc75b-105">MPTHREAT\_LOCALIZED\_INFO structure</span></span>

<span data-ttu-id="cc75b-106">Informations localisées pour une menace.</span><span class="sxs-lookup"><span data-stu-id="cc75b-106">Localized information for a threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc75b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc75b-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_LOCALIZED_INFO {
  MPTHREAT_ID           ThreatID;
  MP_MIDL_STRING LPWSTR CategoryName;
  MP_MIDL_STRING LPWSTR CategoryDescription;
  MP_MIDL_STRING LPWSTR SeverityName;
  MP_MIDL_STRING LPWSTR SeverityDescription;
  MP_MIDL_STRING LPWSTR ShortDescription;
  MP_MIDL_STRING LPWSTR DefaultActionName;;
  MP_MIDL_STRING LPWSTR Advice;
  MP_MIDL_STRING LPWSTR ThreatUrl;
} MPTHREAT_LOCALIZED_INFO, *PMPTHREAT_LOCALIZED_INFO;
```



## <a name="members"></a><span data-ttu-id="cc75b-108">Membres</span><span class="sxs-lookup"><span data-stu-id="cc75b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="cc75b-109">**ThreatID**</span><span class="sxs-lookup"><span data-stu-id="cc75b-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="cc75b-110">Type : **\_ ID MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="cc75b-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="cc75b-111">Identificateur de la menace.</span><span class="sxs-lookup"><span data-stu-id="cc75b-111">Threat identifier.</span></span> <span data-ttu-id="cc75b-112">Le bit supérieur est défini pour identifier les menaces liées à l’antivirus.</span><span class="sxs-lookup"><span data-stu-id="cc75b-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="cc75b-113">**NomCatégorie**</span><span class="sxs-lookup"><span data-stu-id="cc75b-113">**CategoryName**</span></span>
</dt> <dd>

<span data-ttu-id="cc75b-114">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="cc75b-114">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="cc75b-115">Classification des menaces, comme un cheval de Troie ou un enregistreur d’enregistreur.</span><span class="sxs-lookup"><span data-stu-id="cc75b-115">Threat classification, such as a trojan or a keylogger.</span></span>

</dd> <dt>

<span data-ttu-id="cc75b-116">**CategoryDescription**</span><span class="sxs-lookup"><span data-stu-id="cc75b-116">**CategoryDescription**</span></span>
</dt> <dd>

<span data-ttu-id="cc75b-117">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="cc75b-117">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="cc75b-118">Description de la catégorie de menace.</span><span class="sxs-lookup"><span data-stu-id="cc75b-118">Description of threat category.</span></span>

</dd> <dt>

<span data-ttu-id="cc75b-119">**SeverityName**</span><span class="sxs-lookup"><span data-stu-id="cc75b-119">**SeverityName**</span></span>
</dt> <dd>

<span data-ttu-id="cc75b-120">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="cc75b-120">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="cc75b-121">Niveau de gravité de la menace, par exemple grave ou modéré.</span><span class="sxs-lookup"><span data-stu-id="cc75b-121">Threat severity level, such as severe or moderate.</span></span>

</dd> <dt>

<span data-ttu-id="cc75b-122">**SeverityDescription**</span><span class="sxs-lookup"><span data-stu-id="cc75b-122">**SeverityDescription**</span></span>
</dt> <dd>

<span data-ttu-id="cc75b-123">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="cc75b-123">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="cc75b-124">Description du niveau de gravité de la menace.</span><span class="sxs-lookup"><span data-stu-id="cc75b-124">Description of threat severity level.</span></span>

</dd> <dt>

<span data-ttu-id="cc75b-125">**ShortDescription**</span><span class="sxs-lookup"><span data-stu-id="cc75b-125">**ShortDescription**</span></span>
</dt> <dd>

<span data-ttu-id="cc75b-126">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="cc75b-126">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="cc75b-127">Description sommaire de la menace.</span><span class="sxs-lookup"><span data-stu-id="cc75b-127">Short description of threat.</span></span>

</dd> <dt>

<span data-ttu-id="cc75b-128">**DefaultActionName;**</span><span class="sxs-lookup"><span data-stu-id="cc75b-128">**DefaultActionName;**</span></span>
</dt> <dd>

<span data-ttu-id="cc75b-129">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="cc75b-129">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="cc75b-130">Nom de l’action par défaut, par exemple supprimer ou mettre en quarantaine, suggéré par le moteur.</span><span class="sxs-lookup"><span data-stu-id="cc75b-130">Name of default action, such as remove or quarantine, suggested by engine.</span></span>

</dd> <dt>

<span data-ttu-id="cc75b-131">**Conseils**</span><span class="sxs-lookup"><span data-stu-id="cc75b-131">**Advice**</span></span>
</dt> <dd>

<span data-ttu-id="cc75b-132">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="cc75b-132">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="cc75b-133">Conseils pour une menace particulière.</span><span class="sxs-lookup"><span data-stu-id="cc75b-133">Advice for the particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="cc75b-134">**ThreatUrl**</span><span class="sxs-lookup"><span data-stu-id="cc75b-134">**ThreatUrl**</span></span>
</dt> <dd>

<span data-ttu-id="cc75b-135">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="cc75b-135">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="cc75b-136">URL d’une page Web contenant des informations sur la menace.</span><span class="sxs-lookup"><span data-stu-id="cc75b-136">A URL to a webpage containing information about the threat.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc75b-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc75b-137">Requirements</span></span>



| <span data-ttu-id="cc75b-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc75b-138">Requirement</span></span> | <span data-ttu-id="cc75b-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc75b-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc75b-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc75b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="cc75b-141">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc75b-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="cc75b-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc75b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="cc75b-143">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc75b-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc75b-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc75b-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc75b-145"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc75b-145"><dt>MpClient.h</dt></span></span> </dl> |



 

 





