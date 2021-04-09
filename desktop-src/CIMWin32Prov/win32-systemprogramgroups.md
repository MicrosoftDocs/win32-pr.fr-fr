---
description: La \_ classe WMI de l’Association SystemProgramGroups Win32 associe un système informatique et un groupe de programmes logique.
ms.assetid: cbf810c8-a967-4d60-889c-e47c43b039ea
ms.tgt_platform: multiple
title: Classe Win32_SystemProgramGroups
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemProgramGroups
- Win32_SystemProgramGroups.Element
- Win32_SystemProgramGroups.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1a8ca556c24295e2c4b04ab851610ef35ec9b715
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111479"
---
# <a name="win32_systemprogramgroups-class"></a><span data-ttu-id="33f41-103">\_Classe SystemProgramGroups Win32</span><span class="sxs-lookup"><span data-stu-id="33f41-103">Win32\_SystemProgramGroups class</span></span>

<span data-ttu-id="33f41-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ SystemProgramGroups Win32** associe un système informatique et un groupe de programmes logique.</span><span class="sxs-lookup"><span data-stu-id="33f41-104">The **Win32\_SystemProgramGroups** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a logical program group.</span></span>

<span data-ttu-id="33f41-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="33f41-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="33f41-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="33f41-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="33f41-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33f41-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C505-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemProgramGroups : Win32_SystemSetting
{
  Win32_ComputerSystem      REF Element;
  Win32_LogicalProgramGroup REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="33f41-108">Membres</span><span class="sxs-lookup"><span data-stu-id="33f41-108">Members</span></span>

<span data-ttu-id="33f41-109">La classe **Win32 \_ SystemProgramGroups** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="33f41-109">The **Win32\_SystemProgramGroups** class has these types of members:</span></span>

-   [<span data-ttu-id="33f41-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="33f41-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="33f41-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="33f41-111">Properties</span></span>

<span data-ttu-id="33f41-112">La classe **Win32 \_ SystemProgramGroups** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="33f41-112">The **Win32\_SystemProgramGroups** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="33f41-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="33f41-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f41-114">Type de données : **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="33f41-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="33f41-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="33f41-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33f41-116">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="33f41-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="33f41-117">Référence à l’instance de qui représente le système informatique contenant le groupe de programmes logique.</span><span class="sxs-lookup"><span data-stu-id="33f41-117">Reference to the instance representing the computer system containing the logical program group.</span></span>

</dd> <dt>

<span data-ttu-id="33f41-118">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="33f41-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f41-119">Type de données : **Win32 \_ LogicalProgramGroup**</span><span class="sxs-lookup"><span data-stu-id="33f41-119">Data type: **Win32\_LogicalProgramGroup**</span></span>
</dt> <dt>

<span data-ttu-id="33f41-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="33f41-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33f41-121">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ LogicalProgramGroup")</span><span class="sxs-lookup"><span data-stu-id="33f41-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_LogicalProgramGroup")</span></span>
</dt> </dl>

<span data-ttu-id="33f41-122">Référence à l’instance de qui représente le groupe de programmes logique sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="33f41-122">Reference to the instance representing the logical program group on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33f41-123">Notes</span><span class="sxs-lookup"><span data-stu-id="33f41-123">Remarks</span></span>

<span data-ttu-id="33f41-124">La classe **Win32 \_ SystemProgramGroups** est dérivée de [**Win32 \_ SystemSetting**](win32-systemsetting.md).</span><span class="sxs-lookup"><span data-stu-id="33f41-124">The **Win32\_SystemProgramGroups** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="33f41-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33f41-125">Requirements</span></span>



| <span data-ttu-id="33f41-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33f41-126">Requirement</span></span> | <span data-ttu-id="33f41-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="33f41-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33f41-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33f41-128">Minimum supported client</span></span><br/> | <span data-ttu-id="33f41-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33f41-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="33f41-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33f41-130">Minimum supported server</span></span><br/> | <span data-ttu-id="33f41-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33f41-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="33f41-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="33f41-132">Namespace</span></span><br/>                | <span data-ttu-id="33f41-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="33f41-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="33f41-134">MOF</span><span class="sxs-lookup"><span data-stu-id="33f41-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33f41-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33f41-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="33f41-136">DLL</span><span class="sxs-lookup"><span data-stu-id="33f41-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33f41-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33f41-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33f41-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33f41-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33f41-139">**\_SystemSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="33f41-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="33f41-140">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="33f41-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
