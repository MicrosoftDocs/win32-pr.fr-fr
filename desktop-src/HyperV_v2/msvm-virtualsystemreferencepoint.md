---
description: Représente un point de référence pour un système virtuel.
ms.assetid: b3ba4fa7-3b77-4a1d-ab8f-d38af12ab5dd
title: Classe Msvm_VirtualSystemReferencePoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePoint
- Msvm_VirtualSystemReferencePoint.InstanceID
- Msvm_VirtualSystemReferencePoint.ReferencePointType
- Msvm_VirtualSystemReferencePoint.ConsistencyLevel
- Msvm_VirtualSystemReferencePoint.VirtualSystemIdentifier
- Msvm_VirtualSystemReferencePoint.HasAssociatedData
- Msvm_VirtualSystemReferencePoint.VirtualDiskIdentifiers
- Msvm_VirtualSystemReferencePoint.ResilientChangeTrackingIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: add160cf44a592462634704ddf783cd8f4084068
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106522751"
---
# <a name="msvm_virtualsystemreferencepoint-class"></a><span data-ttu-id="868b3-103">MSVM \_ VirtualSystemReferencePoint, classe</span><span class="sxs-lookup"><span data-stu-id="868b3-103">Msvm\_VirtualSystemReferencePoint class</span></span>

<span data-ttu-id="868b3-104">Représente un point de référence pour un système virtuel.</span><span class="sxs-lookup"><span data-stu-id="868b3-104">Represents a reference point for a virtual system.</span></span>

<span data-ttu-id="868b3-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="868b3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="868b3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="868b3-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePoint : CIM_ManagedElement
{
  string  InstanceID;
  uint16  ReferencePointType;
  uint16  ConsistencyLevel;
  string  VirtualSystemIdentifier;
  boolean HasAssociatedData;
  string  VirtualDiskIdentifiers[];
  string  ResilientChangeTrackingIdentifiers[];
};
```

## <a name="members"></a><span data-ttu-id="868b3-107">Membres</span><span class="sxs-lookup"><span data-stu-id="868b3-107">Members</span></span>

<span data-ttu-id="868b3-108">La classe **MSVM \_ VirtualSystemReferencePoint** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="868b3-108">The **Msvm\_VirtualSystemReferencePoint** class has these types of members:</span></span>

-   [<span data-ttu-id="868b3-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="868b3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="868b3-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="868b3-110">Properties</span></span>

<span data-ttu-id="868b3-111">La classe **MSVM \_ VirtualSystemReferencePoint** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="868b3-111">The **Msvm\_VirtualSystemReferencePoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="868b3-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="868b3-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="868b3-113">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="868b3-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="868b3-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="868b3-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="868b3-115">Niveau de cohérence du point de référence.</span><span class="sxs-lookup"><span data-stu-id="868b3-115">The consistency level of the reference point.</span></span>

<dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="868b3-116"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Cohérence des applications** (1)</span><span class="sxs-lookup"><span data-stu-id="868b3-116"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="868b3-117">Le point de référence indique un point dans le temps où le système virtuel était dans un état de cohérence des applications.</span><span class="sxs-lookup"><span data-stu-id="868b3-117">The reference point indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="868b3-118"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Cohérence des incidents** (2)</span><span class="sxs-lookup"><span data-stu-id="868b3-118"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="868b3-119">Le point de référence indique un point dans le temps où le système virtuel se trouvait dans un état de cohérence en cas d’incident.</span><span class="sxs-lookup"><span data-stu-id="868b3-119">The reference point indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="868b3-120">**HasAssociatedData**</span><span class="sxs-lookup"><span data-stu-id="868b3-120">**HasAssociatedData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="868b3-121">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="868b3-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="868b3-122">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="868b3-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="868b3-123">A la valeur **true** si le point de référence a des données associées.</span><span class="sxs-lookup"><span data-stu-id="868b3-123">Set to **true** if the reference point has associated data.</span></span> <span data-ttu-id="868b3-124">Cela est valide uniquement pour les points de référence basés sur un journal.</span><span class="sxs-lookup"><span data-stu-id="868b3-124">This is valid only for log based reference points.</span></span> <span data-ttu-id="868b3-125">Pour les points de référence basés sur RCT, **HasAssociatedData** est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="868b3-125">For RCT-based reference points, **HasAssociatedData** is set to **false**.</span></span> <span data-ttu-id="868b3-126">Pour les points de référence basés sur un journal, une fois le journal ignoré, **HasAssociatedData** prend la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="868b3-126">For log based reference points, once the log is discarded **HasAssociatedData** becomes **false**.</span></span>

</dd> <dt>

<span data-ttu-id="868b3-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="868b3-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="868b3-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="868b3-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="868b3-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="868b3-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="868b3-130">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="868b3-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="868b3-131">Identification unique d’un objet de point de référence.</span><span class="sxs-lookup"><span data-stu-id="868b3-131">Unique identification of a reference point object.</span></span>

</dd> <dt>

<span data-ttu-id="868b3-132">**ReferencePointType**</span><span class="sxs-lookup"><span data-stu-id="868b3-132">**ReferencePointType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="868b3-133">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="868b3-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="868b3-134">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="868b3-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="868b3-135">Indique le type du point de référence.</span><span class="sxs-lookup"><span data-stu-id="868b3-135">Indicates the type of the reference point.</span></span>

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="868b3-136"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Basé sur le journal** (1)</span><span class="sxs-lookup"><span data-stu-id="868b3-136"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="868b3-137">Suivi du journal de réplication Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="868b3-137">Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="868b3-138"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**Basé sur RCT** (2)</span><span class="sxs-lookup"><span data-stu-id="868b3-138"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (2)</span></span>


</dt> <dd>

<span data-ttu-id="868b3-139">Basé sur une Change Tracking résiliente des disques virtuels.</span><span class="sxs-lookup"><span data-stu-id="868b3-139">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="868b3-140">**ResilientChangeTrackingIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="868b3-140">**ResilientChangeTrackingIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="868b3-141">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="868b3-141">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="868b3-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="868b3-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="868b3-143">Tableau d’ID RCT correspondant aux disques virtuels de la machine virtuelle au moment de la création de ce point de référence.</span><span class="sxs-lookup"><span data-stu-id="868b3-143">An array of RCT IDs corresponding to the virtual disks of the VM at the time this reference point was created.</span></span> <span data-ttu-id="868b3-144">Ce champ est valide uniquement pour les points de référence basés sur RCT.</span><span class="sxs-lookup"><span data-stu-id="868b3-144">This field is valid only for RCT-based reference points.</span></span>

</dd> <dt>

<span data-ttu-id="868b3-145">**VirtualDiskIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="868b3-145">**VirtualDiskIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="868b3-146">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="868b3-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="868b3-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="868b3-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="868b3-148">Tableau d’ID d’instance WMI correspondant aux disques virtuels de la machine virtuelle au moment de la création de ce point de référence.</span><span class="sxs-lookup"><span data-stu-id="868b3-148">An array of WMI instance IDs corresponding to the virtual disks of the VM at the time this reference point was created.</span></span> <span data-ttu-id="868b3-149">Ces disques virtuels sont associés à des ID RCT.</span><span class="sxs-lookup"><span data-stu-id="868b3-149">These virtual disks have RCT IDs associated with them.</span></span>

</dd> <dt>

<span data-ttu-id="868b3-150">**Attribut virtualsystemidentifier**</span><span class="sxs-lookup"><span data-stu-id="868b3-150">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="868b3-151">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="868b3-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="868b3-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="868b3-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="868b3-153">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ CIM**](cim-computersystem.md).**Name**»)</span><span class="sxs-lookup"><span data-stu-id="868b3-153">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="868b3-154">Nom du [**\_ ComputerSystem CIM**](cim-computersystem.md) auquel ce point de référence appartient</span><span class="sxs-lookup"><span data-stu-id="868b3-154">The name of the [**CIM\_ComputerSystem**](cim-computersystem.md) to which this reference point belongs</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="868b3-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="868b3-155">Requirements</span></span>



| <span data-ttu-id="868b3-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="868b3-156">Requirement</span></span> | <span data-ttu-id="868b3-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="868b3-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="868b3-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="868b3-158">Minimum supported client</span></span><br/> | <span data-ttu-id="868b3-159">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="868b3-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="868b3-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="868b3-160">Minimum supported server</span></span><br/> | <span data-ttu-id="868b3-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="868b3-161">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="868b3-162">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="868b3-162">Namespace</span></span><br/>                | <span data-ttu-id="868b3-163">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="868b3-163">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="868b3-164">MOF</span><span class="sxs-lookup"><span data-stu-id="868b3-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="868b3-165"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="868b3-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="868b3-166">DLL</span><span class="sxs-lookup"><span data-stu-id="868b3-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="868b3-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="868b3-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="868b3-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="868b3-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="868b3-169">**\_Propriété MANAGEDELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="868b3-169">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

