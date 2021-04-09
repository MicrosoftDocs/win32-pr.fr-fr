---
description: La \_ classe d’IRQ CIM représente une ligne de demande d’interruption (IRQ) d’architecture Intel.
ms.assetid: d72d4914-c57b-496d-a9fe-d8f5b522504c
ms.tgt_platform: multiple
title: Classe CIM_IRQ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_IRQ
- CIM_IRQ.Caption
- CIM_IRQ.Description
- CIM_IRQ.InstallDate
- CIM_IRQ.Name
- CIM_IRQ.Status
- CIM_IRQ.Availability
- CIM_IRQ.CreationClassName
- CIM_IRQ.CSCreationClassName
- CIM_IRQ.CSName
- CIM_IRQ.IRQNumber
- CIM_IRQ.Shareable
- CIM_IRQ.TriggerLevel
- CIM_IRQ.TriggerType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 03a336caa02c766160fe6501f91b28f06a872ecb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861246"
---
# <a name="cim_irq-class"></a><span data-ttu-id="430db-103">\_Classe d’IRQ CIM</span><span class="sxs-lookup"><span data-stu-id="430db-103">CIM\_IRQ class</span></span>

<span data-ttu-id="430db-104">La classe d' **\_ IRQ CIM** représente une ligne de demande d’interruption (IRQ) d’architecture Intel.</span><span class="sxs-lookup"><span data-stu-id="430db-104">The **CIM\_IRQ** class represents an Intel architecture interrupt request line (IRQ).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="430db-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="430db-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="430db-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="430db-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="430db-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="430db-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="430db-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="430db-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="430db-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="430db-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C51A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_IRQ : CIM_SystemResource
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  uint32   IRQNumber;
  boolean  Shareable;
  uint16   TriggerLevel;
  uint16   TriggerType;
};
```

## <a name="members"></a><span data-ttu-id="430db-110">Membres</span><span class="sxs-lookup"><span data-stu-id="430db-110">Members</span></span>

<span data-ttu-id="430db-111">La classe d' **\_ IRQ CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="430db-111">The **CIM\_IRQ** class has these types of members:</span></span>

-   [<span data-ttu-id="430db-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="430db-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="430db-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="430db-113">Properties</span></span>

<span data-ttu-id="430db-114">La classe d' **\_ IRQ CIM** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="430db-114">The **CIM\_IRQ** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="430db-115">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="430db-115">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="430db-116">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="430db-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="430db-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="430db-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="430db-118">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="430db-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="430db-119">Disponibilité de l’IRQ.</span><span class="sxs-lookup"><span data-stu-id="430db-119">Availability of the IRQ.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="430db-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="430db-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="430db-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="430db-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="430db-122"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Disponible** (3)</span><span class="sxs-lookup"><span data-stu-id="430db-122"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="430db-123"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**En cours d’utilisation/non disponible** (4)</span><span class="sxs-lookup"><span data-stu-id="430db-123"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="430db-124"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**En cours d’utilisation et disponible/partageable** (5)</span><span class="sxs-lookup"><span data-stu-id="430db-124"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="430db-125">En cours d’utilisation et disponible/partageable</span><span class="sxs-lookup"><span data-stu-id="430db-125">In use and available/sharable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="430db-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="430db-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="430db-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="430db-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="430db-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="430db-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="430db-129">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="430db-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="430db-130">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="430db-130">A short textual description of the object.</span></span>

<span data-ttu-id="430db-131">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="430db-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="430db-132">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="430db-132">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="430db-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="430db-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="430db-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="430db-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="430db-135">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="430db-135">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="430db-136">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="430db-136">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="430db-137">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="430db-137">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="430db-138">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="430db-138">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="430db-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="430db-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="430db-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="430db-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="430db-141">Qualificateurs : [**propagé**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM CIM \_**](cim-computersystem.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="430db-141">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="430db-142">Portée du nom de la classe de création du système de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="430db-142">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="430db-143">**CSName**</span><span class="sxs-lookup"><span data-stu-id="430db-143">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="430db-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="430db-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="430db-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="430db-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="430db-146">Qualificateurs : [**propagé**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM CIM \_**](cim-computersystem.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="430db-146">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="430db-147">Nom du système d’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="430db-147">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="430db-148">**Description**</span><span class="sxs-lookup"><span data-stu-id="430db-148">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="430db-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="430db-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="430db-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="430db-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="430db-151">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="430db-151">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="430db-152">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="430db-152">A textual description of the object.</span></span>

<span data-ttu-id="430db-153">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="430db-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="430db-154">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="430db-154">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="430db-155">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="430db-155">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="430db-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="430db-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="430db-157">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="430db-157">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="430db-158">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="430db-158">Indicates when the object was installed.</span></span> <span data-ttu-id="430db-159">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="430db-159">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="430db-160">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="430db-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="430db-161">**Numéro IRQ**</span><span class="sxs-lookup"><span data-stu-id="430db-161">**IRQNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="430db-162">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="430db-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="430db-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="430db-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="430db-164">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 001,1 "), [**clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="430db-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.1"), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="430db-165">Partie de la valeur de clé de l’objet, numéro IRQ.</span><span class="sxs-lookup"><span data-stu-id="430db-165">Part of the object's key value, IRQ number.</span></span>

</dd> <dt>

<span data-ttu-id="430db-166">**Nom**</span><span class="sxs-lookup"><span data-stu-id="430db-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="430db-167">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="430db-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="430db-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="430db-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="430db-169">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="430db-169">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="430db-170">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="430db-170">Label by which the object is known.</span></span> <span data-ttu-id="430db-171">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="430db-171">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="430db-172">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="430db-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="430db-173">**Partageable**</span><span class="sxs-lookup"><span data-stu-id="430db-173">**Shareable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="430db-174">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="430db-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="430db-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="430db-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="430db-176">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="430db-176">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="430db-177">Si la **valeur est true**, l’IRQ peut être partagée.</span><span class="sxs-lookup"><span data-stu-id="430db-177">If **TRUE**, the IRQ can be shared.</span></span>

</dd> <dt>

<span data-ttu-id="430db-178">**État**</span><span class="sxs-lookup"><span data-stu-id="430db-178">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="430db-179">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="430db-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="430db-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="430db-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="430db-181">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="430db-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="430db-182">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="430db-182">String that indicates the current status of the object.</span></span> <span data-ttu-id="430db-183">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="430db-183">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="430db-184">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="430db-184">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="430db-185">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="430db-185">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="430db-186">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="430db-186">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="430db-187">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="430db-187">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="430db-188">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="430db-188">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="430db-189">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="430db-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="430db-190">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="430db-190">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="430db-191">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="430db-191">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="430db-192">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="430db-192">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="430db-193">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="430db-193">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="430db-194">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="430db-194">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="430db-195">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="430db-195">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="430db-196">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="430db-196">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="430db-197">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="430db-197">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="430db-198">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="430db-198">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="430db-199">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="430db-199">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="430db-200">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="430db-200">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="430db-201">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="430db-201">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="430db-202">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="430db-202">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="430db-203">**TriggerLevel**</span><span class="sxs-lookup"><span data-stu-id="430db-203">**TriggerLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="430db-204">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="430db-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="430db-205">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="430db-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="430db-206">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Ressource système DMTF IRQ Info \| 001,3»)</span><span class="sxs-lookup"><span data-stu-id="430db-206">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource IRQ Info\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="430db-207">Indique si l’interruption est déclenchée par le signal matériel qui passe en haut ou en bas.</span><span class="sxs-lookup"><span data-stu-id="430db-207">Indicates whether the interruption is triggered by the hardware signal going high or low.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="430db-208">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="430db-208">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="430db-209">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="430db-209">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_Low"></span><span id="active_low"></span><span id="ACTIVE_LOW"></span>

<span data-ttu-id="430db-210">**Faible actif** (3)</span><span class="sxs-lookup"><span data-stu-id="430db-210">**Active Low** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_High"></span><span id="active_high"></span><span id="ACTIVE_HIGH"></span>

<span data-ttu-id="430db-211">**Élevé actif** (4)</span><span class="sxs-lookup"><span data-stu-id="430db-211">**Active High** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="430db-212">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="430db-212">**TriggerType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="430db-213">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="430db-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="430db-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="430db-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="430db-215">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 001,3 "," MIF. \|Ressource système DMTF IRQ Info \| 001,2»)</span><span class="sxs-lookup"><span data-stu-id="430db-215">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.3", "MIF.DMTF\|System Resource IRQ Info\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="430db-216">Type d’interruption qui peut se produire.</span><span class="sxs-lookup"><span data-stu-id="430db-216">Type of interruption that can occur.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="430db-217">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="430db-217">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="430db-218">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="430db-218">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>

<span data-ttu-id="430db-219">**Niveau** (3)</span><span class="sxs-lookup"><span data-stu-id="430db-219">**Level** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Edge"></span><span id="edge"></span><span id="EDGE"></span>

<span data-ttu-id="430db-220">**Edge** (4)</span><span class="sxs-lookup"><span data-stu-id="430db-220">**Edge** (4)</span></span>


<span data-ttu-id="430db-221"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="430db-221"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="430db-222">Notes</span><span class="sxs-lookup"><span data-stu-id="430db-222">Remarks</span></span>

<span data-ttu-id="430db-223">La classe d' **\_ IRQ CIM** est dérivée de la [**\_ SystemResource CIM**](cim-systemresource.md). WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="430db-223">The **CIM\_IRQ** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).WMI does not implement this class.</span></span> <span data-ttu-id="430db-224">Consultez [classes Win32](win32-provider.md) pour les classes dérivées de l' **\_ IRQ CIM**.</span><span class="sxs-lookup"><span data-stu-id="430db-224">See [Win32 Classes](win32-provider.md) for classes derived from **CIM\_IRQ**.</span></span>

<span data-ttu-id="430db-225">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="430db-225">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="430db-226">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="430db-226">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="430db-227">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="430db-227">Requirements</span></span>



| <span data-ttu-id="430db-228">Condition requise</span><span class="sxs-lookup"><span data-stu-id="430db-228">Requirement</span></span> | <span data-ttu-id="430db-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="430db-229">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="430db-230">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="430db-230">Minimum supported client</span></span><br/> | <span data-ttu-id="430db-231">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="430db-231">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="430db-232">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="430db-232">Minimum supported server</span></span><br/> | <span data-ttu-id="430db-233">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="430db-233">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="430db-234">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="430db-234">Namespace</span></span><br/>                | <span data-ttu-id="430db-235">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="430db-235">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="430db-236">MOF</span><span class="sxs-lookup"><span data-stu-id="430db-236">MOF</span></span><br/>                      | <dl> <span data-ttu-id="430db-237"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="430db-237"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="430db-238">DLL</span><span class="sxs-lookup"><span data-stu-id="430db-238">DLL</span></span><br/>                      | <dl> <span data-ttu-id="430db-239"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="430db-239"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="430db-240">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="430db-240">See also</span></span>

<dl> <dt>

[<span data-ttu-id="430db-241">**\_SYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="430db-241">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> </dl>

 

