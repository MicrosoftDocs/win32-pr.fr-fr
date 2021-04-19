---
description: La \_ classe CIM MemoryCheck spécifie une condition pour la quantité minimale de mémoire qui doit être disponible sur un système.
ms.assetid: a7d22f31-a285-41c4-b069-47c54865ddf5
ms.tgt_platform: multiple
title: Classe CIM_MemoryCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryCheck
- CIM_MemoryCheck.CheckID
- CIM_MemoryCheck.Caption
- CIM_MemoryCheck.Description
- CIM_MemoryCheck.CheckMode
- CIM_MemoryCheck.Name
- CIM_MemoryCheck.TargetOperatingSystem
- CIM_MemoryCheck.Version
- CIM_MemoryCheck.SoftwareElementID
- CIM_MemoryCheck.SoftwareElementState
- CIM_MemoryCheck.MemorySize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4265b108bd57bcb91aa903fd163ff14bd91311ae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517410"
---
# <a name="cim_memorycheck-class"></a><span data-ttu-id="01b3e-103">\_Classe CIM MemoryCheck</span><span class="sxs-lookup"><span data-stu-id="01b3e-103">CIM\_MemoryCheck class</span></span>

<span data-ttu-id="01b3e-104">La classe **CIM \_ MemoryCheck** spécifie une condition pour la quantité minimale de mémoire qui doit être disponible sur un système.</span><span class="sxs-lookup"><span data-stu-id="01b3e-104">The **CIM\_MemoryCheck** class specifies a condition for the minimum amount of memory that must be available on a system.</span></span> <span data-ttu-id="01b3e-105">La valeur amount est spécifiée dans la propriété **MemorySize** .</span><span class="sxs-lookup"><span data-stu-id="01b3e-105">The amount is specified in the **MemorySize** property.</span></span> <span data-ttu-id="01b3e-106">Les détails des vérifications sont comparés à la valeur de la propriété **FreePhysicalMemory** de l’objet [**CIM \_ OperatingSystem**](cim-operatingsystem.md) référencé par une association [**CIM \_ installée**](cim-installedos.md) pour l’objet [**\_ ComputerSystem CIM**](cim-computersystem.md) qui décrit l’environnement.</span><span class="sxs-lookup"><span data-stu-id="01b3e-106">Details of the checks are compared with the value of the **FreePhysicalMemory** property of the [**CIM\_OperatingSystem**](cim-operatingsystem.md) object referenced by a [**CIM\_InstalledOS**](cim-installedos.md) association for the [**CIM\_ComputerSystem**](cim-computersystem.md) object that describes the environment.</span></span> <span data-ttu-id="01b3e-107">Lorsque la valeur de la propriété **FreePhysicalMemory** est supérieure ou égale à la valeur spécifiée dans **MemorySize**, la condition est satisfaite.</span><span class="sxs-lookup"><span data-stu-id="01b3e-107">When the value of the **FreePhysicalMemory** property is greater than or equal to the value specified in **MemorySize**, the condition is satisfied.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="01b3e-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="01b3e-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="01b3e-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="01b3e-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="01b3e-110">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="01b3e-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="01b3e-111">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="01b3e-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="01b3e-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01b3e-112">Syntax</span></span>

``` syntax
[UUID("{DC0E96FE-DB2A-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_MemoryCheck : CIM_Check
{
  string  CheckID;
  string  Caption;
  string  Description;
  boolean CheckMode;
  string  Name;
  uint16  TargetOperatingSystem;
  string  Version;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
  uint64  MemorySize;
};
```

## <a name="members"></a><span data-ttu-id="01b3e-113">Membres</span><span class="sxs-lookup"><span data-stu-id="01b3e-113">Members</span></span>

<span data-ttu-id="01b3e-114">La classe **CIM \_ MemoryCheck** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="01b3e-114">The **CIM\_MemoryCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="01b3e-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="01b3e-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="01b3e-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="01b3e-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="01b3e-117">Méthodes</span><span class="sxs-lookup"><span data-stu-id="01b3e-117">Methods</span></span>

<span data-ttu-id="01b3e-118">La classe **CIM \_ MemoryCheck** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="01b3e-118">The **CIM\_MemoryCheck** class has these methods.</span></span>



| <span data-ttu-id="01b3e-119">Méthode</span><span class="sxs-lookup"><span data-stu-id="01b3e-119">Method</span></span>                                                   | <span data-ttu-id="01b3e-120">Description</span><span class="sxs-lookup"><span data-stu-id="01b3e-120">Description</span></span>                                                   |
|:---------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="01b3e-121">**Appeler**</span><span class="sxs-lookup"><span data-stu-id="01b3e-121">**Invoke**</span></span>](invoke-method-in-class-cim-memorycheck.md) | <span data-ttu-id="01b3e-122">Effectue une action particulière.</span><span class="sxs-lookup"><span data-stu-id="01b3e-122">Takes a particular action.</span></span> <span data-ttu-id="01b3e-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="01b3e-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="01b3e-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="01b3e-124">Properties</span></span>

<span data-ttu-id="01b3e-125">La classe **CIM \_ MemoryCheck** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="01b3e-125">The **CIM\_MemoryCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01b3e-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="01b3e-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01b3e-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="01b3e-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01b3e-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="01b3e-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01b3e-129">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="01b3e-129">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="01b3e-130">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="01b3e-130">A short textual description of the subject.</span></span>

<span data-ttu-id="01b3e-131">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="01b3e-131">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="01b3e-132">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="01b3e-132">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01b3e-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="01b3e-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01b3e-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="01b3e-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01b3e-135">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="01b3e-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="01b3e-136">Identificateur utilisé conjointement avec d’autres clés pour identifier de manière unique la vérification.</span><span class="sxs-lookup"><span data-stu-id="01b3e-136">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="01b3e-137">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="01b3e-137">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="01b3e-138">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="01b3e-138">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01b3e-139">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="01b3e-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="01b3e-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="01b3e-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01b3e-141">Si la **valeur est true**, la condition est supposée exister dans l’environnement.</span><span class="sxs-lookup"><span data-stu-id="01b3e-141">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="01b3e-142">Par exemple, un fichier est censé se trouver sur un système. la méthode [**Invoke**](invoke-method-in-class-cim-check.md) doit donc retourner la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="01b3e-142">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="01b3e-143">Si la **valeur est false**, la condition n’est pas censée exister.</span><span class="sxs-lookup"><span data-stu-id="01b3e-143">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="01b3e-144">Par exemple, un fichier ne se trouve pas sur un système, donc la méthode [**Invoke**](invoke-method-in-class-cim-check.md) doit retourner **false**.</span><span class="sxs-lookup"><span data-stu-id="01b3e-144">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="01b3e-145">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="01b3e-145">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="01b3e-146">**Description**</span><span class="sxs-lookup"><span data-stu-id="01b3e-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01b3e-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="01b3e-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01b3e-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="01b3e-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01b3e-149">Description des objets.</span><span class="sxs-lookup"><span data-stu-id="01b3e-149">A description of the objects.</span></span>

<span data-ttu-id="01b3e-150">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="01b3e-150">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="01b3e-151">**MemorySize**</span><span class="sxs-lookup"><span data-stu-id="01b3e-151">**MemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01b3e-152">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="01b3e-152">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="01b3e-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="01b3e-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01b3e-154">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**FreePhysicalMemory**"), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilo-octets ")</span><span class="sxs-lookup"><span data-stu-id="01b3e-154">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**FreePhysicalMemory**"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="01b3e-155">Quantité de mémoire qui doit exister sur un système informatique pour qu’un élément logiciel s’exécute correctement.</span><span class="sxs-lookup"><span data-stu-id="01b3e-155">Amount of memory that needs to exist on a computer system for a software element to execute properly.</span></span>

<span data-ttu-id="01b3e-156">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="01b3e-156">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="01b3e-157">**Nom**</span><span class="sxs-lookup"><span data-stu-id="01b3e-157">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01b3e-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="01b3e-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01b3e-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="01b3e-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01b3e-160">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="01b3e-160">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="01b3e-161">Nom utilisé pour identifier l’élément logiciel</span><span class="sxs-lookup"><span data-stu-id="01b3e-161">Name used to identify the software element</span></span>

<span data-ttu-id="01b3e-162">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="01b3e-162">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="01b3e-163">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="01b3e-163">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01b3e-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="01b3e-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01b3e-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="01b3e-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01b3e-166">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="01b3e-166">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="01b3e-167">Il s’agit d’un identificateur pour cet élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="01b3e-167">This is an identifier for this software element.</span></span>

<span data-ttu-id="01b3e-168">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="01b3e-168">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="01b3e-169">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="01b3e-169">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01b3e-170">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="01b3e-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="01b3e-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="01b3e-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01b3e-172">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="01b3e-172">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="01b3e-173">État de l’élément logiciel d’un élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="01b3e-173">The software element state of a software element.</span></span>

<span data-ttu-id="01b3e-174">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="01b3e-174">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="01b3e-175"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Déployable** (0)</span><span class="sxs-lookup"><span data-stu-id="01b3e-175"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="01b3e-176">Décrit les détails nécessaires à la réussite de la distribution et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État installable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="01b3e-176">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="01b3e-177"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installation** (1)</span><span class="sxs-lookup"><span data-stu-id="01b3e-177"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="01b3e-178">Décrit les détails nécessaires à l’installation réussie et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État exécutable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="01b3e-178">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="01b3e-179"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Exécutable** (2)</span><span class="sxs-lookup"><span data-stu-id="01b3e-179"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="01b3e-180">Décrit les détails nécessaires pour une exécution réussie et les détails (conditions et actions) requis pour créer un élément logiciel dans l’État en cours d’exécution (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="01b3e-180">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="01b3e-181"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**En cours d’exécution** (3)</span><span class="sxs-lookup"><span data-stu-id="01b3e-181"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="01b3e-182">Décrit les détails nécessaires à l’analyse et à l’utilisation d’un élément de début.</span><span class="sxs-lookup"><span data-stu-id="01b3e-182">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="01b3e-183">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="01b3e-183">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01b3e-184">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="01b3e-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="01b3e-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="01b3e-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01b3e-186">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informations sur les composants logiciels DMTF \| 002,5»)</span><span class="sxs-lookup"><span data-stu-id="01b3e-186">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="01b3e-187">Système d’exploitation cible de l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="01b3e-187">Target operating system of the software element.</span></span>

<span data-ttu-id="01b3e-188">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="01b3e-188">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="01b3e-189"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="01b3e-189"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="01b3e-190"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="01b3e-190"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="01b3e-191"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="01b3e-191"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="01b3e-192">Mac OS</span><span class="sxs-lookup"><span data-stu-id="01b3e-192">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="01b3e-193"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="01b3e-193"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="01b3e-194">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="01b3e-194">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="01b3e-195"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="01b3e-195"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="01b3e-196"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="01b3e-196"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="01b3e-197"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX numérique** (6)</span><span class="sxs-lookup"><span data-stu-id="01b3e-197"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="01b3e-198"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="01b3e-198"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="01b3e-199">Ouvrir des machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="01b3e-199">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="01b3e-200"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="01b3e-200"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="01b3e-201">HP-UX</span><span class="sxs-lookup"><span data-stu-id="01b3e-201">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="01b3e-202"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="01b3e-202"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="01b3e-203"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="01b3e-203"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="01b3e-204"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="01b3e-204"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="01b3e-205"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="01b3e-205"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="01b3e-206"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="01b3e-206"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="01b3e-207">Machine virtuelle Microsoft pour Java</span><span class="sxs-lookup"><span data-stu-id="01b3e-207">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="01b3e-208"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="01b3e-208"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="01b3e-209"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="01b3e-209"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="01b3e-210">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="01b3e-210">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="01b3e-211"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="01b3e-211"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="01b3e-212">Windows 95</span><span class="sxs-lookup"><span data-stu-id="01b3e-212">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="01b3e-213"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="01b3e-213"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="01b3e-214">Windows 98</span><span class="sxs-lookup"><span data-stu-id="01b3e-214">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="01b3e-215"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="01b3e-215"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="01b3e-216">Windows NT</span><span class="sxs-lookup"><span data-stu-id="01b3e-216">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="01b3e-217"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="01b3e-217"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="01b3e-218">Windows CE</span><span class="sxs-lookup"><span data-stu-id="01b3e-218">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="01b3e-219"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="01b3e-219"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="01b3e-220">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="01b3e-220">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="01b3e-221"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="01b3e-221"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="01b3e-222"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="01b3e-222"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="01b3e-223"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="01b3e-223"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="01b3e-224"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Dépendant d’UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="01b3e-224"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="01b3e-225"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="01b3e-225"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="01b3e-226"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="01b3e-226"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="01b3e-227"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="01b3e-227"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="01b3e-228"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="01b3e-228"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="01b3e-229"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="01b3e-229"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="01b3e-230"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="01b3e-230"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="01b3e-231"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="01b3e-231"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="01b3e-232"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="01b3e-232"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="01b3e-233">Une série</span><span class="sxs-lookup"><span data-stu-id="01b3e-233">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="01b3e-234"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="01b3e-234"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="01b3e-235">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="01b3e-235">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="01b3e-236"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="01b3e-236"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="01b3e-237">NT tandem</span><span class="sxs-lookup"><span data-stu-id="01b3e-237">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="01b3e-238"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="01b3e-238"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="01b3e-239">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="01b3e-239">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="01b3e-240"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="01b3e-240"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="01b3e-241"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="01b3e-241"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="01b3e-242"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="01b3e-242"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="01b3e-243"><span id="VM_ESA"></span><span id="vm_esa"></span>**Machine virtuelle/SEEE** (39)</span><span class="sxs-lookup"><span data-stu-id="01b3e-243"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="01b3e-244"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactif** (40)</span><span class="sxs-lookup"><span data-stu-id="01b3e-244"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="01b3e-245"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="01b3e-245"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="01b3e-246">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="01b3e-246">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="01b3e-247"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="01b3e-247"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="01b3e-248"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="01b3e-248"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="01b3e-249"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**Hurd gnu** (44)</span><span class="sxs-lookup"><span data-stu-id="01b3e-249"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="01b3e-250"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="01b3e-250"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="01b3e-251">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="01b3e-251">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="01b3e-252"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Noyau Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="01b3e-252"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="01b3e-253"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="01b3e-253"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="01b3e-254"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="01b3e-254"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="01b3e-255"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="01b3e-255"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="01b3e-256"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="01b3e-256"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="01b3e-257"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="01b3e-257"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="01b3e-258"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menthe** (52)</span><span class="sxs-lookup"><span data-stu-id="01b3e-258"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="01b3e-259"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="01b3e-259"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="01b3e-260"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="01b3e-260"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="01b3e-261"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="01b3e-261"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="01b3e-262"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="01b3e-262"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="01b3e-263">Palm OS</span><span class="sxs-lookup"><span data-stu-id="01b3e-263">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="01b3e-264"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="01b3e-264"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="01b3e-265"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="01b3e-265"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="01b3e-266"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dédié** (59)</span><span class="sxs-lookup"><span data-stu-id="01b3e-266"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="01b3e-267"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="01b3e-267"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="01b3e-268"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="01b3e-268"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="01b3e-269">**Version**</span><span class="sxs-lookup"><span data-stu-id="01b3e-269">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01b3e-270">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="01b3e-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01b3e-271">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="01b3e-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01b3e-272">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Version**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="01b3e-272">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="01b3e-273">Version de l’opération.</span><span class="sxs-lookup"><span data-stu-id="01b3e-273">Version of the operation.</span></span>

<span data-ttu-id="01b3e-274">La version de l’opération doit se présenter sous l’une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="01b3e-274">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="01b3e-275"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="01b3e-275"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="01b3e-276"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="01b3e-276"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="01b3e-277">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="01b3e-277">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01b3e-278">Notes</span><span class="sxs-lookup"><span data-stu-id="01b3e-278">Remarks</span></span>

<span data-ttu-id="01b3e-279">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="01b3e-279">WMI does not implement this class.</span></span>

<span data-ttu-id="01b3e-280">La classe **CIM \_ MemoryCheck** est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="01b3e-280">The **CIM\_MemoryCheck** class is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<span data-ttu-id="01b3e-281">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="01b3e-281">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="01b3e-282">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="01b3e-282">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="01b3e-283">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01b3e-283">Requirements</span></span>



| <span data-ttu-id="01b3e-284">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01b3e-284">Requirement</span></span> | <span data-ttu-id="01b3e-285">Valeur</span><span class="sxs-lookup"><span data-stu-id="01b3e-285">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01b3e-286">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01b3e-286">Minimum supported client</span></span><br/> | <span data-ttu-id="01b3e-287">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01b3e-287">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="01b3e-288">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01b3e-288">Minimum supported server</span></span><br/> | <span data-ttu-id="01b3e-289">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01b3e-289">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="01b3e-290">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="01b3e-290">Namespace</span></span><br/>                | <span data-ttu-id="01b3e-291">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="01b3e-291">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="01b3e-292">MOF</span><span class="sxs-lookup"><span data-stu-id="01b3e-292">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01b3e-293"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01b3e-293"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="01b3e-294">DLL</span><span class="sxs-lookup"><span data-stu-id="01b3e-294">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01b3e-295"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01b3e-295"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01b3e-296">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01b3e-296">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01b3e-297">**\_Vérification CIM**</span><span class="sxs-lookup"><span data-stu-id="01b3e-297">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

