---
description: Représente les fonctionnalités d’un \_ objet CIM VirtualSystemManagementService.
ms.assetid: 484b0378-b354-49c4-b98b-a960a7b07b92
title: Classe CIM_VirtualSystemManagementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementCapabilities
- CIM_VirtualSystemManagementCapabilities.VirtualSystemTypesSupported
- CIM_VirtualSystemManagementCapabilities.SynchronousMethodsSupported
- CIM_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported
- CIM_VirtualSystemManagementCapabilities.IndicationsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2772068ed011a2a61cdd4f5c1396e057838b7720
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543491"
---
# <a name="cim_virtualsystemmanagementcapabilities-class"></a><span data-ttu-id="7e035-103">\_Classe CIM VirtualSystemManagementCapabilities</span><span class="sxs-lookup"><span data-stu-id="7e035-103">CIM\_VirtualSystemManagementCapabilities class</span></span>

<span data-ttu-id="7e035-104">Représente les fonctionnalités d’un objet [**CIM \_ VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="7e035-104">Represents the capabilities of a [**CIM\_VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e035-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e035-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemManagementCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string VirtualSystemTypesSupported[];
  uint16 SynchronousMethodsSupported[];
  uint16 AsynchronousMethodsSupported[];
  uint16 IndicationsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="7e035-106">Membres</span><span class="sxs-lookup"><span data-stu-id="7e035-106">Members</span></span>

<span data-ttu-id="7e035-107">La classe **CIM \_ VirtualSystemManagementCapabilities** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7e035-107">The **CIM\_VirtualSystemManagementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="7e035-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7e035-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7e035-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7e035-109">Properties</span></span>

<span data-ttu-id="7e035-110">La classe **CIM \_ VirtualSystemManagementCapabilities** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7e035-110">The **CIM\_VirtualSystemManagementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7e035-111">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="7e035-111">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e035-112">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7e035-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7e035-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7e035-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e035-114">Tableau qui contient des noms de méthode pour les méthodes de classe [**\_ VirtualSystemManagementService CIM**](cim-virtualsystemmanagementservice.md) qui sont prises en charge pour les opérations asynchrones.</span><span class="sxs-lookup"><span data-stu-id="7e035-114">An array that contains method names for the [**CIM\_VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) class methods that are supported for asynchronous operations.</span></span>

<dt>

<span id="DefineSystemSupported"></span><span id="definesystemsupported"></span><span id="DEFINESYSTEMSUPPORTED"></span>

<span data-ttu-id="7e035-115">**DefineSystemSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="7e035-115">**DefineSystemSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemSupported"></span><span id="destroysystemsupported"></span><span id="DESTROYSYSTEMSUPPORTED"></span>

<span data-ttu-id="7e035-116">**DestroySystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="7e035-116">**DestroySystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemConfigurationSupported"></span><span id="destroysystemconfigurationsupported"></span><span id="DESTROYSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="7e035-117">**DestroySystemConfigurationSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="7e035-117">**DestroySystemConfigurationSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyResourceSettingsSupported"></span><span id="modifyresourcesettingssupported"></span><span id="MODIFYRESOURCESETTINGSSUPPORTED"></span>

<span data-ttu-id="7e035-118">**ModifyResourceSettingsSupported** (5)</span><span class="sxs-lookup"><span data-stu-id="7e035-118">**ModifyResourceSettingsSupported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifySystemSettingsSupported"></span><span id="modifysystemsettingssupported"></span><span id="MODIFYSYSTEMSETTINGSSUPPORTED"></span>

<span data-ttu-id="7e035-119">**ModifySystemSettingsSupported** (6)</span><span class="sxs-lookup"><span data-stu-id="7e035-119">**ModifySystemSettingsSupported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesSupported"></span><span id="removeresourcessupported"></span><span id="REMOVERESOURCESSUPPORTED"></span>

<span data-ttu-id="7e035-120">**RemoveResourcesSupported** (7)</span><span class="sxs-lookup"><span data-stu-id="7e035-120">**RemoveResourcesSupported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SelectSystemConfigurationSupported"></span><span id="selectsystemconfigurationsupported"></span><span id="SELECTSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="7e035-121">**SelectSystemConfigurationSupported** (8)</span><span class="sxs-lookup"><span data-stu-id="7e035-121">**SelectSystemConfigurationSupported** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SnapshotSystemSupported"></span><span id="snapshotsystemsupported"></span><span id="SNAPSHOTSYSTEMSUPPORTED"></span>

<span data-ttu-id="7e035-122">**SnapshotSystemSupported** (9)</span><span class="sxs-lookup"><span data-stu-id="7e035-122">**SnapshotSystemSupported** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesSupported"></span><span id="addresourcessupported"></span><span id="ADDRESOURCESSUPPORTED"></span>

<span data-ttu-id="7e035-123">**AddResourcesSupported** (10)</span><span class="sxs-lookup"><span data-stu-id="7e035-123">**AddResourcesSupported** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="7e035-124">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="7e035-124">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="7e035-125">**Fournisseur réservé** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="7e035-125">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7e035-126">**IndicationsSupported**</span><span class="sxs-lookup"><span data-stu-id="7e035-126">**IndicationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e035-127">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7e035-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7e035-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7e035-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e035-129">Tableau qui contient les types d’indications pris en charge de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="7e035-129">An array that contains the supported indications types of the implementation.</span></span>

<dt>

<span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="7e035-130">**VirtualResourceStateChangeIndicationsSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="7e035-130">**VirtualResourceStateChangeIndicationsSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="7e035-131">**ConcreteJobStateChangeIndicationsSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="7e035-131">**ConcreteJobStateChangeIndicationsSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="7e035-132">**VirtualSystemStateChangeIndicationsSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="7e035-132">**VirtualSystemStateChangeIndicationsSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="7e035-133">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="7e035-133">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="7e035-134">**Fournisseur réservé** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="7e035-134">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7e035-135">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="7e035-135">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e035-136">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7e035-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7e035-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7e035-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e035-138">Tableau qui contient des noms de méthodes pour les méthodes de la classe [**\_ VirtualSystemManagementService CIM**](cim-virtualsystemmanagementservice.md) qui sont prises en charge pour les opérations synchrones.</span><span class="sxs-lookup"><span data-stu-id="7e035-138">An array that contains method names for the [**CIM\_VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) class methods that are supported for synchronous operations.</span></span>

<dt>

<span id="DefineSystemSupported"></span><span id="definesystemsupported"></span><span id="DEFINESYSTEMSUPPORTED"></span>

<span data-ttu-id="7e035-139">**DefineSystemSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="7e035-139">**DefineSystemSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemSupported"></span><span id="destroysystemsupported"></span><span id="DESTROYSYSTEMSUPPORTED"></span>

<span data-ttu-id="7e035-140">**DestroySystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="7e035-140">**DestroySystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemConfigurationSupported"></span><span id="destroysystemconfigurationsupported"></span><span id="DESTROYSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="7e035-141">**DestroySystemConfigurationSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="7e035-141">**DestroySystemConfigurationSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyResourceSettingsSupported"></span><span id="modifyresourcesettingssupported"></span><span id="MODIFYRESOURCESETTINGSSUPPORTED"></span>

<span data-ttu-id="7e035-142">**ModifyResourceSettingsSupported** (5)</span><span class="sxs-lookup"><span data-stu-id="7e035-142">**ModifyResourceSettingsSupported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifySystemSettingsSupported"></span><span id="modifysystemsettingssupported"></span><span id="MODIFYSYSTEMSETTINGSSUPPORTED"></span>

<span data-ttu-id="7e035-143">**ModifySystemSettingsSupported** (6)</span><span class="sxs-lookup"><span data-stu-id="7e035-143">**ModifySystemSettingsSupported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesSupported"></span><span id="removeresourcessupported"></span><span id="REMOVERESOURCESSUPPORTED"></span>

<span data-ttu-id="7e035-144">**RemoveResourcesSupported** (7)</span><span class="sxs-lookup"><span data-stu-id="7e035-144">**RemoveResourcesSupported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SelectSystemConfigurationSupported"></span><span id="selectsystemconfigurationsupported"></span><span id="SELECTSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="7e035-145">**SelectSystemConfigurationSupported** (8)</span><span class="sxs-lookup"><span data-stu-id="7e035-145">**SelectSystemConfigurationSupported** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SnapshotSystemSupported"></span><span id="snapshotsystemsupported"></span><span id="SNAPSHOTSYSTEMSUPPORTED"></span>

<span data-ttu-id="7e035-146">**SnapshotSystemSupported** (9)</span><span class="sxs-lookup"><span data-stu-id="7e035-146">**SnapshotSystemSupported** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesSupported"></span><span id="addresourcessupported"></span><span id="ADDRESOURCESSUPPORTED"></span>

<span data-ttu-id="7e035-147">**AddResourcesSupported** (10)</span><span class="sxs-lookup"><span data-stu-id="7e035-147">**AddResourcesSupported** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="7e035-148">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="7e035-148">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="7e035-149">**Fournisseur réservé** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="7e035-149">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7e035-150">**VirtualSystemTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="7e035-150">**VirtualSystemTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e035-151">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="7e035-151">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7e035-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7e035-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e035-153">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md).**VirtualSystemType**")</span><span class="sxs-lookup"><span data-stu-id="7e035-153">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md).**VirtualSystemType**")</span></span>
</dt> </dl>

<span data-ttu-id="7e035-154">Type des systèmes virtuels pris en charge par l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="7e035-154">The type of virtual systems supported by the implementation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e035-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e035-155">Requirements</span></span>



| <span data-ttu-id="7e035-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e035-156">Requirement</span></span> | <span data-ttu-id="7e035-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e035-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e035-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e035-158">Minimum supported client</span></span><br/> | <span data-ttu-id="7e035-159">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7e035-159">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="7e035-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e035-160">Minimum supported server</span></span><br/> | <span data-ttu-id="7e035-161">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7e035-161">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="7e035-162">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7e035-162">Namespace</span></span><br/>                | <span data-ttu-id="7e035-163">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="7e035-163">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7e035-164">MOF</span><span class="sxs-lookup"><span data-stu-id="7e035-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e035-165"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e035-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e035-166">DLL</span><span class="sxs-lookup"><span data-stu-id="7e035-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e035-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7e035-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7e035-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e035-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e035-169">**\_ENABLEDLOGICALELEMENTCAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="7e035-169">**CIM\_EnabledLogicalElementCapabilities**</span></span>](cim-enabledlogicalelementcapabilities.md)
</dt> </dl>

 

