---
title: Classe MDM_Policy_Config01_DeviceGuard02
description: La \_ stratégie MDM \_ Config01 \_ DeviceGuard02 configure les stratégies Device Guard.
ms.assetid: b8edf906-2486-4d8d-9410-d216bacf1728
keywords:
- Classe MDM_Policy_Config01_DeviceGuard02
- Classe MDM_Policy_Config01_DeviceGuard02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DeviceGuard02
- MDM_Policy_Config01_DeviceGuard02.InstanceID
- MDM_Policy_Config01_DeviceGuard02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ebcc8f3d929708cdff3ada8fe440f49a1aeb1ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032407"
---
# <a name="mdm_policy_config01_deviceguard02-class"></a><span data-ttu-id="6d66c-105">\_Classe DeviceGuard02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="6d66c-105">MDM\_Policy\_Config01\_DeviceGuard02 class</span></span>

<span data-ttu-id="6d66c-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="6d66c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6d66c-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="6d66c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6d66c-108">La \_ stratégie MDM \_ Config01 \_ DeviceGuard02 configure les stratégies Device Guard.</span><span class="sxs-lookup"><span data-stu-id="6d66c-108">The MDM\_Policy\_Config01\_DeviceGuard02 configures the Device Guard policies.</span></span>

<span data-ttu-id="6d66c-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6d66c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d66c-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d66c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DeviceGuard02
{
  string InstanceID;
  string ParentID;
  sint32 EnableVirtualizationBasedSecurity;
  sint32 LsaCfgFlags;
  sint32 RequirePlatformSecurityFeatures;
};
```

## <a name="members"></a><span data-ttu-id="6d66c-111">Membres</span><span class="sxs-lookup"><span data-stu-id="6d66c-111">Members</span></span>

<span data-ttu-id="6d66c-112">La **classe \_ \_ Config01 \_ DeviceGuard02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6d66c-112">The **MDM\_Policy\_Config01\_DeviceGuard02** class has these types of members:</span></span>

-   [<span data-ttu-id="6d66c-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6d66c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6d66c-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6d66c-114">Properties</span></span>

<span data-ttu-id="6d66c-115">La **classe \_ \_ Config01 \_ DeviceGuard02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6d66c-115">The **MDM\_Policy\_Config01\_DeviceGuard02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6d66c-116">EnableVirtualizationBasedSecurity</span><span class="sxs-lookup"><span data-stu-id="6d66c-116">EnableVirtualizationBasedSecurity</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-enablevirtualizationbasedsecurity)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d66c-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6d66c-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d66c-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6d66c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6d66c-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6d66c-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d66c-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6d66c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d66c-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6d66c-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d66c-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6d66c-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6d66c-123">LsaCfgFlags</span><span class="sxs-lookup"><span data-stu-id="6d66c-123">LsaCfgFlags</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-lsacfgflags)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d66c-124">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6d66c-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d66c-125">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6d66c-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6d66c-126">**ID**</span><span class="sxs-lookup"><span data-stu-id="6d66c-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d66c-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6d66c-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d66c-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6d66c-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d66c-129">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6d66c-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6d66c-130">RequirePlatformSecurityFeatures</span><span class="sxs-lookup"><span data-stu-id="6d66c-130">RequirePlatformSecurityFeatures</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-requireplatformsecurityfeatures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d66c-131">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6d66c-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d66c-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6d66c-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d66c-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d66c-133">Requirements</span></span>



| <span data-ttu-id="6d66c-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d66c-134">Requirement</span></span> | <span data-ttu-id="6d66c-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d66c-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d66c-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d66c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6d66c-137">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d66c-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6d66c-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d66c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6d66c-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d66c-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6d66c-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6d66c-140">Namespace</span></span><br/>                | <span data-ttu-id="6d66c-141">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="6d66c-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="6d66c-142">MOF</span><span class="sxs-lookup"><span data-stu-id="6d66c-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d66c-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d66c-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d66c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="6d66c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d66c-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d66c-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

