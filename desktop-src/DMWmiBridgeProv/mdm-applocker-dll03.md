---
title: Classe MDM_AppLocker_DLL03
description: La \_ \_ classe DLL03 de MDM AppLocker définit les restrictions de stratégie pour le traitement des fichiers dll.
ms.assetid: 956b2ec0-f8a8-41d1-a571-01e73c4cebf9
keywords:
- Classe MDM_AppLocker_DLL03
- Classe MDM_AppLocker_DLL03, Description
topic_type:
- apiref
api_name:
- MDM_AppLocker_DLL03
- MDM_AppLocker_DLL03.InstanceID
- MDM_AppLocker_DLL03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c332a7d606b21ed9641c3c25f10a011cf7bea6e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512609"
---
# <a name="mdm_applocker_dll03-class"></a><span data-ttu-id="77ce1-105">\_ \_ Classe DLL03 de MDM AppLocker</span><span class="sxs-lookup"><span data-stu-id="77ce1-105">MDM\_AppLocker\_DLL03 class</span></span>

<span data-ttu-id="77ce1-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="77ce1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="77ce1-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="77ce1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="77ce1-108">La **classe \_ \_ DLL03 de MDM AppLocker** définit les restrictions de stratégie pour le traitement des fichiers dll.</span><span class="sxs-lookup"><span data-stu-id="77ce1-108">The **MDM\_AppLocker\_DLL03** class defines the policy restrictions for processing DLL files.</span></span>

<span data-ttu-id="77ce1-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="77ce1-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="77ce1-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77ce1-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_DLL03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
  string NonInteractiveProcessEnforcement;
};
```

## <a name="members"></a><span data-ttu-id="77ce1-111">Membres</span><span class="sxs-lookup"><span data-stu-id="77ce1-111">Members</span></span>

<span data-ttu-id="77ce1-112">La **classe \_ \_ DLL03 de MDM AppLocker** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="77ce1-112">The **MDM\_AppLocker\_DLL03** class has these types of members:</span></span>

-   [<span data-ttu-id="77ce1-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="77ce1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="77ce1-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="77ce1-114">Properties</span></span>

<span data-ttu-id="77ce1-115">La **classe \_ \_ DLL03 de MDM AppLocker** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="77ce1-115">The **MDM\_AppLocker\_DLL03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="77ce1-116">**EnforcementMode**</span><span class="sxs-lookup"><span data-stu-id="77ce1-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ce1-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="77ce1-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77ce1-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="77ce1-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="77ce1-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="77ce1-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ce1-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="77ce1-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77ce1-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="77ce1-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77ce1-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="77ce1-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="77ce1-123">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="77ce1-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="77ce1-124">**NonInteractiveProcessEnforcement**</span><span class="sxs-lookup"><span data-stu-id="77ce1-124">**NonInteractiveProcessEnforcement**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ce1-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="77ce1-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77ce1-126">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="77ce1-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="77ce1-127">**ID**</span><span class="sxs-lookup"><span data-stu-id="77ce1-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ce1-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="77ce1-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77ce1-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="77ce1-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77ce1-130">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="77ce1-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="77ce1-131">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="77ce1-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="77ce1-132">Pour cette classe, la chaîne est « ./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions »</span><span class="sxs-lookup"><span data-stu-id="77ce1-132">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span></span>

</dd> <dt>

[<span data-ttu-id="77ce1-133">**Stratégie**</span><span class="sxs-lookup"><span data-stu-id="77ce1-133">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="77ce1-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="77ce1-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77ce1-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="77ce1-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="77ce1-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77ce1-136">Requirements</span></span>



| <span data-ttu-id="77ce1-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77ce1-137">Requirement</span></span> | <span data-ttu-id="77ce1-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="77ce1-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77ce1-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77ce1-139">Minimum supported client</span></span><br/> | <span data-ttu-id="77ce1-140">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77ce1-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="77ce1-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77ce1-141">Minimum supported server</span></span><br/> | <span data-ttu-id="77ce1-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="77ce1-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="77ce1-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="77ce1-143">Namespace</span></span><br/>                | <span data-ttu-id="77ce1-144">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="77ce1-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="77ce1-145">MOF</span><span class="sxs-lookup"><span data-stu-id="77ce1-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77ce1-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="77ce1-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="77ce1-147">DLL</span><span class="sxs-lookup"><span data-stu-id="77ce1-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77ce1-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77ce1-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77ce1-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77ce1-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77ce1-150">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="77ce1-150">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

