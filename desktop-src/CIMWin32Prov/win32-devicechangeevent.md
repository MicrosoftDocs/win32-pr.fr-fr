---
description: La \_ classe WMI DeviceChangeEvent abstraite Win32 représente les événements de changement d’appareil qui résultent de l’ajout, de la suppression ou de la modification d’appareils sur le système informatique.
ms.assetid: 78155357-4231-4ded-980e-89feeb864ef2
ms.tgt_platform: multiple
title: Classe Win32_DeviceChangeEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceChangeEvent
- Win32_DeviceChangeEvent.SECURITY_DESCRIPTOR
- Win32_DeviceChangeEvent.TIME_CREATED
- Win32_DeviceChangeEvent.EventType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0f97ab262d95b70a69b06e15202a78d5c1364f90
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749029"
---
# <a name="win32_devicechangeevent-class"></a><span data-ttu-id="ea72d-103">\_Classe DeviceChangeEvent Win32</span><span class="sxs-lookup"><span data-stu-id="ea72d-103">Win32\_DeviceChangeEvent class</span></span>

<span data-ttu-id="ea72d-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DeviceChangeEvent** abstraite Win32 représente les événements de changement d’appareil qui résultent de l’ajout, de la suppression ou de la modification d’appareils sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="ea72d-104">The **Win32\_DeviceChangeEvent** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents device change events that result from the addition, removal, or modification of devices on the computer system.</span></span> <span data-ttu-id="ea72d-105">Cela comprend les modifications apportées à la configuration matérielle (ancrage et déconnexion), à l’état du matériel ou aux appareils récemment mappés (mappage d’un lecteur réseau).</span><span class="sxs-lookup"><span data-stu-id="ea72d-105">This includes changes in the hardware configuration (docking and undocking), the hardware state, or newly mapped devices (mapping of a network drive).</span></span> <span data-ttu-id="ea72d-106">Par exemple, un appareil a été modifié lors de l’envoi d’un \_ message WM DEVICECHANGE.</span><span class="sxs-lookup"><span data-stu-id="ea72d-106">For example, a device has changed when a WM\_DEVICECHANGE message is sent.</span></span>

<span data-ttu-id="ea72d-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ea72d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ea72d-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="ea72d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea72d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea72d-109">Syntax</span></span>

``` syntax
[UUID("0DE6AAF8-49F1-4868-B3D4-61CB69BA4322"), AMENDMENT]
class Win32_DeviceChangeEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
};
```

## <a name="members"></a><span data-ttu-id="ea72d-110">Membres</span><span class="sxs-lookup"><span data-stu-id="ea72d-110">Members</span></span>

<span data-ttu-id="ea72d-111">La classe **Win32 \_ DeviceChangeEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ea72d-111">The **Win32\_DeviceChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="ea72d-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ea72d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ea72d-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ea72d-113">Properties</span></span>

<span data-ttu-id="ea72d-114">La classe **Win32 \_ DeviceChangeEvent** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ea72d-114">The **Win32\_DeviceChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ea72d-115">**EventType**</span><span class="sxs-lookup"><span data-stu-id="ea72d-115">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea72d-116">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea72d-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea72d-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea72d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea72d-118">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("messages de gestion Win32APIDevice \| WM \_ DEVICECHANGE \| wParam", "Win32APIDevice de gestion des messages \| WM \_ SETTINGCHANGE")</span><span class="sxs-lookup"><span data-stu-id="ea72d-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIDevice Management Messages\|WM\_DEVICECHANGE\|wParam", "Win32APIDevice Management Messages\|WM\_SETTINGCHANGE")</span></span>
</dt> </dl>

<span data-ttu-id="ea72d-119">Type de notification de modification d’événement qui s’est produite.</span><span class="sxs-lookup"><span data-stu-id="ea72d-119">Type of event change notification that has occurred.</span></span>

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

<span data-ttu-id="ea72d-120">**Configuration modifiée** (1)</span><span class="sxs-lookup"><span data-stu-id="ea72d-120">**Configuration Changed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

<span data-ttu-id="ea72d-121">**Arrivée** de l’appareil (2)</span><span class="sxs-lookup"><span data-stu-id="ea72d-121">**Device Arrival** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

<span data-ttu-id="ea72d-122">**Suppression** de l’appareil (3)</span><span class="sxs-lookup"><span data-stu-id="ea72d-122">**Device Removal** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

<span data-ttu-id="ea72d-123">**Ancrage** (4)</span><span class="sxs-lookup"><span data-stu-id="ea72d-123">**Docking** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ea72d-124">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="ea72d-124">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea72d-125">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="ea72d-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="ea72d-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea72d-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea72d-127">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="ea72d-127">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="ea72d-128">Cette propriété est héritée de l' [**\_ \_ événement**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="ea72d-128">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="ea72d-129">Pour plus d’informations sur les constantes utilisées pour définir ce descripteur de sécurité, voir la rubrique sur les [constantes de sécurité WMI](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="ea72d-129">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="ea72d-130">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="ea72d-130">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea72d-131">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ea72d-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ea72d-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea72d-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea72d-133">Valeur unique qui indique l’heure à laquelle l’événement a été généré.</span><span class="sxs-lookup"><span data-stu-id="ea72d-133">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="ea72d-134">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="ea72d-134">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="ea72d-135">Les informations sont au format de temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="ea72d-135">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="ea72d-136">Cette propriété est héritée de l' [**\_ \_ événement**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="ea72d-136">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="ea72d-137">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ea72d-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ea72d-138">Notes</span><span class="sxs-lookup"><span data-stu-id="ea72d-138">Remarks</span></span>

<span data-ttu-id="ea72d-139">Le **\_ DeviceChangeEvent Win32** est une classe abstraite dérivée de [**\_ \_ ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent).</span><span class="sxs-lookup"><span data-stu-id="ea72d-139">The **Win32\_DeviceChangeEvent** is an abstract class derived from [**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent).</span></span>

## <a name="requirements"></a><span data-ttu-id="ea72d-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea72d-140">Requirements</span></span>



| <span data-ttu-id="ea72d-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea72d-141">Requirement</span></span> | <span data-ttu-id="ea72d-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea72d-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea72d-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea72d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="ea72d-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ea72d-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ea72d-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea72d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="ea72d-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea72d-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ea72d-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ea72d-147">Namespace</span></span><br/>                | <span data-ttu-id="ea72d-148">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ea72d-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ea72d-149">MOF</span><span class="sxs-lookup"><span data-stu-id="ea72d-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea72d-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea72d-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ea72d-151">DLL</span><span class="sxs-lookup"><span data-stu-id="ea72d-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea72d-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea72d-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea72d-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea72d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea72d-154">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="ea72d-154">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> <dt>

<span data-ttu-id="ea72d-155">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ea72d-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

