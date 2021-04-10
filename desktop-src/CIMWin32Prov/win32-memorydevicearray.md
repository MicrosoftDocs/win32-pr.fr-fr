---
description: La \_ classe WMI de l’Association MemoryDeviceArray Win32 associe un périphérique de mémoire et le tableau de mémoire dans lequel il réside.
ms.assetid: 39ea6333-2352-488b-99e4-97594bea7dcd
ms.tgt_platform: multiple
title: Classe Win32_MemoryDeviceArray
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryDeviceArray
- Win32_MemoryDeviceArray.GroupComponent
- Win32_MemoryDeviceArray.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1e527f77183c3bdc09d464f6fed4808e45adefa5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860697"
---
# <a name="win32_memorydevicearray-class"></a><span data-ttu-id="327de-103">\_Classe MemoryDeviceArray Win32</span><span class="sxs-lookup"><span data-stu-id="327de-103">Win32\_MemoryDeviceArray class</span></span>

<span data-ttu-id="327de-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ MemoryDeviceArray Win32** associe un périphérique de mémoire et le tableau de mémoire dans lequel il réside.</span><span class="sxs-lookup"><span data-stu-id="327de-104">The **Win32\_MemoryDeviceArray** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a memory device and the memory array in which it resides.</span></span>

<span data-ttu-id="327de-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="327de-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="327de-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="327de-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="327de-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="327de-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF563-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_MemoryDeviceArray : CIM_Component
{
  Win32_MemoryArray  REF GroupComponent;
  Win32_MemoryDevice REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="327de-108">Membres</span><span class="sxs-lookup"><span data-stu-id="327de-108">Members</span></span>

<span data-ttu-id="327de-109">La classe **Win32 \_ MemoryDeviceArray** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="327de-109">The **Win32\_MemoryDeviceArray** class has these types of members:</span></span>

-   [<span data-ttu-id="327de-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="327de-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="327de-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="327de-111">Properties</span></span>

<span data-ttu-id="327de-112">La classe **Win32 \_ MemoryDeviceArray** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="327de-112">The **Win32\_MemoryDeviceArray** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="327de-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="327de-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327de-114">Type de données : **Win32 \_ MemoryArray**</span><span class="sxs-lookup"><span data-stu-id="327de-114">Data type: **Win32\_MemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="327de-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="327de-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="327de-116">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryArray")</span><span class="sxs-lookup"><span data-stu-id="327de-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="327de-117">[**\_ MemoryArray Win32**](win32-memoryarray.md) qui représente la partie du tableau de mémoire de l' \_ Association Win32 MemoryDeviceArray.</span><span class="sxs-lookup"><span data-stu-id="327de-117">A [**Win32\_MemoryArray**](win32-memoryarray.md) that represents the memory array part of the Win32\_MemoryDeviceArray association.</span></span>

</dd> <dt>

<span data-ttu-id="327de-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="327de-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327de-119">Type de données : **Win32 \_ MemoryDevice**</span><span class="sxs-lookup"><span data-stu-id="327de-119">Data type: **Win32\_MemoryDevice**</span></span>
</dt> <dt>

<span data-ttu-id="327de-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="327de-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="327de-121">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryDevice")</span><span class="sxs-lookup"><span data-stu-id="327de-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryDevice")</span></span>
</dt> </dl>

<span data-ttu-id="327de-122">[**\_ MemoryDevice Win32**](win32-memorydevice.md) qui représente une partie de l’appareil mémoire de l' \_ Association Win32 MemoryDeviceArray.</span><span class="sxs-lookup"><span data-stu-id="327de-122">A [**Win32\_MemoryDevice**](win32-memorydevice.md) that represents a memory device part of the Win32\_MemoryDeviceArray association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="327de-123">Notes</span><span class="sxs-lookup"><span data-stu-id="327de-123">Remarks</span></span>

<span data-ttu-id="327de-124">La classe **Win32 \_ MemoryDeviceArray** est dérivée [**du \_ composant CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="327de-124">The **Win32\_MemoryDeviceArray** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="327de-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="327de-125">Requirements</span></span>



| <span data-ttu-id="327de-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="327de-126">Requirement</span></span> | <span data-ttu-id="327de-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="327de-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="327de-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="327de-128">Minimum supported client</span></span><br/> | <span data-ttu-id="327de-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="327de-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="327de-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="327de-130">Minimum supported server</span></span><br/> | <span data-ttu-id="327de-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="327de-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="327de-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="327de-132">Namespace</span></span><br/>                | <span data-ttu-id="327de-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="327de-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="327de-134">MOF</span><span class="sxs-lookup"><span data-stu-id="327de-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="327de-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="327de-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="327de-136">DLL</span><span class="sxs-lookup"><span data-stu-id="327de-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="327de-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="327de-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="327de-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="327de-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="327de-139">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="327de-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="327de-140">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="327de-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

