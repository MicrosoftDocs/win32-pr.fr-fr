---
description: Représente l’état configuré des paramètres de sécurité pour.
ms.assetid: c57ab966-591e-4dd9-87be-0d2b81611d5d
title: Classe Msvm_SecuritySettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecuritySettingData
- Msvm_SecuritySettingData.TpmEnabled
- Msvm_SecuritySettingData.KsdEnabled
- Msvm_SecuritySettingData.ShieldingRequested
- Msvm_SecuritySettingData.DataProtectionRequested
- Msvm_SecuritySettingData.EncryptStateAndVmMigrationTraffic
- Msvm_SecuritySettingData.VirtualizationBasedSecurityOptOut
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b7125e06ad4ce33e70a8cf84b24933e7390e7a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518500"
---
# <a name="msvm_securitysettingdata-class"></a><span data-ttu-id="7b57a-103">MSVM \_ SecuritySettingData, classe</span><span class="sxs-lookup"><span data-stu-id="7b57a-103">Msvm\_SecuritySettingData class</span></span>

<span data-ttu-id="7b57a-104">Représente l’état configuré des paramètres de sécurité pour un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7b57a-104">Represents the configured state of the security settings for a virtual machine.</span></span>

<span data-ttu-id="7b57a-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7b57a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b57a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b57a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecuritySettingData : CIM_SettingData
{
  boolean TpmEnabled;
  boolean KsdEnabled;
  boolean ShieldingRequested;
  boolean DataProtectionRequested;
  boolean EncryptStateAndVmMigrationTraffic;
  boolean VirtualizationBasedSecurityOptOut;
};
```

## <a name="members"></a><span data-ttu-id="7b57a-107">Membres</span><span class="sxs-lookup"><span data-stu-id="7b57a-107">Members</span></span>

<span data-ttu-id="7b57a-108">La classe **MSVM \_ SecuritySettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7b57a-108">The **Msvm\_SecuritySettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="7b57a-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7b57a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b57a-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7b57a-110">Properties</span></span>

<span data-ttu-id="7b57a-111">La classe **MSVM \_ SecuritySettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7b57a-111">The **Msvm\_SecuritySettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b57a-112">**DataProtectionRequested**</span><span class="sxs-lookup"><span data-stu-id="7b57a-112">**DataProtectionRequested**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b57a-113">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7b57a-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7b57a-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b57a-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b57a-115">Qualificateurs : [ **requis**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b57a-115">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b57a-116">**true** pour demander la protection des données pour une machine virtuelle ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="7b57a-116">**true** to request data protection for a VM; otherwise, **false**.</span></span> <span data-ttu-id="7b57a-117">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="7b57a-117">The default value is **false.**</span></span>

</dd> <dt>

<span data-ttu-id="7b57a-118">**EncryptStateAndVmMigrationTraffic**</span><span class="sxs-lookup"><span data-stu-id="7b57a-118">**EncryptStateAndVmMigrationTraffic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b57a-119">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7b57a-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7b57a-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b57a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b57a-121">Qualificateurs : [ **requis**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b57a-121">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b57a-122">**true** pour que l’État et le trafic de migration d’une machine virtuelle soient chiffrés ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="7b57a-122">**true** to have the state and migration traffic of a VM encrypted; otherwise, **false**.</span></span> <span data-ttu-id="7b57a-123">La valeur par défaut d’une machine virtuelle nouvellement créée est **false**.</span><span class="sxs-lookup"><span data-stu-id="7b57a-123">The default value for a newly-created VM is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="7b57a-124">**KsdEnabled**</span><span class="sxs-lookup"><span data-stu-id="7b57a-124">**KsdEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b57a-125">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7b57a-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7b57a-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b57a-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b57a-127">Qualificateurs : [ **requis**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b57a-127">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b57a-128">**true** pour activer un dispositif de stockage de clés (KSD) pour cet ordinateur virtuel ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="7b57a-128">**true** to enable a key storage device (KSD) for this virtual machine; otherwise, **false**.</span></span> <span data-ttu-id="7b57a-129">Une machine virtuelle nouvellement créée a un KSD de désactivation.</span><span class="sxs-lookup"><span data-stu-id="7b57a-129">A newly-created VM has a disable KSD.</span></span>

</dd> <dt>

<span data-ttu-id="7b57a-130">**ShieldingRequested**</span><span class="sxs-lookup"><span data-stu-id="7b57a-130">**ShieldingRequested**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b57a-131">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7b57a-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7b57a-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b57a-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b57a-133">Qualificateurs : [ **requis**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b57a-133">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b57a-134">**true** pour demander la protection d’une machine virtuelle ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="7b57a-134">**true** to request shielding for a VM; otherwise, **false**.</span></span> <span data-ttu-id="7b57a-135">Une machine virtuelle nouvellement créée présente l’état de la protection initiale **« false »**.</span><span class="sxs-lookup"><span data-stu-id="7b57a-135">A newly-created VM has an initial shielding requested state of **false**.</span></span>

</dd> <dt>

<span data-ttu-id="7b57a-136">**Définit**</span><span class="sxs-lookup"><span data-stu-id="7b57a-136">**TpmEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b57a-137">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7b57a-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7b57a-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b57a-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b57a-139">Qualificateurs : [ **requis**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b57a-139">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b57a-140">**true** pour activer un module de plateforme sécurisée (TPM) de plateforme sécurisée pour cet ordinateur virtuel ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="7b57a-140">**true** to enable a trusted platform nodule (TPM) for this virtual machine; otherwise, **false**.</span></span> <span data-ttu-id="7b57a-141">Une machine virtuelle qui vient d’être créée a un module de plateforme sécurisée désactivée.</span><span class="sxs-lookup"><span data-stu-id="7b57a-141">A newly-created VM has a disable TPM.</span></span>

</dd> <dt>

<span data-ttu-id="7b57a-142">**VirtualizationBasedSecurityOptOut**</span><span class="sxs-lookup"><span data-stu-id="7b57a-142">**VirtualizationBasedSecurityOptOut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b57a-143">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7b57a-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7b57a-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b57a-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b57a-145">Qualificateurs : [ **requis**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b57a-145">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b57a-146">**true** pour ne pas offrir de sécurité basée sur la virtualisation des machines virtuelles ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="7b57a-146">**true** to not offer a VM virtualization-based security; otherwise, **false**.</span></span> <span data-ttu-id="7b57a-147">Le paramètre par défaut pour l’état de désactivation de la machine virtuelle nouvellement créée est **false**.</span><span class="sxs-lookup"><span data-stu-id="7b57a-147">The default setting for a newly-crated VM's opt-out state is **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b57a-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b57a-148">Requirements</span></span>



| <span data-ttu-id="7b57a-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b57a-149">Requirement</span></span> | <span data-ttu-id="7b57a-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b57a-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b57a-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b57a-151">Minimum supported client</span></span><br/> | <span data-ttu-id="7b57a-152">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b57a-152">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7b57a-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b57a-153">Minimum supported server</span></span><br/> | <span data-ttu-id="7b57a-154">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7b57a-154">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7b57a-155">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7b57a-155">Namespace</span></span><br/>                | <span data-ttu-id="7b57a-156">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="7b57a-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7b57a-157">MOF</span><span class="sxs-lookup"><span data-stu-id="7b57a-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b57a-158"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b57a-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b57a-159">DLL</span><span class="sxs-lookup"><span data-stu-id="7b57a-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b57a-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7b57a-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7b57a-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b57a-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b57a-162">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="7b57a-162">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

