---
description: La \_ classe WMI de l’Association PrinterSetting Win32 associe une imprimante et ses paramètres de configuration.
ms.assetid: 5d0f0724-0583-449b-a6da-336e7c8e526e
ms.tgt_platform: multiple
title: Classe Win32_PrinterSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterSetting
- Win32_PrinterSetting.Setting
- Win32_PrinterSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90a77678e61b755550ebb1818c34ccdc3159a88c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200998"
---
# <a name="win32_printersetting-class"></a><span data-ttu-id="00825-103">\_Classe PrinterSetting Win32</span><span class="sxs-lookup"><span data-stu-id="00825-103">Win32\_PrinterSetting class</span></span>

<span data-ttu-id="00825-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ PrinterSetting Win32** associe une imprimante et ses paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="00825-104">The **Win32\_PrinterSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a printer and its configuration settings.</span></span>

<span data-ttu-id="00825-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="00825-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="00825-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="00825-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="00825-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00825-107">Syntax</span></span>

``` syntax
class Win32_PrinterSetting : Win32_DeviceSettings
{
  CIM_Setting       REF Setting;
  CIM_LogicalDevice REF Element;
};
```

## <a name="members"></a><span data-ttu-id="00825-108">Membres</span><span class="sxs-lookup"><span data-stu-id="00825-108">Members</span></span>

<span data-ttu-id="00825-109">La classe **Win32 \_ PrinterSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="00825-109">The **Win32\_PrinterSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="00825-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="00825-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="00825-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="00825-111">Properties</span></span>

<span data-ttu-id="00825-112">La classe **Win32 \_ PrinterSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="00825-112">The **Win32\_PrinterSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="00825-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="00825-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00825-114">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="00825-114">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="00825-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00825-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00825-116">Qualificateurs : [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="00825-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="00825-117">[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui représente les propriétés de l’appareil logique sur lequel les paramètres peuvent être appliqués.</span><span class="sxs-lookup"><span data-stu-id="00825-117">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents properties of the logical device on which the settings can be applied.</span></span>

<span data-ttu-id="00825-118">Cette propriété est héritée de [**Win32 \_ DeviceSettings**](win32-devicesettings.md).</span><span class="sxs-lookup"><span data-stu-id="00825-118">This property is inherited from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

</dd> <dt>

<span data-ttu-id="00825-119">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="00825-119">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00825-120">Type de données **: \_ paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="00825-120">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="00825-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00825-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00825-122">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« paramètre CIM CIM \| \_ »)</span><span class="sxs-lookup"><span data-stu-id="00825-122">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_Setting")</span></span>
</dt> </dl>

<span data-ttu-id="00825-123">[**\_ Paramètre CIM**](cim-setting.md) qui représente les paramètres qui peuvent être appliqués à l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="00825-123">A [**CIM\_Setting**](cim-setting.md) that represents settings that can be applied to the logical device.</span></span>

<span data-ttu-id="00825-124">Cette propriété est héritée de [**Win32 \_ DeviceSettings**](win32-devicesettings.md).</span><span class="sxs-lookup"><span data-stu-id="00825-124">This property is inherited from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00825-125">Notes</span><span class="sxs-lookup"><span data-stu-id="00825-125">Remarks</span></span>

<span data-ttu-id="00825-126">La classe **Win32 \_ PrinterSetting** est dérivée de [**Win32 \_ DeviceSettings**](win32-devicesettings.md).</span><span class="sxs-lookup"><span data-stu-id="00825-126">The **Win32\_PrinterSetting** class is derived from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="00825-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00825-127">Requirements</span></span>



| <span data-ttu-id="00825-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00825-128">Requirement</span></span> | <span data-ttu-id="00825-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="00825-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="00825-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00825-130">Minimum supported client</span></span><br/> | <span data-ttu-id="00825-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="00825-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="00825-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00825-132">Minimum supported server</span></span><br/> | <span data-ttu-id="00825-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00825-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="00825-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="00825-134">Namespace</span></span><br/>                | <span data-ttu-id="00825-135">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="00825-135">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="00825-136">MOF</span><span class="sxs-lookup"><span data-stu-id="00825-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00825-137"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="00825-137"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="00825-138">DLL</span><span class="sxs-lookup"><span data-stu-id="00825-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00825-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00825-139"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="00825-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00825-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00825-141">**\_DeviceSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="00825-141">**Win32\_DeviceSettings**</span></span>](win32-devicesettings.md)
</dt> <dt>

[<span data-ttu-id="00825-142">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="00825-142">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
