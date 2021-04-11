---
description: La \_ classe CIM DiskSpaceCheck vérifie la quantité d’espace disque disponible du système et la spécifie dans la propriété AvailableDiskSpace.
ms.assetid: 51440084-7713-4106-b05b-cd2827f4cb05
ms.tgt_platform: multiple
title: Classe CIM_DiskSpaceCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskSpaceCheck
- CIM_DiskSpaceCheck.CheckID
- CIM_DiskSpaceCheck.Caption
- CIM_DiskSpaceCheck.Description
- CIM_DiskSpaceCheck.CheckMode
- CIM_DiskSpaceCheck.Name
- CIM_DiskSpaceCheck.TargetOperatingSystem
- CIM_DiskSpaceCheck.Version
- CIM_DiskSpaceCheck.SoftwareElementID
- CIM_DiskSpaceCheck.SoftwareElementState
- CIM_DiskSpaceCheck.AvailableDiskSpace
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ad7452698b4969e78ee14cf4144e1f5c7883892b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110874"
---
# <a name="cim_diskspacecheck-class"></a><span data-ttu-id="76821-103">\_Classe CIM DiskSpaceCheck</span><span class="sxs-lookup"><span data-stu-id="76821-103">CIM\_DiskSpaceCheck class</span></span>

<span data-ttu-id="76821-104">La classe **CIM \_ DiskSpaceCheck** vérifie la quantité d’espace disque disponible du système et la spécifie dans la propriété **AvailableDiskSpace** .</span><span class="sxs-lookup"><span data-stu-id="76821-104">The **CIM\_DiskSpaceCheck** class checks the system's amount of available disk space and specifies it in the **AvailableDiskSpace** property.</span></span> <span data-ttu-id="76821-105">Les détails sont comparés à la valeur de la propriété **AvailableSpace** de l’objet [**CIM \_ FileSystem**](cim-filesystem.md) associé à l' [**objet \_ ComputerSystem CIM**](cim-computersystem.md) , qui décrit l’environnement système.</span><span class="sxs-lookup"><span data-stu-id="76821-105">Details are compared with the value in the **AvailableSpace** property of the [**CIM\_FileSystem**](cim-filesystem.md) object that is associated with the [**CIM\_ComputerSystem**](cim-computersystem.md) object, which describes the system environment.</span></span> <span data-ttu-id="76821-106">Lorsque la valeur de la propriété **AvailableSpace** est supérieure ou égale à la valeur spécifiée dans la propriété **AvailableDiskSpace** , la condition est satisfaite.</span><span class="sxs-lookup"><span data-stu-id="76821-106">When the value of the **AvailableSpace** property is greater than or equal to the value specified in the **AvailableDiskSpace** property, the condition is satisfied.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="76821-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="76821-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="76821-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="76821-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="76821-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="76821-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="76821-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="76821-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="76821-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76821-111">Syntax</span></span>

``` syntax
[UUID("{D3B1178A-DB29-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_DiskSpaceCheck : CIM_Check
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
  uint64  AvailableDiskSpace;
};
```

## <a name="members"></a><span data-ttu-id="76821-112">Membres</span><span class="sxs-lookup"><span data-stu-id="76821-112">Members</span></span>

<span data-ttu-id="76821-113">La classe **CIM \_ DiskSpaceCheck** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="76821-113">The **CIM\_DiskSpaceCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="76821-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="76821-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="76821-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="76821-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="76821-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="76821-116">Methods</span></span>

<span data-ttu-id="76821-117">La classe **CIM \_ DiskSpaceCheck** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="76821-117">The **CIM\_DiskSpaceCheck** class has these methods.</span></span>



| <span data-ttu-id="76821-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="76821-118">Method</span></span>                                                      | <span data-ttu-id="76821-119">Description</span><span class="sxs-lookup"><span data-stu-id="76821-119">Description</span></span>                                                   |
|:------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="76821-120">**Appeler**</span><span class="sxs-lookup"><span data-stu-id="76821-120">**Invoke**</span></span>](invoke-method-in-class-cim-diskspacecheck.md) | <span data-ttu-id="76821-121">Effectue une action particulière.</span><span class="sxs-lookup"><span data-stu-id="76821-121">Takes a particular action.</span></span> <span data-ttu-id="76821-122">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="76821-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="76821-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="76821-123">Properties</span></span>

<span data-ttu-id="76821-124">La classe **CIM \_ DiskSpaceCheck** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="76821-124">The **CIM\_DiskSpaceCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="76821-125">**AvailableDiskSpace**</span><span class="sxs-lookup"><span data-stu-id="76821-125">**AvailableDiskSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76821-126">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="76821-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="76821-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76821-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76821-128">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**AvailableSpace** "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilo-octets ")</span><span class="sxs-lookup"><span data-stu-id="76821-128">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**AvailableSpace** "), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="76821-129">Espace disque disponible.</span><span class="sxs-lookup"><span data-stu-id="76821-129">Available disk space.</span></span>

<span data-ttu-id="76821-130">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="76821-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="76821-131">**Caption**</span><span class="sxs-lookup"><span data-stu-id="76821-131">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76821-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76821-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76821-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76821-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76821-134">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="76821-134">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="76821-135">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="76821-135">A short textual description of the subject.</span></span>

<span data-ttu-id="76821-136">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="76821-136">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="76821-137">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="76821-137">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76821-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76821-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76821-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76821-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76821-140">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="76821-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="76821-141">Identificateur utilisé conjointement avec d’autres clés pour identifier de manière unique la vérification.</span><span class="sxs-lookup"><span data-stu-id="76821-141">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="76821-142">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="76821-142">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="76821-143">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="76821-143">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76821-144">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="76821-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="76821-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76821-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76821-146">Si la **valeur est true**, la condition est supposée exister dans l’environnement.</span><span class="sxs-lookup"><span data-stu-id="76821-146">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="76821-147">Par exemple, un fichier est censé se trouver sur un système. la méthode [**Invoke**](invoke-method-in-class-cim-check.md) doit donc retourner la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="76821-147">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="76821-148">Si la **valeur est false**, la condition n’est pas censée exister.</span><span class="sxs-lookup"><span data-stu-id="76821-148">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="76821-149">Par exemple, un fichier ne se trouve pas sur un système, donc la méthode [**Invoke**](invoke-method-in-class-cim-check.md) doit retourner **false**.</span><span class="sxs-lookup"><span data-stu-id="76821-149">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="76821-150">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="76821-150">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="76821-151">**Description**</span><span class="sxs-lookup"><span data-stu-id="76821-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76821-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76821-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76821-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76821-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76821-154">Description des objets.</span><span class="sxs-lookup"><span data-stu-id="76821-154">A description of the objects.</span></span>

<span data-ttu-id="76821-155">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="76821-155">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="76821-156">**Nom**</span><span class="sxs-lookup"><span data-stu-id="76821-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76821-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76821-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76821-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76821-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76821-159">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="76821-159">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="76821-160">Nom utilisé pour identifier l’élément logiciel</span><span class="sxs-lookup"><span data-stu-id="76821-160">Name used to identify the software element</span></span>

<span data-ttu-id="76821-161">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="76821-161">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="76821-162">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="76821-162">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76821-163">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76821-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76821-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76821-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76821-165">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="76821-165">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="76821-166">Il s’agit d’un identificateur pour cet élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="76821-166">This is an identifier for this software element.</span></span>

<span data-ttu-id="76821-167">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="76821-167">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="76821-168">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="76821-168">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76821-169">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76821-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76821-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76821-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76821-171">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="76821-171">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="76821-172">État de l’élément logiciel d’un élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="76821-172">The software element state of a software element.</span></span>

<span data-ttu-id="76821-173">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="76821-173">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="76821-174"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Déployable** (0)</span><span class="sxs-lookup"><span data-stu-id="76821-174"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="76821-175">Décrit les détails nécessaires à la réussite de la distribution et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État installable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="76821-175">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="76821-176"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installation** (1)</span><span class="sxs-lookup"><span data-stu-id="76821-176"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="76821-177">Décrit les détails nécessaires à l’installation réussie et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État exécutable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="76821-177">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="76821-178"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Exécutable** (2)</span><span class="sxs-lookup"><span data-stu-id="76821-178"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="76821-179">Décrit les détails nécessaires pour une exécution réussie et les détails (conditions et actions) requis pour créer un élément logiciel dans l’État en cours d’exécution (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="76821-179">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="76821-180"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**En cours d’exécution** (3)</span><span class="sxs-lookup"><span data-stu-id="76821-180"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="76821-181">Décrit les détails nécessaires à l’analyse et à l’utilisation d’un élément de début.</span><span class="sxs-lookup"><span data-stu-id="76821-181">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="76821-182">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="76821-182">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76821-183">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76821-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76821-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76821-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76821-185">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informations sur les composants logiciels DMTF \| 002,5»)</span><span class="sxs-lookup"><span data-stu-id="76821-185">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="76821-186">Système d’exploitation cible de l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="76821-186">Target operating system of the software element.</span></span>

<span data-ttu-id="76821-187">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="76821-187">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="76821-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="76821-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="76821-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="76821-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="76821-190"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="76821-190"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="76821-191">Mac OS</span><span class="sxs-lookup"><span data-stu-id="76821-191">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="76821-192"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="76821-192"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="76821-193">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="76821-193">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="76821-194"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="76821-194"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="76821-195"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="76821-195"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="76821-196"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX numérique** (6)</span><span class="sxs-lookup"><span data-stu-id="76821-196"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="76821-197"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="76821-197"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="76821-198">Ouvrir des machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="76821-198">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="76821-199"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="76821-199"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="76821-200">HP-UX</span><span class="sxs-lookup"><span data-stu-id="76821-200">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="76821-201"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="76821-201"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="76821-202"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="76821-202"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="76821-203"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="76821-203"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="76821-204"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="76821-204"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="76821-205"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="76821-205"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="76821-206">Machine virtuelle Microsoft pour Java</span><span class="sxs-lookup"><span data-stu-id="76821-206">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="76821-207"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="76821-207"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="76821-208"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="76821-208"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="76821-209">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="76821-209">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="76821-210"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="76821-210"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="76821-211">Windows 95</span><span class="sxs-lookup"><span data-stu-id="76821-211">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="76821-212"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="76821-212"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="76821-213">Windows 98</span><span class="sxs-lookup"><span data-stu-id="76821-213">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="76821-214"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="76821-214"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="76821-215">Windows NT</span><span class="sxs-lookup"><span data-stu-id="76821-215">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="76821-216"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="76821-216"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="76821-217">Windows CE</span><span class="sxs-lookup"><span data-stu-id="76821-217">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="76821-218"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="76821-218"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="76821-219">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="76821-219">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="76821-220"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="76821-220"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="76821-221"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="76821-221"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="76821-222"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="76821-222"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="76821-223"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Dépendant d’UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="76821-223"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="76821-224"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="76821-224"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="76821-225"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="76821-225"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="76821-226"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="76821-226"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="76821-227"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="76821-227"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="76821-228"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="76821-228"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="76821-229"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="76821-229"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="76821-230"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="76821-230"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="76821-231"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="76821-231"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="76821-232">Une série</span><span class="sxs-lookup"><span data-stu-id="76821-232">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="76821-233"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="76821-233"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="76821-234">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="76821-234">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="76821-235"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="76821-235"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="76821-236">NT tandem</span><span class="sxs-lookup"><span data-stu-id="76821-236">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="76821-237"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="76821-237"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="76821-238">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="76821-238">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="76821-239"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="76821-239"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="76821-240"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="76821-240"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="76821-241"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="76821-241"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="76821-242"><span id="VM_ESA"></span><span id="vm_esa"></span>**Machine virtuelle/SEEE** (39)</span><span class="sxs-lookup"><span data-stu-id="76821-242"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="76821-243"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactif** (40)</span><span class="sxs-lookup"><span data-stu-id="76821-243"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="76821-244"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="76821-244"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="76821-245">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="76821-245">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="76821-246"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="76821-246"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="76821-247"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="76821-247"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="76821-248"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**Hurd gnu** (44)</span><span class="sxs-lookup"><span data-stu-id="76821-248"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="76821-249"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="76821-249"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="76821-250">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="76821-250">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="76821-251"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Noyau Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="76821-251"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="76821-252"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="76821-252"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="76821-253"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="76821-253"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="76821-254"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="76821-254"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="76821-255"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="76821-255"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="76821-256"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="76821-256"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="76821-257"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menthe** (52)</span><span class="sxs-lookup"><span data-stu-id="76821-257"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="76821-258"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="76821-258"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="76821-259"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="76821-259"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="76821-260"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="76821-260"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="76821-261"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="76821-261"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="76821-262">Palm OS</span><span class="sxs-lookup"><span data-stu-id="76821-262">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="76821-263"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="76821-263"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="76821-264"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="76821-264"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="76821-265"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dédié** (59)</span><span class="sxs-lookup"><span data-stu-id="76821-265"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="76821-266"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="76821-266"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="76821-267"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="76821-267"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="76821-268">**Version**</span><span class="sxs-lookup"><span data-stu-id="76821-268">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76821-269">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76821-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76821-270">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76821-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76821-271">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Version**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="76821-271">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="76821-272">Version de l’opération.</span><span class="sxs-lookup"><span data-stu-id="76821-272">Version of the operation.</span></span>

<span data-ttu-id="76821-273">La version de l’opération doit se présenter sous l’une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="76821-273">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="76821-274"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="76821-274"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="76821-275"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="76821-275"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="76821-276">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="76821-276">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76821-277">Notes</span><span class="sxs-lookup"><span data-stu-id="76821-277">Remarks</span></span>

<span data-ttu-id="76821-278">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="76821-278">WMI does not implement this class.</span></span>

<span data-ttu-id="76821-279">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="76821-279">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="76821-280">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="76821-280">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="76821-281">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76821-281">Requirements</span></span>



| <span data-ttu-id="76821-282">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76821-282">Requirement</span></span> | <span data-ttu-id="76821-283">Valeur</span><span class="sxs-lookup"><span data-stu-id="76821-283">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76821-284">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76821-284">Minimum supported client</span></span><br/> | <span data-ttu-id="76821-285">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76821-285">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="76821-286">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76821-286">Minimum supported server</span></span><br/> | <span data-ttu-id="76821-287">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76821-287">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="76821-288">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="76821-288">Namespace</span></span><br/>                | <span data-ttu-id="76821-289">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="76821-289">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="76821-290">MOF</span><span class="sxs-lookup"><span data-stu-id="76821-290">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76821-291"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="76821-291"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="76821-292">DLL</span><span class="sxs-lookup"><span data-stu-id="76821-292">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76821-293"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76821-293"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76821-294">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76821-294">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76821-295">**\_Vérification CIM**</span><span class="sxs-lookup"><span data-stu-id="76821-295">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

