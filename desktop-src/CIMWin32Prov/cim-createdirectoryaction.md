---
description: La \_ classe CIM CreateDirectoryAction crée des répertoires vides pour les éléments logiciels à installer localement.
ms.assetid: e8587534-4bb3-44de-98a1-8d777f1da1b3
ms.tgt_platform: multiple
title: Classe CIM_CreateDirectoryAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CreateDirectoryAction
- CIM_CreateDirectoryAction.ActionID
- CIM_CreateDirectoryAction.Caption
- CIM_CreateDirectoryAction.Description
- CIM_CreateDirectoryAction.Direction
- CIM_CreateDirectoryAction.Name
- CIM_CreateDirectoryAction.SoftwareElementID
- CIM_CreateDirectoryAction.SoftwareElementState
- CIM_CreateDirectoryAction.TargetOperatingSystem
- CIM_CreateDirectoryAction.Version
- CIM_CreateDirectoryAction.DirectoryName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f7d0c2fb8d255a02d6df6f6677a31fa3366dfa6f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861278"
---
# <a name="cim_createdirectoryaction-class"></a><span data-ttu-id="4d07a-103">\_Classe CIM CreateDirectoryAction</span><span class="sxs-lookup"><span data-stu-id="4d07a-103">CIM\_CreateDirectoryAction class</span></span>

<span data-ttu-id="4d07a-104">La classe **CIM \_ CreateDirectoryAction** crée des répertoires vides pour les éléments logiciels à installer localement.</span><span class="sxs-lookup"><span data-stu-id="4d07a-104">The **CIM\_CreateDirectoryAction** class creates empty directories for software elements to be installed locally.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4d07a-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="4d07a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4d07a-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4d07a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4d07a-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4d07a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4d07a-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="4d07a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d07a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d07a-109">Syntax</span></span>

``` syntax
[UUID("{87946AAC-DB22-11d2-85FC-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_CreateDirectoryAction : CIM_DirectoryAction
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
  string DirectoryName;
};
```

## <a name="members"></a><span data-ttu-id="4d07a-110">Membres</span><span class="sxs-lookup"><span data-stu-id="4d07a-110">Members</span></span>

<span data-ttu-id="4d07a-111">La classe **CIM \_ CreateDirectoryAction** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4d07a-111">The **CIM\_CreateDirectoryAction** class has these types of members:</span></span>

-   [<span data-ttu-id="4d07a-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4d07a-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="4d07a-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4d07a-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4d07a-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4d07a-114">Methods</span></span>

<span data-ttu-id="4d07a-115">La classe **CIM \_ CreateDirectoryAction** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4d07a-115">The **CIM\_CreateDirectoryAction** class has these methods.</span></span>



| <span data-ttu-id="4d07a-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="4d07a-116">Method</span></span>                                                             | <span data-ttu-id="4d07a-117">Description</span><span class="sxs-lookup"><span data-stu-id="4d07a-117">Description</span></span>                                                                                                                                  |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d07a-118">**Appeler**</span><span class="sxs-lookup"><span data-stu-id="4d07a-118">**Invoke**</span></span>](invoke-method-in-class-cim-createdirectoryaction.md) | <span data-ttu-id="4d07a-119">Effectue une action particulière.</span><span class="sxs-lookup"><span data-stu-id="4d07a-119">Takes a particular action.</span></span> <span data-ttu-id="4d07a-120">Les détails de la façon dont la méthode exécute l’action sont spécifiques à l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="4d07a-120">The details of how the method performs the action are implementation-specific.</span></span> <span data-ttu-id="4d07a-121">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="4d07a-121">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4d07a-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4d07a-122">Properties</span></span>

<span data-ttu-id="4d07a-123">La classe **CIM \_ CreateDirectoryAction** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4d07a-123">The **CIM\_CreateDirectoryAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4d07a-124">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="4d07a-124">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d07a-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4d07a-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d07a-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d07a-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d07a-127">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="4d07a-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4d07a-128">Identificateur unique affecté à une action particulière pour un élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="4d07a-128">Unique identifier assigned to a particular action for a software element.</span></span>

<span data-ttu-id="4d07a-129">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="4d07a-129">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d07a-130">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4d07a-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d07a-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4d07a-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d07a-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d07a-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d07a-133">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="4d07a-133">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4d07a-134">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4d07a-134">Short textual description of the object.</span></span>

<span data-ttu-id="4d07a-135">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="4d07a-135">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d07a-136">**Description**</span><span class="sxs-lookup"><span data-stu-id="4d07a-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d07a-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4d07a-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d07a-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d07a-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d07a-139">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4d07a-139">Description of the object.</span></span>

<span data-ttu-id="4d07a-140">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="4d07a-140">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d07a-141">**Sens**</span><span class="sxs-lookup"><span data-stu-id="4d07a-141">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d07a-142">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4d07a-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4d07a-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d07a-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d07a-144">Indique si un objet [**d' \_ action CIM**](cim-action.md) particulier fait partie d’une séquence d’actions pour faire passer l’élément logiciel actuel à son état suivant, tel que « installer », ou pour supprimer l’élément logiciel actuel, tel que « désinstaller ».</span><span class="sxs-lookup"><span data-stu-id="4d07a-144">Indicates whether a particular [**CIM\_Action**](cim-action.md) object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<span data-ttu-id="4d07a-145">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="4d07a-145">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="4d07a-146">**Installer** (0)</span><span class="sxs-lookup"><span data-stu-id="4d07a-146">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="4d07a-147">**Désinstaller** (1)</span><span class="sxs-lookup"><span data-stu-id="4d07a-147">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4d07a-148">**DirectoryName**</span><span class="sxs-lookup"><span data-stu-id="4d07a-148">**DirectoryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d07a-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4d07a-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d07a-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d07a-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d07a-151">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="4d07a-151">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="4d07a-152">Nom du répertoire auquel s’applique l’action.</span><span class="sxs-lookup"><span data-stu-id="4d07a-152">Name of the directory to which the action applies.</span></span>

<span data-ttu-id="4d07a-153">Cette propriété est héritée de la [**\_ DirectoryAction CIM**](cim-directoryaction.md).</span><span class="sxs-lookup"><span data-stu-id="4d07a-153">This property is inherited from [**CIM\_DirectoryAction**](cim-directoryaction.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d07a-154">**Nom**</span><span class="sxs-lookup"><span data-stu-id="4d07a-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d07a-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4d07a-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d07a-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d07a-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d07a-157">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="4d07a-157">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4d07a-158">Identifie l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="4d07a-158">Identifies the software element.</span></span>

<span data-ttu-id="4d07a-159">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="4d07a-159">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d07a-160">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="4d07a-160">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d07a-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4d07a-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d07a-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d07a-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d07a-163">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="4d07a-163">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4d07a-164">Identificateur de l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="4d07a-164">Identifier for the software element.</span></span>

<span data-ttu-id="4d07a-165">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="4d07a-165">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d07a-166">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="4d07a-166">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d07a-167">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4d07a-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4d07a-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d07a-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d07a-169">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4d07a-169">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4d07a-170">État d’un élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="4d07a-170">State of a software element.</span></span>

<span data-ttu-id="4d07a-171">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="4d07a-171">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="4d07a-172"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Déployable** (0)</span><span class="sxs-lookup"><span data-stu-id="4d07a-172"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4d07a-173">Décrit les détails nécessaires à la réussite de la distribution et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État installable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="4d07a-173">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="4d07a-174"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installation** (1)</span><span class="sxs-lookup"><span data-stu-id="4d07a-174"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4d07a-175">Décrit les détails nécessaires à l’installation réussie et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État exécutable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="4d07a-175">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="4d07a-176"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Exécutable** (2)</span><span class="sxs-lookup"><span data-stu-id="4d07a-176"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4d07a-177">Décrit les détails nécessaires pour une exécution réussie et les détails (conditions et actions) requis pour créer un élément logiciel dans l’État en cours d’exécution (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="4d07a-177">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="4d07a-178"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**En cours d’exécution** (3)</span><span class="sxs-lookup"><span data-stu-id="4d07a-178"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4d07a-179">Décrit les détails nécessaires à l’analyse et à l’utilisation d’un élément de début.</span><span class="sxs-lookup"><span data-stu-id="4d07a-179">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d07a-180">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="4d07a-180">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d07a-181">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4d07a-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4d07a-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d07a-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d07a-183">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informations sur les composants logiciels DMTF \| 002,5»)</span><span class="sxs-lookup"><span data-stu-id="4d07a-183">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="4d07a-184">Système d’exploitation cible de l’élément logiciel propriétaire.</span><span class="sxs-lookup"><span data-stu-id="4d07a-184">Target operating system of the owning software element.</span></span>

<span data-ttu-id="4d07a-185">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="4d07a-185">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4d07a-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="4d07a-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4d07a-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="4d07a-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="4d07a-188"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="4d07a-188"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4d07a-189">Mac OS</span><span class="sxs-lookup"><span data-stu-id="4d07a-189">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="4d07a-190"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="4d07a-190"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="4d07a-191"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="4d07a-191"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="4d07a-192"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="4d07a-192"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="4d07a-193"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX numérique** (6)</span><span class="sxs-lookup"><span data-stu-id="4d07a-193"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="4d07a-194"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="4d07a-194"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="4d07a-195">Ouvrir des machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="4d07a-195">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="4d07a-196"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="4d07a-196"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="4d07a-197">HP-UX</span><span class="sxs-lookup"><span data-stu-id="4d07a-197">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="4d07a-198"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="4d07a-198"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="4d07a-199"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="4d07a-199"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="4d07a-200"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="4d07a-200"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="4d07a-201"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="4d07a-201"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="4d07a-202"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="4d07a-202"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="4d07a-203">Machine virtuelle Microsoft pour Java</span><span class="sxs-lookup"><span data-stu-id="4d07a-203">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="4d07a-204"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="4d07a-204"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="4d07a-205"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="4d07a-205"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="4d07a-206">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="4d07a-206">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="4d07a-207"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="4d07a-207"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="4d07a-208">Windows 95</span><span class="sxs-lookup"><span data-stu-id="4d07a-208">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="4d07a-209"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="4d07a-209"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="4d07a-210">Windows 98</span><span class="sxs-lookup"><span data-stu-id="4d07a-210">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="4d07a-211"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="4d07a-211"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="4d07a-212">Windows NT</span><span class="sxs-lookup"><span data-stu-id="4d07a-212">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="4d07a-213"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="4d07a-213"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="4d07a-214">Windows CE</span><span class="sxs-lookup"><span data-stu-id="4d07a-214">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="4d07a-215"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="4d07a-215"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="4d07a-216">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="4d07a-216">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="4d07a-217"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="4d07a-217"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="4d07a-218"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="4d07a-218"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="4d07a-219"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="4d07a-219"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="4d07a-220"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Dépendant d’UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="4d07a-220"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="4d07a-221"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="4d07a-221"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="4d07a-222"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="4d07a-222"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="4d07a-223"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="4d07a-223"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="4d07a-224"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="4d07a-224"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="4d07a-225"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="4d07a-225"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="4d07a-226"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="4d07a-226"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="4d07a-227"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="4d07a-227"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="4d07a-228"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="4d07a-228"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="4d07a-229">Une série</span><span class="sxs-lookup"><span data-stu-id="4d07a-229">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="4d07a-230"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="4d07a-230"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="4d07a-231">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="4d07a-231">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="4d07a-232"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="4d07a-232"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="4d07a-233">NT tandem</span><span class="sxs-lookup"><span data-stu-id="4d07a-233">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="4d07a-234"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="4d07a-234"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="4d07a-235">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="4d07a-235">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="4d07a-236"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="4d07a-236"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="4d07a-237"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="4d07a-237"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="4d07a-238"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="4d07a-238"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="4d07a-239"><span id="VM_ESA"></span><span id="vm_esa"></span>**Machine virtuelle/SEEE** (39)</span><span class="sxs-lookup"><span data-stu-id="4d07a-239"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="4d07a-240"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactif** (40)</span><span class="sxs-lookup"><span data-stu-id="4d07a-240"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="4d07a-241"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="4d07a-241"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="4d07a-242">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="4d07a-242">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="4d07a-243"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="4d07a-243"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="4d07a-244"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="4d07a-244"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="4d07a-245"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**Hurd gnu** (44)</span><span class="sxs-lookup"><span data-stu-id="4d07a-245"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="4d07a-246"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="4d07a-246"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="4d07a-247">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="4d07a-247">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="4d07a-248"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Noyau Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="4d07a-248"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="4d07a-249"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="4d07a-249"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="4d07a-250"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="4d07a-250"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="4d07a-251"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="4d07a-251"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="4d07a-252"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="4d07a-252"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="4d07a-253"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="4d07a-253"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="4d07a-254"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menthe** (52)</span><span class="sxs-lookup"><span data-stu-id="4d07a-254"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="4d07a-255"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="4d07a-255"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="4d07a-256">Être un système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="4d07a-256">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="4d07a-257"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="4d07a-257"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="4d07a-258"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="4d07a-258"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="4d07a-259"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="4d07a-259"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="4d07a-260">Palm OS</span><span class="sxs-lookup"><span data-stu-id="4d07a-260">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="4d07a-261"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="4d07a-261"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="4d07a-262"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="4d07a-262"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="4d07a-263"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dédié** (59)</span><span class="sxs-lookup"><span data-stu-id="4d07a-263"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="4d07a-264"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="4d07a-264"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="4d07a-265"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="4d07a-265"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4d07a-266">**Version**</span><span class="sxs-lookup"><span data-stu-id="4d07a-266">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d07a-267">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4d07a-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d07a-268">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d07a-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d07a-269">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Version**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="4d07a-269">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="4d07a-270">Version de l’opération.</span><span class="sxs-lookup"><span data-stu-id="4d07a-270">Version of the operation.</span></span>

<span data-ttu-id="4d07a-271">La version de l’opération doit se présenter sous l’une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="4d07a-271">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="4d07a-272"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="4d07a-272"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="4d07a-273"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="4d07a-273"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="4d07a-274">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="4d07a-274">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d07a-275">Notes</span><span class="sxs-lookup"><span data-stu-id="4d07a-275">Remarks</span></span>

<span data-ttu-id="4d07a-276">La classe **CIM \_ CreateDirectoryAction** est dérivée de [**CIM \_ DirectoryAction**](cim-directoryaction.md).</span><span class="sxs-lookup"><span data-stu-id="4d07a-276">The **CIM\_CreateDirectoryAction** class is derived from [**CIM\_DirectoryAction**](cim-directoryaction.md).</span></span>

<span data-ttu-id="4d07a-277">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="4d07a-277">WMI does not implement this class.</span></span> <span data-ttu-id="4d07a-278">Pour les classes dérivées de **CIM \_ CreateDirectoryAction**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4d07a-278">For classes derived from **CIM\_CreateDirectoryAction**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="4d07a-279">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="4d07a-279">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4d07a-280">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="4d07a-280">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d07a-281">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d07a-281">Requirements</span></span>



| <span data-ttu-id="4d07a-282">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d07a-282">Requirement</span></span> | <span data-ttu-id="4d07a-283">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d07a-283">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d07a-284">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d07a-284">Minimum supported client</span></span><br/> | <span data-ttu-id="4d07a-285">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d07a-285">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4d07a-286">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d07a-286">Minimum supported server</span></span><br/> | <span data-ttu-id="4d07a-287">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d07a-287">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4d07a-288">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4d07a-288">Namespace</span></span><br/>                | <span data-ttu-id="4d07a-289">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="4d07a-289">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4d07a-290">MOF</span><span class="sxs-lookup"><span data-stu-id="4d07a-290">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d07a-291"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d07a-291"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d07a-292">DLL</span><span class="sxs-lookup"><span data-stu-id="4d07a-292">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d07a-293"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d07a-293"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d07a-294">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d07a-294">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d07a-295">**\_DIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="4d07a-295">**CIM\_DirectoryAction**</span></span>](cim-directoryaction.md)
</dt> </dl>

 

