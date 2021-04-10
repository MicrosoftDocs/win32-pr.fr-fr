---
description: La \_ classe WMI de l’Association AllocatedResource Win32 associe un appareil logique à une ressource système. Cette classe est utilisée pour détecter les ressources, telles que les IRQ ou les canaux DMA, qui sont utilisées par un appareil spécifique.
ms.assetid: cfac1209-1405-4fee-847c-8a61504bfac1
ms.tgt_platform: multiple
title: Classe Win32_AllocatedResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AllocatedResource
- Win32_AllocatedResource.Dependent
- Win32_AllocatedResource.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 87a57e53a85e4433ae325fc2ed441211db75b79f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950795"
---
# <a name="win32_allocatedresource-class"></a><span data-ttu-id="9ef46-104">\_Classe AllocatedResource Win32</span><span class="sxs-lookup"><span data-stu-id="9ef46-104">Win32\_AllocatedResource class</span></span>

<span data-ttu-id="9ef46-105">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ AllocatedResource Win32** associe un appareil logique à une ressource système.</span><span class="sxs-lookup"><span data-stu-id="9ef46-105">The **Win32\_AllocatedResource** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical device to a system resource.</span></span> <span data-ttu-id="9ef46-106">Cette classe est utilisée pour détecter les ressources, telles que les IRQ ou les canaux DMA, qui sont utilisées par un appareil spécifique.</span><span class="sxs-lookup"><span data-stu-id="9ef46-106">This class is used to discover which resources, such as IRQs or DMA channels, are in use by a specific device.</span></span>

<span data-ttu-id="9ef46-107">Cette classe est obsolète.</span><span class="sxs-lookup"><span data-stu-id="9ef46-107">This class is obsolete.</span></span> <span data-ttu-id="9ef46-108">À la place de cette classe, vous devez utiliser les propriétés de la classe [**Win32 \_ PNPAllocatedResource**](win32-pnpallocatedresource.md) .</span><span class="sxs-lookup"><span data-stu-id="9ef46-108">In place of this class, you should use the properties in the [**Win32\_PNPAllocatedResource**](win32-pnpallocatedresource.md) class.</span></span>

<span data-ttu-id="9ef46-109">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9ef46-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9ef46-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="9ef46-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ef46-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ef46-111">Syntax</span></span>

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), UUID("{8502C50D-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_AllocatedResource : CIM_Dependency
{
  CIM_LogicalDevice  REF Dependent;
  CIM_SystemResource REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="9ef46-112">Membres</span><span class="sxs-lookup"><span data-stu-id="9ef46-112">Members</span></span>

<span data-ttu-id="9ef46-113">La classe **Win32 \_ AllocatedResource** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9ef46-113">The **Win32\_AllocatedResource** class has these types of members:</span></span>

-   [<span data-ttu-id="9ef46-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9ef46-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9ef46-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9ef46-115">Properties</span></span>

<span data-ttu-id="9ef46-116">La classe **Win32 \_ AllocatedResource** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="9ef46-116">The **Win32\_AllocatedResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9ef46-117">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="9ef46-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ef46-118">Type de données : **CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="9ef46-118">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="9ef46-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ef46-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ef46-120">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ SystemResource")</span><span class="sxs-lookup"><span data-stu-id="9ef46-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_SystemResource")</span></span>
</dt> </dl>

<span data-ttu-id="9ef46-121">[**\_ SystemResource CIM**](cim-systemresource.md) qui décrit les propriétés d’une ressource système disponible pour l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="9ef46-121">A [**CIM\_SystemResource**](cim-systemresource.md) that describes the properties of a system resource available to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="9ef46-122">**Charge**</span><span class="sxs-lookup"><span data-stu-id="9ef46-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ef46-123">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="9ef46-123">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="9ef46-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ef46-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ef46-125">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« CIM \| CIM \_ LogicalDevice »)</span><span class="sxs-lookup"><span data-stu-id="9ef46-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="9ef46-126">[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui représente les propriétés de l’appareil logique qui utilise les ressources système qui lui sont affectées.</span><span class="sxs-lookup"><span data-stu-id="9ef46-126">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the properties of the logical device that is using the system resources assigned to it.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ef46-127">Notes</span><span class="sxs-lookup"><span data-stu-id="9ef46-127">Remarks</span></span>

<span data-ttu-id="9ef46-128">La classe **Win32 \_ AllocatedResource** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="9ef46-128">The **Win32\_AllocatedResource** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ef46-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ef46-129">Requirements</span></span>



| <span data-ttu-id="9ef46-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ef46-130">Requirement</span></span> | <span data-ttu-id="9ef46-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ef46-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ef46-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ef46-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9ef46-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ef46-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9ef46-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ef46-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9ef46-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ef46-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9ef46-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9ef46-136">Namespace</span></span><br/>                | <span data-ttu-id="9ef46-137">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="9ef46-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9ef46-138">MOF</span><span class="sxs-lookup"><span data-stu-id="9ef46-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ef46-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ef46-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ef46-140">DLL</span><span class="sxs-lookup"><span data-stu-id="9ef46-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ef46-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ef46-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ef46-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ef46-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ef46-143">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="9ef46-143">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="9ef46-144">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="9ef46-144">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

