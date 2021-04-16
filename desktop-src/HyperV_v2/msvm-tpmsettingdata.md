---
description: Représente l’état configuré du périphérique TPM.
ms.assetid: 948ccb47-3626-48f1-b18f-ef1d05978b21
title: Classe Msvm_TPMSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TPMSettingData
- Msvm_TPMSettingData.Shielded
- Msvm_TPMSettingData.DataProtected
- Msvm_TPMSettingData.EnabledState
- Msvm_TPMSettingData.KeyProtector
- Msvm_TPMSettingData.LastKnownGoodKeyProtector
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8a14f50f01212129ed34cc7e45ee28facbdb991f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527669"
---
# <a name="msvm_tpmsettingdata-class"></a><span data-ttu-id="1cafa-103">MSVM \_ TPMSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="1cafa-103">Msvm\_TPMSettingData class</span></span>

<span data-ttu-id="1cafa-104">Représente l’état configuré du périphérique TPM.</span><span class="sxs-lookup"><span data-stu-id="1cafa-104">Represents the configured state of the TPM device.</span></span>

<span data-ttu-id="1cafa-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="1cafa-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cafa-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1cafa-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TPMSettingData : CIM_ResourceAllocationSettingData
{
  boolean Shielded = FALSE;
  boolean DataProtected = FALSE;
  uint16  EnabledState = 3;
  uint8   KeyProtector[];
  uint8   LastKnownGoodKeyProtector[];
};
```

## <a name="members"></a><span data-ttu-id="1cafa-107">Membres</span><span class="sxs-lookup"><span data-stu-id="1cafa-107">Members</span></span>

<span data-ttu-id="1cafa-108">La classe **MSVM \_ TPMSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1cafa-108">The **Msvm\_TPMSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="1cafa-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1cafa-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1cafa-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1cafa-110">Properties</span></span>

<span data-ttu-id="1cafa-111">La classe **MSVM \_ TPMSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="1cafa-111">The **Msvm\_TPMSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1cafa-112">**DataProtected**</span><span class="sxs-lookup"><span data-stu-id="1cafa-112">**DataProtected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cafa-113">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="1cafa-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1cafa-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cafa-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1cafa-115">Qualificateurs : [ **requis**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1cafa-115">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1cafa-116">**true** pour définir une stratégie de protection des données d’une machine virtuelle ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="1cafa-116">**true** to set a policy to protect a VM's data; otherwise, **false**.</span></span> <span data-ttu-id="1cafa-117">Un module de plateforme sécurisée nouvellement créé est désactivé. l’état initial de la protection des données est donc **false**.</span><span class="sxs-lookup"><span data-stu-id="1cafa-117">A newly created TPM is disabled, so the initial data protection state is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="1cafa-118">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="1cafa-118">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cafa-119">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1cafa-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1cafa-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cafa-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1cafa-121">Qualificateurs : [ **requis**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1cafa-121">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1cafa-122">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="1cafa-122">The enabled and disabled states of an element.</span></span> <span data-ttu-id="1cafa-123">La valeur par défaut est **Disabled**.</span><span class="sxs-lookup"><span data-stu-id="1cafa-123">The default value is **Disabled**.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1cafa-124">**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="1cafa-124">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1cafa-125">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="1cafa-125">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1cafa-126">**Keyprotector**</span><span class="sxs-lookup"><span data-stu-id="1cafa-126">**KeyProtector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cafa-127">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="1cafa-127">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="1cafa-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cafa-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1cafa-129">Qualificateurs : [**obligatoire**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**</span><span class="sxs-lookup"><span data-stu-id="1cafa-129">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**</span></span>
</dt> </dl>

<span data-ttu-id="1cafa-130">Protecteur de clé du client du service Guardian hôte.</span><span class="sxs-lookup"><span data-stu-id="1cafa-130">The key protector from Host Guardian Service client.</span></span>

</dd> <dt>

<span data-ttu-id="1cafa-131">**LastKnownGoodKeyProtector**</span><span class="sxs-lookup"><span data-stu-id="1cafa-131">**LastKnownGoodKeyProtector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cafa-132">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="1cafa-132">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="1cafa-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cafa-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1cafa-134">Qualificateurs : [**obligatoire**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**</span><span class="sxs-lookup"><span data-stu-id="1cafa-134">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**</span></span>
</dt> </dl>

<span data-ttu-id="1cafa-135">Le dernier protecteur de clé correct connu a correctement chiffré l’état du périphérique TPM lors du dernier démarrage de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="1cafa-135">The last known good key protector successfully encrypted TPM device state in the last VM boot.</span></span>

<span data-ttu-id="1cafa-136">Cette propriété est en lecture seule pour le client WMI et peut uniquement être modifiée par le périphérique TPM de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="1cafa-136">This property is read-only for the WMI client, and can only be modified by the VM TPM device.</span></span>

</dd> <dt>

<span data-ttu-id="1cafa-137">**Protégé**</span><span class="sxs-lookup"><span data-stu-id="1cafa-137">**Shielded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cafa-138">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="1cafa-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1cafa-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cafa-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1cafa-140">Qualificateurs : [ **requis**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1cafa-140">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1cafa-141">**true** pour définir une stratégie qui protège un ordinateur virtuel ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="1cafa-141">**true** to define a policy that shields a virtual machine; otherwise, **false**.</span></span> <span data-ttu-id="1cafa-142">Un module de plateforme sécurisée nouvellement créé est désactivé, donc l’état de la protection initiale est **false**.</span><span class="sxs-lookup"><span data-stu-id="1cafa-142">A newly created TPM is disabled, so the initial shielding state is **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1cafa-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cafa-143">Requirements</span></span>



| <span data-ttu-id="1cafa-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1cafa-144">Requirement</span></span> | <span data-ttu-id="1cafa-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cafa-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cafa-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cafa-146">Minimum supported client</span></span><br/> | <span data-ttu-id="1cafa-147">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cafa-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="1cafa-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cafa-148">Minimum supported server</span></span><br/> | <span data-ttu-id="1cafa-149">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1cafa-149">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="1cafa-150">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="1cafa-150">End of client support</span></span><br/>    | <span data-ttu-id="1cafa-151">Windows 10</span><span class="sxs-lookup"><span data-stu-id="1cafa-151">Windows 10</span></span><br/>                                                                                   |
| <span data-ttu-id="1cafa-152">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="1cafa-152">End of server support</span></span><br/>    | <span data-ttu-id="1cafa-153">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1cafa-153">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="1cafa-154">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1cafa-154">Namespace</span></span><br/>                | <span data-ttu-id="1cafa-155">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="1cafa-155">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1cafa-156">MOF</span><span class="sxs-lookup"><span data-stu-id="1cafa-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1cafa-157"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1cafa-157"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1cafa-158">DLL</span><span class="sxs-lookup"><span data-stu-id="1cafa-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cafa-159"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1cafa-159"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1cafa-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cafa-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cafa-161">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="1cafa-161">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

