---
title: Classe MDM_WindowsAdvancedThreatProtection
description: La \_ classe WINDOWSADVANCEDTHREATPROTECTION MDM est utilisée pour intégrer et annuler des points de terminaison pour Windows Defender-protection avancée contre les menaces (émission).
ms.assetid: 7a95253e-6d13-4c1b-b78d-c56c6378f7c3
keywords:
- Classe MDM_WindowsAdvancedThreatProtection
- Classe MDM_WindowsAdvancedThreatProtection, Description
topic_type:
- apiref
api_name:
- MDM_WindowsAdvancedThreatProtection
- MDM_WindowsAdvancedThreatProtection.InstanceID
- MDM_WindowsAdvancedThreatProtection.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c369406a3c8bcf982aeb18b4bbb53c1af4983e84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511579"
---
# <a name="mdm_windowsadvancedthreatprotection-class"></a><span data-ttu-id="d22a5-105">\_Classe WINDOWSADVANCEDTHREATPROTECTION MDM</span><span class="sxs-lookup"><span data-stu-id="d22a5-105">MDM\_WindowsAdvancedThreatProtection class</span></span>

<span data-ttu-id="d22a5-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="d22a5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d22a5-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="d22a5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d22a5-108">La **classe \_ WindowsAdvancedThreatProtection MDM** est utilisée pour intégrer et annuler des points de terminaison pour Windows Defender-protection avancée contre les menaces (émission).</span><span class="sxs-lookup"><span data-stu-id="d22a5-108">The **MDM\_WindowsAdvancedThreatProtection** class is used to onboard and offboard endpoints for Windows Defender Advanced Threat Protection (WDATP).</span></span>

<span data-ttu-id="d22a5-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d22a5-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d22a5-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d22a5-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection
{
  string InstanceID;
  string ParentID;
  string Onboarding;
  string Offboarding;
};
```

## <a name="members"></a><span data-ttu-id="d22a5-111">Membres</span><span class="sxs-lookup"><span data-stu-id="d22a5-111">Members</span></span>

<span data-ttu-id="d22a5-112">La **classe \_ WindowsAdvancedThreatProtection MDM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d22a5-112">The **MDM\_WindowsAdvancedThreatProtection** class has these types of members:</span></span>

-   [<span data-ttu-id="d22a5-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d22a5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d22a5-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d22a5-114">Properties</span></span>

<span data-ttu-id="d22a5-115">La **classe \_ WindowsAdvancedThreatProtection MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d22a5-115">The **MDM\_WindowsAdvancedThreatProtection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d22a5-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d22a5-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d22a5-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d22a5-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d22a5-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d22a5-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d22a5-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d22a5-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d22a5-120">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="d22a5-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="d22a5-121">Pour cette classe, la chaîne est « WindowsAdvancedThreatProtection ».</span><span class="sxs-lookup"><span data-stu-id="d22a5-121">For this class, the string is "WindowsAdvancedThreatProtection".</span></span>

</dd> <dt>

[<span data-ttu-id="d22a5-122">Désintégration</span><span class="sxs-lookup"><span data-stu-id="d22a5-122">Offboarding</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#offboarding)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d22a5-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d22a5-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d22a5-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d22a5-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d22a5-125">Intégration</span><span class="sxs-lookup"><span data-stu-id="d22a5-125">Onboarding</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#onboarding)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d22a5-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d22a5-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d22a5-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d22a5-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d22a5-128">**ID**</span><span class="sxs-lookup"><span data-stu-id="d22a5-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d22a5-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d22a5-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d22a5-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d22a5-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d22a5-131">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d22a5-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d22a5-132">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="d22a5-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="d22a5-133">Pour cette classe, la chaîne est « ./Vendor/MSFT/ »</span><span class="sxs-lookup"><span data-stu-id="d22a5-133">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d22a5-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d22a5-134">Requirements</span></span>



| <span data-ttu-id="d22a5-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d22a5-135">Requirement</span></span> | <span data-ttu-id="d22a5-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="d22a5-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d22a5-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d22a5-137">Minimum supported client</span></span><br/> | <span data-ttu-id="d22a5-138">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d22a5-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d22a5-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d22a5-139">Minimum supported server</span></span><br/> | <span data-ttu-id="d22a5-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d22a5-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="d22a5-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d22a5-141">Namespace</span></span><br/>                | <span data-ttu-id="d22a5-142">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="d22a5-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="d22a5-143">MOF</span><span class="sxs-lookup"><span data-stu-id="d22a5-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d22a5-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d22a5-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="d22a5-145">DLL</span><span class="sxs-lookup"><span data-stu-id="d22a5-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d22a5-146"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="d22a5-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d22a5-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d22a5-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d22a5-148">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="d22a5-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

