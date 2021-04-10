---
title: Classe MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
description: La \_ \_ \_ classe ENTERPRISEDATAPROTECTION01 StoreApps03 de MDM AppLocker capture la liste des applications Windows autorisées à gérer les données d’entreprise. Doit être utilisé conjointement avec les paramètres de./Vendor/MSFT/Policy/ConfigSource/DataProtection.
ms.assetid: f37fe52d-dbe1-45b7-acd5-5047c46d9bd0
keywords:
- Classe MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
- Classe MDM_AppLocker_EnterpriseDataProtection01_StoreApps03, Description
topic_type:
- apiref
api_name:
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03.InstanceID
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 240f641e542bbbe0c71fd686e2d9df3908b9bab3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942805"
---
# <a name="mdm_applocker_enterprisedataprotection01_storeapps03-class"></a><span data-ttu-id="32c24-106">\_ \_ Classe StoreApps03 ENTERPRISEDATAPROTECTION01 de MDM AppLocker \_</span><span class="sxs-lookup"><span data-stu-id="32c24-106">MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03 class</span></span>

<span data-ttu-id="32c24-107">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="32c24-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="32c24-108">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="32c24-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="32c24-109">La **classe \_ \_ EnterpriseDataProtection01 \_ StoreApps03 de MDM AppLocker** capture la liste des applications Windows autorisées à gérer les données d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="32c24-109">The **MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03** class captures the list of Windows apps that are allowed to handle enterprise data.</span></span> <span data-ttu-id="32c24-110">Doit être utilisé conjointement avec les paramètres de./Vendor/MSFT/Policy/ConfigSource/DataProtection.</span><span class="sxs-lookup"><span data-stu-id="32c24-110">Should be used in conjunction with the settings in ./Vendor/MSFT/Policy/ConfigSource/DataProtection .</span></span>

<span data-ttu-id="32c24-111">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="32c24-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="32c24-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32c24-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a><span data-ttu-id="32c24-113">Membres</span><span class="sxs-lookup"><span data-stu-id="32c24-113">Members</span></span>

<span data-ttu-id="32c24-114">La **classe \_ \_ EnterpriseDataProtection01 \_ StoreApps03 de MDM AppLocker** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="32c24-114">The **MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03** class has these types of members:</span></span>

-   [<span data-ttu-id="32c24-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="32c24-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32c24-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="32c24-116">Properties</span></span>

<span data-ttu-id="32c24-117">La **classe \_ \_ EnterpriseDataProtection01 \_ StoreApps03 de MDM AppLocker** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="32c24-117">The **MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="32c24-118">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="32c24-118">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32c24-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="32c24-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32c24-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32c24-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32c24-121">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="32c24-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="32c24-122">Définit des restrictions pour l’exécution d’applications à partir du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="32c24-122">Defines restrictions for running apps from the Windows Store.</span></span>

</dd> <dt>

<span data-ttu-id="32c24-123">**ID**</span><span class="sxs-lookup"><span data-stu-id="32c24-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32c24-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="32c24-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32c24-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32c24-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32c24-126">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="32c24-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="32c24-127">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="32c24-127">Describes the full path to the parent node.</span></span> <span data-ttu-id="32c24-128">Pour cette classe, la chaîne est « ./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*regroupement*»</span><span class="sxs-lookup"><span data-stu-id="32c24-128">For this class, the string is "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="32c24-129">**Stratégie**</span><span class="sxs-lookup"><span data-stu-id="32c24-129">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32c24-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="32c24-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32c24-131">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="32c24-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32c24-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32c24-132">Requirements</span></span>



| <span data-ttu-id="32c24-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32c24-133">Requirement</span></span> | <span data-ttu-id="32c24-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="32c24-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32c24-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32c24-135">Minimum supported client</span></span><br/> | <span data-ttu-id="32c24-136">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="32c24-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="32c24-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32c24-137">Minimum supported server</span></span><br/> | <span data-ttu-id="32c24-138">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="32c24-138">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="32c24-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="32c24-139">Namespace</span></span><br/>                | <span data-ttu-id="32c24-140">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="32c24-140">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="32c24-141">MOF</span><span class="sxs-lookup"><span data-stu-id="32c24-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32c24-142"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32c24-142"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="32c24-143">DLL</span><span class="sxs-lookup"><span data-stu-id="32c24-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32c24-144"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32c24-144"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32c24-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32c24-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32c24-146">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="32c24-146">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

