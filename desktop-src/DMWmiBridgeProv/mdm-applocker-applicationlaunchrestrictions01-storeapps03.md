---
title: Classe MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
description: La \_ \_ classe ApplicationLaunchRestrictions01 STOREAPPS03 de MDM AppLocker \_ vous permet de spécifier les applications exe autorisées ou non pour la protection des données d’entreprise.
ms.assetid: de5ceaea-589a-4ed7-8dd6-eb9477d68e0e
keywords:
- Classe MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
- Classe MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03, Description
topic_type:
- apiref
api_name:
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03.InstanceID
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54c58610c10e672a6fbc1406b2d022b8ce211871
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512800"
---
# <a name="mdm_applocker_applicationlaunchrestrictions01_storeapps03-class"></a><span data-ttu-id="8dc3f-105">\_ \_ Classe StoreApps03 APPLICATIONLAUNCHRESTRICTIONS01 de MDM AppLocker \_</span><span class="sxs-lookup"><span data-stu-id="8dc3f-105">MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03 class</span></span>

<span data-ttu-id="8dc3f-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="8dc3f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8dc3f-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="8dc3f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8dc3f-108">La **classe \_ \_ ApplicationLaunchRestrictions01 \_ StoreApps03 de MDM AppLocker** vous permet de spécifier les applications exe autorisées ou non pour la protection des données d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="8dc3f-108">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03** class allows you to specify which EXE applications are allowed or disallowed for Enterprise Data Protection.</span></span>

<span data-ttu-id="8dc3f-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8dc3f-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dc3f-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8dc3f-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
};
```

## <a name="members"></a><span data-ttu-id="8dc3f-111">Membres</span><span class="sxs-lookup"><span data-stu-id="8dc3f-111">Members</span></span>

<span data-ttu-id="8dc3f-112">La **classe \_ \_ ApplicationLaunchRestrictions01 \_ StoreApps03 de MDM AppLocker** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8dc3f-112">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03** class has these types of members:</span></span>

-   [<span data-ttu-id="8dc3f-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8dc3f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8dc3f-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8dc3f-114">Properties</span></span>

<span data-ttu-id="8dc3f-115">La **classe \_ \_ ApplicationLaunchRestrictions01 \_ StoreApps03 de MDM AppLocker** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="8dc3f-115">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="8dc3f-116">**EnforcementMode**</span><span class="sxs-lookup"><span data-stu-id="8dc3f-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dc3f-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8dc3f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dc3f-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8dc3f-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8dc3f-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8dc3f-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dc3f-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8dc3f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dc3f-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8dc3f-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dc3f-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8dc3f-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8dc3f-123">Définit des restrictions pour l’exécution d’applications à partir du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="8dc3f-123">Defines restrictions for running apps from the Windows Store.</span></span>

</dd> <dt>

<span data-ttu-id="8dc3f-124">**ID**</span><span class="sxs-lookup"><span data-stu-id="8dc3f-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dc3f-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8dc3f-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dc3f-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8dc3f-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dc3f-127">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8dc3f-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8dc3f-128">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="8dc3f-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="8dc3f-129">Pour cette classe, la chaîne est « ./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*regroupement*»</span><span class="sxs-lookup"><span data-stu-id="8dc3f-129">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="8dc3f-130">**Stratégie**</span><span class="sxs-lookup"><span data-stu-id="8dc3f-130">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dc3f-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8dc3f-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dc3f-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8dc3f-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8dc3f-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8dc3f-133">Requirements</span></span>



| <span data-ttu-id="8dc3f-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8dc3f-134">Requirement</span></span> | <span data-ttu-id="8dc3f-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="8dc3f-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dc3f-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8dc3f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8dc3f-137">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8dc3f-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8dc3f-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8dc3f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8dc3f-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8dc3f-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8dc3f-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8dc3f-140">Namespace</span></span><br/>                | <span data-ttu-id="8dc3f-141">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="8dc3f-141">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="8dc3f-142">MOF</span><span class="sxs-lookup"><span data-stu-id="8dc3f-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8dc3f-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8dc3f-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8dc3f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="8dc3f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8dc3f-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8dc3f-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8dc3f-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8dc3f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dc3f-147">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="8dc3f-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

