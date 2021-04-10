---
description: La \_ classe WMI de l’Association 1394ControllerDevice Win32 associe le contrôleur de bus série haute vitesse (IEEE 1394 FireWire) et l' \_ instance du LogicalDevice CIM qui lui est connectée.
ms.assetid: 327fbced-4637-4402-a06f-6ac352da920c
ms.tgt_platform: multiple
title: Classe Win32_1394ControllerDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_1394ControllerDevice
- Win32_1394ControllerDevice.NegotiatedDataWidth
- Win32_1394ControllerDevice.NegotiatedSpeed
- Win32_1394ControllerDevice.AccessState
- Win32_1394ControllerDevice.NumberOfHardResets
- Win32_1394ControllerDevice.NumberOfSoftResets
- Win32_1394ControllerDevice.Antecedent
- Win32_1394ControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: af3a54db81a388184da148cd411895ebb910de7d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861594"
---
# <a name="win32_1394controllerdevice-class"></a><span data-ttu-id="01826-103">\_Classe 1394ControllerDevice Win32</span><span class="sxs-lookup"><span data-stu-id="01826-103">Win32\_1394ControllerDevice class</span></span>

<span data-ttu-id="01826-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ 1394ControllerDevice Win32** associe le contrôleur de bus série haute vitesse (IEEE 1394 FireWire) et l’instance du [**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui lui est connectée.</span><span class="sxs-lookup"><span data-stu-id="01826-104">The **Win32\_1394ControllerDevice** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates the high-speed serial bus (IEEE 1394 Firewire) Controller and the [**CIM\_LogicalDevice**](cim-logicaldevice.md) instance connected to it.</span></span> <span data-ttu-id="01826-105">Ce bus série offre une connectivité améliorée pour un large éventail d’appareils, notamment les composants audio ou vidéo des consommateurs, les périphériques de stockage, les autres ordinateurs et les appareils portables.</span><span class="sxs-lookup"><span data-stu-id="01826-105">This serial bus provides enhanced connectivity for a wide range of devices, including consumer audio or video components, storage peripherals, other computers, and portable devices.</span></span> <span data-ttu-id="01826-106">IEEE 1394 a été adopté par l’industrie de l’électronique grand public et fournit une interface d’extension compatible Plug-and-Play.</span><span class="sxs-lookup"><span data-stu-id="01826-106">IEEE 1394 has been adopted by the consumer electronics industry and provides a Plug and Play-compatible expansion interface.</span></span>

<span data-ttu-id="01826-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="01826-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="01826-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="01826-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="01826-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01826-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8835CFC9-BAEF-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class Win32_1394ControllerDevice : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  Win32_1394Controller REF Antecedent;
  CIM_LogicalDevice    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="01826-110">Membres</span><span class="sxs-lookup"><span data-stu-id="01826-110">Members</span></span>

<span data-ttu-id="01826-111">La classe **Win32 \_ 1394ControllerDevice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="01826-111">The **Win32\_1394ControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="01826-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="01826-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01826-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="01826-113">Properties</span></span>

<span data-ttu-id="01826-114">La classe **Win32 \_ 1394ControllerDevice** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="01826-114">The **Win32\_1394ControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01826-115">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="01826-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01826-116">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="01826-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="01826-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="01826-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01826-118">Indique si le contrôleur commande ou accède activement à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="01826-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="01826-119">Ces informations sont nécessaires lorsqu’un périphérique logique peut être utilisé par plusieurs contrôleurs, ou y accéder via.</span><span class="sxs-lookup"><span data-stu-id="01826-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="01826-120">Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="01826-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="01826-121">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="01826-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="01826-122">**Actif** (1)</span><span class="sxs-lookup"><span data-stu-id="01826-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="01826-123">**Inactif** (2)</span><span class="sxs-lookup"><span data-stu-id="01826-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="01826-124">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="01826-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01826-125">Type de données : **Win32 \_ 1394Controller**</span><span class="sxs-lookup"><span data-stu-id="01826-125">Data type: **Win32\_1394Controller**</span></span>
</dt> <dt>

<span data-ttu-id="01826-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="01826-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01826-127">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ 1394Controller")</span><span class="sxs-lookup"><span data-stu-id="01826-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_1394Controller")</span></span>
</dt> </dl>

<span data-ttu-id="01826-128">La \_ référence antécédente Win32 1394Controller représente le contrôleur 1394 associé à cet appareil.</span><span class="sxs-lookup"><span data-stu-id="01826-128">The Win32\_1394Controller antecedent reference represents the 1394 controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="01826-129">**Charge**</span><span class="sxs-lookup"><span data-stu-id="01826-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01826-130">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="01826-130">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="01826-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="01826-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01826-132">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« CIM \| CIM \_ LogicalDevice »)</span><span class="sxs-lookup"><span data-stu-id="01826-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="01826-133">La \_ référence dépendante du LOGICALDEVICE CIM représente le \_ LogicalDevice CIM connecté au contrôleur 1394.</span><span class="sxs-lookup"><span data-stu-id="01826-133">The CIM\_LogicalDevice dependent reference represents the CIM\_LogicalDevice connected to the 1394 controller.</span></span>

</dd> <dt>

<span data-ttu-id="01826-134">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="01826-134">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01826-135">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="01826-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="01826-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="01826-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01826-137">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits »)</span><span class="sxs-lookup"><span data-stu-id="01826-137">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="01826-138">Lorsque plusieurs largeurs de données de bus ou de connexion sont possibles, cette propriété définit celle qui est utilisée entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="01826-138">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="01826-139">La largeur des données est spécifiée en bits.</span><span class="sxs-lookup"><span data-stu-id="01826-139">Data width is specified in bits.</span></span> <span data-ttu-id="01826-140">Si la largeur des données n’est pas négociée, ou si ces informations ne sont pas disponibles ou importantes pour la gestion des appareils, la propriété doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="01826-140">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="01826-141">Cette propriété est héritée de la [**\_ DeviceConnection CIM**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="01826-141">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="01826-142">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="01826-142">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01826-143">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="01826-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="01826-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="01826-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01826-145">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="01826-145">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="01826-146">Lorsque plusieurs vitesses de bus ou de connexion sont possibles, cette propriété définit celle qui est utilisée entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="01826-146">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="01826-147">La vitesse est spécifiée en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="01826-147">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="01826-148">Si les vitesses de connexion ou de bus ne sont pas négociées, ou si ces informations ne sont pas disponibles ou importantes pour la gestion des appareils, la propriété doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="01826-148">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="01826-149">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="01826-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="01826-150">Cette propriété est héritée de la [**\_ DeviceConnection CIM**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="01826-150">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="01826-151">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="01826-151">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01826-152">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="01826-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="01826-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="01826-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01826-154">Nombre de réinitialisations matérielles émises par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="01826-154">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="01826-155">Une réinitialisation matérielle retourne l’appareil à son état d’initialisation ou de démarrage.</span><span class="sxs-lookup"><span data-stu-id="01826-155">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="01826-156">Toutes les informations sur l’état de l’appareil interne et les données sont perdues.</span><span class="sxs-lookup"><span data-stu-id="01826-156">All internal device state information and data are lost.</span></span>

<span data-ttu-id="01826-157">Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="01826-157">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="01826-158">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="01826-158">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01826-159">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="01826-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="01826-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="01826-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01826-161">Nombre de réinitialisations logicielles émises par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="01826-161">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="01826-162">Une réinitialisation logicielle n’efface pas complètement l’état actuel de l’appareil et les données.</span><span class="sxs-lookup"><span data-stu-id="01826-162">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="01826-163">Les sémantiques exactes dépendent de l’appareil et des protocoles et mécanismes utilisés pour communiquer avec lui.</span><span class="sxs-lookup"><span data-stu-id="01826-163">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="01826-164">Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="01826-164">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01826-165">Notes</span><span class="sxs-lookup"><span data-stu-id="01826-165">Remarks</span></span>

<span data-ttu-id="01826-166">La classe **Win32 \_ 1394ControllerDevice** est dérivée de [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="01826-166">The **Win32\_1394ControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="examples"></a><span data-ttu-id="01826-167">Exemples</span><span class="sxs-lookup"><span data-stu-id="01826-167">Examples</span></span>

<span data-ttu-id="01826-168">L’exemple de code PowerShell suivant récupère les informations de périphérique du contrôleur 1394.</span><span class="sxs-lookup"><span data-stu-id="01826-168">The following PowerShell code sample retrieves 1394 controller device information.</span></span>


```PowerShell
# Helper function to return AccessState

function get-WmiAccessState {
param ([uint16] $char)

# parse and return values

If ($char -le 2 -and $char -ge 0) {

switch ($char) {
0 {"00-Reserved"}
1 {"01-Reserved"}
2 {"02-Unknown"}
}
}

Else {
"$char - unknown value"
}
}

# Get 1394 Controller Device information from WMI
$1394Cont = Get-WMIObject Win32_1394ControllerDevice

# Display Details
"Win32_1394ControllerDevice WMI Information"
"=========================================="

foreach ($device in $1394Cont) {

"Device Characteristics - Device {0}" -f ++$i

"Access State : {0}" -f (Get-WmiAccessState($ch))
"Antecedent : {0}" -f $device.Antecedent
"Negotiated Data Width : {0}" -f $device.NegotiatedDataWidth
"Negotiated Speed : {0}" -f $device.NegotiatedSpeed
"Number of Hard Resets : {0}" -f $device.NumberofHardResets
"Number of Soft Resets : {0}" -f $device.NumberofSoftResets
} 
```



<span data-ttu-id="01826-169">L’exemple de code précédent retourne les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="01826-169">The previous code sample returns the following information:</span></span>

``` syntax
# Win32_1394ControllerDevice WMI Information

Device Characteristics -Device 1
Access State : 00-Reserved
Antecedent : \\UK0N055\root\CIMV2:Win32_1394Controller.DeviceID="PCI\\VEN_1217&DEV_00F7&SUBSYS_01CC1028
&REV_02\\4&2FE911E8&0&0CF0"
Negotiated Data Width :
Negotiated Speed :
Number of Hard Resets :
Number of Soft Resets :
```

## <a name="requirements"></a><span data-ttu-id="01826-170">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01826-170">Requirements</span></span>



| <span data-ttu-id="01826-171">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01826-171">Requirement</span></span> | <span data-ttu-id="01826-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="01826-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01826-173">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01826-173">Minimum supported client</span></span><br/> | <span data-ttu-id="01826-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01826-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="01826-175">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01826-175">Minimum supported server</span></span><br/> | <span data-ttu-id="01826-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01826-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="01826-177">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="01826-177">Namespace</span></span><br/>                | <span data-ttu-id="01826-178">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="01826-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="01826-179">MOF</span><span class="sxs-lookup"><span data-stu-id="01826-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01826-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01826-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="01826-181">DLL</span><span class="sxs-lookup"><span data-stu-id="01826-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01826-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01826-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01826-183">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01826-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01826-184">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="01826-184">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="01826-185">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="01826-185">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

