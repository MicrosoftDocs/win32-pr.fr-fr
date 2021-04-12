---
description: Une \_ classe ComputerSystem CIM représente une collection spéciale d' \_ instances ManagedSystemElement CIM.
ms.assetid: c4fd0598-3cb3-428f-ad39-a14232ef7c17
ms.tgt_platform: multiple
title: CIM_ComputerSystem, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystem
- CIM_ComputerSystem.Caption
- CIM_ComputerSystem.Description
- CIM_ComputerSystem.InstallDate
- CIM_ComputerSystem.Status
- CIM_ComputerSystem.CreationClassName
- CIM_ComputerSystem.Name
- CIM_ComputerSystem.PrimaryOwnerContact
- CIM_ComputerSystem.PrimaryOwnerName
- CIM_ComputerSystem.Roles
- CIM_ComputerSystem.NameFormat
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4645a8d4b2440b0b102658d3eca74d825d774dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483536"
---
# <a name="cim_computersystem-class-cimwin32-wmi-providers"></a><span data-ttu-id="821c4-103">CIM_ComputerSystem, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="821c4-103">CIM_ComputerSystem class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="821c4-104">Une **classe \_ ComputerSystem CIM** représente une collection spéciale d' [**instances \_ ManagedSystemElement CIM**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="821c4-104">A **CIM\_ComputerSystem** class represents a special collection of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) instances.</span></span> <span data-ttu-id="821c4-105">Cette collection fournit des fonctionnalités d’ordinateur et sert de point d’agrégation pour associer un ou plusieurs des éléments suivants : système de fichiers, système d’exploitation, processeur et mémoire (stockage volatile et non volatile).</span><span class="sxs-lookup"><span data-stu-id="821c4-105">This collection provides computer capabilities and serves as an aggregation point to associate one or more of the following elements: file system, operating system, processor and memory (volatile and non-volatile storage).</span></span> <span data-ttu-id="821c4-106">Cette classe est dérivée [**du \_ système CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="821c4-106">This class is derived from [**CIM\_System**](cim-system.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="821c4-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="821c4-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="821c4-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="821c4-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="821c4-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="821c4-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="821c4-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="821c4-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="821c4-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="821c4-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C525-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ComputerSystem : CIM_System
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  string   Roles[];
  string   NameFormat;
};
```

## <a name="members"></a><span data-ttu-id="821c4-112">Membres</span><span class="sxs-lookup"><span data-stu-id="821c4-112">Members</span></span>

<span data-ttu-id="821c4-113">La classe de l' **\_ ComputerSystem CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="821c4-113">The **CIM\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="821c4-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="821c4-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="821c4-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="821c4-115">Properties</span></span>

<span data-ttu-id="821c4-116">La classe de l' **\_ ComputerSystem CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="821c4-116">The **CIM\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="821c4-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="821c4-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="821c4-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="821c4-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="821c4-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="821c4-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="821c4-120">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="821c4-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="821c4-121">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="821c4-121">A short textual description of the object.</span></span>

<span data-ttu-id="821c4-122">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="821c4-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="821c4-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="821c4-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="821c4-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="821c4-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="821c4-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="821c4-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="821c4-126">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="821c4-126">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="821c4-127">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="821c4-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="821c4-128">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="821c4-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="821c4-129">Cette propriété est héritée [**du \_ système CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="821c4-129">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="821c4-130">**Description**</span><span class="sxs-lookup"><span data-stu-id="821c4-130">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="821c4-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="821c4-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="821c4-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="821c4-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="821c4-133">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="821c4-133">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="821c4-134">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="821c4-134">A textual description of the object.</span></span>

<span data-ttu-id="821c4-135">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="821c4-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="821c4-136">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="821c4-136">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="821c4-137">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="821c4-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="821c4-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="821c4-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="821c4-139">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="821c4-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="821c4-140">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="821c4-140">Indicates when the object was installed.</span></span> <span data-ttu-id="821c4-141">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="821c4-141">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="821c4-142">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="821c4-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="821c4-143">**Nom**</span><span class="sxs-lookup"><span data-stu-id="821c4-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="821c4-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="821c4-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="821c4-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="821c4-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="821c4-146">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="821c4-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="821c4-147">Définit l’étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="821c4-147">Defines the label by which the object is known.</span></span>

<span data-ttu-id="821c4-148">Cette propriété est héritée [**du \_ système CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="821c4-148">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="821c4-149">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="821c4-149">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="821c4-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="821c4-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="821c4-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="821c4-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="821c4-152">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span><span class="sxs-lookup"><span data-stu-id="821c4-152">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span></span>
</dt> </dl>

<span data-ttu-id="821c4-153">Identifie la manière dont le nom du système informatique est généré, à l’aide d’une heuristique.</span><span class="sxs-lookup"><span data-stu-id="821c4-153">Identifies how the computer system name is generated, using a heuristic.</span></span> <span data-ttu-id="821c4-154">L’heuristique est décrite en détail dans la spécification du modèle commun CIM v2.</span><span class="sxs-lookup"><span data-stu-id="821c4-154">The heuristic is outlined, in detail, in the CIM V2 Common Model specification.</span></span> <span data-ttu-id="821c4-155">Il part du principe que les règles documentées sont parcourues dans l’ordre, pour déterminer et assigner un nom.</span><span class="sxs-lookup"><span data-stu-id="821c4-155">It assumes that the documented rules are traversed in order, to determine and assign a name.</span></span> <span data-ttu-id="821c4-156">La liste des valeurs de **NameFormat** définit l’ordre de priorité pour l’attribution du nom de système de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="821c4-156">The **NameFormat** values list defines the precedence order for assigning the computer system name.</span></span> <span data-ttu-id="821c4-157">Plusieurs règles mappent à la même valeur.</span><span class="sxs-lookup"><span data-stu-id="821c4-157">Several rules do map to the same Value.</span></span>

<span data-ttu-id="821c4-158">Notez que le **nom** de l’objet est calculé à l’aide de la méthode heuristique est la valeur de clé du système.</span><span class="sxs-lookup"><span data-stu-id="821c4-158">Note that the object's **Name** is calculated using the heuristic is the system's key value.</span></span> <span data-ttu-id="821c4-159">D’autres noms peuvent être attribués et utilisés pour l’objet qui est mieux adapté à l’entreprise, à l’aide d’alias.</span><span class="sxs-lookup"><span data-stu-id="821c4-159">Other names can be assigned and used for the object that better suit the business, using Aliases.</span></span>

<dt>

<span id="IP"></span><span id="ip"></span>

<span data-ttu-id="821c4-160">**IP** (« IP »)</span><span class="sxs-lookup"><span data-stu-id="821c4-160">**IP** ("IP")</span></span>


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

<span data-ttu-id="821c4-161">**Composer** (« composer »)</span><span class="sxs-lookup"><span data-stu-id="821c4-161">**Dial** ("Dial")</span></span>


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

<span data-ttu-id="821c4-162">**HID** (« HID »)</span><span class="sxs-lookup"><span data-stu-id="821c4-162">**HID** ("HID")</span></span>


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

<span data-ttu-id="821c4-163">**NWA** (« NWA »)</span><span class="sxs-lookup"><span data-stu-id="821c4-163">**NWA** ("NWA")</span></span>


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

<span data-ttu-id="821c4-164">**Hwa** (« Hwa »)</span><span class="sxs-lookup"><span data-stu-id="821c4-164">**HWA** ("HWA")</span></span>


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

<span data-ttu-id="821c4-165">**X25** (« x25 »)</span><span class="sxs-lookup"><span data-stu-id="821c4-165">**X25** ("X25")</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

<span data-ttu-id="821c4-166">**RNIS** (« RNIS »)</span><span class="sxs-lookup"><span data-stu-id="821c4-166">**ISDN** ("ISDN")</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="821c4-167">**IPX** (« IPX »)</span><span class="sxs-lookup"><span data-stu-id="821c4-167">**IPX** ("IPX")</span></span>


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

<span data-ttu-id="821c4-168">**DCC** (« DCC »)</span><span class="sxs-lookup"><span data-stu-id="821c4-168">**DCC** ("DCC")</span></span>


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

<span data-ttu-id="821c4-169">**ICD** ("ICD")</span><span class="sxs-lookup"><span data-stu-id="821c4-169">**ICD** ("ICD")</span></span>


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

<span data-ttu-id="821c4-170">**E. 164** ("e. 164")</span><span class="sxs-lookup"><span data-stu-id="821c4-170">**E.164** ("E.164")</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="821c4-171">**SNA** (« SNA »)</span><span class="sxs-lookup"><span data-stu-id="821c4-171">**SNA** ("SNA")</span></span>


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

<span data-ttu-id="821c4-172">**OID/OSI** (« OID/OSI »)</span><span class="sxs-lookup"><span data-stu-id="821c4-172">**OID/OSI** ("OID/OSI")</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="821c4-173">**Autre** (« autre »)</span><span class="sxs-lookup"><span data-stu-id="821c4-173">**Other** ("Other")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="821c4-174">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="821c4-174">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="821c4-175">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="821c4-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="821c4-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="821c4-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="821c4-177">Comment le propriétaire du système principal peut être atteint (par exemple, un numéro de téléphone ou une adresse de messagerie).</span><span class="sxs-lookup"><span data-stu-id="821c4-177">How the primary system owner can be reached (for example, phone number or email address).</span></span>

<span data-ttu-id="821c4-178">Cette propriété est héritée [**du \_ système CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="821c4-178">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="821c4-179">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="821c4-179">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="821c4-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="821c4-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="821c4-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="821c4-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="821c4-182">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="821c4-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="821c4-183">Nom du propriétaire du système principal.</span><span class="sxs-lookup"><span data-stu-id="821c4-183">Name of the primary system owner.</span></span>

<span data-ttu-id="821c4-184">Cette propriété est héritée [**du \_ système CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="821c4-184">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="821c4-185">**Rôles**</span><span class="sxs-lookup"><span data-stu-id="821c4-185">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="821c4-186">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="821c4-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="821c4-187">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="821c4-187">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="821c4-188">Rôles joués par le système dans l’environnement informatique.</span><span class="sxs-lookup"><span data-stu-id="821c4-188">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="821c4-189">Les sous-classes du système peuvent remplacer cette propriété pour définir des valeurs de rôle explicites.</span><span class="sxs-lookup"><span data-stu-id="821c4-189">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="821c4-190">Un groupe de travail peut également décrire les heuristiques, les conventions et les instructions pour la spécification des rôles.</span><span class="sxs-lookup"><span data-stu-id="821c4-190">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="821c4-191">Par exemple, pour une instance d’un système de mise en réseau, cette propriété peut contenir la chaîne « Switch » ou « Bridge ».</span><span class="sxs-lookup"><span data-stu-id="821c4-191">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

<span data-ttu-id="821c4-192">Cette propriété est héritée [**du \_ système CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="821c4-192">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="821c4-193">**État**</span><span class="sxs-lookup"><span data-stu-id="821c4-193">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="821c4-194">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="821c4-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="821c4-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="821c4-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="821c4-196">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="821c4-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="821c4-197">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="821c4-197">String that indicates the current status of the object.</span></span> <span data-ttu-id="821c4-198">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="821c4-198">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="821c4-199">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="821c4-199">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="821c4-200">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="821c4-200">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="821c4-201">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="821c4-201">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="821c4-202">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="821c4-202">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="821c4-203">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="821c4-203">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="821c4-204">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="821c4-204">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="821c4-205">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="821c4-205">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="821c4-206">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="821c4-206">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="821c4-207">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="821c4-207">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="821c4-208">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="821c4-208">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="821c4-209">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="821c4-209">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="821c4-210">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="821c4-210">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="821c4-211">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="821c4-211">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="821c4-212">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="821c4-212">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="821c4-213">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="821c4-213">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="821c4-214">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="821c4-214">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="821c4-215">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="821c4-215">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="821c4-216">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="821c4-216">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="821c4-217">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="821c4-217">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="821c4-218"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="821c4-218"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="821c4-219">Notes</span><span class="sxs-lookup"><span data-stu-id="821c4-219">Remarks</span></span>

<span data-ttu-id="821c4-220">La **classe \_ ComputerSystem CIM** est dérivée [**du \_ système CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="821c4-220">The **CIM\_ComputerSystem** class is derived from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="821c4-221">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="821c4-221">WMI does not implement this class.</span></span> <span data-ttu-id="821c4-222">Pour plus d’informations sur les classes dérivées de **CIM \_ ComputerSystem**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="821c4-222">For more information about classes derived from **CIM\_ComputerSystem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="821c4-223">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="821c4-223">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="821c4-224">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="821c4-224">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="821c4-225">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="821c4-225">Requirements</span></span>



| <span data-ttu-id="821c4-226">Condition requise</span><span class="sxs-lookup"><span data-stu-id="821c4-226">Requirement</span></span> | <span data-ttu-id="821c4-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="821c4-227">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="821c4-228">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="821c4-228">Minimum supported client</span></span><br/> | <span data-ttu-id="821c4-229">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="821c4-229">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="821c4-230">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="821c4-230">Minimum supported server</span></span><br/> | <span data-ttu-id="821c4-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="821c4-231">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="821c4-232">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="821c4-232">Namespace</span></span><br/>                | <span data-ttu-id="821c4-233">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="821c4-233">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="821c4-234">MOF</span><span class="sxs-lookup"><span data-stu-id="821c4-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="821c4-235"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="821c4-235"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="821c4-236">DLL</span><span class="sxs-lookup"><span data-stu-id="821c4-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="821c4-237"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="821c4-237"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="821c4-238">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="821c4-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="821c4-239">**\_Système CIM**</span><span class="sxs-lookup"><span data-stu-id="821c4-239">**CIM\_System**</span></span>](cim-system.md)
</dt> </dl>

 

