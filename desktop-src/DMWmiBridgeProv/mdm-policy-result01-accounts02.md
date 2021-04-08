---
title: Classe MDM_Policy_Result01_Accounts02
description: La \_ \_ classe Accounts02 de la stratégie MDM Result01 représente des \_ stratégies liées aux comptes.
ms.assetid: 581d63de-6ea8-4c4a-8b94-06228ed07371
keywords:
- Classe MDM_Policy_Result01_Accounts02
- Classe MDM_Policy_Result01_Accounts02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Accounts02
- MDM_Policy_Result01_Accounts02.InstanceID
- MDM_Policy_Result01_Accounts02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e5c240f9cd4d3703122c0ea051f35ec8326e2df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741668"
---
# <a name="mdm_policy_result01_accounts02-class"></a><span data-ttu-id="08167-105">\_Classe Accounts02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="08167-105">MDM\_Policy\_Result01\_Accounts02 class</span></span>

<span data-ttu-id="08167-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="08167-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="08167-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="08167-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="08167-108">La classe Accounts02 de la **\_ stratégie MDM \_ Result01 \_** représente des stratégies liées aux comptes.</span><span class="sxs-lookup"><span data-stu-id="08167-108">The **MDM\_Policy\_Result01\_Accounts02** class represents policies related to accounts.</span></span>

<span data-ttu-id="08167-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="08167-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="08167-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08167-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Accounts02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMicrosoftAccountConnection;
  sint32 AllowMicrosoftAccountSignInAssistant;
  sint32 AllowAddingNonMicrosoftAccountsManually;
  string DomainNamesForEmailSync;
};
```

## <a name="members"></a><span data-ttu-id="08167-111">Membres</span><span class="sxs-lookup"><span data-stu-id="08167-111">Members</span></span>

<span data-ttu-id="08167-112">La **classe \_ \_ Result01 \_ Accounts02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="08167-112">The **MDM\_Policy\_Result01\_Accounts02** class has these types of members:</span></span>

-   [<span data-ttu-id="08167-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="08167-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="08167-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="08167-114">Properties</span></span>

<span data-ttu-id="08167-115">La **classe \_ \_ Result01 \_ Accounts02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="08167-115">The **MDM\_Policy\_Result01\_Accounts02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="08167-116">AllowAddingNonMicrosoftAccountsManually</span><span class="sxs-lookup"><span data-stu-id="08167-116">AllowAddingNonMicrosoftAccountsManually</span></span>](/windows/client-management/mdm/policy-csp-accounts#accounts-allowaddingnonmicrosoftaccountsmanually)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08167-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="08167-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08167-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="08167-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08167-119">AllowMicrosoftAccountConnection</span><span class="sxs-lookup"><span data-stu-id="08167-119">AllowMicrosoftAccountConnection</span></span>](/windows/client-management/mdm/policy-csp-accounts#accounts-allowmicrosoftaccountconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08167-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="08167-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08167-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="08167-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08167-122">AllowMicrosoftAccountSignInAssistant</span><span class="sxs-lookup"><span data-stu-id="08167-122">AllowMicrosoftAccountSignInAssistant</span></span>](/windows/client-management/mdm/policy-csp-accounts#accounts-allowmicrosoftaccountsigninassistant)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08167-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="08167-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08167-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="08167-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="08167-125">DomainNamesForEmailSync</span><span class="sxs-lookup"><span data-stu-id="08167-125">DomainNamesForEmailSync</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08167-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="08167-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08167-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="08167-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="08167-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="08167-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08167-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="08167-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08167-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08167-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08167-131">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="08167-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="08167-132">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="08167-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="08167-133">Pour cette classe, la chaîne est « Accounts ».</span><span class="sxs-lookup"><span data-stu-id="08167-133">For this class, the string is "Accounts".</span></span>

</dd> <dt>

<span data-ttu-id="08167-134">**ID**</span><span class="sxs-lookup"><span data-stu-id="08167-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08167-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="08167-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08167-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08167-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08167-137">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="08167-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="08167-138">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="08167-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="08167-139">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Result »</span><span class="sxs-lookup"><span data-stu-id="08167-139">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="08167-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08167-140">Requirements</span></span>



| <span data-ttu-id="08167-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08167-141">Requirement</span></span> | <span data-ttu-id="08167-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="08167-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08167-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08167-143">Minimum supported client</span></span><br/> | <span data-ttu-id="08167-144">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08167-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="08167-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08167-145">Minimum supported server</span></span><br/> | <span data-ttu-id="08167-146">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="08167-146">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="08167-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="08167-147">Namespace</span></span><br/>                | <span data-ttu-id="08167-148">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="08167-148">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="08167-149">MOF</span><span class="sxs-lookup"><span data-stu-id="08167-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08167-150"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08167-150"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="08167-151">DLL</span><span class="sxs-lookup"><span data-stu-id="08167-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08167-152"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08167-152"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08167-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08167-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08167-154">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="08167-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

