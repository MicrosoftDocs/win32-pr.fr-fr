---
title: Classe MDM_PassportForWork_PINComplexity03
description: La \_ \_ classe PINComplexity03 MDM PassportForWork définit la complexité du code confidentiel pour les informations d’identification de connexion pour Windows Hello entreprise.
ms.assetid: 83dcf859-03da-4508-b809-bafd24dc8bd4
keywords:
- Classe MDM_PassportForWork_PINComplexity03
- Classe MDM_PassportForWork_PINComplexity03, Description
topic_type:
- apiref
api_name:
- MDM_PassportForWork_PINComplexity03
- MDM_PassportForWork_PINComplexity03.InstanceID
- MDM_PassportForWork_PINComplexity03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a9d01cd152935a1daa0a9b0721ea27129e21934
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941935"
---
# <a name="mdm_passportforwork_pincomplexity03-class"></a><span data-ttu-id="40714-105">\_ \_ Classe PINCOMPLEXITY03 PassportForWork MDM</span><span class="sxs-lookup"><span data-stu-id="40714-105">MDM\_PassportForWork\_PINComplexity03 class</span></span>

<span data-ttu-id="40714-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="40714-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="40714-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="40714-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="40714-108">La **classe \_ \_ PINComplexity03 MDM PassportForWork** définit la complexité du code confidentiel pour les informations d’identification de connexion pour Windows Hello entreprise.</span><span class="sxs-lookup"><span data-stu-id="40714-108">The **MDM\_PassportForWork\_PINComplexity03** class defines the PIN complexity for the logon credentials for Windows Hello for Business.</span></span>

<span data-ttu-id="40714-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="40714-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="40714-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40714-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_PINComplexity03
{
  string InstanceID;
  string ParentID;
  sint32 MinimumPINLength;
  sint32 MaximumPINLength;
  sint32 UppercaseLetters;
  sint32 LowercaseLetters;
  sint32 SpecialCharacters;
  sint32 Digits;
  sint32 History;
  sint32 Expiration;
};
```

## <a name="members"></a><span data-ttu-id="40714-111">Membres</span><span class="sxs-lookup"><span data-stu-id="40714-111">Members</span></span>

<span data-ttu-id="40714-112">La **classe \_ PassportForWork \_ PINComplexity03 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="40714-112">The **MDM\_PassportForWork\_PINComplexity03** class has these types of members:</span></span>

-   [<span data-ttu-id="40714-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="40714-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="40714-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="40714-114">Properties</span></span>

<span data-ttu-id="40714-115">La **classe \_ PassportForWork \_ PINComplexity03 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="40714-115">The **MDM\_PassportForWork\_PINComplexity03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="40714-116">Chiffres</span><span class="sxs-lookup"><span data-stu-id="40714-116">Digits</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-digits)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40714-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="40714-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="40714-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40714-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40714-119">Expiration</span><span class="sxs-lookup"><span data-stu-id="40714-119">Expiration</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-expiration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40714-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="40714-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="40714-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40714-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40714-122">History</span><span class="sxs-lookup"><span data-stu-id="40714-122">History</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-history)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40714-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="40714-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="40714-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40714-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="40714-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="40714-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40714-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40714-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40714-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="40714-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40714-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="40714-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="40714-129">Nœud racine pour les stratégies de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="40714-129">Root node for PIN policies.</span></span>

</dd> <dt>

[<span data-ttu-id="40714-130">LowercaseLetters</span><span class="sxs-lookup"><span data-stu-id="40714-130">LowercaseLetters</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-lowercaseletters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40714-131">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="40714-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="40714-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40714-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40714-133">MaximumPINLength</span><span class="sxs-lookup"><span data-stu-id="40714-133">MaximumPINLength</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-maximumpinlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40714-134">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="40714-134">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="40714-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40714-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40714-136">MinimumPINLength</span><span class="sxs-lookup"><span data-stu-id="40714-136">MinimumPINLength</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-minimumpinlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40714-137">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="40714-137">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="40714-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40714-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="40714-139">**ID**</span><span class="sxs-lookup"><span data-stu-id="40714-139">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40714-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40714-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40714-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="40714-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40714-142">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="40714-142">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="40714-143">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="40714-143">Describes the full path to the parent node.</span></span> <span data-ttu-id="40714-144">Pour cette classe, la chaîne est « ./Vendor/MSFT/PassPortForWork/*TenantID*/Policies »</span><span class="sxs-lookup"><span data-stu-id="40714-144">For this class, the string is "./Vendor/MSFT/PassPortForWork/*TenantID*/Policies"</span></span>

</dd> <dt>

[<span data-ttu-id="40714-145">SpecialCharacters</span><span class="sxs-lookup"><span data-stu-id="40714-145">SpecialCharacters</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-specialcharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40714-146">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="40714-146">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="40714-147">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40714-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40714-148">UppercaseLetters</span><span class="sxs-lookup"><span data-stu-id="40714-148">UppercaseLetters</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-uppercaseletters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40714-149">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="40714-149">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="40714-150">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40714-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="40714-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40714-151">Requirements</span></span>



| <span data-ttu-id="40714-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40714-152">Requirement</span></span> | <span data-ttu-id="40714-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="40714-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40714-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40714-154">Minimum supported client</span></span><br/> | <span data-ttu-id="40714-155">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="40714-155">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="40714-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40714-156">Minimum supported server</span></span><br/> | <span data-ttu-id="40714-157">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="40714-157">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="40714-158">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="40714-158">Namespace</span></span><br/>                | <span data-ttu-id="40714-159">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="40714-159">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="40714-160">MOF</span><span class="sxs-lookup"><span data-stu-id="40714-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40714-161"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40714-161"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="40714-162">DLL</span><span class="sxs-lookup"><span data-stu-id="40714-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40714-163"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40714-163"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40714-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40714-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40714-165">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="40714-165">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

