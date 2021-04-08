---
title: Classe MDM_Policy_Config01_RemoteAssistance02
description: La \_ classe Config01 RemoteAssistance02 de la stratégie MDM \_ \_ configure les stratégies d’assistance à distance.
ms.assetid: bcc6c570-66d9-4dcd-b7f2-2d03733c0bcb
keywords:
- Classe MDM_Policy_Config01_RemoteAssistance02
- Classe MDM_Policy_Config01_RemoteAssistance02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteAssistance02
- MDM_Policy_Config01_RemoteAssistance02.InstanceID
- MDM_Policy_Config01_RemoteAssistance02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aceadb2eb784e72e4e332cdd34df44d779c99e97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843541"
---
# <a name="mdm_policy_config01_remoteassistance02-class"></a><span data-ttu-id="4739a-105">\_Classe RemoteAssistance02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="4739a-105">MDM\_Policy\_Config01\_RemoteAssistance02 class</span></span>

<span data-ttu-id="4739a-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="4739a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4739a-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="4739a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4739a-108">La \_ classe Config01 RemoteAssistance02 de la stratégie MDM \_ \_ configure les stratégies d’assistance à distance.</span><span class="sxs-lookup"><span data-stu-id="4739a-108">The MDM\_Policy\_Config01\_RemoteAssistance02 class configures the remote assistance policies.</span></span>

<span data-ttu-id="4739a-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4739a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4739a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4739a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteAssistance02
{
  string InstanceID;
  string ParentID;
  string CustomizeWarningMessages;
  string SessionLogging;
  string SolicitedRemoteAssistance;
  string UnsolicitedRemoteAssistance;
};
```

## <a name="members"></a><span data-ttu-id="4739a-111">Membres</span><span class="sxs-lookup"><span data-stu-id="4739a-111">Members</span></span>

<span data-ttu-id="4739a-112">La **classe \_ \_ Config01 \_ RemoteAssistance02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4739a-112">The **MDM\_Policy\_Config01\_RemoteAssistance02** class has these types of members:</span></span>

-   [<span data-ttu-id="4739a-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4739a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4739a-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4739a-114">Properties</span></span>

<span data-ttu-id="4739a-115">La **classe \_ \_ Config01 \_ RemoteAssistance02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="4739a-115">The **MDM\_Policy\_Config01\_RemoteAssistance02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="4739a-116">CustomizeWarningMessages</span><span class="sxs-lookup"><span data-stu-id="4739a-116">CustomizeWarningMessages</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-customizewarningmessages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4739a-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4739a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4739a-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4739a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4739a-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4739a-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4739a-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4739a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4739a-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4739a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4739a-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4739a-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4739a-123">**ID**</span><span class="sxs-lookup"><span data-stu-id="4739a-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4739a-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4739a-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4739a-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4739a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4739a-126">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4739a-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4739a-127">SessionLogging</span><span class="sxs-lookup"><span data-stu-id="4739a-127">SessionLogging</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-sessionlogging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4739a-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4739a-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4739a-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4739a-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4739a-130">SolicitedRemoteAssistance</span><span class="sxs-lookup"><span data-stu-id="4739a-130">SolicitedRemoteAssistance</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-solicitedremoteassistance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4739a-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4739a-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4739a-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4739a-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4739a-133">UnsolicitedRemoteAssistance</span><span class="sxs-lookup"><span data-stu-id="4739a-133">UnsolicitedRemoteAssistance</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-unsolicitedremoteassistance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4739a-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4739a-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4739a-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4739a-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4739a-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4739a-136">Requirements</span></span>



| <span data-ttu-id="4739a-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4739a-137">Requirement</span></span> | <span data-ttu-id="4739a-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="4739a-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4739a-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4739a-139">Minimum supported client</span></span><br/> | <span data-ttu-id="4739a-140">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4739a-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4739a-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4739a-141">Minimum supported server</span></span><br/> | <span data-ttu-id="4739a-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4739a-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="4739a-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4739a-143">Namespace</span></span><br/>                | <span data-ttu-id="4739a-144">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="4739a-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="4739a-145">MOF</span><span class="sxs-lookup"><span data-stu-id="4739a-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4739a-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4739a-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4739a-147">DLL</span><span class="sxs-lookup"><span data-stu-id="4739a-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4739a-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4739a-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

