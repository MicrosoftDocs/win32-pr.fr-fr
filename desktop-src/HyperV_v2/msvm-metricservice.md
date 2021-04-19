---
description: Offre la possibilité de gérer les métriques.
ms.assetid: 39dee432-995d-472a-84c3-eede95dccb43
title: Classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService
- Msvm_MetricService.InstanceID
- Msvm_MetricService.Caption
- Msvm_MetricService.Description
- Msvm_MetricService.ElementName
- Msvm_MetricService.InstallDate
- Msvm_MetricService.OperationalStatus
- Msvm_MetricService.StatusDescriptions
- Msvm_MetricService.Status
- Msvm_MetricService.HealthState
- Msvm_MetricService.CommunicationStatus
- Msvm_MetricService.DetailedStatus
- Msvm_MetricService.OperatingStatus
- Msvm_MetricService.PrimaryStatus
- Msvm_MetricService.EnabledState
- Msvm_MetricService.OtherEnabledState
- Msvm_MetricService.RequestedState
- Msvm_MetricService.EnabledDefault
- Msvm_MetricService.TimeOfLastStateChange
- Msvm_MetricService.AvailableRequestedStates
- Msvm_MetricService.TransitioningToState
- Msvm_MetricService.SystemCreationClassName
- Msvm_MetricService.SystemName
- Msvm_MetricService.Name
- Msvm_MetricService.CreationClassName
- Msvm_MetricService.PrimaryOwnerName
- Msvm_MetricService.PrimaryOwnerContact
- Msvm_MetricService.StartMode
- Msvm_MetricService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c4117e3adf3db5a2b0073615ae999b9f85bb9b18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529437"
---
# <a name="msvm_metricservice-class"></a><span data-ttu-id="d1233-103">MSVM \_ MetricService, classe</span><span class="sxs-lookup"><span data-stu-id="d1233-103">Msvm\_MetricService class</span></span>

<span data-ttu-id="d1233-104">Offre la possibilité de gérer les métriques.</span><span class="sxs-lookup"><span data-stu-id="d1233-104">Provides the ability to manage metrics.</span></span>

<span data-ttu-id="d1233-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d1233-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1233-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1233-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricService : CIM_MetricService
{
  string   InstanceID;
  string   Caption = "Hyper-V Metric Service";
  string   Description = "Provides Hyper-V Metric WMI management";
  string   ElementName = "Hyper-V Metric Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
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
  string   Name = "metricsvc";
  string   CreationClassName = "Msvm_MetricService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="d1233-107">Membres</span><span class="sxs-lookup"><span data-stu-id="d1233-107">Members</span></span>

<span data-ttu-id="d1233-108">La classe **MSVM \_ MetricService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d1233-108">The **Msvm\_MetricService** class has these types of members:</span></span>

-   [<span data-ttu-id="d1233-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d1233-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="d1233-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d1233-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d1233-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d1233-111">Methods</span></span>

<span data-ttu-id="d1233-112">La classe **MSVM \_ MetricService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d1233-112">The **Msvm\_MetricService** class has these methods.</span></span>



| <span data-ttu-id="d1233-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="d1233-113">Method</span></span>                                                                    | <span data-ttu-id="d1233-114">Description</span><span class="sxs-lookup"><span data-stu-id="d1233-114">Description</span></span>                                                                             |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1233-115">**ControlMetrics**</span><span class="sxs-lookup"><span data-stu-id="d1233-115">**ControlMetrics**</span></span>](controlmetrics-msvm-metricservice.md)               | <span data-ttu-id="d1233-116">Utilisé pour contrôler la collection de mesures pour un ou des éléments managés.</span><span class="sxs-lookup"><span data-stu-id="d1233-116">Used to control the collection of metrics for a managed element or elements.</span></span><br/> |
| [<span data-ttu-id="d1233-117">**ControlMetricsByClass**</span><span class="sxs-lookup"><span data-stu-id="d1233-117">**ControlMetricsByClass**</span></span>](msvm-metricservice-controlmetricsbyclass.md) | <span data-ttu-id="d1233-118">Contrôle les métriques par classe.</span><span class="sxs-lookup"><span data-stu-id="d1233-118">Controls the metrics by class.</span></span><br/>                                               |
| [<span data-ttu-id="d1233-119">**ControlSampleTimes**</span><span class="sxs-lookup"><span data-stu-id="d1233-119">**ControlSampleTimes**</span></span>](msvm-metricservice-controlsampletimes.md)       | <span data-ttu-id="d1233-120">Définit les heures de l’exemple de contrôle.</span><span class="sxs-lookup"><span data-stu-id="d1233-120">Sets the control sample times.</span></span><br/>                                               |
| [<span data-ttu-id="d1233-121">**GetMetricValues**</span><span class="sxs-lookup"><span data-stu-id="d1233-121">**GetMetricValues**</span></span>](msvm-metricservice-getmetricvalues.md)             | <span data-ttu-id="d1233-122">Récupère les valeurs de métriques.</span><span class="sxs-lookup"><span data-stu-id="d1233-122">Retrieves the metric values.</span></span><br/>                                                 |
| [<span data-ttu-id="d1233-123">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="d1233-123">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-metricservice.md) | <span data-ttu-id="d1233-124">Modifie les données de paramètre pour le service.</span><span class="sxs-lookup"><span data-stu-id="d1233-124">Modifies the setting data for the service.</span></span><br/>                                   |
| [<span data-ttu-id="d1233-125">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="d1233-125">**RequestStateChange**</span></span>](msvm-metricservice-requeststatechange.md)       | <span data-ttu-id="d1233-126">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="d1233-126">Requests a state change.</span></span><br/>                                                     |
| [<span data-ttu-id="d1233-127">**ShowMetrics**</span><span class="sxs-lookup"><span data-stu-id="d1233-127">**ShowMetrics**</span></span>](msvm-metricservice-showmetrics.md)                     | <span data-ttu-id="d1233-128">Affiche les métriques spécifiées.</span><span class="sxs-lookup"><span data-stu-id="d1233-128">Shows the specified metrics.</span></span><br/>                                                 |
| [<span data-ttu-id="d1233-129">**ShowMetricsByClass**</span><span class="sxs-lookup"><span data-stu-id="d1233-129">**ShowMetricsByClass**</span></span>](msvm-metricservice-showmetricsbyclass.md)       | <span data-ttu-id="d1233-130">Affiche les métriques par classe.</span><span class="sxs-lookup"><span data-stu-id="d1233-130">Shows the metrics by class.</span></span><br/>                                                  |
| [<span data-ttu-id="d1233-131">**StartService**</span><span class="sxs-lookup"><span data-stu-id="d1233-131">**StartService**</span></span>](msvm-metricservice-startservice.md)                   | <span data-ttu-id="d1233-132">démarre le service.</span><span class="sxs-lookup"><span data-stu-id="d1233-132">Starts the service.</span></span><br/>                                                          |
| [<span data-ttu-id="d1233-133">**StopService**</span><span class="sxs-lookup"><span data-stu-id="d1233-133">**StopService**</span></span>](msvm-metricservice-stopservice.md)                     | <span data-ttu-id="d1233-134">arrête le service.</span><span class="sxs-lookup"><span data-stu-id="d1233-134">Stops the service.</span></span><br/>                                                           |



 

### <a name="properties"></a><span data-ttu-id="d1233-135">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d1233-135">Properties</span></span>

<span data-ttu-id="d1233-136">La classe **MSVM \_ MetricService** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d1233-136">The **Msvm\_MetricService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1233-137">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="d1233-137">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-138">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1233-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d1233-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-140">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="d1233-140">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="d1233-141">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d1233-141">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d1233-142">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d1233-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d1233-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1233-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-145">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d1233-145">A short description of the object.</span></span> <span data-ttu-id="d1233-146">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « Hyper-V Metric service ».</span><span class="sxs-lookup"><span data-stu-id="d1233-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service".</span></span>

</dd> <dt>

<span data-ttu-id="d1233-147">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="d1233-147">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-148">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1233-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1233-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-150">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="d1233-150">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="d1233-151">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="d1233-151">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d1233-152">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d1233-152">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d1233-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d1233-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="d1233-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="d1233-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="d1233-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="d1233-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="d1233-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d1233-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d1233-160">)</span><span class="sxs-lookup"><span data-stu-id="d1233-160">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d1233-161">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d1233-161">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d1233-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1233-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-164">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="d1233-164">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d1233-165">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur « MSVM \_ MetricService ».</span><span class="sxs-lookup"><span data-stu-id="d1233-165">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_MetricService".</span></span>

</dd> <dt>

<span data-ttu-id="d1233-166">**Description**</span><span class="sxs-lookup"><span data-stu-id="d1233-166">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-167">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d1233-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1233-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-169">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="d1233-169">A description of the object.</span></span> <span data-ttu-id="d1233-170">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « fournit la gestion WMI de métrique Hyper-V ».</span><span class="sxs-lookup"><span data-stu-id="d1233-170">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Provides Hyper-V Metric WMI management".</span></span>

</dd> <dt>

<span data-ttu-id="d1233-171">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="d1233-171">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-172">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1233-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1233-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-174">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="d1233-174">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="d1233-175">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="d1233-175">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d1233-176">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d1233-176">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d1233-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="d1233-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-178"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="d1233-178"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-179"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="d1233-179"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-180"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="d1233-180"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-181"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="d1233-181"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-182"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="d1233-182"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-183"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="d1233-183"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-184"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d1233-184"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d1233-185">)</span><span class="sxs-lookup"><span data-stu-id="d1233-185">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d1233-186">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d1233-186">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-187">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d1233-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1233-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-189">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d1233-189">A display name for the object.</span></span> <span data-ttu-id="d1233-190">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « Hyper-V Metric service ».</span><span class="sxs-lookup"><span data-stu-id="d1233-190">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service".</span></span>

</dd> <dt>

<span data-ttu-id="d1233-191">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="d1233-191">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-192">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1233-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1233-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-194">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="d1233-194">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="d1233-195">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="d1233-195">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="d1233-196">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d1233-196">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-197">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d1233-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1233-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-199">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="d1233-199">The enabled and disabled states of an element.</span></span> <span data-ttu-id="d1233-200">Cette propriété peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="d1233-200">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="d1233-201">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="d1233-201">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="d1233-202">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="d1233-202">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-203">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1233-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1233-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-205">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="d1233-205">The current health of the element.</span></span> <span data-ttu-id="d1233-206">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="d1233-206">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="d1233-207">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="d1233-207">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="d1233-208">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="d1233-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="d1233-209">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d1233-209">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-210">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d1233-210">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d1233-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-212">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="d1233-212">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="d1233-213">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d1233-213">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d1233-214">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d1233-214">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-215">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d1233-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1233-216">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1233-217">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="d1233-217">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d1233-218">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="d1233-218">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d1233-219">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="d1233-219">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d1233-220">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d1233-220">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-221">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d1233-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1233-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-223">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="d1233-223">The label by which the object is known.</span></span> <span data-ttu-id="d1233-224">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur « metricsvc ».</span><span class="sxs-lookup"><span data-stu-id="d1233-224">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "metricsvc".</span></span>

</dd> <dt>

<span data-ttu-id="d1233-225">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="d1233-225">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-226">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1233-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1233-227">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-228">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="d1233-228">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="d1233-229">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="d1233-229">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d1233-230">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d1233-230">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d1233-231"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d1233-231"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-232"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="d1233-232"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-233"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="d1233-233"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="d1233-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-235"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="d1233-235"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-236"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="d1233-236"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-237"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="d1233-237"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-238"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="d1233-238"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-239"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="d1233-239"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-240"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="d1233-240"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-241"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="d1233-241"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-242"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="d1233-242"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-243"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="d1233-243"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-244"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="d1233-244"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-245"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="d1233-245"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-246"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="d1233-246"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="d1233-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="d1233-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d1233-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d1233-250">)</span><span class="sxs-lookup"><span data-stu-id="d1233-250">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d1233-251">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d1233-251">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-252">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1233-252">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d1233-253">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-254">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d1233-254">The current statuses of the object.</span></span> <span data-ttu-id="d1233-255">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau a toujours la valeur 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="d1233-255">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="d1233-256">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="d1233-256">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-257">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d1233-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1233-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-259">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="d1233-259">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="d1233-260">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="d1233-260">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="d1233-261">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="d1233-261">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d1233-262">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="d1233-262">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-263">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d1233-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1233-264">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-265">Valeur qui fournit des informations sur la façon dont le propriétaire principal du service est accessible (par exemple, numéro de téléphone, adresse e-mail, etc.).</span><span class="sxs-lookup"><span data-stu-id="d1233-265">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="d1233-266">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="d1233-266">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d1233-267">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="d1233-267">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-268">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d1233-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1233-269">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-270">Nom du propriétaire principal du service, s’il est défini.</span><span class="sxs-lookup"><span data-stu-id="d1233-270">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="d1233-271">Le propriétaire principal est le contact de support initial pour le service.</span><span class="sxs-lookup"><span data-stu-id="d1233-271">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="d1233-272">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="d1233-272">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d1233-273">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="d1233-273">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-274">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1233-274">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1233-275">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-276">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="d1233-276">Provides high level status information.</span></span> <span data-ttu-id="d1233-277">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="d1233-277">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="d1233-278">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="d1233-278">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d1233-279">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d1233-279">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d1233-280"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d1233-280"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-281"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="d1233-281"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-282"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="d1233-282"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-283"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="d1233-283"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-284"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="d1233-284"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d1233-285"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d1233-285"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d1233-286">)</span><span class="sxs-lookup"><span data-stu-id="d1233-286">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d1233-287">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="d1233-287">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-288">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1233-288">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1233-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-290">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="d1233-290">The last requested or desired state for the element.</span></span> <span data-ttu-id="d1233-291">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="d1233-291">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="d1233-292">Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="d1233-292">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="d1233-293">Une instance particulière de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) peut ne pas prendre en charge la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="d1233-293">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="d1233-294">Si cela se produit, la valeur 12 (non applicable) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="d1233-294">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="d1233-295">Cette propriété est héritée de la **\_ EnabledLogicalElement CIM** et est toujours définie sur 12 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="d1233-295">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="d1233-296">**Cours**</span><span class="sxs-lookup"><span data-stu-id="d1233-296">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-297">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d1233-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1233-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-299">Indique si le service est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d1233-299">Indicates whether the service is currently running.</span></span> <span data-ttu-id="d1233-300">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="d1233-300">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="d1233-301">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="d1233-301">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-302">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d1233-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1233-303">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-304">Valeur de chaîne qui indique si le service est démarré automatiquement par un système, un système d’exploitation ou s’il est démarré uniquement sur demande.</span><span class="sxs-lookup"><span data-stu-id="d1233-304">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="d1233-305">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="d1233-305">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d1233-306">**État**</span><span class="sxs-lookup"><span data-stu-id="d1233-306">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-307">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d1233-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1233-308">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-309">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur « OK ».</span><span class="sxs-lookup"><span data-stu-id="d1233-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="d1233-310">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d1233-310">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-311">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="d1233-311">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d1233-312">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-313">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="d1233-313">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="d1233-314">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et les chaînes ont toujours la valeur « OK ».</span><span class="sxs-lookup"><span data-stu-id="d1233-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and the strings are always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="d1233-315">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d1233-315">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-316">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d1233-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1233-317">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-318">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="d1233-318">The scoping system's creation class name.</span></span> <span data-ttu-id="d1233-319">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur « MSVM \_ ComputerSystem ».</span><span class="sxs-lookup"><span data-stu-id="d1233-319">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="d1233-320">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d1233-320">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-321">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d1233-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1233-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-323">Nom du système de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="d1233-323">The name of the hosting computer system.</span></span> <span data-ttu-id="d1233-324">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="d1233-324">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="d1233-325">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="d1233-325">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-326">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d1233-326">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d1233-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-328">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="d1233-328">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="d1233-329">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d1233-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d1233-330">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="d1233-330">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1233-331">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1233-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1233-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1233-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1233-333">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="d1233-333">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="d1233-334">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d1233-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d1233-335">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1233-335">Requirements</span></span>



| <span data-ttu-id="d1233-336">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1233-336">Requirement</span></span> | <span data-ttu-id="d1233-337">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1233-337">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1233-338">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1233-338">Minimum supported client</span></span><br/> | <span data-ttu-id="d1233-339">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1233-339">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d1233-340">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1233-340">Minimum supported server</span></span><br/> | <span data-ttu-id="d1233-341">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1233-341">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d1233-342">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d1233-342">Namespace</span></span><br/>                | <span data-ttu-id="d1233-343">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="d1233-343">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d1233-344">MOF</span><span class="sxs-lookup"><span data-stu-id="d1233-344">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1233-345"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1233-345"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1233-346">DLL</span><span class="sxs-lookup"><span data-stu-id="d1233-346">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1233-347"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d1233-347"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

