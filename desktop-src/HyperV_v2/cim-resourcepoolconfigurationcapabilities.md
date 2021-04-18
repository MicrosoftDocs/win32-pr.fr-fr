---
description: Gère les fonctionnalités de l' \_ instance CIM ResourcePoolConfigurationService pour un \_ objet ResourcePool CIM.
ms.assetid: bd2eb4da-8ecd-4adb-b657-837c8da4dcdc
title: Classe CIM_ResourcePoolConfigurationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationCapabilities
- CIM_ResourcePoolConfigurationCapabilities.AsynchronousMethodsSupported
- CIM_ResourcePoolConfigurationCapabilities.SynchronousMethodsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 967b307049fa9c5f81b8deb6da96bcaa3be9acc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513002"
---
# <a name="cim_resourcepoolconfigurationcapabilities-class"></a><span data-ttu-id="03620-103">\_Classe CIM ResourcePoolConfigurationCapabilities</span><span class="sxs-lookup"><span data-stu-id="03620-103">CIM\_ResourcePoolConfigurationCapabilities class</span></span>

<span data-ttu-id="03620-104">Gère les fonctionnalités de l’instance [**CIM \_ ResourcePoolConfigurationService**](cim-resourcepoolconfigurationservice.md) pour un [**objet \_ ResourcePool CIM**](cim-resourcepool.md) .</span><span class="sxs-lookup"><span data-stu-id="03620-104">Manages the capabilities of the [**CIM\_ResourcePoolConfigurationService**](cim-resourcepoolconfigurationservice.md) instance for a [**CIM\_ResourcePool**](cim-resourcepool.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="03620-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03620-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_ResourcePoolConfigurationCapabilities : CIM_Capabilities
{
  uint32 AsynchronousMethodsSupported[];
  uint32 SynchronousMethodsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="03620-106">Membres</span><span class="sxs-lookup"><span data-stu-id="03620-106">Members</span></span>

<span data-ttu-id="03620-107">La classe **CIM \_ ResourcePoolConfigurationCapabilities** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="03620-107">The **CIM\_ResourcePoolConfigurationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="03620-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="03620-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03620-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="03620-109">Properties</span></span>

<span data-ttu-id="03620-110">La classe **CIM \_ ResourcePoolConfigurationCapabilities** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="03620-110">The **CIM\_ResourcePoolConfigurationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03620-111">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="03620-111">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03620-112">Type de données : tableau **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03620-112">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="03620-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="03620-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03620-114">Méthodes du service de configuration prises en charge pour les opérations asynchrones.</span><span class="sxs-lookup"><span data-stu-id="03620-114">The methods of the configuration service that are supported for asynchronous operations.</span></span>

<dt>

<span id="CreateResourcePool_is_supported"></span><span id="createresourcepool_is_supported"></span><span id="CREATERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="03620-115">**CreateResourcePool est pris en charge** (2)</span><span class="sxs-lookup"><span data-stu-id="03620-115">**CreateResourcePool is supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CreateChild_ResourcePool_is_supported"></span><span id="createchild_resourcepool_is_supported"></span><span id="CREATECHILD_RESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="03620-116">**CreateChild ResourcePool est pris en charge** (3)</span><span class="sxs-lookup"><span data-stu-id="03620-116">**CreateChild ResourcePool is supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DeleteResourcePool_is_supported"></span><span id="deleteresourcepool_is_supported"></span><span id="DELETERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="03620-117">**DeleteResourcePool est pris en charge** (4)</span><span class="sxs-lookup"><span data-stu-id="03620-117">**DeleteResourcePool is supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesToResourcePool_is_supported"></span><span id="addresourcestoresourcepool_is_supported"></span><span id="ADDRESOURCESTORESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="03620-118">**AddResourcesToResourcePool est pris en charge** (5)</span><span class="sxs-lookup"><span data-stu-id="03620-118">**AddResourcesToResourcePool is supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesFromResourcePool_is_supported"></span><span id="removeresourcesfromresourcepool_is_supported"></span><span id="REMOVERESOURCESFROMRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="03620-119">**RemoveResourcesFromResourcePool est pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="03620-119">**RemoveResourcesFromResourcePool is supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangeParentResourcePool_is_supported"></span><span id="changeparentresourcepool_is_supported"></span><span id="CHANGEPARENTRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="03620-120">**ChangeParentResourcePool est pris en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="03620-120">**ChangeParentResourcePool is supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="03620-121">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="03620-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="03620-122">**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="03620-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="03620-123">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="03620-123">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03620-124">Type de données : tableau **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03620-124">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="03620-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="03620-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03620-126">Méthodes du service de configuration prises en charge pour les opérations synchrones.</span><span class="sxs-lookup"><span data-stu-id="03620-126">The methods of the configuration service that are supported for synchronous operations.</span></span>

<dt>

<span id="CreateResourcePool_is_supported"></span><span id="createresourcepool_is_supported"></span><span id="CREATERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="03620-127">**CreateResourcePool est pris en charge** (2)</span><span class="sxs-lookup"><span data-stu-id="03620-127">**CreateResourcePool is supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CreateChild_ResourcePool_is_supported"></span><span id="createchild_resourcepool_is_supported"></span><span id="CREATECHILD_RESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="03620-128">**CreateChild ResourcePool est pris en charge** (3)</span><span class="sxs-lookup"><span data-stu-id="03620-128">**CreateChild ResourcePool is supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DeleteResourcePool_is_supported"></span><span id="deleteresourcepool_is_supported"></span><span id="DELETERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="03620-129">**DeleteResourcePool est pris en charge** (4)</span><span class="sxs-lookup"><span data-stu-id="03620-129">**DeleteResourcePool is supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesToResourcePool_is_supported"></span><span id="addresourcestoresourcepool_is_supported"></span><span id="ADDRESOURCESTORESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="03620-130">**AddResourcesToResourcePool est pris en charge** (5)</span><span class="sxs-lookup"><span data-stu-id="03620-130">**AddResourcesToResourcePool is supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesFromResourcePool_is_supported"></span><span id="removeresourcesfromresourcepool_is_supported"></span><span id="REMOVERESOURCESFROMRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="03620-131">**RemoveResourcesFromResourcePool est pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="03620-131">**RemoveResourcesFromResourcePool is supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="CIM_ChangeParentResourcePool_is_supported"></span><span id="cim_changeparentresourcepool_is_supported"></span><span id="CIM_CHANGEPARENTRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="03620-132">**CIM \_ ChangeParentResourcePool est pris en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="03620-132">**CIM\_ChangeParentResourcePool is supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="03620-133">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="03620-133">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="03620-134">**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="03620-134">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="03620-135"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="03620-135"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="03620-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03620-136">Requirements</span></span>



| <span data-ttu-id="03620-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03620-137">Requirement</span></span> | <span data-ttu-id="03620-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="03620-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03620-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03620-139">Minimum supported client</span></span><br/> | <span data-ttu-id="03620-140">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="03620-140">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="03620-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03620-141">Minimum supported server</span></span><br/> | <span data-ttu-id="03620-142">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="03620-142">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="03620-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="03620-143">Namespace</span></span><br/>                | <span data-ttu-id="03620-144">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="03620-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="03620-145">MOF</span><span class="sxs-lookup"><span data-stu-id="03620-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03620-146"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03620-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="03620-147">DLL</span><span class="sxs-lookup"><span data-stu-id="03620-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03620-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="03620-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="03620-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03620-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03620-150">**\_Fonctionnalités CIM**</span><span class="sxs-lookup"><span data-stu-id="03620-150">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

 




