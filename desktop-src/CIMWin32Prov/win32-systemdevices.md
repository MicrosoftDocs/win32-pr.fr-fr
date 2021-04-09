---
description: La \_ classe WMI de l’Association SystemDevices Win32 associe un système informatique et un périphérique logique installés sur ce système.
ms.assetid: 84dfcb75-3b44-4b27-8eee-779be522eb1f
ms.tgt_platform: multiple
title: Classe Win32_SystemDevices
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDevices
- Win32_SystemDevices.GroupComponent
- Win32_SystemDevices.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b2b28c11e10318e3bca562baf93bc20df9b756cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861573"
---
# <a name="win32_systemdevices-class"></a><span data-ttu-id="3c33f-103">\_Classe SystemDevices Win32</span><span class="sxs-lookup"><span data-stu-id="3c33f-103">Win32\_SystemDevices class</span></span>

<span data-ttu-id="3c33f-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ SystemDevices Win32** associe un système informatique et un périphérique logique installés sur ce système.</span><span class="sxs-lookup"><span data-stu-id="3c33f-104">The **Win32\_SystemDevices** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a logical device installed on that system.</span></span>

<span data-ttu-id="3c33f-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3c33f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3c33f-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="3c33f-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c33f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c33f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F4-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDevices : CIM_SystemDevice
{
  Win32_ComputerSystem REF GroupComponent;
  CIM_LogicalDevice    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="3c33f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="3c33f-108">Members</span></span>

<span data-ttu-id="3c33f-109">La classe **Win32 \_ SystemDevices** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3c33f-109">The **Win32\_SystemDevices** class has these types of members:</span></span>

-   [<span data-ttu-id="3c33f-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3c33f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3c33f-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3c33f-111">Properties</span></span>

<span data-ttu-id="3c33f-112">La classe **Win32 \_ SystemDevices** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="3c33f-112">The **Win32\_SystemDevices** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3c33f-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="3c33f-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c33f-114">Type de données : **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="3c33f-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="3c33f-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c33f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c33f-116">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**substitution**](../wmisdk/standard-qualifiers.md) (« GroupComponent »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI \| Win32 \_ ComputerSystem »)</span><span class="sxs-lookup"><span data-stu-id="3c33f-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="3c33f-117">Référence à l’instance de qui représente les propriétés du système informatique sur lequel se trouve le périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="3c33f-117">Reference to the instance representing the properties of the computer system where the logical device exists.</span></span>

</dd> <dt>

<span data-ttu-id="3c33f-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="3c33f-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c33f-119">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="3c33f-119">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="3c33f-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c33f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c33f-121">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) (« PartComponent »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« CIM \| CIM \_ LogicalDevice »)</span><span class="sxs-lookup"><span data-stu-id="3c33f-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="3c33f-122">Référence à l’instance de qui représente les propriétés d’un périphérique logique qui existe sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="3c33f-122">Reference to the instance representing the properties of a logical device that exists on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c33f-123">Notes</span><span class="sxs-lookup"><span data-stu-id="3c33f-123">Remarks</span></span>

<span data-ttu-id="3c33f-124">La classe **Win32 \_ SystemDevices** est dérivée de [**CIM \_ SystemDevice**](cim-systemdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3c33f-124">The **Win32\_SystemDevices** class is derived from [**CIM\_SystemDevice**](cim-systemdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c33f-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c33f-125">Requirements</span></span>



| <span data-ttu-id="3c33f-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c33f-126">Requirement</span></span> | <span data-ttu-id="3c33f-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c33f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c33f-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c33f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3c33f-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c33f-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3c33f-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c33f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3c33f-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c33f-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3c33f-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3c33f-132">Namespace</span></span><br/>                | <span data-ttu-id="3c33f-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="3c33f-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3c33f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="3c33f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c33f-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c33f-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c33f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3c33f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c33f-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c33f-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c33f-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c33f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c33f-139">**\_SYSTEMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3c33f-139">**CIM\_SystemDevice**</span></span>](cim-systemdevice.md)
</dt> <dt>

[<span data-ttu-id="3c33f-140">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="3c33f-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
