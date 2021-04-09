---
description: La \_ classe WMI de l’Association PrinterController Win32 associe une imprimante et l’appareil local auquel l’imprimante est connectée. Notez que cette classe retourne uniquement des instances pour les imprimantes locales.
ms.assetid: fb483b28-11f1-4153-893e-492f71763712
ms.tgt_platform: multiple
title: Classe Win32_PrinterController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterController
- Win32_PrinterController.AccessState
- Win32_PrinterController.Antecedent
- Win32_PrinterController.Dependent
- Win32_PrinterController.NegotiatedDataWidth
- Win32_PrinterController.NegotiatedSpeed
- Win32_PrinterController.NumberOfHardResets
- Win32_PrinterController.NumberOfSoftResets
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ee38b827aed2dfffe1e7ef4f5049b16eee50791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861178"
---
# <a name="win32_printercontroller-class"></a><span data-ttu-id="273e4-104">\_Classe PrinterController Win32</span><span class="sxs-lookup"><span data-stu-id="273e4-104">Win32\_PrinterController class</span></span>

<span data-ttu-id="273e4-105">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ PrinterController Win32** associe une imprimante et l’appareil local auquel l’imprimante est connectée.</span><span class="sxs-lookup"><span data-stu-id="273e4-105">The **Win32\_PrinterController** association [WMI class](../wmisdk/retrieving-a-class.md) relates a printer and the local device to which the printer is connected.</span></span> <span data-ttu-id="273e4-106">Notez que cette classe retourne uniquement des instances pour les imprimantes locales.</span><span class="sxs-lookup"><span data-stu-id="273e4-106">Note that this class only returns instances for local printers.</span></span>

<span data-ttu-id="273e4-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="273e4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="273e4-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="273e4-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="273e4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="273e4-109">Syntax</span></span>

``` syntax
class Win32_PrinterController : CIM_ControlledBy
{
  uint16             AccessState;
  CIM_Controller REF Antecedent;
  Win32_Printer  REF Dependent;
  uint32             NegotiatedDataWidth;
  uint64             NegotiatedSpeed;
  uint32             NumberOfHardResets;
  uint32             NumberOfSoftResets;
};
```

## <a name="members"></a><span data-ttu-id="273e4-110">Membres</span><span class="sxs-lookup"><span data-stu-id="273e4-110">Members</span></span>

<span data-ttu-id="273e4-111">La classe **Win32 \_ PrinterController** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="273e4-111">The **Win32\_PrinterController** class has these types of members:</span></span>

-   [<span data-ttu-id="273e4-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="273e4-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="273e4-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="273e4-113">Properties</span></span>

<span data-ttu-id="273e4-114">La classe **Win32 \_ PrinterController** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="273e4-114">The **Win32\_PrinterController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="273e4-115">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="273e4-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273e4-116">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="273e4-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="273e4-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="273e4-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273e4-118">État de l’accès du contrôleur à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="273e4-118">State of the controller access to the device.</span></span> <span data-ttu-id="273e4-119">Ces informations sont nécessaires lorsqu’un périphérique logique peut être utilisé par plusieurs contrôleurs, ou y accéder via.</span><span class="sxs-lookup"><span data-stu-id="273e4-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="273e4-120">Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="273e4-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="273e4-121"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="273e4-121"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="273e4-122">Unknown</span><span class="sxs-lookup"><span data-stu-id="273e4-122">Unknown</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="273e4-123"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="273e4-123"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="273e4-124">Actif</span><span class="sxs-lookup"><span data-stu-id="273e4-124">Active</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="273e4-125"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="273e4-125"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="273e4-126">Inactif</span><span class="sxs-lookup"><span data-stu-id="273e4-126">Inactive</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="273e4-127">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="273e4-127">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273e4-128">Type de données **: \_ contrôleur CIM**</span><span class="sxs-lookup"><span data-stu-id="273e4-128">Data type: **CIM\_Controller**</span></span>
</dt> <dt>

<span data-ttu-id="273e4-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="273e4-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="273e4-130">Qualificateurs : [ **clé**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="273e4-130">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="273e4-131">Référence à l’instance de [**\_ contrôleur CIM**](cim-controller.md) représentant l’appareil local associé à cette imprimante.</span><span class="sxs-lookup"><span data-stu-id="273e4-131">Reference to the [**CIM\_Controller**](cim-controller.md) instance representing the local device associated with this printer.</span></span>

<span data-ttu-id="273e4-132">Cette propriété est héritée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="273e4-132">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="273e4-133">**Charge**</span><span class="sxs-lookup"><span data-stu-id="273e4-133">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273e4-134">Type de données **: \_ imprimante Win32**</span><span class="sxs-lookup"><span data-stu-id="273e4-134">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="273e4-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="273e4-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="273e4-136">Qualificateurs : [ **clé**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="273e4-136">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="273e4-137">Référence à l’instance d' [**\_ imprimante Win32**](win32-printer.md) représentant l’imprimante associée à l’appareil local.</span><span class="sxs-lookup"><span data-stu-id="273e4-137">Reference to the [**Win32\_Printer**](win32-printer.md) instance representing the printer associated with the local device.</span></span>

<span data-ttu-id="273e4-138">Cette propriété est héritée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="273e4-138">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="273e4-139">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="273e4-139">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273e4-140">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="273e4-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="273e4-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="273e4-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273e4-142">Largeur des données en cours d’utilisation entre les appareils (lorsque plusieurs largeurs de données de bus ou de connexion sont possibles).</span><span class="sxs-lookup"><span data-stu-id="273e4-142">Data width in use between devices (when several bus or connection data widths are possible).</span></span> <span data-ttu-id="273e4-143">La largeur des données est spécifiée en bits.</span><span class="sxs-lookup"><span data-stu-id="273e4-143">Data width is specified in bits.</span></span> <span data-ttu-id="273e4-144">Si la largeur des données n’est pas négociée, ou si ces informations ne sont pas disponibles ou importantes pour la gestion des appareils, la propriété doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="273e4-144">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="273e4-145">Cette propriété est héritée de la [**\_ DeviceConnection CIM**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="273e4-145">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="273e4-146">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="273e4-146">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273e4-147">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="273e4-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="273e4-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="273e4-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273e4-149">Vitesse d’utilisation entre les appareils (lorsque plusieurs vitesses de bus ou de connexion sont possibles).</span><span class="sxs-lookup"><span data-stu-id="273e4-149">Speed in use between devices (when several bus or connection speeds are possible).</span></span> <span data-ttu-id="273e4-150">La vitesse est spécifiée en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="273e4-150">Speed is specified in bits per second.</span></span> <span data-ttu-id="273e4-151">Si les vitesses de connexion ou de bus ne sont pas négociées, ou si ces informations ne sont pas disponibles ou importantes pour la gestion des appareils, la propriété doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="273e4-151">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="273e4-152">Cette propriété est héritée de la [**\_ DeviceConnection CIM**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="273e4-152">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

<span data-ttu-id="273e4-153">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="273e4-153">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="273e4-154">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="273e4-154">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273e4-155">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="273e4-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="273e4-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="273e4-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273e4-157">Nombre de réinitialisations matérielles émises par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="273e4-157">Number of hard resets issued by the controller.</span></span>

<span data-ttu-id="273e4-158">Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="273e4-158">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="273e4-159">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="273e4-159">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="273e4-160">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="273e4-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="273e4-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="273e4-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="273e4-162">Nombre de réinitialisations logicielles émises par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="273e4-162">Number of soft resets issued by the controller.</span></span>

<span data-ttu-id="273e4-163">Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="273e4-163">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="273e4-164">Notes</span><span class="sxs-lookup"><span data-stu-id="273e4-164">Remarks</span></span>

<span data-ttu-id="273e4-165">La classe **Win32 \_ PrinterController** est dérivée de [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="273e4-165">The **Win32\_PrinterController** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="273e4-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="273e4-166">Requirements</span></span>



| <span data-ttu-id="273e4-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="273e4-167">Requirement</span></span> | <span data-ttu-id="273e4-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="273e4-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="273e4-169">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="273e4-169">Minimum supported client</span></span><br/> | <span data-ttu-id="273e4-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="273e4-170">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="273e4-171">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="273e4-171">Minimum supported server</span></span><br/> | <span data-ttu-id="273e4-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="273e4-172">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="273e4-173">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="273e4-173">Namespace</span></span><br/>                | <span data-ttu-id="273e4-174">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="273e4-174">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="273e4-175">MOF</span><span class="sxs-lookup"><span data-stu-id="273e4-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="273e4-176"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="273e4-176"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="273e4-177">DLL</span><span class="sxs-lookup"><span data-stu-id="273e4-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="273e4-178"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="273e4-178"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="273e4-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="273e4-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="273e4-180">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="273e4-180">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="273e4-181">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="273e4-181">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
