---
title: Classe MDM_Policy_Config01_DeviceLock02
description: La \_ classe Config01 DeviceLock02 de la stratégie MDM \_ \_ représente les stratégies de verrouillage des appareils disponibles.
ms.assetid: 222081ec-c38f-481d-ae38-941fd1317197
keywords:
- Classe MDM_Policy_Config01_DeviceLock02
- Classe MDM_Policy_Config01_DeviceLock02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DeviceLock02
- MDM_Policy_Config01_DeviceLock02.InstanceID
- MDM_Policy_Config01_DeviceLock02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c5926912d276fbe04f75c161196c47d0f0dd384
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105727"
---
# <a name="mdm_policy_config01_devicelock02-class"></a><span data-ttu-id="8ae12-105">\_Classe DeviceLock02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="8ae12-105">MDM\_Policy\_Config01\_DeviceLock02 class</span></span>

<span data-ttu-id="8ae12-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="8ae12-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8ae12-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="8ae12-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8ae12-108">La **classe \_ \_ Config01 \_ DeviceLock02 de la stratégie MDM** représente les stratégies de verrouillage des appareils disponibles.</span><span class="sxs-lookup"><span data-stu-id="8ae12-108">The **MDM\_Policy\_Config01\_DeviceLock02** class represents the device lock policies available.</span></span>

<span data-ttu-id="8ae12-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8ae12-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ae12-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ae12-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DeviceLock02
{
  string InstanceID;
  string ParentID;
  sint32 AllowScreenTimeoutWhileLockedUserConfig;
  sint32 AllowSimpleDevicePassword;
  sint32 AlphanumericDevicePasswordRequired;
  sint32 DevicePasswordEnabled;
  sint32 DevicePasswordExpiration;
  sint32 DevicePasswordHistory;
  string EnforceLockScreenAndLogonImage;
  string EnforceLockScreenProvider;
  sint32 MinimumPasswordAge;
  sint32 MaxDevicePasswordFailedAttempts;
  sint32 MaxInactivityTimeDeviceLock;
  sint32 MinDevicePasswordComplexCharacters;
  sint32 MinDevicePasswordLength;
  sint32 ScreenTimeoutWhileLocked;
  string PreventLockScreenSlideShow;
};
```

## <a name="members"></a><span data-ttu-id="8ae12-111">Membres</span><span class="sxs-lookup"><span data-stu-id="8ae12-111">Members</span></span>

<span data-ttu-id="8ae12-112">La **classe \_ \_ Config01 \_ DeviceLock02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8ae12-112">The **MDM\_Policy\_Config01\_DeviceLock02** class has these types of members:</span></span>

-   [<span data-ttu-id="8ae12-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8ae12-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8ae12-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8ae12-114">Properties</span></span>

<span data-ttu-id="8ae12-115">La **classe \_ \_ Config01 \_ DeviceLock02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="8ae12-115">The **MDM\_Policy\_Config01\_DeviceLock02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8ae12-116">AllowScreenTimeoutWhileLockedUserConfig</span><span class="sxs-lookup"><span data-stu-id="8ae12-116">AllowScreenTimeoutWhileLockedUserConfig</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae12-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ae12-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ae12-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ae12-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ae12-119">AllowSimpleDevicePassword</span><span class="sxs-lookup"><span data-stu-id="8ae12-119">AllowSimpleDevicePassword</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-allowsimpledevicepassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae12-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ae12-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ae12-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ae12-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ae12-122">AlphanumericDevicePasswordRequired</span><span class="sxs-lookup"><span data-stu-id="8ae12-122">AlphanumericDevicePasswordRequired</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-alphanumericdevicepasswordrequired)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae12-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ae12-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ae12-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ae12-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ae12-125">DevicePasswordEnabled</span><span class="sxs-lookup"><span data-stu-id="8ae12-125">DevicePasswordEnabled</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordenabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae12-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ae12-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ae12-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ae12-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8ae12-128">DevicePasswordEnabled ne doit pas être défini sur activé (0) quand WMI est utilisé pour définir les stratégies DeviceLock EAS, étant donné qu’il est activé par défaut dans le CSP de stratégie pour la compatibilité avec Windows 8. x.</span><span class="sxs-lookup"><span data-stu-id="8ae12-128">DevicePasswordEnabled should not be set to Enabled (0) when WMI is used to set the EAS DeviceLock policies given that it is Enabled by default in Policy CSP for back compat with Windows 8.x.</span></span> <span data-ttu-id="8ae12-129">Si DevicePasswordEnabled a la valeur activé (0), le fournisseur de services Cloud de stratégie renvoie une erreur indiquant que DevicePasswordEnabled existe déjà.</span><span class="sxs-lookup"><span data-stu-id="8ae12-129">If DevicePasswordEnabled is set to Enabled(0) then Policy CSP will return an error stating that DevicePasswordEnabled already exists.</span></span> <span data-ttu-id="8ae12-130">Windows 8. x ne prenait pas en charge la stratégie DevicePassword.</span><span class="sxs-lookup"><span data-stu-id="8ae12-130">Windows 8.x did not support DevicePassword policy.</span></span> <span data-ttu-id="8ae12-131">Lors de la désactivation de DevicePasswordEnabled (1), il doit s’agir de la seule stratégie définie dans le groupe de stratégies DeviceLock ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="8ae12-131">When disabling DevicePasswordEnabled  (1) then this should be the only policy set from the DeviceLock group of policies below.</span></span> <span data-ttu-id="8ae12-132">Les stratégies sont répertoriées ci-dessous : >-DevicePasswordEnabled est la stratégie parente des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="8ae12-132">The policies are listed below: > - DevicePasswordEnabled is the parent policy of the following:</span></span>

-   <span data-ttu-id="8ae12-133">DevicePasswordEnabled est la stratégie parente des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="8ae12-133">DevicePasswordEnabled is the parent policy of the following:</span></span>
    -   <span data-ttu-id="8ae12-134">AllowSimpleDevicePassword</span><span class="sxs-lookup"><span data-stu-id="8ae12-134">AllowSimpleDevicePassword</span></span>
    -   <span data-ttu-id="8ae12-135">MinDevicePasswordLength</span><span class="sxs-lookup"><span data-stu-id="8ae12-135">MinDevicePasswordLength</span></span>
    -   <span data-ttu-id="8ae12-136">AlphanumericDevicePasswordRequired est la stratégie parente de :</span><span class="sxs-lookup"><span data-stu-id="8ae12-136">AlphanumericDevicePasswordRequired is the parent policy of:</span></span>
        -   <span data-ttu-id="8ae12-137">MinDevicePasswordComplexCharacters</span><span class="sxs-lookup"><span data-stu-id="8ae12-137">MinDevicePasswordComplexCharacters</span></span> 
    -   <span data-ttu-id="8ae12-138">MaxDevicePasswordFailedAttempts</span><span class="sxs-lookup"><span data-stu-id="8ae12-138">MaxDevicePasswordFailedAttempts</span></span>
    -   <span data-ttu-id="8ae12-139">MaxInactivityTimeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="8ae12-139">MaxInactivityTimeDeviceLock</span></span>

</dd> <dt>

[<span data-ttu-id="8ae12-140">DevicePasswordExpiration</span><span class="sxs-lookup"><span data-stu-id="8ae12-140">DevicePasswordExpiration</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordexpiration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae12-141">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ae12-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ae12-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ae12-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ae12-143">DevicePasswordHistory</span><span class="sxs-lookup"><span data-stu-id="8ae12-143">DevicePasswordHistory</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae12-144">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ae12-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ae12-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ae12-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ae12-146">EnforceLockScreenAndLogonImage</span><span class="sxs-lookup"><span data-stu-id="8ae12-146">EnforceLockScreenAndLogonImage</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-enforcelockscreenandlogonimage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae12-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ae12-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ae12-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ae12-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8ae12-149">EnforceLockScreenProvider</span><span class="sxs-lookup"><span data-stu-id="8ae12-149">EnforceLockScreenProvider</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae12-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ae12-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ae12-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ae12-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8ae12-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8ae12-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae12-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ae12-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ae12-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8ae12-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ae12-155">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8ae12-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8ae12-156">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="8ae12-156">Identifies the name of the parent node.</span></span> <span data-ttu-id="8ae12-157">Pour cette classe, la chaîne est « DeviceLock ».</span><span class="sxs-lookup"><span data-stu-id="8ae12-157">For this class, the string is "DeviceLock".</span></span>

</dd> <dt>

[<span data-ttu-id="8ae12-158">MaxDevicePasswordFailedAttempts</span><span class="sxs-lookup"><span data-stu-id="8ae12-158">MaxDevicePasswordFailedAttempts</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxdevicepasswordfailedattempts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae12-159">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ae12-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ae12-160">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ae12-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ae12-161">MaxInactivityTimeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="8ae12-161">MaxInactivityTimeDeviceLock</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxinactivitytimedevicelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae12-162">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ae12-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ae12-163">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ae12-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ae12-164">MinDevicePasswordComplexCharacters</span><span class="sxs-lookup"><span data-stu-id="8ae12-164">MinDevicePasswordComplexCharacters</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordcomplexcharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae12-165">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ae12-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ae12-166">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ae12-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ae12-167">MinDevicePasswordLength</span><span class="sxs-lookup"><span data-stu-id="8ae12-167">MinDevicePasswordLength</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae12-168">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ae12-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ae12-169">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ae12-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ae12-170">MinimumPasswordAge</span><span class="sxs-lookup"><span data-stu-id="8ae12-170">MinimumPasswordAge</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-minimumpasswordage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae12-171">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ae12-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ae12-172">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ae12-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8ae12-173">**ID**</span><span class="sxs-lookup"><span data-stu-id="8ae12-173">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae12-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ae12-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ae12-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8ae12-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ae12-176">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8ae12-176">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8ae12-177">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="8ae12-177">Describes the full path to the parent node.</span></span> <span data-ttu-id="8ae12-178">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Config »</span><span class="sxs-lookup"><span data-stu-id="8ae12-178">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="8ae12-179">PreventLockScreenSlideShow</span><span class="sxs-lookup"><span data-stu-id="8ae12-179">PreventLockScreenSlideShow</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-preventlockscreenslideshow)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae12-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ae12-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ae12-181">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ae12-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8ae12-182">ScreenTimeoutWhileLocked</span><span class="sxs-lookup"><span data-stu-id="8ae12-182">ScreenTimeoutWhileLocked</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae12-183">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ae12-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ae12-184">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ae12-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8ae12-185">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ae12-185">Requirements</span></span>



| <span data-ttu-id="8ae12-186">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ae12-186">Requirement</span></span> | <span data-ttu-id="8ae12-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ae12-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ae12-188">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ae12-188">Minimum supported client</span></span><br/> | <span data-ttu-id="8ae12-189">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ae12-189">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8ae12-190">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ae12-190">Minimum supported server</span></span><br/> | <span data-ttu-id="8ae12-191">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ae12-191">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8ae12-192">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8ae12-192">Namespace</span></span><br/>                | <span data-ttu-id="8ae12-193">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="8ae12-193">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="8ae12-194">MOF</span><span class="sxs-lookup"><span data-stu-id="8ae12-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ae12-195"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8ae12-195"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8ae12-196">DLL</span><span class="sxs-lookup"><span data-stu-id="8ae12-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ae12-197"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ae12-197"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ae12-198">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ae12-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ae12-199">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="8ae12-199">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

