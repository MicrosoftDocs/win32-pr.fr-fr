---
description: L' \_ Association CIM SoftwareElementActions identifie les actions d’un élément logiciel.
ms.assetid: 2f8a584c-dff0-48f8-bc5f-2b833b5c0b18
ms.tgt_platform: multiple
title: Classe CIM_SoftwareElementActions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementActions
- CIM_SoftwareElementActions.Action
- CIM_SoftwareElementActions.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f51cc122cdf354be9611ca1cca4ebcbe1635d14
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513125"
---
# <a name="cim_softwareelementactions-class"></a><span data-ttu-id="7bd6b-103">\_Classe CIM SoftwareElementActions</span><span class="sxs-lookup"><span data-stu-id="7bd6b-103">CIM\_SoftwareElementActions class</span></span>

<span data-ttu-id="7bd6b-104">L’Association **CIM \_ SoftwareElementActions** identifie les actions d’un élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="7bd6b-104">The **CIM\_SoftwareElementActions** association identifies the actions for a software element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7bd6b-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="7bd6b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7bd6b-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7bd6b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7bd6b-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7bd6b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="7bd6b-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="7bd6b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bd6b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7bd6b-109">Syntax</span></span>

``` syntax
[UUID("{4B82D255-E3CD-11d2-8601-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_SoftwareElementActions
{
  CIM_Action          REF Action;
  CIM_SoftwareElement REF Element;
};
```

## <a name="members"></a><span data-ttu-id="7bd6b-110">Membres</span><span class="sxs-lookup"><span data-stu-id="7bd6b-110">Members</span></span>

<span data-ttu-id="7bd6b-111">La classe **CIM \_ SoftwareElementActions** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7bd6b-111">The **CIM\_SoftwareElementActions** class has these types of members:</span></span>

-   [<span data-ttu-id="7bd6b-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7bd6b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7bd6b-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7bd6b-113">Properties</span></span>

<span data-ttu-id="7bd6b-114">La classe **CIM \_ SoftwareElementActions** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7bd6b-114">The **CIM\_SoftwareElementActions** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7bd6b-115">**Action**</span><span class="sxs-lookup"><span data-stu-id="7bd6b-115">**Action**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bd6b-116">Type de données **: \_ action CIM**</span><span class="sxs-lookup"><span data-stu-id="7bd6b-116">Data type: **CIM\_Action**</span></span>
</dt> <dt>

<span data-ttu-id="7bd6b-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7bd6b-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bd6b-118">Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7bd6b-118">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7bd6b-119">Référence à une instance d' [**\_ action CIM**](cim-action.md) .</span><span class="sxs-lookup"><span data-stu-id="7bd6b-119">Reference to a [**CIM\_Action**](cim-action.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="7bd6b-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="7bd6b-120">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bd6b-121">Type de données : **CIM \_ SoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="7bd6b-121">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="7bd6b-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7bd6b-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bd6b-123">Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7bd6b-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7bd6b-124">Référence à une [**instance \_ SoftwareElement CIM**](cim-softwareelement.md) .</span><span class="sxs-lookup"><span data-stu-id="7bd6b-124">Reference to a [**CIM\_SoftwareElement**](cim-softwareelement.md) instance.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7bd6b-125">Notes</span><span class="sxs-lookup"><span data-stu-id="7bd6b-125">Remarks</span></span>

<span data-ttu-id="7bd6b-126">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="7bd6b-126">WMI does not implement this class.</span></span> <span data-ttu-id="7bd6b-127">Pour les classes WMI dérivées de **CIM \_ SoftwareElementActions**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7bd6b-127">For WMI classes derived from **CIM\_SoftwareElementActions**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="7bd6b-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="7bd6b-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7bd6b-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="7bd6b-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bd6b-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7bd6b-130">Requirements</span></span>



| <span data-ttu-id="7bd6b-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7bd6b-131">Requirement</span></span> | <span data-ttu-id="7bd6b-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="7bd6b-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bd6b-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bd6b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7bd6b-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7bd6b-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7bd6b-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bd6b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7bd6b-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7bd6b-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7bd6b-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7bd6b-137">Namespace</span></span><br/>                | <span data-ttu-id="7bd6b-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="7bd6b-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7bd6b-139">MOF</span><span class="sxs-lookup"><span data-stu-id="7bd6b-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7bd6b-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7bd6b-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7bd6b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7bd6b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bd6b-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bd6b-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

