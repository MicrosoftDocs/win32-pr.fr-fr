---
title: Classe MDM_Policy_Config01_Bluetooth02
description: La \_ classe Config01 Bluetooth02 de la stratégie MDM \_ \_ représente les stratégies de gestion Bluetooth disponibles.
ms.assetid: 8544c8df-a57b-4e21-87ee-f819aeddc071
keywords:
- Classe MDM_Policy_Config01_Bluetooth02
- Classe MDM_Policy_Config01_Bluetooth02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Bluetooth02
- MDM_Policy_Config01_Bluetooth02.InstanceID
- MDM_Policy_Config01_Bluetooth02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceeea1cd099fa00d6138a0ff1d37123725f0be2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103317"
---
# <a name="mdm_policy_config01_bluetooth02-class"></a><span data-ttu-id="ee10d-105">\_Classe Bluetooth02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="ee10d-105">MDM\_Policy\_Config01\_Bluetooth02 class</span></span>

<span data-ttu-id="ee10d-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="ee10d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ee10d-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="ee10d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ee10d-108">La **classe \_ \_ Config01 \_ Bluetooth02 de la stratégie MDM** représente les stratégies de gestion Bluetooth disponibles.</span><span class="sxs-lookup"><span data-stu-id="ee10d-108">The **MDM\_Policy\_Config01\_Bluetooth02** class represents the Bluetooth management policies available.</span></span>

<span data-ttu-id="ee10d-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ee10d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee10d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee10d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Bluetooth02
{
  string InstanceID;
  string ParentID;
  sint32 AllowDiscoverableMode;
  string LocalDeviceName;
  sint32 AllowAdvertising;
  string ServicesAllowedList;
  sint32 AllowPrepairing;
};
```

## <a name="members"></a><span data-ttu-id="ee10d-111">Membres</span><span class="sxs-lookup"><span data-stu-id="ee10d-111">Members</span></span>

<span data-ttu-id="ee10d-112">La **classe \_ \_ Config01 \_ Bluetooth02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ee10d-112">The **MDM\_Policy\_Config01\_Bluetooth02** class has these types of members:</span></span>

-   [<span data-ttu-id="ee10d-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ee10d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ee10d-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ee10d-114">Properties</span></span>

<span data-ttu-id="ee10d-115">La **classe \_ \_ Config01 \_ Bluetooth02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ee10d-115">The **MDM\_Policy\_Config01\_Bluetooth02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ee10d-116">AllowAdvertising</span><span class="sxs-lookup"><span data-stu-id="ee10d-116">AllowAdvertising</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowadvertising)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee10d-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="ee10d-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ee10d-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ee10d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ee10d-119">AllowDiscoverableMode</span><span class="sxs-lookup"><span data-stu-id="ee10d-119">AllowDiscoverableMode</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowdiscoverablemode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee10d-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="ee10d-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ee10d-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ee10d-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ee10d-122">AllowPrepairing</span><span class="sxs-lookup"><span data-stu-id="ee10d-122">AllowPrepairing</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowprepairing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee10d-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="ee10d-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ee10d-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ee10d-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ee10d-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ee10d-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee10d-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee10d-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee10d-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee10d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee10d-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ee10d-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ee10d-129">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="ee10d-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="ee10d-130">Pour cette classe, la chaîne est « Bluetooth ».</span><span class="sxs-lookup"><span data-stu-id="ee10d-130">For this class, the string is "Bluetooth".</span></span>

</dd> <dt>

[<span data-ttu-id="ee10d-131">LocalDeviceName</span><span class="sxs-lookup"><span data-stu-id="ee10d-131">LocalDeviceName</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-localdevicename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee10d-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee10d-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee10d-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ee10d-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ee10d-134">**ID**</span><span class="sxs-lookup"><span data-stu-id="ee10d-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee10d-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee10d-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee10d-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee10d-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee10d-137">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ee10d-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ee10d-138">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="ee10d-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="ee10d-139">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Config »</span><span class="sxs-lookup"><span data-stu-id="ee10d-139">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="ee10d-140">ServicesAllowedList</span><span class="sxs-lookup"><span data-stu-id="ee10d-140">ServicesAllowedList</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-servicesallowedlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee10d-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee10d-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee10d-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ee10d-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee10d-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee10d-143">Requirements</span></span>



| <span data-ttu-id="ee10d-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee10d-144">Requirement</span></span> | <span data-ttu-id="ee10d-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee10d-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee10d-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee10d-146">Minimum supported client</span></span><br/> | <span data-ttu-id="ee10d-147">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee10d-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ee10d-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee10d-148">Minimum supported server</span></span><br/> | <span data-ttu-id="ee10d-149">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee10d-149">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ee10d-150">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ee10d-150">Namespace</span></span><br/>                | <span data-ttu-id="ee10d-151">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="ee10d-151">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="ee10d-152">MOF</span><span class="sxs-lookup"><span data-stu-id="ee10d-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee10d-153"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee10d-153"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee10d-154">DLL</span><span class="sxs-lookup"><span data-stu-id="ee10d-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee10d-155"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee10d-155"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee10d-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee10d-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee10d-157">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="ee10d-157">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

