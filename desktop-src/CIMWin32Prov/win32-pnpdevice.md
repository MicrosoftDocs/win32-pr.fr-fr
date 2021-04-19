---
description: La \_ classe WMI de l’Association PnPDevice Win32 associe un appareil (connu pour Configuration Manager en tant que PNPEntity) et la fonction qu’il exécute.
ms.assetid: 5163a423-60f2-416d-bf82-89517b499f93
ms.tgt_platform: multiple
title: Classe Win32_PnPDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDevice
- Win32_PnPDevice.SameElement
- Win32_PnPDevice.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c17dc6d4169854469d630e2a622eacc85e8a587c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516589"
---
# <a name="win32_pnpdevice-class"></a><span data-ttu-id="20696-103">\_Classe PnPDevice Win32</span><span class="sxs-lookup"><span data-stu-id="20696-103">Win32\_PnPDevice class</span></span>

<span data-ttu-id="20696-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ PnPDevice Win32** associe un appareil (connu pour Configuration Manager en tant que PNPEntity) et la fonction qu’il exécute.</span><span class="sxs-lookup"><span data-stu-id="20696-104">The **Win32\_PnPDevice** association [WMI class](../wmisdk/retrieving-a-class.md) relates a device (known to Configuration Manager as a PNPEntity) and the function it performs.</span></span> <span data-ttu-id="20696-105">Sa fonction est représentée par une sous-classe de l’appareil logique qui décrit son utilisation.</span><span class="sxs-lookup"><span data-stu-id="20696-105">Its function is represented by a subclass of the logical device that describes its use.</span></span> <span data-ttu-id="20696-106">Par exemple, un [**\_ clavier Win32**](win32-keyboard.md) ou une instance [**Win32 \_ DiskDrive**](win32-diskdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="20696-106">For example, a [**Win32\_Keyboard**](win32-keyboard.md) or [**Win32\_DiskDrive**](win32-diskdrive.md) instance.</span></span> <span data-ttu-id="20696-107">Les deux objets référencés représentent le même périphérique système sous-jacent ; les modifications apportées à l’allocation des ressources côté PNPEntity affecteront l’appareil associé.</span><span class="sxs-lookup"><span data-stu-id="20696-107">Both referenced objects represent the same underlying system device; changes to resource allocation on the PNPEntity side will effect the associated device.</span></span>

<span data-ttu-id="20696-108">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="20696-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="20696-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="20696-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="20696-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20696-110">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{FE28FD96-C875-11d2-B352-00104BC97924}"), AMENDMENT]
class Win32_PnPDevice
{
  CIM_LogicalDevice REF SameElement;
  Win32_PnPEntity   REF SystemElement;
};
```

## <a name="members"></a><span data-ttu-id="20696-111">Membres</span><span class="sxs-lookup"><span data-stu-id="20696-111">Members</span></span>

<span data-ttu-id="20696-112">La classe **Win32 \_ PnPDevice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="20696-112">The **Win32\_PnPDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="20696-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="20696-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="20696-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="20696-114">Properties</span></span>

<span data-ttu-id="20696-115">La classe **Win32 \_ PnPDevice** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="20696-115">The **Win32\_PnPDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="20696-116">**SameElement**</span><span class="sxs-lookup"><span data-stu-id="20696-116">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20696-117">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="20696-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="20696-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="20696-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20696-119">Qualificateurs : [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="20696-119">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="20696-120">Référence à l’instance du [**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui représente les propriétés de l’appareil logique associées à l’appareil plug-and-Play.</span><span class="sxs-lookup"><span data-stu-id="20696-120">Reference to the [**CIM\_LogicalDevice**](cim-logicaldevice.md) instance representing the logical device properties associated with the Plug and Play device.</span></span>

</dd> <dt>

<span data-ttu-id="20696-121">**SYSTEME**</span><span class="sxs-lookup"><span data-stu-id="20696-121">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20696-122">Type de données : **Win32 \_ PnPEntity**</span><span class="sxs-lookup"><span data-stu-id="20696-122">Data type: **Win32\_PnPEntity**</span></span>
</dt> <dt>

<span data-ttu-id="20696-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="20696-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20696-124">Qualificateurs : [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PnPEntity")</span><span class="sxs-lookup"><span data-stu-id="20696-124">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PnPEntity")</span></span>
</dt> </dl>

<span data-ttu-id="20696-125">Référence à l’instance [**Win32 \_ PnPEntity**](win32-pnpentity.md) qui représente l’appareil plug-and-Play associé à l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="20696-125">Reference to the [**Win32\_PnPEntity**](win32-pnpentity.md) instance representing the Plug and Play device associated with the logical device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="20696-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20696-126">Requirements</span></span>



| <span data-ttu-id="20696-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20696-127">Requirement</span></span> | <span data-ttu-id="20696-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="20696-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20696-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20696-129">Minimum supported client</span></span><br/> | <span data-ttu-id="20696-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20696-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="20696-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20696-131">Minimum supported server</span></span><br/> | <span data-ttu-id="20696-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20696-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="20696-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="20696-133">Namespace</span></span><br/>                | <span data-ttu-id="20696-134">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="20696-134">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="20696-135">MOF</span><span class="sxs-lookup"><span data-stu-id="20696-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20696-136"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20696-136"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="20696-137">DLL</span><span class="sxs-lookup"><span data-stu-id="20696-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20696-138"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20696-138"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20696-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20696-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20696-140">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="20696-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
