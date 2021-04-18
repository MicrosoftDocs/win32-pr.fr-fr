---
description: La \_ classe CIM CopyFileAction représente le déplacement ou la copie de fichiers à partir d’un système informatique vers un nouvel emplacement.
ms.assetid: c80b5002-d489-4b7e-b9a2-4460c3596958
ms.tgt_platform: multiple
title: Classe CIM_CopyFileAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CopyFileAction
- CIM_CopyFileAction.ActionID
- CIM_CopyFileAction.Caption
- CIM_CopyFileAction.Description
- CIM_CopyFileAction.Direction
- CIM_CopyFileAction.Name
- CIM_CopyFileAction.SoftwareElementID
- CIM_CopyFileAction.SoftwareElementState
- CIM_CopyFileAction.TargetOperatingSystem
- CIM_CopyFileAction.Version
- CIM_CopyFileAction.DeleteAfterCopy
- CIM_CopyFileAction.Destination
- CIM_CopyFileAction.Source
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c0303f4696d1baa5129d93cd2e6a7703be611ed9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515936"
---
# <a name="cim_copyfileaction-class"></a><span data-ttu-id="19df5-103">\_Classe CIM CopyFileAction</span><span class="sxs-lookup"><span data-stu-id="19df5-103">CIM\_CopyFileAction class</span></span>

<span data-ttu-id="19df5-104">La classe **CIM \_ CopyFileAction** représente le déplacement ou la copie de fichiers à partir d’un système informatique vers un nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="19df5-104">The **CIM\_CopyFileAction** class represents moving or copying files from a computer system to a new location.</span></span>

<span data-ttu-id="19df5-105">Les informations d’emplacement pour la copie sont spécifiées à l’aide des associations [**CIM \_ ToDirectorySpecification**](cim-todirectoryspecification.md) et [**CIM \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md) , ou des associations [**CIM \_ ToDirectoryAction**](cim-todirectoryaction.md) et [**CIM \_ FromDirectoryAction**](cim-fromdirectoryaction.md) .</span><span class="sxs-lookup"><span data-stu-id="19df5-105">Location information for copying is specified by using either the [**CIM\_ToDirectorySpecification**](cim-todirectoryspecification.md) and [**CIM\_FromDirectorySpecification**](cim-fromdirectoryspecification.md) associations, or the [**CIM\_ToDirectoryAction**](cim-todirectoryaction.md) and [**CIM\_FromDirectoryAction**](cim-fromdirectoryaction.md) associations.</span></span> <span data-ttu-id="19df5-106">Le premier jeu est utilisé lorsque la source ou la cible doit exister avant que des actions soient effectuées.</span><span class="sxs-lookup"><span data-stu-id="19df5-106">The first set is used when the source or target are to exist before any actions are taken.</span></span> <span data-ttu-id="19df5-107">Le deuxième jeu est utilisé lorsque la source ou la cible sont créées dans le cadre d’une action précédente.</span><span class="sxs-lookup"><span data-stu-id="19df5-107">The second set is used when the source or target are created as a part of a previous action.</span></span> <span data-ttu-id="19df5-108">Dans ce dernier cas, l’action de création du répertoire doit se produire avant l’objet **CIM \_ CopyFileAction** .</span><span class="sxs-lookup"><span data-stu-id="19df5-108">In the latter case, the action to create the directory must occur prior to the **CIM\_CopyFileAction** object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="19df5-109">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="19df5-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="19df5-110">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="19df5-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="19df5-111">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="19df5-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="19df5-112">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="19df5-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="19df5-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19df5-113">Syntax</span></span>

``` syntax
[UUID("{73553260-DB22-11d2-85FC-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_CopyFileAction : CIM_FileAction
{
  string  ActionID;
  string  Caption;
  string  Description;
  uint16  Direction;
  string  Name;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
  uint16  TargetOperatingSystem;
  string  Version;
  boolean DeleteAfterCopy;
  string  Destination;
  string  Source;
};
```

## <a name="members"></a><span data-ttu-id="19df5-114">Membres</span><span class="sxs-lookup"><span data-stu-id="19df5-114">Members</span></span>

<span data-ttu-id="19df5-115">La classe **CIM \_ CopyFileAction** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="19df5-115">The **CIM\_CopyFileAction** class has these types of members:</span></span>

-   [<span data-ttu-id="19df5-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="19df5-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="19df5-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="19df5-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="19df5-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="19df5-118">Methods</span></span>

<span data-ttu-id="19df5-119">La classe **CIM \_ CopyFileAction** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="19df5-119">The **CIM\_CopyFileAction** class has these methods.</span></span>



| <span data-ttu-id="19df5-120">Méthode</span><span class="sxs-lookup"><span data-stu-id="19df5-120">Method</span></span>                                                      | <span data-ttu-id="19df5-121">Description</span><span class="sxs-lookup"><span data-stu-id="19df5-121">Description</span></span>                                                                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19df5-122">**Appeler**</span><span class="sxs-lookup"><span data-stu-id="19df5-122">**Invoke**</span></span>](invoke-method-in-class-cim-copyfileaction.md) | <span data-ttu-id="19df5-123">Effectue une action particulière.</span><span class="sxs-lookup"><span data-stu-id="19df5-123">Takes a particular action.</span></span> <span data-ttu-id="19df5-124">Les détails de la façon dont la méthode exécute l’action sont spécifiques à l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="19df5-124">The details of how the method performs the action are implementation-specific.</span></span> <span data-ttu-id="19df5-125">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="19df5-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="19df5-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="19df5-126">Properties</span></span>

<span data-ttu-id="19df5-127">La classe **CIM \_ CopyFileAction** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="19df5-127">The **CIM\_CopyFileAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="19df5-128">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="19df5-128">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19df5-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="19df5-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19df5-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19df5-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19df5-131">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="19df5-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="19df5-132">Identificateur unique affecté à une action particulière pour un élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="19df5-132">Unique identifier assigned to a particular action for a software element.</span></span>

<span data-ttu-id="19df5-133">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="19df5-133">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="19df5-134">**Caption**</span><span class="sxs-lookup"><span data-stu-id="19df5-134">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19df5-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="19df5-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19df5-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19df5-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19df5-137">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="19df5-137">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="19df5-138">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="19df5-138">Short textual description of the object.</span></span>

<span data-ttu-id="19df5-139">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="19df5-139">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="19df5-140">**DeleteAfterCopy**</span><span class="sxs-lookup"><span data-stu-id="19df5-140">**DeleteAfterCopy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19df5-141">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="19df5-141">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="19df5-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19df5-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19df5-143">Si la **valeur est true**, le fichier source est supprimé après l’opération de copie.</span><span class="sxs-lookup"><span data-stu-id="19df5-143">If **TRUE**, the source file is deleted after the copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="19df5-144">**Description**</span><span class="sxs-lookup"><span data-stu-id="19df5-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19df5-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="19df5-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19df5-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19df5-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19df5-147">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="19df5-147">Description of the object.</span></span>

<span data-ttu-id="19df5-148">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="19df5-148">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="19df5-149">**Destination**</span><span class="sxs-lookup"><span data-stu-id="19df5-149">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19df5-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="19df5-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19df5-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19df5-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19df5-152">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="19df5-152">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="19df5-153">Nom de fichier de destination complet.</span><span class="sxs-lookup"><span data-stu-id="19df5-153">Fully qualified destination file name.</span></span>

</dd> <dt>

<span data-ttu-id="19df5-154">**Sens**</span><span class="sxs-lookup"><span data-stu-id="19df5-154">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19df5-155">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="19df5-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="19df5-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19df5-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19df5-157">Indique si un objet [**d' \_ action CIM**](cim-action.md) particulier fait partie d’une séquence d’actions pour faire passer l’élément logiciel actuel à son état suivant, tel que « installer », ou pour supprimer l’élément logiciel actuel, tel que « désinstaller ».</span><span class="sxs-lookup"><span data-stu-id="19df5-157">Indicates whether a particular [**CIM\_Action**](cim-action.md) object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<span data-ttu-id="19df5-158">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="19df5-158">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="19df5-159">**Installer** (0)</span><span class="sxs-lookup"><span data-stu-id="19df5-159">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="19df5-160">**Désinstaller** (1)</span><span class="sxs-lookup"><span data-stu-id="19df5-160">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="19df5-161">**Nom**</span><span class="sxs-lookup"><span data-stu-id="19df5-161">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19df5-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="19df5-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19df5-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19df5-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19df5-164">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="19df5-164">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="19df5-165">Identifie l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="19df5-165">Identifies the software element.</span></span>

<span data-ttu-id="19df5-166">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="19df5-166">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="19df5-167">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="19df5-167">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19df5-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="19df5-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19df5-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19df5-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19df5-170">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="19df5-170">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="19df5-171">Identificateur de l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="19df5-171">Identifier for the software element.</span></span>

<span data-ttu-id="19df5-172">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="19df5-172">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="19df5-173">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="19df5-173">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19df5-174">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="19df5-174">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="19df5-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19df5-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19df5-176">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="19df5-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="19df5-177">État d’un élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="19df5-177">State of a software element.</span></span>

<span data-ttu-id="19df5-178">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="19df5-178">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="19df5-179"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Déployable** (0)</span><span class="sxs-lookup"><span data-stu-id="19df5-179"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="19df5-180">Décrit les détails nécessaires à la réussite de la distribution et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État installable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="19df5-180">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="19df5-181"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installation** (1)</span><span class="sxs-lookup"><span data-stu-id="19df5-181"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="19df5-182">Décrit les détails nécessaires à l’installation réussie et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État exécutable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="19df5-182">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="19df5-183"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Exécutable** (2)</span><span class="sxs-lookup"><span data-stu-id="19df5-183"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="19df5-184">Décrit les détails nécessaires pour une exécution réussie et les détails (conditions et actions) requis pour créer un élément logiciel dans l’État en cours d’exécution (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="19df5-184">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="19df5-185"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**En cours d’exécution** (3)</span><span class="sxs-lookup"><span data-stu-id="19df5-185"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="19df5-186">Décrit les détails nécessaires à l’analyse et à l’utilisation d’un élément de début.</span><span class="sxs-lookup"><span data-stu-id="19df5-186">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="19df5-187">**Source**</span><span class="sxs-lookup"><span data-stu-id="19df5-187">**Source**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19df5-188">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="19df5-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19df5-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19df5-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19df5-190">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="19df5-190">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="19df5-191">Nom complet du fichier source.</span><span class="sxs-lookup"><span data-stu-id="19df5-191">Fully qualified source file name.</span></span>

</dd> <dt>

<span data-ttu-id="19df5-192">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="19df5-192">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19df5-193">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="19df5-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="19df5-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19df5-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19df5-195">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informations sur les composants logiciels DMTF \| 002,5»)</span><span class="sxs-lookup"><span data-stu-id="19df5-195">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="19df5-196">Système d’exploitation cible de l’élément logiciel propriétaire.</span><span class="sxs-lookup"><span data-stu-id="19df5-196">Target operating system of the owning software element.</span></span>

<span data-ttu-id="19df5-197">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="19df5-197">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="19df5-198"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="19df5-198"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="19df5-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="19df5-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="19df5-200"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="19df5-200"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="19df5-201">Mac OS</span><span class="sxs-lookup"><span data-stu-id="19df5-201">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="19df5-202"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="19df5-202"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="19df5-203"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="19df5-203"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="19df5-204"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="19df5-204"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="19df5-205"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX numérique** (6)</span><span class="sxs-lookup"><span data-stu-id="19df5-205"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="19df5-206"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="19df5-206"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="19df5-207">Ouvrir des machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="19df5-207">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="19df5-208"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="19df5-208"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="19df5-209">HP-UX</span><span class="sxs-lookup"><span data-stu-id="19df5-209">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="19df5-210"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="19df5-210"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="19df5-211"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="19df5-211"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="19df5-212"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="19df5-212"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="19df5-213"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="19df5-213"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="19df5-214"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="19df5-214"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="19df5-215">Machine virtuelle Microsoft pour Java</span><span class="sxs-lookup"><span data-stu-id="19df5-215">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="19df5-216"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="19df5-216"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="19df5-217"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="19df5-217"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="19df5-218">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="19df5-218">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="19df5-219"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="19df5-219"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="19df5-220">Windows 95</span><span class="sxs-lookup"><span data-stu-id="19df5-220">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="19df5-221"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="19df5-221"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="19df5-222">Windows 98</span><span class="sxs-lookup"><span data-stu-id="19df5-222">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="19df5-223"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="19df5-223"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="19df5-224">Windows NT</span><span class="sxs-lookup"><span data-stu-id="19df5-224">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="19df5-225"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="19df5-225"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="19df5-226">Windows CE</span><span class="sxs-lookup"><span data-stu-id="19df5-226">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="19df5-227"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="19df5-227"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="19df5-228">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="19df5-228">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="19df5-229"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="19df5-229"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="19df5-230"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="19df5-230"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="19df5-231"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="19df5-231"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="19df5-232"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Dépendant d’UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="19df5-232"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="19df5-233"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="19df5-233"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="19df5-234"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="19df5-234"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="19df5-235"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="19df5-235"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="19df5-236"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="19df5-236"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="19df5-237"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="19df5-237"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="19df5-238"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="19df5-238"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="19df5-239"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="19df5-239"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="19df5-240"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="19df5-240"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="19df5-241">Une série</span><span class="sxs-lookup"><span data-stu-id="19df5-241">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="19df5-242"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="19df5-242"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="19df5-243">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="19df5-243">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="19df5-244"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="19df5-244"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="19df5-245">NT tandem</span><span class="sxs-lookup"><span data-stu-id="19df5-245">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="19df5-246"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="19df5-246"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="19df5-247">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="19df5-247">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="19df5-248"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="19df5-248"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="19df5-249"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="19df5-249"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="19df5-250"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="19df5-250"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="19df5-251"><span id="VM_ESA"></span><span id="vm_esa"></span>**Machine virtuelle/SEEE** (39)</span><span class="sxs-lookup"><span data-stu-id="19df5-251"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="19df5-252"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactif** (40)</span><span class="sxs-lookup"><span data-stu-id="19df5-252"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="19df5-253"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="19df5-253"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="19df5-254">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="19df5-254">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="19df5-255"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="19df5-255"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="19df5-256"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="19df5-256"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="19df5-257"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**Hurd gnu** (44)</span><span class="sxs-lookup"><span data-stu-id="19df5-257"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="19df5-258"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="19df5-258"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="19df5-259">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="19df5-259">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="19df5-260"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Noyau Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="19df5-260"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="19df5-261"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="19df5-261"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="19df5-262"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="19df5-262"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="19df5-263"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="19df5-263"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="19df5-264"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="19df5-264"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="19df5-265"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="19df5-265"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="19df5-266"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menthe** (52)</span><span class="sxs-lookup"><span data-stu-id="19df5-266"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="19df5-267"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="19df5-267"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="19df5-268">Être un système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="19df5-268">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="19df5-269"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="19df5-269"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="19df5-270"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="19df5-270"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="19df5-271"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="19df5-271"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="19df5-272">Palm OS</span><span class="sxs-lookup"><span data-stu-id="19df5-272">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="19df5-273"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="19df5-273"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="19df5-274"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="19df5-274"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="19df5-275"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dédié** (59)</span><span class="sxs-lookup"><span data-stu-id="19df5-275"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="19df5-276"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="19df5-276"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="19df5-277"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="19df5-277"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="19df5-278">**Version**</span><span class="sxs-lookup"><span data-stu-id="19df5-278">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19df5-279">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="19df5-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19df5-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19df5-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19df5-281">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Version**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="19df5-281">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="19df5-282">Version de l’opération.</span><span class="sxs-lookup"><span data-stu-id="19df5-282">Version of the operation.</span></span>

<span data-ttu-id="19df5-283">La version de l’opération doit se présenter sous l’une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="19df5-283">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="19df5-284"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="19df5-284"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="19df5-285"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="19df5-285"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="19df5-286">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="19df5-286">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19df5-287">Notes</span><span class="sxs-lookup"><span data-stu-id="19df5-287">Remarks</span></span>

<span data-ttu-id="19df5-288">La classe **CIM \_ CopyFileAction** est dérivée de [**CIM \_ FileAction**](cim-fileaction.md).</span><span class="sxs-lookup"><span data-stu-id="19df5-288">The **CIM\_CopyFileAction** class is derived from [**CIM\_FileAction**](cim-fileaction.md).</span></span>

<span data-ttu-id="19df5-289">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="19df5-289">WMI does not implement this class.</span></span> <span data-ttu-id="19df5-290">Pour plus d’informations sur les classes dérivées de **CIM \_ CopyFileAction**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="19df5-290">For more information about classes derived from **CIM\_CopyFileAction**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="19df5-291">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="19df5-291">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="19df5-292">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="19df5-292">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="19df5-293">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19df5-293">Requirements</span></span>



| <span data-ttu-id="19df5-294">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19df5-294">Requirement</span></span> | <span data-ttu-id="19df5-295">Valeur</span><span class="sxs-lookup"><span data-stu-id="19df5-295">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19df5-296">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19df5-296">Minimum supported client</span></span><br/> | <span data-ttu-id="19df5-297">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19df5-297">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="19df5-298">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19df5-298">Minimum supported server</span></span><br/> | <span data-ttu-id="19df5-299">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19df5-299">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="19df5-300">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="19df5-300">Namespace</span></span><br/>                | <span data-ttu-id="19df5-301">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="19df5-301">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="19df5-302">MOF</span><span class="sxs-lookup"><span data-stu-id="19df5-302">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19df5-303"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19df5-303"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="19df5-304">DLL</span><span class="sxs-lookup"><span data-stu-id="19df5-304">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19df5-305"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19df5-305"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19df5-306">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19df5-306">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19df5-307">**\_FILEACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="19df5-307">**CIM\_FileAction**</span></span>](cim-fileaction.md)
</dt> </dl>

 

