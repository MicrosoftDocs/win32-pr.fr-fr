---
title: Classe MDM_Policy_Result01_EventLogService02
description: La \_ classe Result01 EventLogService02 de la stratégie MDM \_ \_ représente le comportement du journal des événements.
ms.assetid: 6d4908e9-d283-486a-8309-57d5c5ec83d0
keywords:
- Classe MDM_Policy_Result01_EventLogService02
- Classe MDM_Policy_Result01_EventLogService02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_EventLogService02
- MDM_Policy_Result01_EventLogService02.InstanceID
- MDM_Policy_Result01_EventLogService02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 914a00c3646490e5d4679579aab7a38474a34f00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465434"
---
# <a name="mdm_policy_result01_eventlogservice02-class"></a><span data-ttu-id="c691b-105">\_Classe EventLogService02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="c691b-105">MDM\_Policy\_Result01\_EventLogService02 class</span></span>

<span data-ttu-id="c691b-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="c691b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c691b-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="c691b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c691b-108">La \_ classe Result01 EventLogService02 de la stratégie MDM \_ \_ représente le comportement du journal des événements.</span><span class="sxs-lookup"><span data-stu-id="c691b-108">The MDM\_Policy\_Result01\_EventLogService02 class represents the event log behavior.</span></span>

<span data-ttu-id="c691b-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c691b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c691b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c691b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_EventLogService02
{
  string InstanceID;
  string ParentID;
  string ControlEventLogBehavior;
  string SpecifyMaximumFileSizeApplicationLog;
  string SpecifyMaximumFileSizeSecurityLog;
  string SpecifyMaximumFileSizeSystemLog;
};
```

## <a name="members"></a><span data-ttu-id="c691b-111">Membres</span><span class="sxs-lookup"><span data-stu-id="c691b-111">Members</span></span>

<span data-ttu-id="c691b-112">La **classe \_ \_ Result01 \_ EventLogService02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c691b-112">The **MDM\_Policy\_Result01\_EventLogService02** class has these types of members:</span></span>

-   [<span data-ttu-id="c691b-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c691b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c691b-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c691b-114">Properties</span></span>

<span data-ttu-id="c691b-115">La **classe \_ \_ Result01 \_ EventLogService02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c691b-115">The **MDM\_Policy\_Result01\_EventLogService02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c691b-116">ControlEventLogBehavior</span><span class="sxs-lookup"><span data-stu-id="c691b-116">ControlEventLogBehavior</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-controleventlogbehavior)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c691b-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c691b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c691b-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c691b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c691b-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c691b-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c691b-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c691b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c691b-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c691b-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c691b-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c691b-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c691b-123">**ID**</span><span class="sxs-lookup"><span data-stu-id="c691b-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c691b-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c691b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c691b-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c691b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c691b-126">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c691b-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c691b-127">SpecifyMaximumFileSizeApplicationLog</span><span class="sxs-lookup"><span data-stu-id="c691b-127">SpecifyMaximumFileSizeApplicationLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizeapplicationlog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c691b-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c691b-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c691b-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c691b-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c691b-130">SpecifyMaximumFileSizeSecurityLog</span><span class="sxs-lookup"><span data-stu-id="c691b-130">SpecifyMaximumFileSizeSecurityLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizesecuritylog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c691b-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c691b-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c691b-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c691b-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c691b-133">SpecifyMaximumFileSizeSystemLog</span><span class="sxs-lookup"><span data-stu-id="c691b-133">SpecifyMaximumFileSizeSystemLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizesystemlog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c691b-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c691b-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c691b-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c691b-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c691b-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c691b-136">Requirements</span></span>



| <span data-ttu-id="c691b-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c691b-137">Requirement</span></span> | <span data-ttu-id="c691b-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="c691b-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c691b-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c691b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c691b-140">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c691b-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c691b-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c691b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c691b-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c691b-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c691b-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c691b-143">Namespace</span></span><br/>                | <span data-ttu-id="c691b-144">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="c691b-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c691b-145">MOF</span><span class="sxs-lookup"><span data-stu-id="c691b-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c691b-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c691b-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c691b-147">DLL</span><span class="sxs-lookup"><span data-stu-id="c691b-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c691b-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c691b-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

