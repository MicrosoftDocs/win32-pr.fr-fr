---
title: Classe MDM_AssignedAccess
description: La \_ classe ASSIGNEDACCESS MDM est utilisée pour configurer l’appareil pour qu’il s’exécute en mode plein écran.
ms.assetid: b9837f91-3c13-4a80-bf6d-66d8b53dfa70
keywords:
- Classe MDM_AssignedAccess
- Classe MDM_AssignedAccess, Description
topic_type:
- apiref
api_name:
- MDM_AssignedAccess
- MDM_AssignedAccess.InstanceID
- MDM_AssignedAccess.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b5f03f99183400d4e7672323072415918e8e58e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466879"
---
# <a name="mdm_assignedaccess-class"></a><span data-ttu-id="a733f-105">\_Classe ASSIGNEDACCESS MDM</span><span class="sxs-lookup"><span data-stu-id="a733f-105">MDM\_AssignedAccess class</span></span>

<span data-ttu-id="a733f-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="a733f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a733f-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="a733f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a733f-108">La **classe \_ AssignedAccess MDM** est utilisée pour configurer l’appareil pour qu’il s’exécute en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="a733f-108">The **MDM\_AssignedAccess** class is used to set the device to run in kiosk mode.</span></span> <span data-ttu-id="a733f-109">Une fois la classe exécutée, la connexion utilisateur suivante associée au mode plein écran place l’appareil en mode plein écran exécutant l’application spécifiée dans le package d’approvisionnement.</span><span class="sxs-lookup"><span data-stu-id="a733f-109">Once the class has been executed, then the next user login that is associated with the kiosk mode puts the device in the kiosk mode running the application specified in the provisioning package.</span></span>

<span data-ttu-id="a733f-110">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a733f-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a733f-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a733f-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AssignedAccess
{
  string InstanceID;
  string ParentID;
  string KioskModeApp;
  string Configuration;
};
```

## <a name="members"></a><span data-ttu-id="a733f-112">Membres</span><span class="sxs-lookup"><span data-stu-id="a733f-112">Members</span></span>

<span data-ttu-id="a733f-113">La **classe \_ AssignedAccess MDM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a733f-113">The **MDM\_AssignedAccess** class has these types of members:</span></span>

-   [<span data-ttu-id="a733f-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a733f-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a733f-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a733f-115">Properties</span></span>

<span data-ttu-id="a733f-116">La **classe \_ AssignedAccess MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a733f-116">The **MDM\_AssignedAccess** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a733f-117">Configuration</span><span class="sxs-lookup"><span data-stu-id="a733f-117">Configuration</span></span>](/windows/client-management/mdm/assignedaccess-csp#assignedaccess-configuration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a733f-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a733f-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a733f-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a733f-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a733f-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a733f-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a733f-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a733f-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a733f-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a733f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a733f-123">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a733f-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a733f-124">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="a733f-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="a733f-125">Pour cette classe, la chaîne est « AssignedAccess ».</span><span class="sxs-lookup"><span data-stu-id="a733f-125">For this class, the string is "AssignedAccess".</span></span>

</dd> <dt>

[<span data-ttu-id="a733f-126">KioskModeApp</span><span class="sxs-lookup"><span data-stu-id="a733f-126">KioskModeApp</span></span>](/windows/client-management/mdm/assignedaccess-csp#assignedaccess-kioskmodeapp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a733f-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a733f-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a733f-128">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a733f-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a733f-129">**ID**</span><span class="sxs-lookup"><span data-stu-id="a733f-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a733f-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a733f-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a733f-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a733f-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a733f-132">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a733f-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a733f-133">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="a733f-133">Describes the full path to the parent node.</span></span> <span data-ttu-id="a733f-134">Pour cette classe, la chaîne est « ./Vendor/MSFT/ »</span><span class="sxs-lookup"><span data-stu-id="a733f-134">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a733f-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a733f-135">Requirements</span></span>



| <span data-ttu-id="a733f-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a733f-136">Requirement</span></span> | <span data-ttu-id="a733f-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="a733f-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a733f-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a733f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a733f-139">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a733f-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a733f-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a733f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a733f-141">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a733f-141">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a733f-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a733f-142">Namespace</span></span><br/>                | <span data-ttu-id="a733f-143">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="a733f-143">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a733f-144">MOF</span><span class="sxs-lookup"><span data-stu-id="a733f-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a733f-145"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a733f-145"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a733f-146">DLL</span><span class="sxs-lookup"><span data-stu-id="a733f-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a733f-147"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a733f-147"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a733f-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a733f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a733f-149">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="a733f-149">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

