---
description: La \_ classe WMI de l’Association AssociatedProcessorMemory Win32 associe un processeur et sa mémoire cache.
ms.assetid: 23da2a9d-772e-4258-9489-07d47801b2d8
ms.tgt_platform: multiple
title: Classe Win32_AssociatedProcessorMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AssociatedProcessorMemory
- Win32_AssociatedProcessorMemory.BusSpeed
- Win32_AssociatedProcessorMemory.Dependent
- Win32_AssociatedProcessorMemory.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3737dca869c539d1414c4399f35fb8f107697b70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950794"
---
# <a name="win32_associatedprocessormemory-class"></a><span data-ttu-id="84e2f-103">\_Classe AssociatedProcessorMemory Win32</span><span class="sxs-lookup"><span data-stu-id="84e2f-103">Win32\_AssociatedProcessorMemory class</span></span>

<span data-ttu-id="84e2f-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ AssociatedProcessorMemory Win32** associe un processeur et sa mémoire cache.</span><span class="sxs-lookup"><span data-stu-id="84e2f-104">The **Win32\_AssociatedProcessorMemory** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a processor and its cache memory.</span></span>

<span data-ttu-id="84e2f-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="84e2f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="84e2f-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="84e2f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="84e2f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84e2f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{074737F0-ACBC-11d2-ABF6-00805F538618}"), AMENDMENT]
class Win32_AssociatedProcessorMemory : CIM_AssociatedProcessorMemory
{
  uint32                BusSpeed;
  Win32_Processor   REF Dependent;
  Win32_CacheMemory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="84e2f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="84e2f-108">Members</span></span>

<span data-ttu-id="84e2f-109">La classe **Win32 \_ AssociatedProcessorMemory** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="84e2f-109">The **Win32\_AssociatedProcessorMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="84e2f-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="84e2f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84e2f-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="84e2f-111">Properties</span></span>

<span data-ttu-id="84e2f-112">La classe **Win32 \_ AssociatedProcessorMemory** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="84e2f-112">The **Win32\_AssociatedProcessorMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84e2f-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="84e2f-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84e2f-114">Type de données : **Win32 \_ CacheMemory**</span><span class="sxs-lookup"><span data-stu-id="84e2f-114">Data type: **Win32\_CacheMemory**</span></span>
</dt> <dt>

<span data-ttu-id="84e2f-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="84e2f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84e2f-116">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ CacheMemory")</span><span class="sxs-lookup"><span data-stu-id="84e2f-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_CacheMemory")</span></span>
</dt> </dl>

<span data-ttu-id="84e2f-117">[**\_ CacheMemory Win32**](win32-cachememory.md) qui décrit la mémoire cache disponible pour le processeur.</span><span class="sxs-lookup"><span data-stu-id="84e2f-117">A [**Win32\_CacheMemory**](win32-cachememory.md) that describes the cache memory available to the processor.</span></span>

</dd> <dt>

<span data-ttu-id="84e2f-118">**BusSpeed**</span><span class="sxs-lookup"><span data-stu-id="84e2f-118">**BusSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84e2f-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84e2f-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84e2f-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="84e2f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84e2f-121">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« mégahertz »)</span><span class="sxs-lookup"><span data-stu-id="84e2f-121">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="84e2f-122">Vitesse du bus, en mégahertz (MHz), entre le processeur et la mémoire.</span><span class="sxs-lookup"><span data-stu-id="84e2f-122">Speed of the bus, in megahertz (MHz), between the processor and memory.</span></span>

<span data-ttu-id="84e2f-123">Cette propriété est héritée de la [**\_ AssociatedProcessorMemory CIM**](cim-associatedprocessormemory.md).</span><span class="sxs-lookup"><span data-stu-id="84e2f-123">This property is inherited from [**CIM\_AssociatedProcessorMemory**](cim-associatedprocessormemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="84e2f-124">**Charge**</span><span class="sxs-lookup"><span data-stu-id="84e2f-124">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84e2f-125">Type de données **: \_ processeur Win32**</span><span class="sxs-lookup"><span data-stu-id="84e2f-125">Data type: **Win32\_Processor**</span></span>
</dt> <dt>

<span data-ttu-id="84e2f-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="84e2f-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84e2f-127">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« \| processeur Win32 WMI \_ »)</span><span class="sxs-lookup"><span data-stu-id="84e2f-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Processor")</span></span>
</dt> </dl>

<span data-ttu-id="84e2f-128">[**\_ Processeur Win32**](win32-processor.md) qui décrit le processeur qui utilise la mémoire cache.</span><span class="sxs-lookup"><span data-stu-id="84e2f-128">A [**Win32\_Processor**](win32-processor.md) that describes the processor that is using the cache memory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84e2f-129">Notes</span><span class="sxs-lookup"><span data-stu-id="84e2f-129">Remarks</span></span>

<span data-ttu-id="84e2f-130">La classe **Win32 \_ AssociatedProcessorMemory** est dérivée de [**CIM \_ AssociatedProcessorMemory**](cim-associatedprocessormemory.md).</span><span class="sxs-lookup"><span data-stu-id="84e2f-130">The **Win32\_AssociatedProcessorMemory** class is derived from [**CIM\_AssociatedProcessorMemory**](cim-associatedprocessormemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="84e2f-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84e2f-131">Requirements</span></span>



| <span data-ttu-id="84e2f-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84e2f-132">Requirement</span></span> | <span data-ttu-id="84e2f-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="84e2f-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84e2f-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84e2f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="84e2f-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84e2f-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="84e2f-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84e2f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="84e2f-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84e2f-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="84e2f-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="84e2f-138">Namespace</span></span><br/>                | <span data-ttu-id="84e2f-139">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="84e2f-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="84e2f-140">MOF</span><span class="sxs-lookup"><span data-stu-id="84e2f-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84e2f-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84e2f-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="84e2f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="84e2f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84e2f-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84e2f-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84e2f-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84e2f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84e2f-145">**\_ASSOCIATEDPROCESSORMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="84e2f-145">**CIM\_AssociatedProcessorMemory**</span></span>](cim-associatedprocessormemory.md)
</dt> <dt>

[<span data-ttu-id="84e2f-146">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="84e2f-146">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

