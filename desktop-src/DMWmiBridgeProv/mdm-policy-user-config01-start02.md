---
title: Classe MDM_Policy_User_Config01_Start02
description: La \_ \_ classe Config01 Start02 utilisateur de la stratégie MDM \_ \_ représente les stratégies de démarrage disponibles pour chaque utilisateur.
ms.assetid: bbb64553-4d93-433d-96e4-bfd3f5588138
keywords:
- Classe MDM_Policy_User_Config01_Start02
- Classe MDM_Policy_User_Config01_Start02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Start02
- MDM_Policy_User_Config01_Start02.InstanceID
- MDM_Policy_User_Config01_Start02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b98b25ee0c3118f741d3a52bc9001c6106d86f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384723"
---
# <a name="mdm_policy_user_config01_start02-class"></a><span data-ttu-id="fb8f3-105">Classe d’utilisateur de la \_ stratégie MDM \_ \_ Config01 \_ Start02</span><span class="sxs-lookup"><span data-stu-id="fb8f3-105">MDM\_Policy\_User\_Config01\_Start02 class</span></span>

<span data-ttu-id="fb8f3-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="fb8f3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fb8f3-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="fb8f3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fb8f3-108">La **classe \_ \_ \_ Config01 \_ Start02 utilisateur de la stratégie MDM** représente les stratégies de démarrage disponibles pour chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fb8f3-108">The **MDM\_Policy\_User\_Config01\_Start02** class represents the start policies available that are set on a per-user basis.</span></span>

<span data-ttu-id="fb8f3-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fb8f3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb8f3-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb8f3-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Start02
{
  string InstanceID;
  string ParentID;
  sint32 HidePeopleBar;
  string StartLayout;
};
```

## <a name="members"></a><span data-ttu-id="fb8f3-111">Membres</span><span class="sxs-lookup"><span data-stu-id="fb8f3-111">Members</span></span>

<span data-ttu-id="fb8f3-112">La **classe \_ \_ \_ Config01 \_ Start02 de la stratégie MDM User** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fb8f3-112">The **MDM\_Policy\_User\_Config01\_Start02** class has these types of members:</span></span>

-   [<span data-ttu-id="fb8f3-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fb8f3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fb8f3-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fb8f3-114">Properties</span></span>

<span data-ttu-id="fb8f3-115">La **classe \_ \_ \_ Config01 \_ Start02 de la stratégie MDM User** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fb8f3-115">The **MDM\_Policy\_User\_Config01\_Start02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fb8f3-116">HidePeopleBar</span><span class="sxs-lookup"><span data-stu-id="fb8f3-116">HidePeopleBar</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidepeoplebar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb8f3-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fb8f3-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fb8f3-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fb8f3-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fb8f3-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fb8f3-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb8f3-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fb8f3-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb8f3-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb8f3-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb8f3-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fb8f3-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fb8f3-123">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="fb8f3-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="fb8f3-124">Pour cette classe, la chaîne est « start ».</span><span class="sxs-lookup"><span data-stu-id="fb8f3-124">For this class, the string is "Start"</span></span>

</dd> <dt>

<span data-ttu-id="fb8f3-125">**ID**</span><span class="sxs-lookup"><span data-stu-id="fb8f3-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb8f3-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fb8f3-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb8f3-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb8f3-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb8f3-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fb8f3-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fb8f3-129">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="fb8f3-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="fb8f3-130">Pour cette classe, la chaîne est « ./User/Vendor/MSFT/Policy/Config »</span><span class="sxs-lookup"><span data-stu-id="fb8f3-130">For this class, the string is "./User/Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="fb8f3-131">StartLayout</span><span class="sxs-lookup"><span data-stu-id="fb8f3-131">StartLayout</span></span>](/windows/client-management/mdm/policy-csp-start#start-startlayout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb8f3-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fb8f3-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb8f3-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fb8f3-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fb8f3-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb8f3-134">Requirements</span></span>



| <span data-ttu-id="fb8f3-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb8f3-135">Requirement</span></span> | <span data-ttu-id="fb8f3-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb8f3-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb8f3-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb8f3-137">Minimum supported client</span></span><br/> | <span data-ttu-id="fb8f3-138">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb8f3-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fb8f3-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb8f3-139">Minimum supported server</span></span><br/> | <span data-ttu-id="fb8f3-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb8f3-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="fb8f3-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fb8f3-141">Namespace</span></span><br/>                | <span data-ttu-id="fb8f3-142">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="fb8f3-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="fb8f3-143">MOF</span><span class="sxs-lookup"><span data-stu-id="fb8f3-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb8f3-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb8f3-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb8f3-145">DLL</span><span class="sxs-lookup"><span data-stu-id="fb8f3-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb8f3-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb8f3-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb8f3-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb8f3-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb8f3-148">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="fb8f3-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

