---
description: La \_ classe CIM ModifySettingAction représente les informations pour la modification d’un fichier de paramètre spécifique, pour une entrée spécifique, avec une valeur spécifique.
ms.assetid: 6d22bc11-f798-4634-8688-797d4a4a4bee
ms.tgt_platform: multiple
title: Classe CIM_ModifySettingAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ModifySettingAction
- CIM_ModifySettingAction.ActionID
- CIM_ModifySettingAction.Caption
- CIM_ModifySettingAction.Description
- CIM_ModifySettingAction.Direction
- CIM_ModifySettingAction.Name
- CIM_ModifySettingAction.SoftwareElementID
- CIM_ModifySettingAction.SoftwareElementState
- CIM_ModifySettingAction.TargetOperatingSystem
- CIM_ModifySettingAction.Version
- CIM_ModifySettingAction.ActionType
- CIM_ModifySettingAction.EntryName
- CIM_ModifySettingAction.EntryValue
- CIM_ModifySettingAction.FileName
- CIM_ModifySettingAction.SectionKey
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 450e73eaa6f405e47d79cbf3840932e0f106a4b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748692"
---
# <a name="cim_modifysettingaction-class"></a><span data-ttu-id="39e23-103">\_Classe CIM ModifySettingAction</span><span class="sxs-lookup"><span data-stu-id="39e23-103">CIM\_ModifySettingAction class</span></span>

<span data-ttu-id="39e23-104">La classe **CIM \_ ModifySettingAction** représente les informations pour la modification d’un fichier de paramètre spécifique, pour une entrée spécifique, avec une valeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="39e23-104">The **CIM\_ModifySettingAction** class represents the information for modifying a specific setting file, for a specific entry, with a specific value.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="39e23-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="39e23-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="39e23-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="39e23-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="39e23-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="39e23-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="39e23-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="39e23-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="39e23-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39e23-109">Syntax</span></span>

``` syntax
[UUID("{ECDE0B90-DB2A-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ModifySettingAction : CIM_Action
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
  uint16 ActionType;
  string EntryName;
  string EntryValue;
  string FileName;
  string SectionKey;
};
```

## <a name="members"></a><span data-ttu-id="39e23-110">Membres</span><span class="sxs-lookup"><span data-stu-id="39e23-110">Members</span></span>

<span data-ttu-id="39e23-111">La classe **CIM \_ ModifySettingAction** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="39e23-111">The **CIM\_ModifySettingAction** class has these types of members:</span></span>

-   [<span data-ttu-id="39e23-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="39e23-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="39e23-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="39e23-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="39e23-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="39e23-114">Methods</span></span>

<span data-ttu-id="39e23-115">La classe **CIM \_ ModifySettingAction** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="39e23-115">The **CIM\_ModifySettingAction** class has these methods.</span></span>



| <span data-ttu-id="39e23-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="39e23-116">Method</span></span>                                                           | <span data-ttu-id="39e23-117">Description</span><span class="sxs-lookup"><span data-stu-id="39e23-117">Description</span></span>                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="39e23-118">**Appeler**</span><span class="sxs-lookup"><span data-stu-id="39e23-118">**Invoke**</span></span>](invoke-method-in-class-cim-modifysettingaction.md) | <span data-ttu-id="39e23-119">Effectue une action spécifique.</span><span class="sxs-lookup"><span data-stu-id="39e23-119">Takes a specific action.</span></span> <span data-ttu-id="39e23-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="39e23-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="39e23-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="39e23-121">Properties</span></span>

<span data-ttu-id="39e23-122">La classe **CIM \_ ModifySettingAction** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="39e23-122">The **CIM\_ModifySettingAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="39e23-123">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="39e23-123">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e23-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="39e23-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39e23-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39e23-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e23-126">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="39e23-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="39e23-127">Identificateur unique affecté à une action particulière pour un élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="39e23-127">Unique identifier assigned to a particular action for a software element.</span></span>

<span data-ttu-id="39e23-128">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="39e23-128">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="39e23-129">**ActionType**</span><span class="sxs-lookup"><span data-stu-id="39e23-129">**ActionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e23-130">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39e23-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39e23-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39e23-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39e23-132">Type d’action à effectuer sur l’entrée de paramètre spécifiée.</span><span class="sxs-lookup"><span data-stu-id="39e23-132">Type of action to perform on the specified setting entry.</span></span> <span data-ttu-id="39e23-133">Les ajouts sont supposés respecter la casse ; Toutefois, les suppressions sont supposées ne pas respecter la casse.</span><span class="sxs-lookup"><span data-stu-id="39e23-133">Additions are assumed to be case sensitive; however, removals are assumed to be case insensitive.</span></span>

<dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

<span data-ttu-id="39e23-134"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>**Créer** (0)</span><span class="sxs-lookup"><span data-stu-id="39e23-134"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>**Create** (0)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-135">Crée l’entrée spécifiée.</span><span class="sxs-lookup"><span data-stu-id="39e23-135">Creates the specified entry.</span></span>

</dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>

<span data-ttu-id="39e23-136"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Supprimer** (1)</span><span class="sxs-lookup"><span data-stu-id="39e23-136"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Delete** (1)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-137">Supprime l’entrée spécifiée.</span><span class="sxs-lookup"><span data-stu-id="39e23-137">Deletes the specified entry.</span></span>

</dd> <dt>

<span id="Append"></span><span id="append"></span><span id="APPEND"></span>

<span data-ttu-id="39e23-138"><span id="Append"></span><span id="append"></span><span id="APPEND"></span>**Append** (2)</span><span class="sxs-lookup"><span data-stu-id="39e23-138"><span id="Append"></span><span id="append"></span><span id="APPEND"></span>**Append** (2)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-139">Ajoute à la fin de l’entrée spécifiée.</span><span class="sxs-lookup"><span data-stu-id="39e23-139">Appends to the end of the specified entry.</span></span>

</dd> <dt>

<span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>

<span data-ttu-id="39e23-140"><span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>**Supprimer** (3)</span><span class="sxs-lookup"><span data-stu-id="39e23-140"><span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>**Remove** (3)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-141">Supprime la valeur de l’entrée spécifiée.</span><span class="sxs-lookup"><span data-stu-id="39e23-141">Removes the value from the specified entry.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="39e23-142">**Caption**</span><span class="sxs-lookup"><span data-stu-id="39e23-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e23-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="39e23-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39e23-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39e23-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e23-145">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="39e23-145">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="39e23-146">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="39e23-146">Short textual description of the object.</span></span>

<span data-ttu-id="39e23-147">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="39e23-147">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="39e23-148">**Description**</span><span class="sxs-lookup"><span data-stu-id="39e23-148">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e23-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="39e23-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39e23-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39e23-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39e23-151">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="39e23-151">Description of the object.</span></span>

<span data-ttu-id="39e23-152">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="39e23-152">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="39e23-153">**Sens**</span><span class="sxs-lookup"><span data-stu-id="39e23-153">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e23-154">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39e23-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39e23-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39e23-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39e23-156">Indique si un objet [**d' \_ action CIM**](cim-action.md) particulier fait partie d’une séquence d’actions pour faire passer l’élément logiciel actuel à son état suivant, tel que « installer », ou pour supprimer l’élément logiciel actuel, tel que « désinstaller ».</span><span class="sxs-lookup"><span data-stu-id="39e23-156">Indicates whether a particular [**CIM\_Action**](cim-action.md) object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<span data-ttu-id="39e23-157">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="39e23-157">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="39e23-158">**Installer** (0)</span><span class="sxs-lookup"><span data-stu-id="39e23-158">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="39e23-159">**Désinstaller** (1)</span><span class="sxs-lookup"><span data-stu-id="39e23-159">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="39e23-160">**EntryName**</span><span class="sxs-lookup"><span data-stu-id="39e23-160">**EntryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e23-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="39e23-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39e23-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39e23-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e23-163">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="39e23-163">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="39e23-164">Nom de l’entrée à modifier.</span><span class="sxs-lookup"><span data-stu-id="39e23-164">Name of the entry to modify.</span></span>

</dd> <dt>

<span data-ttu-id="39e23-165">**EntryValue**</span><span class="sxs-lookup"><span data-stu-id="39e23-165">**EntryValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e23-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="39e23-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39e23-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39e23-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39e23-168">Valeur à ajouter, à ajouter ou à remplacer le paramètre spécifié.</span><span class="sxs-lookup"><span data-stu-id="39e23-168">Value to add, append, or to replace the specified setting.</span></span>

</dd> <dt>

<span data-ttu-id="39e23-169">**FileName**</span><span class="sxs-lookup"><span data-stu-id="39e23-169">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e23-170">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="39e23-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39e23-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39e23-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e23-172">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="39e23-172">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="39e23-173">Nom de fichier de l’entrée de fichier de paramètres à modifier.</span><span class="sxs-lookup"><span data-stu-id="39e23-173">File name of the setting file entry to modify.</span></span>

</dd> <dt>

<span data-ttu-id="39e23-174">**Nom**</span><span class="sxs-lookup"><span data-stu-id="39e23-174">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e23-175">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="39e23-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39e23-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39e23-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e23-177">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="39e23-177">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="39e23-178">Identifie l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="39e23-178">Identifies the software element.</span></span>

<span data-ttu-id="39e23-179">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="39e23-179">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="39e23-180">**SectionKey**</span><span class="sxs-lookup"><span data-stu-id="39e23-180">**SectionKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e23-181">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="39e23-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39e23-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39e23-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e23-183">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="39e23-183">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="39e23-184">Clé de section de l’entrée de paramètre à modifier.</span><span class="sxs-lookup"><span data-stu-id="39e23-184">Section key of the setting entry to modify.</span></span>

</dd> <dt>

<span data-ttu-id="39e23-185">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="39e23-185">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e23-186">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="39e23-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39e23-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39e23-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e23-188">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="39e23-188">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="39e23-189">Identificateur de l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="39e23-189">Identifier for the software element.</span></span>

<span data-ttu-id="39e23-190">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="39e23-190">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="39e23-191">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="39e23-191">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e23-192">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39e23-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39e23-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39e23-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e23-194">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="39e23-194">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="39e23-195">État d’un élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="39e23-195">State of a software element.</span></span>

<span data-ttu-id="39e23-196">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="39e23-196">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="39e23-197"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Déployable** (0)</span><span class="sxs-lookup"><span data-stu-id="39e23-197"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-198">Décrit les détails nécessaires à la réussite de la distribution et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État installable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="39e23-198">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="39e23-199"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installation** (1)</span><span class="sxs-lookup"><span data-stu-id="39e23-199"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-200">Décrit les détails nécessaires à l’installation réussie et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État exécutable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="39e23-200">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="39e23-201"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Exécutable** (2)</span><span class="sxs-lookup"><span data-stu-id="39e23-201"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-202">Décrit les détails nécessaires pour une exécution réussie et les détails (conditions et actions) requis pour créer un élément logiciel dans l’État en cours d’exécution (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="39e23-202">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="39e23-203"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**En cours d’exécution** (3)</span><span class="sxs-lookup"><span data-stu-id="39e23-203"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-204">Décrit les détails nécessaires à l’analyse et à l’utilisation d’un élément de début.</span><span class="sxs-lookup"><span data-stu-id="39e23-204">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="39e23-205">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="39e23-205">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e23-206">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39e23-206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39e23-207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39e23-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e23-208">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informations sur les composants logiciels DMTF \| 002,5»)</span><span class="sxs-lookup"><span data-stu-id="39e23-208">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="39e23-209">Système d’exploitation cible de l’élément logiciel propriétaire.</span><span class="sxs-lookup"><span data-stu-id="39e23-209">Target operating system of the owning software element.</span></span>

<span data-ttu-id="39e23-210">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="39e23-210">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="39e23-211"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="39e23-211"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="39e23-212"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="39e23-212"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="39e23-213"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="39e23-213"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-214">Mac OS</span><span class="sxs-lookup"><span data-stu-id="39e23-214">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="39e23-215"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="39e23-215"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="39e23-216"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="39e23-216"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="39e23-217"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="39e23-217"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="39e23-218"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX numérique** (6)</span><span class="sxs-lookup"><span data-stu-id="39e23-218"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="39e23-219"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="39e23-219"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-220">Ouvrir des machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="39e23-220">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="39e23-221"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="39e23-221"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-222">HP-UX</span><span class="sxs-lookup"><span data-stu-id="39e23-222">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="39e23-223"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="39e23-223"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="39e23-224"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="39e23-224"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="39e23-225"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="39e23-225"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="39e23-226"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="39e23-226"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="39e23-227"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="39e23-227"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-228">Machine virtuelle Microsoft pour Java</span><span class="sxs-lookup"><span data-stu-id="39e23-228">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="39e23-229"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="39e23-229"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="39e23-230"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="39e23-230"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-231">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="39e23-231">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="39e23-232"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="39e23-232"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-233">Windows 95</span><span class="sxs-lookup"><span data-stu-id="39e23-233">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="39e23-234"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="39e23-234"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-235">Windows 98</span><span class="sxs-lookup"><span data-stu-id="39e23-235">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="39e23-236"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="39e23-236"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-237">Windows NT</span><span class="sxs-lookup"><span data-stu-id="39e23-237">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="39e23-238"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="39e23-238"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-239">Windows CE</span><span class="sxs-lookup"><span data-stu-id="39e23-239">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="39e23-240"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="39e23-240"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-241">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="39e23-241">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="39e23-242"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="39e23-242"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="39e23-243"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="39e23-243"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="39e23-244"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="39e23-244"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="39e23-245"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Dépendant d’UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="39e23-245"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="39e23-246"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="39e23-246"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="39e23-247"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="39e23-247"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="39e23-248"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="39e23-248"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="39e23-249"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="39e23-249"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="39e23-250"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="39e23-250"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="39e23-251"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="39e23-251"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="39e23-252"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="39e23-252"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="39e23-253"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="39e23-253"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-254">Une série</span><span class="sxs-lookup"><span data-stu-id="39e23-254">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="39e23-255"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="39e23-255"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-256">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="39e23-256">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="39e23-257"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="39e23-257"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-258">NT tandem</span><span class="sxs-lookup"><span data-stu-id="39e23-258">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="39e23-259"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="39e23-259"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-260">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="39e23-260">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="39e23-261"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="39e23-261"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="39e23-262"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="39e23-262"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="39e23-263"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="39e23-263"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="39e23-264"><span id="VM_ESA"></span><span id="vm_esa"></span>**Machine virtuelle/SEEE** (39)</span><span class="sxs-lookup"><span data-stu-id="39e23-264"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="39e23-265"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactif** (40)</span><span class="sxs-lookup"><span data-stu-id="39e23-265"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="39e23-266"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="39e23-266"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-267">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="39e23-267">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="39e23-268"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="39e23-268"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="39e23-269"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="39e23-269"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="39e23-270"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**Hurd gnu** (44)</span><span class="sxs-lookup"><span data-stu-id="39e23-270"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="39e23-271"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="39e23-271"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-272">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="39e23-272">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="39e23-273"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Noyau Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="39e23-273"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="39e23-274"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="39e23-274"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="39e23-275"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="39e23-275"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="39e23-276"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="39e23-276"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="39e23-277"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="39e23-277"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="39e23-278"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="39e23-278"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="39e23-279"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menthe** (52)</span><span class="sxs-lookup"><span data-stu-id="39e23-279"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="39e23-280"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="39e23-280"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-281">Être un système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="39e23-281">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="39e23-282"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="39e23-282"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="39e23-283"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="39e23-283"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="39e23-284"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="39e23-284"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="39e23-285">Palm OS</span><span class="sxs-lookup"><span data-stu-id="39e23-285">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="39e23-286"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="39e23-286"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="39e23-287"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="39e23-287"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="39e23-288"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dédié** (59)</span><span class="sxs-lookup"><span data-stu-id="39e23-288"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="39e23-289"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="39e23-289"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="39e23-290"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="39e23-290"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="39e23-291">**Version**</span><span class="sxs-lookup"><span data-stu-id="39e23-291">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e23-292">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="39e23-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39e23-293">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39e23-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e23-294">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Version**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="39e23-294">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="39e23-295">Version de l’opération.</span><span class="sxs-lookup"><span data-stu-id="39e23-295">Version of the operation.</span></span>

<span data-ttu-id="39e23-296">La version de l’opération doit se présenter sous l’une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="39e23-296">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="39e23-297"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="39e23-297"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="39e23-298"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="39e23-298"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="39e23-299">Cette propriété est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="39e23-299">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39e23-300">Notes</span><span class="sxs-lookup"><span data-stu-id="39e23-300">Remarks</span></span>

<span data-ttu-id="39e23-301">La classe **CIM \_ ModifySettingAction** est dérivée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="39e23-301">The **CIM\_ModifySettingAction** class is derived from [**CIM\_Action**](cim-action.md).</span></span>

<span data-ttu-id="39e23-302">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="39e23-302">WMI does not implement this class.</span></span>

<span data-ttu-id="39e23-303">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="39e23-303">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="39e23-304">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="39e23-304">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="39e23-305">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39e23-305">Requirements</span></span>



| <span data-ttu-id="39e23-306">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39e23-306">Requirement</span></span> | <span data-ttu-id="39e23-307">Valeur</span><span class="sxs-lookup"><span data-stu-id="39e23-307">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39e23-308">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39e23-308">Minimum supported client</span></span><br/> | <span data-ttu-id="39e23-309">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39e23-309">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="39e23-310">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39e23-310">Minimum supported server</span></span><br/> | <span data-ttu-id="39e23-311">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39e23-311">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="39e23-312">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="39e23-312">Namespace</span></span><br/>                | <span data-ttu-id="39e23-313">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="39e23-313">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="39e23-314">MOF</span><span class="sxs-lookup"><span data-stu-id="39e23-314">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39e23-315"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="39e23-315"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="39e23-316">DLL</span><span class="sxs-lookup"><span data-stu-id="39e23-316">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39e23-317"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39e23-317"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39e23-318">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39e23-318">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39e23-319">**\_Action CIM**</span><span class="sxs-lookup"><span data-stu-id="39e23-319">**CIM\_Action**</span></span>](cim-action.md)
</dt> </dl>

 

