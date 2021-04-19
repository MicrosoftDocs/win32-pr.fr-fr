---
description: Décrit le service de GPU 3D synthétique.
ms.assetid: fe3d6105-3def-453a-ad81-97cd0bb4613f
title: Classe Msvm_Synthetic3DService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DService
- Msvm_Synthetic3DService.RequestStateChange
- Msvm_Synthetic3DService.StartService
- Msvm_Synthetic3DService.StopService
- Msvm_Synthetic3DService.InstanceID
- Msvm_Synthetic3DService.Caption
- Msvm_Synthetic3DService.Description
- Msvm_Synthetic3DService.ElementName
- Msvm_Synthetic3DService.InstallDate
- Msvm_Synthetic3DService.OperationalStatus
- Msvm_Synthetic3DService.StatusDescriptions
- Msvm_Synthetic3DService.Status
- Msvm_Synthetic3DService.HealthState
- Msvm_Synthetic3DService.CommunicationStatus
- Msvm_Synthetic3DService.DetailedStatus
- Msvm_Synthetic3DService.OperatingStatus
- Msvm_Synthetic3DService.PrimaryStatus
- Msvm_Synthetic3DService.EnabledState
- Msvm_Synthetic3DService.OtherEnabledState
- Msvm_Synthetic3DService.RequestedState
- Msvm_Synthetic3DService.EnabledDefault
- Msvm_Synthetic3DService.TimeOfLastStateChange
- Msvm_Synthetic3DService.AvailableRequestedStates
- Msvm_Synthetic3DService.TransitioningToState
- Msvm_Synthetic3DService.SystemCreationClassName
- Msvm_Synthetic3DService.SystemName
- Msvm_Synthetic3DService.Name
- Msvm_Synthetic3DService.CreationClassName
- Msvm_Synthetic3DService.PrimaryOwnerName
- Msvm_Synthetic3DService.PrimaryOwnerContact
- Msvm_Synthetic3DService.StartMode
- Msvm_Synthetic3DService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e5bdacb764051f4bee2c9a646a00b09615ee5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517574"
---
# <a name="msvm_synthetic3dservice-class"></a><span data-ttu-id="9192b-103">MSVM \_ Synthetic3DService, classe</span><span class="sxs-lookup"><span data-stu-id="9192b-103">Msvm\_Synthetic3DService class</span></span>

<span data-ttu-id="9192b-104">Décrit le service de GPU 3D synthétique.</span><span class="sxs-lookup"><span data-stu-id="9192b-104">Describes the synthetic 3-D GPU service.</span></span>

> [!Note]  
> <span data-ttu-id="9192b-105">Cette classe n’est pas disponible pour les ordinateurs virtuels de génération 2.</span><span class="sxs-lookup"><span data-stu-id="9192b-105">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="9192b-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9192b-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9192b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9192b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synthetic3DService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Synthetic3D Service";
  string   Description = "Microsoft Synthetic3D Service";
  string   ElementName = "Synthetic3D Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The Synthetic 3D service is fully operational." };
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   Name = "synth3d";
  string   CreationClassName = "Msvm_Synthetic3DService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="9192b-108">Membres</span><span class="sxs-lookup"><span data-stu-id="9192b-108">Members</span></span>

<span data-ttu-id="9192b-109">La classe **MSVM \_ Synthetic3DService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9192b-109">The **Msvm\_Synthetic3DService** class has these types of members:</span></span>

-   [<span data-ttu-id="9192b-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9192b-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="9192b-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9192b-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9192b-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9192b-112">Methods</span></span>

<span data-ttu-id="9192b-113">La classe **MSVM \_ Synthetic3DService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="9192b-113">The **Msvm\_Synthetic3DService** class has these methods.</span></span>



| <span data-ttu-id="9192b-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="9192b-114">Method</span></span>                                                                                     | <span data-ttu-id="9192b-115">Description</span><span class="sxs-lookup"><span data-stu-id="9192b-115">Description</span></span>                                                         |
|:-------------------------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="9192b-116">**DisableGPUForVirtualization**</span><span class="sxs-lookup"><span data-stu-id="9192b-116">**DisableGPUForVirtualization**</span></span>](disablegpuforvirtualization-msvm-synthetic3dservice.md) | <span data-ttu-id="9192b-117">Désactive un GPU physique pour la virtualisation.</span><span class="sxs-lookup"><span data-stu-id="9192b-117">Disables a physical GPU for virtualization.</span></span><br/>              |
| [<span data-ttu-id="9192b-118">**EnableGPUForVirtualization**</span><span class="sxs-lookup"><span data-stu-id="9192b-118">**EnableGPUForVirtualization**</span></span>](enablegpuforvirtualization-msvm-synthetic3dservice.md)   | <span data-ttu-id="9192b-119">Active un GPU physique pour la virtualisation.</span><span class="sxs-lookup"><span data-stu-id="9192b-119">Enables a physical GPU for virtualization.</span></span><br/>               |
| [<span data-ttu-id="9192b-120">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="9192b-120">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-synthetic3dservice.md)             | <span data-ttu-id="9192b-121">Modifie les données de paramètre pour le service 3D synthétique.</span><span class="sxs-lookup"><span data-stu-id="9192b-121">Modifies the setting data for the synthetic 3-D service.</span></span><br/> |
| <span data-ttu-id="9192b-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="9192b-122">**RequestStateChange**</span></span>                                                                     | <span data-ttu-id="9192b-123">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9192b-123">This method is not supported.</span></span><br/>                            |
| <span data-ttu-id="9192b-124">**StartService**</span><span class="sxs-lookup"><span data-stu-id="9192b-124">**StartService**</span></span>                                                                           | <span data-ttu-id="9192b-125">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9192b-125">This method is not supported.</span></span><br/>                            |
| <span data-ttu-id="9192b-126">**StopService**</span><span class="sxs-lookup"><span data-stu-id="9192b-126">**StopService**</span></span>                                                                            | <span data-ttu-id="9192b-127">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9192b-127">This method is not supported.</span></span><br/>                            |



 

### <a name="properties"></a><span data-ttu-id="9192b-128">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9192b-128">Properties</span></span>

<span data-ttu-id="9192b-129">La classe **MSVM \_ Synthetic3DService** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9192b-129">The **Msvm\_Synthetic3DService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9192b-130">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="9192b-130">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-131">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9192b-131">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9192b-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-133">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="9192b-133">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="9192b-134">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9192b-134">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9192b-135">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9192b-135">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9192b-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9192b-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-138">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9192b-138">A short description of the object.</span></span> <span data-ttu-id="9192b-139">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9192b-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9192b-140">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="9192b-140">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-141">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9192b-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9192b-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-143">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="9192b-143">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="9192b-144">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="9192b-144">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9192b-145">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9192b-145">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9192b-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9192b-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-147"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="9192b-147"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-148"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="9192b-148"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-149"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="9192b-149"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-150"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="9192b-150"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-151"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="9192b-151"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-152"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="9192b-152"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9192b-153">)</span><span class="sxs-lookup"><span data-stu-id="9192b-153">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9192b-154">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9192b-154">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9192b-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9192b-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-157">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="9192b-157">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9192b-158">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="9192b-158">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="9192b-159">**Description**</span><span class="sxs-lookup"><span data-stu-id="9192b-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9192b-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9192b-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-162">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="9192b-162">A description of the object.</span></span> <span data-ttu-id="9192b-163">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9192b-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9192b-164">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="9192b-164">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-165">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9192b-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9192b-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-167">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="9192b-167">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="9192b-168">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="9192b-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9192b-169">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9192b-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9192b-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="9192b-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="9192b-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="9192b-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="9192b-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="9192b-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="9192b-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="9192b-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="9192b-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9192b-178">)</span><span class="sxs-lookup"><span data-stu-id="9192b-178">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9192b-179">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9192b-179">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9192b-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9192b-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-182">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9192b-182">A display name for the object.</span></span> <span data-ttu-id="9192b-183">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9192b-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9192b-184">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="9192b-184">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-185">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9192b-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9192b-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-187">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="9192b-187">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="9192b-188">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9192b-188">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9192b-189">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="9192b-189">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-190">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9192b-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9192b-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-192">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="9192b-192">The enabled and disabled states of an element.</span></span> <span data-ttu-id="9192b-193">Il peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="9192b-193">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="9192b-194">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9192b-194">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9192b-195">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="9192b-195">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-196">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9192b-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9192b-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-198">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="9192b-198">The current health of the element.</span></span> <span data-ttu-id="9192b-199">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="9192b-199">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="9192b-200">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="9192b-200">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="9192b-201">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9192b-201">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9192b-202">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9192b-202">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-203">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9192b-203">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9192b-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-205">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="9192b-205">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="9192b-206">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9192b-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9192b-207">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9192b-207">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-208">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9192b-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9192b-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9192b-210">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="9192b-210">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9192b-211">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="9192b-211">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9192b-212">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="9192b-212">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9192b-213">**Nom**</span><span class="sxs-lookup"><span data-stu-id="9192b-213">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-214">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9192b-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9192b-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-216">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="9192b-216">The label by which the object is known.</span></span> <span data-ttu-id="9192b-217">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="9192b-217">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="9192b-218">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="9192b-218">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-219">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9192b-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9192b-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-221">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="9192b-221">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="9192b-222">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="9192b-222">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9192b-223">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9192b-223">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9192b-224"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9192b-224"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-225"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="9192b-225"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-226"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="9192b-226"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-227"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="9192b-227"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-228"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="9192b-228"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-229"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="9192b-229"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-230"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="9192b-230"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-231"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="9192b-231"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-232"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="9192b-232"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-233"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="9192b-233"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-234"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="9192b-234"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-235"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="9192b-235"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-236"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="9192b-236"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-237"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="9192b-237"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-238"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="9192b-238"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-239"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="9192b-239"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-240"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="9192b-240"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-241"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="9192b-241"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-242"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="9192b-242"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9192b-243">)</span><span class="sxs-lookup"><span data-stu-id="9192b-243">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9192b-244">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="9192b-244">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-245">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9192b-245">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9192b-246">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-247">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9192b-247">The current statuses of the object.</span></span> <span data-ttu-id="9192b-248">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9192b-248">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9192b-249">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="9192b-249">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-250">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9192b-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9192b-251">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-252">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="9192b-252">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="9192b-253">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="9192b-253">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="9192b-254">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9192b-254">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9192b-255">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="9192b-255">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-256">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9192b-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9192b-257">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-258">Valeur qui fournit des informations sur la façon dont le propriétaire principal du service est accessible (par exemple, numéro de téléphone, adresse e-mail, etc.).</span><span class="sxs-lookup"><span data-stu-id="9192b-258">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="9192b-259">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="9192b-259">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="9192b-260">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="9192b-260">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-261">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9192b-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9192b-262">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-263">Nom du propriétaire principal du service, s’il est défini.</span><span class="sxs-lookup"><span data-stu-id="9192b-263">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="9192b-264">Le propriétaire principal est le contact de support initial pour le service.</span><span class="sxs-lookup"><span data-stu-id="9192b-264">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="9192b-265">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="9192b-265">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="9192b-266">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="9192b-266">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-267">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9192b-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9192b-268">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-269">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="9192b-269">Provides high level status information.</span></span> <span data-ttu-id="9192b-270">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="9192b-270">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="9192b-271">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="9192b-271">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9192b-272">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9192b-272">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9192b-273"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9192b-273"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-274"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="9192b-274"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-275"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="9192b-275"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-276"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="9192b-276"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-277"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="9192b-277"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9192b-278"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="9192b-278"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9192b-279">)</span><span class="sxs-lookup"><span data-stu-id="9192b-279">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9192b-280">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="9192b-280">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-281">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9192b-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9192b-282">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-283">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="9192b-283">The last requested or desired state for the element.</span></span> <span data-ttu-id="9192b-284">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="9192b-284">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="9192b-285">Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="9192b-285">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="9192b-286">Une instance particulière de la [**classe \_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) peut ne pas prendre en charge la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="9192b-286">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="9192b-287">Si cela se produit, la valeur 12 (non applicable) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="9192b-287">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="9192b-288">Cette propriété est héritée de la **\_ EnabledLogicalElement CIM**.</span><span class="sxs-lookup"><span data-stu-id="9192b-288">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="9192b-289">**Cours**</span><span class="sxs-lookup"><span data-stu-id="9192b-289">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-290">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9192b-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9192b-291">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-292">Indique si le service est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="9192b-292">Indicates whether the service is currently running.</span></span> <span data-ttu-id="9192b-293">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="9192b-293">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="9192b-294">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="9192b-294">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-295">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9192b-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9192b-296">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-297">Valeur de chaîne qui indique si le service est démarré automatiquement par un système, un système d’exploitation ou s’il est démarré uniquement sur demande.</span><span class="sxs-lookup"><span data-stu-id="9192b-297">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="9192b-298">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="9192b-298">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="9192b-299">**État**</span><span class="sxs-lookup"><span data-stu-id="9192b-299">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-300">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9192b-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9192b-301">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-302">État de l’élément.</span><span class="sxs-lookup"><span data-stu-id="9192b-302">The status of the element.</span></span> <span data-ttu-id="9192b-303">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9192b-303">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9192b-304">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9192b-304">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-305">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="9192b-305">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9192b-306">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-307">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="9192b-307">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="9192b-308">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9192b-308">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9192b-309">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9192b-309">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-310">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9192b-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9192b-311">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-312">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="9192b-312">The scoping system's creation class name.</span></span> <span data-ttu-id="9192b-313">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="9192b-313">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="9192b-314">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9192b-314">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-315">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9192b-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9192b-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-317">Nom du système de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="9192b-317">The name of the hosting computer system.</span></span> <span data-ttu-id="9192b-318">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="9192b-318">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="9192b-319">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="9192b-319">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-320">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9192b-320">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9192b-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-322">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="9192b-322">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="9192b-323">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9192b-323">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9192b-324">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="9192b-324">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9192b-325">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9192b-325">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9192b-326">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9192b-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9192b-327">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="9192b-327">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="9192b-328">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9192b-328">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9192b-329">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9192b-329">Requirements</span></span>



| <span data-ttu-id="9192b-330">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9192b-330">Requirement</span></span> | <span data-ttu-id="9192b-331">Valeur</span><span class="sxs-lookup"><span data-stu-id="9192b-331">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9192b-332">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9192b-332">Minimum supported client</span></span><br/> | <span data-ttu-id="9192b-333">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9192b-333">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9192b-334">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9192b-334">Minimum supported server</span></span><br/> | <span data-ttu-id="9192b-335">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9192b-335">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9192b-336">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9192b-336">Namespace</span></span><br/>                | <span data-ttu-id="9192b-337">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9192b-337">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9192b-338">MOF</span><span class="sxs-lookup"><span data-stu-id="9192b-338">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9192b-339"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9192b-339"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9192b-340">DLL</span><span class="sxs-lookup"><span data-stu-id="9192b-340">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9192b-341"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9192b-341"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

