---
description: La \_ classe WMI de l’Association MemoryDeviceLocation Win32 fait référence à un périphérique de mémoire et à la mémoire physique sur laquelle il existe.
ms.assetid: 6fef916e-44e2-4b9f-94b7-c7204259004a
ms.tgt_platform: multiple
title: Classe Win32_MemoryDeviceLocation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryDeviceLocation
- Win32_MemoryDeviceLocation.Dependent
- Win32_MemoryDeviceLocation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5cf1ba93a2574810892443aefa43e1c7c501636c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950478"
---
# <a name="win32_memorydevicelocation-class"></a><span data-ttu-id="fb581-103">\_Classe MemoryDeviceLocation Win32</span><span class="sxs-lookup"><span data-stu-id="fb581-103">Win32\_MemoryDeviceLocation class</span></span>

<span data-ttu-id="fb581-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ MemoryDeviceLocation Win32** fait référence à un périphérique de mémoire et à la mémoire physique sur laquelle il existe.</span><span class="sxs-lookup"><span data-stu-id="fb581-104">The **Win32\_MemoryDeviceLocation** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a memory device and the physical memory on which it exists.</span></span>

<span data-ttu-id="fb581-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fb581-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="fb581-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="fb581-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb581-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb581-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_MemoryDeviceLocation : CIM_Realizes
{
  Win32_MemoryDevice   REF Dependent;
  Win32_PhysicalMemory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="fb581-108">Membres</span><span class="sxs-lookup"><span data-stu-id="fb581-108">Members</span></span>

<span data-ttu-id="fb581-109">La classe **Win32 \_ MemoryDeviceLocation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fb581-109">The **Win32\_MemoryDeviceLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="fb581-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fb581-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fb581-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fb581-111">Properties</span></span>

<span data-ttu-id="fb581-112">La classe **Win32 \_ MemoryDeviceLocation** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fb581-112">The **Win32\_MemoryDeviceLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fb581-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="fb581-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb581-114">Type de données : **Win32 \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="fb581-114">Data type: **Win32\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="fb581-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb581-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb581-116">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ PhysicalMemory")</span><span class="sxs-lookup"><span data-stu-id="fb581-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_PhysicalMemory")</span></span>
</dt> </dl>

<span data-ttu-id="fb581-117">[**\_ PhysicalMemory Win32**](win32-physicalmemory.md) qui représente la mémoire physique qui contient le périphérique de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fb581-117">A [**Win32\_PhysicalMemory**](win32-physicalmemory.md) that represents the physical memory containing the memory device.</span></span>

</dd> <dt>

<span data-ttu-id="fb581-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="fb581-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb581-119">Type de données : **Win32 \_ MemoryDevice**</span><span class="sxs-lookup"><span data-stu-id="fb581-119">Data type: **Win32\_MemoryDevice**</span></span>
</dt> <dt>

<span data-ttu-id="fb581-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb581-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb581-121">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI \| Win32 \_ MemoryDevice »)</span><span class="sxs-lookup"><span data-stu-id="fb581-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryDevice")</span></span>
</dt> </dl>

<span data-ttu-id="fb581-122">**\_ MemoryDeviceLocation Win32** qui représente le périphérique de mémoire existant dans la mémoire physique.</span><span class="sxs-lookup"><span data-stu-id="fb581-122">A **Win32\_MemoryDeviceLocation** that represents the memory device existing in the physical memory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb581-123">Notes</span><span class="sxs-lookup"><span data-stu-id="fb581-123">Remarks</span></span>

<span data-ttu-id="fb581-124">La classe **Win32 \_ MemoryDeviceLocation** est dérivée de l' [**\_ esprit CIM**](cim-realizes.md).</span><span class="sxs-lookup"><span data-stu-id="fb581-124">The **Win32\_MemoryDeviceLocation** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb581-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb581-125">Requirements</span></span>



| <span data-ttu-id="fb581-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb581-126">Requirement</span></span> | <span data-ttu-id="fb581-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb581-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb581-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb581-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fb581-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb581-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fb581-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb581-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fb581-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb581-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fb581-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fb581-132">Namespace</span></span><br/>                | <span data-ttu-id="fb581-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="fb581-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fb581-134">MOF</span><span class="sxs-lookup"><span data-stu-id="fb581-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb581-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb581-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb581-136">DLL</span><span class="sxs-lookup"><span data-stu-id="fb581-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb581-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb581-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb581-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb581-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb581-139">**CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fb581-139">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> <dt>

[<span data-ttu-id="fb581-140">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="fb581-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

