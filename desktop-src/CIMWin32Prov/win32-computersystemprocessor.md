---
description: La \_ classe WMI de l’Association ComputerSystemProcessor Win32 associe un système informatique et un processeur s’exécutant sur ce système.
ms.assetid: e630ebea-19bf-43c7-a8a0-7acfda3a752b
ms.tgt_platform: multiple
title: Classe Win32_ComputerSystemProcessor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystemProcessor
- Win32_ComputerSystemProcessor.PartComponent
- Win32_ComputerSystemProcessor.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2f836d8f5e9053029763c38d2c4f2116987b08fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110347"
---
# <a name="win32_computersystemprocessor-class"></a><span data-ttu-id="38e34-103">\_Classe ComputerSystemProcessor Win32</span><span class="sxs-lookup"><span data-stu-id="38e34-103">Win32\_ComputerSystemProcessor class</span></span>

<span data-ttu-id="38e34-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ ComputerSystemProcessor Win32** associe un système informatique et un processeur s’exécutant sur ce système.</span><span class="sxs-lookup"><span data-stu-id="38e34-104">The **Win32\_ComputerSystemProcessor** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a computer system and a processor running on that system.</span></span>

<span data-ttu-id="38e34-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="38e34-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="38e34-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="38e34-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="38e34-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38e34-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{719A6839-C124-11d2-85E8-0000F8102E5F}"), AMENDMENT]
class Win32_ComputerSystemProcessor : Win32_SystemDevices
{
  Win32_Processor      REF PartComponent;
  Win32_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="38e34-108">Membres</span><span class="sxs-lookup"><span data-stu-id="38e34-108">Members</span></span>

<span data-ttu-id="38e34-109">La classe **Win32 \_ ComputerSystemProcessor** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="38e34-109">The **Win32\_ComputerSystemProcessor** class has these types of members:</span></span>

-   [<span data-ttu-id="38e34-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="38e34-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38e34-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="38e34-111">Properties</span></span>

<span data-ttu-id="38e34-112">La classe **Win32 \_ ComputerSystemProcessor** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="38e34-112">The **Win32\_ComputerSystemProcessor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38e34-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="38e34-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38e34-114">Type de données : **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="38e34-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="38e34-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="38e34-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38e34-116">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="38e34-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="38e34-117">Un **\_ ComputerSystem Win32** qui décrit les propriétés du système informatique sur lequel le processeur s’exécute.</span><span class="sxs-lookup"><span data-stu-id="38e34-117">A **Win32\_ComputerSystem** that describes the properties of the computer system on which the processor is running.</span></span>

</dd> <dt>

<span data-ttu-id="38e34-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="38e34-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38e34-119">Type de données **: \_ processeur Win32**</span><span class="sxs-lookup"><span data-stu-id="38e34-119">Data type: **Win32\_Processor**</span></span>
</dt> <dt>

<span data-ttu-id="38e34-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="38e34-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38e34-121">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("processeur WMI \| Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="38e34-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Processor")</span></span>
</dt> </dl>

<span data-ttu-id="38e34-122">[**\_ Processeur Win32**](win32-processor.md) qui décrit les propriétés d’un processeur qui exécute le système informatique.</span><span class="sxs-lookup"><span data-stu-id="38e34-122">A [**Win32\_Processor**](win32-processor.md) that describes the properties of a processor which is running the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38e34-123">Notes</span><span class="sxs-lookup"><span data-stu-id="38e34-123">Remarks</span></span>

<span data-ttu-id="38e34-124">La classe **Win32 \_ ComputerSystemProcessor** est dérivée de [**Win32 \_ SystemDevices**](win32-systemdevices.md).</span><span class="sxs-lookup"><span data-stu-id="38e34-124">The **Win32\_ComputerSystemProcessor** class is derived from [**Win32\_SystemDevices**](win32-systemdevices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="38e34-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38e34-125">Requirements</span></span>



| <span data-ttu-id="38e34-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38e34-126">Requirement</span></span> | <span data-ttu-id="38e34-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="38e34-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38e34-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38e34-128">Minimum supported client</span></span><br/> | <span data-ttu-id="38e34-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38e34-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="38e34-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38e34-130">Minimum supported server</span></span><br/> | <span data-ttu-id="38e34-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38e34-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="38e34-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="38e34-132">Namespace</span></span><br/>                | <span data-ttu-id="38e34-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="38e34-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="38e34-134">MOF</span><span class="sxs-lookup"><span data-stu-id="38e34-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38e34-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38e34-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="38e34-136">DLL</span><span class="sxs-lookup"><span data-stu-id="38e34-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38e34-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38e34-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38e34-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38e34-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38e34-139">**\_SystemDevices Win32**</span><span class="sxs-lookup"><span data-stu-id="38e34-139">**Win32\_SystemDevices**</span></span>](win32-systemdevices.md)
</dt> <dt>

<span data-ttu-id="38e34-140">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38e34-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

