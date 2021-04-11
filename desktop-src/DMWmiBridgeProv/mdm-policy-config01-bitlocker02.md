---
title: Classe MDM_Policy_Config01_BitLocker02
description: La \_ classe Config01 Bitlocker02 de la stratégie MDM \_ \_ représente les stratégies BitLocker disponibles.
ms.assetid: 885df93f-41f5-4cf7-8bce-9b253b190e17
keywords:
- Classe MDM_Policy_Config01_BitLocker02
- Classe MDM_Policy_Config01_BitLocker02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_BitLocker02
- MDM_Policy_Config01_BitLocker02.InstanceID
- MDM_Policy_Config01_BitLocker02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 005c16365dfc227aff4c854e77b2a733a3c4ac70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032669"
---
# <a name="mdm_policy_config01_bitlocker02-class"></a><span data-ttu-id="130bf-105">\_Classe BitLocker02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="130bf-105">MDM\_Policy\_Config01\_BitLocker02 class</span></span>

<span data-ttu-id="130bf-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="130bf-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="130bf-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="130bf-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="130bf-108">La **classe \_ \_ Config01 \_ Bitlocker02 de la stratégie MDM** représente les stratégies BitLocker disponibles.</span><span class="sxs-lookup"><span data-stu-id="130bf-108">The **MDM\_Policy\_Config01\_Bitlocker02** class represents the BitLocker policies available.</span></span>

<span data-ttu-id="130bf-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="130bf-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="130bf-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="130bf-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_BitLocker02
{
  string InstanceID;
  string ParentID;
  sint32 EncryptionMethod;
};
```

## <a name="members"></a><span data-ttu-id="130bf-111">Membres</span><span class="sxs-lookup"><span data-stu-id="130bf-111">Members</span></span>

<span data-ttu-id="130bf-112">La **classe \_ \_ Config01 \_ BitLocker02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="130bf-112">The **MDM\_Policy\_Config01\_BitLocker02** class has these types of members:</span></span>

-   [<span data-ttu-id="130bf-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="130bf-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="130bf-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="130bf-114">Properties</span></span>

<span data-ttu-id="130bf-115">La **classe \_ \_ Config01 \_ BitLocker02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="130bf-115">The **MDM\_Policy\_Config01\_BitLocker02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="130bf-116">EncryptionMethod</span><span class="sxs-lookup"><span data-stu-id="130bf-116">EncryptionMethod</span></span>](/windows/client-management/mdm/policy-csp-bitlocker#bitlocker-encryptionmethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="130bf-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="130bf-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="130bf-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="130bf-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="130bf-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="130bf-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="130bf-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="130bf-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="130bf-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="130bf-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="130bf-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="130bf-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="130bf-123">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="130bf-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="130bf-124">Pour cette classe, la chaîne est « BitLocker »</span><span class="sxs-lookup"><span data-stu-id="130bf-124">For this class, the string is "BitLocker"</span></span>

</dd> <dt>

<span data-ttu-id="130bf-125">**ID**</span><span class="sxs-lookup"><span data-stu-id="130bf-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="130bf-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="130bf-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="130bf-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="130bf-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="130bf-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="130bf-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="130bf-129">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="130bf-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="130bf-130">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Config »</span><span class="sxs-lookup"><span data-stu-id="130bf-130">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="130bf-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="130bf-131">Requirements</span></span>



| <span data-ttu-id="130bf-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="130bf-132">Requirement</span></span> | <span data-ttu-id="130bf-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="130bf-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="130bf-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="130bf-134">Minimum supported client</span></span><br/> | <span data-ttu-id="130bf-135">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="130bf-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="130bf-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="130bf-136">Minimum supported server</span></span><br/> | <span data-ttu-id="130bf-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="130bf-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="130bf-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="130bf-138">Namespace</span></span><br/>                | <span data-ttu-id="130bf-139">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="130bf-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="130bf-140">MOF</span><span class="sxs-lookup"><span data-stu-id="130bf-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="130bf-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="130bf-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="130bf-142">DLL</span><span class="sxs-lookup"><span data-stu-id="130bf-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="130bf-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="130bf-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="130bf-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="130bf-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="130bf-145">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="130bf-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

