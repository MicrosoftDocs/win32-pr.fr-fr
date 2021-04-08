---
title: Classe Win32_TSVirtualIP
description: Définit les paramètres de virtualisation IP (Internet Protocol) pour un serveur hôte de session Bureau à distance (hôte de session Bureau à distance).
ms.assetid: c37d572c-f6db-438b-8290-006a623c6593
ms.tgt_platform: multiple
keywords:
- Win32_TSVirtualIP de la classe Services Bureau à distance
- Win32_TSVirtualIP de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP
- Win32_TSVirtualIP.Caption
- Win32_TSVirtualIP.Description
- Win32_TSVirtualIP.InstallDate
- Win32_TSVirtualIP.Name
- Win32_TSVirtualIP.Status
- Win32_TSVirtualIP.VirtualIPActive
- Win32_TSVirtualIP.PolicySourceVirtualIPActive
- Win32_TSVirtualIP.VirtualIPMode
- Win32_TSVirtualIP.PolicySourceVirtualIPMode
- Win32_TSVirtualIP.ProgramList
- Win32_TSVirtualIP.PolicySourceProgramList
- Win32_TSVirtualIP.NetworkAdapterDescription
- Win32_TSVirtualIP.NetworkAdapterMacAddress
- Win32_TSVirtualIP.PolicySourceNetworkAdapter
- Win32_TSVirtualIP.NetworkAdapterDescriptionList
- Win32_TSVirtualIP.NetworkAdapterMacList
- Win32_TSVirtualIP.VirtualizeLoopbackAddressesEnabled
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f87db04d61dda0c6034b536544362ec09e0aaa66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740181"
---
# <a name="win32_tsvirtualip-class"></a><span data-ttu-id="1e69b-105">\_Classe TSVirtualIP Win32</span><span class="sxs-lookup"><span data-stu-id="1e69b-105">Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="1e69b-106">Définit les paramètres de virtualisation IP (Internet Protocol) pour un serveur hôte de session Bureau à distance (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="1e69b-106">Defines Internet protocol (IP) virtualization settings for a Remote Desktop Session Host (RD Session Host) server.</span></span>

<span data-ttu-id="1e69b-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="1e69b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e69b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e69b-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSVIRTUALIP_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\TSAppSrv\\VirtualIP"), AMENDMENT]
class Win32_TSVirtualIP : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint32   VirtualIPActive;
  uint32   PolicySourceVirtualIPActive;
  uint32   VirtualIPMode;
  uint32   PolicySourceVirtualIPMode;
  string   ProgramList[];
  uint32   PolicySourceProgramList;
  string   NetworkAdapterDescription;
  string   NetworkAdapterMacAddress;
  uint32   PolicySourceNetworkAdapter;
  string   NetworkAdapterDescriptionList[];
  string   NetworkAdapterMacList[];
  uint32   VirtualizeLoopbackAddressesEnabled;
};
```

## <a name="members"></a><span data-ttu-id="1e69b-109">Membres</span><span class="sxs-lookup"><span data-stu-id="1e69b-109">Members</span></span>

<span data-ttu-id="1e69b-110">La classe **Win32 \_ TSVirtualIP** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1e69b-110">The **Win32\_TSVirtualIP** class has these types of members:</span></span>

-   [<span data-ttu-id="1e69b-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1e69b-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="1e69b-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1e69b-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1e69b-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1e69b-113">Methods</span></span>

<span data-ttu-id="1e69b-114">La classe **Win32 \_ TSVirtualIP** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="1e69b-114">The **Win32\_TSVirtualIP** class has these methods.</span></span>



| <span data-ttu-id="1e69b-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="1e69b-115">Method</span></span>                                                                                                   | <span data-ttu-id="1e69b-116">Description</span><span class="sxs-lookup"><span data-stu-id="1e69b-116">Description</span></span>                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e69b-117">**AddProgram**</span><span class="sxs-lookup"><span data-stu-id="1e69b-117">**AddProgram**</span></span>](addprogram-win32-tsvirtualip.md)                                                       | <span data-ttu-id="1e69b-118">Ajoute un programme à la liste des programmes qui utilisent la virtualisation IP.</span><span class="sxs-lookup"><span data-stu-id="1e69b-118">Adds a program to the list of programs that use IP virtualization.</span></span><br/>                                                                                                |
| [<span data-ttu-id="1e69b-119">**RemoveProgram**</span><span class="sxs-lookup"><span data-stu-id="1e69b-119">**RemoveProgram**</span></span>](removeprogram-win32-tsvirtualip.md)                                                 | <span data-ttu-id="1e69b-120">Supprime un programme de la liste des programmes qui utilisent la virtualisation IP.</span><span class="sxs-lookup"><span data-stu-id="1e69b-120">Removes a program from the list of programs that use IP virtualization.</span></span><br/>                                                                                           |
| [<span data-ttu-id="1e69b-121">**SelectNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="1e69b-121">**SelectNetworkAdapter**</span></span>](selectnetworkadapter-win32-tsvirtualip.md)                                   | <span data-ttu-id="1e69b-122">Définit l’adresse MAC de la carte réseau à utiliser pour la virtualisation IP.</span><span class="sxs-lookup"><span data-stu-id="1e69b-122">Sets the MAC address of the network adapter to use for IP virtualization.</span></span><br/>                                                                                         |
| [<span data-ttu-id="1e69b-123">**SetProgramList**</span><span class="sxs-lookup"><span data-stu-id="1e69b-123">**SetProgramList**</span></span>](setprogramlist-win32-tsvirtualip.md)                                               | <span data-ttu-id="1e69b-124">Remplace la liste des programmes qui utilisent la virtualisation IP.</span><span class="sxs-lookup"><span data-stu-id="1e69b-124">Overwrites the list of programs that use IP virtualization.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="1e69b-125">**SetVirtualIPActive**</span><span class="sxs-lookup"><span data-stu-id="1e69b-125">**SetVirtualIPActive**</span></span>](setvirtualipactive-win32-tsvirtualip.md)                                       | <span data-ttu-id="1e69b-126">Définit la valeur de la propriété **VirtualIPActive** .</span><span class="sxs-lookup"><span data-stu-id="1e69b-126">Sets the **VirtualIPActive** property value.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="1e69b-127">**SetVirtualIPMode**</span><span class="sxs-lookup"><span data-stu-id="1e69b-127">**SetVirtualIPMode**</span></span>](setvirtualipmode-win32-tsvirtualip.md)                                           | <span data-ttu-id="1e69b-128">Définit la valeur de la propriété **VirtualIPMode** .</span><span class="sxs-lookup"><span data-stu-id="1e69b-128">Sets the **VirtualIPMode** property value.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="1e69b-129">**SetVirtualizeLoopbackAddressesEnabled**</span><span class="sxs-lookup"><span data-stu-id="1e69b-129">**SetVirtualizeLoopbackAddressesEnabled**</span></span>](setvirtualizeloopbackaddressesenabled-win32-tsvirtualip.md) | <span data-ttu-id="1e69b-130">Définit la valeur de la propriété **VirtualizeLoopbackAddressesEnabled** .</span><span class="sxs-lookup"><span data-stu-id="1e69b-130">Sets the **VirtualizeLoopbackAddressesEnabled** property value.</span></span><br/> <span data-ttu-id="1e69b-131">**Windows Server 2008 R2 :** Cette méthode n’est pas disponible avant Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="1e69b-131">**Windows Server 2008 R2:** This method is not available prior to Windows Server 2012.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1e69b-132">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1e69b-132">Properties</span></span>

<span data-ttu-id="1e69b-133">La classe **Win32 \_ TSVirtualIP** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="1e69b-133">The **Win32\_TSVirtualIP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1e69b-134">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1e69b-134">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e69b-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1e69b-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e69b-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e69b-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e69b-137">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1e69b-137">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1e69b-138">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1e69b-138">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="1e69b-139">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1e69b-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e69b-140">**Description**</span><span class="sxs-lookup"><span data-stu-id="1e69b-140">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e69b-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1e69b-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e69b-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e69b-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e69b-143">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1e69b-143">Description of the object.</span></span>

<span data-ttu-id="1e69b-144">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1e69b-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e69b-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1e69b-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e69b-146">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1e69b-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1e69b-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e69b-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e69b-148">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="1e69b-148">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="1e69b-149">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="1e69b-149">The date the object was installed.</span></span> <span data-ttu-id="1e69b-150">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="1e69b-150">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="1e69b-151">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1e69b-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e69b-152">**Nom**</span><span class="sxs-lookup"><span data-stu-id="1e69b-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e69b-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1e69b-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e69b-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e69b-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e69b-155">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="1e69b-155">The name of the object.</span></span>

<span data-ttu-id="1e69b-156">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1e69b-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e69b-157">**NetworkAdapterDescription**</span><span class="sxs-lookup"><span data-stu-id="1e69b-157">**NetworkAdapterDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e69b-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1e69b-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e69b-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e69b-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e69b-160">Description de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="1e69b-160">The description for the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1e69b-161">**NetworkAdapterDescriptionList**</span><span class="sxs-lookup"><span data-stu-id="1e69b-161">**NetworkAdapterDescriptionList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e69b-162">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="1e69b-162">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1e69b-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e69b-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e69b-164">Liste des descriptions des cartes réseau physiques disponibles.</span><span class="sxs-lookup"><span data-stu-id="1e69b-164">The list of descriptions of the available physical network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="1e69b-165">**NetworkAdapterMacAddress**</span><span class="sxs-lookup"><span data-stu-id="1e69b-165">**NetworkAdapterMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e69b-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1e69b-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e69b-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e69b-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e69b-168">Adresse MAC de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="1e69b-168">The MAC address of the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1e69b-169">**NetworkAdapterMacList**</span><span class="sxs-lookup"><span data-stu-id="1e69b-169">**NetworkAdapterMacList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e69b-170">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="1e69b-170">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1e69b-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e69b-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e69b-172">Liste des adresses MAC des cartes réseau physiques disponibles.</span><span class="sxs-lookup"><span data-stu-id="1e69b-172">The list of MAC addresses of the available physical network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="1e69b-173">**PolicySourceNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="1e69b-173">**PolicySourceNetworkAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e69b-174">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1e69b-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1e69b-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e69b-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e69b-176">Indique si la carte réseau est configurée par le serveur ou par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="1e69b-176">Indicates whether the network adapter is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="1e69b-177">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="1e69b-177">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="1e69b-178">Serveur</span><span class="sxs-lookup"><span data-stu-id="1e69b-178">Server</span></span>

</dd> <dt>

<span data-ttu-id="1e69b-179">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="1e69b-179">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="1e69b-180">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="1e69b-180">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1e69b-181">**PolicySourceProgramList**</span><span class="sxs-lookup"><span data-stu-id="1e69b-181">**PolicySourceProgramList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e69b-182">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1e69b-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1e69b-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e69b-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e69b-184">Indique si la propriété **ProgramList** est configurée par le serveur ou par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="1e69b-184">Indicates whether the **ProgramList** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="1e69b-185">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="1e69b-185">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="1e69b-186">Serveur</span><span class="sxs-lookup"><span data-stu-id="1e69b-186">Server</span></span>

</dd> <dt>

<span data-ttu-id="1e69b-187">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="1e69b-187">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="1e69b-188">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="1e69b-188">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1e69b-189">**PolicySourceVirtualIPActive**</span><span class="sxs-lookup"><span data-stu-id="1e69b-189">**PolicySourceVirtualIPActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e69b-190">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1e69b-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1e69b-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e69b-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e69b-192">Indique si la propriété **VirtualIPActive** est configurée par le serveur ou par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="1e69b-192">Indicates if the **VirtualIPActive** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="1e69b-193">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="1e69b-193">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="1e69b-194">Serveur</span><span class="sxs-lookup"><span data-stu-id="1e69b-194">Server</span></span>

</dd> <dt>

<span data-ttu-id="1e69b-195">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="1e69b-195">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="1e69b-196">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="1e69b-196">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1e69b-197">**PolicySourceVirtualIPMode**</span><span class="sxs-lookup"><span data-stu-id="1e69b-197">**PolicySourceVirtualIPMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e69b-198">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1e69b-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1e69b-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e69b-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e69b-200">Indique si la propriété **VirtualIPMode** est configurée par le serveur ou par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="1e69b-200">Indicates if the **VirtualIPMode** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="1e69b-201">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="1e69b-201">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="1e69b-202">Serveur</span><span class="sxs-lookup"><span data-stu-id="1e69b-202">Server</span></span>

</dd> <dt>

<span data-ttu-id="1e69b-203">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="1e69b-203">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="1e69b-204">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="1e69b-204">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1e69b-205">**ProgramList**</span><span class="sxs-lookup"><span data-stu-id="1e69b-205">**ProgramList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e69b-206">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="1e69b-206">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1e69b-207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e69b-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e69b-208">Spécifie les programmes qui sont configurés pour utiliser la virtualisation IP.</span><span class="sxs-lookup"><span data-stu-id="1e69b-208">Specifies the programs that are configured to use IP virtualization.</span></span> <span data-ttu-id="1e69b-209">Il peut s’agit d’un nom de programme ou d’un chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="1e69b-209">This may a program name or the full path.</span></span>

</dd> <dt>

<span data-ttu-id="1e69b-210">**État**</span><span class="sxs-lookup"><span data-stu-id="1e69b-210">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e69b-211">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1e69b-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e69b-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e69b-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e69b-213">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="1e69b-213">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="1e69b-214">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1e69b-214">Current status of the object.</span></span> <span data-ttu-id="1e69b-215">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="1e69b-215">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="1e69b-216">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="1e69b-216">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="1e69b-217">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="1e69b-217">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1e69b-218">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="1e69b-218">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1e69b-219">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="1e69b-219">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1e69b-220">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1e69b-220">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="1e69b-221">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="1e69b-221">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1e69b-222">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="1e69b-222">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1e69b-223">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="1e69b-223">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1e69b-224">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="1e69b-224">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1e69b-225">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="1e69b-225">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1e69b-226">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="1e69b-226">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1e69b-227">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="1e69b-227">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1e69b-228">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="1e69b-228">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1e69b-229">**VirtualIPActive**</span><span class="sxs-lookup"><span data-stu-id="1e69b-229">**VirtualIPActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e69b-230">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1e69b-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1e69b-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e69b-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e69b-232">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1e69b-232">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1e69b-233">Spécifie si la virtualisation IP est active sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="1e69b-233">Specifies if IP virtualization is active on the server.</span></span> <span data-ttu-id="1e69b-234">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1e69b-234">This can be one of the following values.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="1e69b-235"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="1e69b-235"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1e69b-236">La virtualisation IP n’est pas active.</span><span class="sxs-lookup"><span data-stu-id="1e69b-236">IP virtualization is not active.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="1e69b-237"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="1e69b-237"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1e69b-238">La virtualisation IP est active.</span><span class="sxs-lookup"><span data-stu-id="1e69b-238">IP virtualization is active.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1e69b-239">**VirtualIPMode**</span><span class="sxs-lookup"><span data-stu-id="1e69b-239">**VirtualIPMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e69b-240">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1e69b-240">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1e69b-241">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e69b-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e69b-242">Spécifie le mode de virtualisation IP utilisé sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="1e69b-242">Specifies which IP virtualization mode is being used on the server.</span></span> <span data-ttu-id="1e69b-243">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1e69b-243">This can be one of the following values.</span></span>

<dt>

<span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>

<span data-ttu-id="1e69b-244"><span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>**Par session** (0)</span><span class="sxs-lookup"><span data-stu-id="1e69b-244"><span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>**Per-Session** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1e69b-245">Le mode de virtualisation IP est par session.</span><span class="sxs-lookup"><span data-stu-id="1e69b-245">The IP virtualization mode is per-session.</span></span>

</dd> <dt>

<span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>

<span data-ttu-id="1e69b-246"><span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>**Par programme** (1)</span><span class="sxs-lookup"><span data-stu-id="1e69b-246"><span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>**Per-Program** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1e69b-247">Le mode de virtualisation IP est par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1e69b-247">The IP virtualization mode is per-user.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1e69b-248">**VirtualizeLoopbackAddressesEnabled**</span><span class="sxs-lookup"><span data-stu-id="1e69b-248">**VirtualizeLoopbackAddressesEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e69b-249">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1e69b-249">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1e69b-250">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e69b-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e69b-251">Spécifie si la virtualisation des adresses de bouclage est activée.</span><span class="sxs-lookup"><span data-stu-id="1e69b-251">Specifies whether loopback address virtualization is enabled.</span></span>

<span data-ttu-id="1e69b-252">**Windows Server 2008 R2 :** Cette propriété n’est pas disponible avant Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="1e69b-252">**Windows Server 2008 R2:** This property is not available prior to Windows Server 2012.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="1e69b-253"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="1e69b-253"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1e69b-254">Non activé</span><span class="sxs-lookup"><span data-stu-id="1e69b-254">Not enabled</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="1e69b-255"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="1e69b-255"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1e69b-256">activé</span><span class="sxs-lookup"><span data-stu-id="1e69b-256">Enabled</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1e69b-257">Notes</span><span class="sxs-lookup"><span data-stu-id="1e69b-257">Remarks</span></span>

<span data-ttu-id="1e69b-258">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="1e69b-258">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1e69b-259">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1e69b-259">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1e69b-260">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="1e69b-260">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1e69b-261">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1e69b-261">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e69b-262">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e69b-262">Requirements</span></span>



| <span data-ttu-id="1e69b-263">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e69b-263">Requirement</span></span> | <span data-ttu-id="1e69b-264">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e69b-264">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e69b-265">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e69b-265">Minimum supported client</span></span><br/> | <span data-ttu-id="1e69b-266">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e69b-266">None supported</span></span><br/>                                                               |
| <span data-ttu-id="1e69b-267">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e69b-267">Minimum supported server</span></span><br/> | <span data-ttu-id="1e69b-268">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1e69b-268">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="1e69b-269">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1e69b-269">Namespace</span></span><br/>                | <span data-ttu-id="1e69b-270">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="1e69b-270">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1e69b-271">MOF</span><span class="sxs-lookup"><span data-stu-id="1e69b-271">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e69b-272"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e69b-272"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e69b-273">DLL</span><span class="sxs-lookup"><span data-stu-id="1e69b-273">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e69b-274"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e69b-274"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



 

