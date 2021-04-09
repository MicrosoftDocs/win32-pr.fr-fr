---
description: La \_ classe WMI de l’Association DeviceBus Win32 associe un bus système et un périphérique logique à l’aide du bus. Cette classe est utilisée pour détecter les appareils sur lesquels le bus est utilisé.
ms.assetid: 2d7d83a5-c058-40c0-aab3-7700f4067a16
ms.tgt_platform: multiple
title: Classe Win32_DeviceBus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceBus
- Win32_DeviceBus.Dependent
- Win32_DeviceBus.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2dde01ee6b3f3be026dbc19f8c4b8e2c238f4ff2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111606"
---
# <a name="win32_devicebus-class"></a><span data-ttu-id="6d481-104">\_Classe DeviceBus Win32</span><span class="sxs-lookup"><span data-stu-id="6d481-104">Win32\_DeviceBus class</span></span>

<span data-ttu-id="6d481-105">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ DeviceBus Win32** associe un bus système et un périphérique logique à l’aide du bus.</span><span class="sxs-lookup"><span data-stu-id="6d481-105">The **Win32\_DeviceBus** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a system bus and a logical device using the bus.</span></span> <span data-ttu-id="6d481-106">Cette classe est utilisée pour détecter les appareils sur lesquels le bus est utilisé.</span><span class="sxs-lookup"><span data-stu-id="6d481-106">This class is used to discover which devices are on which bus.</span></span>

<span data-ttu-id="6d481-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6d481-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6d481-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="6d481-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d481-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d481-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceBus : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  Win32_Bus         REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="6d481-110">Membres</span><span class="sxs-lookup"><span data-stu-id="6d481-110">Members</span></span>

<span data-ttu-id="6d481-111">La classe **Win32 \_ DeviceBus** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6d481-111">The **Win32\_DeviceBus** class has these types of members:</span></span>

-   [<span data-ttu-id="6d481-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6d481-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6d481-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6d481-113">Properties</span></span>

<span data-ttu-id="6d481-114">La classe **Win32 \_ DeviceBus** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6d481-114">The **Win32\_DeviceBus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6d481-115">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="6d481-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d481-116">Type de données **: \_ bus Win32**</span><span class="sxs-lookup"><span data-stu-id="6d481-116">Data type: **Win32\_Bus**</span></span>
</dt> <dt>

<span data-ttu-id="6d481-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6d481-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d481-118">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« Antecedent »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« \| bus Win32 WMI \_ »)</span><span class="sxs-lookup"><span data-stu-id="6d481-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Bus")</span></span>
</dt> </dl>

<span data-ttu-id="6d481-119">[**\_ Bus Win32**](win32-bus.md) qui décrit les propriétés du bus système utilisé par l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="6d481-119">A [**Win32\_Bus**](win32-bus.md) that describes the properties of the system bus that is used by the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="6d481-120">**Charge**</span><span class="sxs-lookup"><span data-stu-id="6d481-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d481-121">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="6d481-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="6d481-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6d481-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d481-123">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« CIM \| CIM \_ LogicalDevice »)</span><span class="sxs-lookup"><span data-stu-id="6d481-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="6d481-124">[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui décrit les propriétés de l’appareil logique qui utilise le bus système.</span><span class="sxs-lookup"><span data-stu-id="6d481-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the properties of the logical device that is using the system bus.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d481-125">Notes</span><span class="sxs-lookup"><span data-stu-id="6d481-125">Remarks</span></span>

<span data-ttu-id="6d481-126">La classe **Win32 \_ DeviceBus** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="6d481-126">The **Win32\_DeviceBus** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d481-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d481-127">Requirements</span></span>



| <span data-ttu-id="6d481-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d481-128">Requirement</span></span> | <span data-ttu-id="6d481-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d481-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d481-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d481-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6d481-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6d481-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6d481-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d481-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6d481-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d481-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6d481-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6d481-134">Namespace</span></span><br/>                | <span data-ttu-id="6d481-135">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="6d481-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6d481-136">MOF</span><span class="sxs-lookup"><span data-stu-id="6d481-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d481-137"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d481-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d481-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6d481-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d481-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d481-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d481-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d481-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d481-141">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="6d481-141">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="6d481-142">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="6d481-142">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

