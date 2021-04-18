---
description: La \_ classe WMI de l’Association POTSModemToSerialPort Win32 associe un modem au port série utilisé par le modem.
ms.assetid: 4dbde5ae-f785-4d2d-80d9-508effd72cf2
ms.tgt_platform: multiple
title: Classe Win32_POTSModemToSerialPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_POTSModemToSerialPort
- Win32_POTSModemToSerialPort.NegotiatedDataWidth
- Win32_POTSModemToSerialPort.NegotiatedSpeed
- Win32_POTSModemToSerialPort.AccessState
- Win32_POTSModemToSerialPort.NumberOfHardResets
- Win32_POTSModemToSerialPort.NumberOfSoftResets
- Win32_POTSModemToSerialPort.Dependent
- Win32_POTSModemToSerialPort.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0a1e6128ffde7afce0132dd4415e4eca1f06b5cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527184"
---
# <a name="win32_potsmodemtoserialport-class"></a><span data-ttu-id="ceab8-103">\_Classe POTSModemToSerialPort Win32</span><span class="sxs-lookup"><span data-stu-id="ceab8-103">Win32\_POTSModemToSerialPort class</span></span>

<span data-ttu-id="ceab8-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ POTSModemToSerialPort Win32** associe un modem au port série utilisé par le modem.</span><span class="sxs-lookup"><span data-stu-id="ceab8-104">The **Win32\_POTSModemToSerialPort** association [WMI class](../wmisdk/retrieving-a-class.md) relates a modem to the serial port the modem uses.</span></span>

<span data-ttu-id="ceab8-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ceab8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ceab8-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="ceab8-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceab8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ceab8-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B6-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_POTSModemToSerialPort : CIM_ControlledBy
{
  uint32               NegotiatedDataWidth;
  uint64               NegotiatedSpeed;
  uint16               AccessState;
  uint32               NumberOfHardResets;
  uint32               NumberOfSoftResets;
  Win32_POTSModem  REF Dependent;
  Win32_SerialPort REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="ceab8-108">Membres</span><span class="sxs-lookup"><span data-stu-id="ceab8-108">Members</span></span>

<span data-ttu-id="ceab8-109">La classe **Win32 \_ POTSModemToSerialPort** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ceab8-109">The **Win32\_POTSModemToSerialPort** class has these types of members:</span></span>

-   [<span data-ttu-id="ceab8-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ceab8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ceab8-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ceab8-111">Properties</span></span>

<span data-ttu-id="ceab8-112">La classe **Win32 \_ POTSModemToSerialPort** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ceab8-112">The **Win32\_POTSModemToSerialPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ceab8-113">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="ceab8-113">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceab8-114">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ceab8-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ceab8-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ceab8-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ceab8-116">Indique si le contrôleur commande ou accède activement à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ceab8-116">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="ceab8-117">Ces informations sont nécessaires lorsqu’un périphérique logique peut être utilisé par plusieurs contrôleurs, ou y accéder via.</span><span class="sxs-lookup"><span data-stu-id="ceab8-117">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="ceab8-118">Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="ceab8-118">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ceab8-119">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ceab8-119">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="ceab8-120">**Actif** (1)</span><span class="sxs-lookup"><span data-stu-id="ceab8-120">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="ceab8-121">**Inactif** (2)</span><span class="sxs-lookup"><span data-stu-id="ceab8-121">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ceab8-122">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="ceab8-122">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceab8-123">Type de données : **Win32 \_ SerialPort**</span><span class="sxs-lookup"><span data-stu-id="ceab8-123">Data type: **Win32\_SerialPort**</span></span>
</dt> <dt>

<span data-ttu-id="ceab8-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ceab8-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceab8-125">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SerialPort")</span><span class="sxs-lookup"><span data-stu-id="ceab8-125">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SerialPort")</span></span>
</dt> </dl>

<span data-ttu-id="ceab8-126">Un [**\_ SerialPort Win32**](win32-serialport.md) qui représente le port série utilisé par le modem.</span><span class="sxs-lookup"><span data-stu-id="ceab8-126">A [**Win32\_SerialPort**](win32-serialport.md) that represents the serial port used by the modem.</span></span>

</dd> <dt>

<span data-ttu-id="ceab8-127">**Charge**</span><span class="sxs-lookup"><span data-stu-id="ceab8-127">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceab8-128">Type de données : **Win32 \_ POTSModem**</span><span class="sxs-lookup"><span data-stu-id="ceab8-128">Data type: **Win32\_POTSModem**</span></span>
</dt> <dt>

<span data-ttu-id="ceab8-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ceab8-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceab8-130">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) (« dépendant »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI \| Win32 \_ POTSModem »)</span><span class="sxs-lookup"><span data-stu-id="ceab8-130">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_POTSModem")</span></span>
</dt> </dl>

<span data-ttu-id="ceab8-131">[**\_ POTSModem Win32**](win32-potsmodem.md) qui représente le modem pots utilisant le port série.</span><span class="sxs-lookup"><span data-stu-id="ceab8-131">A [**Win32\_POTSModem**](win32-potsmodem.md) that represents the POTS modem using the serial port.</span></span>

</dd> <dt>

<span data-ttu-id="ceab8-132">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="ceab8-132">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceab8-133">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ceab8-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ceab8-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ceab8-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceab8-135">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« bits »)</span><span class="sxs-lookup"><span data-stu-id="ceab8-135">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="ceab8-136">Lorsque plusieurs largeurs de données de bus ou de connexion sont possibles, cette propriété définit celle qui est utilisée entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="ceab8-136">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="ceab8-137">La largeur des données est spécifiée en bits.</span><span class="sxs-lookup"><span data-stu-id="ceab8-137">Data width is specified in bits.</span></span> <span data-ttu-id="ceab8-138">Si la largeur des données n’est pas négociée, ou si ces informations ne sont pas disponibles ou importantes pour la gestion des appareils, la propriété doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="ceab8-138">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="ceab8-139">Cette propriété est héritée de la [**\_ DeviceConnection CIM**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="ceab8-139">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceab8-140">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="ceab8-140">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceab8-141">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ceab8-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ceab8-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ceab8-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceab8-143">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="ceab8-143">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="ceab8-144">Lorsque plusieurs vitesses de bus ou de connexion sont possibles, cette propriété définit celle qui est utilisée entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="ceab8-144">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="ceab8-145">La vitesse est spécifiée en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="ceab8-145">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="ceab8-146">Si les vitesses de connexion ou de bus ne sont pas négociées, ou si ces informations ne sont pas disponibles ou importantes pour la gestion des appareils, la propriété doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="ceab8-146">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="ceab8-147">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ceab8-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="ceab8-148">Cette propriété est héritée de la [**\_ DeviceConnection CIM**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="ceab8-148">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceab8-149">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="ceab8-149">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceab8-150">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ceab8-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ceab8-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ceab8-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ceab8-152">Nombre de réinitialisations matérielles émises par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="ceab8-152">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="ceab8-153">Une réinitialisation matérielle retourne l’appareil à son état d’initialisation ou de démarrage.</span><span class="sxs-lookup"><span data-stu-id="ceab8-153">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="ceab8-154">Toutes les informations sur l’état de l’appareil interne et les données sont perdues.</span><span class="sxs-lookup"><span data-stu-id="ceab8-154">All internal device state information and data are lost.</span></span>

<span data-ttu-id="ceab8-155">Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="ceab8-155">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceab8-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="ceab8-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceab8-157">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ceab8-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ceab8-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ceab8-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ceab8-159">Nombre de réinitialisations logicielles émises par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="ceab8-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="ceab8-160">Une réinitialisation logicielle n’efface pas complètement l’état actuel de l’appareil et les données.</span><span class="sxs-lookup"><span data-stu-id="ceab8-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="ceab8-161">Les sémantiques exactes dépendent de l’appareil et des protocoles et mécanismes utilisés pour communiquer avec lui.</span><span class="sxs-lookup"><span data-stu-id="ceab8-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="ceab8-162">Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="ceab8-162">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ceab8-163">Notes</span><span class="sxs-lookup"><span data-stu-id="ceab8-163">Remarks</span></span>

<span data-ttu-id="ceab8-164">La classe **Win32 \_ POTSModemToSerialPort** est dérivée de [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="ceab8-164">The **Win32\_POTSModemToSerialPort** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ceab8-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ceab8-165">Requirements</span></span>



| <span data-ttu-id="ceab8-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ceab8-166">Requirement</span></span> | <span data-ttu-id="ceab8-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="ceab8-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ceab8-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ceab8-168">Minimum supported client</span></span><br/> | <span data-ttu-id="ceab8-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ceab8-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ceab8-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ceab8-170">Minimum supported server</span></span><br/> | <span data-ttu-id="ceab8-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ceab8-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ceab8-172">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ceab8-172">Namespace</span></span><br/>                | <span data-ttu-id="ceab8-173">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ceab8-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ceab8-174">MOF</span><span class="sxs-lookup"><span data-stu-id="ceab8-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ceab8-175"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ceab8-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ceab8-176">DLL</span><span class="sxs-lookup"><span data-stu-id="ceab8-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ceab8-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ceab8-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ceab8-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ceab8-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceab8-179">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="ceab8-179">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="ceab8-180">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="ceab8-180">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
