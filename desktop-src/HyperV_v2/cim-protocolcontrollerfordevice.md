---
description: Représente une association entre un périphérique logique et un contrôleur de protocole connecté à l’appareil.
ms.assetid: 1a1efc60-6108-4376-9f73-d2dd41443645
title: Classe CIM_ProtocolControllerForDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolControllerForDevice
- CIM_ProtocolControllerForDevice.Antecedent
- CIM_ProtocolControllerForDevice.Dependent
- CIM_ProtocolControllerForDevice.DeviceNumber
- CIM_ProtocolControllerForDevice.AccessPriority
- CIM_ProtocolControllerForDevice.AccessState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7d3ef7799cccc6e8fe8e219cddfba37cf12b8637
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866734"
---
# <a name="cim_protocolcontrollerfordevice-class"></a><span data-ttu-id="a1611-103">\_Classe CIM ProtocolControllerForDevice</span><span class="sxs-lookup"><span data-stu-id="a1611-103">CIM\_ProtocolControllerForDevice class</span></span>

<span data-ttu-id="a1611-104">Représente une association entre un périphérique logique et un contrôleur de protocole connecté à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a1611-104">Represents an association between a logical device and a protocol controller that is connected to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1611-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1611-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.1000"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_ProtocolControllerForDevice : CIM_Dependency
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  string                     DeviceNumber;
  uint16                     AccessPriority;
  uint16                     AccessState;
};
```

## <a name="members"></a><span data-ttu-id="a1611-106">Membres</span><span class="sxs-lookup"><span data-stu-id="a1611-106">Members</span></span>

<span data-ttu-id="a1611-107">La classe **CIM \_ ProtocolControllerForDevice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a1611-107">The **CIM\_ProtocolControllerForDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="a1611-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a1611-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a1611-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a1611-109">Properties</span></span>

<span data-ttu-id="a1611-110">La classe **CIM \_ ProtocolControllerForDevice** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a1611-110">The **CIM\_ProtocolControllerForDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a1611-111">**AccessPriority**</span><span class="sxs-lookup"><span data-stu-id="a1611-111">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1611-112">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1611-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1611-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a1611-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1611-114">Priorité d’accès donnée à l’appareil via le contrôleur de protocole.</span><span class="sxs-lookup"><span data-stu-id="a1611-114">The access priority given to the device through the protocol controller.</span></span> <span data-ttu-id="a1611-115">La priorité la plus élevée a la valeur la plus faible.</span><span class="sxs-lookup"><span data-stu-id="a1611-115">The highest priority has the lowest value.</span></span>

</dd> <dt>

<span data-ttu-id="a1611-116">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="a1611-116">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1611-117">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1611-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1611-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a1611-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1611-119">Accessibilité de l’appareil logique via le contrôleur de protocole</span><span class="sxs-lookup"><span data-stu-id="a1611-119">The accessibility of the logical device through the protocol controller</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a1611-120">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="a1611-120">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="a1611-121">**Actif** (2)</span><span class="sxs-lookup"><span data-stu-id="a1611-121">**Active** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="a1611-122">**Inactif** (3)</span><span class="sxs-lookup"><span data-stu-id="a1611-122">**Inactive** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Replication_In_Progress"></span><span id="replication_in_progress"></span><span id="REPLICATION_IN_PROGRESS"></span>

<span data-ttu-id="a1611-123">**Réplication en cours** (4)</span><span class="sxs-lookup"><span data-stu-id="a1611-123">**Replication In Progress** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Mapping_Inconsistency"></span><span id="mapping_inconsistency"></span><span id="MAPPING_INCONSISTENCY"></span>

<span data-ttu-id="a1611-124">**Incohérence de mappage** (5)</span><span class="sxs-lookup"><span data-stu-id="a1611-124">**Mapping Inconsistency** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a1611-125">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="a1611-125">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1611-126">Type de données : **CIM \_ ProtocolController**</span><span class="sxs-lookup"><span data-stu-id="a1611-126">Data type: **CIM\_ProtocolController**</span></span>
</dt> <dt>

<span data-ttu-id="a1611-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a1611-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1611-128">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="a1611-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="a1611-129">Contrôleur de protocole dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="a1611-129">The protocol controller in the association.</span></span>

</dd> <dt>

<span data-ttu-id="a1611-130">**Charge**</span><span class="sxs-lookup"><span data-stu-id="a1611-130">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1611-131">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="a1611-131">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="a1611-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a1611-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1611-133">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="a1611-133">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="a1611-134">Unité logique dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="a1611-134">The logical device in the association.</span></span>

</dd> <dt>

<span data-ttu-id="a1611-135">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="a1611-135">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1611-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a1611-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1611-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a1611-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1611-138">Adresse de l’appareil associé dans le contexte du contrôleur de protocole.</span><span class="sxs-lookup"><span data-stu-id="a1611-138">The address of the associated device in the context of the protocol controler.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1611-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1611-139">Requirements</span></span>



| <span data-ttu-id="a1611-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1611-140">Requirement</span></span> | <span data-ttu-id="a1611-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1611-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1611-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1611-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a1611-143">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a1611-143">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="a1611-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1611-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a1611-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a1611-145">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="a1611-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a1611-146">Namespace</span></span><br/>                | <span data-ttu-id="a1611-147">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="a1611-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a1611-148">MOF</span><span class="sxs-lookup"><span data-stu-id="a1611-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1611-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a1611-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a1611-150">DLL</span><span class="sxs-lookup"><span data-stu-id="a1611-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1611-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a1611-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a1611-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1611-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1611-153">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="a1611-153">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

