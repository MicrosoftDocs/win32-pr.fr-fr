---
title: Classe MDM_Policy_Config01_Authentication02
description: La \_ classe Config01 Authentication02 de la stratégie MDM \_ \_ représente les stratégies de gestion des authentifications disponibles.
ms.assetid: 928e0b60-5533-45dc-90e6-be7d70210138
keywords:
- Classe MDM_Policy_Config01_Authentication02
- Classe MDM_Policy_Config01_Authentication02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Authentication02
- MDM_Policy_Config01_Authentication02.InstanceID
- MDM_Policy_Config01_Authentication02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfab66a548f4a92c445f748aca1bb15758ac48c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512565"
---
# <a name="mdm_policy_config01_authentication02-class"></a><span data-ttu-id="b7fcd-105">\_Classe Authentication02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="b7fcd-105">MDM\_Policy\_Config01\_Authentication02 class</span></span>

<span data-ttu-id="b7fcd-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="b7fcd-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b7fcd-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="b7fcd-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b7fcd-108">La **classe \_ \_ Config01 \_ Authentication02 de la stratégie MDM** représente les stratégies de gestion des authentifications disponibles.</span><span class="sxs-lookup"><span data-stu-id="b7fcd-108">The **MDM\_Policy\_Config01\_Authentication02** class represents the authentication management policies available.</span></span>

<span data-ttu-id="b7fcd-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b7fcd-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7fcd-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7fcd-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Authentication02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAadPasswordReset;
  sint32 AllowFastReconnect;
  sint32 AllowFidoDeviceSignon;
  sint32 AllowSecondaryAuthenticationDevice;
};
```

## <a name="members"></a><span data-ttu-id="b7fcd-111">Membres</span><span class="sxs-lookup"><span data-stu-id="b7fcd-111">Members</span></span>

<span data-ttu-id="b7fcd-112">La **classe \_ \_ Config01 \_ Authentication02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b7fcd-112">The **MDM\_Policy\_Config01\_Authentication02** class has these types of members:</span></span>

-   [<span data-ttu-id="b7fcd-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b7fcd-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b7fcd-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b7fcd-114">Properties</span></span>

<span data-ttu-id="b7fcd-115">La **classe \_ \_ Config01 \_ Authentication02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b7fcd-115">The **MDM\_Policy\_Config01\_Authentication02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b7fcd-116">AllowAadPasswordReset</span><span class="sxs-lookup"><span data-stu-id="b7fcd-116">AllowAadPasswordReset</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowaadpasswordreset)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7fcd-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b7fcd-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7fcd-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b7fcd-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b7fcd-119">AllowFastReconnect</span><span class="sxs-lookup"><span data-stu-id="b7fcd-119">AllowFastReconnect</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfastreconnect)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7fcd-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b7fcd-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7fcd-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b7fcd-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b7fcd-122">AllowFidoDeviceSignon</span><span class="sxs-lookup"><span data-stu-id="b7fcd-122">AllowFidoDeviceSignon</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfidodevicesignon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7fcd-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b7fcd-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7fcd-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b7fcd-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b7fcd-125">AllowSecondaryAuthenticationDevice</span><span class="sxs-lookup"><span data-stu-id="b7fcd-125">AllowSecondaryAuthenticationDevice</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowsecondaryauthenticationdevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7fcd-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b7fcd-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7fcd-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b7fcd-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b7fcd-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b7fcd-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7fcd-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b7fcd-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7fcd-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b7fcd-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7fcd-131">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b7fcd-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b7fcd-132">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="b7fcd-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="b7fcd-133">Pour cette classe, la chaîne est « Authentication ».</span><span class="sxs-lookup"><span data-stu-id="b7fcd-133">For this class, the string is "Authentication".</span></span>

</dd> <dt>

<span data-ttu-id="b7fcd-134">**ID**</span><span class="sxs-lookup"><span data-stu-id="b7fcd-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7fcd-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b7fcd-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7fcd-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b7fcd-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7fcd-137">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b7fcd-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b7fcd-138">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="b7fcd-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="b7fcd-139">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Config »</span><span class="sxs-lookup"><span data-stu-id="b7fcd-139">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7fcd-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7fcd-140">Requirements</span></span>



| <span data-ttu-id="b7fcd-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7fcd-141">Requirement</span></span> | <span data-ttu-id="b7fcd-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7fcd-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7fcd-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7fcd-143">Minimum supported client</span></span><br/> | <span data-ttu-id="b7fcd-144">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7fcd-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b7fcd-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7fcd-145">Minimum supported server</span></span><br/> | <span data-ttu-id="b7fcd-146">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7fcd-146">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b7fcd-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b7fcd-147">Namespace</span></span><br/>                | <span data-ttu-id="b7fcd-148">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="b7fcd-148">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="b7fcd-149">MOF</span><span class="sxs-lookup"><span data-stu-id="b7fcd-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7fcd-150"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7fcd-150"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7fcd-151">DLL</span><span class="sxs-lookup"><span data-stu-id="b7fcd-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7fcd-152"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7fcd-152"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7fcd-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7fcd-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7fcd-154">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="b7fcd-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

