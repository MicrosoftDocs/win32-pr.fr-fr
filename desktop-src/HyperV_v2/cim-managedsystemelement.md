---
description: Le \_ MANAGEDSYSTEMELEMENT CIM est la classe de base pour la hiérarchie des éléments système. Tout composant d’un système peut potentiellement être représenté par cette classe ou ses sous-classes.
ms.assetid: 838cc77f-8a8d-429a-8e17-5ede3cc9b6ed
title: Classe CIM_ManagedSystemElement (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedSystemElement
- CIM_ManagedSystemElement.InstallDate
- CIM_ManagedSystemElement.Name
- CIM_ManagedSystemElement.OperationalStatus
- CIM_ManagedSystemElement.StatusDescriptions
- CIM_ManagedSystemElement.Status
- CIM_ManagedSystemElement.HealthState
- CIM_ManagedSystemElement.CommunicationStatus
- CIM_ManagedSystemElement.DetailedStatus
- CIM_ManagedSystemElement.OperatingStatus
- CIM_ManagedSystemElement.PrimaryStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f16b84e24929d5cfdb6e5dd8855d69a8bce2dfda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203609"
---
# <a name="cim_managedsystemelement-class-hyper-v-management"></a><span data-ttu-id="670c8-104">Classe CIM_ManagedSystemElement (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="670c8-104">CIM_ManagedSystemElement class (Hyper-V management)</span></span>

<span data-ttu-id="670c8-105">**CIM \_ ManagedSystemElement** est la classe de base de la hiérarchie d’éléments système.</span><span class="sxs-lookup"><span data-stu-id="670c8-105">**CIM\_ManagedSystemElement** is the base class for the system element hierarchy.</span></span> <span data-ttu-id="670c8-106">Tout composant d’un système peut potentiellement être représenté par cette classe ou ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="670c8-106">Any component of a system can potentially be represented by this class or its subclasses.</span></span>

## <a name="syntax"></a><span data-ttu-id="670c8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="670c8-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ManagedSystemElement : CIM_ManagedElement
{
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
};
```

## <a name="members"></a><span data-ttu-id="670c8-108">Membres</span><span class="sxs-lookup"><span data-stu-id="670c8-108">Members</span></span>

<span data-ttu-id="670c8-109">La **classe \_ ManagedSystemElement CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="670c8-109">The **CIM\_ManagedSystemElement** class has these types of members:</span></span>

-   [<span data-ttu-id="670c8-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="670c8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="670c8-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="670c8-111">Properties</span></span>

<span data-ttu-id="670c8-112">La **classe \_ ManagedSystemElement CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="670c8-112">The **CIM\_ManagedSystemElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="670c8-113">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="670c8-113">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="670c8-114">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="670c8-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="670c8-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="670c8-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="670c8-116">Indique la capacité de l’instrumentation à communiquer avec cet élément.</span><span class="sxs-lookup"><span data-stu-id="670c8-116">Indicates the ability of the instrumentation to communicate with this element.</span></span> <span data-ttu-id="670c8-117">Une valeur **null** indique que l’instrumentation ne prend pas en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="670c8-117">A **NULL** value indicates that instrumentation does not support this property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="670c8-118">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="670c8-118">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="670c8-119">**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="670c8-119">**Not Available** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>

<span data-ttu-id="670c8-120">**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="670c8-120">**Communication OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="670c8-121">**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="670c8-121">**Lost Communication** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="670c8-122">**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="670c8-122">**No Contact** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="670c8-123">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="670c8-123">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="670c8-124">**Fournisseur réservé** (0x8000...)</span><span class="sxs-lookup"><span data-stu-id="670c8-124">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="670c8-125">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="670c8-125">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="670c8-126">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="670c8-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="670c8-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="670c8-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="670c8-128">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**PrimaryStatus**","**CIM \_ CIM**.**HealthState**")</span><span class="sxs-lookup"><span data-stu-id="670c8-128">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**PrimaryStatus**", "**CIM\_ManagedSystemElement**.**HealthState**")</span></span>
</dt> </dl>

<span data-ttu-id="670c8-129">Indique des détails d’État supplémentaires qui complètent la propriété **PrimaryStatus** .</span><span class="sxs-lookup"><span data-stu-id="670c8-129">Indicates additional status details that complement the **PrimaryStatus** property.</span></span> <span data-ttu-id="670c8-130">Une valeur **null** indique que l’instrumentation ne prend pas en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="670c8-130">A **NULL** value indicates that the instrumentation does not support this property.</span></span>

<dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="670c8-131">**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="670c8-131">**Not Available** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>

<span data-ttu-id="670c8-132">**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="670c8-132">**No Additional Information** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="670c8-133">**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="670c8-133">**Stressed** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>

<span data-ttu-id="670c8-134">**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="670c8-134">**Predictive Failure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="670c8-135">**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="670c8-135">**Non-Recoverable Error** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span data-ttu-id="670c8-136">**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="670c8-136">**Supporting Entity in Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="670c8-137">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="670c8-137">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="670c8-138">**Fournisseur réservé** (0x8000...)</span><span class="sxs-lookup"><span data-stu-id="670c8-138">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="670c8-139">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="670c8-139">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="670c8-140">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="670c8-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="670c8-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="670c8-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="670c8-142">Indique l’état actuel de l’élément.</span><span class="sxs-lookup"><span data-stu-id="670c8-142">Indicates the current health of the element.</span></span> <span data-ttu-id="670c8-143">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement l’intégrité de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="670c8-143">This attribute expresses the health of this element, but not necessarily the health of its subcomponents.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="670c8-144">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="670c8-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="670c8-145">**OK** (5)</span><span class="sxs-lookup"><span data-stu-id="670c8-145">**OK** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="670c8-146">**Détérioré/AVERTISSEMENT** (10)</span><span class="sxs-lookup"><span data-stu-id="670c8-146">**Degraded/Warning** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Minor_failure"></span><span id="minor_failure"></span><span id="MINOR_FAILURE"></span>

<span data-ttu-id="670c8-147">**Défaillance mineure** (15)</span><span class="sxs-lookup"><span data-stu-id="670c8-147">**Minor failure** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Major_failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span>

<span data-ttu-id="670c8-148">**Défaillance majeure** (20)</span><span class="sxs-lookup"><span data-stu-id="670c8-148">**Major failure** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span>

<span data-ttu-id="670c8-149">**Défaillance critique** (25)</span><span class="sxs-lookup"><span data-stu-id="670c8-149">**Critical failure** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable_error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="670c8-150">**Erreur non récupérable** (30)</span><span class="sxs-lookup"><span data-stu-id="670c8-150">**Non-recoverable error** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="670c8-151">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="670c8-151">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="670c8-152">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="670c8-152">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="670c8-153">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="670c8-153">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="670c8-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="670c8-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="670c8-155">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="670c8-155">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="670c8-156">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="670c8-156">Indicates when the object was installed.</span></span> <span data-ttu-id="670c8-157">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="670c8-157">The lack of a value does not indicate that the object is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="670c8-158">**Nom**</span><span class="sxs-lookup"><span data-stu-id="670c8-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="670c8-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="670c8-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="670c8-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="670c8-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="670c8-161">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="670c8-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="670c8-162">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="670c8-162">The label by which the object is known.</span></span> <span data-ttu-id="670c8-163">Lorsqu’elle est sous-classée, la propriété **Name** peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="670c8-163">When subclassed, the **Name** property can be overridden to be a key property.</span></span>

</dd> <dt>

<span data-ttu-id="670c8-164">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="670c8-164">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="670c8-165">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="670c8-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="670c8-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="670c8-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="670c8-167">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**»)</span><span class="sxs-lookup"><span data-stu-id="670c8-167">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="670c8-168">Indique l’état opérationnel actuel de l’élément.</span><span class="sxs-lookup"><span data-stu-id="670c8-168">Indicates the current operational condition of the element.</span></span> <span data-ttu-id="670c8-169">Cette propriété peut être utilisée pour fournir plus de détails sur la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="670c8-169">This property can be used to provide more detail about the value of the **EnabledState** property.</span></span> <span data-ttu-id="670c8-170">Une valeur **null** indique que l’instrumentation ne prend pas en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="670c8-170">A **NULL** value indicates that the instrumentation does not support this property.</span></span>

<span data-ttu-id="670c8-171">« Inconnu » indique</span><span class="sxs-lookup"><span data-stu-id="670c8-171">"Unknown" indicates</span></span>

<span data-ttu-id="670c8-172">« None » indique que</span><span class="sxs-lookup"><span data-stu-id="670c8-172">"None" indicates that</span></span>

<span data-ttu-id="670c8-173">Maintenance</span><span class="sxs-lookup"><span data-stu-id="670c8-173">"Servicing"</span></span>

<span data-ttu-id="670c8-174">Démarr</span><span class="sxs-lookup"><span data-stu-id="670c8-174">"Starting"</span></span>

<span data-ttu-id="670c8-175">Arrêt</span><span class="sxs-lookup"><span data-stu-id="670c8-175">"Stopping"</span></span>

<span data-ttu-id="670c8-176">« Stopped » et « Aborted » sont similaires, bien que le premier, tandis que le dernier</span><span class="sxs-lookup"><span data-stu-id="670c8-176">"Stopped" and "Aborted" are similar, although the former , while the latter i</span></span>

<span data-ttu-id="670c8-177">« Dormant » indique que</span><span class="sxs-lookup"><span data-stu-id="670c8-177">"Dormant" indicates that</span></span>

<span data-ttu-id="670c8-178">« Completed » indique que t</span><span class="sxs-lookup"><span data-stu-id="670c8-178">"Completed" indicates that t</span></span>

<span data-ttu-id="670c8-179">Migrant</span><span class="sxs-lookup"><span data-stu-id="670c8-179">"Migrating"</span></span>

<span data-ttu-id="670c8-180">« Inmigration »</span><span class="sxs-lookup"><span data-stu-id="670c8-180">"Immigrating"</span></span>

<span data-ttu-id="670c8-181">"Emigrating"</span><span class="sxs-lookup"><span data-stu-id="670c8-181">"Emigrating"</span></span>

<span data-ttu-id="670c8-182">« Arrêt en cours »</span><span class="sxs-lookup"><span data-stu-id="670c8-182">"Shutting Down"</span></span>

<span data-ttu-id="670c8-183">« In test »</span><span class="sxs-lookup"><span data-stu-id="670c8-183">"In Test"</span></span>

<span data-ttu-id="670c8-184">Transition</span><span class="sxs-lookup"><span data-stu-id="670c8-184">"Transitioning"</span></span>

<span data-ttu-id="670c8-185">« En service »</span><span class="sxs-lookup"><span data-stu-id="670c8-185">"In Service"</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="670c8-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="670c8-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-187">L’implémentation est en général capable de retourner cette propriété, mais elle ne peut pas le faire pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="670c8-187">The implementation is in general capable of returning this property, but is unable to do so at this time.</span></span>

</dd> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="670c8-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="670c8-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-189">L’implémentation (fournisseur) est capable de retourner une valeur pour cette propriété, mais pas encore pour ce composant matériel ou logiciel spécifique, ou la propriété n’est pas utilisée intentionnellement, car elle n’ajoute aucune information significative (comme dans le cas d’une propriété destinée à ajouter des informations supplémentaires à une autre propriété).</span><span class="sxs-lookup"><span data-stu-id="670c8-189">The implementation (provider) is capable of returning a value for this property, but not ever for this particular piece of hardware/software or the property is intentionally not used because it adds no meaningful information (as in the case of a property that is intended to add additional info to another property).</span></span>

</dd> <dt>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>

<span data-ttu-id="670c8-190"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="670c8-190"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-191">Décrit un élément en cours de configuration, de maintenance, de nettoyage ou de gestion.</span><span class="sxs-lookup"><span data-stu-id="670c8-191">Describes an element being configured, maintained, cleaned, or otherwise administered.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="670c8-192"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="670c8-192"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-193">Décrit un élément en cours d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="670c8-193">Describes an element being initialized.</span></span>

</dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="670c8-194"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="670c8-194"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-195">Décrit un élément qui est amené à s’arrêter de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="670c8-195">Describes an element being brought to an orderly stop.</span></span>

</dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="670c8-196"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="670c8-196"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-197">Un arrêt propre et ordonné s’est produit.</span><span class="sxs-lookup"><span data-stu-id="670c8-197">A clean and orderly stop has occurred.</span></span>

</dd> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>

<span data-ttu-id="670c8-198"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="670c8-198"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-199">Un arrêt brutal s’est produit, où l’État et la configuration de l’élément devront peut-être être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="670c8-199">An abrupt stop has occurred, where the state and configuration of the element might need to be updated.</span></span>

</dd> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>

<span data-ttu-id="670c8-200"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="670c8-200"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-201">L’élément est inactif ou suspendu.</span><span class="sxs-lookup"><span data-stu-id="670c8-201">The element is inactive or quiesced.</span></span>

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span data-ttu-id="670c8-202"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="670c8-202"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-203">L’élément a terminé son opération.</span><span class="sxs-lookup"><span data-stu-id="670c8-203">The element has completed its operation.</span></span> <span data-ttu-id="670c8-204">Cette valeur doit être combinée avec la valeur OK, erreur ou détérioré dans le PrimaryStatus afin qu’un client puisse déterminer si l’opération complète s’est terminée avec OK (réussite), s’est terminée avec une erreur (échec) ou s’est terminée avec une erreur détériorée (l’opération s’est terminée, mais elle n’a pas terminé l’opération ou n’a pas signalé d’erreur).</span><span class="sxs-lookup"><span data-stu-id="670c8-204">This value should be combined with either OK, Error, or Degraded in the PrimaryStatus so that a client can tell if the complete operation Completed with OK (passed), Completed with Error (failed), or Completed with Degraded (the operation finished, but it did not complete OK or did not report an error).</span></span>

</dd> <dt>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>

<span data-ttu-id="670c8-205"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="670c8-205"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-206">L’élément est déplacé entre les éléments hôtes.</span><span class="sxs-lookup"><span data-stu-id="670c8-206">The element is being moved between host elements.</span></span>

</dd> <dt>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>

<span data-ttu-id="670c8-207"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="670c8-207"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-208">L’élément est déplacé à l’extérieur de l’élément hôte.</span><span class="sxs-lookup"><span data-stu-id="670c8-208">The element is being moved away from host element.</span></span>

</dd> <dt>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>

<span data-ttu-id="670c8-209"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="670c8-209"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-210">L’élément est déplacé vers un nouvel élément hôte.</span><span class="sxs-lookup"><span data-stu-id="670c8-210">The element is being moved to new host element.</span></span>

</dd> <dt>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>

<span data-ttu-id="670c8-211"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="670c8-211"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="670c8-212"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="670c8-212"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-213">Décrit un élément qui est amené à s’arrêter brusquement.</span><span class="sxs-lookup"><span data-stu-id="670c8-213">Describes an element being brought to an abrupt stop.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="670c8-214"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="670c8-214"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-215">L’élément exécute des fonctions de test.</span><span class="sxs-lookup"><span data-stu-id="670c8-215">The element is performing test functions.</span></span>

</dd> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>

<span data-ttu-id="670c8-216"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="670c8-216"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-217">Décrit un élément qui se trouve entre les États, autrement dit, il n’est pas entièrement disponible dans son état précédent ou son état suivant.</span><span class="sxs-lookup"><span data-stu-id="670c8-217">Describes an element that is between states, that is, it is not fully available in either its previous state or its next state.</span></span> <span data-ttu-id="670c8-218">Cette valeur doit être utilisée si d’autres valeurs indiquant une transition vers un état spécifique ne sont pas applicables.</span><span class="sxs-lookup"><span data-stu-id="670c8-218">This value should be used if other values indicating a transition to a specific state are not applicable.</span></span>

</dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span data-ttu-id="670c8-219"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="670c8-219"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-220">Décrit un élément qui est en service et opérationnel.</span><span class="sxs-lookup"><span data-stu-id="670c8-220">Describes an element that is in service and operational.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="670c8-221"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="670c8-221"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="670c8-222"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (0x8000...)</span><span class="sxs-lookup"><span data-stu-id="670c8-222"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="670c8-223">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="670c8-223">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="670c8-224">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="670c8-224">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="670c8-225">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="670c8-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="670c8-226">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ManagedSystemElement**.**StatusDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="670c8-226">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ManagedSystemElement**.**StatusDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="670c8-227">Contient des indicateurs de l’état actuel de l’élément.</span><span class="sxs-lookup"><span data-stu-id="670c8-227">Contains indicators of the current status of the element.</span></span> <span data-ttu-id="670c8-228">La première valeur de la propriété **OperationalStatus** doit contenir l’état principal de l’élément.</span><span class="sxs-lookup"><span data-stu-id="670c8-228">The first value of the **OperationalStatus** property should contain the primary status for the element.</span></span>

> [!Note]  
> <span data-ttu-id="670c8-229">La propriété **OperationalStatus** remplace la propriété **Status** déprécié.</span><span class="sxs-lookup"><span data-stu-id="670c8-229">The **OperationalStatus** property replaces the deprecated **Status** property.</span></span> <span data-ttu-id="670c8-230">En raison de l’utilisation répandue de la propriété **Status** existante dans les applications de gestion, nous recommandons vivement que les fournisseurs ou l’instrumentation fournissent à la fois les propriétés **Status** et **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="670c8-230">Due to the widespread use of the existing **Status** property in management applications, we strongly recommend that providers or instrumentation provide both the **Status** and **OperationalStatus** properties.</span></span> <span data-ttu-id="670c8-231">En cas d’instrumentation, **Status**, car il s’agit d’une propriété à valeur unique, doit également fournir l’état principal de l’élément.</span><span class="sxs-lookup"><span data-stu-id="670c8-231">When instrumented, **Status**, because it is a single-valued property, should also provide the primary status of the element.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="670c8-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="670c8-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="670c8-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="670c8-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="670c8-234"><span id="OK"></span><span id="ok"></span>**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="670c8-234"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="670c8-235"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (3)</span><span class="sxs-lookup"><span data-stu-id="670c8-235"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="670c8-236"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (4)</span><span class="sxs-lookup"><span data-stu-id="670c8-236"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (4)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-237">L’élément fonctionne, mais nécessite une attention.</span><span class="sxs-lookup"><span data-stu-id="670c8-237">The element is functioning, but needs attention.</span></span> <span data-ttu-id="670c8-238">Les exemples d’États « soulignés » sont surcharge, surchauffe, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="670c8-238">Examples of "Stressed" states are overload, overheated, and so on.</span></span>

</dd> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>

<span data-ttu-id="670c8-239"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (5)</span><span class="sxs-lookup"><span data-stu-id="670c8-239"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (5)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-240">Un élément fonctionne de façon nominale, mais prédit un échec dans un futur proche.</span><span class="sxs-lookup"><span data-stu-id="670c8-240">An element is functioning nominally but predicting a failure in the near future.</span></span>

</dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="670c8-241"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (6)</span><span class="sxs-lookup"><span data-stu-id="670c8-241"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="670c8-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (7)</span><span class="sxs-lookup"><span data-stu-id="670c8-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="670c8-243"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (8)</span><span class="sxs-lookup"><span data-stu-id="670c8-243"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="670c8-244"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (9)</span><span class="sxs-lookup"><span data-stu-id="670c8-244"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="670c8-245"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (10)</span><span class="sxs-lookup"><span data-stu-id="670c8-245"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (10)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-246">Un arrêt ordonné s’est produit.</span><span class="sxs-lookup"><span data-stu-id="670c8-246">An orderly stop has occurred.</span></span>

</dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span data-ttu-id="670c8-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (11)</span><span class="sxs-lookup"><span data-stu-id="670c8-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (11)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-248">Élément en cours de configuration, de maintenance, de nettoyage ou de gestion.</span><span class="sxs-lookup"><span data-stu-id="670c8-248">An element being configured, maintained, cleaned, or otherwise administered.</span></span>

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="670c8-249"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (12)</span><span class="sxs-lookup"><span data-stu-id="670c8-249"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-250">Le système de surveillance a connaissance de cet élément, mais il n’a jamais pu établir de communication avec lui.</span><span class="sxs-lookup"><span data-stu-id="670c8-250">The monitoring system has knowledge of this element, but has never been able to establish communications with it.</span></span>

</dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="670c8-251"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Perte de communication** (13)</span><span class="sxs-lookup"><span data-stu-id="670c8-251"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-252">L’élément ManagedSystem est connu pour exister et a été contacté avec succès par le passé, mais il est actuellement inaccessible.</span><span class="sxs-lookup"><span data-stu-id="670c8-252">The ManagedSystem Element is known to exist and has been contacted successfully in the past, but is currently unreachable.</span></span>

</dd> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>

<span data-ttu-id="670c8-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (14)</span><span class="sxs-lookup"><span data-stu-id="670c8-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (14)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-254">Arrêt brutal, où l’État et la configuration de l’élément devront peut-être être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="670c8-254">An abrupt stop, where where the state and configuration of the element might need to be updated, has occurred.</span></span>

</dd> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>

<span data-ttu-id="670c8-255"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (15)</span><span class="sxs-lookup"><span data-stu-id="670c8-255"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (15)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-256">L’élément est inactif ou suspendu.</span><span class="sxs-lookup"><span data-stu-id="670c8-256">The element is inactive or quiesced.</span></span>

</dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span data-ttu-id="670c8-257"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (16)</span><span class="sxs-lookup"><span data-stu-id="670c8-257"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (16)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-258">Cet élément peut être « OK », mais qu’un autre élément, dont il dépend, est erroné.</span><span class="sxs-lookup"><span data-stu-id="670c8-258">This element might be "OK" but that another element, on which it is dependent, is in error.</span></span> <span data-ttu-id="670c8-259">Par exemple, un service réseau ou un point de terminaison qui ne peut pas fonctionner en raison de problèmes de réseau de couche inférieure.</span><span class="sxs-lookup"><span data-stu-id="670c8-259">An example is a network service or endpoint that cannot function due to lower-layer networking problems.</span></span>

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span data-ttu-id="670c8-260"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (17)</span><span class="sxs-lookup"><span data-stu-id="670c8-260"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (17)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-261">L’élément a terminé son opération.</span><span class="sxs-lookup"><span data-stu-id="670c8-261">The element has completed its operation.</span></span>

</dd> <dt>

<span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>

<span data-ttu-id="670c8-262"><span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>**Mode d’alimentation** (18)</span><span class="sxs-lookup"><span data-stu-id="670c8-262"><span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>**Power Mode** (18)</span></span>


</dt> <dd>

<span data-ttu-id="670c8-263">L’élément contient des informations supplémentaires sur le modèle d’alimentation contenues dans l’Association PowerManagementService associée.</span><span class="sxs-lookup"><span data-stu-id="670c8-263">The element has additional power model information contained in the Associated PowerManagementService association.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="670c8-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="670c8-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="670c8-265"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (0x8000...)</span><span class="sxs-lookup"><span data-stu-id="670c8-265"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="670c8-266">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="670c8-266">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="670c8-267">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="670c8-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="670c8-268">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="670c8-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="670c8-269">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ManagedSystemElement**.**DetailedStatus**","**CIM \_ CIM**.**HealthState**")</span><span class="sxs-lookup"><span data-stu-id="670c8-269">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ManagedSystemElement**.**DetailedStatus**", "**CIM\_ManagedSystemElement**.**HealthState**")</span></span>
</dt> </dl>

<span data-ttu-id="670c8-270">Indique une valeur d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="670c8-270">Indicates a high-level status value.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="670c8-271">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="670c8-271">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="670c8-272">**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="670c8-272">**OK** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="670c8-273">**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="670c8-273">**Degraded** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="670c8-274">**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="670c8-274">**Error** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="670c8-275">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="670c8-275">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="670c8-276">**Fournisseur réservé** (0x8000...)</span><span class="sxs-lookup"><span data-stu-id="670c8-276">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="670c8-277">**État**</span><span class="sxs-lookup"><span data-stu-id="670c8-277">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="670c8-278">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="670c8-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="670c8-279">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="670c8-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="670c8-280">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**\_ ManagedSystemElement CIM**.**OperationalStatus**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="670c8-280">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_ManagedSystemElement**.**OperationalStatus**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="670c8-281">Indique l’état principal de l’objet.</span><span class="sxs-lookup"><span data-stu-id="670c8-281">Indicates the primary status of the object.</span></span>

> [!Note]  
> <span data-ttu-id="670c8-282">Cette propriété est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="670c8-282">This property is deprecated.</span></span> <span data-ttu-id="670c8-283">Elle est remplacée par la propriété **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="670c8-283">It is replaced by the **OperationalStatus** property.</span></span> <span data-ttu-id="670c8-284">Si vous choisissez d’utiliser la propriété **Status** pour la compatibilité descendante, elle doit être secondaire à la propriété **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="670c8-284">If you choose to use the **Status** property for backward compatibility, it should be secondary to the **OperationalStatus** property.</span></span>

 

<dt>



 <span data-ttu-id="670c8-285">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="670c8-285">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="670c8-286">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="670c8-286">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="670c8-287">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="670c8-287">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="670c8-288">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="670c8-288">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="670c8-289">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="670c8-289">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="670c8-290">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="670c8-290">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="670c8-291">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="670c8-291">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="670c8-292">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="670c8-292">("Service")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="670c8-293">(« Souligné »)</span><span class="sxs-lookup"><span data-stu-id="670c8-293">("Stressed")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="670c8-294">(« Non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="670c8-294">("NonRecover")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="670c8-295">(« Aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="670c8-295">("No Contact")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="670c8-296">(« Comm. perdue »)</span><span class="sxs-lookup"><span data-stu-id="670c8-296">("Lost Comm")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="670c8-297">(« Arrêté »)</span><span class="sxs-lookup"><span data-stu-id="670c8-297">("Stopped")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="670c8-298">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="670c8-298">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="670c8-299">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="670c8-299">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="670c8-300">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="670c8-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="670c8-301">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ManagedSystemElement**.**OperationalStatus**»)</span><span class="sxs-lookup"><span data-stu-id="670c8-301">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ManagedSystemElement**.**OperationalStatus**")</span></span>
</dt> </dl>

<span data-ttu-id="670c8-302">Indique les descriptions des valeurs correspondantes dans le tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="670c8-302">Indicates descriptions of the corresponding values in the **OperationalStatus** array.</span></span> <span data-ttu-id="670c8-303">Par exemple, si un élément de la propriété **OperationalStatus** contient la valeur qui s' **arrête**, l’élément au même index de tableau dans cette propriété peut contenir une explication sur la raison de l’arrêt d’un objet.</span><span class="sxs-lookup"><span data-stu-id="670c8-303">For example, if an element in the **OperationalStatus** property contains the value **Stopping**, then the element at the same array index in this property might contain an explanation as to why an object is being stopped.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="670c8-304">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="670c8-304">Requirements</span></span>



| <span data-ttu-id="670c8-305">Condition requise</span><span class="sxs-lookup"><span data-stu-id="670c8-305">Requirement</span></span> | <span data-ttu-id="670c8-306">Valeur</span><span class="sxs-lookup"><span data-stu-id="670c8-306">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="670c8-307">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="670c8-307">Minimum supported client</span></span><br/> | <span data-ttu-id="670c8-308">Windows 8</span><span class="sxs-lookup"><span data-stu-id="670c8-308">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="670c8-309">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="670c8-309">Minimum supported server</span></span><br/> | <span data-ttu-id="670c8-310">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="670c8-310">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="670c8-311">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="670c8-311">Namespace</span></span><br/>                | <span data-ttu-id="670c8-312">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="670c8-312">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="670c8-313">MOF</span><span class="sxs-lookup"><span data-stu-id="670c8-313">MOF</span></span><br/>                      | <dl> <span data-ttu-id="670c8-314"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="670c8-314"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="670c8-315">DLL</span><span class="sxs-lookup"><span data-stu-id="670c8-315">DLL</span></span><br/>                      | <dl> <span data-ttu-id="670c8-316"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="670c8-316"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="670c8-317">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="670c8-317">See also</span></span>

<dl> <dt>

[<span data-ttu-id="670c8-318">**\_Propriété MANAGEDELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="670c8-318">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

