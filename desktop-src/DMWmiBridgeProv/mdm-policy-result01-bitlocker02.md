---
title: Classe MDM_Policy_Result01_BitLocker02
description: La \_ classe Result01 Bitlocker02 de la stratégie MDM \_ \_ représente les stratégies BitLocker disponibles.
ms.assetid: 5b20a129-65a8-4ec1-b938-57ddaca46ac3
keywords:
- Classe MDM_Policy_Result01_BitLocker02
- Classe MDM_Policy_Result01_BitLocker02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_BitLocker02
- MDM_Policy_Result01_BitLocker02.InstanceID
- MDM_Policy_Result01_BitLocker02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b063ab67411d8be7fc4c819934b63c0af0096ec5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466878"
---
# <a name="mdm_policy_result01_bitlocker02-class"></a><span data-ttu-id="fd89a-105">\_Classe BitLocker02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="fd89a-105">MDM\_Policy\_Result01\_BitLocker02 class</span></span>

<span data-ttu-id="fd89a-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="fd89a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fd89a-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="fd89a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fd89a-108">La **classe \_ \_ Result01 \_ Bitlocker02 de la stratégie MDM** représente les stratégies BitLocker disponibles.</span><span class="sxs-lookup"><span data-stu-id="fd89a-108">The **MDM\_Policy\_Result01\_Bitlocker02** class represents the BitLocker policies available.</span></span>

<span data-ttu-id="fd89a-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fd89a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd89a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd89a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_BitLocker02
{
  string InstanceID;
  string ParentID;
  sint32 EncryptionMethod;
};
```

## <a name="members"></a><span data-ttu-id="fd89a-111">Membres</span><span class="sxs-lookup"><span data-stu-id="fd89a-111">Members</span></span>

<span data-ttu-id="fd89a-112">La **classe \_ \_ Result01 \_ BitLocker02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fd89a-112">The **MDM\_Policy\_Result01\_BitLocker02** class has these types of members:</span></span>

-   [<span data-ttu-id="fd89a-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fd89a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fd89a-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fd89a-114">Properties</span></span>

<span data-ttu-id="fd89a-115">La **classe \_ \_ Result01 \_ BitLocker02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fd89a-115">The **MDM\_Policy\_Result01\_BitLocker02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fd89a-116">EncryptionMethod</span><span class="sxs-lookup"><span data-stu-id="fd89a-116">EncryptionMethod</span></span>](/windows/client-management/mdm/policy-csp-bitlocker#bitlocker-encryptionmethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd89a-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fd89a-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd89a-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fd89a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fd89a-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fd89a-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd89a-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd89a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd89a-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd89a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd89a-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fd89a-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fd89a-123">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="fd89a-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="fd89a-124">Pour cette classe, la chaîne est « BitLocker »</span><span class="sxs-lookup"><span data-stu-id="fd89a-124">For this class, the string is "BitLocker"</span></span>

</dd> <dt>

<span data-ttu-id="fd89a-125">**ID**</span><span class="sxs-lookup"><span data-stu-id="fd89a-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd89a-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd89a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd89a-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd89a-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd89a-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fd89a-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fd89a-129">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="fd89a-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="fd89a-130">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Result »</span><span class="sxs-lookup"><span data-stu-id="fd89a-130">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd89a-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd89a-131">Requirements</span></span>



| <span data-ttu-id="fd89a-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd89a-132">Requirement</span></span> | <span data-ttu-id="fd89a-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd89a-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd89a-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd89a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fd89a-135">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd89a-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd89a-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd89a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fd89a-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd89a-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="fd89a-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fd89a-138">Namespace</span></span><br/>                | <span data-ttu-id="fd89a-139">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="fd89a-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="fd89a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="fd89a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd89a-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd89a-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd89a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="fd89a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd89a-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd89a-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd89a-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd89a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd89a-145">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="fd89a-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

