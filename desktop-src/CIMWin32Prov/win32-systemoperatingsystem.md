---
description: La \_ classe WMI de l’Association SystemOperatingSystem Win32 associe un système informatique et son système d’exploitation.
ms.assetid: dc71f80b-6fbd-4bc8-8783-3922d8050518
ms.tgt_platform: multiple
title: Classe Win32_SystemOperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemOperatingSystem
- Win32_SystemOperatingSystem.PrimaryOS
- Win32_SystemOperatingSystem.GroupComponent
- Win32_SystemOperatingSystem.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ba3f8ac94ec882ee1df96da51d93d2c24fde9b3f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111494"
---
# <a name="win32_systemoperatingsystem-class"></a><span data-ttu-id="759f3-103">\_Classe SystemOperatingSystem Win32</span><span class="sxs-lookup"><span data-stu-id="759f3-103">Win32\_SystemOperatingSystem class</span></span>

<span data-ttu-id="759f3-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ SystemOperatingSystem Win32** associe un système informatique et son système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="759f3-104">The **Win32\_SystemOperatingSystem** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and its operating system.</span></span>

<span data-ttu-id="759f3-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="759f3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="759f3-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="759f3-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="759f3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="759f3-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemOperatingSystem : CIM_InstalledOS
{
  boolean                   PrimaryOS;
  Win32_ComputerSystem  REF GroupComponent;
  Win32_OperatingSystem REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="759f3-108">Membres</span><span class="sxs-lookup"><span data-stu-id="759f3-108">Members</span></span>

<span data-ttu-id="759f3-109">La classe **Win32 \_ SystemOperatingSystem** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="759f3-109">The **Win32\_SystemOperatingSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="759f3-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="759f3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="759f3-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="759f3-111">Properties</span></span>

<span data-ttu-id="759f3-112">La classe **Win32 \_ SystemOperatingSystem** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="759f3-112">The **Win32\_SystemOperatingSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="759f3-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="759f3-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759f3-114">Type de données : **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="759f3-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="759f3-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="759f3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759f3-116">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**substitution**](../wmisdk/standard-qualifiers.md) (« GroupComponent »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI \| Win32 \_ ComputerSystem »)</span><span class="sxs-lookup"><span data-stu-id="759f3-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="759f3-117">Un [**\_ ComputerSystem Win32**](win32-computersystemprocessor.md) qui décrit les propriétés du système informatique sur lequel le système d’exploitation est installé.</span><span class="sxs-lookup"><span data-stu-id="759f3-117">A [**Win32\_ComputerSystem**](win32-computersystemprocessor.md) that describes the properties of the computer system upon which the operating system is installed.</span></span>

</dd> <dt>

<span data-ttu-id="759f3-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="759f3-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759f3-119">Type de données : **Win32 \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="759f3-119">Data type: **Win32\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="759f3-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="759f3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759f3-121">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ OperatingSystem")</span><span class="sxs-lookup"><span data-stu-id="759f3-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_OperatingSystem")</span></span>
</dt> </dl>

<span data-ttu-id="759f3-122">[**Win32 \_ OperatingSystem**](win32-operatingsystem.md) qui décrit les propriétés du système d’exploitation en cours d’exécution sur ce système informatique.</span><span class="sxs-lookup"><span data-stu-id="759f3-122">A [**Win32\_OperatingSystem**](win32-operatingsystem.md) that describes properties of the operating system running on this computer system.</span></span>

</dd> <dt>

<span data-ttu-id="759f3-123">**Serveur primaire**</span><span class="sxs-lookup"><span data-stu-id="759f3-123">**PrimaryOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759f3-124">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="759f3-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="759f3-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="759f3-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759f3-126">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Système d’exploitation DMTF \| 001,4»)</span><span class="sxs-lookup"><span data-stu-id="759f3-126">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operating System\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="759f3-127">Si la **valeur est true**, le système d’exploitation installé est le système d’exploitation par défaut pour le système informatique.</span><span class="sxs-lookup"><span data-stu-id="759f3-127">If **TRUE**, the installed operating system is the default operating system for the computer system.</span></span>

<span data-ttu-id="759f3-128">Cette propriété est héritée de [**CIM \_ installed**](cim-installedos.md).</span><span class="sxs-lookup"><span data-stu-id="759f3-128">This property is inherited from [**CIM\_InstalledOS**](cim-installedos.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="759f3-129">Notes</span><span class="sxs-lookup"><span data-stu-id="759f3-129">Remarks</span></span>

<span data-ttu-id="759f3-130">La classe **Win32 \_ SystemOperatingSystem** est dérivée de [**CIM \_ installed**](cim-installedos.md).</span><span class="sxs-lookup"><span data-stu-id="759f3-130">The **Win32\_SystemOperatingSystem** class is derived from [**CIM\_InstalledOS**](cim-installedos.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="759f3-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="759f3-131">Requirements</span></span>



| <span data-ttu-id="759f3-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="759f3-132">Requirement</span></span> | <span data-ttu-id="759f3-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="759f3-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="759f3-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="759f3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="759f3-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="759f3-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="759f3-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="759f3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="759f3-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="759f3-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="759f3-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="759f3-138">Namespace</span></span><br/>                | <span data-ttu-id="759f3-139">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="759f3-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="759f3-140">MOF</span><span class="sxs-lookup"><span data-stu-id="759f3-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="759f3-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="759f3-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="759f3-142">DLL</span><span class="sxs-lookup"><span data-stu-id="759f3-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="759f3-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="759f3-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="759f3-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="759f3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="759f3-145">**CIM \_ installé**</span><span class="sxs-lookup"><span data-stu-id="759f3-145">**CIM\_InstalledOS**</span></span>](cim-installedos.md)
</dt> <dt>

[<span data-ttu-id="759f3-146">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="759f3-146">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
