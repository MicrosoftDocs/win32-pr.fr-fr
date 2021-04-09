---
description: La \_ classe CIM USBControllerHasHub définit les hubs en aval du contrôleur USB.
ms.assetid: 38bc0342-3ff0-42c8-9c1e-ea5a5822e1d3
ms.tgt_platform: multiple
title: Classe CIM_USBControllerHasHub
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBControllerHasHub
- CIM_USBControllerHasHub.NegotiatedDataWidth
- CIM_USBControllerHasHub.NegotiatedSpeed
- CIM_USBControllerHasHub.AccessState
- CIM_USBControllerHasHub.NumberOfHardResets
- CIM_USBControllerHasHub.NumberOfSoftResets
- CIM_USBControllerHasHub.Dependent
- CIM_USBControllerHasHub.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ba0f6d9a618a194faa8d16f9b2f53c6ce10653cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110051"
---
# <a name="cim_usbcontrollerhashub-class"></a><span data-ttu-id="abc46-103">\_Classe CIM USBControllerHasHub</span><span class="sxs-lookup"><span data-stu-id="abc46-103">CIM\_USBControllerHasHub class</span></span>

<span data-ttu-id="abc46-104">La classe **CIM \_ USBControllerHasHub** définit les hubs en aval du contrôleur USB.</span><span class="sxs-lookup"><span data-stu-id="abc46-104">The **CIM\_USBControllerHasHub** class defines the hubs that are downstream of the USB controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="abc46-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="abc46-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="abc46-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="abc46-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="abc46-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="abc46-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="abc46-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="abc46-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="abc46-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="abc46-109">Syntax</span></span>

``` syntax
[AMENDMENT]
class CIM_USBControllerHasHub : CIM_ControlledBy
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  CIM_USBHub        REF Dependent;
  CIM_USBController REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="abc46-110">Membres</span><span class="sxs-lookup"><span data-stu-id="abc46-110">Members</span></span>

<span data-ttu-id="abc46-111">La classe **CIM \_ USBControllerHasHub** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="abc46-111">The **CIM\_USBControllerHasHub** class has these types of members:</span></span>

-   [<span data-ttu-id="abc46-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="abc46-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="abc46-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="abc46-113">Properties</span></span>

<span data-ttu-id="abc46-114">La classe **CIM \_ USBControllerHasHub** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="abc46-114">The **CIM\_USBControllerHasHub** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="abc46-115">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="abc46-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abc46-116">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="abc46-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="abc46-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abc46-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abc46-118">Indique si le contrôleur commande ou accède activement à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="abc46-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="abc46-119">Ces informations sont nécessaires lorsqu’un périphérique logique peut être utilisé par plusieurs contrôleurs, ou y accéder via.</span><span class="sxs-lookup"><span data-stu-id="abc46-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="abc46-120">Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="abc46-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="abc46-121">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="abc46-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="abc46-122">**Actif** (1)</span><span class="sxs-lookup"><span data-stu-id="abc46-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="abc46-123">**Inactif** (2)</span><span class="sxs-lookup"><span data-stu-id="abc46-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="abc46-124">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="abc46-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abc46-125">Type de données : **CIM \_ USBController**</span><span class="sxs-lookup"><span data-stu-id="abc46-125">Data type: **CIM\_USBController**</span></span>
</dt> <dt>

<span data-ttu-id="abc46-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abc46-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abc46-127">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="abc46-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="abc46-128">[**\_ USBController CIM**](cim-usbcontroller.md) décrivant USBController.</span><span class="sxs-lookup"><span data-stu-id="abc46-128">A [**CIM\_USBController**](cim-usbcontroller.md) describing the USBController.</span></span>

</dd> <dt>

<span data-ttu-id="abc46-129">**Charge**</span><span class="sxs-lookup"><span data-stu-id="abc46-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abc46-130">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="abc46-130">Data type: **CIM\_USBHub**</span></span>
</dt> <dt>

<span data-ttu-id="abc46-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abc46-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abc46-132">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="abc46-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="abc46-133">Un [**\_ Usbhub CIM**](cim-usbhub.md) décrivant l’Usbhub qui est associé au contrôleur.</span><span class="sxs-lookup"><span data-stu-id="abc46-133">A [**CIM\_USBHub**](cim-usbhub.md) describing the USBHub that is associated with the Controller.</span></span>

</dd> <dt>

<span data-ttu-id="abc46-134">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="abc46-134">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abc46-135">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="abc46-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="abc46-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abc46-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abc46-137">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits »)</span><span class="sxs-lookup"><span data-stu-id="abc46-137">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="abc46-138">Lorsque plusieurs largeurs de données de bus ou de connexion sont possibles, cette propriété définit celle qui est utilisée entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="abc46-138">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="abc46-139">La largeur des données est spécifiée en bits.</span><span class="sxs-lookup"><span data-stu-id="abc46-139">Data width is specified in bits.</span></span> <span data-ttu-id="abc46-140">Si la largeur des données n’est pas négociée, ou si ces informations ne sont pas disponibles ou importantes pour la gestion des appareils, la propriété doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="abc46-140">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="abc46-141">Cette propriété est héritée de la [**\_ DeviceConnection CIM**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="abc46-141">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="abc46-142">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="abc46-142">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abc46-143">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="abc46-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="abc46-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abc46-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abc46-145">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="abc46-145">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="abc46-146">Lorsque plusieurs vitesses de bus ou de connexion sont possibles, cette propriété définit celle qui est utilisée entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="abc46-146">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="abc46-147">La vitesse est spécifiée en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="abc46-147">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="abc46-148">Si les vitesses de connexion ou de bus ne sont pas négociées, ou si ces informations ne sont pas disponibles ou importantes pour la gestion des appareils, la propriété doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="abc46-148">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="abc46-149">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="abc46-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="abc46-150">Cette propriété est héritée de la [**\_ DeviceConnection CIM**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="abc46-150">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="abc46-151">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="abc46-151">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abc46-152">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="abc46-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="abc46-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abc46-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abc46-154">Nombre de réinitialisations matérielles émises par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="abc46-154">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="abc46-155">Une réinitialisation matérielle retourne l’appareil à son état d’initialisation ou de démarrage.</span><span class="sxs-lookup"><span data-stu-id="abc46-155">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="abc46-156">Toutes les informations sur l’état de l’appareil interne et les données sont perdues.</span><span class="sxs-lookup"><span data-stu-id="abc46-156">All internal device state information and data are lost.</span></span>

<span data-ttu-id="abc46-157">Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="abc46-157">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="abc46-158">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="abc46-158">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abc46-159">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="abc46-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="abc46-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abc46-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abc46-161">Nombre de réinitialisations logicielles émises par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="abc46-161">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="abc46-162">Une réinitialisation logicielle n’efface pas complètement l’état actuel de l’appareil et les données.</span><span class="sxs-lookup"><span data-stu-id="abc46-162">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="abc46-163">Les sémantiques exactes dépendent de l’appareil et des protocoles et mécanismes utilisés pour communiquer avec lui.</span><span class="sxs-lookup"><span data-stu-id="abc46-163">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="abc46-164">Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="abc46-164">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="abc46-165">Notes</span><span class="sxs-lookup"><span data-stu-id="abc46-165">Remarks</span></span>

<span data-ttu-id="abc46-166">La classe **CIM \_ USBControllerHasHub** est dérivée de [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="abc46-166">The **CIM\_USBControllerHasHub** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="abc46-167">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="abc46-167">WMI does not implement this class.</span></span> <span data-ttu-id="abc46-168">Pour les classes WMI dérivées de **CIM \_ USBControllerHasHub**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="abc46-168">For WMI classes derived from **CIM\_USBControllerHasHub**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="abc46-169">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="abc46-169">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="abc46-170">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="abc46-170">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="abc46-171">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="abc46-171">Requirements</span></span>



| <span data-ttu-id="abc46-172">Condition requise</span><span class="sxs-lookup"><span data-stu-id="abc46-172">Requirement</span></span> | <span data-ttu-id="abc46-173">Valeur</span><span class="sxs-lookup"><span data-stu-id="abc46-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="abc46-174">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abc46-174">Minimum supported client</span></span><br/> | <span data-ttu-id="abc46-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc46-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="abc46-176">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abc46-176">Minimum supported server</span></span><br/> | <span data-ttu-id="abc46-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="abc46-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="abc46-178">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="abc46-178">Namespace</span></span><br/>                | <span data-ttu-id="abc46-179">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="abc46-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="abc46-180">MOF</span><span class="sxs-lookup"><span data-stu-id="abc46-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abc46-181"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="abc46-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="abc46-182">DLL</span><span class="sxs-lookup"><span data-stu-id="abc46-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abc46-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abc46-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abc46-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abc46-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abc46-185">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="abc46-185">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> </dl>

 

