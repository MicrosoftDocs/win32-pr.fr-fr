---
description: La \_ classe CIM SettingCheck spécifie les informations nécessaires pour vérifier un fichier de paramètres particulier pour une entrée spécifique qui contient une valeur égale à la valeur spécifiée. Toutes les comparaisons sont supposées ne pas respecter la casse.
ms.assetid: 0e40276c-e794-4ea1-8937-c6d7f110f97d
ms.tgt_platform: multiple
title: Classe CIM_SettingCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingCheck
- CIM_SettingCheck.Caption
- CIM_SettingCheck.CheckID
- CIM_SettingCheck.CheckMode
- CIM_SettingCheck.CheckType
- CIM_SettingCheck.Description
- CIM_SettingCheck.EntryName
- CIM_SettingCheck.EntryValue
- CIM_SettingCheck.FileName
- CIM_SettingCheck.Name
- CIM_SettingCheck.SectionKey
- CIM_SettingCheck.SoftwareElementID
- CIM_SettingCheck.SoftwareElementState
- CIM_SettingCheck.TargetOperatingSystem
- CIM_SettingCheck.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4b360833f216d9feb839a4ed84a0e1ba4cd61ebf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515780"
---
# <a name="cim_settingcheck-class"></a><span data-ttu-id="8cbd1-104">\_Classe CIM SettingCheck</span><span class="sxs-lookup"><span data-stu-id="8cbd1-104">CIM\_SettingCheck class</span></span>

<span data-ttu-id="8cbd1-105">La classe **CIM \_ SettingCheck** spécifie les informations nécessaires pour vérifier un fichier de paramètres particulier pour une entrée spécifique qui contient une valeur égale à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-105">The **CIM\_SettingCheck** class specifies information needed to check a particular setting file for a specific entry that contains a value equal to the value specified.</span></span> <span data-ttu-id="8cbd1-106">Toutes les comparaisons sont supposées ne pas respecter la casse.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-106">All comparisons are assumed to be case insensitive.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8cbd1-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8cbd1-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8cbd1-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8cbd1-109">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="8cbd1-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cbd1-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8cbd1-111">Syntax</span></span>

``` syntax
[UUID("{DC1D8140-DB30-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SettingCheck : CIM_Check
{
  string  Caption;
  string  CheckID;
  boolean CheckMode;
  uint16  CheckType;
  string  Description;
  string  EntryName;
  string  EntryValue;
  string  FileName;
  string  Name;
  string  SectionKey;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
  uint16  TargetOperatingSystem;
  string  Version;
};
```

## <a name="members"></a><span data-ttu-id="8cbd1-112">Membres</span><span class="sxs-lookup"><span data-stu-id="8cbd1-112">Members</span></span>

<span data-ttu-id="8cbd1-113">La classe **CIM \_ SettingCheck** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8cbd1-113">The **CIM\_SettingCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="8cbd1-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8cbd1-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="8cbd1-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8cbd1-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8cbd1-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8cbd1-116">Methods</span></span>

<span data-ttu-id="8cbd1-117">La classe **CIM \_ SettingCheck** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-117">The **CIM\_SettingCheck** class has these methods.</span></span>



| <span data-ttu-id="8cbd1-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="8cbd1-118">Method</span></span>                                                    | <span data-ttu-id="8cbd1-119">Description</span><span class="sxs-lookup"><span data-stu-id="8cbd1-119">Description</span></span>                                                   |
|:----------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="8cbd1-120">**Appeler**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-120">**Invoke**</span></span>](invoke-method-in-class-cim-settingcheck.md) | <span data-ttu-id="8cbd1-121">Effectue une action particulière.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-121">Takes a particular action.</span></span> <span data-ttu-id="8cbd1-122">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8cbd1-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8cbd1-123">Properties</span></span>

<span data-ttu-id="8cbd1-124">La classe **CIM \_ SettingCheck** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-124">The **CIM\_SettingCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8cbd1-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cbd1-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cbd1-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8cbd1-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cbd1-128">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-128">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8cbd1-129">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-129">Short textual description of the object.</span></span>

<span data-ttu-id="8cbd1-130">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="8cbd1-130">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cbd1-131">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-131">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cbd1-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cbd1-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8cbd1-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cbd1-134">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8cbd1-135">Identificateur utilisé conjointement avec d’autres clés pour identifier de manière unique la vérification.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-135">Identifier used in conjunction with other keys to uniquely identify the check.</span></span> <span data-ttu-id="8cbd1-136">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="8cbd1-136">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cbd1-137">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-137">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cbd1-138">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8cbd1-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8cbd1-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cbd1-140">Si la **valeur est true**, la condition est supposée exister dans l’environnement (par exemple, si un fichier se trouve sur un système, la méthode [**Invoke**](invoke-method-in-class-cim-settingcheck.md) doit retourner la **valeur true**).</span><span class="sxs-lookup"><span data-stu-id="8cbd1-140">If **TRUE**, the condition is expected to exist in the environment (for example, if a file is on a system, the [**Invoke**](invoke-method-in-class-cim-settingcheck.md) method should return **TRUE**).</span></span> <span data-ttu-id="8cbd1-141">Si la **valeur est false**, la condition ne doit pas exister (par exemple, si un fichier n’est pas sur un système, la méthode **Invoke** doit retourner **false**).</span><span class="sxs-lookup"><span data-stu-id="8cbd1-141">If **FALSE**, the condition should not exist (for example, if a file is not on a system, the **Invoke** method should return **FALSE**).</span></span>

<span data-ttu-id="8cbd1-142">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="8cbd1-142">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cbd1-143">**CheckType**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-143">**CheckType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cbd1-144">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8cbd1-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8cbd1-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cbd1-146">Façon dont la valeur de paramètre doit être comparée.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-146">Way in which the setting value should be compared.</span></span>

<dt>

<span id="Matches"></span><span id="matches"></span><span id="MATCHES"></span>

<span data-ttu-id="8cbd1-147">**Correspond à** (0)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-147">**Matches** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Contains"></span><span id="contains"></span><span id="CONTAINS"></span>

<span data-ttu-id="8cbd1-148">**Contient** (1)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-148">**Contains** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8cbd1-149">**Description**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cbd1-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cbd1-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8cbd1-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cbd1-152">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-152">Description of the object.</span></span>

<span data-ttu-id="8cbd1-153">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="8cbd1-153">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cbd1-154">**EntryName**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-154">**EntryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cbd1-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cbd1-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8cbd1-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cbd1-157">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-157">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8cbd1-158">Nom de l’entrée à vérifier</span><span class="sxs-lookup"><span data-stu-id="8cbd1-158">Name of the entry to be checked</span></span>

</dd> <dt>

<span data-ttu-id="8cbd1-159">**EntryValue**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-159">**EntryValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cbd1-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cbd1-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8cbd1-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cbd1-162">Valeur associée à l’entrée nommée à vérifier.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-162">Value that is associated with the named entry to check.</span></span>

</dd> <dt>

<span data-ttu-id="8cbd1-163">**FileName**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-163">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cbd1-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cbd1-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8cbd1-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cbd1-166">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-166">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="8cbd1-167">Nom de fichier du fichier de paramètres à vérifier.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-167">File name of the setting file to check.</span></span>

</dd> <dt>

<span data-ttu-id="8cbd1-168">**Nom**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-168">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cbd1-169">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cbd1-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8cbd1-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cbd1-171">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-171">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8cbd1-172">Nom utilisé pour identifier l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-172">Name used to identify the software element.</span></span> <span data-ttu-id="8cbd1-173">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="8cbd1-173">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cbd1-174">**SectionKey**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-174">**SectionKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cbd1-175">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cbd1-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8cbd1-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cbd1-177">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-177">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8cbd1-178">Clé de la section qui contient les paramètres à vérifier.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-178">Key of section that contains the settings to check.</span></span>

</dd> <dt>

<span data-ttu-id="8cbd1-179">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-179">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cbd1-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cbd1-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8cbd1-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cbd1-182">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-182">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8cbd1-183">Identificateur de l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-183">Identifier for the software element.</span></span>

<span data-ttu-id="8cbd1-184">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="8cbd1-184">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cbd1-185">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-185">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cbd1-186">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8cbd1-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8cbd1-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cbd1-188">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-188">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8cbd1-189">État d’un élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-189">State of a software element.</span></span>

<span data-ttu-id="8cbd1-190">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="8cbd1-190">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="8cbd1-191"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Déployable** (0)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-191"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8cbd1-192">Décrit les détails nécessaires à la réussite de la distribution et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État installable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="8cbd1-192">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="8cbd1-193"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installation** (1)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-193"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8cbd1-194">Décrit les détails nécessaires à l’installation réussie et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État exécutable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="8cbd1-194">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="8cbd1-195"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Exécutable** (2)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-195"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8cbd1-196">Décrit les détails nécessaires pour une exécution réussie et les détails (conditions et actions) requis pour créer un élément logiciel dans l’État en cours d’exécution (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="8cbd1-196">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="8cbd1-197"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**En cours d’exécution** (3)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-197"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8cbd1-198">Décrit les détails nécessaires à l’analyse et à l’utilisation d’un élément de début.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-198">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8cbd1-199">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-199">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cbd1-200">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-200">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8cbd1-201">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8cbd1-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cbd1-202">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informations sur les composants logiciels DMTF \| 002,5»)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-202">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="8cbd1-203">Système d’exploitation cible de l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-203">Target operating system of the software element.</span></span>

<span data-ttu-id="8cbd1-204">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="8cbd1-204">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8cbd1-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8cbd1-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="8cbd1-207"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-207"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8cbd1-208">Mac OS</span><span class="sxs-lookup"><span data-stu-id="8cbd1-208">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="8cbd1-209"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-209"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8cbd1-210">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="8cbd1-210">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="8cbd1-211"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-211"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="8cbd1-212"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-212"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="8cbd1-213"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX numérique** (6)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-213"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="8cbd1-214"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-214"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="8cbd1-215">Ouvrir des machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="8cbd1-215">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="8cbd1-216"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-216"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="8cbd1-217">HP-UX</span><span class="sxs-lookup"><span data-stu-id="8cbd1-217">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="8cbd1-218"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-218"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="8cbd1-219"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-219"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="8cbd1-220"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-220"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="8cbd1-221"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-221"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="8cbd1-222"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-222"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="8cbd1-223">Machine virtuelle Microsoft pour Java</span><span class="sxs-lookup"><span data-stu-id="8cbd1-223">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="8cbd1-224"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-224"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="8cbd1-225"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-225"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="8cbd1-226">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="8cbd1-226">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="8cbd1-227"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-227"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="8cbd1-228">Windows 95</span><span class="sxs-lookup"><span data-stu-id="8cbd1-228">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="8cbd1-229"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-229"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="8cbd1-230">Windows 98</span><span class="sxs-lookup"><span data-stu-id="8cbd1-230">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="8cbd1-231"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-231"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="8cbd1-232">Windows NT</span><span class="sxs-lookup"><span data-stu-id="8cbd1-232">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="8cbd1-233"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-233"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="8cbd1-234">Windows CE</span><span class="sxs-lookup"><span data-stu-id="8cbd1-234">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="8cbd1-235"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-235"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="8cbd1-236">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="8cbd1-236">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="8cbd1-237"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-237"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="8cbd1-238"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-238"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="8cbd1-239"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-239"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="8cbd1-240"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Dépendant d’UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-240"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="8cbd1-241"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-241"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="8cbd1-242"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-242"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="8cbd1-243"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-243"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="8cbd1-244"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-244"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="8cbd1-245"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-245"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="8cbd1-246"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-246"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="8cbd1-247"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-247"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="8cbd1-248"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-248"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="8cbd1-249">Une série</span><span class="sxs-lookup"><span data-stu-id="8cbd1-249">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="8cbd1-250"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-250"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="8cbd1-251">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="8cbd1-251">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="8cbd1-252"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-252"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="8cbd1-253">NT tandem</span><span class="sxs-lookup"><span data-stu-id="8cbd1-253">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="8cbd1-254"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-254"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="8cbd1-255">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="8cbd1-255">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="8cbd1-256"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-256"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="8cbd1-257"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-257"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="8cbd1-258"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-258"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="8cbd1-259"><span id="VM_ESA"></span><span id="vm_esa"></span>**Machine virtuelle/SEEE** (39)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-259"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="8cbd1-260"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactif** (40)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-260"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="8cbd1-261"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-261"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="8cbd1-262">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="8cbd1-262">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="8cbd1-263"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-263"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="8cbd1-264"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-264"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="8cbd1-265"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**Hurd gnu** (44)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-265"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="8cbd1-266"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-266"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="8cbd1-267">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="8cbd1-267">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="8cbd1-268"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Noyau Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-268"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="8cbd1-269"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-269"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="8cbd1-270"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-270"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="8cbd1-271"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-271"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="8cbd1-272"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-272"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="8cbd1-273"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-273"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="8cbd1-274"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menthe** (52)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-274"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="8cbd1-275"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-275"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="8cbd1-276"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-276"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="8cbd1-277"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-277"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="8cbd1-278"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-278"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="8cbd1-279">Palm OS</span><span class="sxs-lookup"><span data-stu-id="8cbd1-279">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="8cbd1-280"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-280"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="8cbd1-281"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-281"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="8cbd1-282"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dédié** (59)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-282"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="8cbd1-283"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-283"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="8cbd1-284"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="8cbd1-284"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8cbd1-285">**Version**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-285">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cbd1-286">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cbd1-287">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8cbd1-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cbd1-288">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Version**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="8cbd1-288">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="8cbd1-289">Version de l’opération.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-289">Version of the operation.</span></span>

<span data-ttu-id="8cbd1-290">La version de l’opération doit se présenter sous l’une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8cbd1-290">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="8cbd1-291"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="8cbd1-291"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="8cbd1-292"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="8cbd1-292"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="8cbd1-293">Cette propriété est héritée de la classe de [**\_ vérification CIM**](cim-check.md) .</span><span class="sxs-lookup"><span data-stu-id="8cbd1-293">This property is inherited from the [**CIM\_Check**](cim-check.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8cbd1-294">Notes</span><span class="sxs-lookup"><span data-stu-id="8cbd1-294">Remarks</span></span>

<span data-ttu-id="8cbd1-295">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-295">WMI does not implement this class.</span></span>

<span data-ttu-id="8cbd1-296">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-296">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8cbd1-297">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="8cbd1-297">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cbd1-298">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8cbd1-298">Requirements</span></span>



| <span data-ttu-id="8cbd1-299">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8cbd1-299">Requirement</span></span> | <span data-ttu-id="8cbd1-300">Valeur</span><span class="sxs-lookup"><span data-stu-id="8cbd1-300">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cbd1-301">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8cbd1-301">Minimum supported client</span></span><br/> | <span data-ttu-id="8cbd1-302">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8cbd1-302">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8cbd1-303">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8cbd1-303">Minimum supported server</span></span><br/> | <span data-ttu-id="8cbd1-304">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8cbd1-304">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8cbd1-305">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8cbd1-305">Namespace</span></span><br/>                | <span data-ttu-id="8cbd1-306">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="8cbd1-306">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8cbd1-307">MOF</span><span class="sxs-lookup"><span data-stu-id="8cbd1-307">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8cbd1-308"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8cbd1-308"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8cbd1-309">DLL</span><span class="sxs-lookup"><span data-stu-id="8cbd1-309">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cbd1-310"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cbd1-310"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cbd1-311">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8cbd1-311">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cbd1-312">**\_Vérification CIM**</span><span class="sxs-lookup"><span data-stu-id="8cbd1-312">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

