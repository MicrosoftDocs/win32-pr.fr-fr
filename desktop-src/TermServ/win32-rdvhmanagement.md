---
title: Classe Win32_RdvhManagement
description: Décrit un service de gestion d’hôte virtuel Bureau à distance (RDVH).
ms.assetid: 2a81786c-e772-4596-9846-a46828f9b48b
ms.tgt_platform: multiple
keywords:
- Win32_RdvhManagement de la classe Services Bureau à distance
- Win32_RdvhManagement de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RdvhManagement
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01e2cde81173035d00587782dc45d9ddeb66fcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511947"
---
# <a name="win32_rdvhmanagement-class"></a><span data-ttu-id="84a3a-105">\_Classe RdvhManagement Win32</span><span class="sxs-lookup"><span data-stu-id="84a3a-105">Win32\_RdvhManagement class</span></span>

<span data-ttu-id="84a3a-106">Décrit un service de gestion d’hôte virtuel Bureau à distance (RDVH).</span><span class="sxs-lookup"><span data-stu-id="84a3a-106">Describes a Remote Desktop Virtual Host (RDVH) management service.</span></span>

<span data-ttu-id="84a3a-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="84a3a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="84a3a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84a3a-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_RdvhManagement
{
};
```

## <a name="members"></a><span data-ttu-id="84a3a-109">Membres</span><span class="sxs-lookup"><span data-stu-id="84a3a-109">Members</span></span>

<span data-ttu-id="84a3a-110">La classe **Win32 \_ RdvhManagement** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="84a3a-110">The **Win32\_RdvhManagement** class has these types of members:</span></span>

-   [<span data-ttu-id="84a3a-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="84a3a-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="84a3a-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="84a3a-112">Methods</span></span>

<span data-ttu-id="84a3a-113">La classe **Win32 \_ RdvhManagement** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="84a3a-113">The **Win32\_RdvhManagement** class has these methods.</span></span>



| <span data-ttu-id="84a3a-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="84a3a-114">Method</span></span>                                                                                  | <span data-ttu-id="84a3a-115">Description</span><span class="sxs-lookup"><span data-stu-id="84a3a-115">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84a3a-116">**RdvCreateUserDiskTemplate**</span><span class="sxs-lookup"><span data-stu-id="84a3a-116">**RdvCreateUserDiskTemplate**</span></span>](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | <span data-ttu-id="84a3a-117">Crée un modèle de disque utilisateur de taille maximale spécifiée et à l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="84a3a-117">Creates User Disk Template of specified max size and at the specified location.</span></span> <span data-ttu-id="84a3a-118">Tous les disques utilisateur créés auront des tailles maximales correspondant à la taille maximale du modèle.</span><span class="sxs-lookup"><span data-stu-id="84a3a-118">All User Disks created will have max sizes matching the Template's max size.</span></span><br/> |
| [<span data-ttu-id="84a3a-119">**RdvMigrateVmToDifferentHost**</span><span class="sxs-lookup"><span data-stu-id="84a3a-119">**RdvMigrateVmToDifferentHost**</span></span>](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | <span data-ttu-id="84a3a-120">Lance une migration dynamique de machine virtuelle dans des scénarios VDI</span><span class="sxs-lookup"><span data-stu-id="84a3a-120">Initiates a live migration of virtual machine in VDI scenarios</span></span><br/>                                                                                               |
| [<span data-ttu-id="84a3a-121">**RdvCopyBaseVmLocally**</span><span class="sxs-lookup"><span data-stu-id="84a3a-121">**RdvCopyBaseVmLocally**</span></span>](rdvcopybasevmlocally-win32-rdvhmanagement.md)               | <span data-ttu-id="84a3a-122">Copie l’emplacement de la machine virtuelle de base localement sur le serveur de Hôte de virtualisation des services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="84a3a-122">Copies Base VM location locally to RDV Host server</span></span><br/>                                                                                                           |
| [<span data-ttu-id="84a3a-123">**RdvCreateUserDiskTemplate**</span><span class="sxs-lookup"><span data-stu-id="84a3a-123">**RdvCreateUserDiskTemplate**</span></span>](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | <span data-ttu-id="84a3a-124">Crée un modèle de disque utilisateur de taille maximale spécifiée et à l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="84a3a-124">Creates User Disk Template of specified max size and at the specified location.</span></span> <span data-ttu-id="84a3a-125">Tous les disques utilisateur créés auront des tailles maximales correspondant à la taille maximale du modèle.</span><span class="sxs-lookup"><span data-stu-id="84a3a-125">All User Disks created will have max sizes matching the Template's max size.</span></span><br/> |
| [<span data-ttu-id="84a3a-126">**RdvMigrateVmToDifferentHost**</span><span class="sxs-lookup"><span data-stu-id="84a3a-126">**RdvMigrateVmToDifferentHost**</span></span>](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | <span data-ttu-id="84a3a-127">Lance une migration dynamique de machine virtuelle dans des scénarios VDI.</span><span class="sxs-lookup"><span data-stu-id="84a3a-127">Initiates a live migration of virtual machine in VDI scenarios.</span></span><br/>                                                                                              |
| [<span data-ttu-id="84a3a-128">**RdvSetupVMPermissions**</span><span class="sxs-lookup"><span data-stu-id="84a3a-128">**RdvSetupVMPermissions**</span></span>](rdvsetupvmpermissions-win32-rdvhmanagement.md)             | <span data-ttu-id="84a3a-129">Définit les autorisations dans la machine virtuelle pour l’appelant</span><span class="sxs-lookup"><span data-stu-id="84a3a-129">Sets permissions in VM for the caller</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="84a3a-130">**RdvUndoVMPermissions**</span><span class="sxs-lookup"><span data-stu-id="84a3a-130">**RdvUndoVMPermissions**</span></span>](rdvundovmpermissions-win32-rdvhmanagement.md)               | <span data-ttu-id="84a3a-131">Restaure les autorisations dans la machine virtuelle définie par RdvSetupVMPermissions</span><span class="sxs-lookup"><span data-stu-id="84a3a-131">Reverts permissions in VM set by RdvSetupVMPermissions</span></span><br/>                                                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="84a3a-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84a3a-132">Requirements</span></span>



| <span data-ttu-id="84a3a-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84a3a-133">Requirement</span></span> | <span data-ttu-id="84a3a-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="84a3a-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="84a3a-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84a3a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="84a3a-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="84a3a-136">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="84a3a-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84a3a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="84a3a-138">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="84a3a-138">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="84a3a-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="84a3a-139">Namespace</span></span><br/>                | <span data-ttu-id="84a3a-140">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="84a3a-140">Root\\cimv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="84a3a-141">MOF</span><span class="sxs-lookup"><span data-stu-id="84a3a-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84a3a-142"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84a3a-142"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="84a3a-143">DLL</span><span class="sxs-lookup"><span data-stu-id="84a3a-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84a3a-144"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84a3a-144"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

 





