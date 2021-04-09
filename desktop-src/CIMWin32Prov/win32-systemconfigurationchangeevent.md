---
description: Le \_ SystemConfigurationChangeEvent Win32&\# 8194 ; La classe WMI indique que la liste des appareils a été actualisée sur le système (un appareil a été ajouté ou supprimé ou la configuration a été modifiée).
ms.assetid: dce1e866-e739-4f90-9016-48b20ccfb75b
ms.tgt_platform: multiple
title: Classe Win32_SystemConfigurationChangeEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemConfigurationChangeEvent
- Win32_SystemConfigurationChangeEvent.SECURITY_DESCRIPTOR
- Win32_SystemConfigurationChangeEvent.TIME_CREATED
- Win32_SystemConfigurationChangeEvent.EventType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0bc479d3415906a6536c6df1d163056e94e2af76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111327"
---
# <a name="win32_systemconfigurationchangeevent-class"></a><span data-ttu-id="71404-103">\_Classe SystemConfigurationChangeEvent Win32</span><span class="sxs-lookup"><span data-stu-id="71404-103">Win32\_SystemConfigurationChangeEvent class</span></span>

<span data-ttu-id="71404-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SystemConfigurationChangeEvent** WMI indique que la liste des appareils sur le système a été actualisée (un appareil a été ajouté ou supprimé ou la configuration a été modifiée).</span><span class="sxs-lookup"><span data-stu-id="71404-104">The **Win32\_SystemConfigurationChangeEvent** [WMI class](../wmisdk/retrieving-a-class.md) indicates that the device list on the system has been refreshed (a device has been added or removed, or the configuration changed).</span></span> <span data-ttu-id="71404-105">Un événement est déclenché et une instance de cette classe est créée lorsque le message « DevMgrRefreshOn<*ComputerName*> » est envoyé.</span><span class="sxs-lookup"><span data-stu-id="71404-105">An event is fired and an instance of this is class created when the "DevMgrRefreshOn<*ComputerName*>" message is sent.</span></span> <span data-ttu-id="71404-106">La modification exacte de la liste des appareils n’est pas contenue dans le message, de sorte qu’une actualisation de l’appareil est nécessaire pour obtenir les paramètres système actuels.</span><span class="sxs-lookup"><span data-stu-id="71404-106">The exact change to the device list is not contained in the message, so a device refresh is required to obtain the current system settings.</span></span> <span data-ttu-id="71404-107">Les paramètres IRQ, les ports COM et les versions du BIOS sont des exemples de modifications de configuration affectées.</span><span class="sxs-lookup"><span data-stu-id="71404-107">Examples of configuration changes affected are IRQ settings, COM ports, and BIOS versions.</span></span>

<span data-ttu-id="71404-108">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="71404-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="71404-109">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="71404-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="71404-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71404-110">Syntax</span></span>

``` syntax
[UUID("76746942-D94B-47E2-BBA4-AFD2FDBA61"), AMENDMENT]
class Win32_SystemConfigurationChangeEvent : Win32_DeviceChangeEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
};
```

## <a name="members"></a><span data-ttu-id="71404-111">Membres</span><span class="sxs-lookup"><span data-stu-id="71404-111">Members</span></span>

<span data-ttu-id="71404-112">La classe **Win32 \_ SystemConfigurationChangeEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="71404-112">The **Win32\_SystemConfigurationChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="71404-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="71404-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="71404-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="71404-114">Properties</span></span>

<span data-ttu-id="71404-115">La classe **Win32 \_ SystemConfigurationChangeEvent** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="71404-115">The **Win32\_SystemConfigurationChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="71404-116">**EventType**</span><span class="sxs-lookup"><span data-stu-id="71404-116">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71404-117">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71404-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71404-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="71404-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71404-119">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("messages de gestion Win32APIDevice \| WM \_ DEVICECHANGE \| wParam", "Win32APIDevice de gestion des messages \| WM \_ SETTINGCHANGE")</span><span class="sxs-lookup"><span data-stu-id="71404-119">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice Management Messages\|WM\_DEVICECHANGE\|wParam", "Win32APIDevice Management Messages\|WM\_SETTINGCHANGE")</span></span>
</dt> </dl>

<span data-ttu-id="71404-120">Type de notification de modification d’événement qui s’est produite.</span><span class="sxs-lookup"><span data-stu-id="71404-120">Type of event change notification that has occurred.</span></span>

<span data-ttu-id="71404-121">Cette propriété est héritée de [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md).</span><span class="sxs-lookup"><span data-stu-id="71404-121">This property is inherited from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

<span data-ttu-id="71404-122">**Configuration modifiée** (1)</span><span class="sxs-lookup"><span data-stu-id="71404-122">**Configuration Changed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

<span data-ttu-id="71404-123">**Arrivée** de l’appareil (2)</span><span class="sxs-lookup"><span data-stu-id="71404-123">**Device Arrival** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

<span data-ttu-id="71404-124">**Suppression** de l’appareil (3)</span><span class="sxs-lookup"><span data-stu-id="71404-124">**Device Removal** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

<span data-ttu-id="71404-125">**Ancrage** (4)</span><span class="sxs-lookup"><span data-stu-id="71404-125">**Docking** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="71404-126">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="71404-126">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71404-127">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="71404-127">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="71404-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="71404-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71404-129">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="71404-129">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="71404-130">Cette propriété est héritée de l' [**\_ \_ événement**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="71404-130">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span> <span data-ttu-id="71404-131">Pour plus d’informations sur les constantes utilisées pour définir ce descripteur de sécurité, voir la rubrique sur les [constantes de sécurité WMI](../wmisdk/wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="71404-131">For more information about constants used to set this security descriptor, see [WMI Security Constants](../wmisdk/wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="71404-132">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="71404-132">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71404-133">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="71404-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="71404-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="71404-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71404-135">Valeur unique qui indique l’heure à laquelle l’événement a été généré.</span><span class="sxs-lookup"><span data-stu-id="71404-135">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="71404-136">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="71404-136">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="71404-137">Les informations sont au format de temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="71404-137">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="71404-138">Cette propriété est héritée de l' [**\_ \_ événement**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="71404-138">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span>

<span data-ttu-id="71404-139">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="71404-139">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="71404-140">Notes</span><span class="sxs-lookup"><span data-stu-id="71404-140">Remarks</span></span>

<span data-ttu-id="71404-141">La classe **Win32 \_ SystemConfigurationChangeEvent** est dérivée de [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md).</span><span class="sxs-lookup"><span data-stu-id="71404-141">The **Win32\_SystemConfigurationChangeEvent** class is derived from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="71404-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71404-142">Requirements</span></span>



| <span data-ttu-id="71404-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71404-143">Requirement</span></span> | <span data-ttu-id="71404-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="71404-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71404-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71404-145">Minimum supported client</span></span><br/> | <span data-ttu-id="71404-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71404-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="71404-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71404-147">Minimum supported server</span></span><br/> | <span data-ttu-id="71404-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71404-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="71404-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="71404-149">Namespace</span></span><br/>                | <span data-ttu-id="71404-150">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="71404-150">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="71404-151">MOF</span><span class="sxs-lookup"><span data-stu-id="71404-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71404-152"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="71404-152"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="71404-153">DLL</span><span class="sxs-lookup"><span data-stu-id="71404-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71404-154"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71404-154"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71404-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71404-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71404-156">**\_DeviceChangeEvent Win32**</span><span class="sxs-lookup"><span data-stu-id="71404-156">**Win32\_DeviceChangeEvent**</span></span>](win32-devicechangeevent.md)
</dt> <dt>

[<span data-ttu-id="71404-157">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="71404-157">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
