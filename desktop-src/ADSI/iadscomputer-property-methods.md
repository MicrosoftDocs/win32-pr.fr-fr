---
title: Méthodes de propriété IADsComputer (IADs. h)
description: Les méthodes de l’interface IADsComputer lisent et écrivent les propriétés décrites dans cette rubrique. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: c990b6bb-6256-4216-9435-c85c67db4d13
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsComputer ADSI
topic_type:
- apiref
api_name:
- IADsComputer Property Methods
- IADsComputer.ComputerID
- IADsComputer.get_ComputerID
- IADsComputer.Department
- IADsComputer.get_Department
- IADsComputer.put_Department
- IADsComputer.Description
- IADsComputer.get_Description
- IADsComputer.put_Description
- IADsComputer.Division
- IADsComputer.get_Division
- IADsComputer.put_Division
- IADsComputer.Location
- IADsComputer.get_Location
- IADsComputer.put_Location
- IADsComputer.MemorySize
- IADsComputer.get_MemorySize
- IADsComputer.put_MemorySize
- IADsComputer.Model
- IADsComputer.get_Model
- IADsComputer.put_Model
- IADsComputer.NetAddresses
- IADsComputer.get_NetAddresses
- IADsComputer.put_NetAddresses
- IADsComputer.OperatingSystem
- IADsComputer.get_OperatingSystem
- IADsComputer.put_OperatingSystem
- IADsComputer.OperatingSystemVersion
- IADsComputer.get_OperatingSystemVersion
- IADsComputer.put_OperatingSystemVersion
- IADsComputer.Owner
- IADsComputer.get_Owner
- IADsComputer.put_Owner
- IADsComputer.PrimaryUser
- IADsComputer.get_PrimaryUser
- IADsComputer.put_PrimaryUser
- IADsComputer.Processor
- IADsComputer.get_Processor
- IADsComputer.put_Processor
- IADsComputer.ProcessorCount
- IADsComputer.get_ProcessorCount
- IADsComputer.put_ProcessorCount
- IADsComputer.Role
- IADsComputer.get_Role
- IADsComputer.put_Role
- IADsComputer.Site
- IADsComputer.get_Site
- IADsComputer.StorageCapacity
- IADsComputer.get_StorageCapacity
- IADsComputer.put_StorageCapacity
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f2f3c455e2e43436627b62d142781bb6a605bef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844017"
---
# <a name="iadscomputer-property-methods"></a><span data-ttu-id="ecf52-105">Méthodes de propriété IADsComputer</span><span class="sxs-lookup"><span data-stu-id="ecf52-105">IADsComputer Property Methods</span></span>

<span data-ttu-id="ecf52-106">Les méthodes de l’interface [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) lisent et écrivent les propriétés décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="ecf52-106">The [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) interface methods read and write the properties described in this topic.</span></span> <span data-ttu-id="ecf52-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="ecf52-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="ecf52-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ecf52-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="ecf52-109">**ComputerID**</span><span class="sxs-lookup"><span data-stu-id="ecf52-109">**ComputerID**</span></span>
<span data-ttu-id="ecf52-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ecf52-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="ecf52-111">Identificateur global unique affecté à chaque ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ecf52-111">The globally unique identifier assigned to each computer.</span></span>

<dt>

<span data-ttu-id="ecf52-112">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ecf52-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ecf52-113">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ecf52-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerID(
  [out] BSTR* pbstrComputerID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecf52-114">**Département**</span><span class="sxs-lookup"><span data-stu-id="ecf52-114">**Department**</span></span>
<span data-ttu-id="ecf52-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ecf52-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="ecf52-116">L’unité d’organisation (OU), telle que Department, à laquelle cet ordinateur appartient.</span><span class="sxs-lookup"><span data-stu-id="ecf52-116">The organizational unit (OU), such as department, that this computer belongs to.</span></span>

<dt>

<span data-ttu-id="ecf52-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ecf52-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ecf52-118">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ecf52-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Department(
  [out] BSTR* pbstrDepartment
);
HRESULT put_Department(
  [in] BSTR bstrDepartment
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecf52-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="ecf52-119">**Description**</span></span>
<span data-ttu-id="ecf52-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ecf52-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="ecf52-121">Description de cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ecf52-121">The description of this computer.</span></span>

<dt>

<span data-ttu-id="ecf52-122">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ecf52-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ecf52-123">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ecf52-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecf52-124">**Division**</span><span class="sxs-lookup"><span data-stu-id="ecf52-124">**Division**</span></span>
<span data-ttu-id="ecf52-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ecf52-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="ecf52-126">Division, au sein d’une organisation, à laquelle cet ordinateur appartient.</span><span class="sxs-lookup"><span data-stu-id="ecf52-126">The division, within an organization, that this computer belongs to.</span></span>

<dt>

<span data-ttu-id="ecf52-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ecf52-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ecf52-128">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ecf52-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Division(
  [out] BSTR* pbstrDivision
);
HRESULT put_Division(
  [in] BSTR bstrDivision
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecf52-129">**Lieu**</span><span class="sxs-lookup"><span data-stu-id="ecf52-129">**Location**</span></span>
<span data-ttu-id="ecf52-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ecf52-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="ecf52-131">Emplacement physique affecté de cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ecf52-131">The assigned physical location of this computer.</span></span>

<dt>

<span data-ttu-id="ecf52-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ecf52-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ecf52-133">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ecf52-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Location(
  [out] BSTR* pbstrLocation
);
HRESULT put_Location(
  [in] BSTR bstrLocation
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecf52-134">**MemorySize**</span><span class="sxs-lookup"><span data-stu-id="ecf52-134">**MemorySize**</span></span>
<span data-ttu-id="ecf52-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ecf52-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="ecf52-136">Taille, en mégaoctets, de la mémoire vive (Random Access) de cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ecf52-136">The size, in megabytes, of random access memory for this computer.</span></span>

<dt>

<span data-ttu-id="ecf52-137">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ecf52-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ecf52-138">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ecf52-138">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MemorySize(
  [out] BSTR* pbstrMemorySize
);
HRESULT put_MemorySize(
  [in] BSTR bstrMemorySize
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecf52-139">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="ecf52-139">**Model**</span></span>
<span data-ttu-id="ecf52-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ecf52-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="ecf52-141">Marque et modèle de cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ecf52-141">The make and model of this computer.</span></span>

<dt>

<span data-ttu-id="ecf52-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ecf52-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ecf52-143">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ecf52-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Model(
  [out] BSTR* pbstrModel
);
HRESULT put_Model(
  [in] BSTR bstrModel
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecf52-144">**Adresses**</span><span class="sxs-lookup"><span data-stu-id="ecf52-144">**NetAddresses**</span></span>
<span data-ttu-id="ecf52-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ecf52-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="ecf52-146">Tableau de champs d’adresse réseau qui représentent les adresses par lesquelles cet ordinateur peut être atteint.</span><span class="sxs-lookup"><span data-stu-id="ecf52-146">An array of NetAddress fields that represent the addresses by which this computer can be reached.</span></span> <span data-ttu-id="ecf52-147">NetAddress est un **BSTR** spécifique au fournisseur composé de deux sous-chaînes séparées par un signe deux-points ( :).</span><span class="sxs-lookup"><span data-stu-id="ecf52-147">NetAddress is a provider-specific **BSTR** composed of two substrings separated by a colon (:).</span></span> <span data-ttu-id="ecf52-148">La sous-chaîne de gauche indique le type d’adresse, et la sous-chaîne de droite est une représentation sous forme de chaîne d’une adresse de ce type.</span><span class="sxs-lookup"><span data-stu-id="ecf52-148">The left substring indicates the address type, and the right substring is a string representation of an address of that type.</span></span> <span data-ttu-id="ecf52-149">Par exemple, les adresses TCP/IP se présentent sous la forme : IP : 100.201.301.45.</span><span class="sxs-lookup"><span data-stu-id="ecf52-149">For example, TCP/IP addresses are of the form: IP:100.201.301.45.</span></span> <span data-ttu-id="ecf52-150">Les adresses de type IPX se présentent sous la forme : IPX : 10.123456.80.</span><span class="sxs-lookup"><span data-stu-id="ecf52-150">IPX type addresses are of the form: IPX:10.123456.80.</span></span>

<dt>

<span data-ttu-id="ecf52-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ecf52-151">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ecf52-152">Type de données de script : **variante**</span><span class="sxs-lookup"><span data-stu-id="ecf52-152">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NetAddresses(
  [out] VARIANT* pvNetAddresses
);
HRESULT put_NetAddresses(
  [in] VARIANT vNetAddresses
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecf52-153">**OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="ecf52-153">**OperatingSystem**</span></span>
<span data-ttu-id="ecf52-154"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ecf52-154"></dt> <dd> <dl></span></span>

<span data-ttu-id="ecf52-155">Le système d’exploitation utilisé sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ecf52-155">The operating system used on this computer.</span></span>

<dt>

<span data-ttu-id="ecf52-156">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ecf52-156">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ecf52-157">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ecf52-157">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OperatingSystem(
  [out] BSTR* pbstrOperatingSystem
);
HRESULT put_OperatingSystem(
  [in] BSTR bstrOperatingSystem
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecf52-158">**OperatingSystemVersion renvoyée**</span><span class="sxs-lookup"><span data-stu-id="ecf52-158">**OperatingSystemVersion**</span></span>
<span data-ttu-id="ecf52-159"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ecf52-159"></dt> <dd> <dl></span></span>

<span data-ttu-id="ecf52-160">Version du système d’exploitation utilisé sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ecf52-160">The version of the operating system used on this computer.</span></span>

<dt>

<span data-ttu-id="ecf52-161">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ecf52-161">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ecf52-162">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ecf52-162">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OperatingSystemVersion(
  [out] BSTR* pbstrOperatingSystemVersion
);
HRESULT put_OperatingSystemVersion(
  [in] BSTR bstrOperatingSystemVersion
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecf52-163">**Propriétaire**</span><span class="sxs-lookup"><span data-stu-id="ecf52-163">**Owner**</span></span>
<span data-ttu-id="ecf52-164"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ecf52-164"></dt> <dd> <dl></span></span>

<span data-ttu-id="ecf52-165">Personne à qui cet ordinateur est affecté.</span><span class="sxs-lookup"><span data-stu-id="ecf52-165">The person to whom this computer is assigned.</span></span> <span data-ttu-id="ecf52-166">Cette personne doit également disposer d’une licence pour exécuter le logiciel installé.</span><span class="sxs-lookup"><span data-stu-id="ecf52-166">This person should also have a license to run the installed software.</span></span>

<dt>

<span data-ttu-id="ecf52-167">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ecf52-167">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ecf52-168">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ecf52-168">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Owner(
  [out] BSTR* pbstrOwner
);
HRESULT put_Owner(
  [in] BSTR bstrOwner
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecf52-169">**PrimaryUser**</span><span class="sxs-lookup"><span data-stu-id="ecf52-169">**PrimaryUser**</span></span>
<span data-ttu-id="ecf52-170"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ecf52-170"></dt> <dd> <dl></span></span>

<span data-ttu-id="ecf52-171">Nom de la personne à contacter, par exemple un administrateur, pour cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ecf52-171">The name of the contact person, such as an administrator, for this computer.</span></span>

<dt>

<span data-ttu-id="ecf52-172">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ecf52-172">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ecf52-173">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ecf52-173">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrimaryUser(
  [out] BSTR* pbstrPrimaryUser
);
HRESULT put_PrimaryUser(
  [in] BSTR bstrPrimaryUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecf52-174">**Processeur**</span><span class="sxs-lookup"><span data-stu-id="ecf52-174">**Processor**</span></span>
<span data-ttu-id="ecf52-175"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ecf52-175"></dt> <dd> <dl></span></span>

<span data-ttu-id="ecf52-176">Type de processeur.</span><span class="sxs-lookup"><span data-stu-id="ecf52-176">The processor type.</span></span>

<dt>

<span data-ttu-id="ecf52-177">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ecf52-177">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ecf52-178">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ecf52-178">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Processor(
  [out] BSTR* pbstrProcessor
);
HRESULT put_Processor(
  [in] BSTR bstrProcessor
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecf52-179">**ProcessorCount**</span><span class="sxs-lookup"><span data-stu-id="ecf52-179">**ProcessorCount**</span></span>
<span data-ttu-id="ecf52-180"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ecf52-180"></dt> <dd> <dl></span></span>

<span data-ttu-id="ecf52-181">Nombre de processeurs installés.</span><span class="sxs-lookup"><span data-stu-id="ecf52-181">The number of installed processors.</span></span>

<dt>

<span data-ttu-id="ecf52-182">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ecf52-182">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ecf52-183">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ecf52-183">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ProcessorCount(
  [out] BSTR* pbstrProcessorCount
);
HRESULT put_ProcessorCount(
  [in] BSTR bstrProcessorCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecf52-184">**Rôle**</span><span class="sxs-lookup"><span data-stu-id="ecf52-184">**Role**</span></span>
<span data-ttu-id="ecf52-185"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ecf52-185"></dt> <dd> <dl></span></span>

<span data-ttu-id="ecf52-186">Rôle de cet ordinateur, par exemple, station de travail, serveur ou contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="ecf52-186">The role of this computer, for example, workstation, server, or domain controller.</span></span>

<dt>

<span data-ttu-id="ecf52-187">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ecf52-187">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ecf52-188">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ecf52-188">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Role(
  [out] BSTR* pbstrRole
);
HRESULT put_Role(
  [in] BSTR bstrRole
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecf52-189">**Site**</span><span class="sxs-lookup"><span data-stu-id="ecf52-189">**Site**</span></span>
<span data-ttu-id="ecf52-190"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ecf52-190"></dt> <dd> <dl></span></span>

<span data-ttu-id="ecf52-191">Identificateur global unique qui identifie le site dans lequel cet ordinateur a été installé.</span><span class="sxs-lookup"><span data-stu-id="ecf52-191">The globally unique identifier that identifies the site that this computer was installed in.</span></span> <span data-ttu-id="ecf52-192">Un site est une région physique de bonne connectivité dans un réseau.</span><span class="sxs-lookup"><span data-stu-id="ecf52-192">A site is a physical region of good connectivity in a network.</span></span>

<dt>

<span data-ttu-id="ecf52-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ecf52-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ecf52-194">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ecf52-194">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Site(
  [out] BSTR* pbstrSite
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecf52-195">**StorageCapacity**</span><span class="sxs-lookup"><span data-stu-id="ecf52-195">**StorageCapacity**</span></span>
<span data-ttu-id="ecf52-196"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ecf52-196"></dt> <dd> <dl></span></span>

<span data-ttu-id="ecf52-197">Taille, en mégaoctets, du disque.</span><span class="sxs-lookup"><span data-stu-id="ecf52-197">The size, in megabytes, of the disk.</span></span>

<dt>

<span data-ttu-id="ecf52-198">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ecf52-198">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ecf52-199">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ecf52-199">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StorageCapacity(
  [out] BSTR* pbstrStorageCapacity
);
HRESULT put_StorageCapacity(
  [in] BSTR bstrStorageCapacity
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="ecf52-200">Notes</span><span class="sxs-lookup"><span data-stu-id="ecf52-200">Remarks</span></span>

<span data-ttu-id="ecf52-201">Différents fournisseurs peuvent choisir d’exposer différentes propriétés d’un objet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ecf52-201">Different providers may choose to expose different properties of a computer object.</span></span> <span data-ttu-id="ecf52-202">Pour plus d’informations, consultez [fournisseurs système ADSI](adsi-system-providers.md).</span><span class="sxs-lookup"><span data-stu-id="ecf52-202">For more information, see [ADSI System Providers](adsi-system-providers.md).</span></span>

<span data-ttu-id="ecf52-203">Vous pouvez découvrir les propriétés prises en charge en inspectant les propriétés obligatoires et facultatives par le biais de sa classe de schéma.</span><span class="sxs-lookup"><span data-stu-id="ecf52-203">You can discover what properties are supported by inspecting the mandatory and optional properties through its schema class.</span></span> <span data-ttu-id="ecf52-204">Pour plus d’informations, consultez l’interface [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) .</span><span class="sxs-lookup"><span data-stu-id="ecf52-204">For more information, see the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface.</span></span>

<span data-ttu-id="ecf52-205">Pour examiner l’état d’un ordinateur ou pour effectuer l’opération d’arrêt sur le réseau, vous devez utiliser l’interface [**IADsComputerOperations**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations) .</span><span class="sxs-lookup"><span data-stu-id="ecf52-205">To examine the status of a computer or to perform the shutdown operation across the network, you must use the [**IADsComputerOperations**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="ecf52-206">Exemples</span><span class="sxs-lookup"><span data-stu-id="ecf52-206">Examples</span></span>

<span data-ttu-id="ecf52-207">L’exemple de code Visual Basic suivant examine les propriétés de l’ordinateur prises en charge par le fournisseur Winnt ADSI.</span><span class="sxs-lookup"><span data-stu-id="ecf52-207">The following Visual Basic code example examines computer properties supported by the ADSI WinNT provider.</span></span>


```VB
Dim obj As IADs
On Error Resume Next

Set obj = GetObject("WinNT://myMachine,computer")
If (obj.Class = "Computer") Then
    MsgBox "Computer owner: " & obj.owner
    MsgBox "Computer division: " & obj.Division
    MsgBox "Computer operatingSystem: " & obj.OperatingSystem
    MsgBox "Computer operating System Version: " & obj.OperatingSystemVersion
    MsgBox "Computer processor: " & obj.Processor
    MsgBox "Computer processor Count: " & obj.ProcessorCount
End If
```



<span data-ttu-id="ecf52-208">L’exemple de code C++ suivant examine les propriétés de l’ordinateur prises en charge par le fournisseur Winnt ADSI.</span><span class="sxs-lookup"><span data-stu-id="ecf52-208">The following C++ code example examines computer properties supported by the ADSI WinNT provider.</span></span>


```C++
IADsComputer *pComp = NULL;
LPWSTR adspath = L"WinNT://jeffsmith1,computer";
HRESULT hr = S_OK;
BSTR bstr = NULL;

hr = ADsGetObject(adspath,IID_IADsComputer,(void**)&pComp);
if(FAILED(hr)) {goto Cleanup;}

hr = pComp->get_Owner(&bstr);
if(FAILED(hr)) {goto Cleanup;}

printf("Computer owner: %S\n",bstr);
SysFreeString(bstr);

hr = pComp->get_OperatingSystem(&bstr);
if(FAILED(hr)) {goto Cleanup;}
printf("Operating System: %S\n",bstr);
SysFreeString(bstr);

Cleanup:
    if(pComp) pComp->Release();
    if(bstr) SysFreeString(bstr);
    return hr;
```



## <a name="requirements"></a><span data-ttu-id="ecf52-209">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ecf52-209">Requirements</span></span>



| <span data-ttu-id="ecf52-210">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ecf52-210">Requirement</span></span> | <span data-ttu-id="ecf52-211">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecf52-211">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecf52-212">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecf52-212">Minimum supported client</span></span><br/> | <span data-ttu-id="ecf52-213">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ecf52-213">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ecf52-214">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecf52-214">Minimum supported server</span></span><br/> | <span data-ttu-id="ecf52-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ecf52-215">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ecf52-216">En-tête</span><span class="sxs-lookup"><span data-stu-id="ecf52-216">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecf52-217"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecf52-217"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="ecf52-218">DLL</span><span class="sxs-lookup"><span data-stu-id="ecf52-218">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecf52-219"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecf52-219"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="ecf52-220">IID</span><span class="sxs-lookup"><span data-stu-id="ecf52-220">IID</span></span><br/>                      | <span data-ttu-id="ecf52-221">IID \_ IADsComputer est défini en tant que EFE3CC70-1D9F-11CF-B1F3-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="ecf52-221">IID\_IADsComputer is defined as EFE3CC70-1D9F-11CF-B1F3-02608C9E7553</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="ecf52-222">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecf52-222">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecf52-223">**IADsComputer**</span><span class="sxs-lookup"><span data-stu-id="ecf52-223">**IADsComputer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscomputer)
</dt> <dt>

[<span data-ttu-id="ecf52-224">Fournisseurs système ADSI</span><span class="sxs-lookup"><span data-stu-id="ecf52-224">ADSI System Providers</span></span>](adsi-system-providers.md)
</dt> <dt>

[<span data-ttu-id="ecf52-225">**IADsClass**</span><span class="sxs-lookup"><span data-stu-id="ecf52-225">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="ecf52-226">**IADsComputerOperations**</span><span class="sxs-lookup"><span data-stu-id="ecf52-226">**IADsComputerOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations)
</dt> <dt>

[<span data-ttu-id="ecf52-227">Méthodes de propriété d’interface</span><span class="sxs-lookup"><span data-stu-id="ecf52-227">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





