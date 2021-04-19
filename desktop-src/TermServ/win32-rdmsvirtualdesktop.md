---
title: Classe Win32_RDMSVirtualDesktop
description: Représente un bureau virtuel.
ms.assetid: e2952ec0-38d0-4a1c-b423-3ae1fbc701b3
ms.tgt_platform: multiple
keywords:
- Win32_RDMSVirtualDesktop de la classe Services Bureau à distance
- Win32_RDMSVirtualDesktop de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop.Name
- Win32_RDMSVirtualDesktop.HostName
- Win32_RDMSVirtualDesktop.Status
- Win32_RDMSVirtualDesktop.CollectionAlias
- Win32_RDMSVirtualDesktop.SessionState
- Win32_RDMSVirtualDesktop.SessionUserName
- Win32_RDMSVirtualDesktop.UserName
- Win32_RDMSVirtualDesktop.UserDomain
- Win32_RDMSVirtualDesktop.VMState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 247c49c7ad069b4feff3469ac21ec803ebc9f741
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510531"
---
# <a name="win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="fee98-105">\_Classe RDMSVirtualDesktop Win32</span><span class="sxs-lookup"><span data-stu-id="fee98-105">Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="fee98-106">Représente un bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="fee98-106">Represents a virtual desktop.</span></span>

<span data-ttu-id="fee98-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fee98-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fee98-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fee98-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktop
{
  string Name;
  string HostName;
  uint32 Status;
  string CollectionAlias;
  string SessionState;
  string SessionUserName;
  string UserName;
  string UserDomain;
  uint32 VMState;
};
```

## <a name="members"></a><span data-ttu-id="fee98-109">Membres</span><span class="sxs-lookup"><span data-stu-id="fee98-109">Members</span></span>

<span data-ttu-id="fee98-110">La classe **Win32 \_ RDMSVirtualDesktop** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fee98-110">The **Win32\_RDMSVirtualDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="fee98-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fee98-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="fee98-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fee98-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fee98-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fee98-113">Methods</span></span>

<span data-ttu-id="fee98-114">La classe **Win32 \_ RDMSVirtualDesktop** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="fee98-114">The **Win32\_RDMSVirtualDesktop** class has these methods.</span></span>



| <span data-ttu-id="fee98-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="fee98-115">Method</span></span>                                                                                              | <span data-ttu-id="fee98-116">Description</span><span class="sxs-lookup"><span data-stu-id="fee98-116">Description</span></span>                                                                                            |
|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fee98-117">**GetUserAssignment**</span><span class="sxs-lookup"><span data-stu-id="fee98-117">**GetUserAssignment**</span></span>](getuserassignment-win32-rdmsvirtualdesktop.md)                             | <span data-ttu-id="fee98-118">Récupère le nom d’utilisateur et le nom de domaine de l’utilisateur affecté au bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="fee98-118">Retrieves the username and domain name of the user that is assigned to the virtual desktop.</span></span><br/> |
| [<span data-ttu-id="fee98-119">**GetVirtualDesktopAssignedToUser**</span><span class="sxs-lookup"><span data-stu-id="fee98-119">**GetVirtualDesktopAssignedToUser**</span></span>](getvirtualdesktopassignedtouser-win32-rdmsvirtualdesktop.md) | <span data-ttu-id="fee98-120">Récupère le bureau virtuel affecté à l’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="fee98-120">Retrieves the virtual desktop that is assigned to the specified user.</span></span><br/>                       |
| [<span data-ttu-id="fee98-121">**GetVirtualDesktopDetails**</span><span class="sxs-lookup"><span data-stu-id="fee98-121">**GetVirtualDesktopDetails**</span></span>](getvirtualdesktopdetails-win32-rdmsvirtualdesktop.md)               | <span data-ttu-id="fee98-122">Récupère les informations supplémentaires sur le bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="fee98-122">Retrieves the additional information about the virtual desktop.</span></span><br/>                             |
| [<span data-ttu-id="fee98-123">**GetVirtualDesktopState**</span><span class="sxs-lookup"><span data-stu-id="fee98-123">**GetVirtualDesktopState**</span></span>](getvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | <span data-ttu-id="fee98-124">Récupère l’état du bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="fee98-124">Retrieves the state of the virtual desktop.</span></span><br/>                                                 |
| [<span data-ttu-id="fee98-125">**RemoveUserAssignment**</span><span class="sxs-lookup"><span data-stu-id="fee98-125">**RemoveUserAssignment**</span></span>](removeuserassignment-win32-rdmsvirtualdesktop.md)                       | <span data-ttu-id="fee98-126">Supprime l’affectation d’utilisateur du bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="fee98-126">Removes the user assignment from the virtual desktop.</span></span><br/>                                       |
| [<span data-ttu-id="fee98-127">**SetUserAssignment**</span><span class="sxs-lookup"><span data-stu-id="fee98-127">**SetUserAssignment**</span></span>](setuserassignment-win32-rdmsvirtualdesktop.md)                             | <span data-ttu-id="fee98-128">Affecte un bureau virtuel à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fee98-128">Assigns a virtual desktop to a user.</span></span><br/>                                                        |
| [<span data-ttu-id="fee98-129">**SetVirtualDesktopState**</span><span class="sxs-lookup"><span data-stu-id="fee98-129">**SetVirtualDesktopState**</span></span>](setvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | <span data-ttu-id="fee98-130">Met à jour l’état du bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="fee98-130">Updates the state of the virtual desktop.</span></span><br/>                                                   |



 

### <a name="properties"></a><span data-ttu-id="fee98-131">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fee98-131">Properties</span></span>

<span data-ttu-id="fee98-132">La classe **Win32 \_ RDMSVirtualDesktop** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fee98-132">The **Win32\_RDMSVirtualDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fee98-133">**CollectionAlias**</span><span class="sxs-lookup"><span data-stu-id="fee98-133">**CollectionAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fee98-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fee98-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fee98-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fee98-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fee98-136">Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fee98-136">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fee98-137">Obtient l’alias de la collection de bureaux virtuels qui gère l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="fee98-137">Gets the alias to the virtual desktop collection that manages the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="fee98-138">**HostName**</span><span class="sxs-lookup"><span data-stu-id="fee98-138">**HostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fee98-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fee98-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fee98-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fee98-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fee98-141">Obtient le nom de l’ordinateur qui héberge l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="fee98-141">Gets the name of the machine that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="fee98-142">**Nom**</span><span class="sxs-lookup"><span data-stu-id="fee98-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fee98-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fee98-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fee98-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fee98-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fee98-145">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fee98-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fee98-146">Obtient le nom de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="fee98-146">Gets the name of the of virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="fee98-147">**SessionState**</span><span class="sxs-lookup"><span data-stu-id="fee98-147">**SessionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fee98-148">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fee98-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fee98-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fee98-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fee98-150">Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fee98-150">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fee98-151">Obtient l’état de la session de bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="fee98-151">Gets the state of the virtual desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="fee98-152">**SessionUserName**</span><span class="sxs-lookup"><span data-stu-id="fee98-152">**SessionUserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fee98-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fee98-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fee98-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fee98-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fee98-155">Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fee98-155">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fee98-156">Obtient le nom d’utilisateur de l’utilisateur qui est connecté à la session de bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="fee98-156">Gets the username of the user that is logged in to the virtual desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="fee98-157">**État**</span><span class="sxs-lookup"><span data-stu-id="fee98-157">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fee98-158">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fee98-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fee98-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fee98-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fee98-160">Obtient l’état de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="fee98-160">Gets the status of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="fee98-161">**UserDomain**</span><span class="sxs-lookup"><span data-stu-id="fee98-161">**UserDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fee98-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fee98-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fee98-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fee98-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fee98-164">Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fee98-164">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fee98-165">Obtient le nom de domaine de l’utilisateur affecté au bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="fee98-165">Gets the domain name of the user that is assigned to the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="fee98-166">**UserName**</span><span class="sxs-lookup"><span data-stu-id="fee98-166">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fee98-167">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fee98-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fee98-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fee98-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fee98-169">Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fee98-169">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fee98-170">Obtient le nom d’utilisateur de l’utilisateur affecté au bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="fee98-170">Gets the username of the user that is assigned to the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="fee98-171">**VMState**</span><span class="sxs-lookup"><span data-stu-id="fee98-171">**VMState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fee98-172">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fee98-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fee98-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fee98-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fee98-174">Obtient l’état du bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="fee98-174">Gets the state of the virtual desktop.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fee98-175">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fee98-175">Requirements</span></span>



| <span data-ttu-id="fee98-176">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fee98-176">Requirement</span></span> | <span data-ttu-id="fee98-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="fee98-177">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fee98-178">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fee98-178">Minimum supported client</span></span><br/> | <span data-ttu-id="fee98-179">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fee98-179">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="fee98-180">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fee98-180">Minimum supported server</span></span><br/> | <span data-ttu-id="fee98-181">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fee98-181">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="fee98-182">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fee98-182">Namespace</span></span><br/>                | <span data-ttu-id="fee98-183">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="fee98-183">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="fee98-184">MOF</span><span class="sxs-lookup"><span data-stu-id="fee98-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fee98-185"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fee98-185"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="fee98-186">DLL</span><span class="sxs-lookup"><span data-stu-id="fee98-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fee98-187"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fee98-187"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="fee98-188">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fee98-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fee98-189">Fournisseur de services de gestion Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="fee98-189">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

