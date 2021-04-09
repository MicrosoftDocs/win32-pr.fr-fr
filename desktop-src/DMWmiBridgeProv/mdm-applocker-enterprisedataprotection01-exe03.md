---
title: Classe MDM_AppLocker_EnterpriseDataProtection01_EXE03
description: La \_ \_ \_ classe ENTERPRISEDATAPROTECTION01 EXE03 de MDM AppLocker capture la liste des applications exécutables qui sont autorisées à gérer les données d’entreprise.
ms.assetid: 43f253d4-3f9d-4651-91b4-b7460706e8b4
keywords:
- Classe MDM_AppLocker_EnterpriseDataProtection01_EXE03
- Classe MDM_AppLocker_EnterpriseDataProtection01_EXE03, Description
topic_type:
- apiref
api_name:
- MDM_AppLocker_EnterpriseDataProtection01_EXE03
- MDM_AppLocker_EnterpriseDataProtection01_EXE03.InstanceID
- MDM_AppLocker_EnterpriseDataProtection01_EXE03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b6cbaba46034c26524ca7e12aaa93b588708f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106150"
---
# <a name="mdm_applocker_enterprisedataprotection01_exe03-class"></a><span data-ttu-id="c3e3c-105">\_ \_ Classe EXE03 ENTERPRISEDATAPROTECTION01 de MDM AppLocker \_</span><span class="sxs-lookup"><span data-stu-id="c3e3c-105">MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03 class</span></span>

<span data-ttu-id="c3e3c-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="c3e3c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c3e3c-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="c3e3c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c3e3c-108">La **classe \_ \_ EnterpriseDataProtection01 \_ EXE03 de MDM AppLocker** capture la liste des applications exécutables qui sont autorisées à gérer les données d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="c3e3c-108">The **MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03** class captures the list of executable applications that are allowed to handle enterprise data.</span></span> <span data-ttu-id="c3e3c-109">Doit être utilisé conjointement avec les paramètres de./Vendor/MSFT/Policy/ConfigSource/DataProtection.</span><span class="sxs-lookup"><span data-stu-id="c3e3c-109">Should be used in conjunction with the settings in ./Vendor/MSFT/Policy/ConfigSource/DataProtection .</span></span>

<span data-ttu-id="c3e3c-110">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c3e3c-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3e3c-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3e3c-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_EnterpriseDataProtection01_EXE03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a><span data-ttu-id="c3e3c-112">Membres</span><span class="sxs-lookup"><span data-stu-id="c3e3c-112">Members</span></span>

<span data-ttu-id="c3e3c-113">La **classe \_ \_ EnterpriseDataProtection01 \_ EXE03 de MDM AppLocker** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c3e3c-113">The **MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03** class has these types of members:</span></span>

-   [<span data-ttu-id="c3e3c-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c3e3c-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c3e3c-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c3e3c-115">Properties</span></span>

<span data-ttu-id="c3e3c-116">La **classe \_ \_ EnterpriseDataProtection01 \_ EXE03 de MDM AppLocker** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c3e3c-116">The **MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c3e3c-117">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c3e3c-117">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3e3c-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3e3c-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3e3c-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3e3c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3e3c-120">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c3e3c-120">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c3e3c-121">Définit des restrictions pour le lancement d’applications exécutables.</span><span class="sxs-lookup"><span data-stu-id="c3e3c-121">Defines restrictions for launching executable applications.</span></span>

</dd> <dt>

<span data-ttu-id="c3e3c-122">**ID**</span><span class="sxs-lookup"><span data-stu-id="c3e3c-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3e3c-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3e3c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3e3c-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3e3c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3e3c-125">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c3e3c-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c3e3c-126">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="c3e3c-126">Describes the full path to the parent node.</span></span> <span data-ttu-id="c3e3c-127">Pour cette classe, la chaîne est « ./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*regroupement*»</span><span class="sxs-lookup"><span data-stu-id="c3e3c-127">For this class, the string is "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="c3e3c-128">**Stratégie**</span><span class="sxs-lookup"><span data-stu-id="c3e3c-128">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3e3c-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3e3c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3e3c-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c3e3c-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3e3c-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3e3c-131">Requirements</span></span>



| <span data-ttu-id="c3e3c-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3e3c-132">Requirement</span></span> | <span data-ttu-id="c3e3c-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3e3c-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3e3c-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3e3c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c3e3c-135">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3e3c-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c3e3c-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3e3c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c3e3c-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3e3c-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c3e3c-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c3e3c-138">Namespace</span></span><br/>                | <span data-ttu-id="c3e3c-139">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="c3e3c-139">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="c3e3c-140">MOF</span><span class="sxs-lookup"><span data-stu-id="c3e3c-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3e3c-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c3e3c-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3e3c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c3e3c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3e3c-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3e3c-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3e3c-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3e3c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3e3c-145">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="c3e3c-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

