---
title: Classe MDM_Policy_Result01_Authentication02
description: La \_ classe Result01 Authentication02 de la stratégie MDM \_ \_ représente les stratégies de gestion des authentifications disponibles.
ms.assetid: a67275dc-5f4d-4672-9a6e-84fa65cde3ad
keywords:
- Classe MDM_Policy_Result01_Authentication02
- Classe MDM_Policy_Result01_Authentication02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Authentication02
- MDM_Policy_Result01_Authentication02.InstanceID
- MDM_Policy_Result01_Authentication02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80d80979fe7b025ea7b0677436036c8760d4b0ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106135"
---
# <a name="mdm_policy_result01_authentication02-class"></a><span data-ttu-id="18589-105">\_Classe Authentication02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="18589-105">MDM\_Policy\_Result01\_Authentication02 class</span></span>

<span data-ttu-id="18589-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="18589-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="18589-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="18589-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="18589-108">La **classe \_ \_ Result01 \_ Authentication02 de la stratégie MDM** représente les stratégies de gestion des authentifications disponibles.</span><span class="sxs-lookup"><span data-stu-id="18589-108">The **MDM\_Policy\_Result01\_Authentication02** class represents the authentication management policies available.</span></span>

<span data-ttu-id="18589-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="18589-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="18589-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18589-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Authentication02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAadPasswordReset;
  sint32 AllowFastReconnect;
  sint32 AllowFidoDeviceSignon;
  sint32 AllowSecondaryAuthenticationDevice;
};
```

## <a name="members"></a><span data-ttu-id="18589-111">Membres</span><span class="sxs-lookup"><span data-stu-id="18589-111">Members</span></span>

<span data-ttu-id="18589-112">La **classe \_ \_ Result01 \_ Authentication02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="18589-112">The **MDM\_Policy\_Result01\_Authentication02** class has these types of members:</span></span>

-   [<span data-ttu-id="18589-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="18589-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18589-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="18589-114">Properties</span></span>

<span data-ttu-id="18589-115">La **classe \_ \_ Result01 \_ Authentication02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="18589-115">The **MDM\_Policy\_Result01\_Authentication02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="18589-116">AllowAadPasswordReset</span><span class="sxs-lookup"><span data-stu-id="18589-116">AllowAadPasswordReset</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowaadpasswordreset)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18589-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="18589-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="18589-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="18589-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18589-119">AllowFastReconnect</span><span class="sxs-lookup"><span data-stu-id="18589-119">AllowFastReconnect</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfastreconnect)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18589-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="18589-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="18589-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="18589-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18589-122">AllowFidoDeviceSignon</span><span class="sxs-lookup"><span data-stu-id="18589-122">AllowFidoDeviceSignon</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfidodevicesignon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18589-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="18589-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="18589-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="18589-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18589-125">AllowSecondaryAuthenticationDevice</span><span class="sxs-lookup"><span data-stu-id="18589-125">AllowSecondaryAuthenticationDevice</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowsecondaryauthenticationdevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18589-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="18589-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="18589-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="18589-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18589-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="18589-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18589-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18589-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18589-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18589-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18589-131">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="18589-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="18589-132">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="18589-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="18589-133">Pour cette classe, la chaîne est « Authentication ».</span><span class="sxs-lookup"><span data-stu-id="18589-133">For this class, the string is "Authentication".</span></span>

</dd> <dt>

<span data-ttu-id="18589-134">**ID**</span><span class="sxs-lookup"><span data-stu-id="18589-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18589-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18589-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18589-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18589-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18589-137">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="18589-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="18589-138">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="18589-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="18589-139">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Result »</span><span class="sxs-lookup"><span data-stu-id="18589-139">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18589-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18589-140">Requirements</span></span>



| <span data-ttu-id="18589-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18589-141">Requirement</span></span> | <span data-ttu-id="18589-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="18589-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18589-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18589-143">Minimum supported client</span></span><br/> | <span data-ttu-id="18589-144">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18589-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="18589-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18589-145">Minimum supported server</span></span><br/> | <span data-ttu-id="18589-146">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="18589-146">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="18589-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="18589-147">Namespace</span></span><br/>                | <span data-ttu-id="18589-148">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="18589-148">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="18589-149">MOF</span><span class="sxs-lookup"><span data-stu-id="18589-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18589-150"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18589-150"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="18589-151">DLL</span><span class="sxs-lookup"><span data-stu-id="18589-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18589-152"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18589-152"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18589-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18589-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18589-154">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="18589-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

