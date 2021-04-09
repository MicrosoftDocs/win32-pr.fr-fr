---
description: La \_ classe abstraite CIM DirectoryAction gère les répertoires. La création de répertoires est gérée par la \_ classe CIM CreateDirectoryAction et la suppression des répertoires est gérée par la \_ classe CIM RemoveDirectoryAction.
ms.assetid: 3c1e7023-cf54-4321-a340-b8616300c4c0
ms.tgt_platform: multiple
title: Classe CIM_DirectoryAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectoryAction
- CIM_DirectoryAction.ActionID
- CIM_DirectoryAction.Caption
- CIM_DirectoryAction.Description
- CIM_DirectoryAction.Direction
- CIM_DirectoryAction.Name
- CIM_DirectoryAction.SoftwareElementID
- CIM_DirectoryAction.SoftwareElementState
- CIM_DirectoryAction.TargetOperatingSystem
- CIM_DirectoryAction.Version
- CIM_DirectoryAction.DirectoryName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 130284e8cf19640e7861b17d80a4612b130f7062
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861405"
---
# <a name="cim_directoryaction-class"></a><span data-ttu-id="b21c0-104">\_Classe CIM DirectoryAction</span><span class="sxs-lookup"><span data-stu-id="b21c0-104">CIM\_DirectoryAction class</span></span>

<span data-ttu-id="b21c0-105">La classe abstraite **CIM \_ DirectoryAction** gère les répertoires.</span><span class="sxs-lookup"><span data-stu-id="b21c0-105">The **CIM\_DirectoryAction** abstract class manages directories.</span></span> <span data-ttu-id="b21c0-106">La création de répertoires est gérée par la classe [**CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md) et la suppression des répertoires est gérée par la classe [**CIM \_ RemoveDirectoryAction**](cim-removedirectoryaction.md) .</span><span class="sxs-lookup"><span data-stu-id="b21c0-106">Directory creation is handled by the [**CIM\_CreateDirectoryAction**](cim-createdirectoryaction.md) class and directory removal is handled by the [**CIM\_RemoveDirectoryAction**](cim-removedirectoryaction.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b21c0-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="b21c0-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b21c0-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b21c0-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b21c0-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b21c0-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b21c0-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="b21c0-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b21c0-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b21c0-111">Syntax</span></span>

``` syntax
[UUID("{8875A39E-DB29-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_DirectoryAction : CIM_Action
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

## <a name="members"></a><span data-ttu-id="b21c0-112">Membres</span><span class="sxs-lookup"><span data-stu-id="b21c0-112">Members</span></span>

<span data-ttu-id="b21c0-113">La classe **CIM \_ DirectoryAction** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b21c0-113">The **CIM\_DirectoryAction** class has these types of members:</span></span>

-   [<span data-ttu-id="b21c0-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b21c0-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="b21c0-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b21c0-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b21c0-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b21c0-116">Methods</span></span>

<span data-ttu-id="b21c0-117">La classe **CIM \_ DirectoryAction** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b21c0-117">The **CIM\_DirectoryAction** class has these methods.</span></span>



| <span data-ttu-id="b21c0-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="b21c0-118">Method</span></span>                                                       | <span data-ttu-id="b21c0-119">Description</span><span class="sxs-lookup"><span data-stu-id="b21c0-119">Description</span></span>                                                                  |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="b21c0-120">**Appeler**</span><span class="sxs-lookup"><span data-stu-id="b21c0-120">**Invoke**</span></span>](invoke-method-in-class-cim-directoryaction.md) | <span data-ttu-id="b21c0-121">Effectue une action particulière.</span><span class="sxs-lookup"><span data-stu-id="b21c0-121">Takes a particular action.</span></span> <span data-ttu-id="b21c0-122">Cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="b21c0-122">This method is not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b21c0-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b21c0-123">Properties</span></span>

<span data-ttu-id="b21c0-124">La classe **CIM \_ DirectoryAction** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b21c0-124">The **CIM\_DirectoryAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b21c0-125">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="b21c0-125">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b21c0-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b21c0-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b21c0-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b21c0-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b21c0-128">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b21c0-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b21c0-129">Identificateur unique affecté à une action particulière pour un élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="b21c0-129">Unique identifier assigned to a particular action for a software element.</span></span>

<span data-ttu-id="b21c0-130">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="b21c0-130">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="b21c0-131">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b21c0-131">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b21c0-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b21c0-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b21c0-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b21c0-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b21c0-134">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b21c0-134">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b21c0-135">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b21c0-135">Short textual description of the object.</span></span>

<span data-ttu-id="b21c0-136">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="b21c0-136">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="b21c0-137">**Description**</span><span class="sxs-lookup"><span data-stu-id="b21c0-137">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b21c0-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b21c0-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b21c0-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b21c0-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b21c0-140">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b21c0-140">Description of the object.</span></span>

<span data-ttu-id="b21c0-141">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="b21c0-141">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="b21c0-142">**Sens**</span><span class="sxs-lookup"><span data-stu-id="b21c0-142">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b21c0-143">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b21c0-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b21c0-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b21c0-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b21c0-145">Indique si un objet [**d' \_ action CIM**](cim-action.md) particulier fait partie d’une séquence d’actions pour faire passer l’élément logiciel actuel à son état suivant, tel que « installer », ou pour supprimer l’élément logiciel actuel, tel que « désinstaller ».</span><span class="sxs-lookup"><span data-stu-id="b21c0-145">Indicates whether a particular [**CIM\_Action**](cim-action.md) object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<span data-ttu-id="b21c0-146">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="b21c0-146">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="b21c0-147">**Installer** (0)</span><span class="sxs-lookup"><span data-stu-id="b21c0-147">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="b21c0-148">**Désinstaller** (1)</span><span class="sxs-lookup"><span data-stu-id="b21c0-148">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b21c0-149">**DirectoryName**</span><span class="sxs-lookup"><span data-stu-id="b21c0-149">**DirectoryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b21c0-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b21c0-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b21c0-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b21c0-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b21c0-152">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="b21c0-152">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="b21c0-153">Nom du répertoire auquel s’applique l’action.</span><span class="sxs-lookup"><span data-stu-id="b21c0-153">Name of the directory to which the action applies.</span></span>

</dd> <dt>

<span data-ttu-id="b21c0-154">**Nom**</span><span class="sxs-lookup"><span data-stu-id="b21c0-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b21c0-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b21c0-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b21c0-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b21c0-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b21c0-157">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b21c0-157">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b21c0-158">Identifie l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="b21c0-158">Identifies the software element.</span></span>

<span data-ttu-id="b21c0-159">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="b21c0-159">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="b21c0-160">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="b21c0-160">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b21c0-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b21c0-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b21c0-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b21c0-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b21c0-163">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b21c0-163">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b21c0-164">Identificateur de l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="b21c0-164">Identifier for the software element.</span></span>

<span data-ttu-id="b21c0-165">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="b21c0-165">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="b21c0-166">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="b21c0-166">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b21c0-167">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b21c0-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b21c0-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b21c0-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b21c0-169">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b21c0-169">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b21c0-170">État d’un élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="b21c0-170">State of a software element.</span></span>

<span data-ttu-id="b21c0-171">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="b21c0-171">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="b21c0-172"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Déployable** (0)</span><span class="sxs-lookup"><span data-stu-id="b21c0-172"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b21c0-173">Décrit les détails nécessaires à la réussite de la distribution et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État installable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="b21c0-173">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="b21c0-174"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installation** (1)</span><span class="sxs-lookup"><span data-stu-id="b21c0-174"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b21c0-175">Décrit les détails nécessaires à l’installation réussie et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État exécutable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="b21c0-175">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="b21c0-176"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Exécutable** (2)</span><span class="sxs-lookup"><span data-stu-id="b21c0-176"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b21c0-177">Décrit les détails nécessaires pour une exécution réussie et les détails (conditions et actions) requis pour créer un élément logiciel dans l’État en cours d’exécution (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="b21c0-177">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="b21c0-178"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**En cours d’exécution** (3)</span><span class="sxs-lookup"><span data-stu-id="b21c0-178"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b21c0-179">Décrit les détails nécessaires à l’analyse et à l’utilisation d’un élément de début.</span><span class="sxs-lookup"><span data-stu-id="b21c0-179">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b21c0-180">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="b21c0-180">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b21c0-181">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b21c0-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b21c0-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b21c0-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b21c0-183">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informations sur les composants logiciels DMTF \| 002,5»)</span><span class="sxs-lookup"><span data-stu-id="b21c0-183">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="b21c0-184">Système d’exploitation cible de l’élément logiciel propriétaire.</span><span class="sxs-lookup"><span data-stu-id="b21c0-184">Target operating system of the owning software element.</span></span>

<span data-ttu-id="b21c0-185">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="b21c0-185">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b21c0-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="b21c0-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b21c0-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="b21c0-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="b21c0-188"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="b21c0-188"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b21c0-189">Mac OS</span><span class="sxs-lookup"><span data-stu-id="b21c0-189">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="b21c0-190"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="b21c0-190"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="b21c0-191"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="b21c0-191"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="b21c0-192"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="b21c0-192"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="b21c0-193"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX numérique** (6)</span><span class="sxs-lookup"><span data-stu-id="b21c0-193"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="b21c0-194"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="b21c0-194"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b21c0-195">Ouvrir des machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="b21c0-195">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="b21c0-196"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="b21c0-196"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b21c0-197">HP-UX</span><span class="sxs-lookup"><span data-stu-id="b21c0-197">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="b21c0-198"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="b21c0-198"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="b21c0-199"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="b21c0-199"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="b21c0-200"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="b21c0-200"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="b21c0-201"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="b21c0-201"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="b21c0-202"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="b21c0-202"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b21c0-203">Machine virtuelle Microsoft pour Java</span><span class="sxs-lookup"><span data-stu-id="b21c0-203">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="b21c0-204"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="b21c0-204"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="b21c0-205"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="b21c0-205"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b21c0-206">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="b21c0-206">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="b21c0-207"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="b21c0-207"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="b21c0-208">Windows 95</span><span class="sxs-lookup"><span data-stu-id="b21c0-208">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="b21c0-209"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="b21c0-209"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b21c0-210">Windows 98</span><span class="sxs-lookup"><span data-stu-id="b21c0-210">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="b21c0-211"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="b21c0-211"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b21c0-212">Windows NT</span><span class="sxs-lookup"><span data-stu-id="b21c0-212">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="b21c0-213"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="b21c0-213"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b21c0-214">Windows CE</span><span class="sxs-lookup"><span data-stu-id="b21c0-214">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="b21c0-215"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="b21c0-215"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b21c0-216">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="b21c0-216">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="b21c0-217"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="b21c0-217"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="b21c0-218"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="b21c0-218"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="b21c0-219"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="b21c0-219"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="b21c0-220"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Dépendant d’UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="b21c0-220"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="b21c0-221"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="b21c0-221"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="b21c0-222"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="b21c0-222"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="b21c0-223"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="b21c0-223"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="b21c0-224"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="b21c0-224"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="b21c0-225"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="b21c0-225"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="b21c0-226"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="b21c0-226"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="b21c0-227"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="b21c0-227"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="b21c0-228"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="b21c0-228"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="b21c0-229">Une série</span><span class="sxs-lookup"><span data-stu-id="b21c0-229">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="b21c0-230"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="b21c0-230"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="b21c0-231">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="b21c0-231">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="b21c0-232"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="b21c0-232"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="b21c0-233">NT tandem</span><span class="sxs-lookup"><span data-stu-id="b21c0-233">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="b21c0-234"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="b21c0-234"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="b21c0-235">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="b21c0-235">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="b21c0-236"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="b21c0-236"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="b21c0-237"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="b21c0-237"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="b21c0-238"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="b21c0-238"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="b21c0-239"><span id="VM_ESA"></span><span id="vm_esa"></span>**Machine virtuelle/SEEE** (39)</span><span class="sxs-lookup"><span data-stu-id="b21c0-239"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="b21c0-240"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactif** (40)</span><span class="sxs-lookup"><span data-stu-id="b21c0-240"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="b21c0-241"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="b21c0-241"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="b21c0-242">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="b21c0-242">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="b21c0-243"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="b21c0-243"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="b21c0-244"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="b21c0-244"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="b21c0-245"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**Hurd gnu** (44)</span><span class="sxs-lookup"><span data-stu-id="b21c0-245"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="b21c0-246"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="b21c0-246"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="b21c0-247">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="b21c0-247">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="b21c0-248"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Noyau Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="b21c0-248"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="b21c0-249"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="b21c0-249"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="b21c0-250"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="b21c0-250"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="b21c0-251"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="b21c0-251"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="b21c0-252"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="b21c0-252"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="b21c0-253"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="b21c0-253"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="b21c0-254"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menthe** (52)</span><span class="sxs-lookup"><span data-stu-id="b21c0-254"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="b21c0-255"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="b21c0-255"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="b21c0-256">Être un système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="b21c0-256">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="b21c0-257"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="b21c0-257"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="b21c0-258"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="b21c0-258"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="b21c0-259"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="b21c0-259"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="b21c0-260">Palm OS</span><span class="sxs-lookup"><span data-stu-id="b21c0-260">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="b21c0-261"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="b21c0-261"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="b21c0-262"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="b21c0-262"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="b21c0-263"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dédié** (59)</span><span class="sxs-lookup"><span data-stu-id="b21c0-263"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="b21c0-264"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="b21c0-264"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="b21c0-265"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="b21c0-265"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b21c0-266">**Version**</span><span class="sxs-lookup"><span data-stu-id="b21c0-266">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b21c0-267">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b21c0-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b21c0-268">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b21c0-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b21c0-269">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Version**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="b21c0-269">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="b21c0-270">Version de l’opération.</span><span class="sxs-lookup"><span data-stu-id="b21c0-270">Version of the operation.</span></span>

<span data-ttu-id="b21c0-271">La version de l’opération doit se présenter sous l’une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b21c0-271">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="b21c0-272"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="b21c0-272"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="b21c0-273"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="b21c0-273"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="b21c0-274">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="b21c0-274">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b21c0-275">Notes</span><span class="sxs-lookup"><span data-stu-id="b21c0-275">Remarks</span></span>

<span data-ttu-id="b21c0-276">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="b21c0-276">WMI does not implement this class.</span></span>

<span data-ttu-id="b21c0-277">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="b21c0-277">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b21c0-278">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="b21c0-278">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b21c0-279">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b21c0-279">Requirements</span></span>



| <span data-ttu-id="b21c0-280">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b21c0-280">Requirement</span></span> | <span data-ttu-id="b21c0-281">Valeur</span><span class="sxs-lookup"><span data-stu-id="b21c0-281">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b21c0-282">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b21c0-282">Minimum supported client</span></span><br/> | <span data-ttu-id="b21c0-283">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b21c0-283">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b21c0-284">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b21c0-284">Minimum supported server</span></span><br/> | <span data-ttu-id="b21c0-285">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b21c0-285">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b21c0-286">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b21c0-286">Namespace</span></span><br/>                | <span data-ttu-id="b21c0-287">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="b21c0-287">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b21c0-288">MOF</span><span class="sxs-lookup"><span data-stu-id="b21c0-288">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b21c0-289"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b21c0-289"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b21c0-290">DLL</span><span class="sxs-lookup"><span data-stu-id="b21c0-290">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b21c0-291"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b21c0-291"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b21c0-292">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b21c0-292">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b21c0-293">**\_Action CIM**</span><span class="sxs-lookup"><span data-stu-id="b21c0-293">**CIM\_Action**</span></span>](cim-action.md)
</dt> </dl>

 

