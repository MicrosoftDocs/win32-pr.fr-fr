---
description: La \_ classe WMI de l’Association PhysicalMemoryLocation Win32 associe un tableau de mémoire physique et sa mémoire physique.
ms.assetid: 40252428-77ca-4dfb-8048-c05096a114d8
ms.tgt_platform: multiple
title: Classe Win32_PhysicalMemoryLocation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemoryLocation
- Win32_PhysicalMemoryLocation.LocationWithinContainer
- Win32_PhysicalMemoryLocation.PartComponent
- Win32_PhysicalMemoryLocation.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: daa6d47b13cb5caa74a10f28ab5fcd6e66e1524f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950855"
---
# <a name="win32_physicalmemorylocation-class"></a><span data-ttu-id="9e9d2-103">\_Classe PhysicalMemoryLocation Win32</span><span class="sxs-lookup"><span data-stu-id="9e9d2-103">Win32\_PhysicalMemoryLocation class</span></span>

<span data-ttu-id="9e9d2-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ PhysicalMemoryLocation Win32** associe un tableau de mémoire physique et sa mémoire physique.</span><span class="sxs-lookup"><span data-stu-id="9e9d2-104">The **Win32\_PhysicalMemoryLocation** association [WMI class](../wmisdk/retrieving-a-class.md) relates an array of physical memory and its physical memory.</span></span>

<span data-ttu-id="9e9d2-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9e9d2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9e9d2-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="9e9d2-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e9d2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e9d2-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF562-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_PhysicalMemoryLocation : CIM_PackagedComponent
{
  string                        LocationWithinContainer;
  Win32_PhysicalMemory      REF PartComponent;
  Win32_PhysicalMemoryArray REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="9e9d2-108">Membres</span><span class="sxs-lookup"><span data-stu-id="9e9d2-108">Members</span></span>

<span data-ttu-id="9e9d2-109">La classe **Win32 \_ PhysicalMemoryLocation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9e9d2-109">The **Win32\_PhysicalMemoryLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="9e9d2-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9e9d2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9e9d2-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9e9d2-111">Properties</span></span>

<span data-ttu-id="9e9d2-112">La classe **Win32 \_ PhysicalMemoryLocation** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="9e9d2-112">The **Win32\_PhysicalMemoryLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9e9d2-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="9e9d2-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e9d2-114">Type de données : **Win32 \_ PhysicalMemoryArray**</span><span class="sxs-lookup"><span data-stu-id="9e9d2-114">Data type: **Win32\_PhysicalMemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="9e9d2-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9e9d2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e9d2-116">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PhysicalMemoryArray")</span><span class="sxs-lookup"><span data-stu-id="9e9d2-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PhysicalMemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="9e9d2-117">[**\_ PhysicalMemoryArray Win32**](win32-physicalmemoryarray.md) qui représente le tableau de mémoire physique qui contient la mémoire physique.</span><span class="sxs-lookup"><span data-stu-id="9e9d2-117">A [**Win32\_PhysicalMemoryArray**](win32-physicalmemoryarray.md) that represents the physical memory array that contains the physical memory.</span></span>

</dd> <dt>

<span data-ttu-id="9e9d2-118">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="9e9d2-118">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e9d2-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9e9d2-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e9d2-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9e9d2-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e9d2-121">Chaîne de forme libre qui représente le positionnement de l’élément physique dans le package physique.</span><span class="sxs-lookup"><span data-stu-id="9e9d2-121">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="9e9d2-122">Les informations relatives aux éléments stationnaires dans le conteneur (par exemple, « deuxième baie de lecteur à partir du haut »), des angles, des altitudes et d’autres données peuvent être enregistrées dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="9e9d2-122">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="9e9d2-123">Cette chaîne peut compléter ou être utilisée à la place de l’instanciation de l’objet d' [**\_ emplacement CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="9e9d2-123">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="9e9d2-124">Cette propriété est héritée [**du \_ conteneur CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="9e9d2-124">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e9d2-125">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="9e9d2-125">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e9d2-126">Type de données : **Win32 \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="9e9d2-126">Data type: **Win32\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="9e9d2-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9e9d2-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e9d2-128">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PhysicalMemory")</span><span class="sxs-lookup"><span data-stu-id="9e9d2-128">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PhysicalMemory")</span></span>
</dt> </dl>

<span data-ttu-id="9e9d2-129">[**\_ PhysicalMemory Win32**](win32-physicalmemory.md) qui représente la mémoire physique contenue dans le tableau de mémoire physique.</span><span class="sxs-lookup"><span data-stu-id="9e9d2-129">A [**Win32\_PhysicalMemory**](win32-physicalmemory.md) that represents the physical memory contained in the physical memory array.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e9d2-130">Notes</span><span class="sxs-lookup"><span data-stu-id="9e9d2-130">Remarks</span></span>

<span data-ttu-id="9e9d2-131">La classe **Win32 \_ PhysicalMemoryLocation** est dérivée de [**CIM \_ PackagedComponent**](cim-packagedcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="9e9d2-131">The **Win32\_PhysicalMemoryLocation** class is derived from [**CIM\_PackagedComponent**](cim-packagedcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e9d2-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e9d2-132">Requirements</span></span>



| <span data-ttu-id="9e9d2-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e9d2-133">Requirement</span></span> | <span data-ttu-id="9e9d2-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e9d2-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e9d2-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e9d2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9e9d2-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e9d2-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9e9d2-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e9d2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9e9d2-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e9d2-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9e9d2-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9e9d2-139">Namespace</span></span><br/>                | <span data-ttu-id="9e9d2-140">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="9e9d2-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9e9d2-141">MOF</span><span class="sxs-lookup"><span data-stu-id="9e9d2-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e9d2-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e9d2-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e9d2-143">DLL</span><span class="sxs-lookup"><span data-stu-id="9e9d2-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e9d2-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e9d2-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e9d2-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e9d2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e9d2-146">**\_PACKAGEDCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="9e9d2-146">**CIM\_PackagedComponent**</span></span>](cim-packagedcomponent.md)
</dt> <dt>

[<span data-ttu-id="9e9d2-147">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="9e9d2-147">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
