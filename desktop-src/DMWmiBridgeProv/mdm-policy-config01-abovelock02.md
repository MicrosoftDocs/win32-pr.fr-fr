---
title: Classe MDM_Policy_Config01_AboveLock02
description: La \_ classe AboveLock02 de la stratégie MDM \_ Config01 représente des \_ stratégies qui déterminent les actions autorisées au-dessus de l’écran de verrouillage de l’appareil.
ms.assetid: ad76e424-e5b6-46ba-a6a7-5dc00f983918
keywords:
- Classe MDM_Policy_Config01_AboveLock02
- Classe MDM_Policy_Config01_AboveLock02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_AboveLock02
- MDM_Policy_Config01_AboveLock02.InstanceID
- MDM_Policy_Config01_AboveLock02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703971a10fe927c391831a9db65d270291b56e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510953"
---
# <a name="mdm_policy_config01_abovelock02-class"></a><span data-ttu-id="7ca84-105">\_Classe AboveLock02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="7ca84-105">MDM\_Policy\_Config01\_AboveLock02 class</span></span>

<span data-ttu-id="7ca84-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="7ca84-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7ca84-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="7ca84-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7ca84-108">La classe AboveLock02 de la **\_ stratégie MDM \_ Config01 \_** représente des stratégies qui déterminent les actions autorisées au-dessus de l’écran de verrouillage de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7ca84-108">The **MDM\_Policy\_Config01\_AboveLock02** class represents policies that determine actions that are allowed above the Device Lock screen.</span></span>

<span data-ttu-id="7ca84-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7ca84-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ca84-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ca84-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_AboveLock02
{
  string InstanceID;
  string ParentID;
  sint32 AllowToasts;
  sint32 AllowCortanaAboveLock;
};
```

## <a name="members"></a><span data-ttu-id="7ca84-111">Membres</span><span class="sxs-lookup"><span data-stu-id="7ca84-111">Members</span></span>

<span data-ttu-id="7ca84-112">La **classe \_ \_ Config01 \_ AboveLock02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7ca84-112">The **MDM\_Policy\_Config01\_AboveLock02** class has these types of members:</span></span>

-   [<span data-ttu-id="7ca84-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7ca84-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ca84-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7ca84-114">Properties</span></span>

<span data-ttu-id="7ca84-115">La **classe \_ \_ Config01 \_ AboveLock02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="7ca84-115">The **MDM\_Policy\_Config01\_AboveLock02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7ca84-116">AllowCortanaAboveLock</span><span class="sxs-lookup"><span data-stu-id="7ca84-116">AllowCortanaAboveLock</span></span>](/windows/client-management/mdm/policy-csp-abovelock#abovelock-allowcortanaabovelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca84-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="7ca84-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ca84-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7ca84-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7ca84-119">AllowToasts</span><span class="sxs-lookup"><span data-stu-id="7ca84-119">AllowToasts</span></span>](/windows/client-management/mdm/policy-csp-abovelock#abovelock-allowtoasts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca84-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="7ca84-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ca84-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7ca84-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7ca84-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7ca84-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca84-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7ca84-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ca84-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7ca84-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ca84-125">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7ca84-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7ca84-126">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="7ca84-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="7ca84-127">Pour cette classe, la chaîne est « AboveLock ».</span><span class="sxs-lookup"><span data-stu-id="7ca84-127">For this class, the string is "AboveLock".</span></span>

</dd> <dt>

<span data-ttu-id="7ca84-128">**ID**</span><span class="sxs-lookup"><span data-stu-id="7ca84-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca84-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7ca84-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ca84-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7ca84-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ca84-131">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7ca84-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7ca84-132">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="7ca84-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="7ca84-133">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Config »</span><span class="sxs-lookup"><span data-stu-id="7ca84-133">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7ca84-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ca84-134">Requirements</span></span>



| <span data-ttu-id="7ca84-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ca84-135">Requirement</span></span> | <span data-ttu-id="7ca84-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ca84-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ca84-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ca84-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7ca84-138">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ca84-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7ca84-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ca84-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7ca84-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ca84-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7ca84-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7ca84-141">Namespace</span></span><br/>                | <span data-ttu-id="7ca84-142">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="7ca84-142">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="7ca84-143">MOF</span><span class="sxs-lookup"><span data-stu-id="7ca84-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ca84-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7ca84-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ca84-145">DLL</span><span class="sxs-lookup"><span data-stu-id="7ca84-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ca84-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ca84-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ca84-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ca84-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ca84-148">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="7ca84-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

