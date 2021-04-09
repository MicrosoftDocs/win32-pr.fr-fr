---
description: La \_ classe WMI de l’Association SystemPartitions Win32 associe un système informatique et une partition de disque sur ce système.
ms.assetid: e8f02cd0-9446-4258-b476-5dc6c72c80d4
ms.tgt_platform: multiple
title: Classe Win32_SystemPartitions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemPartitions
- Win32_SystemPartitions.GroupComponent
- Win32_SystemPartitions.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: deae8129772e5d854f05b5b953ec66a12bd5bcaf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861162"
---
# <a name="win32_systempartitions-class"></a><span data-ttu-id="c89e6-103">\_Classe SystemPartitions Win32</span><span class="sxs-lookup"><span data-stu-id="c89e6-103">Win32\_SystemPartitions class</span></span>

<span data-ttu-id="c89e6-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ SystemPartitions Win32** associe un système informatique et une partition de disque sur ce système.</span><span class="sxs-lookup"><span data-stu-id="c89e6-104">The **Win32\_SystemPartitions** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a disk partition on that system.</span></span>

<span data-ttu-id="c89e6-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c89e6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c89e6-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="c89e6-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c89e6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c89e6-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemPartitions : Win32_SystemDevices
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_DiskPartition  REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="c89e6-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c89e6-108">Members</span></span>

<span data-ttu-id="c89e6-109">La classe **Win32 \_ SystemPartitions** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c89e6-109">The **Win32\_SystemPartitions** class has these types of members:</span></span>

-   [<span data-ttu-id="c89e6-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c89e6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c89e6-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c89e6-111">Properties</span></span>

<span data-ttu-id="c89e6-112">La classe **Win32 \_ SystemPartitions** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c89e6-112">The **Win32\_SystemPartitions** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c89e6-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="c89e6-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c89e6-114">Type de données : **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="c89e6-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="c89e6-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c89e6-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c89e6-116">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="c89e6-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="c89e6-117">Référence à l’instance représentant les propriétés du système de l’ordinateur où se trouve la partition de disque.</span><span class="sxs-lookup"><span data-stu-id="c89e6-117">Reference to the instance representing the properties of the computer system where the disk partition is located.</span></span>

</dd> <dt>

<span data-ttu-id="c89e6-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="c89e6-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c89e6-119">Type de données : **Win32 \_ DiskPartition**</span><span class="sxs-lookup"><span data-stu-id="c89e6-119">Data type: **Win32\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="c89e6-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c89e6-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c89e6-121">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ DiskPartition")</span><span class="sxs-lookup"><span data-stu-id="c89e6-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_DiskPartition")</span></span>
</dt> </dl>

<span data-ttu-id="c89e6-122">Référence à l’instance de qui représente les propriétés d’une partition de disque qui existe sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="c89e6-122">Reference to the instance representing the properties of a disk partition that exists on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c89e6-123">Notes</span><span class="sxs-lookup"><span data-stu-id="c89e6-123">Remarks</span></span>

<span data-ttu-id="c89e6-124">La classe **Win32 \_ SystemPartitions** est dérivée de [**Win32 \_ SystemDevices**](win32-systemdevices.md).</span><span class="sxs-lookup"><span data-stu-id="c89e6-124">The **Win32\_SystemPartitions** class is derived from [**Win32\_SystemDevices**](win32-systemdevices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c89e6-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c89e6-125">Requirements</span></span>



| <span data-ttu-id="c89e6-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c89e6-126">Requirement</span></span> | <span data-ttu-id="c89e6-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="c89e6-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c89e6-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c89e6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c89e6-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c89e6-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c89e6-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c89e6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c89e6-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c89e6-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c89e6-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c89e6-132">Namespace</span></span><br/>                | <span data-ttu-id="c89e6-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="c89e6-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c89e6-134">MOF</span><span class="sxs-lookup"><span data-stu-id="c89e6-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c89e6-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c89e6-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c89e6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c89e6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c89e6-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c89e6-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c89e6-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c89e6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c89e6-139">**\_SystemDevices Win32**</span><span class="sxs-lookup"><span data-stu-id="c89e6-139">**Win32\_SystemDevices**</span></span>](win32-systemdevices.md)
</dt> <dt>

[<span data-ttu-id="c89e6-140">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="c89e6-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
