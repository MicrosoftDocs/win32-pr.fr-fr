---
description: Représente une \_ relation CONTROLLEDBY CIM qui indique quels appareils sont accessibles via un contrôleur SCSI et les caractéristiques d’accès.
ms.assetid: a036dbf9-f9ce-4c85-9184-fefcbe4583ba
ms.tgt_platform: multiple
title: Classe CIM_SCSIInterface
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SCSIInterface
- CIM_SCSIInterface.NegotiatedDataWidth
- CIM_SCSIInterface.NegotiatedSpeed
- CIM_SCSIInterface.AccessState
- CIM_SCSIInterface.NumberOfHardResets
- CIM_SCSIInterface.NumberOfSoftResets
- CIM_SCSIInterface.Dependent
- CIM_SCSIInterface.Antecedent
- CIM_SCSIInterface.SCSIRetries
- CIM_SCSIInterface.SCSITimeouts
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1211b142681f15aa8b4d5e61c1d2165a59f5a62c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748596"
---
# <a name="cim_scsiinterface-class"></a><span data-ttu-id="1b89b-103">\_Classe CIM SCSIInterface</span><span class="sxs-lookup"><span data-stu-id="1b89b-103">CIM\_SCSIInterface class</span></span>

<span data-ttu-id="1b89b-104">La classe **CIM \_ SCSIInterface** représente une [**relation \_ ControlledBy CIM**](cim-controlledby.md) qui indique quels appareils sont accessibles via un contrôleur SCSI et les caractéristiques d’accès.</span><span class="sxs-lookup"><span data-stu-id="1b89b-104">The **CIM\_SCSIInterface** class represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through a SCSI controller and the access characteristics.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1b89b-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="1b89b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1b89b-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1b89b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1b89b-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="1b89b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="1b89b-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="1b89b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b89b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b89b-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{7CE7448E-E3D4-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SCSIInterface : CIM_ControlledBy
{
  uint32                 NegotiatedDataWidth;
  uint64                 NegotiatedSpeed;
  uint16                 AccessState;
  uint32                 NumberOfHardResets;
  uint32                 NumberOfSoftResets;
  CIM_LogicalDevice  REF Dependent;
  CIM_SCSIController REF Antecedent;
  uint32                 SCSIRetries;
  uint32                 SCSITimeouts;
};
```

## <a name="members"></a><span data-ttu-id="1b89b-110">Membres</span><span class="sxs-lookup"><span data-stu-id="1b89b-110">Members</span></span>

<span data-ttu-id="1b89b-111">La classe **CIM \_ SCSIInterface** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1b89b-111">The **CIM\_SCSIInterface** class has these types of members:</span></span>

-   [<span data-ttu-id="1b89b-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1b89b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1b89b-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1b89b-113">Properties</span></span>

<span data-ttu-id="1b89b-114">La classe **CIM \_ SCSIInterface** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="1b89b-114">The **CIM\_SCSIInterface** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1b89b-115">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="1b89b-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b89b-116">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b89b-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1b89b-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1b89b-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b89b-118">Indique si le contrôleur commande ou accède activement à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1b89b-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="1b89b-119">Ces informations sont nécessaires lorsqu’un périphérique logique peut être utilisé par plusieurs contrôleurs, ou y accéder via.</span><span class="sxs-lookup"><span data-stu-id="1b89b-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="1b89b-120">Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="1b89b-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1b89b-121">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="1b89b-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="1b89b-122">**Actif** (1)</span><span class="sxs-lookup"><span data-stu-id="1b89b-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="1b89b-123">**Inactif** (2)</span><span class="sxs-lookup"><span data-stu-id="1b89b-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1b89b-124">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="1b89b-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b89b-125">Type de données : **CIM \_ SCSIController**</span><span class="sxs-lookup"><span data-stu-id="1b89b-125">Data type: **CIM\_SCSIController**</span></span>
</dt> <dt>

<span data-ttu-id="1b89b-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1b89b-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b89b-127">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="1b89b-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="1b89b-128">[**\_ SCSIController CIM**](cim-scsicontroller.md) qui décrit le contrôleur SCSI.</span><span class="sxs-lookup"><span data-stu-id="1b89b-128">A [**CIM\_SCSIController**](cim-scsicontroller.md) that describes the SCSI controller.</span></span>

</dd> <dt>

<span data-ttu-id="1b89b-129">**Charge**</span><span class="sxs-lookup"><span data-stu-id="1b89b-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b89b-130">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="1b89b-130">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="1b89b-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1b89b-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b89b-132">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="1b89b-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="1b89b-133">[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui décrit l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="1b89b-133">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="1b89b-134">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="1b89b-134">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b89b-135">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1b89b-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1b89b-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1b89b-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b89b-137">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits »)</span><span class="sxs-lookup"><span data-stu-id="1b89b-137">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="1b89b-138">Lorsque plusieurs largeurs de données de bus ou de connexion sont possibles, cette propriété définit celle qui est utilisée entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="1b89b-138">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="1b89b-139">La largeur des données est spécifiée en bits.</span><span class="sxs-lookup"><span data-stu-id="1b89b-139">Data width is specified in bits.</span></span> <span data-ttu-id="1b89b-140">Si la largeur des données n’est pas négociée, ou si ces informations ne sont pas disponibles ou importantes pour la gestion des appareils, la propriété doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="1b89b-140">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="1b89b-141">Cette propriété est héritée de la [**\_ DeviceConnection CIM**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="1b89b-141">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="1b89b-142">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="1b89b-142">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b89b-143">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1b89b-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1b89b-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1b89b-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b89b-145">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="1b89b-145">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="1b89b-146">Lorsque plusieurs vitesses de bus ou de connexion sont possibles, cette propriété définit celle qui est utilisée entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="1b89b-146">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="1b89b-147">La vitesse est spécifiée en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="1b89b-147">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="1b89b-148">Si les vitesses de connexion ou de bus ne sont pas négociées, ou si ces informations ne sont pas disponibles ou importantes pour la gestion des appareils, la propriété doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="1b89b-148">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="1b89b-149">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1b89b-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="1b89b-150">Cette propriété est héritée de la [**\_ DeviceConnection CIM**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="1b89b-150">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="1b89b-151">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="1b89b-151">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b89b-152">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1b89b-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1b89b-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1b89b-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b89b-154">Nombre de réinitialisations matérielles émises par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="1b89b-154">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="1b89b-155">Une réinitialisation matérielle retourne l’appareil à son état d’initialisation ou de démarrage.</span><span class="sxs-lookup"><span data-stu-id="1b89b-155">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="1b89b-156">Toutes les informations sur l’état de l’appareil interne et les données sont perdues.</span><span class="sxs-lookup"><span data-stu-id="1b89b-156">All internal device state information and data are lost.</span></span>

<span data-ttu-id="1b89b-157">Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="1b89b-157">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="1b89b-158">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="1b89b-158">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b89b-159">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1b89b-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1b89b-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1b89b-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b89b-161">Nombre de réinitialisations logicielles émises par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="1b89b-161">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="1b89b-162">Une réinitialisation logicielle n’efface pas complètement l’état actuel de l’appareil et les données.</span><span class="sxs-lookup"><span data-stu-id="1b89b-162">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="1b89b-163">Les sémantiques exactes dépendent de l’appareil et des protocoles et mécanismes utilisés pour communiquer avec lui.</span><span class="sxs-lookup"><span data-stu-id="1b89b-163">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="1b89b-164">Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="1b89b-164">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="1b89b-165">**SCSIRetries**</span><span class="sxs-lookup"><span data-stu-id="1b89b-165">**SCSIRetries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b89b-166">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1b89b-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1b89b-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1b89b-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b89b-168">Nombre de nouvelles tentatives SCSI qui se sont produites depuis la dernière réinitialisation matérielle ou logicielle liée à l’appareil contrôlé.</span><span class="sxs-lookup"><span data-stu-id="1b89b-168">Number of SCSI retries that have occurred since the last hard or soft reset related to the controlled device.</span></span> <span data-ttu-id="1b89b-169">L’heure de la dernière réinitialisation est indiquée dans la propriété **TimeOfDeviceReset** , héritée de l’Association [**CIM \_ ControlledBy**](cim-controlledby.md) .</span><span class="sxs-lookup"><span data-stu-id="1b89b-169">The time of the last reset is indicated in the **TimeOfDeviceReset** property, inherited from the [**CIM\_ControlledBy**](cim-controlledby.md) association.</span></span>

</dd> <dt>

<span data-ttu-id="1b89b-170">**SCSITimeouts**</span><span class="sxs-lookup"><span data-stu-id="1b89b-170">**SCSITimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b89b-171">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1b89b-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1b89b-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1b89b-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b89b-173">Nombre de délais d’expiration SCSI qui se sont produits depuis la dernière réinitialisation matérielle ou logicielle liée à l’appareil contrôlé.</span><span class="sxs-lookup"><span data-stu-id="1b89b-173">Number of SCSI time-outs that occurred since last hard or soft reset related to the controlled device.</span></span> <span data-ttu-id="1b89b-174">L’heure de la dernière réinitialisation est indiquée dans la propriété **TimeOfDeviceReset** , héritée de l’Association [**CIM \_ ControlledBy**](cim-controlledby.md) .</span><span class="sxs-lookup"><span data-stu-id="1b89b-174">The time of the last reset is indicated in the **TimeOfDeviceReset** property, inherited from the [**CIM\_ControlledBy**](cim-controlledby.md) association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1b89b-175">Notes</span><span class="sxs-lookup"><span data-stu-id="1b89b-175">Remarks</span></span>

<span data-ttu-id="1b89b-176">La classe **CIM \_ SCSIInterface** est dérivée de [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="1b89b-176">The **CIM\_SCSIInterface** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="1b89b-177">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="1b89b-177">WMI does not implement this class.</span></span>

<span data-ttu-id="1b89b-178">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="1b89b-178">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1b89b-179">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="1b89b-179">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b89b-180">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b89b-180">Requirements</span></span>



| <span data-ttu-id="1b89b-181">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b89b-181">Requirement</span></span> | <span data-ttu-id="1b89b-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b89b-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b89b-183">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b89b-183">Minimum supported client</span></span><br/> | <span data-ttu-id="1b89b-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b89b-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1b89b-185">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b89b-185">Minimum supported server</span></span><br/> | <span data-ttu-id="1b89b-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b89b-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1b89b-187">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1b89b-187">Namespace</span></span><br/>                | <span data-ttu-id="1b89b-188">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="1b89b-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1b89b-189">MOF</span><span class="sxs-lookup"><span data-stu-id="1b89b-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b89b-190"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b89b-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b89b-191">DLL</span><span class="sxs-lookup"><span data-stu-id="1b89b-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b89b-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b89b-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b89b-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b89b-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b89b-194">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="1b89b-194">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> </dl>

 

