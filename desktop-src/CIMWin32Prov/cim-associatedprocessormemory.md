---
description: La \_ classe CIM AssociatedProcessorMemory associe le processeur et la mémoire système, ou le cache d’un processeur.
ms.assetid: a4c28a0a-e4cc-4db2-bd77-b7b5023eace6
ms.tgt_platform: multiple
title: Classe CIM_AssociatedProcessorMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedProcessorMemory
- CIM_AssociatedProcessorMemory.Antecedent
- CIM_AssociatedProcessorMemory.Dependent
- CIM_AssociatedProcessorMemory.BusSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f35cdca92cb15e1c6fff215ff1363844e0d47012
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950731"
---
# <a name="cim_associatedprocessormemory-class"></a><span data-ttu-id="ca1f1-103">\_Classe CIM AssociatedProcessorMemory</span><span class="sxs-lookup"><span data-stu-id="ca1f1-103">CIM\_AssociatedProcessorMemory class</span></span>

<span data-ttu-id="ca1f1-104">La classe **CIM \_ AssociatedProcessorMemory** associe le processeur et la mémoire système, ou le cache d’un processeur.</span><span class="sxs-lookup"><span data-stu-id="ca1f1-104">The **CIM\_AssociatedProcessorMemory** class associates the processor and system memory, or a processor's cache.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ca1f1-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="ca1f1-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ca1f1-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ca1f1-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ca1f1-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ca1f1-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ca1f1-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="ca1f1-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca1f1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca1f1-109">Syntax</span></span>

``` syntax
[abstract, UUID("{464FFAB1-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedProcessorMemory : CIM_AssociatedMemory
{
  CIM_Memory    REF Antecedent;
  CIM_Processor REF Dependent;
  uint32            BusSpeed;
};
```

## <a name="members"></a><span data-ttu-id="ca1f1-110">Membres</span><span class="sxs-lookup"><span data-stu-id="ca1f1-110">Members</span></span>

<span data-ttu-id="ca1f1-111">La classe **CIM \_ AssociatedProcessorMemory** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ca1f1-111">The **CIM\_AssociatedProcessorMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="ca1f1-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ca1f1-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ca1f1-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ca1f1-113">Properties</span></span>

<span data-ttu-id="ca1f1-114">La classe **CIM \_ AssociatedProcessorMemory** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ca1f1-114">The **CIM\_AssociatedProcessorMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ca1f1-115">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="ca1f1-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca1f1-116">Type de données **: \_ mémoire CIM**</span><span class="sxs-lookup"><span data-stu-id="ca1f1-116">Data type: **CIM\_Memory**</span></span>
</dt> <dt>

<span data-ttu-id="ca1f1-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ca1f1-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca1f1-118">[**\_ Mémoire CIM**](cim-memory.md) qui décrit la mémoire installée sur un appareil ou associée à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="ca1f1-118">A [**CIM\_Memory**](cim-memory.md) that describes the memory installed on or associated with a device.</span></span>

<span data-ttu-id="ca1f1-119">Cette propriété est héritée de la [**\_ AssociatedMemory CIM**](cim-associatedmemory.md).</span><span class="sxs-lookup"><span data-stu-id="ca1f1-119">This property is inherited from [**CIM\_AssociatedMemory**](cim-associatedmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca1f1-120">**BusSpeed**</span><span class="sxs-lookup"><span data-stu-id="ca1f1-120">**BusSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca1f1-121">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ca1f1-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca1f1-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ca1f1-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca1f1-123">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« mégahertz »)</span><span class="sxs-lookup"><span data-stu-id="ca1f1-123">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="ca1f1-124">Vitesse du bus, en mégahertz (MHz), entre le processeur et la mémoire.</span><span class="sxs-lookup"><span data-stu-id="ca1f1-124">Speed of the bus, in megahertz (MHz), between the processor and memory.</span></span>

</dd> <dt>

<span data-ttu-id="ca1f1-125">**Charge**</span><span class="sxs-lookup"><span data-stu-id="ca1f1-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca1f1-126">Type de données **: \_ processeur CIM**</span><span class="sxs-lookup"><span data-stu-id="ca1f1-126">Data type: **CIM\_Processor**</span></span>
</dt> <dt>

<span data-ttu-id="ca1f1-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ca1f1-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca1f1-128">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="ca1f1-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="ca1f1-129">[**\_ Processeur CIM**](cim-processor.md) décrivant le processeur qui accède à la mémoire ou utilise le cache.</span><span class="sxs-lookup"><span data-stu-id="ca1f1-129">A [**CIM\_Processor**](cim-processor.md) describing the processor that accesses the memory or uses the cache.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca1f1-130">Notes</span><span class="sxs-lookup"><span data-stu-id="ca1f1-130">Remarks</span></span>

<span data-ttu-id="ca1f1-131">La classe **CIM \_ AssociatedProcessorMemory** est dérivée de [**CIM \_ AssociatedMemory**](cim-associatedmemory.md).</span><span class="sxs-lookup"><span data-stu-id="ca1f1-131">The **CIM\_AssociatedProcessorMemory** class is derived from [**CIM\_AssociatedMemory**](cim-associatedmemory.md).</span></span>

<span data-ttu-id="ca1f1-132">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="ca1f1-132">WMI does not implement this class.</span></span> <span data-ttu-id="ca1f1-133">Pour plus d’informations sur les classes dérivées de **CIM \_ AssociatedProcessorMemory**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ca1f1-133">For more information about classes derived from **CIM\_AssociatedProcessorMemory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="ca1f1-134">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="ca1f1-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ca1f1-135">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="ca1f1-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca1f1-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca1f1-136">Requirements</span></span>



| <span data-ttu-id="ca1f1-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca1f1-137">Requirement</span></span> | <span data-ttu-id="ca1f1-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca1f1-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca1f1-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca1f1-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ca1f1-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca1f1-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ca1f1-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca1f1-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ca1f1-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca1f1-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ca1f1-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ca1f1-143">Namespace</span></span><br/>                | <span data-ttu-id="ca1f1-144">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ca1f1-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ca1f1-145">MOF</span><span class="sxs-lookup"><span data-stu-id="ca1f1-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca1f1-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca1f1-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca1f1-147">DLL</span><span class="sxs-lookup"><span data-stu-id="ca1f1-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca1f1-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca1f1-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca1f1-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca1f1-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca1f1-150">**\_ASSOCIATEDMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="ca1f1-150">**CIM\_AssociatedMemory**</span></span>](cim-associatedmemory.md)
</dt> </dl>

 

