---
description: La \_ relation CONTROLLEDBY CIM indique quels appareils sont demandés par l’unité logique du contrôleur, ou accessibles via celui-ci.
ms.assetid: 6aa4e088-32a0-4c88-bb82-341b6ab53b4c
ms.tgt_platform: multiple
title: CIM_ControlledBy, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ControlledBy
- CIM_ControlledBy.NegotiatedDataWidth
- CIM_ControlledBy.NegotiatedSpeed
- CIM_ControlledBy.Dependent
- CIM_ControlledBy.Antecedent
- CIM_ControlledBy.AccessState
- CIM_ControlledBy.NumberOfHardResets
- CIM_ControlledBy.NumberOfSoftResets
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 315eea9fa207a92c3aa1add6fe021127dc3949d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861033"
---
# <a name="cim_controlledby-class-cimwin32-wmi-providers"></a><span data-ttu-id="36443-103">CIM_ControlledBy, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="36443-103">CIM_ControlledBy class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="36443-104">La **relation \_ ControlledBy CIM** indique quels appareils sont demandés par l’unité logique du contrôleur, ou accessibles via celui-ci.</span><span class="sxs-lookup"><span data-stu-id="36443-104">The **CIM\_ControlledBy** relationship indicates which devices are commanded by, or accessed through, the controller logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="36443-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="36443-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="36443-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="36443-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="36443-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="36443-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="36443-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="36443-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="36443-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36443-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53D-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ControlledBy : CIM_DeviceConnection
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  CIM_LogicalDevice REF Dependent;
  CIM_Controller    REF Antecedent;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
};
```

## <a name="members"></a><span data-ttu-id="36443-110">Membres</span><span class="sxs-lookup"><span data-stu-id="36443-110">Members</span></span>

<span data-ttu-id="36443-111">La classe **CIM \_ ControlledBy** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="36443-111">The **CIM\_ControlledBy** class has these types of members:</span></span>

-   [<span data-ttu-id="36443-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="36443-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="36443-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="36443-113">Properties</span></span>

<span data-ttu-id="36443-114">La classe **CIM \_ ControlledBy** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="36443-114">The **CIM\_ControlledBy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="36443-115">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="36443-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36443-116">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="36443-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="36443-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36443-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36443-118">Indique si le contrôleur commande ou accède activement à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="36443-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="36443-119">Ces informations sont nécessaires lorsqu’un périphérique logique peut être utilisé par plusieurs contrôleurs, ou y accéder via.</span><span class="sxs-lookup"><span data-stu-id="36443-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="36443-120">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="36443-120">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="36443-121">**Actif** (1)</span><span class="sxs-lookup"><span data-stu-id="36443-121">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="36443-122">**Inactif** (2)</span><span class="sxs-lookup"><span data-stu-id="36443-122">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="36443-123">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="36443-123">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36443-124">Type de données **: \_ contrôleur CIM**</span><span class="sxs-lookup"><span data-stu-id="36443-124">Data type: **CIM\_Controller**</span></span>
</dt> <dt>

<span data-ttu-id="36443-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36443-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36443-126">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="36443-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="36443-127">[**\_ Contrôleur CIM**](cim-controller.md) qui représente le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="36443-127">A [**CIM\_Controller**](cim-controller.md) that represents the controller.</span></span>

</dd> <dt>

<span data-ttu-id="36443-128">**Charge**</span><span class="sxs-lookup"><span data-stu-id="36443-128">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36443-129">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="36443-129">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="36443-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36443-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36443-131">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="36443-131">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="36443-132">[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui représente l’appareil contrôlé.</span><span class="sxs-lookup"><span data-stu-id="36443-132">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the controlled device.</span></span>

</dd> <dt>

<span data-ttu-id="36443-133">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="36443-133">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36443-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36443-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="36443-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36443-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36443-136">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits »)</span><span class="sxs-lookup"><span data-stu-id="36443-136">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="36443-137">Lorsque plusieurs largeurs de données de bus ou de connexion sont possibles, cette propriété définit celle qui est utilisée entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="36443-137">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="36443-138">La largeur des données est spécifiée en bits.</span><span class="sxs-lookup"><span data-stu-id="36443-138">Data width is specified in bits.</span></span> <span data-ttu-id="36443-139">Si la largeur des données n’est pas négociée, ou si ces informations ne sont pas disponibles ou importantes pour la gestion des appareils, la propriété doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="36443-139">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="36443-140">Cette propriété est héritée de la [**\_ DeviceConnection CIM**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="36443-140">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="36443-141">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="36443-141">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36443-142">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="36443-142">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="36443-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36443-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36443-144">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="36443-144">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="36443-145">Lorsque plusieurs vitesses de bus ou de connexion sont possibles, cette propriété définit celle qui est utilisée entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="36443-145">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="36443-146">La vitesse est spécifiée en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="36443-146">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="36443-147">Si les vitesses de connexion ou de bus ne sont pas négociées, ou si ces informations ne sont pas disponibles ou importantes pour la gestion des appareils, la propriété doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="36443-147">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="36443-148">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="36443-148">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="36443-149">Cette propriété est héritée de la [**\_ DeviceConnection CIM**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="36443-149">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="36443-150">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="36443-150">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36443-151">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36443-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="36443-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36443-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36443-153">Nombre de réinitialisations matérielles émises par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="36443-153">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="36443-154">Une réinitialisation matérielle retourne l’appareil à son état d’initialisation ou de démarrage.</span><span class="sxs-lookup"><span data-stu-id="36443-154">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="36443-155">Toutes les informations sur l’état de l’appareil interne et les données sont perdues.</span><span class="sxs-lookup"><span data-stu-id="36443-155">All internal device state information and data are lost.</span></span>

</dd> <dt>

<span data-ttu-id="36443-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="36443-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36443-157">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36443-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="36443-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36443-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36443-159">Nombre de réinitialisations logicielles émises par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="36443-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="36443-160">Une réinitialisation logicielle n’efface pas complètement l’état actuel de l’appareil et les données.</span><span class="sxs-lookup"><span data-stu-id="36443-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="36443-161">Les sémantiques exactes dépendent de l’appareil et des protocoles et mécanismes utilisés pour communiquer avec lui.</span><span class="sxs-lookup"><span data-stu-id="36443-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36443-162">Notes</span><span class="sxs-lookup"><span data-stu-id="36443-162">Remarks</span></span>

<span data-ttu-id="36443-163">La classe **CIM \_ ControlledBy** est dérivée de [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="36443-163">The **CIM\_ControlledBy** class is derived from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

<span data-ttu-id="36443-164">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="36443-164">WMI does not implement this class.</span></span> <span data-ttu-id="36443-165">Pour plus d’informations sur les classes dérivées de **CIM \_ ControlledBy**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="36443-165">For more information about classes derived from **CIM\_ControlledBy**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="36443-166">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="36443-166">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="36443-167">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="36443-167">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="36443-168">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36443-168">Requirements</span></span>



| <span data-ttu-id="36443-169">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36443-169">Requirement</span></span> | <span data-ttu-id="36443-170">Valeur</span><span class="sxs-lookup"><span data-stu-id="36443-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36443-171">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36443-171">Minimum supported client</span></span><br/> | <span data-ttu-id="36443-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36443-172">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="36443-173">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36443-173">Minimum supported server</span></span><br/> | <span data-ttu-id="36443-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36443-174">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="36443-175">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="36443-175">Namespace</span></span><br/>                | <span data-ttu-id="36443-176">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="36443-176">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="36443-177">MOF</span><span class="sxs-lookup"><span data-stu-id="36443-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36443-178"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="36443-178"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="36443-179">DLL</span><span class="sxs-lookup"><span data-stu-id="36443-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36443-180"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36443-180"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36443-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36443-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36443-182">**\_DEVICECONNECTION CIM**</span><span class="sxs-lookup"><span data-stu-id="36443-182">**CIM\_DeviceConnection**</span></span>](cim-deviceconnection.md)
</dt> </dl>

 

