---
title: Classe Win32_RDMSCollectionProperties
description: Gère les propriétés d’une collection de bureaux virtuels.
ms.assetid: 8c533284-aa7b-4c47-b0a3-33307c4c805b
ms.tgt_platform: multiple
keywords:
- Win32_RDMSCollectionProperties de la classe Services Bureau à distance
- Win32_RDMSCollectionProperties de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties
- Win32_RDMSCollectionProperties.Alias
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopMachineName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopHost
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopGuid
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopOsversion
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRamsizeMB
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopArchitecture
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRemoteFX
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopAdapters
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7397ccc1afd350689ac1eeb984a62177140f50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384448"
---
# <a name="win32_rdmscollectionproperties-class"></a><span data-ttu-id="5cfec-105">\_Classe RDMSCollectionProperties Win32</span><span class="sxs-lookup"><span data-stu-id="5cfec-105">Win32\_RDMSCollectionProperties class</span></span>

<span data-ttu-id="5cfec-106">Gère les propriétés d’une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="5cfec-106">Manages the properties of a virtual desktop collection.</span></span>

<span data-ttu-id="5cfec-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5cfec-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cfec-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5cfec-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSCollectionProperties
{
  string  Alias;
  string  ReferenceVirtualDesktopName;
  string  ReferenceVirtualDesktopMachineName;
  string  ReferenceVirtualDesktopHost;
  string  ReferenceVirtualDesktopGuid;
  string  ReferenceVirtualDesktopOsversion;
  uint32  ReferenceVirtualDesktopRamsizeMB;
  string  ReferenceVirtualDesktopArchitecture;
  boolean ReferenceVirtualDesktopRemoteFX = false;
  string  ReferenceVirtualDesktopAdapters[];
};
```

## <a name="members"></a><span data-ttu-id="5cfec-109">Membres</span><span class="sxs-lookup"><span data-stu-id="5cfec-109">Members</span></span>

<span data-ttu-id="5cfec-110">La classe **Win32 \_ RDMSCollectionProperties** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5cfec-110">The **Win32\_RDMSCollectionProperties** class has these types of members:</span></span>

-   [<span data-ttu-id="5cfec-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5cfec-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="5cfec-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5cfec-112">Properties</span></span>](/windows)

### <a name="methods"></a><span data-ttu-id="5cfec-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5cfec-113">Methods</span></span>

<span data-ttu-id="5cfec-114">La classe **Win32 \_ RDMSCollectionProperties** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="5cfec-114">The **Win32\_RDMSCollectionProperties** class has these methods.</span></span>



| <span data-ttu-id="5cfec-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="5cfec-115">Method</span></span>                                                                                        | <span data-ttu-id="5cfec-116">Description</span><span class="sxs-lookup"><span data-stu-id="5cfec-116">Description</span></span>                                                                         |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="5cfec-117">**GetProvisioningProperties**</span><span class="sxs-lookup"><span data-stu-id="5cfec-117">**GetProvisioningProperties**</span></span>](getprovisioningproperties-win32-rdmscollectionproperties.md) | <span data-ttu-id="5cfec-118">Récupère les propriétés de configuration de la collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="5cfec-118">Retrieves the provisioning properties of the virtual desktop collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5cfec-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5cfec-119">Properties</span></span>

<span data-ttu-id="5cfec-120">La classe **Win32 \_ RDMSCollectionProperties** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5cfec-120">The **Win32\_RDMSCollectionProperties** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5cfec-121">**Alias**</span><span class="sxs-lookup"><span data-stu-id="5cfec-121">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cfec-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5cfec-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5cfec-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5cfec-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5cfec-124">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5cfec-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5cfec-125">Obtient l’alias de la collection.</span><span class="sxs-lookup"><span data-stu-id="5cfec-125">Gets the alias of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="5cfec-126">**ReferenceVirtualDesktopAdapters**</span><span class="sxs-lookup"><span data-stu-id="5cfec-126">**ReferenceVirtualDesktopAdapters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cfec-127">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="5cfec-127">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5cfec-128">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5cfec-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5cfec-129">Obtient et définit les noms des cartes réseau virtuelles de la machine virtuelle maître.</span><span class="sxs-lookup"><span data-stu-id="5cfec-129">Gets and sets the names of the virtual network adapters of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="5cfec-130">**ReferenceVirtualDesktopArchitecture**</span><span class="sxs-lookup"><span data-stu-id="5cfec-130">**ReferenceVirtualDesktopArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cfec-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5cfec-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5cfec-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5cfec-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5cfec-133">Obtient et définit l’architecture de processeur de la machine virtuelle maître.</span><span class="sxs-lookup"><span data-stu-id="5cfec-133">Gets and sets the processor architecture of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="5cfec-134">**ReferenceVirtualDesktopGuid**</span><span class="sxs-lookup"><span data-stu-id="5cfec-134">**ReferenceVirtualDesktopGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cfec-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5cfec-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5cfec-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5cfec-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5cfec-137">Obtient et définit le GUID de la machine virtuelle principale.</span><span class="sxs-lookup"><span data-stu-id="5cfec-137">Gets and sets the GUID of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="5cfec-138">**ReferenceVirtualDesktopHost**</span><span class="sxs-lookup"><span data-stu-id="5cfec-138">**ReferenceVirtualDesktopHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cfec-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5cfec-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5cfec-140">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5cfec-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5cfec-141">Obtient et définit le nom du serveur hôte de la machine virtuelle maître.</span><span class="sxs-lookup"><span data-stu-id="5cfec-141">Gets and sets the host server name of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="5cfec-142">**ReferenceVirtualDesktopMachineName**</span><span class="sxs-lookup"><span data-stu-id="5cfec-142">**ReferenceVirtualDesktopMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cfec-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5cfec-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5cfec-144">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5cfec-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5cfec-145">Obtient et définit le nom d’ordinateur de la machine virtuelle maître.</span><span class="sxs-lookup"><span data-stu-id="5cfec-145">Gets and sets the machine name of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="5cfec-146">**ReferenceVirtualDesktopName**</span><span class="sxs-lookup"><span data-stu-id="5cfec-146">**ReferenceVirtualDesktopName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cfec-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5cfec-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5cfec-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5cfec-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5cfec-149">Obtient et définit le nom de la machine virtuelle maître.</span><span class="sxs-lookup"><span data-stu-id="5cfec-149">Gets and sets the name of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="5cfec-150">**ReferenceVirtualDesktopOsversion**</span><span class="sxs-lookup"><span data-stu-id="5cfec-150">**ReferenceVirtualDesktopOsversion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cfec-151">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5cfec-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5cfec-152">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5cfec-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5cfec-153">Obtient et définit la version du système d’exploitation de la machine virtuelle principale.</span><span class="sxs-lookup"><span data-stu-id="5cfec-153">Gets and sets the OS version of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="5cfec-154">**ReferenceVirtualDesktopRamsizeMB**</span><span class="sxs-lookup"><span data-stu-id="5cfec-154">**ReferenceVirtualDesktopRamsizeMB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cfec-155">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5cfec-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5cfec-156">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5cfec-156">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5cfec-157">Obtient et définit la taille de la mémoire de la machine virtuelle principale.</span><span class="sxs-lookup"><span data-stu-id="5cfec-157">Gets and sets the memory size of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="5cfec-158">**ReferenceVirtualDesktopRemoteFX**</span><span class="sxs-lookup"><span data-stu-id="5cfec-158">**ReferenceVirtualDesktopRemoteFX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cfec-159">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5cfec-159">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5cfec-160">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5cfec-160">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5cfec-161">Obtient et définit une valeur qui indique si RemoteFX est activé pour la machine virtuelle Master.</span><span class="sxs-lookup"><span data-stu-id="5cfec-161">Gets and sets a value that indicates whether RemoteFX is enabled for the master VM.</span></span> <span data-ttu-id="5cfec-162">**True** si RemoteFX est activé ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="5cfec-162">**TRUE** if RemoteFX is enabled; otherwise, **FALSE**.</span></span> <span data-ttu-id="5cfec-163">La valeur par défaut de cette propriété est **false**.</span><span class="sxs-lookup"><span data-stu-id="5cfec-163">The default value for this property is **FALSE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5cfec-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5cfec-164">Requirements</span></span>



| <span data-ttu-id="5cfec-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5cfec-165">Requirement</span></span> | <span data-ttu-id="5cfec-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cfec-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cfec-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5cfec-167">Minimum supported client</span></span><br/> | <span data-ttu-id="5cfec-168">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5cfec-168">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="5cfec-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5cfec-169">Minimum supported server</span></span><br/> | <span data-ttu-id="5cfec-170">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5cfec-170">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="5cfec-171">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5cfec-171">Namespace</span></span><br/>                | <span data-ttu-id="5cfec-172">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="5cfec-172">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="5cfec-173">MOF</span><span class="sxs-lookup"><span data-stu-id="5cfec-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5cfec-174"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5cfec-174"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="5cfec-175">DLL</span><span class="sxs-lookup"><span data-stu-id="5cfec-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5cfec-176"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5cfec-176"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="5cfec-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5cfec-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cfec-178">Fournisseur de services de gestion Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="5cfec-178">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

