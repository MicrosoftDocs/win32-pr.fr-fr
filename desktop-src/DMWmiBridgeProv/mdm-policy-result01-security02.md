---
title: Classe MDM_Policy_Result01_Security02
description: La \_ classe Result01 Security02 de la stratégie MDM \_ \_ représente les stratégies de sécurité disponibles.
ms.assetid: e4f9bbeb-b542-454d-930b-0b4ac88fe189
keywords:
- Classe MDM_Policy_Result01_Security02
- Classe MDM_Policy_Result01_Security02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Security02
- MDM_Policy_Result01_Security02.InstanceID
- MDM_Policy_Result01_Security02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 959d5cbc9382b4bef0899f5b44d8ee2d171bd704
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032660"
---
# <a name="mdm_policy_result01_security02-class"></a><span data-ttu-id="80886-105">\_Classe Security02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="80886-105">MDM\_Policy\_Result01\_Security02 class</span></span>

<span data-ttu-id="80886-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="80886-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="80886-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="80886-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="80886-108">La **classe \_ \_ Result01 \_ Security02 de la stratégie MDM** représente les stratégies de sécurité disponibles.</span><span class="sxs-lookup"><span data-stu-id="80886-108">The **MDM\_Policy\_Result01\_Security02** class represents the security policies available.</span></span>

<span data-ttu-id="80886-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="80886-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="80886-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80886-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Security02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAddProvisioningPackage;
  sint32 AllowRemoveProvisioningPackage;
  sint32 ClearTPMIfNotReady;
  sint32 PreventAutomaticDeviceEncryptionForAzureADJoinedDevices;
  sint32 RequireDeviceEncryption;
  sint32 RequireProvisioningPackageSignature;
  sint32 RequireRetrieveHealthCertificateOnBoot;
};
```

## <a name="members"></a><span data-ttu-id="80886-111">Membres</span><span class="sxs-lookup"><span data-stu-id="80886-111">Members</span></span>

<span data-ttu-id="80886-112">La **classe \_ \_ Result01 \_ Security02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="80886-112">The **MDM\_Policy\_Result01\_Security02** class has these types of members:</span></span>

-   [<span data-ttu-id="80886-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="80886-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80886-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="80886-114">Properties</span></span>

<span data-ttu-id="80886-115">La **classe \_ \_ Result01 \_ Security02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="80886-115">The **MDM\_Policy\_Result01\_Security02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="80886-116">AllowAddProvisioningPackage</span><span class="sxs-lookup"><span data-stu-id="80886-116">AllowAddProvisioningPackage</span></span>](/windows/client-management/mdm/policy-csp-security#security-allowaddprovisioningpackage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="80886-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="80886-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="80886-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80886-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="80886-119">AllowRemoveProvisioningPackage</span><span class="sxs-lookup"><span data-stu-id="80886-119">AllowRemoveProvisioningPackage</span></span>](/windows/client-management/mdm/policy-csp-security#security-allowremoveprovisioningpackage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="80886-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="80886-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="80886-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80886-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="80886-122">ClearTPMIfNotReady</span><span class="sxs-lookup"><span data-stu-id="80886-122">ClearTPMIfNotReady</span></span>](/windows/client-management/mdm/policy-csp-security#security-cleartpmifnotready)
</dt> <dd> <dl> <dt>

<span data-ttu-id="80886-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="80886-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="80886-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80886-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="80886-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="80886-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80886-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80886-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80886-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80886-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80886-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="80886-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="80886-129">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="80886-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="80886-130">Pour cette classe, la chaîne est « Security ».</span><span class="sxs-lookup"><span data-stu-id="80886-130">For this class, the string is "Security".</span></span>

</dd> <dt>

<span data-ttu-id="80886-131">**ID**</span><span class="sxs-lookup"><span data-stu-id="80886-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80886-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80886-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80886-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80886-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80886-134">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="80886-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="80886-135">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="80886-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="80886-136">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Result »</span><span class="sxs-lookup"><span data-stu-id="80886-136">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="80886-137">PreventAutomaticDeviceEncryptionForAzureADJoinedDevices</span><span class="sxs-lookup"><span data-stu-id="80886-137">PreventAutomaticDeviceEncryptionForAzureADJoinedDevices</span></span>](/windows/client-management/mdm/policy-csp-security#security-preventautomaticdeviceencryptionforazureadjoineddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="80886-138">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="80886-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="80886-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80886-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="80886-140">RequireDeviceEncryption</span><span class="sxs-lookup"><span data-stu-id="80886-140">RequireDeviceEncryption</span></span>](/windows/client-management/mdm/policy-csp-security#security-requiredeviceencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="80886-141">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="80886-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="80886-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80886-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="80886-143">RequireProvisioningPackageSignature</span><span class="sxs-lookup"><span data-stu-id="80886-143">RequireProvisioningPackageSignature</span></span>](/windows/client-management/mdm/policy-csp-security#security-requireprovisioningpackagesignature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="80886-144">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="80886-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="80886-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80886-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="80886-146">RequireRetrieveHealthCertificateOnBoot</span><span class="sxs-lookup"><span data-stu-id="80886-146">RequireRetrieveHealthCertificateOnBoot</span></span>](/windows/client-management/mdm/policy-csp-security#security-requireretrievehealthcertificateonboot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="80886-147">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="80886-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="80886-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80886-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80886-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80886-149">Requirements</span></span>



| <span data-ttu-id="80886-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80886-150">Requirement</span></span> | <span data-ttu-id="80886-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="80886-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80886-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80886-152">Minimum supported client</span></span><br/> | <span data-ttu-id="80886-153">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80886-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="80886-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80886-154">Minimum supported server</span></span><br/> | <span data-ttu-id="80886-155">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="80886-155">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="80886-156">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="80886-156">Namespace</span></span><br/>                | <span data-ttu-id="80886-157">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="80886-157">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="80886-158">MOF</span><span class="sxs-lookup"><span data-stu-id="80886-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80886-159"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80886-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="80886-160">DLL</span><span class="sxs-lookup"><span data-stu-id="80886-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80886-161"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80886-161"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80886-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80886-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80886-163">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="80886-163">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

