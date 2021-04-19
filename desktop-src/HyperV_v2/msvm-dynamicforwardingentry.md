---
description: Représente une entrée dans la base de données de transfert (filtrage) associée au service de pontage transparent.
ms.assetid: 3C9FAE99-9543-4A6A-B578-3F4626598DB3
title: Classe Msvm_DynamicForwardingEntry
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DynamicForwardingEntry
- Msvm_DynamicForwardingEntry.InstanceID
- Msvm_DynamicForwardingEntry.Caption
- Msvm_DynamicForwardingEntry.Description
- Msvm_DynamicForwardingEntry.ElementName
- Msvm_DynamicForwardingEntry.InstallDate
- Msvm_DynamicForwardingEntry.Name
- Msvm_DynamicForwardingEntry.OperationalStatus
- Msvm_DynamicForwardingEntry.StatusDescriptions
- Msvm_DynamicForwardingEntry.Status
- Msvm_DynamicForwardingEntry.HealthState
- Msvm_DynamicForwardingEntry.CommunicationStatus
- Msvm_DynamicForwardingEntry.DetailedStatus
- Msvm_DynamicForwardingEntry.OperatingStatus
- Msvm_DynamicForwardingEntry.PrimaryStatus
- Msvm_DynamicForwardingEntry.SystemCreationClassName
- Msvm_DynamicForwardingEntry.SystemName
- Msvm_DynamicForwardingEntry.ServiceCreationClassName
- Msvm_DynamicForwardingEntry.ServiceName
- Msvm_DynamicForwardingEntry.CreationClassName
- Msvm_DynamicForwardingEntry.MACAddress
- Msvm_DynamicForwardingEntry.DynamicStatus
- Msvm_DynamicForwardingEntry.VlanId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f14f8b3a8f5f62e1a474b3d7b7f832b6acd530f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528225"
---
# <a name="msvm_dynamicforwardingentry-class"></a><span data-ttu-id="9fa6f-103">MSVM \_ DynamicForwardingEntry, classe</span><span class="sxs-lookup"><span data-stu-id="9fa6f-103">Msvm\_DynamicForwardingEntry class</span></span>

<span data-ttu-id="9fa6f-104">Représente une entrée dans la base de données de transfert (filtrage) associée au service de pontage transparent.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-104">Represents an entry in the forwarding (filtering) database that is associated with the transparent bridging service.</span></span> <span data-ttu-id="9fa6f-105">L’entrée est faible pour le service, comme spécifié par [**MSVM \_ TransparentBridgingDynamicForwarding**](msvm-transparentbridgingdynamicforwarding.md).</span><span class="sxs-lookup"><span data-stu-id="9fa6f-105">The entry is weak to the service, as specified by [**Msvm\_TransparentBridgingDynamicForwarding**](msvm-transparentbridgingdynamicforwarding.md).</span></span>

<span data-ttu-id="9fa6f-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fa6f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9fa6f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DynamicForwardingEntry : CIM_DynamicForwardingEntry
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   SystemCreationClassName;
  string   SystemName;
  string   ServiceCreationClassName;
  string   ServiceName;
  string   CreationClassName;
  string   MACAddress;
  uint16   DynamicStatus;
  uint16   VlanId;
};
```

## <a name="members"></a><span data-ttu-id="9fa6f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="9fa6f-108">Members</span></span>

<span data-ttu-id="9fa6f-109">La classe **MSVM \_ DynamicForwardingEntry** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9fa6f-109">The **Msvm\_DynamicForwardingEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="9fa6f-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9fa6f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9fa6f-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9fa6f-111">Properties</span></span>

<span data-ttu-id="9fa6f-112">La classe **MSVM \_ DynamicForwardingEntry** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-112">The **Msvm\_DynamicForwardingEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9fa6f-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa6f-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9fa6f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-116">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="9fa6f-116">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="9fa6f-117">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-117">A short description of the object.</span></span> <span data-ttu-id="9fa6f-118">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9fa6f-118">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9fa6f-119">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-119">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa6f-120">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9fa6f-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fa6f-122">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-122">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="9fa6f-123">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-123">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9fa6f-124">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9fa6f-124">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9fa6f-125">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-125">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa6f-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9fa6f-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-128">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="9fa6f-128">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="9fa6f-129">Nom de la classe ou de la sous-classe utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-129">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="9fa6f-130">Quand elle est utilisée avec les autres propriétés de clé de cette classe, cette propriété autorise l’identification unique de toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-130">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="9fa6f-131">Cette propriété est héritée de la [**\_ DynamicForwardingEntry CIM**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9fa6f-131">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9fa6f-132">**Description**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa6f-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9fa6f-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fa6f-135">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="9fa6f-135">A description of the object.</span></span> <span data-ttu-id="9fa6f-136">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9fa6f-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9fa6f-137">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-137">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa6f-138">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9fa6f-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fa6f-140">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-140">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="9fa6f-141">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-141">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9fa6f-142">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9fa6f-142">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9fa6f-143">**DynamicStatus**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-143">**DynamicStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa6f-144">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9fa6f-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fa6f-146">État de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-146">The status of the entry.</span></span> <span data-ttu-id="9fa6f-147">Cette propriété est héritée de la [**\_ DynamicForwardingEntry CIM**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9fa6f-147">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="9fa6f-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="9fa6f-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-149"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Non valide** (2)</span><span class="sxs-lookup"><span data-stu-id="9fa6f-149"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Invalid** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-150"><span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>**Appris** (3)</span><span class="sxs-lookup"><span data-stu-id="9fa6f-150"><span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>**Learned** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-151"><span id="Self"></span><span id="self"></span><span id="SELF"></span>**Self** (4)</span><span class="sxs-lookup"><span data-stu-id="9fa6f-151"><span id="Self"></span><span id="self"></span><span id="SELF"></span>**Self** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-152"><span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>**Mgmt** (5)</span><span class="sxs-lookup"><span data-stu-id="9fa6f-152"><span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>**Mgmt** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9fa6f-153">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-153">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa6f-154">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9fa6f-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fa6f-156">Nom complet de l’élément.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-156">A display name for the element.</span></span> <span data-ttu-id="9fa6f-157">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9fa6f-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9fa6f-158">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-158">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa6f-159">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9fa6f-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fa6f-161">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-161">The current health of the element.</span></span> <span data-ttu-id="9fa6f-162">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5 (« OK »).</span><span class="sxs-lookup"><span data-stu-id="9fa6f-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 ("OK").</span></span>

</dd> <dt>

<span data-ttu-id="9fa6f-163">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-163">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa6f-164">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-164">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9fa6f-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fa6f-166">Renseigné automatiquement lorsque la machine virtuelle est créée.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-166">Automatically populated when the virtual machine is created.</span></span> <span data-ttu-id="9fa6f-167">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9fa6f-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9fa6f-168">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-168">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa6f-169">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9fa6f-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-171">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-171">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9fa6f-172">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-172">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9fa6f-173">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9fa6f-173">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9fa6f-174">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-174">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa6f-175">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9fa6f-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-177">Qualificateurs : **clé**, **MaxLen** (12)</span><span class="sxs-lookup"><span data-stu-id="9fa6f-177">Qualifiers: **Key**, **MaxLen** (12)</span></span>
</dt> </dl>

<span data-ttu-id="9fa6f-178">Adresse MAC de monodiffusion pour laquelle le service de pontage transparent dispose d’informations de transfert et de filtrage.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-178">Unicast MAC address for which the transparent bridging service has forwarding and filtering information.</span></span> <span data-ttu-id="9fa6f-179">L’adresse MAC est mise en forme en tant que 12 chiffres hexadécimaux (par exemple, « 010203040506 »), chaque paire représentant l’un des six octets de l’adresse MAC dans l’ordre de bit « canonique » conformément à la RFC 2469.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-179">The MAC address is formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in "canonical" bit order according to RFC 2469.</span></span> <span data-ttu-id="9fa6f-180">Cette propriété est héritée de la [**\_ DynamicForwardingEntry CIM**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9fa6f-180">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9fa6f-181">**Nom**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-181">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa6f-182">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9fa6f-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fa6f-184">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-184">The label by which the object is known.</span></span> <span data-ttu-id="9fa6f-185">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9fa6f-185">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9fa6f-186">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-186">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa6f-187">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9fa6f-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fa6f-189">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="9fa6f-189">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="9fa6f-190">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9fa6f-191">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9fa6f-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9fa6f-192">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-192">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa6f-193">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-193">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9fa6f-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fa6f-195">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-195">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9fa6f-196">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-196">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa6f-197">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9fa6f-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fa6f-199">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-199">Provides high level status information.</span></span> <span data-ttu-id="9fa6f-200">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-200">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="9fa6f-201">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-201">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9fa6f-202">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9fa6f-202">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9fa6f-203">**ServiceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-203">**ServiceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa6f-204">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-205">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9fa6f-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-206">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="9fa6f-206">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="9fa6f-207">**CreationClassName** du service d’étendue.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-207">The scoping service's **CreationClassName**.</span></span> <span data-ttu-id="9fa6f-208">Cette propriété est héritée de la [**\_ DynamicForwardingEntry CIM**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9fa6f-208">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9fa6f-209">**FormName**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-209">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa6f-210">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9fa6f-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-212">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="9fa6f-212">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="9fa6f-213">Nom du service d’étendue.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-213">The scoping service's name.</span></span> <span data-ttu-id="9fa6f-214">Cette propriété est héritée de la [**\_ DynamicForwardingEntry CIM**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9fa6f-214">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9fa6f-215">**État**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-215">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa6f-216">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9fa6f-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fa6f-218">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-218">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9fa6f-219">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-219">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa6f-220">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-220">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-221">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9fa6f-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fa6f-222">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-222">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9fa6f-223">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-223">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa6f-224">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-225">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9fa6f-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-226">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="9fa6f-226">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="9fa6f-227">**CreationClassName** du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-227">The scoping system's **CreationClassName**.</span></span> <span data-ttu-id="9fa6f-228">Cette propriété est héritée de la [**\_ DynamicForwardingEntry CIM**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9fa6f-228">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9fa6f-229">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-229">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa6f-230">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9fa6f-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-232">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="9fa6f-232">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="9fa6f-233">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-233">The scoping system's name.</span></span> <span data-ttu-id="9fa6f-234">Cette propriété est héritée de la [**\_ DynamicForwardingEntry CIM**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9fa6f-234">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9fa6f-235">**VlanId**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-235">**VlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa6f-236">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-236">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9fa6f-237">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9fa6f-237">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9fa6f-238">Identificateur de réseau local virtuel associé à cette entrée.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-238">The virtual LAN identifier associated with this entry.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9fa6f-239">Notes</span><span class="sxs-lookup"><span data-stu-id="9fa6f-239">Remarks</span></span>

<span data-ttu-id="9fa6f-240">L’accès à la classe **MSVM \_ DynamicForwardingEntry** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="9fa6f-240">Access to the **Msvm\_DynamicForwardingEntry** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9fa6f-241">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="9fa6f-241">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="9fa6f-242">Exemples</span><span class="sxs-lookup"><span data-stu-id="9fa6f-242">Examples</span></span>

<span data-ttu-id="9fa6f-243">Consultez [interrogation d’objets de mise en réseau](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9fa6f-243">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9fa6f-244">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9fa6f-244">Requirements</span></span>



| <span data-ttu-id="9fa6f-245">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9fa6f-245">Requirement</span></span> | <span data-ttu-id="9fa6f-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="9fa6f-246">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fa6f-247">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9fa6f-247">Minimum supported client</span></span><br/> | <span data-ttu-id="9fa6f-248">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9fa6f-248">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9fa6f-249">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9fa6f-249">Minimum supported server</span></span><br/> | <span data-ttu-id="9fa6f-250">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9fa6f-250">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9fa6f-251">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9fa6f-251">Namespace</span></span><br/>                | <span data-ttu-id="9fa6f-252">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9fa6f-252">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9fa6f-253">MOF</span><span class="sxs-lookup"><span data-stu-id="9fa6f-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9fa6f-254"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9fa6f-254"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9fa6f-255">DLL</span><span class="sxs-lookup"><span data-stu-id="9fa6f-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fa6f-256"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9fa6f-256"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9fa6f-257">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9fa6f-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fa6f-258">**\_DYNAMICFORWARDINGENTRY CIM**</span><span class="sxs-lookup"><span data-stu-id="9fa6f-258">**CIM\_DynamicForwardingEntry**</span></span>](cim-dynamicforwardingentry.md)
</dt> <dt>

<span data-ttu-id="9fa6f-259">[**\_DYNAMICFORWARDINGENTRY CIM**](/previous-versions//cc136814(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9fa6f-259">[**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85))</span></span>
</dt> </dl>

 

