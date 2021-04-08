---
title: Structure MPCLEAN_DATA (MpClient. h)
description: Données de notification transmises à la fonction de rappel propre.
ms.assetid: 475A6525-5BD8-4B29-A684-53EE2758C790
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPCLEAN_DATA
- PMPCLEAN_DATA des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPCLEAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89f0c7e867918b6567279be7c41ce72e7e396576
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741028"
---
# <a name="mpclean_data-structure"></a><span data-ttu-id="cf265-105">\_Structure de données MPCLEAN</span><span class="sxs-lookup"><span data-stu-id="cf265-105">MPCLEAN\_DATA structure</span></span>

<span data-ttu-id="cf265-106">Données de notification transmises à la fonction de rappel propre.</span><span class="sxs-lookup"><span data-stu-id="cf265-106">Notification data passed to clean callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf265-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf265-107">Syntax</span></span>


```C++
typedef struct tagMPCLEAN_DATA {
  MPTHREAT_ID      ThreatID;
  MPTHREAT_ACTION  ThreatAction;
  DWORD            dwStatus;
  PMPRESOURCE_INFO ResourceInfo;
} MPCLEAN_DATA, *PMPCLEAN_DATA;
```



## <a name="members"></a><span data-ttu-id="cf265-108">Membres</span><span class="sxs-lookup"><span data-stu-id="cf265-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="cf265-109">**ThreatID**</span><span class="sxs-lookup"><span data-stu-id="cf265-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="cf265-110">Type : **\_ ID MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="cf265-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="cf265-111">Identificateur de la menace pour le nettoyage des menaces **MPNOTIFY \_ \_ \_ Démarrer** / **MPNOTIFY nettoyage des menaces \_ \_ \_ réussies** / **MPNOTIFY nettoyer les événements \_ \_ \_ ayant échoué** .</span><span class="sxs-lookup"><span data-stu-id="cf265-111">Threat identifier for the **MPNOTIFY\_CLEAN\_THREAT\_START**/**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**/**MPNOTIFY\_CLEAN\_THREAT\_FAILED** events.</span></span> <span data-ttu-id="cf265-112">Le bit supérieur est défini pour identifier les menaces liées à l’antivirus.</span><span class="sxs-lookup"><span data-stu-id="cf265-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="cf265-113">**ThreatAction**</span><span class="sxs-lookup"><span data-stu-id="cf265-113">**ThreatAction**</span></span>
</dt> <dd>

<span data-ttu-id="cf265-114">Type : **[ **\_ action MPTHREAT**](mpthreat-action.md)**</span><span class="sxs-lookup"><span data-stu-id="cf265-114">Type: **[**MPTHREAT\_ACTION**](mpthreat-action.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cf265-115">Action de la menace pour le nettoyage des menaces **MPNOTIFY \_ \_ \_ Démarrer** / **MPNOTIFY nettoyer les menaces \_ \_ \_ réussies** / **MPNOTIFY \_ nettoyer les \_ menaces \_ ayant échoué** .</span><span class="sxs-lookup"><span data-stu-id="cf265-115">Threat action for the **MPNOTIFY\_CLEAN\_THREAT\_START**/**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**/**MPNOTIFY\_CLEAN\_THREAT\_FAILED** events.</span></span> <span data-ttu-id="cf265-116">Consultez [**\_ action MPTHREAT**](mpthreat-action.md).</span><span class="sxs-lookup"><span data-stu-id="cf265-116">See [**MPTHREAT\_ACTION**](mpthreat-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf265-117">**dwStatus**</span><span class="sxs-lookup"><span data-stu-id="cf265-117">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="cf265-118">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cf265-118">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="cf265-119">État ou actions supplémentaires associées à l’action effectuée.</span><span class="sxs-lookup"><span data-stu-id="cf265-119">Additional status or actions associated with the action taken.</span></span> <span data-ttu-id="cf265-120">Il s’agit d’une combinaison de bits indicateurs à partir de l' [**\_ indicateur MPSTATUS**](mpstatus-flag.md).</span><span class="sxs-lookup"><span data-stu-id="cf265-120">This is a combination of bit flags from [**MPSTATUS\_FLAG**](mpstatus-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf265-121">**ResourceInfo**</span><span class="sxs-lookup"><span data-stu-id="cf265-121">**ResourceInfo**</span></span>
</dt> <dd>

<span data-ttu-id="cf265-122">Type : **PMPRESOURCE \_ info**</span><span class="sxs-lookup"><span data-stu-id="cf265-122">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="cf265-123">Les informations sur les ressources pour les événements **MPNOTIFY \_ Clean \_ Threat \_ Start** / **MPNOTIFY \_ Clean \_ Threat \_ réussie** / **MPNOTIFY \_ Clean \_ Threat \_ failed** .</span><span class="sxs-lookup"><span data-stu-id="cf265-123">Resource information for the **MPNOTIFY\_CLEAN\_THREAT\_START**/**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**/**MPNOTIFY\_CLEAN\_THREAT\_FAILED** events.</span></span> <span data-ttu-id="cf265-124">Consultez [**MPRESOURCE \_ info**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="cf265-124">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf265-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf265-125">Requirements</span></span>



| <span data-ttu-id="cf265-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf265-126">Requirement</span></span> | <span data-ttu-id="cf265-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf265-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf265-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf265-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cf265-129">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf265-129">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="cf265-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf265-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cf265-131">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf265-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf265-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="cf265-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf265-133"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf265-133"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf265-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf265-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf265-135">**\_informations MPRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="cf265-135">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="cf265-136">**\_indicateur MPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="cf265-136">**MPSTATUS\_FLAG**</span></span>](mpstatus-flag.md)
</dt> <dt>

[<span data-ttu-id="cf265-137">**\_action MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="cf265-137">**MPTHREAT\_ACTION**</span></span>](mpthreat-action.md)
</dt> </dl>

 

 





