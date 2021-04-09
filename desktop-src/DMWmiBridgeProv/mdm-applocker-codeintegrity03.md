---
title: Classe MDM_AppLocker_CodeIntegrity03
description: La \_ \_ classe CODEINTEGRITY03 de MDM AppLocker définit la stratégie d’intégrité du code.
ms.assetid: 8e7649b4-2e89-4d79-923e-3767e5b0ea52
keywords:
- Classe MDM_AppLocker_CodeIntegrity03
- Classe MDM_AppLocker_CodeIntegrity03, Description
topic_type:
- apiref
api_name:
- MDM_AppLocker_CodeIntegrity03
- MDM_AppLocker_CodeIntegrity03.InstanceID
- MDM_AppLocker_CodeIntegrity03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff702f2887f47c1cc5fcebeb4b8ec9a08c450b8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741204"
---
# <a name="mdm_applocker_codeintegrity03-class"></a><span data-ttu-id="6a02b-105">\_ \_ Classe CODEINTEGRITY03 de MDM AppLocker</span><span class="sxs-lookup"><span data-stu-id="6a02b-105">MDM\_AppLocker\_CodeIntegrity03 class</span></span>

<span data-ttu-id="6a02b-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="6a02b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6a02b-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="6a02b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6a02b-108">La **classe \_ \_ CodeIntegrity03 de MDM AppLocker** définit la stratégie d’intégrité du code.</span><span class="sxs-lookup"><span data-stu-id="6a02b-108">The **MDM\_AppLocker\_CodeIntegrity03** class defines the policy for Code Integrity.</span></span>

<span data-ttu-id="6a02b-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6a02b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a02b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a02b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_CodeIntegrity03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a><span data-ttu-id="6a02b-111">Membres</span><span class="sxs-lookup"><span data-stu-id="6a02b-111">Members</span></span>

<span data-ttu-id="6a02b-112">La **classe \_ \_ CodeIntegrity03 de MDM AppLocker** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6a02b-112">The **MDM\_AppLocker\_CodeIntegrity03** class has these types of members:</span></span>

-   [<span data-ttu-id="6a02b-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6a02b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6a02b-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6a02b-114">Properties</span></span>

<span data-ttu-id="6a02b-115">La **classe \_ \_ CodeIntegrity03 de MDM AppLocker** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6a02b-115">The **MDM\_AppLocker\_CodeIntegrity03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6a02b-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6a02b-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a02b-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6a02b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a02b-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a02b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a02b-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6a02b-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6a02b-120">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="6a02b-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="6a02b-121">**ID**</span><span class="sxs-lookup"><span data-stu-id="6a02b-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a02b-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6a02b-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a02b-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a02b-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a02b-124">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6a02b-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6a02b-125">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="6a02b-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="6a02b-126">Pour cette classe, la chaîne est « ./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions »</span><span class="sxs-lookup"><span data-stu-id="6a02b-126">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span></span>

</dd> <dt>

[<span data-ttu-id="6a02b-127">**Stratégie**</span><span class="sxs-lookup"><span data-stu-id="6a02b-127">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a02b-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6a02b-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a02b-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6a02b-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6a02b-130">Qualificateurs : **Octetstring**</span><span class="sxs-lookup"><span data-stu-id="6a02b-130">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6a02b-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a02b-131">Requirements</span></span>



| <span data-ttu-id="6a02b-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a02b-132">Requirement</span></span> | <span data-ttu-id="6a02b-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a02b-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a02b-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a02b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6a02b-135">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a02b-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6a02b-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a02b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6a02b-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a02b-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6a02b-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6a02b-138">Namespace</span></span><br/>                | <span data-ttu-id="6a02b-139">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="6a02b-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="6a02b-140">MOF</span><span class="sxs-lookup"><span data-stu-id="6a02b-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a02b-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a02b-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a02b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6a02b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a02b-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a02b-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a02b-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a02b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a02b-145">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="6a02b-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

