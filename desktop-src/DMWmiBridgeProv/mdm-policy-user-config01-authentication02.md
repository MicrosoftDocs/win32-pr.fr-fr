---
title: Classe MDM_Policy_User_Config01_Authentication02
description: La \_ \_ classe Config01 Authentication02 utilisateur de la stratégie MDM \_ \_ représente les stratégies de gestion des authentifications disponibles.
ms.assetid: 66d94f97-07ea-4025-95f9-d55282df3661
keywords:
- Classe MDM_Policy_User_Config01_Authentication02
- Classe MDM_Policy_User_Config01_Authentication02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Authentication02
- MDM_Policy_User_Config01_Authentication02.InstanceID
- MDM_Policy_User_Config01_Authentication02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10d278ad679f97047d0a4cf7e95eeb2eee0695e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942521"
---
# <a name="mdm_policy_user_config01_authentication02-class"></a><span data-ttu-id="046b1-105">Classe d’utilisateur de la \_ stratégie MDM \_ \_ Config01 \_ Authentication02</span><span class="sxs-lookup"><span data-stu-id="046b1-105">MDM\_Policy\_User\_Config01\_Authentication02 class</span></span>

<span data-ttu-id="046b1-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="046b1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="046b1-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="046b1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="046b1-108">La **classe \_ \_ \_ Config01 \_ Authentication02 utilisateur de la stratégie MDM** représente les stratégies de gestion des authentifications disponibles.</span><span class="sxs-lookup"><span data-stu-id="046b1-108">The **MDM\_Policy\_User\_Config01\_Authentication02** class represents the authentication management policies available.</span></span>

<span data-ttu-id="046b1-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="046b1-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="046b1-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="046b1-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Authentication02
{
  string InstanceID;
  string ParentID;
  sint32 AllowEAPCertSSO;
};
```

## <a name="members"></a><span data-ttu-id="046b1-111">Membres</span><span class="sxs-lookup"><span data-stu-id="046b1-111">Members</span></span>

<span data-ttu-id="046b1-112">La **classe \_ \_ \_ Config01 \_ Authentication02 de la stratégie MDM User** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="046b1-112">The **MDM\_Policy\_User\_Config01\_Authentication02** class has these types of members:</span></span>

-   [<span data-ttu-id="046b1-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="046b1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="046b1-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="046b1-114">Properties</span></span>

<span data-ttu-id="046b1-115">La **classe \_ \_ \_ Config01 \_ Authentication02 de la stratégie MDM User** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="046b1-115">The **MDM\_Policy\_User\_Config01\_Authentication02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="046b1-116">AllowEAPCertSSO</span><span class="sxs-lookup"><span data-stu-id="046b1-116">AllowEAPCertSSO</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-alloweapcertsso)
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b1-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="046b1-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="046b1-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="046b1-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="046b1-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="046b1-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b1-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="046b1-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b1-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="046b1-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b1-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="046b1-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="046b1-123">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="046b1-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="046b1-124">Pour cette classe, la chaîne est « Authentication ».</span><span class="sxs-lookup"><span data-stu-id="046b1-124">For this class, the string is "Authentication".</span></span>

</dd> <dt>

<span data-ttu-id="046b1-125">**ID**</span><span class="sxs-lookup"><span data-stu-id="046b1-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b1-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="046b1-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b1-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="046b1-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b1-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="046b1-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="046b1-129">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="046b1-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="046b1-130">Pour cette classe, la chaîne est « ./User/Vendor/MSFT/Policy/Config »</span><span class="sxs-lookup"><span data-stu-id="046b1-130">For this class, the string is "./User/Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="046b1-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="046b1-131">Requirements</span></span>



| <span data-ttu-id="046b1-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="046b1-132">Requirement</span></span> | <span data-ttu-id="046b1-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="046b1-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="046b1-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="046b1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="046b1-135">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="046b1-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="046b1-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="046b1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="046b1-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="046b1-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="046b1-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="046b1-138">Namespace</span></span><br/>                | <span data-ttu-id="046b1-139">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="046b1-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="046b1-140">MOF</span><span class="sxs-lookup"><span data-stu-id="046b1-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="046b1-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="046b1-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="046b1-142">DLL</span><span class="sxs-lookup"><span data-stu-id="046b1-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="046b1-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="046b1-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="046b1-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="046b1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="046b1-145">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="046b1-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

