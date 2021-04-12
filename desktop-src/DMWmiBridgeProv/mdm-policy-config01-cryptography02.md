---
title: Classe MDM_Policy_Config01_Cryptography02
description: La \_ \_ classe Config01 Cryptography02 de la stratégie MDM \_ représente des stratégies liées au chiffrement.
ms.assetid: e1e06dbd-507e-4da5-bcd5-4d551bd99302
keywords:
- Classe MDM_Policy_Config01_Cryptography02
- Classe MDM_Policy_Config01_Cryptography02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Cryptography02
- MDM_Policy_Config01_Cryptography02.InstanceID
- MDM_Policy_Config01_Cryptography02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92f13a5a04e3d312d8ba262359847719652ecc4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464843"
---
# <a name="mdm_policy_config01_cryptography02-class"></a><span data-ttu-id="c0d94-105">\_Classe Cryptography02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="c0d94-105">MDM\_Policy\_Config01\_Cryptography02 class</span></span>

<span data-ttu-id="c0d94-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="c0d94-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c0d94-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="c0d94-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c0d94-108">La **classe \_ \_ Config01 \_ Cryptography02 de la stratégie MDM** représente des stratégies liées au chiffrement.</span><span class="sxs-lookup"><span data-stu-id="c0d94-108">The **MDM\_Policy\_Config01\_Cryptography02** class represents policies related to cryptography.</span></span>

<span data-ttu-id="c0d94-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c0d94-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0d94-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0d94-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Cryptography02
{
  string InstanceID;
  string ParentID;
  sint32 AllowFipsAlgorithmPolicy;
  string TLSCipherSuites;
};
```

## <a name="members"></a><span data-ttu-id="c0d94-111">Membres</span><span class="sxs-lookup"><span data-stu-id="c0d94-111">Members</span></span>

<span data-ttu-id="c0d94-112">La **classe \_ \_ Config01 \_ Cryptography02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c0d94-112">The **MDM\_Policy\_Config01\_Cryptography02** class has these types of members:</span></span>

-   [<span data-ttu-id="c0d94-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c0d94-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c0d94-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c0d94-114">Properties</span></span>

<span data-ttu-id="c0d94-115">La **classe \_ \_ Config01 \_ Cryptography02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c0d94-115">The **MDM\_Policy\_Config01\_Cryptography02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c0d94-116">AllowFipsAlgorithmPolicy</span><span class="sxs-lookup"><span data-stu-id="c0d94-116">AllowFipsAlgorithmPolicy</span></span>](/windows/client-management/mdm/policy-csp-cryptography#cryptography-allowfipsalgorithmpolicy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d94-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c0d94-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0d94-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c0d94-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c0d94-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c0d94-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d94-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c0d94-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0d94-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c0d94-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0d94-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c0d94-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c0d94-123">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="c0d94-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="c0d94-124">Pour cette classe, la chaîne est « Cryptography ».</span><span class="sxs-lookup"><span data-stu-id="c0d94-124">For this class, the string is "Cryptography"</span></span>

</dd> <dt>

<span data-ttu-id="c0d94-125">**ID**</span><span class="sxs-lookup"><span data-stu-id="c0d94-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d94-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c0d94-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0d94-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c0d94-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0d94-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c0d94-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c0d94-129">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="c0d94-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="c0d94-130">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Config »</span><span class="sxs-lookup"><span data-stu-id="c0d94-130">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="c0d94-131">TLSCipherSuites</span><span class="sxs-lookup"><span data-stu-id="c0d94-131">TLSCipherSuites</span></span>](/windows/client-management/mdm/policy-csp-cryptography#cryptography-tlsciphersuites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d94-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c0d94-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0d94-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c0d94-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0d94-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0d94-134">Requirements</span></span>



| <span data-ttu-id="c0d94-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0d94-135">Requirement</span></span> | <span data-ttu-id="c0d94-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0d94-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0d94-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0d94-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c0d94-138">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0d94-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c0d94-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0d94-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c0d94-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0d94-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c0d94-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c0d94-141">Namespace</span></span><br/>                | <span data-ttu-id="c0d94-142">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="c0d94-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c0d94-143">MOF</span><span class="sxs-lookup"><span data-stu-id="c0d94-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0d94-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0d94-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0d94-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c0d94-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0d94-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0d94-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0d94-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0d94-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0d94-148">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="c0d94-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

