---
description: MSVM \_ GuestService est la classe de base abstraite pour les services de l’invité qui sont accessibles à partir de l’hôte.
ms.assetid: F9E6FFE6-B8C5-4F06-BF22-A4BDB20F813A
title: Classe Msvm_GuestService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService
- Msvm_GuestService.Caption
- Msvm_GuestService.CreationClassName
- Msvm_GuestService.Description
- Msvm_GuestService.InstallDate
- Msvm_GuestService.Name
- Msvm_GuestService.Started
- Msvm_GuestService.StartMode
- Msvm_GuestService.Status
- Msvm_GuestService.SystemCreationClassName
- Msvm_GuestService.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 99d1936a2678fc2d8357974f9c11a250a1d9bce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393431"
---
# <a name="msvm_guestservice-class"></a><span data-ttu-id="aaabc-103">MSVM \_ GuestService, classe</span><span class="sxs-lookup"><span data-stu-id="aaabc-103">Msvm\_GuestService class</span></span>

<span data-ttu-id="aaabc-104">**MSVM \_ GuestService** est la classe de base abstraite pour les services de l’invité qui sont accessibles à partir de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="aaabc-104">**Msvm\_GuestService** is the abstract base class for services in the guest that can be accessed from the host.</span></span> <span data-ttu-id="aaabc-105">Cette classe dérive de la classe de [**\_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service) .</span><span class="sxs-lookup"><span data-stu-id="aaabc-105">This class derives from the [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service) class.</span></span>

<span data-ttu-id="aaabc-106">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="aaabc-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaabc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aaabc-107">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Msvm_GuestService : CIM_Service
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

## <a name="members"></a><span data-ttu-id="aaabc-108">Membres</span><span class="sxs-lookup"><span data-stu-id="aaabc-108">Members</span></span>

<span data-ttu-id="aaabc-109">La classe **MSVM \_ GuestService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="aaabc-109">The **Msvm\_GuestService** class has these types of members:</span></span>

-   [<span data-ttu-id="aaabc-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="aaabc-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="aaabc-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="aaabc-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="aaabc-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="aaabc-112">Methods</span></span>

<span data-ttu-id="aaabc-113">La classe **MSVM \_ GuestService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="aaabc-113">The **Msvm\_GuestService** class has these methods.</span></span>



| <span data-ttu-id="aaabc-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="aaabc-114">Method</span></span>                                                             | <span data-ttu-id="aaabc-115">Description</span><span class="sxs-lookup"><span data-stu-id="aaabc-115">Description</span></span>                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aaabc-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="aaabc-116">**RequestStateChange**</span></span>](requeststatechange-msvm-guestservice.md) | <span data-ttu-id="aaabc-117">Demande que l’état du service invité soit remplacé par la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="aaabc-117">Requests that the state of the guest service be changed to the specified value.</span></span><br/> |
| [<span data-ttu-id="aaabc-118">**StartService**</span><span class="sxs-lookup"><span data-stu-id="aaabc-118">**StartService**</span></span>](startservice-msvm-guestservice.md)             | <span data-ttu-id="aaabc-119">Met le service invité dans un état Démarré.</span><span class="sxs-lookup"><span data-stu-id="aaabc-119">Puts the guest service in a started state.</span></span> <br/>                                     |
| [<span data-ttu-id="aaabc-120">**StopService**</span><span class="sxs-lookup"><span data-stu-id="aaabc-120">**StopService**</span></span>](stopservice-msvm-guestservice.md)               | <span data-ttu-id="aaabc-121">Arrête le service invité.</span><span class="sxs-lookup"><span data-stu-id="aaabc-121">Stops the guest service.</span></span> <br/>                                                       |



 

### <a name="properties"></a><span data-ttu-id="aaabc-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="aaabc-122">Properties</span></span>

<span data-ttu-id="aaabc-123">La classe **MSVM \_ GuestService** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="aaabc-123">The **Msvm\_GuestService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aaabc-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="aaabc-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaabc-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aaabc-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aaabc-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aaabc-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaabc-127">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="aaabc-127">Short textual description of the object.</span></span> <span data-ttu-id="aaabc-128">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="aaabc-128">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="aaabc-129">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="aaabc-129">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaabc-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aaabc-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aaabc-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aaabc-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaabc-132">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="aaabc-132">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="aaabc-133">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="aaabc-133">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="aaabc-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="aaabc-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaabc-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aaabc-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aaabc-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aaabc-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaabc-137">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="aaabc-137">Textual description of the object.</span></span> <span data-ttu-id="aaabc-138">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="aaabc-138">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="aaabc-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="aaabc-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaabc-140">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="aaabc-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aaabc-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aaabc-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaabc-142">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="aaabc-142">Date and time the object was installed.</span></span> <span data-ttu-id="aaabc-143">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="aaabc-143">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="aaabc-144">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="aaabc-144">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="aaabc-145">**Nom**</span><span class="sxs-lookup"><span data-stu-id="aaabc-145">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaabc-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aaabc-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aaabc-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aaabc-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaabc-148">Identificateur unique du service qui fournit également une indication de la fonctionnalité gérée.</span><span class="sxs-lookup"><span data-stu-id="aaabc-148">Unique identifier for the service that also provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="aaabc-149">Pour plus d’informations sur les fonctionnalités, consultez la propriété **Description** de l’objet.</span><span class="sxs-lookup"><span data-stu-id="aaabc-149">For more information about the functionality, see the object's **Description** property.</span></span> <span data-ttu-id="aaabc-150">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="aaabc-150">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="aaabc-151">**Cours**</span><span class="sxs-lookup"><span data-stu-id="aaabc-151">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaabc-152">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="aaabc-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aaabc-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aaabc-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaabc-154">Si la **valeur est true**, le service a démarré.</span><span class="sxs-lookup"><span data-stu-id="aaabc-154">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="aaabc-155">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="aaabc-155">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaabc-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aaabc-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aaabc-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aaabc-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaabc-158">Indique si le service est démarré automatiquement (par exemple, par un système d’exploitation) ou s’il est démarré uniquement à la demande.</span><span class="sxs-lookup"><span data-stu-id="aaabc-158">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="aaabc-159">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="aaabc-159">Values include the following:</span></span>

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

<span data-ttu-id="aaabc-160">**Automatique**</span><span class="sxs-lookup"><span data-stu-id="aaabc-160">**"Automatic"**</span></span>
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

<span data-ttu-id="aaabc-161">**Opération**</span><span class="sxs-lookup"><span data-stu-id="aaabc-161">**"Manual"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="aaabc-162">**État**</span><span class="sxs-lookup"><span data-stu-id="aaabc-162">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaabc-163">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aaabc-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aaabc-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aaabc-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaabc-165">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="aaabc-165">Current status of the object.</span></span> <span data-ttu-id="aaabc-166">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="aaabc-166">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="aaabc-167">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="aaabc-167">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="aaabc-168">**OK**</span><span class="sxs-lookup"><span data-stu-id="aaabc-168">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="aaabc-169">**Erreurs**</span><span class="sxs-lookup"><span data-stu-id="aaabc-169">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="aaabc-170">**Détérioré**</span><span class="sxs-lookup"><span data-stu-id="aaabc-170">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="aaabc-171">**Connue**</span><span class="sxs-lookup"><span data-stu-id="aaabc-171">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="aaabc-172">**« Échec prévu »**</span><span class="sxs-lookup"><span data-stu-id="aaabc-172">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="aaabc-173">**Démarr**</span><span class="sxs-lookup"><span data-stu-id="aaabc-173">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="aaabc-174">**Arrêt**</span><span class="sxs-lookup"><span data-stu-id="aaabc-174">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="aaabc-175">**Services**</span><span class="sxs-lookup"><span data-stu-id="aaabc-175">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="aaabc-176">**Trop sollicité**</span><span class="sxs-lookup"><span data-stu-id="aaabc-176">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="aaabc-177">**« Non récupéré »**</span><span class="sxs-lookup"><span data-stu-id="aaabc-177">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="aaabc-178">**« Aucun contact »**</span><span class="sxs-lookup"><span data-stu-id="aaabc-178">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="aaabc-179">**« Comm. perdue »**</span><span class="sxs-lookup"><span data-stu-id="aaabc-179">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="aaabc-180">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="aaabc-180">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaabc-181">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aaabc-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aaabc-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aaabc-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaabc-183">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="aaabc-183">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="aaabc-184">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="aaabc-184">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaabc-185">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aaabc-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aaabc-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aaabc-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaabc-187">Nom du système qui héberge le service.</span><span class="sxs-lookup"><span data-stu-id="aaabc-187">Name of the system that hosts the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aaabc-188">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aaabc-188">Requirements</span></span>



| <span data-ttu-id="aaabc-189">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aaabc-189">Requirement</span></span> | <span data-ttu-id="aaabc-190">Valeur</span><span class="sxs-lookup"><span data-stu-id="aaabc-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aaabc-191">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aaabc-191">Minimum supported client</span></span><br/> | <span data-ttu-id="aaabc-192">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aaabc-192">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="aaabc-193">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aaabc-193">Minimum supported server</span></span><br/> | <span data-ttu-id="aaabc-194">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aaabc-194">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="aaabc-195">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="aaabc-195">Namespace</span></span><br/>                | <span data-ttu-id="aaabc-196">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="aaabc-196">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="aaabc-197">MOF</span><span class="sxs-lookup"><span data-stu-id="aaabc-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aaabc-198"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aaabc-198"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="aaabc-199">DLL</span><span class="sxs-lookup"><span data-stu-id="aaabc-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aaabc-200"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="aaabc-200"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="aaabc-201">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aaabc-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaabc-202">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="aaabc-202">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dt>

[<span data-ttu-id="aaabc-203">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="aaabc-203">**CIM\_Service**</span></span>](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 

