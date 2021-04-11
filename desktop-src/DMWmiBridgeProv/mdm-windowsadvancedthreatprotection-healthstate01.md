---
title: Classe MDM_WindowsAdvancedThreatProtection_HealthState01
description: La \_ classe WindowsAdvancedThreatProtection \_ HealthState01 MDM est utilisée pour déterminer l’état d’intégrité des points de terminaison Windows Defender-protection avancée contre les menaces (émission).
ms.assetid: 8d630b95-9895-4cb8-99f2-8f869c4dfd18
keywords:
- Classe MDM_WindowsAdvancedThreatProtection_HealthState01
- Classe MDM_WindowsAdvancedThreatProtection_HealthState01, Description
topic_type:
- apiref
api_name:
- MDM_WindowsAdvancedThreatProtection_HealthState01
- MDM_WindowsAdvancedThreatProtection_HealthState01.InstanceID
- MDM_WindowsAdvancedThreatProtection_HealthState01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5519b731cf54a633a659ec865e7a1f0e12deda75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942517"
---
# <a name="mdm_windowsadvancedthreatprotection_healthstate01-class"></a><span data-ttu-id="1c4c4-105">\_ \_ Classe HEALTHSTATE01 WindowsAdvancedThreatProtection MDM</span><span class="sxs-lookup"><span data-stu-id="1c4c4-105">MDM\_WindowsAdvancedThreatProtection\_HealthState01 class</span></span>

<span data-ttu-id="1c4c4-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="1c4c4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1c4c4-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="1c4c4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1c4c4-108">La **classe \_ WindowsAdvancedThreatProtection \_ HealthState01 MDM** est utilisée pour déterminer l’état d’intégrité des points de terminaison Windows Defender-protection avancée contre les menaces (émission).</span><span class="sxs-lookup"><span data-stu-id="1c4c4-108">The **MDM\_WindowsAdvancedThreatProtection\_HealthState01** class is used to determine the health status of Windows Defender Advanced Threat Protection (WDATP) endpoints.</span></span>

<span data-ttu-id="1c4c4-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="1c4c4-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c4c4-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c4c4-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_HealthState01
{
  string   InstanceID;
  string   ParentID;
  datetime LastConnected;
  boolean  SenseIsRunning;
  sint32   OnboardingState;
  string   OrgId;
};
```

## <a name="members"></a><span data-ttu-id="1c4c4-111">Membres</span><span class="sxs-lookup"><span data-stu-id="1c4c4-111">Members</span></span>

<span data-ttu-id="1c4c4-112">La **classe \_ WindowsAdvancedThreatProtection \_ HealthState01 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1c4c4-112">The **MDM\_WindowsAdvancedThreatProtection\_HealthState01** class has these types of members:</span></span>

-   [<span data-ttu-id="1c4c4-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1c4c4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1c4c4-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1c4c4-114">Properties</span></span>

<span data-ttu-id="1c4c4-115">La **classe \_ WindowsAdvancedThreatProtection \_ HealthState01 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="1c4c4-115">The **MDM\_WindowsAdvancedThreatProtection\_HealthState01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1c4c4-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1c4c4-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c4c4-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1c4c4-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c4c4-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1c4c4-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c4c4-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1c4c4-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1c4c4-120">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="1c4c4-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="1c4c4-121">Pour cette classe, la chaîne est « HealthState ».</span><span class="sxs-lookup"><span data-stu-id="1c4c4-121">For this class, the string is "HealthState".</span></span>

</dd> <dt>

[<span data-ttu-id="1c4c4-122">LastConnected</span><span class="sxs-lookup"><span data-stu-id="1c4c4-122">LastConnected</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-lastconnected)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c4c4-123">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1c4c4-123">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1c4c4-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1c4c4-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1c4c4-125">OnboardingState</span><span class="sxs-lookup"><span data-stu-id="1c4c4-125">OnboardingState</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-onboardingstate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c4c4-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1c4c4-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c4c4-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1c4c4-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1c4c4-128">Identifiant OrgID</span><span class="sxs-lookup"><span data-stu-id="1c4c4-128">OrgId</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-orgid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c4c4-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1c4c4-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c4c4-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1c4c4-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1c4c4-131">**ID**</span><span class="sxs-lookup"><span data-stu-id="1c4c4-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c4c4-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1c4c4-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c4c4-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1c4c4-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c4c4-134">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1c4c4-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1c4c4-135">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="1c4c4-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="1c4c4-136">Pour cette classe, la chaîne est « ./Vendor/MSFT/WindowsAdvancedThreatProtection »</span><span class="sxs-lookup"><span data-stu-id="1c4c4-136">For this class, the string is "./Vendor/MSFT/WindowsAdvancedThreatProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="1c4c4-137">SenseIsRunning</span><span class="sxs-lookup"><span data-stu-id="1c4c4-137">SenseIsRunning</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-senseisrunning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c4c4-138">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="1c4c4-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c4c4-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1c4c4-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1c4c4-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c4c4-140">Requirements</span></span>



| <span data-ttu-id="1c4c4-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c4c4-141">Requirement</span></span> | <span data-ttu-id="1c4c4-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c4c4-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c4c4-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c4c4-143">Minimum supported client</span></span><br/> | <span data-ttu-id="1c4c4-144">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c4c4-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1c4c4-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c4c4-145">Minimum supported server</span></span><br/> | <span data-ttu-id="1c4c4-146">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c4c4-146">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="1c4c4-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1c4c4-147">Namespace</span></span><br/>                | <span data-ttu-id="1c4c4-148">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="1c4c4-148">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="1c4c4-149">MOF</span><span class="sxs-lookup"><span data-stu-id="1c4c4-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c4c4-150"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c4c4-150"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="1c4c4-151">DLL</span><span class="sxs-lookup"><span data-stu-id="1c4c4-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c4c4-152"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="1c4c4-152"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c4c4-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c4c4-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c4c4-154">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="1c4c4-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

