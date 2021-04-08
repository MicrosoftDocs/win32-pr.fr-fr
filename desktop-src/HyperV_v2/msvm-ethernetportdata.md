---
description: Classe abstraite qui représente les données de Runtime de port collectées par une extension de commutateur Ethernet.
ms.assetid: bc41ad1d-e7ab-4d04-96a8-26eb68ea6601
title: Classe Msvm_EthernetPortData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortData
- Msvm_EthernetPortData.InstanceID
- Msvm_EthernetPortData.Caption
- Msvm_EthernetPortData.Description
- Msvm_EthernetPortData.ElementName
- Msvm_EthernetPortData.SystemCreationClassName
- Msvm_EthernetPortData.SystemName
- Msvm_EthernetPortData.DeviceCreationClassName
- Msvm_EthernetPortData.DeviceID
- Msvm_EthernetPortData.CreationClassName
- Msvm_EthernetPortData.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 36167d4acad3c0da6b96efb9f9cc1fe58bd41a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865537"
---
# <a name="msvm_ethernetportdata-class"></a><span data-ttu-id="ba646-103">MSVM \_ EthernetPortData, classe</span><span class="sxs-lookup"><span data-stu-id="ba646-103">Msvm\_EthernetPortData class</span></span>

<span data-ttu-id="ba646-104">Classe abstraite qui représente les données de Runtime de port collectées par une extension de commutateur Ethernet.</span><span class="sxs-lookup"><span data-stu-id="ba646-104">An abstract class that represents port runtime data collected by an Ethernet switch extension.</span></span> <span data-ttu-id="ba646-105">Toutes les classes de données de port Ethernet doivent dériver de cette classe abstraite.</span><span class="sxs-lookup"><span data-stu-id="ba646-105">All Ethernet port data classes must derive from this abstract class.</span></span>

<span data-ttu-id="ba646-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ba646-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba646-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba646-107">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortData : CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string SystemCreationClassName;
  string SystemName;
  string DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string DeviceID;
  string CreationClassName;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="ba646-108">Membres</span><span class="sxs-lookup"><span data-stu-id="ba646-108">Members</span></span>

<span data-ttu-id="ba646-109">La classe **MSVM \_ EthernetPortData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ba646-109">The **Msvm\_EthernetPortData** class has these types of members:</span></span>

-   [<span data-ttu-id="ba646-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ba646-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ba646-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ba646-111">Properties</span></span>

<span data-ttu-id="ba646-112">La classe **MSVM \_ EthernetPortData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ba646-112">The **Msvm\_EthernetPortData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ba646-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ba646-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba646-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba646-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba646-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba646-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba646-116">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ba646-116">A short description of the object.</span></span> <span data-ttu-id="ba646-117">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ba646-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ba646-118">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ba646-118">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba646-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba646-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba646-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba646-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba646-121">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ba646-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ba646-122">Nom de la sous-classe utilisée lors de la création de cette instance de données de port.</span><span class="sxs-lookup"><span data-stu-id="ba646-122">The name of the subclass used in the creation of this port data instance.</span></span>

</dd> <dt>

<span data-ttu-id="ba646-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="ba646-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba646-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba646-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba646-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba646-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba646-126">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="ba646-126">A description of the object.</span></span> <span data-ttu-id="ba646-127">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ba646-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ba646-128">**DeviceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ba646-128">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba646-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba646-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba646-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba646-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba646-131">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ LogicalDevice CIM**](cim-logicaldevice.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ba646-131">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ba646-132">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="ba646-132">The scoping system's creation class name.</span></span> <span data-ttu-id="ba646-133">Cette propriété a toujours la valeur « MSVM \_ EthernetSwitchPort ».</span><span class="sxs-lookup"><span data-stu-id="ba646-133">This property is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="ba646-134">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="ba646-134">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba646-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba646-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba646-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba646-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba646-137">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ LogicalDevice CIM**](cim-logicaldevice.md).**DeviceID**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ba646-137">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**DeviceID**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ba646-138">ID d’appareil du port qui étend cette instance de données de port.</span><span class="sxs-lookup"><span data-stu-id="ba646-138">The Device ID of the port that scopes this port data instance.</span></span>

</dd> <dt>

<span data-ttu-id="ba646-139">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ba646-139">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba646-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba646-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba646-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba646-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba646-142">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ba646-142">A display name for the object.</span></span> <span data-ttu-id="ba646-143">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ba646-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ba646-144">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ba646-144">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba646-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba646-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba646-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba646-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba646-147">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="ba646-147">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ba646-148">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="ba646-148">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ba646-149">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ba646-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ba646-150">**Nom**</span><span class="sxs-lookup"><span data-stu-id="ba646-150">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba646-151">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba646-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba646-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba646-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba646-153">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ba646-153">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ba646-154">Chaîne qui identifie de façon unique cette instance de données de port dans l’étendue du commutateur et du port.</span><span class="sxs-lookup"><span data-stu-id="ba646-154">A string that uniquely identifies this port data instance within the scope of the switch and port.</span></span>

</dd> <dt>

<span data-ttu-id="ba646-155">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ba646-155">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba646-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba646-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba646-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba646-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba646-158">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ba646-158">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ba646-159">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="ba646-159">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="ba646-160">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ba646-160">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba646-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba646-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba646-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba646-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba646-163">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ba646-163">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ba646-164">Nom du commutateur virtuel qui s’étend à cette instance de données de port.</span><span class="sxs-lookup"><span data-stu-id="ba646-164">The name of the virtual switch that scopes this port data instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba646-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba646-165">Requirements</span></span>



| <span data-ttu-id="ba646-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba646-166">Requirement</span></span> | <span data-ttu-id="ba646-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba646-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba646-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba646-168">Minimum supported client</span></span><br/> | <span data-ttu-id="ba646-169">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba646-169">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ba646-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba646-170">Minimum supported server</span></span><br/> | <span data-ttu-id="ba646-171">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba646-171">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ba646-172">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ba646-172">Namespace</span></span><br/>                | <span data-ttu-id="ba646-173">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ba646-173">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ba646-174">MOF</span><span class="sxs-lookup"><span data-stu-id="ba646-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba646-175"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba646-175"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba646-176">DLL</span><span class="sxs-lookup"><span data-stu-id="ba646-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba646-177"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ba646-177"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

