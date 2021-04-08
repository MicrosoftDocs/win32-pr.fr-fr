---
title: Classe MDM_Policy_Config01_Camera02
description: La \_ classe Config01 Camera02 de la stratégie MDM \_ \_ représente les stratégies d’appareil photo disponibles.
ms.assetid: dd17c2bc-8c96-4f5e-a4d2-cf1d27a92eb7
keywords:
- Classe MDM_Policy_Config01_Camera02
- Classe MDM_Policy_Config01_Camera02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Camera02
- MDM_Policy_Config01_Camera02.InstanceID
- MDM_Policy_Config01_Camera02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 377a9eb695560d7bf93fd6a5d761b1e95202bf20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740972"
---
# <a name="mdm_policy_config01_camera02-class"></a><span data-ttu-id="80e4a-105">\_Classe Camera02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="80e4a-105">MDM\_Policy\_Config01\_Camera02 class</span></span>

<span data-ttu-id="80e4a-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="80e4a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="80e4a-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="80e4a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="80e4a-108">La **classe \_ \_ Config01 \_ Camera02 de la stratégie MDM** représente les stratégies d’appareil photo disponibles.</span><span class="sxs-lookup"><span data-stu-id="80e4a-108">The **MDM\_Policy\_Config01\_Camera02** class represents the camera policies available.</span></span>

<span data-ttu-id="80e4a-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="80e4a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="80e4a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80e4a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Camera02
{
  string InstanceID;
  string ParentID;
  sint32 AllowCamera;
};
```

## <a name="members"></a><span data-ttu-id="80e4a-111">Membres</span><span class="sxs-lookup"><span data-stu-id="80e4a-111">Members</span></span>

<span data-ttu-id="80e4a-112">La **classe \_ \_ Config01 \_ Camera02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="80e4a-112">The **MDM\_Policy\_Config01\_Camera02** class has these types of members:</span></span>

-   [<span data-ttu-id="80e4a-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="80e4a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80e4a-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="80e4a-114">Properties</span></span>

<span data-ttu-id="80e4a-115">La **classe \_ \_ Config01 \_ Camera02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="80e4a-115">The **MDM\_Policy\_Config01\_Camera02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="80e4a-116">AllowCamera</span><span class="sxs-lookup"><span data-stu-id="80e4a-116">AllowCamera</span></span>](/windows/client-management/mdm/policy-csp-camera#camera-allowcamera)
</dt> <dd> <dl> <dt>

<span data-ttu-id="80e4a-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="80e4a-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="80e4a-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80e4a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="80e4a-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="80e4a-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80e4a-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80e4a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80e4a-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80e4a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80e4a-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="80e4a-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="80e4a-123">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="80e4a-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="80e4a-124">Pour cette classe, la chaîne est « Camera ».</span><span class="sxs-lookup"><span data-stu-id="80e4a-124">For this class, the string is "Camera".</span></span>

</dd> <dt>

<span data-ttu-id="80e4a-125">**ID**</span><span class="sxs-lookup"><span data-stu-id="80e4a-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80e4a-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80e4a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80e4a-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80e4a-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80e4a-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="80e4a-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="80e4a-129">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="80e4a-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="80e4a-130">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Config »</span><span class="sxs-lookup"><span data-stu-id="80e4a-130">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80e4a-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80e4a-131">Requirements</span></span>



| <span data-ttu-id="80e4a-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80e4a-132">Requirement</span></span> | <span data-ttu-id="80e4a-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="80e4a-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80e4a-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80e4a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="80e4a-135">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80e4a-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="80e4a-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80e4a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="80e4a-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="80e4a-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="80e4a-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="80e4a-138">Namespace</span></span><br/>                | <span data-ttu-id="80e4a-139">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="80e4a-139">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="80e4a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="80e4a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80e4a-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80e4a-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="80e4a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="80e4a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80e4a-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80e4a-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80e4a-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80e4a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80e4a-145">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="80e4a-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

