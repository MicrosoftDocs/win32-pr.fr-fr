---
description: Classe abstraite qui représente une ressource pour une instance donnée d’un commutateur Ethernet.
ms.assetid: 5ae1be2a-8d59-4efe-a4ae-7cac1727cfa2
title: Classe Msvm_EthernetSwitchData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchData
- Msvm_EthernetSwitchData.InstanceID
- Msvm_EthernetSwitchData.Caption
- Msvm_EthernetSwitchData.Description
- Msvm_EthernetSwitchData.ElementName
- Msvm_EthernetSwitchData.SystemCreationClassName
- Msvm_EthernetSwitchData.SystemName
- Msvm_EthernetSwitchData.CreationClassName
- Msvm_EthernetSwitchData.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dca2e4e01266a0a7da0f3ec85a86615406625f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520989"
---
# <a name="msvm_ethernetswitchdata-class"></a><span data-ttu-id="f1b7c-103">MSVM \_ EthernetSwitchData, classe</span><span class="sxs-lookup"><span data-stu-id="f1b7c-103">Msvm\_EthernetSwitchData class</span></span>

<span data-ttu-id="f1b7c-104">Classe abstraite qui représente une ressource pour une instance donnée d’un commutateur Ethernet.</span><span class="sxs-lookup"><span data-stu-id="f1b7c-104">Abstract class that represents a resource for a given instance of an Ethernet switch.</span></span>

<span data-ttu-id="f1b7c-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f1b7c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1b7c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1b7c-106">Syntax</span></span>

``` syntax
[Abstract, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchData : CIM_ManagedElement
{
  string InstanceID;
  string Caption = "Ethernet Switch Bandwidth data";
  string Description = "Represents the switch bandwidth resource status.";
  string ElementName = "Ethernet Switch Bandwidth data";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string CreationClassName = " Msvm_EthernetSwitchBandwidthData";
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="f1b7c-107">Membres</span><span class="sxs-lookup"><span data-stu-id="f1b7c-107">Members</span></span>

<span data-ttu-id="f1b7c-108">La classe **MSVM \_ EthernetSwitchData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f1b7c-108">The **Msvm\_EthernetSwitchData** class has these types of members:</span></span>

-   [<span data-ttu-id="f1b7c-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f1b7c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1b7c-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f1b7c-110">Properties</span></span>

<span data-ttu-id="f1b7c-111">La classe **MSVM \_ EthernetSwitchData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="f1b7c-111">The **Msvm\_EthernetSwitchData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1b7c-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f1b7c-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1b7c-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1b7c-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1b7c-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1b7c-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1b7c-115">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f1b7c-115">A short description of the object.</span></span> <span data-ttu-id="f1b7c-116">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f1b7c-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f1b7c-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f1b7c-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1b7c-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1b7c-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1b7c-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1b7c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1b7c-120">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f1b7c-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f1b7c-121">Nom de la classe ou de la sous-classe utilisée dans la création de cette instance.</span><span class="sxs-lookup"><span data-stu-id="f1b7c-121">The name of the class or subclass used in the creation of this instance.</span></span>

</dd> <dt>

<span data-ttu-id="f1b7c-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="f1b7c-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1b7c-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1b7c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1b7c-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1b7c-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1b7c-125">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="f1b7c-125">A description of the object.</span></span> <span data-ttu-id="f1b7c-126">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f1b7c-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f1b7c-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f1b7c-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1b7c-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1b7c-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1b7c-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1b7c-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1b7c-130">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f1b7c-130">A display name for the object.</span></span> <span data-ttu-id="f1b7c-131">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f1b7c-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f1b7c-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f1b7c-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1b7c-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1b7c-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1b7c-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1b7c-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1b7c-135">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="f1b7c-135">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f1b7c-136">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="f1b7c-136">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f1b7c-137">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f1b7c-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f1b7c-138">**Nom**</span><span class="sxs-lookup"><span data-stu-id="f1b7c-138">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1b7c-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1b7c-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1b7c-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1b7c-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1b7c-141">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f1b7c-141">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f1b7c-142">Nom unique de la ressource.</span><span class="sxs-lookup"><span data-stu-id="f1b7c-142">The unique name of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="f1b7c-143">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f1b7c-143">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1b7c-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1b7c-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1b7c-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1b7c-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1b7c-146">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f1b7c-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f1b7c-147">Nom de la classe de création du système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="f1b7c-147">The hosting system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="f1b7c-148">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f1b7c-148">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1b7c-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1b7c-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1b7c-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1b7c-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1b7c-151">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f1b7c-151">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f1b7c-152">Nom du commutateur virtuel auquel l’instance de ressource associée est liée.</span><span class="sxs-lookup"><span data-stu-id="f1b7c-152">The name of the virtual switch to which the associated resource instance is bound.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f1b7c-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1b7c-153">Requirements</span></span>



| <span data-ttu-id="f1b7c-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1b7c-154">Requirement</span></span> | <span data-ttu-id="f1b7c-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1b7c-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1b7c-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1b7c-156">Minimum supported client</span></span><br/> | <span data-ttu-id="f1b7c-157">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1b7c-157">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f1b7c-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1b7c-158">Minimum supported server</span></span><br/> | <span data-ttu-id="f1b7c-159">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1b7c-159">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f1b7c-160">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f1b7c-160">Namespace</span></span><br/>                | <span data-ttu-id="f1b7c-161">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="f1b7c-161">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f1b7c-162">MOF</span><span class="sxs-lookup"><span data-stu-id="f1b7c-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1b7c-163"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1b7c-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1b7c-164">DLL</span><span class="sxs-lookup"><span data-stu-id="f1b7c-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1b7c-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f1b7c-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

