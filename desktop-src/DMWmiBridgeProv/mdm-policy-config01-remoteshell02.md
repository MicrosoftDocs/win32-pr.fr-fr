---
title: Classe MDM_Policy_Config01_RemoteShell02
description: La \_ classe Config01 RemoteShell02 de la stratégie MDM \_ \_ configure les stratégies de l’interpréteur de commandes à distance.
ms.assetid: 7026fadb-ec6a-4696-a24c-1b1e071b94b0
keywords:
- Classe MDM_Policy_Config01_RemoteShell02
- Classe MDM_Policy_Config01_RemoteShell02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteShell02
- MDM_Policy_Config01_RemoteShell02.InstanceID
- MDM_Policy_Config01_RemoteShell02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c318b0c6f23e92d90091495fdc25993d6958ca56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465454"
---
# <a name="mdm_policy_config01_remoteshell02-class"></a><span data-ttu-id="62584-105">\_Classe RemoteShell02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="62584-105">MDM\_Policy\_Config01\_RemoteShell02 class</span></span>

<span data-ttu-id="62584-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="62584-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="62584-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="62584-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="62584-108">La \_ classe Config01 RemoteShell02 de la stratégie MDM \_ \_ configure les stratégies de l’interpréteur de commandes à distance.</span><span class="sxs-lookup"><span data-stu-id="62584-108">The MDM\_Policy\_Config01\_RemoteShell02 class configures the remote shell policies.</span></span>

<span data-ttu-id="62584-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="62584-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="62584-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62584-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteShell02
{
  string InstanceID;
  string ParentID;
  string AllowRemoteShellAccess;
  string MaxConcurrentUsers;
  string SpecifyIdleTimeout;
  string SpecifyMaxMemory;
  string SpecifyMaxProcesses;
  string SpecifyMaxRemoteShells;
  string SpecifyShellTimeout;
};
```

## <a name="members"></a><span data-ttu-id="62584-111">Membres</span><span class="sxs-lookup"><span data-stu-id="62584-111">Members</span></span>

<span data-ttu-id="62584-112">La **classe \_ \_ Config01 \_ RemoteShell02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="62584-112">The **MDM\_Policy\_Config01\_RemoteShell02** class has these types of members:</span></span>

-   [<span data-ttu-id="62584-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="62584-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="62584-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="62584-114">Properties</span></span>

<span data-ttu-id="62584-115">La **classe \_ \_ Config01 \_ RemoteShell02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="62584-115">The **MDM\_Policy\_Config01\_RemoteShell02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="62584-116">AllowRemoteShellAccess</span><span class="sxs-lookup"><span data-stu-id="62584-116">AllowRemoteShellAccess</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-allowremoteshellaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="62584-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="62584-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62584-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="62584-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="62584-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="62584-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62584-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="62584-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62584-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62584-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62584-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="62584-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="62584-123">MaxConcurrentUsers</span><span class="sxs-lookup"><span data-stu-id="62584-123">MaxConcurrentUsers</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-maxconcurrentusers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="62584-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="62584-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62584-125">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="62584-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="62584-126">**ID**</span><span class="sxs-lookup"><span data-stu-id="62584-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62584-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="62584-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62584-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="62584-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62584-129">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="62584-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="62584-130">SpecifyIdleTimeout</span><span class="sxs-lookup"><span data-stu-id="62584-130">SpecifyIdleTimeout</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifyidletimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="62584-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="62584-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62584-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="62584-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="62584-133">SpecifyMaxMemory</span><span class="sxs-lookup"><span data-stu-id="62584-133">SpecifyMaxMemory</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxmemory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="62584-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="62584-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62584-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="62584-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="62584-136">SpecifyMaxProcesses</span><span class="sxs-lookup"><span data-stu-id="62584-136">SpecifyMaxProcesses</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="62584-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="62584-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62584-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="62584-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="62584-139">SpecifyMaxRemoteShells</span><span class="sxs-lookup"><span data-stu-id="62584-139">SpecifyMaxRemoteShells</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxremoteshells)
</dt> <dd> <dl> <dt>

<span data-ttu-id="62584-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="62584-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62584-141">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="62584-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="62584-142">SpecifyShellTimeout</span><span class="sxs-lookup"><span data-stu-id="62584-142">SpecifyShellTimeout</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifyshelltimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="62584-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="62584-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62584-144">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="62584-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="62584-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62584-145">Requirements</span></span>



| <span data-ttu-id="62584-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62584-146">Requirement</span></span> | <span data-ttu-id="62584-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="62584-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62584-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62584-148">Minimum supported client</span></span><br/> | <span data-ttu-id="62584-149">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62584-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="62584-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62584-150">Minimum supported server</span></span><br/> | <span data-ttu-id="62584-151">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="62584-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="62584-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="62584-152">Namespace</span></span><br/>                | <span data-ttu-id="62584-153">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="62584-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="62584-154">MOF</span><span class="sxs-lookup"><span data-stu-id="62584-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62584-155"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62584-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="62584-156">DLL</span><span class="sxs-lookup"><span data-stu-id="62584-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62584-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62584-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

