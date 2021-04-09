---
description: La \_ classe CIM SerialInterface représente une \_ relation ControlledBy CIM qui indique quels appareils sont accessibles par le biais du contrôleur série et les caractéristiques de l’accès.
ms.assetid: bebc304a-c2b7-41c7-b24a-8f450ee3c4bb
ms.tgt_platform: multiple
title: Classe CIM_SerialInterface
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SerialInterface
- CIM_SerialInterface.NegotiatedDataWidth
- CIM_SerialInterface.NegotiatedSpeed
- CIM_SerialInterface.AccessState
- CIM_SerialInterface.NumberOfHardResets
- CIM_SerialInterface.NumberOfSoftResets
- CIM_SerialInterface.Dependent
- CIM_SerialInterface.Antecedent
- CIM_SerialInterface.FlowControlInfo
- CIM_SerialInterface.NumberOfStopBits
- CIM_SerialInterface.ParityInfo
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1df787ff64798f412035a72e6db6d7b01b4b9b0a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861025"
---
# <a name="cim_serialinterface-class"></a><span data-ttu-id="b5ef4-103">\_Classe CIM SerialInterface</span><span class="sxs-lookup"><span data-stu-id="b5ef4-103">CIM\_SerialInterface class</span></span>

<span data-ttu-id="b5ef4-104">La classe **CIM \_ SerialInterface** représente une [**relation \_ ControlledBy CIM**](cim-controlledby.md) qui indique quels appareils sont accessibles par le biais du contrôleur série et les caractéristiques de l’accès.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-104">The **CIM\_SerialInterface** class represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through the serial controller and the characteristics of the access.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b5ef4-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b5ef4-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b5ef4-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b5ef4-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b5ef4-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5ef4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5ef4-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8B309BDA-E3D4-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SerialInterface : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  CIM_LogicalDevice    REF Dependent;
  CIM_SerialController REF Antecedent;
  uint16                   FlowControlInfo;
  uint16                   NumberOfStopBits;
  uint16                   ParityInfo;
};
```

## <a name="members"></a><span data-ttu-id="b5ef4-110">Membres</span><span class="sxs-lookup"><span data-stu-id="b5ef4-110">Members</span></span>

<span data-ttu-id="b5ef4-111">La classe **CIM \_ SerialInterface** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b5ef4-111">The **CIM\_SerialInterface** class has these types of members:</span></span>

-   [<span data-ttu-id="b5ef4-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b5ef4-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5ef4-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b5ef4-113">Properties</span></span>

<span data-ttu-id="b5ef4-114">La classe **CIM \_ SerialInterface** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-114">The **CIM\_SerialInterface** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b5ef4-115">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="b5ef4-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ef4-116">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5ef4-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5ef4-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5ef4-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5ef4-118">Indique si le contrôleur commande ou accède activement à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="b5ef4-119">Ces informations sont nécessaires lorsqu’un périphérique logique peut être utilisé par plusieurs contrôleurs, ou y accéder via.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="b5ef4-120">Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="b5ef4-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b5ef4-121">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="b5ef4-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="b5ef4-122">**Actif** (1)</span><span class="sxs-lookup"><span data-stu-id="b5ef4-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="b5ef4-123">**Inactif** (2)</span><span class="sxs-lookup"><span data-stu-id="b5ef4-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b5ef4-124">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="b5ef4-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ef4-125">Type de données : **CIM \_ SerialController**</span><span class="sxs-lookup"><span data-stu-id="b5ef4-125">Data type: **CIM\_SerialController**</span></span>
</dt> <dt>

<span data-ttu-id="b5ef4-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5ef4-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5ef4-127">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="b5ef4-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b5ef4-128">[**\_ SerialController CIM**](cim-serialcontroller.md) qui décrit le contrôleur série.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-128">A [**CIM\_SerialController**](cim-serialcontroller.md) that describes the serial controller.</span></span>

</dd> <dt>

<span data-ttu-id="b5ef4-129">**Charge**</span><span class="sxs-lookup"><span data-stu-id="b5ef4-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ef4-130">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="b5ef4-130">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="b5ef4-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5ef4-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5ef4-132">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="b5ef4-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b5ef4-133">[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui décrit l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-133">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="b5ef4-134">**FlowControlInfo**</span><span class="sxs-lookup"><span data-stu-id="b5ef4-134">**FlowControlInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ef4-135">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5ef4-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5ef4-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5ef4-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5ef4-137">Indique le contrôle de Flow pour les données transmises.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-137">Indicates the flow control for transmitted data.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b5ef4-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="b5ef4-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b5ef4-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="b5ef4-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="b5ef4-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Aucun** (2)</span><span class="sxs-lookup"><span data-stu-id="b5ef4-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>

<span data-ttu-id="b5ef4-141"><span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>**XOnXOff** (3)</span><span class="sxs-lookup"><span data-stu-id="b5ef4-141"><span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>**XonXoff** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="RTS_CTS"></span><span id="rts_cts"></span>

<span data-ttu-id="b5ef4-142"><span id="RTS_CTS"></span><span id="rts_cts"></span>**RTS/CTS** (4)</span><span class="sxs-lookup"><span data-stu-id="b5ef4-142"><span id="RTS_CTS"></span><span id="rts_cts"></span>**RTS/CTS** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>

<span data-ttu-id="b5ef4-143"><span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>**XOnXOff et RTS/CTS** (5)</span><span class="sxs-lookup"><span data-stu-id="b5ef4-143"><span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>**Both XonXoff and RTS/CTS** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b5ef4-144">XonXoff et RTS/CTS</span><span class="sxs-lookup"><span data-stu-id="b5ef4-144">XonXoff and RTS/CTS</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b5ef4-145">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="b5ef4-145">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ef4-146">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5ef4-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5ef4-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5ef4-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5ef4-148">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits »)</span><span class="sxs-lookup"><span data-stu-id="b5ef4-148">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="b5ef4-149">Lorsque plusieurs largeurs de données de bus ou de connexion sont possibles, cette propriété définit celle qui est utilisée entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-149">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="b5ef4-150">La largeur des données est spécifiée en bits.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-150">Data width is specified in bits.</span></span> <span data-ttu-id="b5ef4-151">Si la largeur des données n’est pas négociée, ou si ces informations ne sont pas disponibles ou importantes pour la gestion des appareils, la propriété doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="b5ef4-151">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="b5ef4-152">Cette propriété est héritée de la [**\_ DeviceConnection CIM**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="b5ef4-152">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5ef4-153">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="b5ef4-153">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ef4-154">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b5ef4-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b5ef4-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5ef4-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5ef4-156">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="b5ef4-156">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="b5ef4-157">Lorsque plusieurs vitesses de bus ou de connexion sont possibles, cette propriété définit celle qui est utilisée entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-157">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="b5ef4-158">La vitesse est spécifiée en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-158">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="b5ef4-159">Si les vitesses de connexion ou de bus ne sont pas négociées, ou si ces informations ne sont pas disponibles ou importantes pour la gestion des appareils, la propriété doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="b5ef4-159">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="b5ef4-160">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b5ef4-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="b5ef4-161">Cette propriété est héritée de la [**\_ DeviceConnection CIM**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="b5ef4-161">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5ef4-162">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="b5ef4-162">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ef4-163">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5ef4-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5ef4-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5ef4-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5ef4-165">Nombre de réinitialisations matérielles émises par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-165">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="b5ef4-166">Une réinitialisation matérielle retourne l’appareil à son état d’initialisation ou de démarrage.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-166">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="b5ef4-167">Toutes les informations sur l’état de l’appareil interne et les données sont perdues.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-167">All internal device state information and data are lost.</span></span>

<span data-ttu-id="b5ef4-168">Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="b5ef4-168">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5ef4-169">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="b5ef4-169">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ef4-170">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5ef4-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5ef4-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5ef4-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5ef4-172">Nombre de réinitialisations logicielles émises par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-172">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="b5ef4-173">Une réinitialisation logicielle n’efface pas complètement l’état actuel de l’appareil et les données.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-173">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="b5ef4-174">Les sémantiques exactes dépendent de l’appareil et des protocoles et mécanismes utilisés pour communiquer avec lui.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-174">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="b5ef4-175">Cette propriété est héritée de la [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="b5ef4-175">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5ef4-176">**NumberOfStopBits**</span><span class="sxs-lookup"><span data-stu-id="b5ef4-176">**NumberOfStopBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ef4-177">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5ef4-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5ef4-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5ef4-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5ef4-179">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits »)</span><span class="sxs-lookup"><span data-stu-id="b5ef4-179">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="b5ef4-180">Nombre de bits d’arrêt à transmettre.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-180">Number of stop bits to transmit.</span></span>

</dd> <dt>

<span data-ttu-id="b5ef4-181">**ParityInfo**</span><span class="sxs-lookup"><span data-stu-id="b5ef4-181">**ParityInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ef4-182">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5ef4-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5ef4-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5ef4-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5ef4-184">Informations sur le paramètre de parité pour les données transmises.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-184">Information about the parity setting for transmitted data.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b5ef4-185">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="b5ef4-185">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="b5ef4-186">**Aucun** (1)</span><span class="sxs-lookup"><span data-stu-id="b5ef4-186">**None** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

<span data-ttu-id="b5ef4-187">**Même** (2)</span><span class="sxs-lookup"><span data-stu-id="b5ef4-187">**Even** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

<span data-ttu-id="b5ef4-188">**Impair** (3)</span><span class="sxs-lookup"><span data-stu-id="b5ef4-188">**Odd** (3)</span></span>


<span data-ttu-id="b5ef4-189"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b5ef4-189"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="b5ef4-190">Notes</span><span class="sxs-lookup"><span data-stu-id="b5ef4-190">Remarks</span></span>

<span data-ttu-id="b5ef4-191">La classe **CIM \_ SerialInterface** est dérivée de [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="b5ef4-191">The **CIM\_SerialInterface** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="b5ef4-192">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-192">WMI does not implement this class.</span></span>

<span data-ttu-id="b5ef4-193">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-193">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b5ef4-194">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="b5ef4-194">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5ef4-195">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5ef4-195">Requirements</span></span>



| <span data-ttu-id="b5ef4-196">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5ef4-196">Requirement</span></span> | <span data-ttu-id="b5ef4-197">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5ef4-197">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5ef4-198">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5ef4-198">Minimum supported client</span></span><br/> | <span data-ttu-id="b5ef4-199">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5ef4-199">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b5ef4-200">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5ef4-200">Minimum supported server</span></span><br/> | <span data-ttu-id="b5ef4-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5ef4-201">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b5ef4-202">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b5ef4-202">Namespace</span></span><br/>                | <span data-ttu-id="b5ef4-203">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="b5ef4-203">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b5ef4-204">MOF</span><span class="sxs-lookup"><span data-stu-id="b5ef4-204">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5ef4-205"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5ef4-205"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5ef4-206">DLL</span><span class="sxs-lookup"><span data-stu-id="b5ef4-206">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5ef4-207"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5ef4-207"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5ef4-208">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5ef4-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5ef4-209">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="b5ef4-209">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> </dl>

 

