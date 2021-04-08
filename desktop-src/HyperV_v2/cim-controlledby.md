---
description: Représente une relation entre un contrôleur et un périphérique logique qui est géré par le contrôleur.
ms.assetid: 5a938fa4-3b91-42ad-beee-12ed0ce6df9a
title: Classe CIM_ControlledBy (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ControlledBy
- CIM_ControlledBy.Antecedent
- CIM_ControlledBy.Dependent
- CIM_ControlledBy.AccessState
- CIM_ControlledBy.TimeOfDeviceReset
- CIM_ControlledBy.NumberOfHardResets
- CIM_ControlledBy.NumberOfSoftResets
- CIM_ControlledBy.DeviceNumber
- CIM_ControlledBy.AccessMode
- CIM_ControlledBy.AccessPriority
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7b035a93c47f9c33d981614ba6fc46b35f916e7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863126"
---
# <a name="cim_controlledby-class-hyper-v-management"></a><span data-ttu-id="4f201-103">Classe CIM_ControlledBy (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="4f201-103">CIM_ControlledBy class (Hyper-V management)</span></span>

<span data-ttu-id="4f201-104">Représente une relation entre un contrôleur et un périphérique logique qui est géré par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="4f201-104">Represents a relationship between a controller and a logical device that is managed by the controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f201-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f201-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_ControlledBy : CIM_DeviceConnection
{
  CIM_Controller    REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint16                AccessState;
  datetime              TimeOfDeviceReset;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  string                DeviceNumber;
  uint16                AccessMode;
  uint16                AccessPriority;
};
```

## <a name="members"></a><span data-ttu-id="4f201-106">Membres</span><span class="sxs-lookup"><span data-stu-id="4f201-106">Members</span></span>

<span data-ttu-id="4f201-107">La classe **CIM \_ ControlledBy** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4f201-107">The **CIM\_ControlledBy** class has these types of members:</span></span>

-   [<span data-ttu-id="4f201-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4f201-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f201-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4f201-109">Properties</span></span>

<span data-ttu-id="4f201-110">La classe **CIM \_ ControlledBy** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4f201-110">The **CIM\_ControlledBy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f201-111">**AccessMode**</span><span class="sxs-lookup"><span data-stu-id="4f201-111">**AccessMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f201-112">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f201-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f201-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f201-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f201-114">Cette propriété qui décrit l’accessibilité de l’appareil par le biais du contrôleur.</span><span class="sxs-lookup"><span data-stu-id="4f201-114">This property that describes the accessibility of the device through the controller.</span></span>

<dt>

<span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>

<span data-ttu-id="4f201-115">**ReadWrite** (2)</span><span class="sxs-lookup"><span data-stu-id="4f201-115">**ReadWrite** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>

<span data-ttu-id="4f201-116">**Lecture seule** (3)</span><span class="sxs-lookup"><span data-stu-id="4f201-116">**ReadOnly** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="NoAccess"></span><span id="noaccess"></span><span id="NOACCESS"></span>

<span data-ttu-id="4f201-117">**NoAccess** (4)</span><span class="sxs-lookup"><span data-stu-id="4f201-117">**NoAccess** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4f201-118">**AccessPriority**</span><span class="sxs-lookup"><span data-stu-id="4f201-118">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f201-119">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f201-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f201-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f201-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f201-121">Priorité pour l’accès de l’appareil par le biais du contrôleur.</span><span class="sxs-lookup"><span data-stu-id="4f201-121">The priority for access of the device through the controller.</span></span> <span data-ttu-id="4f201-122">Une valeur inférieure indique une priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="4f201-122">A lower value indicates a higher priority.</span></span>

</dd> <dt>

<span data-ttu-id="4f201-123">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="4f201-123">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f201-124">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f201-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f201-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f201-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f201-126">Indique si le contrôleur gère activement l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4f201-126">Indicates whether the controller is actively managing the device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4f201-127">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="4f201-127">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="4f201-128">**Actif** (1)</span><span class="sxs-lookup"><span data-stu-id="4f201-128">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="4f201-129">**Inactif** (2)</span><span class="sxs-lookup"><span data-stu-id="4f201-129">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4f201-130">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="4f201-130">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f201-131">Type de données **: \_ contrôleur CIM**</span><span class="sxs-lookup"><span data-stu-id="4f201-131">Data type: **CIM\_Controller**</span></span>
</dt> <dt>

<span data-ttu-id="4f201-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f201-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f201-133">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="4f201-133">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="4f201-134">Contrôleur.</span><span class="sxs-lookup"><span data-stu-id="4f201-134">The controller.</span></span>

</dd> <dt>

<span data-ttu-id="4f201-135">**Charge**</span><span class="sxs-lookup"><span data-stu-id="4f201-135">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f201-136">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="4f201-136">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="4f201-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f201-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f201-138">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="4f201-138">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4f201-139">Périphériques logiques.</span><span class="sxs-lookup"><span data-stu-id="4f201-139">The logical devices.</span></span>

</dd> <dt>

<span data-ttu-id="4f201-140">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="4f201-140">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f201-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4f201-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f201-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f201-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f201-143">Adresse de l’appareil associé dans le contexte du contrôleur.</span><span class="sxs-lookup"><span data-stu-id="4f201-143">The address of the associated device in the context of the controller.</span></span>

</dd> <dt>

<span data-ttu-id="4f201-144">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="4f201-144">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f201-145">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f201-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f201-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f201-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f201-147">Qualificateurs : **compteur**</span><span class="sxs-lookup"><span data-stu-id="4f201-147">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="4f201-148">Nombre de réinitialisations matérielles émises par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="4f201-148">The number of hard resets issued by the controller.</span></span> <span data-ttu-id="4f201-149">Une réinitialisation matérielle retourne un appareil à son état d’initialisation ou de démarrage, après quoi toutes les informations et les données d’état de l’appareil interne sont perdues.</span><span class="sxs-lookup"><span data-stu-id="4f201-149">A hard reset returns a device to its initialization or boot-up state, after which all internal device state information and data are lost.</span></span>

</dd> <dt>

<span data-ttu-id="4f201-150">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="4f201-150">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f201-151">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f201-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f201-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f201-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f201-153">Qualificateurs : **compteur**</span><span class="sxs-lookup"><span data-stu-id="4f201-153">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="4f201-154">Nombre de réinitialisations logicielles émises par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="4f201-154">The number of soft resets issued by the controller.</span></span> <span data-ttu-id="4f201-155">Une réinitialisation logicielle n’efface pas l’État ou les données de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4f201-155">A soft reset does not clear the device state or data.</span></span>

</dd> <dt>

<span data-ttu-id="4f201-156">**TimeOfDeviceReset**</span><span class="sxs-lookup"><span data-stu-id="4f201-156">**TimeOfDeviceReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f201-157">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4f201-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4f201-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f201-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f201-159">Heure de la dernière réinitialisation de l’appareil en aval par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="4f201-159">The time when the downstream device was last reset by the controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f201-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f201-160">Requirements</span></span>



| <span data-ttu-id="4f201-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f201-161">Requirement</span></span> | <span data-ttu-id="4f201-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f201-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f201-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f201-163">Minimum supported client</span></span><br/> | <span data-ttu-id="4f201-164">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4f201-164">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4f201-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f201-165">Minimum supported server</span></span><br/> | <span data-ttu-id="4f201-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4f201-166">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4f201-167">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4f201-167">Namespace</span></span><br/>                | <span data-ttu-id="4f201-168">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="4f201-168">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4f201-169">MOF</span><span class="sxs-lookup"><span data-stu-id="4f201-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f201-170"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f201-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f201-171">DLL</span><span class="sxs-lookup"><span data-stu-id="4f201-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f201-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4f201-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4f201-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f201-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f201-174">**\_DEVICECONNECTION CIM**</span><span class="sxs-lookup"><span data-stu-id="4f201-174">**CIM\_DeviceConnection**</span></span>](cim-deviceconnection.md)
</dt> </dl>

 

