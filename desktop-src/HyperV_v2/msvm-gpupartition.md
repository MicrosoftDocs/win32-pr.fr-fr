---
description: Représente l’état de la partition GPU.
ms.assetid: 319b37d5-b5f0-4251-9482-316347a9015b
title: Classe Msvm_GpuPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GpuPartition
- Msvm_GpuPartition.DeviceInstancePath
- Msvm_GpuPartition.PartitionId
- Msvm_GpuPartition.PartitionVfLuid
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cc0975644609832c692f5522cc756240f7a5bff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524891"
---
# <a name="msvm_gpupartition-class"></a><span data-ttu-id="e397d-103">MSVM \_ GpuPartition, classe</span><span class="sxs-lookup"><span data-stu-id="e397d-103">Msvm\_GpuPartition class</span></span>

<span data-ttu-id="e397d-104">Représente l’état de la partition GPU.</span><span class="sxs-lookup"><span data-stu-id="e397d-104">Represents the state of the GPU partition.</span></span>

<span data-ttu-id="e397d-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e397d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e397d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e397d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GpuPartition : CIM_LogicalDevice
{
  string DeviceInstancePath;
  uint16 PartitionId;
  string PartitionVfLuid;
};
```

## <a name="members"></a><span data-ttu-id="e397d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="e397d-107">Members</span></span>

<span data-ttu-id="e397d-108">La classe **MSVM \_ GpuPartition** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e397d-108">The **Msvm\_GpuPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="e397d-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e397d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e397d-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e397d-110">Properties</span></span>

<span data-ttu-id="e397d-111">La classe **MSVM \_ GpuPartition** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e397d-111">The **Msvm\_GpuPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e397d-112">**DeviceInstancePath**</span><span class="sxs-lookup"><span data-stu-id="e397d-112">**DeviceInstancePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e397d-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e397d-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e397d-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e397d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e397d-115">Chaîne contenant le chemin d’accès à l’instance d’appareil qui identifie l’unité de partition GPU.</span><span class="sxs-lookup"><span data-stu-id="e397d-115">A string containing the device instance path that identifies the GPU partition device.</span></span>

</dd> <dt>

<span data-ttu-id="e397d-116">**PartitionId**</span><span class="sxs-lookup"><span data-stu-id="e397d-116">**PartitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e397d-117">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e397d-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e397d-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e397d-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e397d-119">ID de partition de l’unité de partition GPU.</span><span class="sxs-lookup"><span data-stu-id="e397d-119">The partition ID of the GPU partition device.</span></span>

</dd> <dt>

<span data-ttu-id="e397d-120">**PartitionVfLuid**</span><span class="sxs-lookup"><span data-stu-id="e397d-120">**PartitionVfLuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e397d-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e397d-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e397d-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e397d-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e397d-123">La fonction virtuelle LUID, qui représente une partition GPU.</span><span class="sxs-lookup"><span data-stu-id="e397d-123">The virtual function LUID, which represents a GPU partition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e397d-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e397d-124">Requirements</span></span>



| <span data-ttu-id="e397d-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e397d-125">Requirement</span></span> | <span data-ttu-id="e397d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="e397d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e397d-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e397d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e397d-128">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e397d-128">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e397d-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e397d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e397d-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e397d-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e397d-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e397d-131">Namespace</span></span><br/>                | <span data-ttu-id="e397d-132">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e397d-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e397d-133">MOF</span><span class="sxs-lookup"><span data-stu-id="e397d-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e397d-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e397d-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e397d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e397d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e397d-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e397d-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e397d-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e397d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e397d-138">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="e397d-138">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




