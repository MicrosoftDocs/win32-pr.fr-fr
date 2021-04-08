---
title: Classe MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
description: La \_ \_ classe ApplicationLaunchRestrictions01 EXE03 de MDM AppLocker \_ vous permet de spécifier les applications exe autorisées à lancer.
ms.assetid: 27f10b5c-bc3b-4344-afcf-5718ea13e909
keywords:
- Classe MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
- Classe MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03, Description
topic_type:
- apiref
api_name:
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03.InstanceID
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58aeb86edc21fec974c099fd8d25bd2e3fb244ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843421"
---
# <a name="mdm_applocker_applicationlaunchrestrictions01_exe03-class"></a><span data-ttu-id="9d106-105">\_ \_ Classe EXE03 APPLICATIONLAUNCHRESTRICTIONS01 de MDM AppLocker \_</span><span class="sxs-lookup"><span data-stu-id="9d106-105">MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03 class</span></span>

<span data-ttu-id="9d106-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="9d106-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9d106-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="9d106-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9d106-108">La **classe \_ \_ ApplicationLaunchRestrictions01 \_ EXE03 de MDM AppLocker** vous permet de spécifier les applications exe autorisées à lancer.</span><span class="sxs-lookup"><span data-stu-id="9d106-108">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03** class allows you to specify which EXE applications are allowed to launch.</span></span>

<span data-ttu-id="9d106-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9d106-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d106-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d106-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
  string NonInteractiveProcessEnforcement;
};
```

## <a name="members"></a><span data-ttu-id="9d106-111">Membres</span><span class="sxs-lookup"><span data-stu-id="9d106-111">Members</span></span>

<span data-ttu-id="9d106-112">La **classe \_ \_ ApplicationLaunchRestrictions01 \_ EXE03 de MDM AppLocker** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9d106-112">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03** class has these types of members:</span></span>

-   [<span data-ttu-id="9d106-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9d106-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9d106-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9d106-114">Properties</span></span>

<span data-ttu-id="9d106-115">La **classe \_ \_ ApplicationLaunchRestrictions01 \_ EXE03 de MDM AppLocker** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="9d106-115">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9d106-116">**EnforcementMode**</span><span class="sxs-lookup"><span data-stu-id="9d106-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d106-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9d106-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d106-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9d106-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9d106-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9d106-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d106-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9d106-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d106-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d106-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d106-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9d106-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9d106-123">Définit des restrictions pour le lancement d’applications exécutables.</span><span class="sxs-lookup"><span data-stu-id="9d106-123">Defines restrictions for launching executable applications.</span></span>

</dd> <dt>

[<span data-ttu-id="9d106-124">**NonInteractiveProcessEnforcement**</span><span class="sxs-lookup"><span data-stu-id="9d106-124">**NonInteractiveProcessEnforcement**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d106-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9d106-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d106-126">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9d106-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9d106-127">**ID**</span><span class="sxs-lookup"><span data-stu-id="9d106-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d106-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9d106-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d106-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d106-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d106-130">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9d106-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9d106-131">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="9d106-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="9d106-132">Pour cette classe, la chaîne est « ./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*regroupement*»</span><span class="sxs-lookup"><span data-stu-id="9d106-132">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="9d106-133">**Stratégie**</span><span class="sxs-lookup"><span data-stu-id="9d106-133">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d106-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9d106-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d106-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9d106-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d106-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d106-136">Requirements</span></span>



| <span data-ttu-id="9d106-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d106-137">Requirement</span></span> | <span data-ttu-id="9d106-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d106-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d106-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d106-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9d106-140">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d106-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9d106-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d106-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9d106-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d106-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9d106-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9d106-143">Namespace</span></span><br/>                | <span data-ttu-id="9d106-144">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="9d106-144">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="9d106-145">MOF</span><span class="sxs-lookup"><span data-stu-id="9d106-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d106-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d106-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d106-147">DLL</span><span class="sxs-lookup"><span data-stu-id="9d106-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d106-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d106-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d106-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d106-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d106-150">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="9d106-150">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

