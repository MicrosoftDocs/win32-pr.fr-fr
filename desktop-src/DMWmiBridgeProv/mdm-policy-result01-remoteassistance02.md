---
title: Classe MDM_Policy_Result01_RemoteAssistance02
description: La \_ classe Result01 RemoteAssistance02 de la stratégie MDM \_ \_ représente les stratégies d’assistance à distance.
ms.assetid: ddb932ef-b309-4aad-8ab8-9d88739d90be
keywords:
- Classe MDM_Policy_Result01_RemoteAssistance02
- Classe MDM_Policy_Result01_RemoteAssistance02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_RemoteAssistance02
- MDM_Policy_Result01_RemoteAssistance02.InstanceID
- MDM_Policy_Result01_RemoteAssistance02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ed928668e4851c981ea7c68d02cd1cdbefbda4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032404"
---
# <a name="mdm_policy_result01_remoteassistance02-class"></a><span data-ttu-id="55b08-105">\_Classe RemoteAssistance02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="55b08-105">MDM\_Policy\_Result01\_RemoteAssistance02 class</span></span>

<span data-ttu-id="55b08-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="55b08-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="55b08-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="55b08-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="55b08-108">La \_ classe Result01 RemoteAssistance02 de la stratégie MDM \_ \_ représente les stratégies d’assistance à distance.</span><span class="sxs-lookup"><span data-stu-id="55b08-108">The MDM\_Policy\_Result01\_RemoteAssistance02 class represents the remote assistance policies.</span></span>

<span data-ttu-id="55b08-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="55b08-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="55b08-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55b08-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_RemoteAssistance02
{
  string InstanceID;
  string ParentID;
  string CustomizeWarningMessages;
  string SessionLogging;
  string SolicitedRemoteAssistance;
  string UnsolicitedRemoteAssistance;
};
```

## <a name="members"></a><span data-ttu-id="55b08-111">Membres</span><span class="sxs-lookup"><span data-stu-id="55b08-111">Members</span></span>

<span data-ttu-id="55b08-112">La **classe \_ \_ Result01 \_ RemoteAssistance02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="55b08-112">The **MDM\_Policy\_Result01\_RemoteAssistance02** class has these types of members:</span></span>

-   [<span data-ttu-id="55b08-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="55b08-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="55b08-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="55b08-114">Properties</span></span>

<span data-ttu-id="55b08-115">La **classe \_ \_ Result01 \_ RemoteAssistance02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="55b08-115">The **MDM\_Policy\_Result01\_RemoteAssistance02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="55b08-116">CustomizeWarningMessages</span><span class="sxs-lookup"><span data-stu-id="55b08-116">CustomizeWarningMessages</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-customizewarningmessages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55b08-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="55b08-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55b08-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="55b08-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="55b08-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="55b08-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55b08-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="55b08-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55b08-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="55b08-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55b08-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="55b08-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="55b08-123">**ID**</span><span class="sxs-lookup"><span data-stu-id="55b08-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55b08-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="55b08-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55b08-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="55b08-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55b08-126">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="55b08-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="55b08-127">SessionLogging</span><span class="sxs-lookup"><span data-stu-id="55b08-127">SessionLogging</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-sessionlogging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55b08-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="55b08-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55b08-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="55b08-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="55b08-130">SolicitedRemoteAssistance</span><span class="sxs-lookup"><span data-stu-id="55b08-130">SolicitedRemoteAssistance</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-solicitedremoteassistance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55b08-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="55b08-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55b08-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="55b08-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="55b08-133">UnsolicitedRemoteAssistance</span><span class="sxs-lookup"><span data-stu-id="55b08-133">UnsolicitedRemoteAssistance</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-unsolicitedremoteassistance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55b08-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="55b08-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55b08-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="55b08-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="55b08-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55b08-136">Requirements</span></span>



| <span data-ttu-id="55b08-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55b08-137">Requirement</span></span> | <span data-ttu-id="55b08-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="55b08-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55b08-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55b08-139">Minimum supported client</span></span><br/> | <span data-ttu-id="55b08-140">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55b08-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="55b08-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55b08-141">Minimum supported server</span></span><br/> | <span data-ttu-id="55b08-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="55b08-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="55b08-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="55b08-143">Namespace</span></span><br/>                | <span data-ttu-id="55b08-144">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="55b08-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="55b08-145">MOF</span><span class="sxs-lookup"><span data-stu-id="55b08-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55b08-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55b08-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="55b08-147">DLL</span><span class="sxs-lookup"><span data-stu-id="55b08-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55b08-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55b08-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

