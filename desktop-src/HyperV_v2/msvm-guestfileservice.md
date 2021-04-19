---
description: MSVM \_ GuestFileService contient une méthode qui peut être utilisée pour copier un fichier sur un ordinateur virtuel à partir de l’hôte Hyper-V.
ms.assetid: 3599d5a8-415f-48f8-b887-00a93b7abb83
title: Classe Msvm_GuestFileService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestFileService
- Msvm_GuestFileService.StartService
- Msvm_GuestFileService.StopService
- Msvm_GuestFileService.Caption
- Msvm_GuestFileService.CreationClassName
- Msvm_GuestFileService.Description
- Msvm_GuestFileService.InstallDate
- Msvm_GuestFileService.Name
- Msvm_GuestFileService.Started
- Msvm_GuestFileService.StartMode
- Msvm_GuestFileService.Status
- Msvm_GuestFileService.SystemCreationClassName
- Msvm_GuestFileService.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ee0f235d7549428ecf02e9c758c83bcea33efe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514581"
---
# <a name="msvm_guestfileservice-class"></a><span data-ttu-id="9eda7-103">MSVM \_ GuestFileService, classe</span><span class="sxs-lookup"><span data-stu-id="9eda7-103">Msvm\_GuestFileService class</span></span>

<span data-ttu-id="9eda7-104">**MSVM \_ GuestFileService** contient une méthode qui peut être utilisée pour copier un fichier sur un ordinateur virtuel à partir de l’hôte Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="9eda7-104">**Msvm\_GuestFileService** contains a method that can be used to copy a file to a virtual machine from the Hyper-V host.</span></span> <span data-ttu-id="9eda7-105">Cette classe dérive de [**MSVM \_ GuestService**](msvm-guestservice.md).</span><span class="sxs-lookup"><span data-stu-id="9eda7-105">This class derives from [**Msvm\_GuestService**](msvm-guestservice.md).</span></span>

<span data-ttu-id="9eda7-106">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9eda7-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eda7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9eda7-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestFileService : Msvm_GuestService
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="9eda7-108">Membres</span><span class="sxs-lookup"><span data-stu-id="9eda7-108">Members</span></span>

<span data-ttu-id="9eda7-109">La classe **MSVM \_ GuestFileService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9eda7-109">The **Msvm\_GuestFileService** class has these types of members:</span></span>

-   [<span data-ttu-id="9eda7-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9eda7-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="9eda7-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9eda7-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9eda7-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9eda7-112">Methods</span></span>

<span data-ttu-id="9eda7-113">La classe **MSVM \_ GuestFileService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="9eda7-113">The **Msvm\_GuestFileService** class has these methods.</span></span>



| <span data-ttu-id="9eda7-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="9eda7-114">Method</span></span>                                                             | <span data-ttu-id="9eda7-115">Description</span><span class="sxs-lookup"><span data-stu-id="9eda7-115">Description</span></span>                                                                                                                                                                  |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9eda7-116">**CopyFilesToGuest**</span><span class="sxs-lookup"><span data-stu-id="9eda7-116">**CopyFilesToGuest**</span></span>](copyfilestoguest-msvm-guestfileservice.md) | <span data-ttu-id="9eda7-117">Copie les fichiers de l’hôte Hyper-V vers l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="9eda7-117">Copies files from the Hyper-V host to the virtual machine.</span></span><br/> <span data-ttu-id="9eda7-118">**Windows 8.1 :** Cette méthode n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="9eda7-118">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| <span data-ttu-id="9eda7-119">**StartService**</span><span class="sxs-lookup"><span data-stu-id="9eda7-119">**StartService**</span></span>                                                   | <span data-ttu-id="9eda7-120">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9eda7-120">This method is not supported.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="9eda7-121">**StopService**</span><span class="sxs-lookup"><span data-stu-id="9eda7-121">**StopService**</span></span>                                                    | <span data-ttu-id="9eda7-122">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9eda7-122">This method is not supported.</span></span><br/>                                                                                                                                     |



 

### <a name="properties"></a><span data-ttu-id="9eda7-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9eda7-123">Properties</span></span>

<span data-ttu-id="9eda7-124">La classe **MSVM \_ GuestFileService** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9eda7-124">The **Msvm\_GuestFileService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9eda7-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9eda7-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eda7-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9eda7-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9eda7-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9eda7-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9eda7-128">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9eda7-128">Short textual description of the object.</span></span> <span data-ttu-id="9eda7-129">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9eda7-129">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9eda7-130">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9eda7-130">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eda7-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9eda7-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9eda7-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9eda7-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9eda7-133">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="9eda7-133">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9eda7-134">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="9eda7-134">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="9eda7-135">**Description**</span><span class="sxs-lookup"><span data-stu-id="9eda7-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eda7-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9eda7-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9eda7-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9eda7-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9eda7-138">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9eda7-138">Textual description of the object.</span></span> <span data-ttu-id="9eda7-139">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9eda7-139">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9eda7-140">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9eda7-140">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eda7-141">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9eda7-141">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9eda7-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9eda7-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9eda7-143">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9eda7-143">Date and time the object was installed.</span></span> <span data-ttu-id="9eda7-144">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="9eda7-144">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="9eda7-145">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9eda7-145">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9eda7-146">**Nom**</span><span class="sxs-lookup"><span data-stu-id="9eda7-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eda7-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9eda7-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9eda7-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9eda7-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9eda7-149">Identificateur unique du service qui fournit également une indication de la fonctionnalité gérée.</span><span class="sxs-lookup"><span data-stu-id="9eda7-149">Unique identifier for the service that also provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="9eda7-150">Pour plus d’informations sur les fonctionnalités, consultez la propriété **Description** de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9eda7-150">For more information about the functionality, see the object's **Description** property.</span></span> <span data-ttu-id="9eda7-151">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9eda7-151">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9eda7-152">**Cours**</span><span class="sxs-lookup"><span data-stu-id="9eda7-152">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eda7-153">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9eda7-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9eda7-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9eda7-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9eda7-155">Si la **valeur est true**, le service a démarré.</span><span class="sxs-lookup"><span data-stu-id="9eda7-155">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="9eda7-156">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="9eda7-156">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eda7-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9eda7-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9eda7-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9eda7-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9eda7-159">Indique si le service est démarré automatiquement (par exemple, par un système d’exploitation) ou s’il est démarré uniquement à la demande.</span><span class="sxs-lookup"><span data-stu-id="9eda7-159">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="9eda7-160">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9eda7-160">Values include the following:</span></span>

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

<span data-ttu-id="9eda7-161">**Automatique**</span><span class="sxs-lookup"><span data-stu-id="9eda7-161">**"Automatic"**</span></span>
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

<span data-ttu-id="9eda7-162">**Opération**</span><span class="sxs-lookup"><span data-stu-id="9eda7-162">**"Manual"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9eda7-163">**État**</span><span class="sxs-lookup"><span data-stu-id="9eda7-163">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eda7-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9eda7-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9eda7-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9eda7-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9eda7-166">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9eda7-166">Current status of the object.</span></span> <span data-ttu-id="9eda7-167">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9eda7-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="9eda7-168">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9eda7-168">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="9eda7-169">**OK**</span><span class="sxs-lookup"><span data-stu-id="9eda7-169">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="9eda7-170">**Erreurs**</span><span class="sxs-lookup"><span data-stu-id="9eda7-170">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="9eda7-171">**Détérioré**</span><span class="sxs-lookup"><span data-stu-id="9eda7-171">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="9eda7-172">**Connue**</span><span class="sxs-lookup"><span data-stu-id="9eda7-172">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="9eda7-173">**« Échec prévu »**</span><span class="sxs-lookup"><span data-stu-id="9eda7-173">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="9eda7-174">**Démarr**</span><span class="sxs-lookup"><span data-stu-id="9eda7-174">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="9eda7-175">**Arrêt**</span><span class="sxs-lookup"><span data-stu-id="9eda7-175">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="9eda7-176">**Services**</span><span class="sxs-lookup"><span data-stu-id="9eda7-176">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="9eda7-177">**Trop sollicité**</span><span class="sxs-lookup"><span data-stu-id="9eda7-177">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="9eda7-178">**« Non récupéré »**</span><span class="sxs-lookup"><span data-stu-id="9eda7-178">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="9eda7-179">**« Aucun contact »**</span><span class="sxs-lookup"><span data-stu-id="9eda7-179">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="9eda7-180">**« Comm. perdue »**</span><span class="sxs-lookup"><span data-stu-id="9eda7-180">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9eda7-181">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9eda7-181">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eda7-182">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9eda7-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9eda7-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9eda7-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9eda7-184">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="9eda7-184">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="9eda7-185">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9eda7-185">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eda7-186">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9eda7-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9eda7-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9eda7-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9eda7-188">Nom du système qui héberge le service.</span><span class="sxs-lookup"><span data-stu-id="9eda7-188">Name of the system that hosts the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9eda7-189">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9eda7-189">Requirements</span></span>



| <span data-ttu-id="9eda7-190">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9eda7-190">Requirement</span></span> | <span data-ttu-id="9eda7-191">Valeur</span><span class="sxs-lookup"><span data-stu-id="9eda7-191">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9eda7-192">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9eda7-192">Minimum supported client</span></span><br/> | <span data-ttu-id="9eda7-193">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9eda7-193">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="9eda7-194">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9eda7-194">Minimum supported server</span></span><br/> | <span data-ttu-id="9eda7-195">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9eda7-195">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9eda7-196">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9eda7-196">Namespace</span></span><br/>                | <span data-ttu-id="9eda7-197">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9eda7-197">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9eda7-198">MOF</span><span class="sxs-lookup"><span data-stu-id="9eda7-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9eda7-199"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9eda7-199"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9eda7-200">DLL</span><span class="sxs-lookup"><span data-stu-id="9eda7-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9eda7-201"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9eda7-201"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9eda7-202">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9eda7-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eda7-203">**MSVM \_ GuestService**</span><span class="sxs-lookup"><span data-stu-id="9eda7-203">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

