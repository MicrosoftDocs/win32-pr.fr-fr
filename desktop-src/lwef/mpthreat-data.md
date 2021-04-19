---
title: Structure MPTHREAT_DATA (MpClient. h)
description: Données de notification transmises en raison de la détection ou de la modification des menaces.
ms.assetid: 07A2F88B-9D58-44EC-86D0-BDCC1DF44B94
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPTHREAT_DATA
- PMPTHREAT_DATA des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPTHREAT_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cafbb11dbb3b1a34b38ffd0448db96fd1409efd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518123"
---
# <a name="mpthreat_data-structure"></a><span data-ttu-id="c76ce-105">\_Structure de données MPTHREAT</span><span class="sxs-lookup"><span data-stu-id="c76ce-105">MPTHREAT\_DATA structure</span></span>

<span data-ttu-id="c76ce-106">Données de notification transmises en raison de la détection ou de la modification des menaces.</span><span class="sxs-lookup"><span data-stu-id="c76ce-106">Notification data passed due to threat detection or modification.</span></span>

## <a name="syntax"></a><span data-ttu-id="c76ce-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c76ce-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_DATA {
  MPTHREAT_ID     ThreatID;
  DWORD           dwSessionID;
  MPTHREAT_ACTION ThreatAction;
  DWORD           dwStatus;
} MPTHREAT_DATA, *PMPTHREAT_DATA;
```



## <a name="members"></a><span data-ttu-id="c76ce-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c76ce-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c76ce-109">**ThreatID**</span><span class="sxs-lookup"><span data-stu-id="c76ce-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="c76ce-110">Type : **\_ ID MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="c76ce-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="c76ce-111">Identificateur de la menace.</span><span class="sxs-lookup"><span data-stu-id="c76ce-111">Threat identifier.</span></span> <span data-ttu-id="c76ce-112">Le bit supérieur est défini pour identifier les menaces liées à l’antivirus.</span><span class="sxs-lookup"><span data-stu-id="c76ce-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="c76ce-113">**dwSessionID**</span><span class="sxs-lookup"><span data-stu-id="c76ce-113">**dwSessionID**</span></span>
</dt> <dd>

<span data-ttu-id="c76ce-114">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c76ce-114">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="c76ce-115">Session associée à la menace.</span><span class="sxs-lookup"><span data-stu-id="c76ce-115">Session associated with the threat.</span></span> <span data-ttu-id="c76ce-116">Affectez la valeur-1 si aucune information spécifique à la session n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="c76ce-116">Set to -1 if no session specific information is available.</span></span>

</dd> <dt>

<span data-ttu-id="c76ce-117">**ThreatAction**</span><span class="sxs-lookup"><span data-stu-id="c76ce-117">**ThreatAction**</span></span>
</dt> <dd>

<span data-ttu-id="c76ce-118">Type : **[ **\_ action MPTHREAT**](mpthreat-action.md)**</span><span class="sxs-lookup"><span data-stu-id="c76ce-118">Type: **[**MPTHREAT\_ACTION**](mpthreat-action.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c76ce-119">L’action de menace a été tentée pour les événements **MPNOTIFY \_ Threat \_ Clean \_ réussite** / **MPNOTIFY \_ Threat \_ Clean \_ failed** .</span><span class="sxs-lookup"><span data-stu-id="c76ce-119">Threat action tried for the **MPNOTIFY\_THREAT\_CLEAN\_SUCCEEDED**/**MPNOTIFY\_THREAT\_CLEAN\_FAILED** events.</span></span>

</dd> <dt>

<span data-ttu-id="c76ce-120">**dwStatus**</span><span class="sxs-lookup"><span data-stu-id="c76ce-120">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="c76ce-121">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c76ce-121">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="c76ce-122">État ou actions supplémentaires associées à l’action effectuée.</span><span class="sxs-lookup"><span data-stu-id="c76ce-122">Additional status or actions associated with the action taken.</span></span> <span data-ttu-id="c76ce-123">Il s’agit d’une combinaison de bits indicateurs à partir de l' [**\_ indicateur MPSTATUS**](mpstatus-flag.md).</span><span class="sxs-lookup"><span data-stu-id="c76ce-123">This is a combination of bit flags from [**MPSTATUS\_FLAG**](mpstatus-flag.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c76ce-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c76ce-124">Requirements</span></span>



| <span data-ttu-id="c76ce-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c76ce-125">Requirement</span></span> | <span data-ttu-id="c76ce-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="c76ce-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c76ce-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c76ce-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c76ce-128">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c76ce-128">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c76ce-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c76ce-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c76ce-130">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c76ce-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c76ce-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="c76ce-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c76ce-132"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c76ce-132"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c76ce-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c76ce-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c76ce-134">**\_indicateur MPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="c76ce-134">**MPSTATUS\_FLAG**</span></span>](mpstatus-flag.md)
</dt> <dt>

[<span data-ttu-id="c76ce-135">**\_action MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="c76ce-135">**MPTHREAT\_ACTION**</span></span>](mpthreat-action.md)
</dt> </dl>

 

 





