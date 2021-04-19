---
description: Associe un appareil de stockage au contrôleur de stockage qui possède l’appareil.
ms.assetid: 3DE05EDC-C54A-4C3C-9057-4418246037D5
title: Classe Msvm_ControlledBy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ControlledBy
- Msvm_ControlledBy.NegotiatedSpeed
- Msvm_ControlledBy.NegotiatedDataWidth
- Msvm_ControlledBy.Antecedent
- Msvm_ControlledBy.Dependent
- Msvm_ControlledBy.AccessState
- Msvm_ControlledBy.TimeOfDeviceReset
- Msvm_ControlledBy.NumberOfHardResets
- Msvm_ControlledBy.NumberOfSoftResets
- Msvm_ControlledBy.DeviceNumber
- Msvm_ControlledBy.AccessMode
- Msvm_ControlledBy.AccessPriority
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7986ffb842f7a1a104a0a8d846c1b6ee47a21523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530720"
---
# <a name="msvm_controlledby-class"></a><span data-ttu-id="c90f5-103">MSVM \_ ControlledBy, classe</span><span class="sxs-lookup"><span data-stu-id="c90f5-103">Msvm\_ControlledBy class</span></span>

<span data-ttu-id="c90f5-104">Associe un appareil de stockage au contrôleur de stockage qui possède l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c90f5-104">Associates a storage device with the storage controller that owns the device.</span></span> <span data-ttu-id="c90f5-105">Cette association est utilisée avec les contrôleurs de disque et IDE.</span><span class="sxs-lookup"><span data-stu-id="c90f5-105">This association is used with both IDE and floppy controllers.</span></span>

<span data-ttu-id="c90f5-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c90f5-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c90f5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c90f5-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ControlledBy : CIM_ControlledBy
{
  uint64                NegotiatedSpeed = 0;
  uint32                NegotiatedDataWidth = 0;
  CIM_Controller    REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint16                AccessState = 1;
  datetime              TimeOfDeviceReset;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  string                DeviceNumber;
  uint16                AccessMode = 2;
  uint16                AccessPriority = 0;
};
```

## <a name="members"></a><span data-ttu-id="c90f5-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c90f5-108">Members</span></span>

<span data-ttu-id="c90f5-109">La classe **MSVM \_ ControlledBy** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c90f5-109">The **Msvm\_ControlledBy** class has these types of members:</span></span>

-   [<span data-ttu-id="c90f5-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c90f5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c90f5-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c90f5-111">Properties</span></span>

<span data-ttu-id="c90f5-112">La classe **MSVM \_ ControlledBy** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c90f5-112">The **Msvm\_ControlledBy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c90f5-113">**AccessMode**</span><span class="sxs-lookup"><span data-stu-id="c90f5-113">**AccessMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c90f5-114">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c90f5-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c90f5-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c90f5-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c90f5-116">Accessibilité de l’appareil via le contrôleur antécédent.</span><span class="sxs-lookup"><span data-stu-id="c90f5-116">The accessibility of the device through the antecedent controller.</span></span> <span data-ttu-id="c90f5-117">Cette propriété est héritée de la [**\_ ControlledBy CIM**](/windows/desktop/CIMWin32Prov/cim-controlledby)et est toujours définie sur 2 (lecture/écriture).</span><span class="sxs-lookup"><span data-stu-id="c90f5-117">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), and it is always set to 2 (read/write).</span></span>

</dd> <dt>

<span data-ttu-id="c90f5-118">**AccessPriority**</span><span class="sxs-lookup"><span data-stu-id="c90f5-118">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c90f5-119">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c90f5-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c90f5-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c90f5-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c90f5-121">Priorité donnée aux accès de l’appareil par le biais de ce contrôleur.</span><span class="sxs-lookup"><span data-stu-id="c90f5-121">The priority given to accesses of the device through this controller.</span></span> <span data-ttu-id="c90f5-122">Le chemin d’accès avec la priorité la plus élevée aura la valeur la plus faible.</span><span class="sxs-lookup"><span data-stu-id="c90f5-122">The highest priority path will have the lowest value.</span></span> <span data-ttu-id="c90f5-123">Cette propriété est héritée de [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)et est toujours définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="c90f5-123">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="c90f5-124">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="c90f5-124">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c90f5-125">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c90f5-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c90f5-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c90f5-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c90f5-127">Indique si le contrôleur commande ou accède activement à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c90f5-127">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="c90f5-128">Cette propriété est héritée de [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)et est toujours définie sur 1 (active).</span><span class="sxs-lookup"><span data-stu-id="c90f5-128">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), and it is always set to 1 (Active).</span></span>

</dd> <dt>

<span data-ttu-id="c90f5-129">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="c90f5-129">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c90f5-130">Type de données : **[ **\_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller)**</span><span class="sxs-lookup"><span data-stu-id="c90f5-130">Data type: **[**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller)**</span></span>
</dt> <dt>

<span data-ttu-id="c90f5-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c90f5-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c90f5-132">Référence au contrôleur.</span><span class="sxs-lookup"><span data-stu-id="c90f5-132">A reference to the controller.</span></span> <span data-ttu-id="c90f5-133">Cette propriété est héritée de la [**\_ ControlledBy CIM**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span><span class="sxs-lookup"><span data-stu-id="c90f5-133">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span></span>

</dd> <dt>

<span data-ttu-id="c90f5-134">**Charge**</span><span class="sxs-lookup"><span data-stu-id="c90f5-134">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c90f5-135">Type de données : **[ **\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="c90f5-135">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="c90f5-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c90f5-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c90f5-137">Référence à l’appareil contrôlé.</span><span class="sxs-lookup"><span data-stu-id="c90f5-137">A reference to the controlled device.</span></span> <span data-ttu-id="c90f5-138">Cette propriété est héritée de la [**\_ ControlledBy CIM**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span><span class="sxs-lookup"><span data-stu-id="c90f5-138">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span></span>

</dd> <dt>

<span data-ttu-id="c90f5-139">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="c90f5-139">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c90f5-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c90f5-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c90f5-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c90f5-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c90f5-142">Adresse de l’appareil associé dans le contexte du contrôleur antécédent.</span><span class="sxs-lookup"><span data-stu-id="c90f5-142">The address of the associated device in the context of the antecedent controller.</span></span> <span data-ttu-id="c90f5-143">Cette propriété est héritée de la [**\_ ControlledBy CIM**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span><span class="sxs-lookup"><span data-stu-id="c90f5-143">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span></span>

</dd> <dt>

<span data-ttu-id="c90f5-144">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="c90f5-144">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c90f5-145">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c90f5-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c90f5-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c90f5-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c90f5-147">Cette propriété est héritée de [**CIM \_ DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)et est toujours définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="c90f5-147">This property is inherited from [**CIM\_DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="c90f5-148">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="c90f5-148">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c90f5-149">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c90f5-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c90f5-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c90f5-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c90f5-151">Cette propriété est héritée de [**CIM \_ DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)et est toujours définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="c90f5-151">This property is inherited from [**CIM\_DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="c90f5-152">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="c90f5-152">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c90f5-153">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c90f5-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c90f5-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c90f5-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c90f5-155">Cette propriété est héritée de [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c90f5-155">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c90f5-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="c90f5-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c90f5-157">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c90f5-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c90f5-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c90f5-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c90f5-159">Cette propriété est héritée de [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c90f5-159">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c90f5-160">**TimeOfDeviceReset**</span><span class="sxs-lookup"><span data-stu-id="c90f5-160">**TimeOfDeviceReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c90f5-161">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c90f5-161">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c90f5-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c90f5-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c90f5-163">Cette propriété est héritée de [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c90f5-163">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c90f5-164">Notes</span><span class="sxs-lookup"><span data-stu-id="c90f5-164">Remarks</span></span>

<span data-ttu-id="c90f5-165">L’accès à la classe **MSVM \_ ControlledBy** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="c90f5-165">Access to the **Msvm\_ControlledBy** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c90f5-166">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c90f5-166">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c90f5-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c90f5-167">Requirements</span></span>



| <span data-ttu-id="c90f5-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c90f5-168">Requirement</span></span> | <span data-ttu-id="c90f5-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="c90f5-169">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c90f5-170">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c90f5-170">Minimum supported client</span></span><br/> | <span data-ttu-id="c90f5-171">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c90f5-171">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c90f5-172">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c90f5-172">Minimum supported server</span></span><br/> | <span data-ttu-id="c90f5-173">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c90f5-173">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c90f5-174">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c90f5-174">Namespace</span></span><br/>                | <span data-ttu-id="c90f5-175">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c90f5-175">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c90f5-176">MOF</span><span class="sxs-lookup"><span data-stu-id="c90f5-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c90f5-177"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c90f5-177"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c90f5-178">DLL</span><span class="sxs-lookup"><span data-stu-id="c90f5-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c90f5-179"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c90f5-179"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c90f5-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c90f5-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c90f5-181">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="c90f5-181">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="c90f5-182">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="c90f5-182">**CIM\_ControlledBy**</span></span>](/windows/desktop/CIMWin32Prov/cim-controlledby)
</dt> <dt>

[<span data-ttu-id="c90f5-183">Classes de stockage</span><span class="sxs-lookup"><span data-stu-id="c90f5-183">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

