---
description: La \_ classe WMI DeviceSettings abstract, association WMI associe un appareil logique et un paramètre qui lui est appliqué.
ms.assetid: 4f6c4c26-8da9-4e2c-8b8c-cec658ac08d4
ms.tgt_platform: multiple
title: Classe Win32_DeviceSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceSettings
- Win32_DeviceSettings.Setting
- Win32_DeviceSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1cd9cae29cfa608c9f3c0c36ebfe3ca7f903c809
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201085"
---
# <a name="win32_devicesettings-class"></a><span data-ttu-id="bd4e2-103">\_Classe DeviceSettings Win32</span><span class="sxs-lookup"><span data-stu-id="bd4e2-103">Win32\_DeviceSettings class</span></span>

<span data-ttu-id="bd4e2-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DeviceSettings** abstract, association WMI associe un appareil logique et un paramètre qui lui est appliqué.</span><span class="sxs-lookup"><span data-stu-id="bd4e2-104">The **Win32\_DeviceSettings** abstract, association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical device and a setting that can be applied to it.</span></span>

<span data-ttu-id="bd4e2-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="bd4e2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="bd4e2-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="bd4e2-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd4e2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd4e2-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4FD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceSettings : CIM_ElementSetting
{
  CIM_Setting       REF Setting;
  CIM_LogicalDevice REF Element;
};
```

## <a name="members"></a><span data-ttu-id="bd4e2-108">Membres</span><span class="sxs-lookup"><span data-stu-id="bd4e2-108">Members</span></span>

<span data-ttu-id="bd4e2-109">La classe **Win32 \_ DeviceSettings** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bd4e2-109">The **Win32\_DeviceSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="bd4e2-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bd4e2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bd4e2-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bd4e2-111">Properties</span></span>

<span data-ttu-id="bd4e2-112">La classe **Win32 \_ DeviceSettings** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="bd4e2-112">The **Win32\_DeviceSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bd4e2-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="bd4e2-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd4e2-114">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="bd4e2-114">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="bd4e2-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd4e2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd4e2-116">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="bd4e2-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="bd4e2-117">[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui représente les propriétés de l’appareil logique sur lequel les paramètres peuvent être appliqués.</span><span class="sxs-lookup"><span data-stu-id="bd4e2-117">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents properties of the logical device on which the settings can be applied.</span></span>

</dd> <dt>

<span data-ttu-id="bd4e2-118">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="bd4e2-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd4e2-119">Type de données **: \_ paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="bd4e2-119">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="bd4e2-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd4e2-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd4e2-121">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« paramètre »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« paramètre CIM \| CIM \_ »)</span><span class="sxs-lookup"><span data-stu-id="bd4e2-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_Setting")</span></span>
</dt> </dl>

<span data-ttu-id="bd4e2-122">[**\_ Paramètre CIM**](cim-setting.md) qui représente les paramètres qui peuvent être appliqués à l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="bd4e2-122">A [**CIM\_Setting**](cim-setting.md) that represents settings that can be applied to the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd4e2-123">Notes</span><span class="sxs-lookup"><span data-stu-id="bd4e2-123">Remarks</span></span>

<span data-ttu-id="bd4e2-124">La classe **Win32 \_ DeviceSettings** est dérivée de [**CIM \_ ElementSetting**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="bd4e2-124">The **Win32\_DeviceSettings** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd4e2-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd4e2-125">Requirements</span></span>



| <span data-ttu-id="bd4e2-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd4e2-126">Requirement</span></span> | <span data-ttu-id="bd4e2-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd4e2-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd4e2-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd4e2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bd4e2-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd4e2-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bd4e2-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd4e2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bd4e2-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd4e2-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bd4e2-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bd4e2-132">Namespace</span></span><br/>                | <span data-ttu-id="bd4e2-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="bd4e2-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bd4e2-134">MOF</span><span class="sxs-lookup"><span data-stu-id="bd4e2-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd4e2-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd4e2-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd4e2-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bd4e2-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd4e2-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd4e2-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd4e2-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd4e2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd4e2-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="bd4e2-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="bd4e2-140">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="bd4e2-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

