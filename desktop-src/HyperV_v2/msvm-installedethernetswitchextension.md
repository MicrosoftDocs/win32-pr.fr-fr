---
description: Représente une instance d’un composant d’extension installé sur un système hôte.
ms.assetid: ad24fb08-36af-42a8-a910-63eae54fa5b8
title: Classe Msvm_InstalledEthernetSwitchExtension
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InstalledEthernetSwitchExtension
- Msvm_InstalledEthernetSwitchExtension.InstanceID
- Msvm_InstalledEthernetSwitchExtension.Caption
- Msvm_InstalledEthernetSwitchExtension.Description
- Msvm_InstalledEthernetSwitchExtension.ElementName
- Msvm_InstalledEthernetSwitchExtension.InstallDate
- Msvm_InstalledEthernetSwitchExtension.Name
- Msvm_InstalledEthernetSwitchExtension.OperationalStatus
- Msvm_InstalledEthernetSwitchExtension.StatusDescriptions
- Msvm_InstalledEthernetSwitchExtension.Status
- Msvm_InstalledEthernetSwitchExtension.HealthState
- Msvm_InstalledEthernetSwitchExtension.CommunicationStatus
- Msvm_InstalledEthernetSwitchExtension.DetailedStatus
- Msvm_InstalledEthernetSwitchExtension.OperatingStatus
- Msvm_InstalledEthernetSwitchExtension.PrimaryStatus
- Msvm_InstalledEthernetSwitchExtension.ExtensionType
- Msvm_InstalledEthernetSwitchExtension.Vendor
- Msvm_InstalledEthernetSwitchExtension.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bfbe0b1996751613c31913447cb0d200d71b8168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521398"
---
# <a name="msvm_installedethernetswitchextension-class"></a><span data-ttu-id="a3f67-103">MSVM \_ InstalledEthernetSwitchExtension, classe</span><span class="sxs-lookup"><span data-stu-id="a3f67-103">Msvm\_InstalledEthernetSwitchExtension class</span></span>

<span data-ttu-id="a3f67-104">Représente une instance d’un composant d’extension installé sur un système hôte.</span><span class="sxs-lookup"><span data-stu-id="a3f67-104">Represents an instance of an extension component installed on a host system.</span></span>

<span data-ttu-id="a3f67-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a3f67-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3f67-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3f67-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InstalledEthernetSwitchExtension : CIM_ManagedSystemElement
{
  string   InstanceID;
  string   Caption = " System Virtual Ethernet Switch Extension";
  string   Description = "Microsoft NDIS Packet Capture Filter Driver";
  string   ElementName = "Microsoft NDIS Capture";
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint8    ExtensionType;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="a3f67-107">Membres</span><span class="sxs-lookup"><span data-stu-id="a3f67-107">Members</span></span>

<span data-ttu-id="a3f67-108">La classe **MSVM \_ InstalledEthernetSwitchExtension** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a3f67-108">The **Msvm\_InstalledEthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="a3f67-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a3f67-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a3f67-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a3f67-110">Properties</span></span>

<span data-ttu-id="a3f67-111">La classe **MSVM \_ InstalledEthernetSwitchExtension** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a3f67-111">The **Msvm\_InstalledEthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a3f67-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a3f67-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3f67-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a3f67-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a3f67-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-115">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="a3f67-115">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="a3f67-116">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a3f67-116">A short description of the object.</span></span> <span data-ttu-id="a3f67-117">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a3f67-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a3f67-118">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="a3f67-118">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3f67-119">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a3f67-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a3f67-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3f67-121">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="a3f67-121">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="a3f67-122">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="a3f67-122">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a3f67-123">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a3f67-123">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a3f67-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="a3f67-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3f67-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a3f67-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a3f67-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3f67-127">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="a3f67-127">A description of the object.</span></span> <span data-ttu-id="a3f67-128">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a3f67-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a3f67-129">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="a3f67-129">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3f67-130">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a3f67-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a3f67-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3f67-132">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="a3f67-132">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="a3f67-133">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="a3f67-133">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a3f67-134">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a3f67-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a3f67-135">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a3f67-135">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3f67-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a3f67-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a3f67-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3f67-138">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a3f67-138">A display name for the object.</span></span> <span data-ttu-id="a3f67-139">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a3f67-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a3f67-140">**ExtensionType**</span><span class="sxs-lookup"><span data-stu-id="a3f67-140">**ExtensionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3f67-141">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="a3f67-141">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a3f67-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3f67-143">Indique le type du composant d’extension.</span><span class="sxs-lookup"><span data-stu-id="a3f67-143">Indicates the type of the extension component.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a3f67-144">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="a3f67-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Capture"></span><span id="capture"></span><span id="CAPTURE"></span>

<span data-ttu-id="a3f67-145">**Capture** (1)</span><span class="sxs-lookup"><span data-stu-id="a3f67-145">**Capture** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>

<span data-ttu-id="a3f67-146">**Filtre** (2)</span><span class="sxs-lookup"><span data-stu-id="a3f67-146">**Filter** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Forwarding"></span><span id="forwarding"></span><span id="FORWARDING"></span>

<span data-ttu-id="a3f67-147">**Transfert** (3)</span><span class="sxs-lookup"><span data-stu-id="a3f67-147">**Forwarding** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Monitoring"></span><span id="monitoring"></span><span id="MONITORING"></span>

<span data-ttu-id="a3f67-148">**Analyse** (4)</span><span class="sxs-lookup"><span data-stu-id="a3f67-148">**Monitoring** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Native"></span><span id="native"></span><span id="NATIVE"></span>

<span data-ttu-id="a3f67-149">**Natif** (5)</span><span class="sxs-lookup"><span data-stu-id="a3f67-149">**Native** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a3f67-150">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="a3f67-150">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3f67-151">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a3f67-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a3f67-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3f67-153">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="a3f67-153">The current health of the element.</span></span> <span data-ttu-id="a3f67-154">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="a3f67-154">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="a3f67-155">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="a3f67-155">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="a3f67-156">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="a3f67-156">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="a3f67-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a3f67-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3f67-158">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a3f67-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a3f67-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3f67-160">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a3f67-160">The date and time when the object was installed.</span></span> <span data-ttu-id="a3f67-161">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="a3f67-161">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="a3f67-162">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a3f67-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a3f67-163">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a3f67-163">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3f67-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a3f67-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a3f67-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-166">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="a3f67-166">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a3f67-167">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="a3f67-167">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a3f67-168">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a3f67-168">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a3f67-169">**Nom**</span><span class="sxs-lookup"><span data-stu-id="a3f67-169">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3f67-170">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a3f67-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a3f67-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-172">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a3f67-172">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a3f67-173">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="a3f67-173">The label by which the object is known.</span></span> <span data-ttu-id="a3f67-174">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a3f67-174">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a3f67-175">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="a3f67-175">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3f67-176">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a3f67-176">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a3f67-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3f67-178">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="a3f67-178">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="a3f67-179">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="a3f67-179">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a3f67-180">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a3f67-180">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a3f67-181">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="a3f67-181">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3f67-182">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a3f67-182">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a3f67-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3f67-184">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a3f67-184">The current statuses of the object.</span></span> <span data-ttu-id="a3f67-185">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau a toujours la valeur 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="a3f67-185">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="a3f67-186">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="a3f67-186">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3f67-187">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a3f67-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a3f67-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3f67-189">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="a3f67-189">Provides high level status information.</span></span> <span data-ttu-id="a3f67-190">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="a3f67-190">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="a3f67-191">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="a3f67-191">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a3f67-192">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a3f67-192">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a3f67-193">**État**</span><span class="sxs-lookup"><span data-stu-id="a3f67-193">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3f67-194">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a3f67-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a3f67-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3f67-196">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a3f67-196">The current status of the object.</span></span> <span data-ttu-id="a3f67-197">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a3f67-197">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a3f67-198">OK</span><span class="sxs-lookup"><span data-stu-id="a3f67-198">"OK"</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-199"><span id="OK"></span><span id="ok"></span>**Bien**</span><span class="sxs-lookup"><span data-stu-id="a3f67-199"><span id="OK"></span><span id="ok"></span>**OK**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-200"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreurs**</span><span class="sxs-lookup"><span data-stu-id="a3f67-200"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-201"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré**</span><span class="sxs-lookup"><span data-stu-id="a3f67-201"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Connue**</span><span class="sxs-lookup"><span data-stu-id="a3f67-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-203"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Échec prévu**</span><span class="sxs-lookup"><span data-stu-id="a3f67-203"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Pred Fail**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-204"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarr**</span><span class="sxs-lookup"><span data-stu-id="a3f67-204"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-205"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt**</span><span class="sxs-lookup"><span data-stu-id="a3f67-205"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-206"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Services**</span><span class="sxs-lookup"><span data-stu-id="a3f67-206"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-207"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Trop sollicité**</span><span class="sxs-lookup"><span data-stu-id="a3f67-207"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-208"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**Non récupéré**</span><span class="sxs-lookup"><span data-stu-id="a3f67-208"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**NonRecover**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-209"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact**</span><span class="sxs-lookup"><span data-stu-id="a3f67-209"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-210"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Communication perdue**</span><span class="sxs-lookup"><span data-stu-id="a3f67-210"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Lost Comm**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a3f67-211">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a3f67-211">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3f67-212">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="a3f67-212">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a3f67-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3f67-214">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="a3f67-214">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="a3f67-215">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau est toujours défini sur « OK ».</span><span class="sxs-lookup"><span data-stu-id="a3f67-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="a3f67-216">**Fournisseur**</span><span class="sxs-lookup"><span data-stu-id="a3f67-216">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3f67-217">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a3f67-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a3f67-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3f67-219">Indique le fournisseur qui fournit l’extension.</span><span class="sxs-lookup"><span data-stu-id="a3f67-219">Indicates the vendor providing the extension.</span></span>

</dd> <dt>

<span data-ttu-id="a3f67-220">**Version**</span><span class="sxs-lookup"><span data-stu-id="a3f67-220">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3f67-221">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a3f67-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3f67-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a3f67-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3f67-223">Version de l’extension dans un format « major. minor », par exemple « 2,0 ».</span><span class="sxs-lookup"><span data-stu-id="a3f67-223">The version of the extension in a format of "major.minor", for example "2.0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a3f67-224">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3f67-224">Requirements</span></span>



| <span data-ttu-id="a3f67-225">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3f67-225">Requirement</span></span> | <span data-ttu-id="a3f67-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3f67-226">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3f67-227">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3f67-227">Minimum supported client</span></span><br/> | <span data-ttu-id="a3f67-228">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a3f67-228">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a3f67-229">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3f67-229">Minimum supported server</span></span><br/> | <span data-ttu-id="a3f67-230">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a3f67-230">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a3f67-231">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a3f67-231">Namespace</span></span><br/>                | <span data-ttu-id="a3f67-232">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="a3f67-232">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a3f67-233">MOF</span><span class="sxs-lookup"><span data-stu-id="a3f67-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a3f67-234"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a3f67-234"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a3f67-235">DLL</span><span class="sxs-lookup"><span data-stu-id="a3f67-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3f67-236"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a3f67-236"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

