---
description: La \_ classe CIM OperatingSystem représente un système d’exploitation d’ordinateur, qui est constitué de logiciels et de microprogrammes permettant de rendre le matériel d’un système d’ordinateur utilisable.
ms.assetid: 014d2553-e1ac-4394-84ae-307af3658f6e
ms.tgt_platform: multiple
title: Classe CIM_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystem
- CIM_OperatingSystem.Caption
- CIM_OperatingSystem.CreationClassName
- CIM_OperatingSystem.CSCreationClassName
- CIM_OperatingSystem.CSName
- CIM_OperatingSystem.CurrentTimeZone
- CIM_OperatingSystem.Description
- CIM_OperatingSystem.Distributed
- CIM_OperatingSystem.FreePhysicalMemory
- CIM_OperatingSystem.FreeSpaceInPagingFiles
- CIM_OperatingSystem.FreeVirtualMemory
- CIM_OperatingSystem.InstallDate
- CIM_OperatingSystem.LastBootUpTime
- CIM_OperatingSystem.LocalDateTime
- CIM_OperatingSystem.MaxNumberOfProcesses
- CIM_OperatingSystem.MaxProcessMemorySize
- CIM_OperatingSystem.Name
- CIM_OperatingSystem.NumberOfLicensedUsers
- CIM_OperatingSystem.NumberOfProcesses
- CIM_OperatingSystem.NumberOfUsers
- CIM_OperatingSystem.OSType
- CIM_OperatingSystem.OtherTypeDescription
- CIM_OperatingSystem.SizeStoredInPagingFiles
- CIM_OperatingSystem.Status
- CIM_OperatingSystem.TotalSwapSpaceSize
- CIM_OperatingSystem.TotalVirtualMemorySize
- CIM_OperatingSystem.TotalVisibleMemorySize
- CIM_OperatingSystem.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5b4af54a0f086bee4b743b083c27a67777786bc4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523743"
---
# <a name="cim_operatingsystem-class"></a><span data-ttu-id="49f5e-103">\_Classe CIM OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="49f5e-103">CIM\_OperatingSystem class</span></span>

<span data-ttu-id="49f5e-104">La classe **CIM \_ OperatingSystem** représente un système d’exploitation d’ordinateur, qui est constitué de logiciels et de microprogrammes permettant de rendre le matériel d’un système d’ordinateur utilisable.</span><span class="sxs-lookup"><span data-stu-id="49f5e-104">The **CIM\_OperatingSystem** class represents a computer operating system, which is made up of software and firmware that make a computer system's hardware usable.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="49f5e-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="49f5e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="49f5e-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="49f5e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="49f5e-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="49f5e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="49f5e-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="49f5e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="49f5e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49f5e-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C565-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_OperatingSystem : CIM_LogicalElement
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  sint16   CurrentTimeZone;
  string   Description;
  boolean  Distributed;
  uint64   FreePhysicalMemory;
  uint64   FreeSpaceInPagingFiles;
  uint64   FreeVirtualMemory;
  datetime InstallDate;
  datetime LastBootUpTime;
  datetime LocalDateTime;
  uint32   MaxNumberOfProcesses;
  uint64   MaxProcessMemorySize;
  string   Name;
  uint32   NumberOfLicensedUsers;
  uint32   NumberOfProcesses;
  uint32   NumberOfUsers;
  uint16   OSType;
  string   OtherTypeDescription;
  uint64   SizeStoredInPagingFiles;
  string   Status;
  uint64   TotalSwapSpaceSize;
  uint64   TotalVirtualMemorySize;
  uint64   TotalVisibleMemorySize;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="49f5e-110">Membres</span><span class="sxs-lookup"><span data-stu-id="49f5e-110">Members</span></span>

<span data-ttu-id="49f5e-111">La classe **CIM \_ OperatingSystem** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="49f5e-111">The **CIM\_OperatingSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="49f5e-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="49f5e-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="49f5e-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="49f5e-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="49f5e-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="49f5e-114">Methods</span></span>

<span data-ttu-id="49f5e-115">La classe **CIM \_ OperatingSystem** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="49f5e-115">The **CIM\_OperatingSystem** class has these methods.</span></span>



| <span data-ttu-id="49f5e-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="49f5e-116">Method</span></span>                                                           | <span data-ttu-id="49f5e-117">Description</span><span class="sxs-lookup"><span data-stu-id="49f5e-117">Description</span></span>                                                                                                                            |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49f5e-118">**Reboot**</span><span class="sxs-lookup"><span data-stu-id="49f5e-118">**Reboot**</span></span>](reboot-method-in-class-cim-operatingsystem.md)     | <span data-ttu-id="49f5e-119">Méthode de la classe qui arrête le système informatique, puis le redémarre.</span><span class="sxs-lookup"><span data-stu-id="49f5e-119">Class method that shuts down the computer system, then restarts it.</span></span> <span data-ttu-id="49f5e-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="49f5e-120">Not implemented by WMI.</span></span><br/>                                 |
| [<span data-ttu-id="49f5e-121">**Correct**</span><span class="sxs-lookup"><span data-stu-id="49f5e-121">**Shutdown**</span></span>](shutdown-method-in-class-cim-operatingsystem.md) | <span data-ttu-id="49f5e-122">Méthode de classe qui décharge les programmes et les dll jusqu’au point où il est possible de mettre hors tension l’ordinateur en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="49f5e-122">Class method that unloads programs and DLLs to the point where it is safe to turn off the computer.</span></span> <span data-ttu-id="49f5e-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="49f5e-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="49f5e-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="49f5e-124">Properties</span></span>

<span data-ttu-id="49f5e-125">La classe **CIM \_ OperatingSystem** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="49f5e-125">The **CIM\_OperatingSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="49f5e-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="49f5e-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="49f5e-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-129">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="49f5e-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-130">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="49f5e-130">Short textual description of the object.</span></span>

<span data-ttu-id="49f5e-131">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="49f5e-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="49f5e-132">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="49f5e-132">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="49f5e-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-135">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="49f5e-135">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-136">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="49f5e-136">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="49f5e-137">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="49f5e-137">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="49f5e-138">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="49f5e-138">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="49f5e-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-141">Qualificateurs : [**propagé**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM CIM \_**](cim-computersystem.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="49f5e-141">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-142">Portée du nom de la classe de création du système de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="49f5e-142">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="49f5e-143">**CSName**</span><span class="sxs-lookup"><span data-stu-id="49f5e-143">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="49f5e-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-146">Qualificateurs : [**propagé**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM CIM \_**](cim-computersystem.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="49f5e-146">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-147">Nom du système d’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="49f5e-147">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="49f5e-148">**CurrentTimeZone**</span><span class="sxs-lookup"><span data-stu-id="49f5e-148">**CurrentTimeZone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-149">Type de données : **sint16**</span><span class="sxs-lookup"><span data-stu-id="49f5e-149">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-151">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« minutes »)</span><span class="sxs-lookup"><span data-stu-id="49f5e-151">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-152">Nombre de minutes pendant lequel le système d’exploitation est décalé par rapport à l’heure GMT (Greenwich Mean Time).</span><span class="sxs-lookup"><span data-stu-id="49f5e-152">Number of minutes the operating system is offset from Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="49f5e-153">Le nombre est positif, négatif ou égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="49f5e-153">The number is positive, negative, or zero.</span></span>

</dd> <dt>

<span data-ttu-id="49f5e-154">**Description**</span><span class="sxs-lookup"><span data-stu-id="49f5e-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="49f5e-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-157">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="49f5e-157">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-158">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="49f5e-158">Textual description of the object.</span></span>

<span data-ttu-id="49f5e-159">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="49f5e-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="49f5e-160">**Graphique**</span><span class="sxs-lookup"><span data-stu-id="49f5e-160">**Distributed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-161">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="49f5e-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-163">Si la **valeur est true**, le système d’exploitation est distribué sur plusieurs nœuds système de l’ordinateur, qui doivent être regroupés en tant que cluster.</span><span class="sxs-lookup"><span data-stu-id="49f5e-163">If **TRUE**, the operating system is distributed across several computer system nodes, which should be grouped as a cluster.</span></span>

</dd> <dt>

<span data-ttu-id="49f5e-164">**FreePhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="49f5e-164">**FreePhysicalMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-165">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="49f5e-165">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-167">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« kilo-octets »)</span><span class="sxs-lookup"><span data-stu-id="49f5e-167">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-168">Nombre de kilo-octets de mémoire physique actuellement inutilisée et disponible.</span><span class="sxs-lookup"><span data-stu-id="49f5e-168">Number of kilobytes of physical memory currently unused and available.</span></span>

<span data-ttu-id="49f5e-169">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="49f5e-169">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="49f5e-170">**FreeSpaceInPagingFiles**</span><span class="sxs-lookup"><span data-stu-id="49f5e-170">**FreeSpaceInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-171">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="49f5e-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-173">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Paramètres de mémoire système DMTF \| 001,4»), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« kilo-octets »)</span><span class="sxs-lookup"><span data-stu-id="49f5e-173">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Memory Settings\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-174">Nombre de kilo-octets qui peuvent être mappés dans les fichiers de pagination du système d’exploitation sans entraîner le remplacement d’autres pages. La valeur 0 indique qu’il n’y a aucun fichier de pagination.</span><span class="sxs-lookup"><span data-stu-id="49f5e-174">Number of kilobytes that can be mapped into the operating system's paging files without causing other pages to be swapped out. A value of 0 indicates that there are no paging files.</span></span>

<span data-ttu-id="49f5e-175">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="49f5e-175">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="49f5e-176">**FreeVirtualMemory**</span><span class="sxs-lookup"><span data-stu-id="49f5e-176">**FreeVirtualMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-177">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="49f5e-177">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-179">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« kilo-octets »)</span><span class="sxs-lookup"><span data-stu-id="49f5e-179">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-180">Nombre de kilo-octets de mémoire virtuelle actuellement inutilisés et disponibles.</span><span class="sxs-lookup"><span data-stu-id="49f5e-180">Number of kilobytes of virtual memory currently unused and available.</span></span> <span data-ttu-id="49f5e-181">Par exemple, vous pouvez calculer cela en ajoutant la quantité de RAM libre à la quantité d’espace de pagination libre (c’est-à-dire en ajoutant les propriétés **FreePhysicalMemory** et **FreeSpaceInPagingFiles** ).</span><span class="sxs-lookup"><span data-stu-id="49f5e-181">For example, this can be calculated by adding the amount of free RAM to the amount of free paging space (that is, adding the **FreePhysicalMemory** and **FreeSpaceInPagingFiles** properties).</span></span>

<span data-ttu-id="49f5e-182">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="49f5e-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="49f5e-183">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="49f5e-183">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-184">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="49f5e-184">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-186">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="49f5e-186">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-187">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="49f5e-187">Date and time the object was installed.</span></span> <span data-ttu-id="49f5e-188">Cette propriété ne requiert pas de valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="49f5e-188">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="49f5e-189">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="49f5e-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="49f5e-190">**LastBootUpTime**</span><span class="sxs-lookup"><span data-stu-id="49f5e-190">**LastBootUpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-191">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="49f5e-191">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-193">Heure du dernier démarrage du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="49f5e-193">Time when the operating system was last booted.</span></span>

</dd> <dt>

<span data-ttu-id="49f5e-194">**LocalDateTime**</span><span class="sxs-lookup"><span data-stu-id="49f5e-194">**LocalDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-195">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="49f5e-195">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-197">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrSystemDate "," MIF. \|Informations générales sur DMTF \| 001,6»)</span><span class="sxs-lookup"><span data-stu-id="49f5e-197">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemDate", "MIF.DMTF\|General Information\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-198">Notion du système d’exploitation de la date et de l’heure locales de la journée.</span><span class="sxs-lookup"><span data-stu-id="49f5e-198">Operating system's notion of the local date and time of day.</span></span>

</dd> <dt>

<span data-ttu-id="49f5e-199">**MaxNumberOfProcesses**</span><span class="sxs-lookup"><span data-stu-id="49f5e-199">**MaxNumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-200">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="49f5e-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-201">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-202">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrSystemMaxProcesses ")</span><span class="sxs-lookup"><span data-stu-id="49f5e-202">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemMaxProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-203">Nombre maximal de contextes de processus que le système d’exploitation peut prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="49f5e-203">Maximum number of process contexts the operating system can support.</span></span> <span data-ttu-id="49f5e-204">S’il n’y a pas de valeur maximale fixe, la valeur doit être 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="49f5e-204">If there is no fixed maximum, the value should be 0 (zero).</span></span> <span data-ttu-id="49f5e-205">Sur les systèmes qui ont un maximum fixe, cet objet peut aider à diagnostiquer les défaillances qui se produisent lorsque le maximum est atteint.</span><span class="sxs-lookup"><span data-stu-id="49f5e-205">On systems that have a fixed maximum, this object can help diagnose failures that occur when the maximum is reached.</span></span> <span data-ttu-id="49f5e-206">S’il est inconnu, entrez-1.</span><span class="sxs-lookup"><span data-stu-id="49f5e-206">If unknown, enter -1.</span></span>

</dd> <dt>

<span data-ttu-id="49f5e-207">**MaxProcessMemorySize**</span><span class="sxs-lookup"><span data-stu-id="49f5e-207">**MaxProcessMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-208">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="49f5e-208">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-210">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« kilo-octets »)</span><span class="sxs-lookup"><span data-stu-id="49f5e-210">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-211">Nombre maximal de kilo-octets de mémoire qui peuvent être alloués à un processus.</span><span class="sxs-lookup"><span data-stu-id="49f5e-211">Maximum number of kilobytes of memory that can be allocated to a process.</span></span> <span data-ttu-id="49f5e-212">Pour les systèmes d’exploitation sans mémoire virtuelle, cette valeur est généralement égale à la quantité totale de mémoire physique, moins la mémoire utilisée par le BIOS et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="49f5e-212">For operating systems with no virtual memory, this value is typically equal to the total amount of physical memory, minus memory used by the BIOS and the operating system.</span></span> <span data-ttu-id="49f5e-213">Pour certains systèmes d’exploitation, cette valeur peut être l’infini, auquel cas 0 doit être entré.</span><span class="sxs-lookup"><span data-stu-id="49f5e-213">For some operating systems, this value can be infinity, in which case 0 should be entered.</span></span> <span data-ttu-id="49f5e-214">Dans d’autres cas, cette valeur peut être une constante, par exemple 2 Go ou 4 Go.</span><span class="sxs-lookup"><span data-stu-id="49f5e-214">In other cases, this value can be a constant, for example, 2 GB or 4 GB.</span></span>

<span data-ttu-id="49f5e-215">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="49f5e-215">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="49f5e-216">**Nom**</span><span class="sxs-lookup"><span data-stu-id="49f5e-216">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-217">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="49f5e-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-219">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="49f5e-219">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-220">Clé d’une instance de système d’exploitation au sein d’un système informatique.</span><span class="sxs-lookup"><span data-stu-id="49f5e-220">Key of an operating system instance within a computer system.</span></span>

<span data-ttu-id="49f5e-221">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="49f5e-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="49f5e-222">**NumberOfLicensedUsers**</span><span class="sxs-lookup"><span data-stu-id="49f5e-222">**NumberOfLicensedUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-223">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="49f5e-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-225">Nombre de licences utilisateur pour le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="49f5e-225">Number of user licenses for the operating system.</span></span> <span data-ttu-id="49f5e-226">Si la valeur est Unlimited, entrez 0, si inconnu, entrez-1.</span><span class="sxs-lookup"><span data-stu-id="49f5e-226">If unlimited, enter 0, if unknown, enter -1.</span></span>

</dd> <dt>

<span data-ttu-id="49f5e-227">**NumberOfProcesses**</span><span class="sxs-lookup"><span data-stu-id="49f5e-227">**NumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-228">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="49f5e-228">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-229">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-230">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrSystemProcesses ")</span><span class="sxs-lookup"><span data-stu-id="49f5e-230">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-231">Nombre de contextes de processus actuellement chargés ou en cours d’exécution sur le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="49f5e-231">Number of process contexts currently loaded or running on the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="49f5e-232">**Numdatabases**</span><span class="sxs-lookup"><span data-stu-id="49f5e-232">**NumberOfUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-233">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="49f5e-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-234">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-235">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrSystemNumUsers ")</span><span class="sxs-lookup"><span data-stu-id="49f5e-235">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemNumUsers")</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-236">Nombre de sessions utilisateur pour lesquelles le système d’exploitation stocke actuellement des informations d’État.</span><span class="sxs-lookup"><span data-stu-id="49f5e-236">Number of user sessions for which the operating system is currently storing state information.</span></span>

</dd> <dt>

<span data-ttu-id="49f5e-237">**OSType**</span><span class="sxs-lookup"><span data-stu-id="49f5e-237">**OSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-238">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="49f5e-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-239">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-240">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ OperatingSystem**.**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="49f5e-240">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_OperatingSystem**.**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-241">Type de système d'exploitation.</span><span class="sxs-lookup"><span data-stu-id="49f5e-241">Type of operating system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="49f5e-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="49f5e-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="49f5e-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="49f5e-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="49f5e-244"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="49f5e-244"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="49f5e-245">Mac OS</span><span class="sxs-lookup"><span data-stu-id="49f5e-245">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="49f5e-246"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="49f5e-246"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="49f5e-247">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="49f5e-247">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="49f5e-248"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="49f5e-248"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="49f5e-249"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="49f5e-249"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="49f5e-250"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX numérique** (6)</span><span class="sxs-lookup"><span data-stu-id="49f5e-250"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="49f5e-251"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="49f5e-251"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="49f5e-252">Ouvrir des machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="49f5e-252">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="49f5e-253"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="49f5e-253"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="49f5e-254">HP-UX</span><span class="sxs-lookup"><span data-stu-id="49f5e-254">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="49f5e-255"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="49f5e-255"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="49f5e-256"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="49f5e-256"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="49f5e-257"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="49f5e-257"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="49f5e-258"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="49f5e-258"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="49f5e-259"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="49f5e-259"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="49f5e-260">Machine virtuelle Microsoft pour Java</span><span class="sxs-lookup"><span data-stu-id="49f5e-260">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="49f5e-261"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="49f5e-261"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="49f5e-262"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="49f5e-262"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="49f5e-263">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="49f5e-263">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="49f5e-264"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="49f5e-264"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="49f5e-265">Windows 95</span><span class="sxs-lookup"><span data-stu-id="49f5e-265">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="49f5e-266"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="49f5e-266"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="49f5e-267">Windows 98</span><span class="sxs-lookup"><span data-stu-id="49f5e-267">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="49f5e-268"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="49f5e-268"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="49f5e-269">Windows NT</span><span class="sxs-lookup"><span data-stu-id="49f5e-269">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="49f5e-270"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="49f5e-270"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="49f5e-271">Windows CE</span><span class="sxs-lookup"><span data-stu-id="49f5e-271">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="49f5e-272"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="49f5e-272"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="49f5e-273">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="49f5e-273">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="49f5e-274"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="49f5e-274"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="49f5e-275"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="49f5e-275"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="49f5e-276"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="49f5e-276"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="49f5e-277"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Dépendant d’UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="49f5e-277"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="49f5e-278"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="49f5e-278"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="49f5e-279"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="49f5e-279"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="49f5e-280"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="49f5e-280"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="49f5e-281"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="49f5e-281"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="49f5e-282"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="49f5e-282"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="49f5e-283"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="49f5e-283"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="49f5e-284"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="49f5e-284"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="49f5e-285"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="49f5e-285"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="49f5e-286">Une série</span><span class="sxs-lookup"><span data-stu-id="49f5e-286">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="49f5e-287"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="49f5e-287"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="49f5e-288">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="49f5e-288">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="49f5e-289"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="49f5e-289"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="49f5e-290">NT tandem</span><span class="sxs-lookup"><span data-stu-id="49f5e-290">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="49f5e-291"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="49f5e-291"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="49f5e-292">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="49f5e-292">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="49f5e-293"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="49f5e-293"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="49f5e-294"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="49f5e-294"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="49f5e-295"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="49f5e-295"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="49f5e-296"><span id="VM_ESA"></span><span id="vm_esa"></span>**Machine virtuelle/SEEE** (39)</span><span class="sxs-lookup"><span data-stu-id="49f5e-296"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="49f5e-297"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactif** (40)</span><span class="sxs-lookup"><span data-stu-id="49f5e-297"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="49f5e-298"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="49f5e-298"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="49f5e-299">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="49f5e-299">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="49f5e-300"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="49f5e-300"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="49f5e-301"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="49f5e-301"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="49f5e-302"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**Hurd gnu** (44)</span><span class="sxs-lookup"><span data-stu-id="49f5e-302"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="49f5e-303"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="49f5e-303"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="49f5e-304">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="49f5e-304">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="49f5e-305"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Noyau Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="49f5e-305"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="49f5e-306"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="49f5e-306"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="49f5e-307"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="49f5e-307"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="49f5e-308"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="49f5e-308"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="49f5e-309"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="49f5e-309"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="49f5e-310"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="49f5e-310"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="49f5e-311"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menthe** (52)</span><span class="sxs-lookup"><span data-stu-id="49f5e-311"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="49f5e-312"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="49f5e-312"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="49f5e-313"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="49f5e-313"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="49f5e-314"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="49f5e-314"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="49f5e-315"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="49f5e-315"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="49f5e-316">Palm OS</span><span class="sxs-lookup"><span data-stu-id="49f5e-316">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="49f5e-317"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="49f5e-317"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="49f5e-318"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="49f5e-318"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="49f5e-319"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dédié** (59)</span><span class="sxs-lookup"><span data-stu-id="49f5e-319"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

<span data-ttu-id="49f5e-320"><span id="OS_390"></span><span id="os_390"></span>**OS/390** (60)</span><span class="sxs-lookup"><span data-stu-id="49f5e-320"><span id="OS_390"></span><span id="os_390"></span>**OS/390** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="49f5e-321"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span><span class="sxs-lookup"><span data-stu-id="49f5e-321"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="49f5e-322"><span id="TPF"></span><span id="tpf"></span>**TPF** (62)</span><span class="sxs-lookup"><span data-stu-id="49f5e-322"><span id="TPF"></span><span id="tpf"></span>**TPF** (62)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="49f5e-323">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="49f5e-323">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-324">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="49f5e-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-325">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-326">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ OperatingSystem**.**OSType**")</span><span class="sxs-lookup"><span data-stu-id="49f5e-326">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_OperatingSystem**.**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-327">Décrit le fabricant et le type de système d’exploitation lorsque la propriété **OSTYPE** a la valeur 1 (« other »).</span><span class="sxs-lookup"><span data-stu-id="49f5e-327">Describes the manufacturer and operating system type when the **OSType** property is set to 1 ("Other").</span></span> <span data-ttu-id="49f5e-328">Le format de la chaîne insérée dans **OtherTypeDescription** doit être semblable aux chaînes de **valeurs** définies pour **OSTYPE**.</span><span class="sxs-lookup"><span data-stu-id="49f5e-328">The format of the string inserted in **OtherTypeDescription** should be similar to the **Values** strings defined for **OSType**.</span></span> <span data-ttu-id="49f5e-329">Cette propriété doit être définie sur Null lorsque **OSTYPE** est une valeur autre que 1 (un).</span><span class="sxs-lookup"><span data-stu-id="49f5e-329">This property should be set to null when **OSType** is a value other than 1 (one).</span></span>

</dd> <dt>

<span data-ttu-id="49f5e-330">**SizeStoredInPagingFiles**</span><span class="sxs-lookup"><span data-stu-id="49f5e-330">**SizeStoredInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-331">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="49f5e-331">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-333">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Paramètres de mémoire système DMTF \| 001,3»), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« kilo-octets »)</span><span class="sxs-lookup"><span data-stu-id="49f5e-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Memory Settings\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-334">Nombre de kilo-octets pouvant être stockés dans les fichiers de pagination du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="49f5e-334">Number of kilobytes that can be stored in the operating system's paging files.</span></span> <span data-ttu-id="49f5e-335">Ce nombre ne représente pas la taille physique réelle du fichier d’échange sur le disque.</span><span class="sxs-lookup"><span data-stu-id="49f5e-335">This number does not represent the actual physical size of the paging file on disk.</span></span> <span data-ttu-id="49f5e-336">La valeur 0 (zéro) indique qu’il n’y a aucun fichier de pagination.</span><span class="sxs-lookup"><span data-stu-id="49f5e-336">A value of 0 (zero)indicates that there are no paging files.</span></span>

<span data-ttu-id="49f5e-337">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="49f5e-337">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="49f5e-338">**État**</span><span class="sxs-lookup"><span data-stu-id="49f5e-338">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-339">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="49f5e-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-340">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-341">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="49f5e-341">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-342">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="49f5e-342">Current status of the object.</span></span>

<span data-ttu-id="49f5e-343">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="49f5e-343">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="49f5e-344">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="49f5e-344">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="49f5e-345">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="49f5e-345">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="49f5e-346">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="49f5e-346">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="49f5e-347">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="49f5e-347">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="49f5e-348">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="49f5e-348">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="49f5e-349">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="49f5e-349">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="49f5e-350">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="49f5e-350">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="49f5e-351">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="49f5e-351">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="49f5e-352">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="49f5e-352">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="49f5e-353">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="49f5e-353">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="49f5e-354">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="49f5e-354">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="49f5e-355">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="49f5e-355">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="49f5e-356">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="49f5e-356">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="49f5e-357">**TotalSwapSpaceSize**</span><span class="sxs-lookup"><span data-stu-id="49f5e-357">**TotalSwapSpaceSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-358">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="49f5e-358">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-359">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-360">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« kilo-octets »)</span><span class="sxs-lookup"><span data-stu-id="49f5e-360">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-361">Espace d’échange total, en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="49f5e-361">Total swap space, in kilobytes.</span></span> <span data-ttu-id="49f5e-362">Cette valeur peut être null (non spécifié) si l’espace d’échange n’est pas distingué des fichiers d’échange.</span><span class="sxs-lookup"><span data-stu-id="49f5e-362">This value can be null (unspecified) if swap space is not distinguished from page files.</span></span> <span data-ttu-id="49f5e-363">Toutefois, certains systèmes d’exploitation distinguent ces concepts.</span><span class="sxs-lookup"><span data-stu-id="49f5e-363">However, some operating systems distinguish these concepts.</span></span> <span data-ttu-id="49f5e-364">Par exemple, les processus entiers peuvent être « échangés » dans UNIX lorsque la liste de pages gratuites tombe en dessous d’un montant spécifié.</span><span class="sxs-lookup"><span data-stu-id="49f5e-364">For example, entire processes can be "swapped out" in UNIX when the free page list falls and remains below a specified amount.</span></span>

<span data-ttu-id="49f5e-365">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="49f5e-365">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="49f5e-366">**TotalVirtualMemorySize**</span><span class="sxs-lookup"><span data-stu-id="49f5e-366">**TotalVirtualMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-367">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="49f5e-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-368">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-369">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« kilo-octets »)</span><span class="sxs-lookup"><span data-stu-id="49f5e-369">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-370">Nombre de kilo-octets de mémoire virtuelle.</span><span class="sxs-lookup"><span data-stu-id="49f5e-370">Number of kilobytes of virtual memory.</span></span> <span data-ttu-id="49f5e-371">Par exemple, calculez-le en ajoutant la quantité de mémoire RAM totale à la quantité d’espace de pagination (c’est-à-dire, ajoutez la quantité de mémoire dans ou agrégée par le système informatique à la propriété **SizeStoredInPagingFiles** .</span><span class="sxs-lookup"><span data-stu-id="49f5e-371">For example, calculate this by adding the amount of total RAM to the amount of paging space (that is, add the amount of memory in or aggregated by the computer system to the **SizeStoredInPagingFiles** property.</span></span>

<span data-ttu-id="49f5e-372">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="49f5e-372">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="49f5e-373">**TotalVisibleMemorySize**</span><span class="sxs-lookup"><span data-stu-id="49f5e-373">**TotalVisibleMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-374">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="49f5e-374">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-375">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-376">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« kilo-octets »)</span><span class="sxs-lookup"><span data-stu-id="49f5e-376">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-377">Quantité totale de mémoire physique, en kilo-octets, disponible pour le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="49f5e-377">Total amount of physical memory, in kilobytes, available to the operating system.</span></span> <span data-ttu-id="49f5e-378">Cette valeur n’indique pas nécessairement la véritable quantité de mémoire physique, mais ce qui est signalé au système d’exploitation comme disponible.</span><span class="sxs-lookup"><span data-stu-id="49f5e-378">This value does not necessarily indicate the true amount of physical memory, but what is reported to the operating system as available to it.</span></span>

<span data-ttu-id="49f5e-379">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="49f5e-379">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="49f5e-380">**Version**</span><span class="sxs-lookup"><span data-stu-id="49f5e-380">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f5e-381">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="49f5e-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-382">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f5e-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f5e-383">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Système d’exploitation DMTF \| 001,3»)</span><span class="sxs-lookup"><span data-stu-id="49f5e-383">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operating System\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="49f5e-384">Version de l’opération.</span><span class="sxs-lookup"><span data-stu-id="49f5e-384">Version of the operation.</span></span>

<span data-ttu-id="49f5e-385">La version de l’opération doit se présenter sous l’une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="49f5e-385">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="49f5e-386"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="49f5e-386"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="49f5e-387"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="49f5e-387"><major>.<minor><letter><revision></span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49f5e-388">Notes</span><span class="sxs-lookup"><span data-stu-id="49f5e-388">Remarks</span></span>

<span data-ttu-id="49f5e-389">La classe **CIM \_ OperatingSystem** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="49f5e-389">The **CIM\_OperatingSystem** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="49f5e-390">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="49f5e-390">WMI does not implement this class.</span></span> <span data-ttu-id="49f5e-391">Pour les classes WMI dérivées de **CIM \_ OperatingSystem**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="49f5e-391">For WMI classes that are derived from **CIM\_OperatingSystem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="49f5e-392">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="49f5e-392">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="49f5e-393">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="49f5e-393">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="49f5e-394">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49f5e-394">Requirements</span></span>



| <span data-ttu-id="49f5e-395">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49f5e-395">Requirement</span></span> | <span data-ttu-id="49f5e-396">Valeur</span><span class="sxs-lookup"><span data-stu-id="49f5e-396">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49f5e-397">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49f5e-397">Minimum supported client</span></span><br/> | <span data-ttu-id="49f5e-398">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49f5e-398">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="49f5e-399">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49f5e-399">Minimum supported server</span></span><br/> | <span data-ttu-id="49f5e-400">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49f5e-400">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="49f5e-401">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="49f5e-401">Namespace</span></span><br/>                | <span data-ttu-id="49f5e-402">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="49f5e-402">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="49f5e-403">MOF</span><span class="sxs-lookup"><span data-stu-id="49f5e-403">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49f5e-404"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="49f5e-404"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="49f5e-405">DLL</span><span class="sxs-lookup"><span data-stu-id="49f5e-405">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49f5e-406"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49f5e-406"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49f5e-407">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49f5e-407">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49f5e-408">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="49f5e-408">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

