---
title: Classe MDM_Policy_Result01_DeviceGuard02
description: La \_ classe Result01 DeviceGuard02 de la stratégie MDM \_ \_ configure les stratégies Device Guard.
ms.assetid: ba21d324-85dc-4cb5-8123-196413e457eb
keywords:
- Classe MDM_Policy_Result01_DeviceGuard02
- Classe MDM_Policy_Result01_DeviceGuard02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DeviceGuard02
- MDM_Policy_Result01_DeviceGuard02.InstanceID
- MDM_Policy_Result01_DeviceGuard02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e206a732628e442a391cb8b29f7712f5a5ec8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032596"
---
# <a name="mdm_policy_result01_deviceguard02-class"></a><span data-ttu-id="3b1af-105">\_Classe DeviceGuard02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="3b1af-105">MDM\_Policy\_Result01\_DeviceGuard02 class</span></span>

<span data-ttu-id="3b1af-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="3b1af-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3b1af-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="3b1af-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3b1af-108">La \_ classe Result01 DeviceGuard02 de la stratégie MDM \_ \_ configure les stratégies Device Guard.</span><span class="sxs-lookup"><span data-stu-id="3b1af-108">The MDM\_Policy\_Result01\_DeviceGuard02 class configures the Device Guard policies.</span></span>

<span data-ttu-id="3b1af-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3b1af-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b1af-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b1af-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DeviceGuard02
{
  string InstanceID;
  string ParentID;
  sint32 EnableVirtualizationBasedSecurity;
  sint32 LsaCfgFlags;
  sint32 RequirePlatformSecurityFeatures;
};
```

## <a name="members"></a><span data-ttu-id="3b1af-111">Membres</span><span class="sxs-lookup"><span data-stu-id="3b1af-111">Members</span></span>

<span data-ttu-id="3b1af-112">La **classe \_ \_ Result01 \_ DeviceGuard02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3b1af-112">The **MDM\_Policy\_Result01\_DeviceGuard02** class has these types of members:</span></span>

-   [<span data-ttu-id="3b1af-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3b1af-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b1af-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3b1af-114">Properties</span></span>

<span data-ttu-id="3b1af-115">La **classe \_ \_ Result01 \_ DeviceGuard02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="3b1af-115">The **MDM\_Policy\_Result01\_DeviceGuard02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3b1af-116">EnableVirtualizationBasedSecurity</span><span class="sxs-lookup"><span data-stu-id="3b1af-116">EnableVirtualizationBasedSecurity</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-enablevirtualizationbasedsecurity)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b1af-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="3b1af-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b1af-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3b1af-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3b1af-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3b1af-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b1af-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3b1af-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b1af-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3b1af-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b1af-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3b1af-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3b1af-123">LsaCfgFlags</span><span class="sxs-lookup"><span data-stu-id="3b1af-123">LsaCfgFlags</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-lsacfgflags)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b1af-124">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="3b1af-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b1af-125">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3b1af-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3b1af-126">**ID**</span><span class="sxs-lookup"><span data-stu-id="3b1af-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b1af-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3b1af-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b1af-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3b1af-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b1af-129">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3b1af-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3b1af-130">RequirePlatformSecurityFeatures</span><span class="sxs-lookup"><span data-stu-id="3b1af-130">RequirePlatformSecurityFeatures</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-requireplatformsecurityfeatures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b1af-131">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="3b1af-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b1af-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3b1af-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b1af-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b1af-133">Requirements</span></span>



| <span data-ttu-id="3b1af-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b1af-134">Requirement</span></span> | <span data-ttu-id="3b1af-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b1af-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b1af-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b1af-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3b1af-137">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b1af-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3b1af-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b1af-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3b1af-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b1af-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3b1af-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3b1af-140">Namespace</span></span><br/>                | <span data-ttu-id="3b1af-141">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="3b1af-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="3b1af-142">MOF</span><span class="sxs-lookup"><span data-stu-id="3b1af-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b1af-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b1af-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b1af-144">DLL</span><span class="sxs-lookup"><span data-stu-id="3b1af-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b1af-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b1af-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

