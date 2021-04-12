---
title: Classe MDM_Policy_Result01_Experience02
description: La \_ classe Result01 Experience02 de la stratégie MDM \_ \_ représente les stratégies d’expérience disponibles.
ms.assetid: c6dc2ef1-1f12-40b0-9d5f-9e886fe1e128
keywords:
- Classe MDM_Policy_Result01_Experience02
- Classe MDM_Policy_Result01_Experience02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Experience02
- MDM_Policy_Result01_Experience02.InstanceID
- MDM_Policy_Result01_Experience02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a767c96d7ee23b4dad9719fa74850b39f0759b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032406"
---
# <a name="mdm_policy_result01_experience02-class"></a><span data-ttu-id="31462-105">\_Classe Experience02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="31462-105">MDM\_Policy\_Result01\_Experience02 class</span></span>

<span data-ttu-id="31462-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="31462-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="31462-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="31462-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="31462-108">La **classe \_ \_ Result01 \_ Experience02 de la stratégie MDM** représente les stratégies d’expérience disponibles.</span><span class="sxs-lookup"><span data-stu-id="31462-108">The **MDM\_Policy\_Result01\_Experience02** class represents the experience policies available.</span></span>

<span data-ttu-id="31462-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="31462-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="31462-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31462-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Experience02
{
  string InstanceID;
  string ParentID;
  sint32 AllowCortana;
  sint32 AllowDeviceDiscovery;
  sint32 AllowFindMyDevice;
  sint32 AllowManualMDMUnenrollment;
  sint32 AllowSharingOfOfficeFiles;
  sint32 AllowSIMErrorDialogPromptWhenNoSIM;
  sint32 AllowSaveAsOfOfficeFiles;
  sint32 AllowScreenCapture;
  sint32 AllowSyncMySettings;
  sint32 AllowWindowsTips;
  sint32 DoNotShowFeedbackNotifications;
};
```

## <a name="members"></a><span data-ttu-id="31462-111">Membres</span><span class="sxs-lookup"><span data-stu-id="31462-111">Members</span></span>

<span data-ttu-id="31462-112">La **classe \_ \_ Result01 \_ Experience02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="31462-112">The **MDM\_Policy\_Result01\_Experience02** class has these types of members:</span></span>

-   [<span data-ttu-id="31462-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="31462-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="31462-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="31462-114">Properties</span></span>

<span data-ttu-id="31462-115">La **classe \_ \_ Result01 \_ Experience02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="31462-115">The **MDM\_Policy\_Result01\_Experience02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="31462-116">AllowCortana</span><span class="sxs-lookup"><span data-stu-id="31462-116">AllowCortana</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowcortana)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31462-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31462-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31462-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31462-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31462-119">AllowDeviceDiscovery</span><span class="sxs-lookup"><span data-stu-id="31462-119">AllowDeviceDiscovery</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowdevicediscovery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31462-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31462-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31462-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31462-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31462-122">AllowFindMyDevice</span><span class="sxs-lookup"><span data-stu-id="31462-122">AllowFindMyDevice</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowfindmydevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31462-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31462-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31462-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31462-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31462-125">AllowManualMDMUnenrollment</span><span class="sxs-lookup"><span data-stu-id="31462-125">AllowManualMDMUnenrollment</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowmanualmdmunenrollment)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31462-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31462-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31462-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31462-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31462-128">AllowSaveAsOfOfficeFiles</span><span class="sxs-lookup"><span data-stu-id="31462-128">AllowSaveAsOfOfficeFiles</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsaveasofofficefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31462-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31462-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31462-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31462-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="31462-131">AllowScreenCapture</span><span class="sxs-lookup"><span data-stu-id="31462-131">AllowScreenCapture</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31462-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31462-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31462-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31462-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31462-134">AllowSharingOfOfficeFiles</span><span class="sxs-lookup"><span data-stu-id="31462-134">AllowSharingOfOfficeFiles</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsharingofofficefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31462-135">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31462-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31462-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31462-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="31462-137">AllowSIMErrorDialogPromptWhenNoSIM</span><span class="sxs-lookup"><span data-stu-id="31462-137">AllowSIMErrorDialogPromptWhenNoSIM</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31462-138">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31462-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31462-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31462-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31462-140">AllowSyncMySettings</span><span class="sxs-lookup"><span data-stu-id="31462-140">AllowSyncMySettings</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsyncmysettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31462-141">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31462-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31462-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31462-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31462-143">AllowWindowsTips</span><span class="sxs-lookup"><span data-stu-id="31462-143">AllowWindowsTips</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowstips)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31462-144">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31462-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31462-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31462-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31462-146">DoNotShowFeedbackNotifications</span><span class="sxs-lookup"><span data-stu-id="31462-146">DoNotShowFeedbackNotifications</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-donotshowfeedbacknotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31462-147">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31462-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31462-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="31462-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="31462-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="31462-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31462-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31462-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31462-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31462-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31462-152">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="31462-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="31462-153">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="31462-153">Identifies the name of the parent node.</span></span> <span data-ttu-id="31462-154">Pour cette classe, la chaîne est « experience ».</span><span class="sxs-lookup"><span data-stu-id="31462-154">For this class, the string is "Experience".</span></span>

</dd> <dt>

<span data-ttu-id="31462-155">**ID**</span><span class="sxs-lookup"><span data-stu-id="31462-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31462-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31462-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31462-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31462-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31462-158">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="31462-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="31462-159">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="31462-159">Describes the full path to the parent node.</span></span> <span data-ttu-id="31462-160">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Result »</span><span class="sxs-lookup"><span data-stu-id="31462-160">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31462-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31462-161">Requirements</span></span>



| <span data-ttu-id="31462-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31462-162">Requirement</span></span> | <span data-ttu-id="31462-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="31462-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31462-164">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31462-164">Minimum supported client</span></span><br/> | <span data-ttu-id="31462-165">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31462-165">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="31462-166">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31462-166">Minimum supported server</span></span><br/> | <span data-ttu-id="31462-167">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="31462-167">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="31462-168">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="31462-168">Namespace</span></span><br/>                | <span data-ttu-id="31462-169">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="31462-169">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="31462-170">MOF</span><span class="sxs-lookup"><span data-stu-id="31462-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31462-171"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31462-171"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="31462-172">DLL</span><span class="sxs-lookup"><span data-stu-id="31462-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31462-173"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31462-173"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31462-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31462-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31462-175">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="31462-175">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

