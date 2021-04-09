---
description: Le \_ IRQResource Win32 &\# 160 ; La classe WMI représente un numéro d’interruption (IRQ) sur un système informatique exécutant Windows.
ms.assetid: bae0c28e-2b66-40ac-9679-b2dfe9269306
ms.tgt_platform: multiple
title: Classe Win32_IRQResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_IRQResource
- Win32_IRQResource.Availability
- Win32_IRQResource.Caption
- Win32_IRQResource.CreationClassName
- Win32_IRQResource.CSCreationClassName
- Win32_IRQResource.CSName
- Win32_IRQResource.Description
- Win32_IRQResource.Hardware
- Win32_IRQResource.InstallDate
- Win32_IRQResource.IRQNumber
- Win32_IRQResource.Name
- Win32_IRQResource.Shareable
- Win32_IRQResource.Status
- Win32_IRQResource.TriggerLevel
- Win32_IRQResource.TriggerType
- Win32_IRQResource.Vector
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cd02487fe166cd7ce55482eaca1339c8701f2b62
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110338"
---
# <a name="win32_irqresource-class"></a><span data-ttu-id="b2b31-103">\_Classe IRQResource Win32</span><span class="sxs-lookup"><span data-stu-id="b2b31-103">Win32\_IRQResource class</span></span>

<span data-ttu-id="b2b31-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ IRQResource** WMI représente un numéro d’interruption (IRQ) sur un système informatique exécutant Windows.  </span><span class="sxs-lookup"><span data-stu-id="b2b31-104">The **Win32\_IRQResource**  [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents an interrupt request line (IRQ) number on a computer system running Windows.</span></span> <span data-ttu-id="b2b31-105">Une requête d’interruption est un signal envoyé au processeur par un appareil ou un programme pour les événements critiques de temps.</span><span class="sxs-lookup"><span data-stu-id="b2b31-105">An interrupt request is a signal sent to the CPU by a device or program for time critical events.</span></span> <span data-ttu-id="b2b31-106">L’IRQ peut être basée sur le matériel ou sur le logiciel.</span><span class="sxs-lookup"><span data-stu-id="b2b31-106">IRQ can be hardware-based or software-based.</span></span>

<span data-ttu-id="b2b31-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b2b31-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b2b31-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="b2b31-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2b31-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2b31-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_IRQResource : CIM_IRQ
{
  uint16   Availability;
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  boolean  Hardware;
  datetime InstallDate;
  uint32   IRQNumber;
  string   Name;
  boolean  Shareable;
  string   Status;
  uint16   TriggerLevel;
  uint16   TriggerType;
  uint32   Vector;
};
```

## <a name="members"></a><span data-ttu-id="b2b31-110">Membres</span><span class="sxs-lookup"><span data-stu-id="b2b31-110">Members</span></span>

<span data-ttu-id="b2b31-111">La classe **Win32 \_ IRQResource** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b2b31-111">The **Win32\_IRQResource** class has these types of members:</span></span>

-   [<span data-ttu-id="b2b31-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b2b31-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b2b31-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b2b31-113">Properties</span></span>

<span data-ttu-id="b2b31-114">La classe **Win32 \_ IRQResource** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b2b31-114">The **Win32\_IRQResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2b31-115">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="b2b31-115">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b31-116">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b2b31-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2b31-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-118">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="b2b31-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="b2b31-119">Disponibilité de l’IRQ.</span><span class="sxs-lookup"><span data-stu-id="b2b31-119">Availability of the IRQ.</span></span>

<span data-ttu-id="b2b31-120">Cette propriété est héritée de l' [**\_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="b2b31-120">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="b2b31-121"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="b2b31-121"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="b2b31-122">Autres</span><span class="sxs-lookup"><span data-stu-id="b2b31-122">Other</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b2b31-123"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="b2b31-123"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b2b31-124">Unknown</span><span class="sxs-lookup"><span data-stu-id="b2b31-124">Unknown</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b2b31-125"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="b2b31-125"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b2b31-126">Disponible</span><span class="sxs-lookup"><span data-stu-id="b2b31-126">Available</span></span>

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="b2b31-127"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Disponible** (3)</span><span class="sxs-lookup"><span data-stu-id="b2b31-127"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b2b31-128">En cours d’utilisation ou non disponible</span><span class="sxs-lookup"><span data-stu-id="b2b31-128">In Use or Not Available</span></span>

</dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="b2b31-129"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**En cours d’utilisation/non disponible** (4)</span><span class="sxs-lookup"><span data-stu-id="b2b31-129"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b2b31-130">En cours d’utilisation et disponible ou partageable</span><span class="sxs-lookup"><span data-stu-id="b2b31-130">In Use and Available or Sharable</span></span>

</dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="b2b31-131"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**En cours d’utilisation et disponible/partageable** (5)</span><span class="sxs-lookup"><span data-stu-id="b2b31-131"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b2b31-132">En cours d’utilisation et disponible/partageable</span><span class="sxs-lookup"><span data-stu-id="b2b31-132">In use and available/sharable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b2b31-133">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b2b31-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b31-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b2b31-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2b31-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-136">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="b2b31-136">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b2b31-137">Description succincte de l’objet d’une chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="b2b31-137">Short description of the object a one-line string.</span></span>

<span data-ttu-id="b2b31-138">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b2b31-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2b31-139">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b2b31-139">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b31-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b2b31-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2b31-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-142">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b2b31-142">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b2b31-143">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="b2b31-143">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="b2b31-144">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="b2b31-144">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b2b31-145">Cette propriété est héritée de l' [**\_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="b2b31-145">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2b31-146">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b2b31-146">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b31-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b2b31-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2b31-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-149">Qualificateurs : [**propagé**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM CIM \_**](cim-computersystem.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b2b31-149">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b2b31-150">Nom de la classe de création de système d’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="b2b31-150">Name of the scoping computer system creation class.</span></span>

<span data-ttu-id="b2b31-151">Cette propriété est héritée de l' [**\_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="b2b31-151">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2b31-152">**CSName**</span><span class="sxs-lookup"><span data-stu-id="b2b31-152">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b31-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b2b31-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2b31-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-155">Qualificateurs : [**propagé**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM CIM \_**](cim-computersystem.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b2b31-155">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b2b31-156">Nom du système informatique d’étendue.</span><span class="sxs-lookup"><span data-stu-id="b2b31-156">Name of the scoping computer system.</span></span>

<span data-ttu-id="b2b31-157">Cette propriété est héritée de l' [**\_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="b2b31-157">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2b31-158">**Description**</span><span class="sxs-lookup"><span data-stu-id="b2b31-158">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b31-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b2b31-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2b31-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-161">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="b2b31-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b2b31-162">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b2b31-162">Textual description of the object.</span></span>

<span data-ttu-id="b2b31-163">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b2b31-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2b31-164">**Matériel**</span><span class="sxs-lookup"><span data-stu-id="b2b31-164">**Hardware**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b31-165">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b2b31-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2b31-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-167">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| System structures \| \_ InterfaceType descripteur \| InterfaceType")</span><span class="sxs-lookup"><span data-stu-id="b2b31-167">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Structures\|RESOURCE\_DESCRIPTOR\|InterfaceType")</span></span>
</dt> </dl>

<span data-ttu-id="b2b31-168">Si la **valeur est true**, l’interruption est basée sur le matériel ou les logiciels.</span><span class="sxs-lookup"><span data-stu-id="b2b31-168">If **TRUE**, the interrupt is hardware or software based.</span></span> <span data-ttu-id="b2b31-169">Une IRQ matérielle est un câble physique du périphérique vers la puce de contrôleur d’interruptions programmable (PIC) par le biais duquel l’UC peut être avertie des événements critiques du temps.</span><span class="sxs-lookup"><span data-stu-id="b2b31-169">A hardware IRQ is a physical wire from the peripheral to the programmable interrupt controller (PIC) chip through which the CPU can be notified of time-critical events.</span></span> <span data-ttu-id="b2b31-170">Certaines lignes IRQ sont réservées pour les appareils standard, tels que le clavier, les lecteurs de disquette et l’horloge système.</span><span class="sxs-lookup"><span data-stu-id="b2b31-170">Some IRQ lines are reserved for standard devices, such as the keyboard, floppy disk drives, and the system clock.</span></span> <span data-ttu-id="b2b31-171">Une interruption logicielle permet aux applications d’attirer l’attention du processeur.</span><span class="sxs-lookup"><span data-stu-id="b2b31-171">A software interrupt allows applications to get the attention of the processor.</span></span>

</dd> <dt>

<span data-ttu-id="b2b31-172">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b2b31-172">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b31-173">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b2b31-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2b31-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-175">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="b2b31-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b2b31-176">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b2b31-176">Date and time the object was installed.</span></span> <span data-ttu-id="b2b31-177">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="b2b31-177">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b2b31-178">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b2b31-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2b31-179">**Numéro IRQ**</span><span class="sxs-lookup"><span data-stu-id="b2b31-179">**IRQNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b31-180">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2b31-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2b31-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-182">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 001,1 "), [**clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b2b31-182">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.1"), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b2b31-183">Partie de la valeur de clé de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b2b31-183">Part of the object's key value.</span></span>

<span data-ttu-id="b2b31-184">Cette propriété est héritée de l' [**\_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="b2b31-184">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2b31-185">**Nom**</span><span class="sxs-lookup"><span data-stu-id="b2b31-185">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b31-186">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b2b31-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2b31-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-188">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b2b31-188">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b2b31-189">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="b2b31-189">Label by which the object is known.</span></span> <span data-ttu-id="b2b31-190">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="b2b31-190">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="b2b31-191">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b2b31-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2b31-192">**Partageable**</span><span class="sxs-lookup"><span data-stu-id="b2b31-192">**Shareable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b31-193">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b2b31-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2b31-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-195">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="b2b31-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="b2b31-196">Si la **valeur est true**, l’IRQ peut être partagée.</span><span class="sxs-lookup"><span data-stu-id="b2b31-196">If **TRUE**, the IRQ can be shared.</span></span>

<span data-ttu-id="b2b31-197">Cette propriété est héritée de l' [**\_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="b2b31-197">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2b31-198">**État**</span><span class="sxs-lookup"><span data-stu-id="b2b31-198">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b31-199">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b2b31-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2b31-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-201">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="b2b31-201">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b2b31-202">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b2b31-202">Current status of the object.</span></span> <span data-ttu-id="b2b31-203">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="b2b31-203">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b2b31-204">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="b2b31-204">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b2b31-205">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="b2b31-205">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b2b31-206">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="b2b31-206">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b2b31-207">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="b2b31-207">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b2b31-208">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b2b31-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b2b31-209">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2b31-209">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b2b31-210">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="b2b31-210">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b2b31-211">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="b2b31-211">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b2b31-212">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="b2b31-212">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b2b31-213">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="b2b31-213">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b2b31-214">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="b2b31-214">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b2b31-215">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="b2b31-215">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b2b31-216">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="b2b31-216">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b2b31-217">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="b2b31-217">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b2b31-218">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="b2b31-218">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b2b31-219">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="b2b31-219">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b2b31-220">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="b2b31-220">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b2b31-221">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="b2b31-221">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b2b31-222">**TriggerLevel**</span><span class="sxs-lookup"><span data-stu-id="b2b31-222">**TriggerLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b31-223">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b2b31-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2b31-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-225">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Ressource système DMTF IRQ Info \| 001,3»)</span><span class="sxs-lookup"><span data-stu-id="b2b31-225">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource IRQ Info\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="b2b31-226">Niveau de déclenchement d’IRQ indiquant si l’interruption est déclenchée par le signal matériel passant à High (4) ou Low (3).</span><span class="sxs-lookup"><span data-stu-id="b2b31-226">IRQ trigger level indicating whether the interrupt is triggered by the hardware signal going high (4) or low (3).</span></span>

<span data-ttu-id="b2b31-227">Cette propriété est héritée de l' [**\_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="b2b31-227">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b2b31-228">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="b2b31-228">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b2b31-229">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="b2b31-229">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_Low"></span><span id="active_low"></span><span id="ACTIVE_LOW"></span>

<span data-ttu-id="b2b31-230">**Faible actif** (3)</span><span class="sxs-lookup"><span data-stu-id="b2b31-230">**Active Low** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_High"></span><span id="active_high"></span><span id="ACTIVE_HIGH"></span>

<span data-ttu-id="b2b31-231">**Élevé actif** (4)</span><span class="sxs-lookup"><span data-stu-id="b2b31-231">**Active High** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b2b31-232">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="b2b31-232">**TriggerType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b31-233">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b2b31-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-234">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2b31-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-235">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 001,3 "," MIF. \|Ressource système DMTF IRQ Info \| 001,2»)</span><span class="sxs-lookup"><span data-stu-id="b2b31-235">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.3", "MIF.DMTF\|System Resource IRQ Info\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="b2b31-236">Type de déclencheur IRQ indiquant si des interruptions déclenchées par le bord (4) ou déclenchées par le niveau (3) se produisent.</span><span class="sxs-lookup"><span data-stu-id="b2b31-236">IRQ trigger type indicating whether edge-triggered (4) or level-triggered (3) interrupts occur.</span></span>

<span data-ttu-id="b2b31-237">Cette propriété est héritée de l' [**\_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="b2b31-237">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b2b31-238">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="b2b31-238">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b2b31-239">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="b2b31-239">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>

<span data-ttu-id="b2b31-240">**Niveau** (3)</span><span class="sxs-lookup"><span data-stu-id="b2b31-240">**Level** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Edge"></span><span id="edge"></span><span id="EDGE"></span>

<span data-ttu-id="b2b31-241">**Edge** (4)</span><span class="sxs-lookup"><span data-stu-id="b2b31-241">**Edge** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b2b31-242">**Vecteur**</span><span class="sxs-lookup"><span data-stu-id="b2b31-242">**Vector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b31-243">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2b31-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2b31-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b31-245">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api de \| structures système \| cm niveau d’interruption de [**\_ \_ \_ descripteur de ressource partielle**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor) \| \| ")</span><span class="sxs-lookup"><span data-stu-id="b2b31-245">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Structures\|[**CM\_PARTIAL\_RESOURCE\_DESCRIPTOR**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor)\|Interrupt\|Level")</span></span>
</dt> </dl>

<span data-ttu-id="b2b31-246">Vecteur de la ressource IRQ Windows.</span><span class="sxs-lookup"><span data-stu-id="b2b31-246">Vector of the Windows IRQ resource.</span></span> <span data-ttu-id="b2b31-247">Un vecteur contient l’adresse mémoire de la fonction qui s’exécute une fois que la demande d’interruption est acceptée par le processeur.</span><span class="sxs-lookup"><span data-stu-id="b2b31-247">A vector contains the memory address to the function that will execute once the interrupt request is acknowledged by the CPU.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2b31-248">Notes</span><span class="sxs-lookup"><span data-stu-id="b2b31-248">Remarks</span></span>

<span data-ttu-id="b2b31-249">La classe **Win32 \_ IRQResource** est dérivée de l' [**\_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="b2b31-249">The **Win32\_IRQResource** class is derived from [**CIM\_IRQ**](cim-irq.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2b31-250">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2b31-250">Requirements</span></span>



| <span data-ttu-id="b2b31-251">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2b31-251">Requirement</span></span> | <span data-ttu-id="b2b31-252">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2b31-252">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2b31-253">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2b31-253">Minimum supported client</span></span><br/> | <span data-ttu-id="b2b31-254">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b2b31-254">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b2b31-255">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2b31-255">Minimum supported server</span></span><br/> | <span data-ttu-id="b2b31-256">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2b31-256">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b2b31-257">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b2b31-257">Namespace</span></span><br/>                | <span data-ttu-id="b2b31-258">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="b2b31-258">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b2b31-259">MOF</span><span class="sxs-lookup"><span data-stu-id="b2b31-259">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2b31-260"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2b31-260"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2b31-261">DLL</span><span class="sxs-lookup"><span data-stu-id="b2b31-261">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2b31-262"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2b31-262"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2b31-263">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2b31-263">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2b31-264">**\_IRQ CIM**</span><span class="sxs-lookup"><span data-stu-id="b2b31-264">**CIM\_IRQ**</span></span>](cim-irq.md)
</dt> <dt>

[<span data-ttu-id="b2b31-265">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="b2b31-265">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

