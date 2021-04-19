---
description: La \_ classe WMI de l’Association USBControllerDevice Win32 associe un contrôleur USB (Universal Serial Bus) et l' \_ instance du LogicalDevice CIM qui lui est connectée.
ms.assetid: a0c64984-9116-4cb8-86e0-38c897cb7119
ms.tgt_platform: multiple
title: Classe Win32_USBControllerDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_USBControllerDevice
- Win32_USBControllerDevice.NegotiatedDataWidth
- Win32_USBControllerDevice.NegotiatedSpeed
- Win32_USBControllerDevice.AccessState
- Win32_USBControllerDevice.NumberOfHardResets
- Win32_USBControllerDevice.NumberOfSoftResets
- Win32_USBControllerDevice.Antecedent
- Win32_USBControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9bf72c92a4ae23ac7750cdd52914e86f5dbcdd01
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515351"
---
# <a name="win32_usbcontrollerdevice-class"></a><span data-ttu-id="08731-103">\_Classe USBControllerDevice Win32</span><span class="sxs-lookup"><span data-stu-id="08731-103">Win32\_USBControllerDevice class</span></span>

<span data-ttu-id="08731-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ USBControllerDevice Win32** associe un contrôleur USB (Universal Serial Bus) et l’instance du [**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui lui est connectée.</span><span class="sxs-lookup"><span data-stu-id="08731-104">The **Win32\_USBControllerDevice** association [WMI class](../wmisdk/retrieving-a-class.md) relates a universal serial bus (USB) controller and the [**CIM\_LogicalDevice**](cim-logicaldevice.md) instance connected to it.</span></span>

<span data-ttu-id="08731-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="08731-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="08731-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="08731-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="08731-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08731-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{DE57D792-A032-11D2-90F0-0060081A46FD}"), AMENDMENT]
class Win32_USBControllerDevice : CIM_ControlledBy
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  CIM_USBController REF Antecedent;
  CIM_LogicalDevice REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="08731-108">Membres</span><span class="sxs-lookup"><span data-stu-id="08731-108">Members</span></span>

<span data-ttu-id="08731-109">La classe **Win32 \_ USBControllerDevice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="08731-109">The **Win32\_USBControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="08731-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="08731-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="08731-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="08731-111">Properties</span></span>

<span data-ttu-id="08731-112">La classe **Win32 \_ USBControllerDevice** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="08731-112">The **Win32\_USBControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="08731-113">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="08731-113">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08731-114">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08731-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08731-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08731-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08731-116">Indique si le contrôleur commande ou accède activement à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="08731-116">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="08731-117">Ces informations sont nécessaires lorsqu’un périphérique logique peut être utilisé par plusieurs contrôleurs, ou y accéder via.</span><span class="sxs-lookup"><span data-stu-id="08731-117">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="08731-118">Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="08731-118">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="08731-119">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="08731-119">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="08731-120">**Actif** (1)</span><span class="sxs-lookup"><span data-stu-id="08731-120">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="08731-121">**Inactif** (2)</span><span class="sxs-lookup"><span data-stu-id="08731-121">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="08731-122">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="08731-122">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08731-123">Type de données : **CIM \_ USBController**</span><span class="sxs-lookup"><span data-stu-id="08731-123">Data type: **CIM\_USBController**</span></span>
</dt> <dt>

<span data-ttu-id="08731-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08731-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08731-125">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ USBController")</span><span class="sxs-lookup"><span data-stu-id="08731-125">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_USBController")</span></span>
</dt> </dl>

<span data-ttu-id="08731-126">[**\_ USBController CIM**](cim-usbcontroller.md) représentant le contrôleur USB (Universal Serial Bus) associé à cet appareil.</span><span class="sxs-lookup"><span data-stu-id="08731-126">A [**CIM\_USBController**](cim-usbcontroller.md) representing the Universal Serial Bus (USB) controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="08731-127">**Charge**</span><span class="sxs-lookup"><span data-stu-id="08731-127">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08731-128">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="08731-128">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="08731-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08731-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08731-130">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) (« dépendant »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« CIM \| CIM \_ LogicalDevice »)</span><span class="sxs-lookup"><span data-stu-id="08731-130">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="08731-131">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) décrivant l’unité logique connectée au contrôleur USB (Universal Serial Bus).</span><span class="sxs-lookup"><span data-stu-id="08731-131">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) describing the logical device connected to the Universal Serial Bus (USB) controller.</span></span>

</dd> <dt>

<span data-ttu-id="08731-132">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="08731-132">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08731-133">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08731-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08731-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08731-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08731-135">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« bits »)</span><span class="sxs-lookup"><span data-stu-id="08731-135">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="08731-136">Lorsque plusieurs largeurs de données de bus ou de connexion sont possibles, cette propriété définit celle qui est utilisée entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="08731-136">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="08731-137">La largeur des données est spécifiée en bits.</span><span class="sxs-lookup"><span data-stu-id="08731-137">Data width is specified in bits.</span></span> <span data-ttu-id="08731-138">Si la largeur des données n’est pas négociée, ou si ces informations ne sont pas disponibles ou importantes pour la gestion des appareils, la propriété doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="08731-138">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="08731-139">Cette propriété est héritée de la [**\_ DeviceConnection CIM**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="08731-139">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="08731-140">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="08731-140">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08731-141">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="08731-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="08731-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08731-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08731-143">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="08731-143">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="08731-144">Lorsque plusieurs vitesses de bus ou de connexion sont possibles, cette propriété définit celle qui est utilisée entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="08731-144">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="08731-145">La vitesse est spécifiée en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="08731-145">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="08731-146">Si les vitesses de connexion ou de bus ne sont pas négociées, ou si ces informations ne sont pas disponibles ou importantes pour la gestion des appareils, la propriété doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="08731-146">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="08731-147">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="08731-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="08731-148">Cette propriété est héritée de la [**\_ DeviceConnection CIM**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="08731-148">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="08731-149">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="08731-149">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08731-150">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08731-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08731-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08731-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08731-152">Nombre de réinitialisations matérielles émises par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="08731-152">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="08731-153">Une réinitialisation matérielle retourne l’appareil à son état d’initialisation ou de démarrage.</span><span class="sxs-lookup"><span data-stu-id="08731-153">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="08731-154">Toutes les informations sur l’état de l’appareil interne et les données sont perdues.</span><span class="sxs-lookup"><span data-stu-id="08731-154">All internal device state information and data are lost.</span></span>

<span data-ttu-id="08731-155">Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="08731-155">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="08731-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="08731-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08731-157">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08731-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08731-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08731-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08731-159">Nombre de réinitialisations logicielles émises par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="08731-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="08731-160">Une réinitialisation logicielle n’efface pas complètement l’état actuel de l’appareil et les données.</span><span class="sxs-lookup"><span data-stu-id="08731-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="08731-161">Les sémantiques exactes dépendent de l’appareil et des protocoles et mécanismes utilisés pour communiquer avec lui.</span><span class="sxs-lookup"><span data-stu-id="08731-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="08731-162">Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="08731-162">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08731-163">Notes</span><span class="sxs-lookup"><span data-stu-id="08731-163">Remarks</span></span>

<span data-ttu-id="08731-164">La classe **Win32 \_ USBControllerDevice** est dérivée de [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="08731-164">The **Win32\_USBControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="08731-165">Pour plus d’informations sur l’utilisation de, consultez l’article [affichage des périphériques USB à l’aide](https://devblogs.microsoft.com/powershell/displaying-usb-devices-using-wmi/) du blog WMI.</span><span class="sxs-lookup"><span data-stu-id="08731-165">For a discussion on using, see the [Displaying USB Devices using WMI](https://devblogs.microsoft.com/powershell/displaying-usb-devices-using-wmi/) blog article.</span></span> <span data-ttu-id="08731-166">Pour plus d’informations sur l’utilisation des classes d’association, consultez l’article [obtenir-USB – utilisation des classes d’association WMI dans PowerShell](https://devblogs.microsoft.com/powershell/get-usb-using-wmi-association-classes-in-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="08731-166">For a discussion of using association classes, see the [Get-USB – Using WMI Association Classes in PowerShell](https://devblogs.microsoft.com/powershell/get-usb-using-wmi-association-classes-in-powershell/) article.</span></span>

## <a name="examples"></a><span data-ttu-id="08731-167">Exemples</span><span class="sxs-lookup"><span data-stu-id="08731-167">Examples</span></span>

<span data-ttu-id="08731-168">L’exemple PowerShell suivant récupère l’unité logique dépendante et affiche les informations pertinentes.</span><span class="sxs-lookup"><span data-stu-id="08731-168">The following PowerShell example retrieves the dependent logical device and displays the relevant information.</span></span>


```PowerShell
gwmi Win32_USBControllerDevice |%{[wmi]($_.Dependent)} | Sort Manufacturer,Description,DeviceID | Ft -GroupBy Manufacturer Description,Service,DeviceID
```



## <a name="requirements"></a><span data-ttu-id="08731-169">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08731-169">Requirements</span></span>



| <span data-ttu-id="08731-170">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08731-170">Requirement</span></span> | <span data-ttu-id="08731-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="08731-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08731-172">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08731-172">Minimum supported client</span></span><br/> | <span data-ttu-id="08731-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08731-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="08731-174">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08731-174">Minimum supported server</span></span><br/> | <span data-ttu-id="08731-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08731-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="08731-176">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="08731-176">Namespace</span></span><br/>                | <span data-ttu-id="08731-177">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="08731-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="08731-178">MOF</span><span class="sxs-lookup"><span data-stu-id="08731-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08731-179"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08731-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="08731-180">DLL</span><span class="sxs-lookup"><span data-stu-id="08731-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08731-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08731-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08731-182">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08731-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08731-183">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="08731-183">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="08731-184">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="08731-184">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
