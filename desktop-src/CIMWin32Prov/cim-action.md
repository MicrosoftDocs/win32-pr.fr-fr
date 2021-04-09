---
description: Une \_ classe d’action CIM est une opération qui fait partie d’un processus de création d’un élément logiciel dans son état suivant ou d’élimination de l’élément logiciel dans l’état actuel.
ms.assetid: d1f72aaf-7e26-414f-99e7-ff8f14d66360
ms.tgt_platform: multiple
title: Classe CIM_Action
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Action
- CIM_Action.ActionID
- CIM_Action.Caption
- CIM_Action.Description
- CIM_Action.Direction
- CIM_Action.Name
- CIM_Action.SoftwareElementID
- CIM_Action.SoftwareElementState
- CIM_Action.TargetOperatingSystem
- CIM_Action.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a5f37fa4b62c1e8b678533de4abaa7f6a172904e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110527"
---
# <a name="cim_action-class"></a><span data-ttu-id="1510c-103">\_Classe d’action CIM</span><span class="sxs-lookup"><span data-stu-id="1510c-103">CIM\_Action class</span></span>

<span data-ttu-id="1510c-104">Une classe d' **\_ action CIM** est une opération qui fait partie d’un processus de création d’un élément logiciel dans son état suivant ou d’élimination de l’élément logiciel dans l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="1510c-104">A **CIM\_Action** class is an operation that is part of a process to either create a software element in its next state or to eliminate the software element in the current state.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1510c-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="1510c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1510c-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1510c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1510c-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="1510c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1510c-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="1510c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1510c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1510c-109">Syntax</span></span>

``` syntax
[UUID("{2F156260-DB21-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_Action
{
  string ActionID;
  string Caption;
  string Description;
  uint16 Direction;
  string Name;
  string SoftwareElementID;
  uint16 SoftwareElementState;
  uint16 TargetOperatingSystem;
  string Version;
};
```

## <a name="members"></a><span data-ttu-id="1510c-110">Membres</span><span class="sxs-lookup"><span data-stu-id="1510c-110">Members</span></span>

<span data-ttu-id="1510c-111">La classe d' **\_ action CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1510c-111">The **CIM\_Action** class has these types of members:</span></span>

-   [<span data-ttu-id="1510c-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1510c-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="1510c-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1510c-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1510c-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1510c-114">Methods</span></span>

<span data-ttu-id="1510c-115">La classe d' **\_ action CIM** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="1510c-115">The **CIM\_Action** class has these methods.</span></span>



| <span data-ttu-id="1510c-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="1510c-116">Method</span></span>                                              | <span data-ttu-id="1510c-117">Description</span><span class="sxs-lookup"><span data-stu-id="1510c-117">Description</span></span>                                                   |
|:----------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="1510c-118">**Appeler**</span><span class="sxs-lookup"><span data-stu-id="1510c-118">**Invoke**</span></span>](invoke-method-in-class-cim-action.md) | <span data-ttu-id="1510c-119">Effectue une action particulière.</span><span class="sxs-lookup"><span data-stu-id="1510c-119">Takes a particular action.</span></span> <span data-ttu-id="1510c-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="1510c-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1510c-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1510c-121">Properties</span></span>

<span data-ttu-id="1510c-122">La classe d' **\_ action CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="1510c-122">The **CIM\_Action** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1510c-123">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="1510c-123">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1510c-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1510c-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1510c-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1510c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1510c-126">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1510c-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1510c-127">Identificateur unique affecté à une action particulière pour un élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="1510c-127">Unique identifier assigned to a particular action for a software element.</span></span>

</dd> <dt>

<span data-ttu-id="1510c-128">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1510c-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1510c-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1510c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1510c-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1510c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1510c-131">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1510c-131">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1510c-132">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1510c-132">Short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="1510c-133">**Description**</span><span class="sxs-lookup"><span data-stu-id="1510c-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1510c-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1510c-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1510c-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1510c-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1510c-136">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1510c-136">Description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="1510c-137">**Sens**</span><span class="sxs-lookup"><span data-stu-id="1510c-137">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1510c-138">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1510c-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1510c-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1510c-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1510c-140">Indique si un objet **d' \_ action CIM** particulier fait partie d’une séquence d’actions pour faire passer l’élément logiciel actuel à son état suivant, tel que « installer », ou pour supprimer l’élément logiciel actuel, tel que « désinstaller ».</span><span class="sxs-lookup"><span data-stu-id="1510c-140">Indicates whether a particular **CIM\_Action** object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="1510c-141">**Installer** (0)</span><span class="sxs-lookup"><span data-stu-id="1510c-141">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="1510c-142">**Désinstaller** (1)</span><span class="sxs-lookup"><span data-stu-id="1510c-142">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1510c-143">**Nom**</span><span class="sxs-lookup"><span data-stu-id="1510c-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1510c-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1510c-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1510c-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1510c-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1510c-146">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1510c-146">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1510c-147">Identifie l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="1510c-147">Identifies the software element.</span></span>

</dd> <dt>

<span data-ttu-id="1510c-148">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="1510c-148">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1510c-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1510c-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1510c-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1510c-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1510c-151">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1510c-151">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1510c-152">Identificateur de l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="1510c-152">Identifier for the software element.</span></span>

</dd> <dt>

<span data-ttu-id="1510c-153">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="1510c-153">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1510c-154">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1510c-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1510c-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1510c-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1510c-156">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1510c-156">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1510c-157">État d’un élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="1510c-157">State of a software element.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="1510c-158"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Déployable** (0)</span><span class="sxs-lookup"><span data-stu-id="1510c-158"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1510c-159">Décrit les détails nécessaires à la réussite de la distribution et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État installable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="1510c-159">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="1510c-160"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installation** (1)</span><span class="sxs-lookup"><span data-stu-id="1510c-160"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1510c-161">Décrit les détails nécessaires à l’installation réussie et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État exécutable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="1510c-161">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="1510c-162"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Exécutable** (2)</span><span class="sxs-lookup"><span data-stu-id="1510c-162"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1510c-163">Décrit les détails nécessaires pour une exécution réussie et les détails (conditions et actions) requis pour créer un élément logiciel dans l’État en cours d’exécution (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="1510c-163">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="1510c-164"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**En cours d’exécution** (3)</span><span class="sxs-lookup"><span data-stu-id="1510c-164"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1510c-165">Décrit les détails nécessaires à l’analyse et à l’utilisation d’un élément de début.</span><span class="sxs-lookup"><span data-stu-id="1510c-165">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1510c-166">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="1510c-166">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1510c-167">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1510c-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1510c-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1510c-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1510c-169">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informations sur les composants logiciels DMTF \| 002,5»)</span><span class="sxs-lookup"><span data-stu-id="1510c-169">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="1510c-170">Système d’exploitation cible de l’élément logiciel propriétaire.</span><span class="sxs-lookup"><span data-stu-id="1510c-170">Target operating system of the owning software element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1510c-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="1510c-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1510c-172"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="1510c-172"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="1510c-173"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="1510c-173"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1510c-174">Mac OS</span><span class="sxs-lookup"><span data-stu-id="1510c-174">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="1510c-175"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="1510c-175"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="1510c-176"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="1510c-176"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="1510c-177"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="1510c-177"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="1510c-178"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX numérique** (6)</span><span class="sxs-lookup"><span data-stu-id="1510c-178"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="1510c-179"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="1510c-179"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="1510c-180">Ouvrir des machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="1510c-180">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="1510c-181"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="1510c-181"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="1510c-182">HP-UX</span><span class="sxs-lookup"><span data-stu-id="1510c-182">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="1510c-183"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="1510c-183"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="1510c-184"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="1510c-184"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="1510c-185"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="1510c-185"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="1510c-186"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="1510c-186"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="1510c-187"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="1510c-187"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="1510c-188">Machine virtuelle Microsoft pour Java</span><span class="sxs-lookup"><span data-stu-id="1510c-188">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="1510c-189"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="1510c-189"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="1510c-190"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="1510c-190"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="1510c-191">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="1510c-191">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="1510c-192"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="1510c-192"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="1510c-193">Windows 95</span><span class="sxs-lookup"><span data-stu-id="1510c-193">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="1510c-194"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="1510c-194"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="1510c-195">Windows 98</span><span class="sxs-lookup"><span data-stu-id="1510c-195">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="1510c-196"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="1510c-196"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="1510c-197">Windows NT</span><span class="sxs-lookup"><span data-stu-id="1510c-197">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="1510c-198"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="1510c-198"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="1510c-199">Windows CE</span><span class="sxs-lookup"><span data-stu-id="1510c-199">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="1510c-200"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="1510c-200"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1510c-201">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="1510c-201">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="1510c-202"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="1510c-202"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="1510c-203"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="1510c-203"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="1510c-204"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="1510c-204"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="1510c-205"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Dépendant d’UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="1510c-205"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="1510c-206"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="1510c-206"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="1510c-207"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="1510c-207"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="1510c-208"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="1510c-208"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="1510c-209"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="1510c-209"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="1510c-210"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="1510c-210"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="1510c-211"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="1510c-211"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="1510c-212"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="1510c-212"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="1510c-213"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="1510c-213"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="1510c-214">Une série</span><span class="sxs-lookup"><span data-stu-id="1510c-214">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="1510c-215"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="1510c-215"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="1510c-216">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="1510c-216">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="1510c-217"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="1510c-217"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="1510c-218">NT tandem</span><span class="sxs-lookup"><span data-stu-id="1510c-218">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="1510c-219"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="1510c-219"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="1510c-220">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="1510c-220">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="1510c-221"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="1510c-221"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="1510c-222"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="1510c-222"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="1510c-223"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="1510c-223"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="1510c-224"><span id="VM_ESA"></span><span id="vm_esa"></span>**Machine virtuelle/SEEE** (39)</span><span class="sxs-lookup"><span data-stu-id="1510c-224"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="1510c-225"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactif** (40)</span><span class="sxs-lookup"><span data-stu-id="1510c-225"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="1510c-226"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="1510c-226"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="1510c-227">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="1510c-227">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="1510c-228"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="1510c-228"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="1510c-229"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="1510c-229"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="1510c-230"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**Hurd gnu** (44)</span><span class="sxs-lookup"><span data-stu-id="1510c-230"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="1510c-231"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="1510c-231"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="1510c-232">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="1510c-232">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="1510c-233"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Noyau Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="1510c-233"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="1510c-234"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="1510c-234"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="1510c-235"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="1510c-235"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="1510c-236"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="1510c-236"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="1510c-237"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="1510c-237"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="1510c-238"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="1510c-238"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="1510c-239"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menthe** (52)</span><span class="sxs-lookup"><span data-stu-id="1510c-239"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="1510c-240"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="1510c-240"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="1510c-241">Être un système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="1510c-241">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="1510c-242"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="1510c-242"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="1510c-243"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="1510c-243"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="1510c-244"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="1510c-244"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="1510c-245">Palm OS</span><span class="sxs-lookup"><span data-stu-id="1510c-245">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="1510c-246"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="1510c-246"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="1510c-247"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="1510c-247"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="1510c-248"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dédié** (59)</span><span class="sxs-lookup"><span data-stu-id="1510c-248"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="1510c-249"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="1510c-249"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="1510c-250"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="1510c-250"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1510c-251">**Version**</span><span class="sxs-lookup"><span data-stu-id="1510c-251">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1510c-252">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1510c-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1510c-253">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1510c-253">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1510c-254">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Version**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="1510c-254">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="1510c-255">Version de l’opération.</span><span class="sxs-lookup"><span data-stu-id="1510c-255">Version of the operation.</span></span>

<span data-ttu-id="1510c-256">La version de l’opération doit se présenter sous l’une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="1510c-256">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="1510c-257"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="1510c-257"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="1510c-258"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="1510c-258"><major>.<minor><letter><revision></span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1510c-259">Notes</span><span class="sxs-lookup"><span data-stu-id="1510c-259">Remarks</span></span>

<span data-ttu-id="1510c-260">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="1510c-260">WMI does not implement this class.</span></span> <span data-ttu-id="1510c-261">Consultez [classes Win32](win32-provider.md) pour les classes dérivées de l' **\_ action CIM**.</span><span class="sxs-lookup"><span data-stu-id="1510c-261">See [Win32 Classes](win32-provider.md) for classes derived from **CIM\_Action**.</span></span>

<span data-ttu-id="1510c-262">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="1510c-262">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1510c-263">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="1510c-263">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1510c-264">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1510c-264">Requirements</span></span>



| <span data-ttu-id="1510c-265">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1510c-265">Requirement</span></span> | <span data-ttu-id="1510c-266">Valeur</span><span class="sxs-lookup"><span data-stu-id="1510c-266">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1510c-267">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1510c-267">Minimum supported client</span></span><br/> | <span data-ttu-id="1510c-268">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1510c-268">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1510c-269">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1510c-269">Minimum supported server</span></span><br/> | <span data-ttu-id="1510c-270">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1510c-270">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1510c-271">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1510c-271">Namespace</span></span><br/>                | <span data-ttu-id="1510c-272">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="1510c-272">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1510c-273">MOF</span><span class="sxs-lookup"><span data-stu-id="1510c-273">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1510c-274"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1510c-274"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1510c-275">DLL</span><span class="sxs-lookup"><span data-stu-id="1510c-275">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1510c-276"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1510c-276"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1510c-277">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1510c-277">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1510c-278">Classes CIM</span><span class="sxs-lookup"><span data-stu-id="1510c-278">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

