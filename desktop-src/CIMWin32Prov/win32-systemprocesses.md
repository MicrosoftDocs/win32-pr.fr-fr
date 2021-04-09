---
description: La \_ classe WMI de l’Association SystemProcesses Win32 associe un système informatique et un processus s’exécutant sur ce système.
ms.assetid: 0d8c3ec6-265e-4486-8e94-f5acd2845cf5
ms.tgt_platform: multiple
title: Classe Win32_SystemProcesses
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemProcesses
- Win32_SystemProcesses.GroupComponent
- Win32_SystemProcesses.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1b963aea5d9c651e27dc4380200e40dd3dcb9a77
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033691"
---
# <a name="win32_systemprocesses-class"></a><span data-ttu-id="1d04c-103">\_Classe SystemProcesses Win32</span><span class="sxs-lookup"><span data-stu-id="1d04c-103">Win32\_SystemProcesses class</span></span>

<span data-ttu-id="1d04c-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ SystemProcesses Win32** associe un système informatique et un processus s’exécutant sur ce système.</span><span class="sxs-lookup"><span data-stu-id="1d04c-104">The **Win32\_SystemProcesses** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a process running on that system.</span></span>

<span data-ttu-id="1d04c-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="1d04c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1d04c-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="1d04c-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d04c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d04c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemProcesses : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_Process        REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="1d04c-108">Membres</span><span class="sxs-lookup"><span data-stu-id="1d04c-108">Members</span></span>

<span data-ttu-id="1d04c-109">La classe **Win32 \_ SystemProcesses** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1d04c-109">The **Win32\_SystemProcesses** class has these types of members:</span></span>

-   [<span data-ttu-id="1d04c-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1d04c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1d04c-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1d04c-111">Properties</span></span>

<span data-ttu-id="1d04c-112">La classe **Win32 \_ SystemProcesses** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="1d04c-112">The **Win32\_SystemProcesses** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d04c-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="1d04c-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d04c-114">Type de données : **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="1d04c-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="1d04c-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d04c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d04c-116">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**substitution**](../wmisdk/standard-qualifiers.md) (« GroupComponent »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI \| Win32 \_ ComputerSystem »)</span><span class="sxs-lookup"><span data-stu-id="1d04c-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="1d04c-117">Référence à l’instance de qui représente le système informatique sur lequel le processus s’exécute.</span><span class="sxs-lookup"><span data-stu-id="1d04c-117">Reference to the instance representing the computer system upon which the process is running.</span></span>

</dd> <dt>

<span data-ttu-id="1d04c-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="1d04c-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d04c-119">Type de données **: \_ processus Win32**</span><span class="sxs-lookup"><span data-stu-id="1d04c-119">Data type: **Win32\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="1d04c-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d04c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d04c-121">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("processus WMI \| Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="1d04c-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Process")</span></span>
</dt> </dl>

<span data-ttu-id="1d04c-122">Référence à l’instance de qui représente le processus en cours d’exécution sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="1d04c-122">Reference to the instance representing the process running on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d04c-123">Notes</span><span class="sxs-lookup"><span data-stu-id="1d04c-123">Remarks</span></span>

<span data-ttu-id="1d04c-124">La classe **Win32 \_ SystemProcesses** est dérivée de [**CIM \_ SystemComponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="1d04c-124">The **Win32\_SystemProcesses** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d04c-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d04c-125">Requirements</span></span>



| <span data-ttu-id="1d04c-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d04c-126">Requirement</span></span> | <span data-ttu-id="1d04c-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d04c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d04c-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d04c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1d04c-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d04c-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1d04c-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d04c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1d04c-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d04c-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1d04c-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1d04c-132">Namespace</span></span><br/>                | <span data-ttu-id="1d04c-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="1d04c-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1d04c-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1d04c-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d04c-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d04c-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d04c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1d04c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d04c-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d04c-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d04c-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d04c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d04c-139">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="1d04c-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="1d04c-140">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="1d04c-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
