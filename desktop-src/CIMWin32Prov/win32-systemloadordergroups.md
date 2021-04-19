---
description: La \_ classe WMI de l’Association SystemLoadOrderGroups Win32 associe un système informatique et un groupe d’ordre de chargement.
ms.assetid: fb637300-0f70-465a-a72b-f0ab3f246790
ms.tgt_platform: multiple
title: Classe Win32_SystemLoadOrderGroups
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemLoadOrderGroups
- Win32_SystemLoadOrderGroups.GroupComponent
- Win32_SystemLoadOrderGroups.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 510acfbde2f562493a454abe80a4f7788377e556
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538834"
---
# <a name="win32_systemloadordergroups-class"></a><span data-ttu-id="4d262-103">\_Classe SystemLoadOrderGroups Win32</span><span class="sxs-lookup"><span data-stu-id="4d262-103">Win32\_SystemLoadOrderGroups class</span></span>

<span data-ttu-id="4d262-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ SystemLoadOrderGroups Win32** associe un système informatique et un groupe d’ordre de chargement.</span><span class="sxs-lookup"><span data-stu-id="4d262-104">The **Win32\_SystemLoadOrderGroups** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a load order group.</span></span>

<span data-ttu-id="4d262-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4d262-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4d262-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="4d262-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d262-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d262-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C503-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemLoadOrderGroups : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_LoadOrderGroup REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="4d262-108">Membres</span><span class="sxs-lookup"><span data-stu-id="4d262-108">Members</span></span>

<span data-ttu-id="4d262-109">La classe **Win32 \_ SystemLoadOrderGroups** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4d262-109">The **Win32\_SystemLoadOrderGroups** class has these types of members:</span></span>

-   [<span data-ttu-id="4d262-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4d262-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4d262-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4d262-111">Properties</span></span>

<span data-ttu-id="4d262-112">La classe **Win32 \_ SystemLoadOrderGroups** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="4d262-112">The **Win32\_SystemLoadOrderGroups** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4d262-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="4d262-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d262-114">Type de données : **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="4d262-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="4d262-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d262-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d262-116">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**substitution**](../wmisdk/standard-qualifiers.md) (« GroupComponent »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI \| Win32 \_ ComputerSystem »)</span><span class="sxs-lookup"><span data-stu-id="4d262-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="4d262-117">Référence à l’instance représentant le système de l’ordinateur où se trouve le groupe d’ordre de chargement.</span><span class="sxs-lookup"><span data-stu-id="4d262-117">Reference to the instance representing the computer system where the load order group exists.</span></span>

</dd> <dt>

<span data-ttu-id="4d262-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="4d262-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d262-119">Type de données : **Win32 \_ LoadOrderGroup**</span><span class="sxs-lookup"><span data-stu-id="4d262-119">Data type: **Win32\_LoadOrderGroup**</span></span>
</dt> <dt>

<span data-ttu-id="4d262-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d262-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d262-121">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ LoadOrderGroup")</span><span class="sxs-lookup"><span data-stu-id="4d262-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_LoadOrderGroup")</span></span>
</dt> </dl>

<span data-ttu-id="4d262-122">Référence à l’instance de qui représente le groupe d’ordre de chargement existant sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="4d262-122">Reference to the instance representing the load order group existing on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d262-123">Notes</span><span class="sxs-lookup"><span data-stu-id="4d262-123">Remarks</span></span>

<span data-ttu-id="4d262-124">La classe **Win32 \_ SystemLoadOrderGroups** est dérivée de [**CIM \_ SystemComponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="4d262-124">The **Win32\_SystemLoadOrderGroups** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d262-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d262-125">Requirements</span></span>



| <span data-ttu-id="4d262-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d262-126">Requirement</span></span> | <span data-ttu-id="4d262-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d262-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d262-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d262-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4d262-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d262-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4d262-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d262-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4d262-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d262-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4d262-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4d262-132">Namespace</span></span><br/>                | <span data-ttu-id="4d262-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="4d262-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4d262-134">MOF</span><span class="sxs-lookup"><span data-stu-id="4d262-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d262-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d262-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d262-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4d262-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d262-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d262-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d262-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d262-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d262-139">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="4d262-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="4d262-140">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="4d262-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
