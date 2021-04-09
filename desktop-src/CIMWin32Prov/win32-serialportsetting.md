---
description: La \_ classe WMI de l’Association SerialPortSetting Win32 associe un port série et ses paramètres de configuration.
ms.assetid: 57856207-abe5-4d93-9a34-acfe30ccd80c
ms.tgt_platform: multiple
title: Classe Win32_SerialPortSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortSetting
- Win32_SerialPortSetting.Setting
- Win32_SerialPortSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 713cdb57b5ed7135529959d3c17f7453924ce1dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950447"
---
# <a name="win32_serialportsetting-class"></a><span data-ttu-id="38975-103">\_Classe SerialPortSetting Win32</span><span class="sxs-lookup"><span data-stu-id="38975-103">Win32\_SerialPortSetting class</span></span>

<span data-ttu-id="38975-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ SerialPortSetting Win32** associe un port série et ses paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="38975-104">The **Win32\_SerialPortSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a serial port and its configuration settings.</span></span>

<span data-ttu-id="38975-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="38975-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="38975-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="38975-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="38975-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38975-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortSetting : Win32_DeviceSettings
{
  Win32_SerialPortConfiguration REF Setting;
  Win32_SerialPort              REF Element;
};
```

## <a name="members"></a><span data-ttu-id="38975-108">Membres</span><span class="sxs-lookup"><span data-stu-id="38975-108">Members</span></span>

<span data-ttu-id="38975-109">La classe **Win32 \_ SerialPortSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="38975-109">The **Win32\_SerialPortSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="38975-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="38975-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38975-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="38975-111">Properties</span></span>

<span data-ttu-id="38975-112">La classe **Win32 \_ SerialPortSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="38975-112">The **Win32\_SerialPortSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38975-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="38975-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38975-114">Type de données : **Win32 \_ SerialPort**</span><span class="sxs-lookup"><span data-stu-id="38975-114">Data type: **Win32\_SerialPort**</span></span>
</dt> <dt>

<span data-ttu-id="38975-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="38975-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38975-116">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SerialPort")</span><span class="sxs-lookup"><span data-stu-id="38975-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SerialPort")</span></span>
</dt> </dl>

<span data-ttu-id="38975-117">Un [**\_ SerialPort Win32**](win32-serialport.md) qui contient les propriétés d’un port série sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="38975-117">A [**Win32\_SerialPort**](win32-serialport.md) that contains the properties of a serial port on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="38975-118">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="38975-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38975-119">Type de données : **Win32 \_ SerialPortConfiguration**</span><span class="sxs-lookup"><span data-stu-id="38975-119">Data type: **Win32\_SerialPortConfiguration**</span></span>
</dt> <dt>

<span data-ttu-id="38975-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="38975-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38975-121">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SerialPortConfiguration")</span><span class="sxs-lookup"><span data-stu-id="38975-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SerialPortConfiguration")</span></span>
</dt> </dl>

<span data-ttu-id="38975-122">[**\_ SerialPortConfiguration Win32**](win32-serialportconfiguration.md) qui contient le paramètre de configuration pour le port série.</span><span class="sxs-lookup"><span data-stu-id="38975-122">A [**Win32\_SerialPortConfiguration**](win32-serialportconfiguration.md) that contains the configuration setting for the serial port.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38975-123">Notes</span><span class="sxs-lookup"><span data-stu-id="38975-123">Remarks</span></span>

<span data-ttu-id="38975-124">La classe **Win32 \_ SerialPortSetting** est dérivée de [**Win32 \_ DeviceSettings**](win32-devicesettings.md).</span><span class="sxs-lookup"><span data-stu-id="38975-124">The **Win32\_SerialPortSetting** class is derived from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="38975-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38975-125">Requirements</span></span>



| <span data-ttu-id="38975-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38975-126">Requirement</span></span> | <span data-ttu-id="38975-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="38975-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38975-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38975-128">Minimum supported client</span></span><br/> | <span data-ttu-id="38975-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38975-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="38975-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38975-130">Minimum supported server</span></span><br/> | <span data-ttu-id="38975-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38975-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="38975-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="38975-132">Namespace</span></span><br/>                | <span data-ttu-id="38975-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="38975-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="38975-134">MOF</span><span class="sxs-lookup"><span data-stu-id="38975-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38975-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38975-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="38975-136">DLL</span><span class="sxs-lookup"><span data-stu-id="38975-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38975-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38975-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38975-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38975-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38975-139">**\_DeviceSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="38975-139">**Win32\_DeviceSettings**</span></span>](win32-devicesettings.md)
</dt> <dt>

[<span data-ttu-id="38975-140">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="38975-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
