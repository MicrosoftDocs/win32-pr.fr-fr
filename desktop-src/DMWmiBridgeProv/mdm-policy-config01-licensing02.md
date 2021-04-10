---
title: Classe MDM_Policy_Config01_Licensing02
description: La \_ classe Config01 Licensing02 de la stratégie MDM \_ \_ représente les stratégies de licence disponibles.
ms.assetid: 7ec186e9-626e-4361-88fd-665b947ca23d
keywords:
- Classe MDM_Policy_Config01_Licensing02
- Classe MDM_Policy_Config01_Licensing02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Licensing02
- MDM_Policy_Config01_Licensing02.InstanceID
- MDM_Policy_Config01_Licensing02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d654facc7ec3ba08d1f5b0f31497545945cc73d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942110"
---
# <a name="mdm_policy_config01_licensing02-class"></a><span data-ttu-id="33404-105">\_Classe Licensing02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="33404-105">MDM\_Policy\_Config01\_Licensing02 class</span></span>

<span data-ttu-id="33404-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="33404-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="33404-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="33404-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="33404-108">La **classe \_ \_ Config01 \_ Licensing02 de la stratégie MDM** représente les stratégies de licence disponibles.</span><span class="sxs-lookup"><span data-stu-id="33404-108">The **MDM\_Policy\_Config01\_Licensing02** class represents the licensing policies available.</span></span>

<span data-ttu-id="33404-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="33404-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="33404-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33404-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Licensing02
{
  string InstanceID;
  string ParentID;
  sint32 AllowWindowsEntitlementReactivation;
  sint32 DisallowKMSClientOnlineAVSValidation;
};
```

## <a name="members"></a><span data-ttu-id="33404-111">Membres</span><span class="sxs-lookup"><span data-stu-id="33404-111">Members</span></span>

<span data-ttu-id="33404-112">La **classe \_ \_ Config01 \_ Licensing02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="33404-112">The **MDM\_Policy\_Config01\_Licensing02** class has these types of members:</span></span>

-   [<span data-ttu-id="33404-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="33404-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="33404-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="33404-114">Properties</span></span>

<span data-ttu-id="33404-115">La **classe \_ \_ Config01 \_ Licensing02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="33404-115">The **MDM\_Policy\_Config01\_Licensing02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="33404-116">AllowWindowsEntitlementReactivation</span><span class="sxs-lookup"><span data-stu-id="33404-116">AllowWindowsEntitlementReactivation</span></span>](/windows/client-management/mdm/policy-csp-licensing#licensing-allowwindowsentitlementreactivation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33404-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="33404-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33404-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33404-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33404-119">DisallowKMSClientOnlineAVSValidation</span><span class="sxs-lookup"><span data-stu-id="33404-119">DisallowKMSClientOnlineAVSValidation</span></span>](/windows/client-management/mdm/policy-csp-licensing#licensing-disallowkmsclientonlineavsvalidation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33404-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="33404-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33404-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33404-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33404-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="33404-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33404-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33404-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33404-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="33404-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33404-125">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="33404-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="33404-126">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="33404-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="33404-127">Pour cette classe, la chaîne est « Licensing ».</span><span class="sxs-lookup"><span data-stu-id="33404-127">For this class, the string is "Licensing".</span></span>

</dd> <dt>

<span data-ttu-id="33404-128">**ID**</span><span class="sxs-lookup"><span data-stu-id="33404-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33404-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33404-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33404-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="33404-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33404-131">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="33404-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="33404-132">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="33404-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="33404-133">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Config »</span><span class="sxs-lookup"><span data-stu-id="33404-133">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="33404-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33404-134">Requirements</span></span>



| <span data-ttu-id="33404-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33404-135">Requirement</span></span> | <span data-ttu-id="33404-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="33404-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33404-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33404-137">Minimum supported client</span></span><br/> | <span data-ttu-id="33404-138">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33404-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="33404-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33404-139">Minimum supported server</span></span><br/> | <span data-ttu-id="33404-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="33404-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="33404-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="33404-141">Namespace</span></span><br/>                | <span data-ttu-id="33404-142">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="33404-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="33404-143">MOF</span><span class="sxs-lookup"><span data-stu-id="33404-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33404-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33404-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="33404-145">DLL</span><span class="sxs-lookup"><span data-stu-id="33404-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33404-146"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="33404-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

