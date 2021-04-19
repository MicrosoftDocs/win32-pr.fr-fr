---
description: Utilisé dans la méthode QueryGuestClusterInformation de la \_ classe MSVM VssService pour récupérer des informations sur le cluster invité dont fait partie la machine virtuelle.
ms.assetid: c484b38d-9137-44da-a368-a2a673b94ef8
title: Classe Msvm_GuestClusterInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestClusterInformation
- Msvm_GuestClusterInformation.ClusterId
- Msvm_GuestClusterInformation.ClusterSize
- Msvm_GuestClusterInformation.SharedVirtualHardDisks
- Msvm_GuestClusterInformation.SharedVirtualHardDiskPaths
- Msvm_GuestClusterInformation.IsClustered
- Msvm_GuestClusterInformation.IsOnline
- Msvm_GuestClusterInformation.IsOwned
- Msvm_GuestClusterInformation.IsActiveActive
- Msvm_GuestClusterInformation.LastResourceMoveTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ee7fa33f142e47b9493e53aa5bc4779623d6ef40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515884"
---
# <a name="msvm_guestclusterinformation-class"></a><span data-ttu-id="514e6-103">MSVM \_ GuestClusterInformation, classe</span><span class="sxs-lookup"><span data-stu-id="514e6-103">Msvm\_GuestClusterInformation class</span></span>

<span data-ttu-id="514e6-104">Utilisé dans la méthode [**QueryGuestClusterInformation**](msvm-vssservice-queryguestclusterinformation.md) de la classe [**MSVM \_ VssService**](msvm-vssservice.md) pour récupérer des informations sur le cluster invité dont fait partie la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="514e6-104">Used in the [**QueryGuestClusterInformation**](msvm-vssservice-queryguestclusterinformation.md) method in the [**Msvm\_VssService**](msvm-vssservice.md) class to retrieve information about the guest cluster the VM is part of.</span></span>

<span data-ttu-id="514e6-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="514e6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="514e6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="514e6-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestClusterInformation
{
  string  ClusterId;
  uint16  ClusterSize;
  string  SharedVirtualHardDisks[];
  string  SharedVirtualHardDiskPaths[];
  boolean IsClustered[];
  boolean IsOnline[];
  boolean IsOwned[];
  boolean IsActiveActive[];
  uint64  LastResourceMoveTime;
};
```

## <a name="members"></a><span data-ttu-id="514e6-107">Membres</span><span class="sxs-lookup"><span data-stu-id="514e6-107">Members</span></span>

<span data-ttu-id="514e6-108">La classe **MSVM \_ GuestClusterInformation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="514e6-108">The **Msvm\_GuestClusterInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="514e6-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="514e6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="514e6-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="514e6-110">Properties</span></span>

<span data-ttu-id="514e6-111">La classe **MSVM \_ GuestClusterInformation** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="514e6-111">The **Msvm\_GuestClusterInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="514e6-112">**ClusterId**</span><span class="sxs-lookup"><span data-stu-id="514e6-112">**ClusterId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="514e6-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="514e6-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="514e6-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="514e6-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="514e6-115">Identificateur du cluster de basculement dont le système d’exploitation invité de la machine virtuelle fait partie.</span><span class="sxs-lookup"><span data-stu-id="514e6-115">The identifier of the failover cluster the VM's guest Operating System is a part of.</span></span>

</dd> <dt>

<span data-ttu-id="514e6-116">**ClusterSize**</span><span class="sxs-lookup"><span data-stu-id="514e6-116">**ClusterSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="514e6-117">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="514e6-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="514e6-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="514e6-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="514e6-119">Nombre de nœuds dans le cluster dont le système d’exploitation invité de la machine virtuelle fait partie.</span><span class="sxs-lookup"><span data-stu-id="514e6-119">Number of nodes in the cluster the VM's guest Operating System is a part of.</span></span>

</dd> <dt>

<span data-ttu-id="514e6-120">**IsActiveActive**</span><span class="sxs-lookup"><span data-stu-id="514e6-120">**IsActiveActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="514e6-121">Type de données : tableau **booléen**</span><span class="sxs-lookup"><span data-stu-id="514e6-121">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="514e6-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="514e6-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="514e6-123">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="514e6-123">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="514e6-124">Tableau de valeurs booléennes correspondant à chaque disque dur virtuel partagé indiquant si la ressource de disque correspondante dans le cluster invité est partagée entre les machines virtuelles en mode actif/actif.</span><span class="sxs-lookup"><span data-stu-id="514e6-124">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk resource in the guest cluster is shared between VMs in active/active mode.</span></span>

</dd> <dt>

<span data-ttu-id="514e6-125">**IsClustered**</span><span class="sxs-lookup"><span data-stu-id="514e6-125">**IsClustered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="514e6-126">Type de données : tableau **booléen**</span><span class="sxs-lookup"><span data-stu-id="514e6-126">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="514e6-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="514e6-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="514e6-128">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="514e6-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="514e6-129">Tableau de valeurs booléennes correspondant à chaque disque dur virtuel partagé indiquant si le disque correspondant est une ressource de cluster dans le cluster invité.</span><span class="sxs-lookup"><span data-stu-id="514e6-129">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk is a cluster resource in the guest cluster.</span></span>

</dd> <dt>

<span data-ttu-id="514e6-130">**IsOnline**</span><span class="sxs-lookup"><span data-stu-id="514e6-130">**IsOnline**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="514e6-131">Type de données : tableau **booléen**</span><span class="sxs-lookup"><span data-stu-id="514e6-131">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="514e6-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="514e6-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="514e6-133">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="514e6-133">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="514e6-134">Tableau de valeurs booléennes correspondant à chaque disque dur virtuel partagé indiquant si la ressource de disque correspondante dans le cluster invité est en ligne.</span><span class="sxs-lookup"><span data-stu-id="514e6-134">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk resource in the guest cluster is online.</span></span>

</dd> <dt>

<span data-ttu-id="514e6-135">**IsOwned**</span><span class="sxs-lookup"><span data-stu-id="514e6-135">**IsOwned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="514e6-136">Type de données : tableau **booléen**</span><span class="sxs-lookup"><span data-stu-id="514e6-136">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="514e6-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="514e6-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="514e6-138">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="514e6-138">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="514e6-139">Tableau de valeurs booléennes correspondant à chaque disque dur virtuel partagé, indiquant si la ressource de disque correspondante dans le cluster invité est Currenly appartenant à cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="514e6-139">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk resource in the guest cluster is currenly owned by this VM.</span></span>

</dd> <dt>

<span data-ttu-id="514e6-140">**LastResourceMoveTime**</span><span class="sxs-lookup"><span data-stu-id="514e6-140">**LastResourceMoveTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="514e6-141">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="514e6-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="514e6-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="514e6-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="514e6-143">Nombre de battements d’horloge lors du dernier déplacement de l’une des ressources de disque partagé.</span><span class="sxs-lookup"><span data-stu-id="514e6-143">The clock tick count when one of the shared disk resources last moved.</span></span>

> [!Note]  
> <span data-ttu-id="514e6-144">Cette propriété a été ajoutée dans Windows 10, version 1703 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="514e6-144">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="514e6-145">**SharedVirtualHardDiskPaths**</span><span class="sxs-lookup"><span data-stu-id="514e6-145">**SharedVirtualHardDiskPaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="514e6-146">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="514e6-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="514e6-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="514e6-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="514e6-148">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="514e6-148">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="514e6-149">Tableau de chemins d’accès de disque dur virtuel partagés connectés à la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="514e6-149">An array of shared virtual hard disk paths connected to the VM.</span></span>

</dd> <dt>

<span data-ttu-id="514e6-150">**SharedVirtualHardDisks**</span><span class="sxs-lookup"><span data-stu-id="514e6-150">**SharedVirtualHardDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="514e6-151">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="514e6-151">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="514e6-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="514e6-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="514e6-153">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="514e6-153">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="514e6-154">Tableau de données de paramètre d’allocation de ressources (RASD) représentant les disques durs virtuels partagés connectés à la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="514e6-154">An array of Resource Allocation Setting Data (RASD) representing the shared virtual hard disks connected to the VM.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="514e6-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="514e6-155">Requirements</span></span>



| <span data-ttu-id="514e6-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="514e6-156">Requirement</span></span> | <span data-ttu-id="514e6-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="514e6-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="514e6-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="514e6-158">Minimum supported client</span></span><br/> | <span data-ttu-id="514e6-159">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="514e6-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="514e6-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="514e6-160">Minimum supported server</span></span><br/> | <span data-ttu-id="514e6-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="514e6-161">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="514e6-162">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="514e6-162">Namespace</span></span><br/>                | <span data-ttu-id="514e6-163">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="514e6-163">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="514e6-164">MOF</span><span class="sxs-lookup"><span data-stu-id="514e6-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="514e6-165"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="514e6-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="514e6-166">DLL</span><span class="sxs-lookup"><span data-stu-id="514e6-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="514e6-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="514e6-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

