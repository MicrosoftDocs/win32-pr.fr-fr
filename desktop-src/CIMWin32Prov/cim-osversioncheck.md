---
description: La \_ classe CIM OSVersionCheck spécifie les versions du système d’exploitation qui peuvent prendre en charge un élément logiciel.
ms.assetid: 6796cfc4-3b6f-43a4-b5f0-854a95284238
ms.tgt_platform: multiple
title: Classe CIM_OSVersionCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OSVersionCheck
- CIM_OSVersionCheck.CheckID
- CIM_OSVersionCheck.Caption
- CIM_OSVersionCheck.Description
- CIM_OSVersionCheck.CheckMode
- CIM_OSVersionCheck.Name
- CIM_OSVersionCheck.TargetOperatingSystem
- CIM_OSVersionCheck.Version
- CIM_OSVersionCheck.SoftwareElementID
- CIM_OSVersionCheck.SoftwareElementState
- CIM_OSVersionCheck.MaximumVersion
- CIM_OSVersionCheck.MinimumVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c341b9038b5b40b559b4a121adb88fbb2d7b5205
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033702"
---
# <a name="cim_osversioncheck-class"></a><span data-ttu-id="9ecbc-103">\_Classe CIM OSVersionCheck</span><span class="sxs-lookup"><span data-stu-id="9ecbc-103">CIM\_OSVersionCheck class</span></span>

<span data-ttu-id="9ecbc-104">La classe **CIM \_ OSVersionCheck** spécifie les versions du système d’exploitation qui peuvent prendre en charge un élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-104">The **CIM\_OSVersionCheck** class specifies the versions of the operating system that can support a software element.</span></span> <span data-ttu-id="9ecbc-105">La vérification peut être exécutée pour une plage de versions de système d’exploitation spécifique, minimale, maximale ou.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-105">The check can be run for a specific, minimum, maximum, or a range of operating system releases.</span></span> <span data-ttu-id="9ecbc-106">Pour spécifier une version spécifique du système d’exploitation, les versions minimale et maximale doivent être égales.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-106">To specify a specific operating system version, the minimum and maximum versions must be equal.</span></span> <span data-ttu-id="9ecbc-107">Pour spécifier la version minimale, la version minimale doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-107">To specify the minimum version, the minimum version only must be specified.</span></span> <span data-ttu-id="9ecbc-108">Pour spécifier une version maximale, vous devez uniquement spécifier la version maximale.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-108">To specify a maximum version, the maximum version only needs to be specified.</span></span> <span data-ttu-id="9ecbc-109">Pour spécifier une plage, les versions minimale et maximale doivent être spécifiées.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-109">To specify a range, both minimum and maximum versions must be specified.</span></span>

<span data-ttu-id="9ecbc-110">Le type de système d’exploitation est spécifié dans la propriété **TargetOperatingSystem** de l’élément Software propriétaire.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-110">The type of operating system is specified in the **TargetOperatingSystem** property of the owning software element.</span></span> <span data-ttu-id="9ecbc-111">Les détails des vérifications sont comparés aux détails correspondants trouvés dans un objet [**CIM \_ OperatingSystem**](cim-operatingsystem.md) référencé par une association [**CIM \_ installée**](cim-installedos.md) pour l’objet [**\_ ComputerSystem CIM**](cim-computersystem.md) qui décrit l’environnement.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-111">Details of the checks are compared with the corresponding details found in a [**CIM\_OperatingSystem**](cim-operatingsystem.md) object referenced by a [**CIM\_InstalledOS**](cim-installedos.md) association for the [**CIM\_ComputerSystem**](cim-computersystem.md) object that describes the environment.</span></span> <span data-ttu-id="9ecbc-112">Au moins une classe **CIM \_ OperatingSystem** doit satisfaire les détails de la condition pour que la vérification soit satisfaite.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-112">At least one **CIM\_OperatingSystem** class must satisfy the details of the condition for the check to be satisfied.</span></span> <span data-ttu-id="9ecbc-113">En d’autres termes, tous les systèmes d’exploitation sur le système d’exploitation approprié doivent satisfaire à la condition.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-113">In other words, not all of the operating systems on the relevant computer system need to satisfy the condition.</span></span> <span data-ttu-id="9ecbc-114">En outre, la propriété **OSTYPE** de la classe **CIM \_ OperatingSystem** doit correspondre au type de la propriété **TargetOperatingSystem** .</span><span class="sxs-lookup"><span data-stu-id="9ecbc-114">Also, the **OSType** property of the **CIM\_OperatingSystem** class must match the type of the **TargetOperatingSystem** property.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9ecbc-115">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-115">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9ecbc-116">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9ecbc-116">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9ecbc-117">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-117">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9ecbc-118">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-118">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ecbc-119">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ecbc-119">Syntax</span></span>

``` syntax
[UUID("{FEE8368A-DB2A-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_OSVersionCheck : CIM_Check
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
  string  MaximumVersion;
  string  MinimumVersion;
};
```

## <a name="members"></a><span data-ttu-id="9ecbc-120">Membres</span><span class="sxs-lookup"><span data-stu-id="9ecbc-120">Members</span></span>

<span data-ttu-id="9ecbc-121">La classe **CIM \_ OSVersionCheck** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9ecbc-121">The **CIM\_OSVersionCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="9ecbc-122">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9ecbc-122">Methods</span></span>](#methods)
-   [<span data-ttu-id="9ecbc-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9ecbc-123">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9ecbc-124">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9ecbc-124">Methods</span></span>

<span data-ttu-id="9ecbc-125">La classe **CIM \_ OSVersionCheck** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-125">The **CIM\_OSVersionCheck** class has these methods.</span></span>



| <span data-ttu-id="9ecbc-126">Méthode</span><span class="sxs-lookup"><span data-stu-id="9ecbc-126">Method</span></span>                                                      | <span data-ttu-id="9ecbc-127">Description</span><span class="sxs-lookup"><span data-stu-id="9ecbc-127">Description</span></span>                                                   |
|:------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="9ecbc-128">**Appeler**</span><span class="sxs-lookup"><span data-stu-id="9ecbc-128">**Invoke**</span></span>](invoke-method-in-class-cim-osversioncheck.md) | <span data-ttu-id="9ecbc-129">Effectue une action particulière.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-129">Takes a particular action.</span></span> <span data-ttu-id="9ecbc-130">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-130">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9ecbc-131">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9ecbc-131">Properties</span></span>

<span data-ttu-id="9ecbc-132">La classe **CIM \_ OSVersionCheck** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-132">The **CIM\_OSVersionCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9ecbc-133">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9ecbc-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecbc-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9ecbc-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ecbc-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ecbc-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ecbc-136">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-136">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9ecbc-137">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-137">A short textual description of the subject.</span></span>

<span data-ttu-id="9ecbc-138">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9ecbc-138">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ecbc-139">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="9ecbc-139">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecbc-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9ecbc-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ecbc-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ecbc-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ecbc-142">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-142">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9ecbc-143">Identificateur utilisé conjointement avec d’autres clés pour identifier de manière unique la vérification.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-143">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="9ecbc-144">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9ecbc-144">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ecbc-145">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="9ecbc-145">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecbc-146">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9ecbc-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9ecbc-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ecbc-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ecbc-148">Si la **valeur est true**, la condition est supposée exister dans l’environnement.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-148">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="9ecbc-149">Par exemple, un fichier est censé se trouver sur un système. la méthode [**Invoke**](invoke-method-in-class-cim-check.md) doit donc retourner la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-149">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="9ecbc-150">Si la **valeur est false**, la condition n’est pas censée exister.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-150">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="9ecbc-151">Par exemple, un fichier ne se trouve pas sur un système, donc la méthode [**Invoke**](invoke-method-in-class-cim-check.md) doit retourner **false**.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-151">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="9ecbc-152">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9ecbc-152">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ecbc-153">**Description**</span><span class="sxs-lookup"><span data-stu-id="9ecbc-153">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecbc-154">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9ecbc-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ecbc-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ecbc-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ecbc-156">Description des objets.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-156">A description of the objects.</span></span>

<span data-ttu-id="9ecbc-157">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9ecbc-157">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ecbc-158">**MaximumVersion**</span><span class="sxs-lookup"><span data-stu-id="9ecbc-158">**MaximumVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecbc-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9ecbc-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ecbc-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ecbc-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ecbc-161">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**Version**")</span><span class="sxs-lookup"><span data-stu-id="9ecbc-161">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Version**")</span></span>
</dt> </dl>

<span data-ttu-id="9ecbc-162">Version maximale du système d’exploitation requis.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-162">Maximum version of the required operating system.</span></span>

<span data-ttu-id="9ecbc-163">La valeur est encodée dans l’une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9ecbc-163">The value is encoded in one of the following forms:</span></span>

-   <span data-ttu-id="9ecbc-164"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="9ecbc-164"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="9ecbc-165"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="9ecbc-165"><major>.<minor><letter><revision></span></span>

</dd> <dt>

<span data-ttu-id="9ecbc-166">**MinimumVersion**</span><span class="sxs-lookup"><span data-stu-id="9ecbc-166">**MinimumVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecbc-167">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9ecbc-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ecbc-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ecbc-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ecbc-169">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**Version**")</span><span class="sxs-lookup"><span data-stu-id="9ecbc-169">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Version**")</span></span>
</dt> </dl>

<span data-ttu-id="9ecbc-170">Version minimale du système d’exploitation requis.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-170">Minimum version of the required operating system.</span></span>

<span data-ttu-id="9ecbc-171">La valeur est encodée dans l’une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9ecbc-171">The value is encoded in one of the following forms:</span></span>

-   <span data-ttu-id="9ecbc-172"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="9ecbc-172"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="9ecbc-173"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="9ecbc-173"><major>.<minor><letter><revision></span></span>

</dd> <dt>

<span data-ttu-id="9ecbc-174">**Nom**</span><span class="sxs-lookup"><span data-stu-id="9ecbc-174">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecbc-175">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9ecbc-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ecbc-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ecbc-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ecbc-177">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-177">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9ecbc-178">Nom utilisé pour identifier l’élément logiciel</span><span class="sxs-lookup"><span data-stu-id="9ecbc-178">Name used to identify the software element</span></span>

<span data-ttu-id="9ecbc-179">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9ecbc-179">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ecbc-180">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="9ecbc-180">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecbc-181">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9ecbc-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ecbc-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ecbc-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ecbc-183">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-183">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9ecbc-184">Il s’agit d’un identificateur pour cet élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-184">This is an identifier for this software element.</span></span>

<span data-ttu-id="9ecbc-185">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9ecbc-185">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ecbc-186">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="9ecbc-186">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecbc-187">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9ecbc-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9ecbc-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ecbc-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ecbc-189">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-189">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9ecbc-190">État de l’élément logiciel d’un élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-190">The software element state of a software element.</span></span>

<span data-ttu-id="9ecbc-191">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9ecbc-191">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="9ecbc-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Déployable** (0)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="9ecbc-193">Décrit les détails nécessaires à la réussite de la distribution et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État installable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="9ecbc-193">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="9ecbc-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installation** (1)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9ecbc-195">Décrit les détails nécessaires à l’installation réussie et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État exécutable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="9ecbc-195">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="9ecbc-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Exécutable** (2)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9ecbc-197">Décrit les détails nécessaires pour une exécution réussie et les détails (conditions et actions) requis pour créer un élément logiciel dans l’État en cours d’exécution (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="9ecbc-197">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="9ecbc-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**En cours d’exécution** (3)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9ecbc-199">Décrit les détails nécessaires à l’analyse et à l’utilisation d’un élément de début.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-199">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9ecbc-200">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="9ecbc-200">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecbc-201">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9ecbc-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9ecbc-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ecbc-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ecbc-203">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informations sur les composants logiciels DMTF \| 002,5»)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-203">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="9ecbc-204">Système d’exploitation cible de l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-204">Target operating system of the software element.</span></span>

<span data-ttu-id="9ecbc-205">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9ecbc-205">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ecbc-206"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-206"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9ecbc-207"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-207"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="9ecbc-208"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-208"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9ecbc-209">Mac OS</span><span class="sxs-lookup"><span data-stu-id="9ecbc-209">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="9ecbc-210"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-210"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9ecbc-211">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="9ecbc-211">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="9ecbc-212"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-212"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="9ecbc-213"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-213"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="9ecbc-214"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX numérique** (6)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-214"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="9ecbc-215"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-215"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9ecbc-216">Ouvrir des machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="9ecbc-216">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="9ecbc-217"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-217"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="9ecbc-218">HP-UX</span><span class="sxs-lookup"><span data-stu-id="9ecbc-218">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="9ecbc-219"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-219"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="9ecbc-220"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-220"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="9ecbc-221"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-221"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="9ecbc-222"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-222"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="9ecbc-223"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-223"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9ecbc-224">Machine virtuelle Microsoft pour Java</span><span class="sxs-lookup"><span data-stu-id="9ecbc-224">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="9ecbc-225"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-225"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="9ecbc-226"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-226"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="9ecbc-227">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="9ecbc-227">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="9ecbc-228"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-228"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="9ecbc-229">Windows 95</span><span class="sxs-lookup"><span data-stu-id="9ecbc-229">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="9ecbc-230"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-230"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="9ecbc-231">Windows 98</span><span class="sxs-lookup"><span data-stu-id="9ecbc-231">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="9ecbc-232"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-232"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="9ecbc-233">Windows NT</span><span class="sxs-lookup"><span data-stu-id="9ecbc-233">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="9ecbc-234"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-234"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="9ecbc-235">Windows CE</span><span class="sxs-lookup"><span data-stu-id="9ecbc-235">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="9ecbc-236"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-236"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="9ecbc-237">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="9ecbc-237">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="9ecbc-238"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-238"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="9ecbc-239"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-239"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="9ecbc-240"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-240"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="9ecbc-241"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Dépendant d’UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-241"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="9ecbc-242"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-242"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="9ecbc-243"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-243"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="9ecbc-244"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-244"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="9ecbc-245"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-245"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="9ecbc-246"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-246"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="9ecbc-247"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-247"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="9ecbc-248"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-248"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="9ecbc-249"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-249"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="9ecbc-250">Une série</span><span class="sxs-lookup"><span data-stu-id="9ecbc-250">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="9ecbc-251"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-251"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="9ecbc-252">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="9ecbc-252">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="9ecbc-253"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-253"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="9ecbc-254">NT tandem</span><span class="sxs-lookup"><span data-stu-id="9ecbc-254">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="9ecbc-255"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-255"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="9ecbc-256">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="9ecbc-256">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="9ecbc-257"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-257"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="9ecbc-258"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-258"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="9ecbc-259"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-259"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="9ecbc-260"><span id="VM_ESA"></span><span id="vm_esa"></span>**Machine virtuelle/SEEE** (39)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-260"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="9ecbc-261"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactif** (40)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-261"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="9ecbc-262"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-262"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="9ecbc-263">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="9ecbc-263">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="9ecbc-264"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-264"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="9ecbc-265"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-265"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="9ecbc-266"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**Hurd gnu** (44)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-266"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="9ecbc-267"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-267"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="9ecbc-268">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="9ecbc-268">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="9ecbc-269"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Noyau Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-269"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="9ecbc-270"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-270"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="9ecbc-271"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-271"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="9ecbc-272"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-272"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="9ecbc-273"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-273"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="9ecbc-274"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-274"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="9ecbc-275"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menthe** (52)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-275"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="9ecbc-276"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-276"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="9ecbc-277"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-277"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="9ecbc-278"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-278"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="9ecbc-279"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-279"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="9ecbc-280">Palm OS</span><span class="sxs-lookup"><span data-stu-id="9ecbc-280">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="9ecbc-281"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-281"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="9ecbc-282"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-282"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="9ecbc-283"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dédié** (59)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-283"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="9ecbc-284"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-284"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="9ecbc-285"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="9ecbc-285"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9ecbc-286">**Version**</span><span class="sxs-lookup"><span data-stu-id="9ecbc-286">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecbc-287">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9ecbc-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ecbc-288">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ecbc-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ecbc-289">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Version**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="9ecbc-289">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="9ecbc-290">Version de l’opération.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-290">Version of the operation.</span></span>

<span data-ttu-id="9ecbc-291">La version de l’opération doit se présenter sous l’une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9ecbc-291">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="9ecbc-292"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="9ecbc-292"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="9ecbc-293"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="9ecbc-293"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="9ecbc-294">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9ecbc-294">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ecbc-295">Notes</span><span class="sxs-lookup"><span data-stu-id="9ecbc-295">Remarks</span></span>

<span data-ttu-id="9ecbc-296">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-296">WMI does not implement this class.</span></span>

<span data-ttu-id="9ecbc-297">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-297">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9ecbc-298">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="9ecbc-298">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ecbc-299">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ecbc-299">Requirements</span></span>



| <span data-ttu-id="9ecbc-300">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ecbc-300">Requirement</span></span> | <span data-ttu-id="9ecbc-301">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ecbc-301">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ecbc-302">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ecbc-302">Minimum supported client</span></span><br/> | <span data-ttu-id="9ecbc-303">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ecbc-303">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9ecbc-304">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ecbc-304">Minimum supported server</span></span><br/> | <span data-ttu-id="9ecbc-305">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ecbc-305">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9ecbc-306">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9ecbc-306">Namespace</span></span><br/>                | <span data-ttu-id="9ecbc-307">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="9ecbc-307">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9ecbc-308">MOF</span><span class="sxs-lookup"><span data-stu-id="9ecbc-308">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ecbc-309"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ecbc-309"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ecbc-310">DLL</span><span class="sxs-lookup"><span data-stu-id="9ecbc-310">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ecbc-311"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ecbc-311"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ecbc-312">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ecbc-312">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ecbc-313">**\_Vérification CIM**</span><span class="sxs-lookup"><span data-stu-id="9ecbc-313">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

