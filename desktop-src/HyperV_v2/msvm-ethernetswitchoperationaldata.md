---
description: Représente les paramètres opérationnels du commutateur.
ms.assetid: f225d321-8f40-4e6c-b30d-8fab3f84761d
title: Classe Msvm_EthernetSwitchOperationalData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchOperationalData
- Msvm_EthernetSwitchOperationalData.InstanceID
- Msvm_EthernetSwitchOperationalData.Caption
- Msvm_EthernetSwitchOperationalData.Description
- Msvm_EthernetSwitchOperationalData.ElementName
- Msvm_EthernetSwitchOperationalData.SystemCreationClassName
- Msvm_EthernetSwitchOperationalData.SystemName
- Msvm_EthernetSwitchOperationalData.CreationClassName
- Msvm_EthernetSwitchOperationalData.Name
- Msvm_EthernetSwitchOperationalData.CurrentSwitchingMode
- Msvm_EthernetSwitchOperationalData.SupportedSwitchingModes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3d9aacd8380650ddaf2790aeacf4a2327b54f973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321241"
---
# <a name="msvm_ethernetswitchoperationaldata-class"></a><span data-ttu-id="83941-103">MSVM \_ EthernetSwitchOperationalData, classe</span><span class="sxs-lookup"><span data-stu-id="83941-103">Msvm\_EthernetSwitchOperationalData class</span></span>

<span data-ttu-id="83941-104">Représente les paramètres opérationnels du commutateur.</span><span class="sxs-lookup"><span data-stu-id="83941-104">Represents switch operational parameters.</span></span>

<span data-ttu-id="83941-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="83941-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="83941-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83941-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1D18CDCF-209E-4172-875D-6D208A0A8375"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Modes Supported "), AMENDMENT]
class Msvm_EthernetSwitchOperationalData : Msvm_EthernetSwitchData
{
  string InstanceID;
  string Caption = "Ethernet Switch Modes Supported";
  string Description = "Represents switch operational parameters.";
  string ElementName = "Ethernet Switch Modes Supported";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string CreationClassName = " Msvm_EthernetSwitchOperationalData";
  string Name;
  uint32 CurrentSwitchingMode = 1;
  uint32 SupportedSwitchingModes[] = {1};
};
```

## <a name="members"></a><span data-ttu-id="83941-107">Membres</span><span class="sxs-lookup"><span data-stu-id="83941-107">Members</span></span>

<span data-ttu-id="83941-108">La classe **MSVM \_ EthernetSwitchOperationalData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="83941-108">The **Msvm\_EthernetSwitchOperationalData** class has these types of members:</span></span>

-   [<span data-ttu-id="83941-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="83941-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="83941-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="83941-110">Properties</span></span>

<span data-ttu-id="83941-111">La classe **MSVM \_ EthernetSwitchOperationalData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="83941-111">The **Msvm\_EthernetSwitchOperationalData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="83941-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="83941-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83941-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="83941-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83941-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83941-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83941-115">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="83941-115">A short description of the object.</span></span> <span data-ttu-id="83941-116">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="83941-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="83941-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="83941-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83941-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="83941-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83941-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83941-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83941-120">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="83941-120">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="83941-121">Nom de la classe ou de la sous-classe utilisée dans la création de cette instance.</span><span class="sxs-lookup"><span data-stu-id="83941-121">The name of the class or subclass used in the creation of this instance.</span></span> <span data-ttu-id="83941-122">Cette propriété est héritée de [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="83941-122">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="83941-123">**CurrentSwitchingMode**</span><span class="sxs-lookup"><span data-stu-id="83941-123">**CurrentSwitchingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83941-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83941-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83941-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83941-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83941-126">Qualificateurs : **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="83941-126">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="83941-127">Mode de basculement actuel sur le commutateur.</span><span class="sxs-lookup"><span data-stu-id="83941-127">The current switching mode on the switch.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="83941-128">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="83941-128">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1Q"></span><span id="802.1q"></span>

<span data-ttu-id="83941-129">**802.1 q** (1)</span><span class="sxs-lookup"><span data-stu-id="83941-129">**802.1Q** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1Qbg"></span><span id="802.1qbg"></span><span id="802.1QBG"></span>

<span data-ttu-id="83941-130">**802.1 QBG** (2)</span><span class="sxs-lookup"><span data-stu-id="83941-130">**802.1Qbg** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1Qbh"></span><span id="802.1qbh"></span><span id="802.1QBH"></span>

<span data-ttu-id="83941-131">**802.1 QBH** (3)</span><span class="sxs-lookup"><span data-stu-id="83941-131">**802.1Qbh** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="83941-132">**Description**</span><span class="sxs-lookup"><span data-stu-id="83941-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83941-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="83941-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83941-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83941-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83941-135">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="83941-135">A description of the object.</span></span> <span data-ttu-id="83941-136">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="83941-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="83941-137">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="83941-137">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83941-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="83941-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83941-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83941-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83941-140">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="83941-140">A display name for the object.</span></span> <span data-ttu-id="83941-141">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="83941-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="83941-142">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="83941-142">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83941-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="83941-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83941-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83941-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83941-145">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="83941-145">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="83941-146">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="83941-146">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="83941-147">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="83941-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="83941-148">**Nom**</span><span class="sxs-lookup"><span data-stu-id="83941-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83941-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="83941-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83941-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83941-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83941-151">Qualificateurs : **clé**, **remplacement**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="83941-151">Qualifiers: **Key**, **Override**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="83941-152">Nom unique de la ressource.</span><span class="sxs-lookup"><span data-stu-id="83941-152">The unique name of the resource.</span></span> <span data-ttu-id="83941-153">Cette propriété est héritée de [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="83941-153">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="83941-154">**SupportedSwitchingModes**</span><span class="sxs-lookup"><span data-stu-id="83941-154">**SupportedSwitchingModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83941-155">Type de données : tableau **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83941-155">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="83941-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83941-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83941-157">Qualificateurs : **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="83941-157">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="83941-158">Modes de commutation pris en charge par le commutateur.</span><span class="sxs-lookup"><span data-stu-id="83941-158">The switching modes supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="83941-159">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="83941-159">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83941-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="83941-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83941-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83941-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83941-162">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="83941-162">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="83941-163">Nom de la classe de création du système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="83941-163">The hosting system's creation class name.</span></span> <span data-ttu-id="83941-164">Cette propriété est héritée de [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="83941-164">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="83941-165">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="83941-165">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83941-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="83941-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83941-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83941-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83941-168">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="83941-168">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="83941-169">Nom du commutateur virtuel auquel l’instance de ressource associée est liée.</span><span class="sxs-lookup"><span data-stu-id="83941-169">The name of the virtual switch to which the associated resource instance is bound.</span></span> <span data-ttu-id="83941-170">Cette propriété est héritée de [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="83941-170">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="83941-171">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83941-171">Requirements</span></span>



| <span data-ttu-id="83941-172">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83941-172">Requirement</span></span> | <span data-ttu-id="83941-173">Valeur</span><span class="sxs-lookup"><span data-stu-id="83941-173">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83941-174">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83941-174">Minimum supported client</span></span><br/> | <span data-ttu-id="83941-175">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83941-175">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="83941-176">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83941-176">Minimum supported server</span></span><br/> | <span data-ttu-id="83941-177">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83941-177">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="83941-178">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="83941-178">Namespace</span></span><br/>                | <span data-ttu-id="83941-179">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="83941-179">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="83941-180">MOF</span><span class="sxs-lookup"><span data-stu-id="83941-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83941-181"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83941-181"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="83941-182">DLL</span><span class="sxs-lookup"><span data-stu-id="83941-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83941-183"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="83941-183"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

