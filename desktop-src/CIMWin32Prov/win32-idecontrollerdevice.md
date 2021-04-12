---
description: La \_ classe WMI de l’Association IDEControllerDevice Win32 associe un contrôleur IDE (Integrated Drive Electronics) et l’appareil logique connecté à, par exemple, à un lecteur de disque.
ms.assetid: 1b0a551c-d836-4147-91ed-a0a7d97f4a5b
ms.tgt_platform: multiple
title: Classe Win32_IDEControllerDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_IDEControllerDevice
- Win32_IDEControllerDevice.NegotiatedDataWidth
- Win32_IDEControllerDevice.NegotiatedSpeed
- Win32_IDEControllerDevice.AccessState
- Win32_IDEControllerDevice.NumberOfHardResets
- Win32_IDEControllerDevice.NumberOfSoftResets
- Win32_IDEControllerDevice.Antecedent
- Win32_IDEControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc690aadd442d656132b2d9e4539cc27961c3ef9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393199"
---
# <a name="win32_idecontrollerdevice-class"></a><span data-ttu-id="6ad30-103">\_Classe IDEControllerDevice Win32</span><span class="sxs-lookup"><span data-stu-id="6ad30-103">Win32\_IDEControllerDevice class</span></span>

<span data-ttu-id="6ad30-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ IDEControllerDevice Win32** associe un contrôleur IDE (Integrated Drive Electronics) et l’appareil logique connecté à, par exemple, à un lecteur de disque.</span><span class="sxs-lookup"><span data-stu-id="6ad30-104">The **Win32\_IDEControllerDevice** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates an Integrated Drive Electronics (IDE) controller and the logical device connected to, for example, a disk drive.</span></span>

<span data-ttu-id="6ad30-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6ad30-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6ad30-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="6ad30-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ad30-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ad30-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{5BC42B62-C7A1-11d2-911D-0060081A46FD}"), AMENDMENT]
class Win32_IDEControllerDevice : CIM_ControlledBy
{
  uint32                  NegotiatedDataWidth;
  uint64                  NegotiatedSpeed;
  uint16                  AccessState;
  uint32                  NumberOfHardResets;
  uint32                  NumberOfSoftResets;
  Win32_IDEController REF Antecedent;
  CIM_LogicalDevice   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6ad30-108">Membres</span><span class="sxs-lookup"><span data-stu-id="6ad30-108">Members</span></span>

<span data-ttu-id="6ad30-109">La classe **Win32 \_ IDEControllerDevice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6ad30-109">The **Win32\_IDEControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="6ad30-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6ad30-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6ad30-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6ad30-111">Properties</span></span>

<span data-ttu-id="6ad30-112">La classe **Win32 \_ IDEControllerDevice** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6ad30-112">The **Win32\_IDEControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6ad30-113">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="6ad30-113">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ad30-114">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6ad30-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6ad30-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6ad30-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ad30-116">Indique si le contrôleur commande ou accède activement à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6ad30-116">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="6ad30-117">Ces informations sont nécessaires lorsqu’un périphérique logique peut être utilisé par plusieurs contrôleurs, ou y accéder via.</span><span class="sxs-lookup"><span data-stu-id="6ad30-117">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="6ad30-118">Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="6ad30-118">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6ad30-119">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="6ad30-119">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="6ad30-120">**Actif** (1)</span><span class="sxs-lookup"><span data-stu-id="6ad30-120">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="6ad30-121">**Inactif** (2)</span><span class="sxs-lookup"><span data-stu-id="6ad30-121">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6ad30-122">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="6ad30-122">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ad30-123">Type de données : **Win32 \_ IDEController**</span><span class="sxs-lookup"><span data-stu-id="6ad30-123">Data type: **Win32\_IDEController**</span></span>
</dt> <dt>

<span data-ttu-id="6ad30-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6ad30-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ad30-125">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| Win32 \_ IDEController")</span><span class="sxs-lookup"><span data-stu-id="6ad30-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|Win32\_IDEController")</span></span>
</dt> </dl>

<span data-ttu-id="6ad30-126">[**\_ IDEController Win32**](win32-idecontroller.md) qui représente le contrôleur IDE associé à cet appareil.</span><span class="sxs-lookup"><span data-stu-id="6ad30-126">A [**Win32\_IDEController**](win32-idecontroller.md) that represents the IDE controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="6ad30-127">**Charge**</span><span class="sxs-lookup"><span data-stu-id="6ad30-127">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ad30-128">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="6ad30-128">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="6ad30-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6ad30-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ad30-130">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« CIM \| CIM \_ LogicalDevice »)</span><span class="sxs-lookup"><span data-stu-id="6ad30-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="6ad30-131">[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui représente l’appareil logique connecté au contrôleur IDE.</span><span class="sxs-lookup"><span data-stu-id="6ad30-131">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the logical device connected to the IDE controller.</span></span>

</dd> <dt>

<span data-ttu-id="6ad30-132">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="6ad30-132">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ad30-133">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ad30-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ad30-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6ad30-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ad30-135">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits »)</span><span class="sxs-lookup"><span data-stu-id="6ad30-135">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="6ad30-136">Lorsque plusieurs largeurs de données de bus ou de connexion sont possibles, cette propriété définit celle qui est utilisée entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="6ad30-136">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="6ad30-137">La largeur des données est spécifiée en bits.</span><span class="sxs-lookup"><span data-stu-id="6ad30-137">Data width is specified in bits.</span></span> <span data-ttu-id="6ad30-138">Si la largeur des données n’est pas négociée, ou si ces informations ne sont pas disponibles ou importantes pour la gestion des appareils, la propriété doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="6ad30-138">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="6ad30-139">Cette propriété est héritée de la [**\_ DeviceConnection CIM**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="6ad30-139">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ad30-140">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="6ad30-140">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ad30-141">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6ad30-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6ad30-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6ad30-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ad30-143">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="6ad30-143">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="6ad30-144">Lorsque plusieurs vitesses de bus ou de connexion sont possibles, cette propriété définit celle qui est utilisée entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="6ad30-144">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="6ad30-145">La vitesse est spécifiée en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="6ad30-145">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="6ad30-146">Si les vitesses de connexion ou de bus ne sont pas négociées, ou si ces informations ne sont pas disponibles ou importantes pour la gestion des appareils, la propriété doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="6ad30-146">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="6ad30-147">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6ad30-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="6ad30-148">Cette propriété est héritée de la [**\_ DeviceConnection CIM**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="6ad30-148">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ad30-149">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="6ad30-149">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ad30-150">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ad30-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ad30-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6ad30-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ad30-152">Nombre de réinitialisations matérielles émises par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="6ad30-152">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="6ad30-153">Une réinitialisation matérielle retourne l’appareil à son état d’initialisation ou de démarrage.</span><span class="sxs-lookup"><span data-stu-id="6ad30-153">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="6ad30-154">Toutes les informations sur l’état de l’appareil interne et les données sont perdues.</span><span class="sxs-lookup"><span data-stu-id="6ad30-154">All internal device state information and data are lost.</span></span>

<span data-ttu-id="6ad30-155">Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="6ad30-155">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ad30-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="6ad30-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ad30-157">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ad30-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ad30-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6ad30-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ad30-159">Nombre de réinitialisations logicielles émises par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="6ad30-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="6ad30-160">Une réinitialisation logicielle n’efface pas complètement l’état actuel de l’appareil et les données.</span><span class="sxs-lookup"><span data-stu-id="6ad30-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="6ad30-161">Les sémantiques exactes dépendent de l’appareil et des protocoles et mécanismes utilisés pour communiquer avec lui.</span><span class="sxs-lookup"><span data-stu-id="6ad30-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="6ad30-162">Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="6ad30-162">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ad30-163">Notes</span><span class="sxs-lookup"><span data-stu-id="6ad30-163">Remarks</span></span>

<span data-ttu-id="6ad30-164">La classe **Win32 \_ IDEControllerDevice** est dérivée de [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="6ad30-164">The **Win32\_IDEControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ad30-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ad30-165">Requirements</span></span>



| <span data-ttu-id="6ad30-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ad30-166">Requirement</span></span> | <span data-ttu-id="6ad30-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ad30-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ad30-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ad30-168">Minimum supported client</span></span><br/> | <span data-ttu-id="6ad30-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ad30-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6ad30-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ad30-170">Minimum supported server</span></span><br/> | <span data-ttu-id="6ad30-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ad30-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6ad30-172">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6ad30-172">Namespace</span></span><br/>                | <span data-ttu-id="6ad30-173">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="6ad30-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6ad30-174">MOF</span><span class="sxs-lookup"><span data-stu-id="6ad30-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ad30-175"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ad30-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ad30-176">DLL</span><span class="sxs-lookup"><span data-stu-id="6ad30-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ad30-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ad30-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ad30-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ad30-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ad30-179">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="6ad30-179">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="6ad30-180">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="6ad30-180">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

