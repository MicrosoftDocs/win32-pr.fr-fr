---
title: Classe MDM_WindowsAdvancedThreatProtection_Configuration01
description: La \_ classe WindowsAdvancedThreatProtection \_ Configuration01 MDM est utilisée pour déterminer la configuration des points de terminaison Windows Defender-protection avancée contre les menaces (émission).
ms.assetid: b4b2ff02-3836-4044-b8fa-d3405f433d8c
keywords:
- Classe MDM_WindowsAdvancedThreatProtection_Configuration01
- Classe MDM_WindowsAdvancedThreatProtection_Configuration01, Description
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MDM_WindowsAdvancedThreatProtection_Configuration01
- MDM_WindowsAdvancedThreatProtection_Configuration01.InstanceID
- MDM_WindowsAdvancedThreatProtection_Configuration01.ParentID
- MDM_WindowsAdvancedThreatProtection_Configuration01.GroupIds
api_type:
- DllExport
api_location:
- Mofs\DMWmiBridgeProv.dll
ms.openlocfilehash: c6cd6689a66735790c381ac307a443c08464a379
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509006"
---
# <a name="mdm_windowsadvancedthreatprotection_configuration01-class"></a><span data-ttu-id="8fc8a-105">\_ \_ Classe CONFIGURATION01 WindowsAdvancedThreatProtection MDM</span><span class="sxs-lookup"><span data-stu-id="8fc8a-105">MDM\_WindowsAdvancedThreatProtection\_Configuration01 class</span></span>

<span data-ttu-id="8fc8a-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="8fc8a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8fc8a-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="8fc8a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8fc8a-108">La **classe \_ WindowsAdvancedThreatProtection \_ Configuration01 MDM** est utilisée pour déterminer la configuration des points de terminaison Windows Defender-protection avancée contre les menaces (émission).</span><span class="sxs-lookup"><span data-stu-id="8fc8a-108">The **MDM\_WindowsAdvancedThreatProtection\_Configuration01** class is used to determine the configuration of Windows Defender Advanced Threat Protection (WDATP) endpoints.</span></span>

<span data-ttu-id="8fc8a-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8fc8a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fc8a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8fc8a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_Configuration01
{
  string InstanceID;
  string ParentID;
  sint32 SampleSharing;
  string GroupIds;
  sint32 TelemetryReportingFrequency;
};
```

## <a name="members"></a><span data-ttu-id="8fc8a-111">Membres</span><span class="sxs-lookup"><span data-stu-id="8fc8a-111">Members</span></span>

<span data-ttu-id="8fc8a-112">La **classe \_ WindowsAdvancedThreatProtection \_ Configuration01 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8fc8a-112">The **MDM\_WindowsAdvancedThreatProtection\_Configuration01** class has these types of members:</span></span>

-   [<span data-ttu-id="8fc8a-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8fc8a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8fc8a-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8fc8a-114">Properties</span></span>

<span data-ttu-id="8fc8a-115">La **classe \_ WindowsAdvancedThreatProtection \_ Configuration01 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="8fc8a-115">The **MDM\_WindowsAdvancedThreatProtection\_Configuration01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8fc8a-116">**GroupIds**</span><span class="sxs-lookup"><span data-stu-id="8fc8a-116">**GroupIds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fc8a-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8fc8a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fc8a-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8fc8a-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8fc8a-119">TBD</span><span class="sxs-lookup"><span data-stu-id="8fc8a-119">TBD</span></span>

</dd> <dt>

<span data-ttu-id="8fc8a-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8fc8a-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fc8a-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8fc8a-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fc8a-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8fc8a-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fc8a-123">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8fc8a-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8fc8a-124">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="8fc8a-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="8fc8a-125">Pour cette classe, la chaîne est « configuration ».</span><span class="sxs-lookup"><span data-stu-id="8fc8a-125">For this class, the string is "Configuration".</span></span>

</dd> <dt>

<span data-ttu-id="8fc8a-126">**ID**</span><span class="sxs-lookup"><span data-stu-id="8fc8a-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fc8a-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8fc8a-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fc8a-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8fc8a-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fc8a-129">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8fc8a-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8fc8a-130">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="8fc8a-130">Describes the full path to the parent node.</span></span> <span data-ttu-id="8fc8a-131">Pour cette classe, la chaîne est « ./Vendor/MSFT/WindowsAdvancedThreatProtection »</span><span class="sxs-lookup"><span data-stu-id="8fc8a-131">For this class, the string is "./Vendor/MSFT/WindowsAdvancedThreatProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="8fc8a-132">SampleSharing</span><span class="sxs-lookup"><span data-stu-id="8fc8a-132">SampleSharing</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#configuration-samplesharing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fc8a-133">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8fc8a-133">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8fc8a-134">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8fc8a-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8fc8a-135">TelemetryReportingFrequency</span><span class="sxs-lookup"><span data-stu-id="8fc8a-135">TelemetryReportingFrequency</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#configuration-telemetryreportingfrequency)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fc8a-136">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8fc8a-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8fc8a-137">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8fc8a-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8fc8a-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fc8a-138">Requirements</span></span>



| <span data-ttu-id="8fc8a-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8fc8a-139">Requirement</span></span> | <span data-ttu-id="8fc8a-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fc8a-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fc8a-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fc8a-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8fc8a-142">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8fc8a-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8fc8a-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fc8a-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8fc8a-144">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fc8a-144">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="8fc8a-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8fc8a-145">Namespace</span></span><br/>                | <span data-ttu-id="8fc8a-146">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="8fc8a-146">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="8fc8a-147">MOF</span><span class="sxs-lookup"><span data-stu-id="8fc8a-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fc8a-148"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8fc8a-148"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="8fc8a-149">DLL</span><span class="sxs-lookup"><span data-stu-id="8fc8a-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fc8a-150"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="8fc8a-150"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fc8a-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fc8a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fc8a-152">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="8fc8a-152">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

