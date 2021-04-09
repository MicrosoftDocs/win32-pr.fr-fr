---
description: Le \_ VolumeChangeEvent Win32 représente un événement de lecteur local qui résulte de l’ajout d’une lettre de lecteur ou d’un lecteur monté sur le système informatique.
ms.assetid: 38595319-d7a1-4dcd-9ad8-a27cc484b699
ms.tgt_platform: multiple
title: Classe Win32_VolumeChangeEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VolumeChangeEvent
- Win32_VolumeChangeEvent.SECURITY_DESCRIPTOR
- Win32_VolumeChangeEvent.TIME_CREATED
- Win32_VolumeChangeEvent.EventType
- Win32_VolumeChangeEvent.DriveName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e7610cae8d0cc746774b99a101e3c6aaf1f8a64d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110218"
---
# <a name="win32_volumechangeevent-class"></a><span data-ttu-id="07c30-103">\_Classe VolumeChangeEvent Win32</span><span class="sxs-lookup"><span data-stu-id="07c30-103">Win32\_VolumeChangeEvent class</span></span>

<span data-ttu-id="07c30-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) de **\_ VolumeChangeEvent Win32** représente un événement de lecteur local qui résulte de l’ajout d’une lettre de lecteur ou d’un lecteur monté sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="07c30-104">The **Win32\_VolumeChangeEvent** [WMI class](../wmisdk/retrieving-a-class.md) represents a local drive event that results from the addition of a drive letter or mounted drive on the computer system.</span></span> <span data-ttu-id="07c30-105">Les lecteurs réseau ne sont pas pris en charge actuellement.</span><span class="sxs-lookup"><span data-stu-id="07c30-105">Network drives are not currently supported.</span></span>

<span data-ttu-id="07c30-106">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="07c30-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="07c30-107">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="07c30-107">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="07c30-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07c30-108">Syntax</span></span>

``` syntax
[UUID("455CE053-2552-4051-A3E4-C4200DC31B7"), AMENDMENT]
class Win32_VolumeChangeEvent : Win32_DeviceChangeEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
  string DriveName;
};
```

## <a name="members"></a><span data-ttu-id="07c30-109">Membres</span><span class="sxs-lookup"><span data-stu-id="07c30-109">Members</span></span>

<span data-ttu-id="07c30-110">La classe **Win32 \_ VolumeChangeEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="07c30-110">The **Win32\_VolumeChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="07c30-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="07c30-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="07c30-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="07c30-112">Properties</span></span>

<span data-ttu-id="07c30-113">La classe **Win32 \_ VolumeChangeEvent** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="07c30-113">The **Win32\_VolumeChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="07c30-114">**DriveName**</span><span class="sxs-lookup"><span data-stu-id="07c30-114">**DriveName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c30-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="07c30-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07c30-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="07c30-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07c30-117">Nom du lecteur (lettre) qui a été ajouté ou supprimé du système.</span><span class="sxs-lookup"><span data-stu-id="07c30-117">Drive name (letter) that has been added or removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="07c30-118">**EventType**</span><span class="sxs-lookup"><span data-stu-id="07c30-118">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c30-119">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07c30-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07c30-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="07c30-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07c30-121">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("messages de gestion Win32APIDevice \| WM \_ DEVICECHANGE \| wParam", "Win32APIDevice de gestion des messages \| WM \_ SETTINGCHANGE")</span><span class="sxs-lookup"><span data-stu-id="07c30-121">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice Management Messages\|WM\_DEVICECHANGE\|wParam", "Win32APIDevice Management Messages\|WM\_SETTINGCHANGE")</span></span>
</dt> </dl>

<span data-ttu-id="07c30-122">Type de notification de modification d’événement qui s’est produite.</span><span class="sxs-lookup"><span data-stu-id="07c30-122">Type of event change notification that has occurred.</span></span>

<span data-ttu-id="07c30-123">Cette propriété est héritée de [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md).</span><span class="sxs-lookup"><span data-stu-id="07c30-123">This property is inherited from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

<span data-ttu-id="07c30-124">**Configuration modifiée** (1)</span><span class="sxs-lookup"><span data-stu-id="07c30-124">**Configuration Changed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

<span data-ttu-id="07c30-125">**Arrivée** de l’appareil (2)</span><span class="sxs-lookup"><span data-stu-id="07c30-125">**Device Arrival** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

<span data-ttu-id="07c30-126">**Suppression** de l’appareil (3)</span><span class="sxs-lookup"><span data-stu-id="07c30-126">**Device Removal** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

<span data-ttu-id="07c30-127">**Ancrage** (4)</span><span class="sxs-lookup"><span data-stu-id="07c30-127">**Docking** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="07c30-128">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="07c30-128">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c30-129">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="07c30-129">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="07c30-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="07c30-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07c30-131">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="07c30-131">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="07c30-132">Cette propriété est héritée de l' [**\_ \_ événement**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="07c30-132">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span> <span data-ttu-id="07c30-133">Pour plus d’informations sur les constantes utilisées pour définir ce descripteur de sécurité, voir la rubrique sur les [constantes de sécurité WMI](../wmisdk/wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="07c30-133">For more information about constants used to set this security descriptor, see [WMI Security Constants](../wmisdk/wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="07c30-134">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="07c30-134">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07c30-135">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="07c30-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="07c30-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="07c30-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07c30-137">Valeur unique qui indique l’heure à laquelle l’événement a été généré.</span><span class="sxs-lookup"><span data-stu-id="07c30-137">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="07c30-138">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="07c30-138">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="07c30-139">Les informations sont au format de temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="07c30-139">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="07c30-140">Cette propriété est héritée de l' [**\_ \_ événement**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="07c30-140">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span>

<span data-ttu-id="07c30-141">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="07c30-141">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07c30-142">Notes</span><span class="sxs-lookup"><span data-stu-id="07c30-142">Remarks</span></span>

<span data-ttu-id="07c30-143">La classe **Win32 \_ VolumeChangeEvent** est dérivée de [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md).</span><span class="sxs-lookup"><span data-stu-id="07c30-143">The **Win32\_VolumeChangeEvent** class is derived from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="07c30-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07c30-144">Requirements</span></span>



| <span data-ttu-id="07c30-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07c30-145">Requirement</span></span> | <span data-ttu-id="07c30-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="07c30-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07c30-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07c30-147">Minimum supported client</span></span><br/> | <span data-ttu-id="07c30-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07c30-148">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="07c30-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07c30-149">Minimum supported server</span></span><br/> | <span data-ttu-id="07c30-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07c30-150">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="07c30-151">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="07c30-151">Namespace</span></span><br/>                | <span data-ttu-id="07c30-152">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="07c30-152">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="07c30-153">MOF</span><span class="sxs-lookup"><span data-stu-id="07c30-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07c30-154"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="07c30-154"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="07c30-155">DLL</span><span class="sxs-lookup"><span data-stu-id="07c30-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07c30-156"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07c30-156"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07c30-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07c30-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07c30-158">**\_DeviceChangeEvent Win32**</span><span class="sxs-lookup"><span data-stu-id="07c30-158">**Win32\_DeviceChangeEvent**</span></span>](win32-devicechangeevent.md)
</dt> <dt>

[<span data-ttu-id="07c30-159">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="07c30-159">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
