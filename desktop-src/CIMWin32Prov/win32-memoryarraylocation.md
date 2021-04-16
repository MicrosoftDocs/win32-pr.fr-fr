---
description: La \_ classe WMI de l’Association MemoryArrayLocation Win32 associe un tableau de mémoire logique et le tableau de mémoire physique sur lequel il existe.
ms.assetid: 455daeee-ad67-4599-84d6-fa3f4ac593aa
ms.tgt_platform: multiple
title: Classe Win32_MemoryArrayLocation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryArrayLocation
- Win32_MemoryArrayLocation.Dependent
- Win32_MemoryArrayLocation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 62aae3bf672b12bdb947ff8ce6b76f919eaa11b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524103"
---
# <a name="win32_memoryarraylocation-class"></a><span data-ttu-id="24992-103">\_Classe MemoryArrayLocation Win32</span><span class="sxs-lookup"><span data-stu-id="24992-103">Win32\_MemoryArrayLocation class</span></span>

<span data-ttu-id="24992-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ MemoryArrayLocation Win32** associe un tableau de mémoire logique et le tableau de mémoire physique sur lequel il existe.</span><span class="sxs-lookup"><span data-stu-id="24992-104">The **Win32\_MemoryArrayLocation** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical memory array and the physical memory array on which it exists.</span></span>

<span data-ttu-id="24992-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="24992-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="24992-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="24992-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="24992-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24992-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF561-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_MemoryArrayLocation : CIM_Realizes
{
  Win32_MemoryArray         REF Dependent;
  Win32_PhysicalMemoryArray REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="24992-108">Membres</span><span class="sxs-lookup"><span data-stu-id="24992-108">Members</span></span>

<span data-ttu-id="24992-109">La classe **Win32 \_ MemoryArrayLocation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="24992-109">The **Win32\_MemoryArrayLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="24992-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="24992-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="24992-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="24992-111">Properties</span></span>

<span data-ttu-id="24992-112">La classe **Win32 \_ MemoryArrayLocation** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="24992-112">The **Win32\_MemoryArrayLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="24992-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="24992-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24992-114">Type de données : **Win32 \_ PhysicalMemoryArray**</span><span class="sxs-lookup"><span data-stu-id="24992-114">Data type: **Win32\_PhysicalMemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="24992-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="24992-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24992-116">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ PhysicalMemoryArray")</span><span class="sxs-lookup"><span data-stu-id="24992-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_PhysicalMemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="24992-117">[**\_ PhysicalMemoryArray Win32**](win32-physicalmemoryarray.md) qui décrit le tableau de mémoire physique qui implémente le tableau de mémoire logique.</span><span class="sxs-lookup"><span data-stu-id="24992-117">A [**Win32\_PhysicalMemoryArray**](win32-physicalmemoryarray.md) that describes the physical memory array that implements the logical memory array.</span></span>

</dd> <dt>

<span data-ttu-id="24992-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="24992-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24992-119">Type de données : **Win32 \_ MemoryArray**</span><span class="sxs-lookup"><span data-stu-id="24992-119">Data type: **Win32\_MemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="24992-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="24992-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24992-121">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI \| Win32 \_ MemoryArray »)</span><span class="sxs-lookup"><span data-stu-id="24992-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="24992-122">[**\_ MemoryArray Win32**](win32-memoryarray.md) qui décrit le tableau de mémoire logique implémenté par le tableau de mémoire physique.</span><span class="sxs-lookup"><span data-stu-id="24992-122">A [**Win32\_MemoryArray**](win32-memoryarray.md) that describes the logical memory array implemented by the physical memory array.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="24992-123">Notes</span><span class="sxs-lookup"><span data-stu-id="24992-123">Remarks</span></span>

<span data-ttu-id="24992-124">La classe **Win32 \_ MemoryArrayLocation** est dérivée de l' [**\_ esprit CIM**](cim-realizes.md).</span><span class="sxs-lookup"><span data-stu-id="24992-124">The **Win32\_MemoryArrayLocation** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="24992-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24992-125">Requirements</span></span>



| <span data-ttu-id="24992-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24992-126">Requirement</span></span> | <span data-ttu-id="24992-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="24992-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24992-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24992-128">Minimum supported client</span></span><br/> | <span data-ttu-id="24992-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="24992-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="24992-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24992-130">Minimum supported server</span></span><br/> | <span data-ttu-id="24992-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24992-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="24992-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="24992-132">Namespace</span></span><br/>                | <span data-ttu-id="24992-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="24992-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="24992-134">MOF</span><span class="sxs-lookup"><span data-stu-id="24992-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24992-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="24992-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="24992-136">DLL</span><span class="sxs-lookup"><span data-stu-id="24992-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24992-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24992-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24992-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24992-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24992-139">**CIM \_**</span><span class="sxs-lookup"><span data-stu-id="24992-139">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> <dt>

[<span data-ttu-id="24992-140">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="24992-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

