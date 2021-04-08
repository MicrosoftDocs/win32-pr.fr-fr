---
title: Classe MDM_Policy_Result01_DeviceLock02
description: La \_ classe Result01 DeviceLock02 de la stratégie MDM \_ \_ représente les stratégies de verrouillage des appareils disponibles.
ms.assetid: 9aac25a8-8502-468f-9478-1ac4ccccaf0b
keywords:
- Classe MDM_Policy_Result01_DeviceLock02
- Classe MDM_Policy_Result01_DeviceLock02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DeviceLock02
- MDM_Policy_Result01_DeviceLock02.InstanceID
- MDM_Policy_Result01_DeviceLock02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa93236b99add5cb49e0b54aa10eab9e959ab01a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843634"
---
# <a name="mdm_policy_result01_devicelock02-class"></a><span data-ttu-id="90ef4-105">\_Classe DeviceLock02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="90ef4-105">MDM\_Policy\_Result01\_DeviceLock02 class</span></span>

<span data-ttu-id="90ef4-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="90ef4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="90ef4-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="90ef4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="90ef4-108">La **classe \_ \_ Result01 \_ DeviceLock02 de la stratégie MDM** représente les stratégies de verrouillage des appareils disponibles.</span><span class="sxs-lookup"><span data-stu-id="90ef4-108">The **MDM\_Policy\_Result01\_DeviceLock02** class represents the device lock policies available.</span></span>

<span data-ttu-id="90ef4-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="90ef4-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="90ef4-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90ef4-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DeviceLock02
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

## <a name="members"></a><span data-ttu-id="90ef4-111">Membres</span><span class="sxs-lookup"><span data-stu-id="90ef4-111">Members</span></span>

<span data-ttu-id="90ef4-112">La **classe \_ \_ Result01 \_ DeviceLock02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="90ef4-112">The **MDM\_Policy\_Result01\_DeviceLock02** class has these types of members:</span></span>

-   [<span data-ttu-id="90ef4-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="90ef4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="90ef4-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="90ef4-114">Properties</span></span>

<span data-ttu-id="90ef4-115">La **classe \_ \_ Result01 \_ DeviceLock02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="90ef4-115">The **MDM\_Policy\_Result01\_DeviceLock02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="90ef4-116">AllowScreenTimeoutWhileLockedUserConfig</span><span class="sxs-lookup"><span data-stu-id="90ef4-116">AllowScreenTimeoutWhileLockedUserConfig</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90ef4-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="90ef4-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="90ef4-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="90ef4-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="90ef4-119">AllowSimpleDevicePassword</span><span class="sxs-lookup"><span data-stu-id="90ef4-119">AllowSimpleDevicePassword</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-allowsimpledevicepassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90ef4-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="90ef4-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="90ef4-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="90ef4-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="90ef4-122">AlphanumericDevicePasswordRequired</span><span class="sxs-lookup"><span data-stu-id="90ef4-122">AlphanumericDevicePasswordRequired</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-alphanumericdevicepasswordrequired)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90ef4-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="90ef4-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="90ef4-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="90ef4-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="90ef4-125">DevicePasswordEnabled</span><span class="sxs-lookup"><span data-stu-id="90ef4-125">DevicePasswordEnabled</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordenabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90ef4-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="90ef4-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="90ef4-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="90ef4-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="90ef4-128">DevicePasswordExpiration</span><span class="sxs-lookup"><span data-stu-id="90ef4-128">DevicePasswordExpiration</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordexpiration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90ef4-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="90ef4-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="90ef4-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="90ef4-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="90ef4-131">DevicePasswordHistory</span><span class="sxs-lookup"><span data-stu-id="90ef4-131">DevicePasswordHistory</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90ef4-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="90ef4-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="90ef4-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="90ef4-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="90ef4-134">EnforceLockScreenAndLogonImage</span><span class="sxs-lookup"><span data-stu-id="90ef4-134">EnforceLockScreenAndLogonImage</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-enforcelockscreenandlogonimage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90ef4-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90ef4-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90ef4-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="90ef4-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="90ef4-137">EnforceLockScreenProvider</span><span class="sxs-lookup"><span data-stu-id="90ef4-137">EnforceLockScreenProvider</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90ef4-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90ef4-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90ef4-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="90ef4-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="90ef4-140">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="90ef4-140">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90ef4-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90ef4-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90ef4-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90ef4-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90ef4-143">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="90ef4-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="90ef4-144">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="90ef4-144">Identifies the name of the parent node.</span></span> <span data-ttu-id="90ef4-145">Pour cette classe, la chaîne est « DeviceLock ».</span><span class="sxs-lookup"><span data-stu-id="90ef4-145">For this class, the string is "DeviceLock".</span></span>

</dd> <dt>

[<span data-ttu-id="90ef4-146">MaxDevicePasswordFailedAttempts</span><span class="sxs-lookup"><span data-stu-id="90ef4-146">MaxDevicePasswordFailedAttempts</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxdevicepasswordfailedattempts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90ef4-147">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="90ef4-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="90ef4-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="90ef4-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="90ef4-149">MaxInactivityTimeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="90ef4-149">MaxInactivityTimeDeviceLock</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxinactivitytimedevicelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90ef4-150">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="90ef4-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="90ef4-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="90ef4-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="90ef4-152">MinDevicePasswordComplexCharacters</span><span class="sxs-lookup"><span data-stu-id="90ef4-152">MinDevicePasswordComplexCharacters</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordcomplexcharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90ef4-153">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="90ef4-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="90ef4-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="90ef4-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="90ef4-155">MinDevicePasswordLength</span><span class="sxs-lookup"><span data-stu-id="90ef4-155">MinDevicePasswordLength</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90ef4-156">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="90ef4-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="90ef4-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="90ef4-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="90ef4-158">MinimumPasswordAge</span><span class="sxs-lookup"><span data-stu-id="90ef4-158">MinimumPasswordAge</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-minimumpasswordage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90ef4-159">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="90ef4-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="90ef4-160">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="90ef4-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="90ef4-161">**ID**</span><span class="sxs-lookup"><span data-stu-id="90ef4-161">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90ef4-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90ef4-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90ef4-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90ef4-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90ef4-164">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="90ef4-164">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="90ef4-165">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="90ef4-165">Describes the full path to the parent node.</span></span> <span data-ttu-id="90ef4-166">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Result »</span><span class="sxs-lookup"><span data-stu-id="90ef4-166">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="90ef4-167">PreventLockScreenSlideShow</span><span class="sxs-lookup"><span data-stu-id="90ef4-167">PreventLockScreenSlideShow</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-preventlockscreenslideshow)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90ef4-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90ef4-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90ef4-169">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="90ef4-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="90ef4-170">ScreenTimeoutWhileLocked</span><span class="sxs-lookup"><span data-stu-id="90ef4-170">ScreenTimeoutWhileLocked</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90ef4-171">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="90ef4-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="90ef4-172">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="90ef4-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="90ef4-173">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90ef4-173">Requirements</span></span>



| <span data-ttu-id="90ef4-174">Condition requise</span><span class="sxs-lookup"><span data-stu-id="90ef4-174">Requirement</span></span> | <span data-ttu-id="90ef4-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="90ef4-175">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90ef4-176">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90ef4-176">Minimum supported client</span></span><br/> | <span data-ttu-id="90ef4-177">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="90ef4-177">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="90ef4-178">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90ef4-178">Minimum supported server</span></span><br/> | <span data-ttu-id="90ef4-179">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="90ef4-179">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="90ef4-180">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="90ef4-180">Namespace</span></span><br/>                | <span data-ttu-id="90ef4-181">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="90ef4-181">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="90ef4-182">MOF</span><span class="sxs-lookup"><span data-stu-id="90ef4-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90ef4-183"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="90ef4-183"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="90ef4-184">DLL</span><span class="sxs-lookup"><span data-stu-id="90ef4-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90ef4-185"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90ef4-185"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90ef4-186">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90ef4-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90ef4-187">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="90ef4-187">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

