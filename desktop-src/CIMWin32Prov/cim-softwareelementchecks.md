---
description: La \_ classe d’association CIM SoftwareElementChecks associe un élément logiciel à des informations sur la condition ou l’emplacement qu’une fonctionnalité peut nécessiter.
ms.assetid: ff130fe9-ddb2-4e4f-86d3-53f1d8ed14aa
ms.tgt_platform: multiple
title: Classe CIM_SoftwareElementChecks
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementChecks
- CIM_SoftwareElementChecks.Check
- CIM_SoftwareElementChecks.Element
- CIM_SoftwareElementChecks.Phase
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea6fcb02794174e825994f70270745741c9b7713
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860841"
---
# <a name="cim_softwareelementchecks-class"></a><span data-ttu-id="c8027-103">\_Classe CIM SoftwareElementChecks</span><span class="sxs-lookup"><span data-stu-id="c8027-103">CIM\_SoftwareElementChecks class</span></span>

<span data-ttu-id="c8027-104">La classe d’association **CIM \_ SoftwareElementChecks** associe un élément logiciel à des informations sur la condition ou l’emplacement qu’une fonctionnalité peut nécessiter.</span><span class="sxs-lookup"><span data-stu-id="c8027-104">The **CIM\_SoftwareElementChecks** association class relates a software element with condition or location information that a feature may require.</span></span>

<span data-ttu-id="c8027-105">Étant donné que les éléments logiciels dans un état prêt à être en cours d’exécution ne peuvent pas passer à un autre État, la valeur de la propriété **phase** est limitée à in-State pour les objets [**CIM \_ SoftwareElement**](cim-softwareelement.md) dans un état prêt à être exécuté.</span><span class="sxs-lookup"><span data-stu-id="c8027-105">Because software elements in a ready-to-run state cannot transition into another state, the value of the **Phase** property is restricted to in-state for [**CIM\_SoftwareElement**](cim-softwareelement.md) objects in a ready-to-run state.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8027-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="c8027-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c8027-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c8027-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c8027-108">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c8027-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="c8027-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="c8027-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8027-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8027-110">Syntax</span></span>

``` syntax
[UUID("{24783E8A-DB31-11d2-85FC-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_SoftwareElementChecks
{
  CIM_Check           REF Check;
  CIM_SoftwareElement REF Element;
  uint16                  Phase;
};
```

## <a name="members"></a><span data-ttu-id="c8027-111">Membres</span><span class="sxs-lookup"><span data-stu-id="c8027-111">Members</span></span>

<span data-ttu-id="c8027-112">La classe **CIM \_ SoftwareElementChecks** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c8027-112">The **CIM\_SoftwareElementChecks** class has these types of members:</span></span>

-   [<span data-ttu-id="c8027-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c8027-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c8027-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c8027-114">Properties</span></span>

<span data-ttu-id="c8027-115">La classe **CIM \_ SoftwareElementChecks** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c8027-115">The **CIM\_SoftwareElementChecks** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c8027-116">**Vérification**</span><span class="sxs-lookup"><span data-stu-id="c8027-116">**Check**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8027-117">Type de données **: \_ vérification CIM**</span><span class="sxs-lookup"><span data-stu-id="c8027-117">Data type: **CIM\_Check**</span></span>
</dt> <dt>

<span data-ttu-id="c8027-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8027-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8027-119">Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c8027-119">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c8027-120">Référence à la vérification.</span><span class="sxs-lookup"><span data-stu-id="c8027-120">Reference to the check.</span></span>

</dd> <dt>

<span data-ttu-id="c8027-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="c8027-121">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8027-122">Type de données : **CIM \_ SoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="c8027-122">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="c8027-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8027-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8027-124">Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c8027-124">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c8027-125">Référence à l’élément.</span><span class="sxs-lookup"><span data-stu-id="c8027-125">Reference to the element.</span></span>

</dd> <dt>

<span data-ttu-id="c8027-126">**Phase**</span><span class="sxs-lookup"><span data-stu-id="c8027-126">**Phase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8027-127">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c8027-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c8027-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8027-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8027-129">Indique si le contrôle référencé est un contrôle à l’État ou un contrôle d’état suivant.</span><span class="sxs-lookup"><span data-stu-id="c8027-129">Indicates whether the referenced check is an in-state check or a next-state check.</span></span>

<dt>

<span id="In-State"></span><span id="in-state"></span><span id="IN-STATE"></span>

<span data-ttu-id="c8027-130">**In-State** (0)</span><span class="sxs-lookup"><span data-stu-id="c8027-130">**In-State** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Next-State"></span><span id="next-state"></span><span id="NEXT-STATE"></span>

<span data-ttu-id="c8027-131">**État suivant** (1)</span><span class="sxs-lookup"><span data-stu-id="c8027-131">**Next-State** (1)</span></span>


<span data-ttu-id="c8027-132"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c8027-132"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="c8027-133">Notes</span><span class="sxs-lookup"><span data-stu-id="c8027-133">Remarks</span></span>

<span data-ttu-id="c8027-134">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="c8027-134">WMI does not implement this class.</span></span> <span data-ttu-id="c8027-135">Pour les classes WMI dérivées de **CIM \_ SoftwareElementChecks**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c8027-135">For WMI classes derived from **CIM\_SoftwareElementChecks**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c8027-136">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="c8027-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c8027-137">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="c8027-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8027-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8027-138">Requirements</span></span>



| <span data-ttu-id="c8027-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8027-139">Requirement</span></span> | <span data-ttu-id="c8027-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8027-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8027-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8027-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c8027-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8027-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c8027-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8027-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c8027-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8027-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c8027-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c8027-145">Namespace</span></span><br/>                | <span data-ttu-id="c8027-146">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="c8027-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c8027-147">MOF</span><span class="sxs-lookup"><span data-stu-id="c8027-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8027-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8027-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8027-149">DLL</span><span class="sxs-lookup"><span data-stu-id="c8027-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8027-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8027-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

