---
title: Classe MDM_Policy_Config01_Accounts02
description: La \_ \_ classe Accounts02 de la stratégie MDM Config01 représente des \_ stratégies liées aux comptes.
ms.assetid: 628a0745-0ac5-4038-8ea8-04344098682d
keywords:
- Classe MDM_Policy_Config01_Accounts02
- Classe MDM_Policy_Config01_Accounts02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Accounts02
- MDM_Policy_Config01_Accounts02.InstanceID
- MDM_Policy_Config01_Accounts02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8833f1477014f3c7c2200e07c242549f5235fbdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032673"
---
# <a name="mdm_policy_config01_accounts02-class"></a><span data-ttu-id="1dbde-105">\_Classe Accounts02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="1dbde-105">MDM\_Policy\_Config01\_Accounts02 class</span></span>

<span data-ttu-id="1dbde-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="1dbde-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1dbde-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="1dbde-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1dbde-108">La classe Accounts02 de la **\_ stratégie MDM \_ Config01 \_** représente des stratégies liées aux comptes.</span><span class="sxs-lookup"><span data-stu-id="1dbde-108">The **MDM\_Policy\_Config01\_Accounts02** class represents policies related to accounts.</span></span>

<span data-ttu-id="1dbde-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="1dbde-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dbde-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1dbde-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Accounts02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMicrosoftAccountConnection;
  sint32 AllowMicrosoftAccountSignInAssistant;
  sint32 AllowAddingNonMicrosoftAccountsManually;
  string DomainNamesForEmailSync;
};
```

## <a name="members"></a><span data-ttu-id="1dbde-111">Membres</span><span class="sxs-lookup"><span data-stu-id="1dbde-111">Members</span></span>

<span data-ttu-id="1dbde-112">La **classe \_ \_ Config01 \_ Accounts02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1dbde-112">The **MDM\_Policy\_Config01\_Accounts02** class has these types of members:</span></span>

-   [<span data-ttu-id="1dbde-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1dbde-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1dbde-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1dbde-114">Properties</span></span>

<span data-ttu-id="1dbde-115">La **classe \_ \_ Config01 \_ Accounts02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="1dbde-115">The **MDM\_Policy\_Config01\_Accounts02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1dbde-116">AllowAddingNonMicrosoftAccountsManually</span><span class="sxs-lookup"><span data-stu-id="1dbde-116">AllowAddingNonMicrosoftAccountsManually</span></span>](/windows/client-management/mdm/policy-csp-accounts#accounts-allowaddingnonmicrosoftaccountsmanually)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dbde-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1dbde-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1dbde-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1dbde-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1dbde-119">AllowMicrosoftAccountConnection</span><span class="sxs-lookup"><span data-stu-id="1dbde-119">AllowMicrosoftAccountConnection</span></span>](/windows/client-management/mdm/policy-csp-accounts#accounts-allowmicrosoftaccountconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dbde-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1dbde-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1dbde-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1dbde-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1dbde-122">AllowMicrosoftAccountSignInAssistant</span><span class="sxs-lookup"><span data-stu-id="1dbde-122">AllowMicrosoftAccountSignInAssistant</span></span>](/windows/client-management/mdm/policy-csp-accounts#accounts-allowmicrosoftaccountsigninassistant)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dbde-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1dbde-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1dbde-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1dbde-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1dbde-125">DomainNamesForEmailSync</span><span class="sxs-lookup"><span data-stu-id="1dbde-125">DomainNamesForEmailSync</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dbde-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1dbde-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dbde-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1dbde-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1dbde-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1dbde-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dbde-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1dbde-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dbde-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1dbde-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dbde-131">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1dbde-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1dbde-132">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="1dbde-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="1dbde-133">Pour cette classe, la chaîne est « Accounts ».</span><span class="sxs-lookup"><span data-stu-id="1dbde-133">For this class, the string is "Accounts".</span></span>

</dd> <dt>

<span data-ttu-id="1dbde-134">**ID**</span><span class="sxs-lookup"><span data-stu-id="1dbde-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dbde-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1dbde-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dbde-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1dbde-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dbde-137">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1dbde-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1dbde-138">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="1dbde-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="1dbde-139">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Config »</span><span class="sxs-lookup"><span data-stu-id="1dbde-139">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1dbde-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1dbde-140">Requirements</span></span>



| <span data-ttu-id="1dbde-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1dbde-141">Requirement</span></span> | <span data-ttu-id="1dbde-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="1dbde-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dbde-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1dbde-143">Minimum supported client</span></span><br/> | <span data-ttu-id="1dbde-144">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1dbde-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1dbde-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1dbde-145">Minimum supported server</span></span><br/> | <span data-ttu-id="1dbde-146">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1dbde-146">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1dbde-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1dbde-147">Namespace</span></span><br/>                | <span data-ttu-id="1dbde-148">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="1dbde-148">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="1dbde-149">MOF</span><span class="sxs-lookup"><span data-stu-id="1dbde-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1dbde-150"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1dbde-150"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1dbde-151">DLL</span><span class="sxs-lookup"><span data-stu-id="1dbde-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1dbde-152"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1dbde-152"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dbde-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1dbde-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dbde-154">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="1dbde-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

