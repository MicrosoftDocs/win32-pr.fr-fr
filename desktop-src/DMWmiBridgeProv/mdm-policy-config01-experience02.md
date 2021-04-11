---
title: Classe MDM_Policy_Config01_Experience02
description: La \_ classe Config01 Experience02 de la stratégie MDM \_ \_ représente les stratégies d’expérience disponibles.
ms.assetid: 21052983-696c-4137-9c72-16ea3b4a1eb7
keywords:
- Classe MDM_Policy_Config01_Experience02
- Classe MDM_Policy_Config01_Experience02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Experience02
- MDM_Policy_Config01_Experience02.InstanceID
- MDM_Policy_Config01_Experience02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38885dbc22c51bfa9e1653f81dba38255f6ba6a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105721"
---
# <a name="mdm_policy_config01_experience02-class"></a><span data-ttu-id="f29f1-105">\_Classe Experience02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="f29f1-105">MDM\_Policy\_Config01\_Experience02 class</span></span>

<span data-ttu-id="f29f1-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="f29f1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f29f1-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="f29f1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f29f1-108">La **classe \_ \_ Config01 \_ Experience02 de la stratégie MDM** représente les stratégies d’expérience disponibles.</span><span class="sxs-lookup"><span data-stu-id="f29f1-108">The **MDM\_Policy\_Config01\_Experience02** class represents the experience policies available.</span></span>

<span data-ttu-id="f29f1-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f29f1-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f29f1-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f29f1-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Experience02
{
  string InstanceID;
  string ParentID;
  sint32 AllowCortana;
  sint32 AllowDeviceDiscovery;
  sint32 AllowFindMyDevice;
  sint32 AllowManualMDMUnenrollment;
  sint32 AllowSaveAsOfOfficeFiles;
  sint32 AllowScreenCapture;
  sint32 AllowSIMErrorDialogPromptWhenNoSIM;
  sint32 AllowSharingOfOfficeFiles;
  sint32 AllowSyncMySettings;
  sint32 AllowWindowsTips;
  sint32 DoNotShowFeedbackNotifications;
};
```

## <a name="members"></a><span data-ttu-id="f29f1-111">Membres</span><span class="sxs-lookup"><span data-stu-id="f29f1-111">Members</span></span>

<span data-ttu-id="f29f1-112">La **classe \_ \_ Config01 \_ Experience02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f29f1-112">The **MDM\_Policy\_Config01\_Experience02** class has these types of members:</span></span>

-   [<span data-ttu-id="f29f1-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f29f1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f29f1-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f29f1-114">Properties</span></span>

<span data-ttu-id="f29f1-115">La **classe \_ \_ Config01 \_ Experience02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="f29f1-115">The **MDM\_Policy\_Config01\_Experience02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f29f1-116">AllowCortana</span><span class="sxs-lookup"><span data-stu-id="f29f1-116">AllowCortana</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowcortana)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f29f1-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f29f1-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f29f1-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f29f1-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f29f1-119">AllowDeviceDiscovery</span><span class="sxs-lookup"><span data-stu-id="f29f1-119">AllowDeviceDiscovery</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowdevicediscovery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f29f1-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f29f1-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f29f1-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f29f1-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f29f1-122">AllowFindMyDevice</span><span class="sxs-lookup"><span data-stu-id="f29f1-122">AllowFindMyDevice</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowfindmydevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f29f1-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f29f1-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f29f1-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f29f1-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f29f1-125">AllowManualMDMUnenrollment</span><span class="sxs-lookup"><span data-stu-id="f29f1-125">AllowManualMDMUnenrollment</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowmanualmdmunenrollment)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f29f1-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f29f1-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f29f1-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f29f1-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f29f1-128">AllowSaveAsOfOfficeFiles</span><span class="sxs-lookup"><span data-stu-id="f29f1-128">AllowSaveAsOfOfficeFiles</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsaveasofofficefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f29f1-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f29f1-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f29f1-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f29f1-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f29f1-131">AllowScreenCapture</span><span class="sxs-lookup"><span data-stu-id="f29f1-131">AllowScreenCapture</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f29f1-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f29f1-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f29f1-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f29f1-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f29f1-134">AllowSharingOfOfficeFiles</span><span class="sxs-lookup"><span data-stu-id="f29f1-134">AllowSharingOfOfficeFiles</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsharingofofficefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f29f1-135">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f29f1-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f29f1-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f29f1-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f29f1-137">AllowSIMErrorDialogPromptWhenNoSIM</span><span class="sxs-lookup"><span data-stu-id="f29f1-137">AllowSIMErrorDialogPromptWhenNoSIM</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f29f1-138">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f29f1-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f29f1-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f29f1-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f29f1-140">AllowSyncMySettings</span><span class="sxs-lookup"><span data-stu-id="f29f1-140">AllowSyncMySettings</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsyncmysettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f29f1-141">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f29f1-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f29f1-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f29f1-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f29f1-143">AllowWindowsTips</span><span class="sxs-lookup"><span data-stu-id="f29f1-143">AllowWindowsTips</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowstips)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f29f1-144">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f29f1-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f29f1-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f29f1-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f29f1-146">DoNotShowFeedbackNotifications</span><span class="sxs-lookup"><span data-stu-id="f29f1-146">DoNotShowFeedbackNotifications</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-donotshowfeedbacknotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f29f1-147">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f29f1-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f29f1-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f29f1-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f29f1-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f29f1-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f29f1-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f29f1-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f29f1-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f29f1-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f29f1-152">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f29f1-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f29f1-153">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="f29f1-153">Identifies the name of the parent node.</span></span> <span data-ttu-id="f29f1-154">Pour cette classe, la chaîne est « experience ».</span><span class="sxs-lookup"><span data-stu-id="f29f1-154">For this class, the string is "Experience".</span></span>

</dd> <dt>

<span data-ttu-id="f29f1-155">**ID**</span><span class="sxs-lookup"><span data-stu-id="f29f1-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f29f1-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f29f1-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f29f1-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f29f1-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f29f1-158">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f29f1-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f29f1-159">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="f29f1-159">Describes the full path to the parent node.</span></span> <span data-ttu-id="f29f1-160">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Config »</span><span class="sxs-lookup"><span data-stu-id="f29f1-160">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f29f1-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f29f1-161">Requirements</span></span>



| <span data-ttu-id="f29f1-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f29f1-162">Requirement</span></span> | <span data-ttu-id="f29f1-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="f29f1-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f29f1-164">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f29f1-164">Minimum supported client</span></span><br/> | <span data-ttu-id="f29f1-165">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f29f1-165">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f29f1-166">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f29f1-166">Minimum supported server</span></span><br/> | <span data-ttu-id="f29f1-167">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f29f1-167">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f29f1-168">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f29f1-168">Namespace</span></span><br/>                | <span data-ttu-id="f29f1-169">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="f29f1-169">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="f29f1-170">MOF</span><span class="sxs-lookup"><span data-stu-id="f29f1-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f29f1-171"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f29f1-171"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f29f1-172">DLL</span><span class="sxs-lookup"><span data-stu-id="f29f1-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f29f1-173"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f29f1-173"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f29f1-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f29f1-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f29f1-175">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="f29f1-175">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

