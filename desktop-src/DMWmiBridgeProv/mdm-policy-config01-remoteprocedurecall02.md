---
title: Classe MDM_Policy_Config01_RemoteProcedureCall02
description: La \_ classe Config01 RemoteProcedureCall02 de la stratégie MDM \_ \_ configure les stratégies d’appel de procédure distante.
ms.assetid: d844c59d-c71e-4a8f-ad1e-955a918a36b8
keywords:
- Classe MDM_Policy_Config01_RemoteProcedureCall02
- Classe MDM_Policy_Config01_RemoteProcedureCall02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteProcedureCall02
- MDM_Policy_Config01_RemoteProcedureCall02.InstanceID
- MDM_Policy_Config01_RemoteProcedureCall02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1c1a188afd3694273080c6c369a8dc37abb22a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465234"
---
# <a name="mdm_policy_config01_remoteprocedurecall02-class"></a><span data-ttu-id="d62b9-105">\_Classe RemoteProcedureCall02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="d62b9-105">MDM\_Policy\_Config01\_RemoteProcedureCall02 class</span></span>

<span data-ttu-id="d62b9-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="d62b9-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d62b9-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="d62b9-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d62b9-108">La \_ classe Config01 RemoteProcedureCall02 de la stratégie MDM \_ \_ configure les stratégies d’appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="d62b9-108">The MDM\_Policy\_Config01\_RemoteProcedureCall02 class configures the remote procedure call policies.</span></span>

<span data-ttu-id="d62b9-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d62b9-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d62b9-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d62b9-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteProcedureCall02
{
  string InstanceID;
  string ParentID;
  string RestrictUnauthenticatedRPCClients;
  string RPCEndpointMapperClientAuthentication;
};
```

## <a name="members"></a><span data-ttu-id="d62b9-111">Membres</span><span class="sxs-lookup"><span data-stu-id="d62b9-111">Members</span></span>

<span data-ttu-id="d62b9-112">La **classe \_ \_ Config01 \_ RemoteProcedureCall02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d62b9-112">The **MDM\_Policy\_Config01\_RemoteProcedureCall02** class has these types of members:</span></span>

-   [<span data-ttu-id="d62b9-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d62b9-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d62b9-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d62b9-114">Properties</span></span>

<span data-ttu-id="d62b9-115">La **classe \_ \_ Config01 \_ RemoteProcedureCall02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d62b9-115">The **MDM\_Policy\_Config01\_RemoteProcedureCall02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d62b9-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d62b9-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62b9-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d62b9-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d62b9-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d62b9-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d62b9-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d62b9-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d62b9-120">**ID**</span><span class="sxs-lookup"><span data-stu-id="d62b9-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62b9-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d62b9-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d62b9-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d62b9-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d62b9-123">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d62b9-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d62b9-124">RestrictUnauthenticatedRPCClients</span><span class="sxs-lookup"><span data-stu-id="d62b9-124">RestrictUnauthenticatedRPCClients</span></span>](/windows/client-management/mdm/policy-csp-remoteprocedurecall#remoteprocedurecall-restrictunauthenticatedrpcclients)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62b9-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d62b9-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d62b9-126">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d62b9-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d62b9-127">RPCEndpointMapperClientAuthentication</span><span class="sxs-lookup"><span data-stu-id="d62b9-127">RPCEndpointMapperClientAuthentication</span></span>](/windows/client-management/mdm/policy-csp-remoteprocedurecall#remoteprocedurecall-rpcendpointmapperclientauthentication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62b9-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d62b9-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d62b9-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d62b9-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d62b9-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d62b9-130">Requirements</span></span>



| <span data-ttu-id="d62b9-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d62b9-131">Requirement</span></span> | <span data-ttu-id="d62b9-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="d62b9-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d62b9-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d62b9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d62b9-134">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d62b9-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d62b9-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d62b9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d62b9-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d62b9-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d62b9-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d62b9-137">Namespace</span></span><br/>                | <span data-ttu-id="d62b9-138">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="d62b9-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d62b9-139">MOF</span><span class="sxs-lookup"><span data-stu-id="d62b9-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d62b9-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d62b9-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d62b9-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d62b9-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d62b9-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d62b9-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

