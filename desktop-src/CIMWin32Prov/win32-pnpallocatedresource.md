---
description: La \_ classe WMI de l’Association Win32 PnPAllocatedResource représente une association entre les unités logiques et les ressources système.
ms.assetid: e3cef457-cf88-4df5-8db8-b0495f636904
ms.tgt_platform: multiple
title: Classe Win32_PnPAllocatedResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPAllocatedResource
- Win32_PnPAllocatedResource.Antecedent
- Win32_PnPAllocatedResource.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 353009016c8d4d54cdc92fb8f0ed062567dded6f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861710"
---
# <a name="win32_pnpallocatedresource-class"></a><span data-ttu-id="1f917-103">\_Classe PnPAllocatedResource Win32</span><span class="sxs-lookup"><span data-stu-id="1f917-103">Win32\_PnPAllocatedResource class</span></span>

<span data-ttu-id="1f917-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **Win32 \_ PnPAllocatedResource** représente une association entre les unités logiques et les ressources système.</span><span class="sxs-lookup"><span data-stu-id="1f917-104">The **Win32\_PnPAllocatedResource** association [WMI class](../wmisdk/retrieving-a-class.md) represents an association between logical devices and system resources.</span></span> <span data-ttu-id="1f917-105">Cette classe est utilisée pour découvrir les ressources qui sont utilisées par un périphérique spécifique, par exemple une demande d’interruption (IRQ) ou un canal d’accès direct à la mémoire (DMA).</span><span class="sxs-lookup"><span data-stu-id="1f917-105">This class is used to discover the resources that are in-use by a specific device, such as an Interrupt ReQuest (IRQ) or a Direct Memory Access (DMA) channel.</span></span>

<span data-ttu-id="1f917-106">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="1f917-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1f917-107">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="1f917-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f917-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f917-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("970C0998-41FE-4275-B7D9-7DABAD3FBC4D"), AMENDMENT]
class Win32_PnPAllocatedResource : CIM_AllocatedResource
{
  CIM_SystemResource REF Antecedent;
  Win32_PnPEntity    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="1f917-109">Membres</span><span class="sxs-lookup"><span data-stu-id="1f917-109">Members</span></span>

<span data-ttu-id="1f917-110">La classe **Win32 \_ PnPAllocatedResource** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1f917-110">The **Win32\_PnPAllocatedResource** class has these types of members:</span></span>

-   [<span data-ttu-id="1f917-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1f917-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1f917-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1f917-112">Properties</span></span>

<span data-ttu-id="1f917-113">La classe **Win32 \_ PnPAllocatedResource** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="1f917-113">The **Win32\_PnPAllocatedResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1f917-114">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="1f917-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f917-115">Type de données : **CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="1f917-115">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="1f917-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1f917-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f917-117">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ SystemResource")</span><span class="sxs-lookup"><span data-stu-id="1f917-117">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_SystemResource")</span></span>
</dt> </dl>

<span data-ttu-id="1f917-118">Référence à l' [**instance \_ SystemResource CIM**](cim-systemresource.md) qui représente les propriétés d’une ressource système disponible pour l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="1f917-118">Reference to the [**CIM\_SystemResource**](cim-systemresource.md) instance that represents the properties of a system resource available to the logical device.</span></span> <span data-ttu-id="1f917-119">Cette propriété est héritée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="1f917-119">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f917-120">**Charge**</span><span class="sxs-lookup"><span data-stu-id="1f917-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f917-121">Type de données : **Win32 \_ PnPEntity**</span><span class="sxs-lookup"><span data-stu-id="1f917-121">Data type: **Win32\_PnPEntity**</span></span>
</dt> <dt>

<span data-ttu-id="1f917-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1f917-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f917-123">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) (« dépendant »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« CIM \| CIM \_ LogicalDevice »)</span><span class="sxs-lookup"><span data-stu-id="1f917-123">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="1f917-124">Référence à l’instance [**Win32 \_ PnPEntity**](win32-pnpentity.md) qui représente les propriétés de l’unité logique à l’aide des ressources système qui lui sont affectées.</span><span class="sxs-lookup"><span data-stu-id="1f917-124">Reference to the [**Win32\_PnPEntity**](win32-pnpentity.md) instance that represents the properties of the logical device using the system resources assigned to it.</span></span> <span data-ttu-id="1f917-125">Cette propriété est héritée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="1f917-125">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f917-126">Notes</span><span class="sxs-lookup"><span data-stu-id="1f917-126">Remarks</span></span>

<span data-ttu-id="1f917-127">La classe **Win32 \_ PnPAllocatedResource** est dérivée de [**CIM \_ AllocatedResource**](cim-allocatedresource.md).</span><span class="sxs-lookup"><span data-stu-id="1f917-127">The **Win32\_PnPAllocatedResource** class is derived from [**CIM\_AllocatedResource**](cim-allocatedresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f917-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f917-128">Requirements</span></span>



| <span data-ttu-id="1f917-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f917-129">Requirement</span></span> | <span data-ttu-id="1f917-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f917-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f917-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f917-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1f917-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f917-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1f917-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f917-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1f917-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f917-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1f917-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1f917-135">Namespace</span></span><br/>                | <span data-ttu-id="1f917-136">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="1f917-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1f917-137">MOF</span><span class="sxs-lookup"><span data-stu-id="1f917-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f917-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f917-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f917-139">DLL</span><span class="sxs-lookup"><span data-stu-id="1f917-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f917-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f917-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f917-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f917-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f917-142">**\_ALLOCATEDRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="1f917-142">**CIM\_AllocatedResource**</span></span>](cim-allocatedresource.md)
</dt> <dt>

[<span data-ttu-id="1f917-143">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="1f917-143">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
