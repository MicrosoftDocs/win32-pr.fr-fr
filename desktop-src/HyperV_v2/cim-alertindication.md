---
description: Une superclasse concrète pour les notifications d’alerte CIM.
ms.assetid: ec4cf41d-decd-4f21-b805-90db4a61376d
title: Classe CIM_AlertIndication
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlertIndication
- CIM_AlertIndication.Description
- CIM_AlertIndication.AlertingManagedElement
- CIM_AlertIndication.AlertingElementFormat
- CIM_AlertIndication.OtherAlertingElementFormat
- CIM_AlertIndication.AlertType
- CIM_AlertIndication.OtherAlertType
- CIM_AlertIndication.PerceivedSeverity
- CIM_AlertIndication.ProbableCause
- CIM_AlertIndication.ProbableCauseDescription
- CIM_AlertIndication.Trending
- CIM_AlertIndication.RecommendedActions
- CIM_AlertIndication.EventID
- CIM_AlertIndication.EventTime
- CIM_AlertIndication.SystemCreationClassName
- CIM_AlertIndication.SystemName
- CIM_AlertIndication.ProviderName
- CIM_AlertIndication.Message
- CIM_AlertIndication.MessageArguments
- CIM_AlertIndication.MessageID
- CIM_AlertIndication.OwningEntity
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a1916705ee696c949dba2a557f7077ade8db7ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517221"
---
# <a name="cim_alertindication-class"></a><span data-ttu-id="eb3f1-103">\_Classe CIM AlertIndication</span><span class="sxs-lookup"><span data-stu-id="eb3f1-103">CIM\_AlertIndication class</span></span>

<span data-ttu-id="eb3f1-104">Une superclasse concrète pour les notifications d’alerte CIM.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-104">A concrete superclass for CIM alert notifications.</span></span> <span data-ttu-id="eb3f1-105">**CIM \_ AlertIndication** est un type spécialisé de classe d' **\_ indication CIM** qui contient des informations sur la gravité, la cause, les actions recommandées et d’autres données pour un événement réel.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-105">**CIM\_AlertIndication** is a specialized type of **CIM\_Indication** class that contains information about the severity, cause, recommended actions, and other data for a real world event.</span></span> <span data-ttu-id="eb3f1-106">Cet événement et ses données peuvent ou non être modélisés dans la hiérarchie de classes CIM.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-106">This event and its data may or may not be modeled in the CIM class hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb3f1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb3f1-107">Syntax</span></span>

``` syntax
[Indication, Version("2.22.0"), UMLPackagePath("CIM::Event"), AMENDMENT]
class CIM_AlertIndication : CIM_ProcessIndication
{
  string   Description;
  string   AlertingManagedElement;
  uint16   AlertingElementFormat = 0;
  string   OtherAlertingElementFormat;
  uint16   AlertType;
  string   OtherAlertType;
  uint16   PerceivedSeverity;
  uint16   ProbableCause;
  string   ProbableCauseDescription;
  uint16   Trending;
  string   RecommendedActions[];
  string   EventID;
  datetime EventTime;
  string   SystemCreationClassName;
  string   SystemName;
  string   ProviderName;
  string   Message;
  string   MessageArguments[];
  string   MessageID;
  string   OwningEntity;
};
```

## <a name="members"></a><span data-ttu-id="eb3f1-108">Membres</span><span class="sxs-lookup"><span data-stu-id="eb3f1-108">Members</span></span>

<span data-ttu-id="eb3f1-109">La classe **CIM \_ AlertIndication** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="eb3f1-109">The **CIM\_AlertIndication** class has these types of members:</span></span>

-   [<span data-ttu-id="eb3f1-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eb3f1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eb3f1-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eb3f1-111">Properties</span></span>

<span data-ttu-id="eb3f1-112">La classe **CIM \_ AlertIndication** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-112">The **CIM\_AlertIndication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eb3f1-113">**AlertingElementFormat**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-113">**AlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb3f1-114">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb3f1-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-116">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**AlertingManagedElement**","**CIM \_ AlertIndication**.**OtherAlertingElementFormat**")</span><span class="sxs-lookup"><span data-stu-id="eb3f1-116">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertingManagedElement**", "**CIM\_AlertIndication**.**OtherAlertingElementFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="eb3f1-117">Format de la propriété **AlertingManagedElement** .</span><span class="sxs-lookup"><span data-stu-id="eb3f1-117">The format of the **AlertingManagedElement** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eb3f1-118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="eb3f1-119">Le format est inconnu ou ne peut pas être interprété de manière significative par une application cliente CIM.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-119">The format is unknown or not meaningfully interpretable by a CIM client application.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="eb3f1-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="eb3f1-121">Le format est défini par la valeur de la propriété OtherAlertingElementFormat.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-121">The format is defined by the value of the OtherAlertingElementFormat property.</span></span>

</dd> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>

<span data-ttu-id="eb3f1-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span></span>


</dt> <dd>

<span data-ttu-id="eb3f1-123">Le format est un CIMObjectPath, qui spécifie une instance dans le schéma CIM.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-123">The format is a CIMObjectPath, specifying an instance in the CIM Schema.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="eb3f1-124">**AlertingManagedElement**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-124">**AlertingManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb3f1-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb3f1-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-127">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**AlertingElementFormat**")</span><span class="sxs-lookup"><span data-stu-id="eb3f1-127">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertingElementFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="eb3f1-128">Informations d’identification de l’entité (IE, l’instance) pour lesquelles cette indication est générée.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-128">The identifying information of the entity (ie, the instance) for which this Indication is generated.</span></span> <span data-ttu-id="eb3f1-129">La propriété contient le chemin d’accès d’une instance, encodé sous la forme d’un paramètre de chaîne, si l’instance est modélisée dans le schéma CIM.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-129">The property contains the path of an instance, encoded as a string parameter - if the instance is modeled in the CIM Schema.</span></span> <span data-ttu-id="eb3f1-130">S’il ne s’agit pas d’une instance CIM, la propriété contient une chaîne d’identification qui nomme l’entité pour laquelle l’alerte est générée.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-130">If not a CIM instance, the property contains some identifying string that names the entity for which the Alert is generated.</span></span> <span data-ttu-id="eb3f1-131">Le chemin d’accès ou la chaîne d’identification est mis en forme selon la propriété AlertingElementFormat.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-131">The path or identifying string is formatted per the AlertingElementFormat property.</span></span>

</dd> <dt>

<span data-ttu-id="eb3f1-132">**AlertType**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-132">**AlertType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb3f1-133">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb3f1-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-135">Qualificateurs : [**requis**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Type d’événement ")</span><span class="sxs-lookup"><span data-stu-id="eb3f1-135">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Event type")</span></span>
</dt> </dl>

<span data-ttu-id="eb3f1-136">Classification principale de l’indication.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-136">The primary classification of the indication.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="eb3f1-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="eb3f1-138">\- Autres.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-138">\- Other.</span></span> <span data-ttu-id="eb3f1-139">La propriété OtherAlertType de l’indication transmet sa classification.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-139">The Indication's OtherAlertType property conveys its classification.</span></span> <span data-ttu-id="eb3f1-140">L’utilisation de « Other » dans une énumération est une convention CIM standard.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-140">Use of "Other" in an enumeration is a standard CIM convention.</span></span> <span data-ttu-id="eb3f1-141">Cela signifie que l’indication actuelle ne tient pas dans les catégories décrites par cette énumération.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-141">It means that the current Indication does not fit into the categories described by this enumeration.</span></span>

</dd> <dt>

<span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>

<span data-ttu-id="eb3f1-142"><span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>**Alerte de communication** (2)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-142"><span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>**Communications Alert** (2)</span></span>


</dt> <dd>

<span data-ttu-id="eb3f1-143">Une indication de ce type est principalement associée aux procédures et/ou aux processus requis pour transmettre des informations d’un point à un autre.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-143">An Indication of this type is principally associated with the procedures and/or processes required to convey information from one point to another.</span></span>

</dd> <dt>

<span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>

<span data-ttu-id="eb3f1-144"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Alerte de qualité de service** (3)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-144"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Quality of Service Alert** (3)</span></span>


</dt> <dd>

<span data-ttu-id="eb3f1-145">Une indication de ce type est principalement associée à une dégradation ou à des erreurs dans les performances ou la fonction d’une entité.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-145">An Indication of this type is principally associated with a degradation or errors in the performance or function of an entity.</span></span>

</dd> <dt>

<span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>

<span data-ttu-id="eb3f1-146"><span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>**Erreur de traitement** (4)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-146"><span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>**Processing Error** (4)</span></span>


</dt> <dd>

<span data-ttu-id="eb3f1-147">Une indication de ce type est principalement associée à un logiciel ou à une erreur de traitement.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-147">An Indication of this type is principally associated with a software or processing fault.</span></span>

</dd> <dt>

<span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>

<span data-ttu-id="eb3f1-148"><span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>**Alerte** de l’appareil (5)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-148"><span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>**Device Alert** (5)</span></span>


</dt> <dd>

<span data-ttu-id="eb3f1-149">Une indication de ce type est principalement associée à une défaillance matérielle ou matérielle.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-149">An Indication of this type is principally associated with an equipment or hardware fault.</span></span>

</dd> <dt>

<span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>

<span data-ttu-id="eb3f1-150"><span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>**Alerte environnementale** (6)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-150"><span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>**Environmental Alert** (6)</span></span>


</dt> <dd>

<span data-ttu-id="eb3f1-151">Alerte environnementale.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-151">Environmental Alert.</span></span> <span data-ttu-id="eb3f1-152">Une indication de ce type est principalement associée à une condition relative à un boîtier dans lequel le matériel réside, ou à d’autres considérations environnementales.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-152">An Indication of this type is principally associated with a condition relating to an enclosure in which the hardware resides, or other environmental considerations.</span></span>

</dd> <dt>

<span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>

<span data-ttu-id="eb3f1-153"><span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>**Modification du modèle** (7)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-153"><span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>**Model Change** (7)</span></span>


</dt> <dd>

<span data-ttu-id="eb3f1-154">L’indication traite les modifications apportées au modèle d’information.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-154">The Indication addresses changes in the Information Model.</span></span> <span data-ttu-id="eb3f1-155">Par exemple, il peut incorporer une indication de cycle de vie pour transmettre la modification de modèle spécifique qui est alerté.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-155">For example, it may embed a Lifecycle Indication to convey the specific model change being alerted.</span></span>

</dd> <dt>

<span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>

<span data-ttu-id="eb3f1-156"><span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>**Alerte de sécurité** (8)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-156"><span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>**Security Alert** (8)</span></span>


</dt> <dd>

<span data-ttu-id="eb3f1-157">.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-157">.</span></span> <span data-ttu-id="eb3f1-158">Une indication de ce type est associée.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-158">An Indication of this type is associated.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="eb3f1-159">**Description**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb3f1-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb3f1-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-162">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Texte supplémentaire»)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-162">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Additional text")</span></span>
</dt> </dl>

<span data-ttu-id="eb3f1-163">Brève description de l’indication.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-163">A short description of the Indication.</span></span>

</dd> <dt>

<span data-ttu-id="eb3f1-164">**EventID**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-164">**EventID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb3f1-165">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb3f1-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-167">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**ProbableCause**")</span><span class="sxs-lookup"><span data-stu-id="eb3f1-167">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="eb3f1-168">Instrumentation ou valeur spécifique au fournisseur qui décrit l’événement réel sous-jacent représenté par l’indication.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-168">An instrumentation or provider specific value that describes the underlying real-world event represented by the indication.</span></span> <span data-ttu-id="eb3f1-169">Les indications ayant la même valeur **eventID** non NULL sont prises en compte, par l’entité de création, pour représenter le même événement.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-169">Indications with the same non-NULL **EventID** value are considered, by the creating entity, to represent the same event.</span></span> <span data-ttu-id="eb3f1-170">La comparaison de deux valeurs **eventID** est définie uniquement pour les indications d’alerte avec des valeurs identiques, non null des propriétés **SystemCreateClassName**, **SystemName** et **providerName** .</span><span class="sxs-lookup"><span data-stu-id="eb3f1-170">The comparison of two **EventID** values is only defined for alert indications with identical, non-NULL values of **SystemCreateClassName**, **SystemName** and **ProviderName** properties.</span></span>

</dd> <dt>

<span data-ttu-id="eb3f1-171">**EventTime**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-171">**EventTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb3f1-172">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-172">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb3f1-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-174">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**ProbableCause**")</span><span class="sxs-lookup"><span data-stu-id="eb3f1-174">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="eb3f1-175">Date et heure qui indique le moment où l’événement sous-jacent a été détecté pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-175">The time and date that indicates when the underlying event was first detected.</span></span> <span data-ttu-id="eb3f1-176">Si ces valeurs sont spécifiées et que l’entité de création ne peut pas fournir ces informations, cette propriété doit avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-176">If this values is specified and the creating entity is not capable of providing this information, this property must be set to **NULL**.</span></span> <span data-ttu-id="eb3f1-177">Cette valeur est basée sur la notion de la date et de l’heure locales de l’objet **CIM \_ ManageSystemElement** qui a généré l’indication.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-177">This value is based on the notion of the local date and time of the **CIM\_ManageSystemElement** object that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="eb3f1-178">**Message**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-178">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb3f1-179">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb3f1-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-181">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**MessageID**","**CIM \_ AlertIndication**.**MessageArguments**")</span><span class="sxs-lookup"><span data-stu-id="eb3f1-181">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**MessageID**", "**CIM\_AlertIndication**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="eb3f1-182">Message mis en forme pour l’indication d’alerte.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-182">The formatted message for the alert indication.</span></span> <span data-ttu-id="eb3f1-183">Ce message est mis en forme en combinant un ou plusieurs des éléments dynamiques spécifiés dans la propriété **MessageArguments** , et avec les éléments statiques identifiés de manière unique par la propriété **MessageID** .</span><span class="sxs-lookup"><span data-stu-id="eb3f1-183">This message is formatted by combining one or more of the dynamic elements specified in the **MessageArguments** property, and with the static elements uniquely identified by the **MessageID** property.</span></span>

</dd> <dt>

<span data-ttu-id="eb3f1-184">**MessageArguments**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-184">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb3f1-185">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-185">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb3f1-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-187">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**Message**« , »**CIM \_ AlertIndication**.**MessageID**»)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-187">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**Message**", "**CIM\_AlertIndication**.**MessageID**")</span></span>
</dt> </dl>

<span data-ttu-id="eb3f1-188">Tableau qui contient le contenu dynamique du message pour l’indication d’alerte.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-188">An array that contains the dynamic content of the message for the alert indication.</span></span>

</dd> <dt>

<span data-ttu-id="eb3f1-189">**ID**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-189">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb3f1-190">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb3f1-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-192">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**Message**« , »**CIM \_ AlertIndication**.**MessageArguments**")</span><span class="sxs-lookup"><span data-stu-id="eb3f1-192">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**Message**", "**CIM\_AlertIndication**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="eb3f1-193">ID unique du format du message, avec l’étendue de l’organisation spécifiée dans **OwningEntity**.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-193">The unique ID of the message format, withing the scope of the organization specified in **OwningEntity**.</span></span>

</dd> <dt>

<span data-ttu-id="eb3f1-194">**OtherAlertingElementFormat**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-194">**OtherAlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb3f1-195">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb3f1-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-197">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**AlertingElementFormat**")</span><span class="sxs-lookup"><span data-stu-id="eb3f1-197">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertingElementFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="eb3f1-198">Définit le format de la propriété **AlertingManagedElement** lorsque la propriété **AlertingElementFormat** est définie sur « 1 » (autre); dans le cas contraire, cette valeur doit être définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-198">Defines the format of the **AlertingManagedElement** property when the **AlertingElementFormat** property is set to "1" (other); otherwise, this value must be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="eb3f1-199">**OtherAlertType**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-199">**OtherAlertType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb3f1-200">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-201">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb3f1-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-202">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**AlertType**")</span><span class="sxs-lookup"><span data-stu-id="eb3f1-202">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertType**")</span></span>
</dt> </dl>

<span data-ttu-id="eb3f1-203">Chaîne qui décrit la valeur **AlertType** lorsque la propriété **AlertType** est définie sur « 1 » (autre changement d’État).</span><span class="sxs-lookup"><span data-stu-id="eb3f1-203">A string that describes the **AlertType** value when the **AlertType** property is set to "1" (Other State Change).</span></span>

</dd> <dt>

<span data-ttu-id="eb3f1-204">**OwningEntity**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-204">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb3f1-205">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb3f1-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb3f1-207">ID unique de l’organisation qui est propriétaire de la définition du format de la propriété de **message** .</span><span class="sxs-lookup"><span data-stu-id="eb3f1-207">The unique ID of the organization that owns the definition of the format of the **Message** property.</span></span> <span data-ttu-id="eb3f1-208">**OwningEntity** doit inclure un nom de droits d’auteur, de marque déposée ou unique qui est détenu par l’entité métier ou le corps de normes qui a défini le format du message.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-208">**OwningEntity** must include a copyrighted, trademarked, or unique name that is owned by the business entity or standards body that defined the message format.</span></span>

</dd> <dt>

<span data-ttu-id="eb3f1-209">**PerceivedSeverity**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-209">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb3f1-210">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb3f1-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-212">Qualificateurs : [**obligatoire**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PerceivedSeverity"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Gravité perçue»)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-212">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PerceivedSeverity"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Perceived severity")</span></span>
</dt> </dl>

<span data-ttu-id="eb3f1-213">Gravité de l’indication d’alerte à partir du point de vue de l’élément qui a déclenché l’alerte.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-213">The severity of the alert indication from the point of view of the element that raised the alert.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eb3f1-214"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-214"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="eb3f1-215">Suit l’utilisation courante.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-215">Follows common usage.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="eb3f1-216"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-216"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="eb3f1-217">Indique que la valeur de la gravité se trouve dans la propriété OtherSeverity.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-217">Indicates that the Severity's value can be found in the OtherSeverity property.</span></span>

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span data-ttu-id="eb3f1-218"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informations** (2)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-218"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="eb3f1-219">Suit l’utilisation courante.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-219">Follows common usage.</span></span>

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="eb3f1-220"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Détérioré/AVERTISSEMENT** (3)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-220"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>


</dt> <dd>

<span data-ttu-id="eb3f1-221">Doit être utilisé pour permettre à l’utilisateur de décider si une action est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-221">Should be used when its appropriate to let the user decide if action is needed.</span></span>

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span data-ttu-id="eb3f1-222"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Mineure** (4)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-222"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Minor** (4)</span></span>


</dt> <dd>

<span data-ttu-id="eb3f1-223">Indique qu’une action est nécessaire, mais que la situation n’est pas grave pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-223">Indicates action is needed, but the situation is not serious at this time.</span></span>

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span data-ttu-id="eb3f1-224"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Principal** (5)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-224"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Major** (5)</span></span>


</dt> <dd>

<span data-ttu-id="eb3f1-225">Indique que l’action est nécessaire maintenant.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-225">Indicates action is needed now.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="eb3f1-226"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critique** (6)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-226"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (6)</span></span>


</dt> <dd>

<span data-ttu-id="eb3f1-227">L’action est nécessaire maintenant et l’étendue est large (peut-être une interruption imminente d’une ressource critique se produira-t-elle).</span><span class="sxs-lookup"><span data-stu-id="eb3f1-227">Action is needed NOW and the scope is broad (perhaps an imminent outage to a critical resource will result).</span></span>

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span data-ttu-id="eb3f1-228"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Irrécupérable/irrécupérable** (7)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-228"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/NonRecoverable** (7)</span></span>


</dt> <dd>

<span data-ttu-id="eb3f1-229">Indique qu’une erreur s’est produite, mais qu’il est trop tard pour prendre une mesure corrective.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-229">Indicates an error occurred, but it's too late to take remedial action.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="eb3f1-230">**ProbableCause**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-230">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb3f1-231">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-231">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-232">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb3f1-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-233">Qualificateurs : [**requis**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Cause probable "," Recommendation. ITU \| M3100. probableCause "," ITU-IANA-Alarm-TC "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**ProbableCauseDescription**","**CIM \_ AlertIndication**.**EventID**","**CIM \_ AlertIndication**.**EventTime**")</span><span class="sxs-lookup"><span data-stu-id="eb3f1-233">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Probable cause", "Recommendation.ITU\|M3100.probableCause", "ITU-IANA-ALARM-TC"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCauseDescription**", "**CIM\_AlertIndication**.**EventID**", "**CIM\_AlertIndication**.**EventTime**")</span></span>
</dt> </dl>

<span data-ttu-id="eb3f1-234">Cause probable de la situation qui a entraîné l’indication de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-234">The probable cause of the situation which resulted in the alert indication.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eb3f1-235">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-235">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="eb3f1-236">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-236">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>

<span data-ttu-id="eb3f1-237">**Erreur de carte/carte** (2)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-237">**Adapter/Card Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="eb3f1-238">**Défaillance du sous-système d’application** (3)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-238">**Application Subsystem Failure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>

<span data-ttu-id="eb3f1-239">**Bande passante réduite** (4)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-239">**Bandwidth Reduced** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>

<span data-ttu-id="eb3f1-240">**Erreur d’établissement** de la connexion (5)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-240">**Connection Establishment Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>

<span data-ttu-id="eb3f1-241">**Erreur de protocole de communication** (6)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-241">**Communications Protocol Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="eb3f1-242">**Défaillance du sous-système de communication** (7)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-242">**Communications Subsystem Failure** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>

<span data-ttu-id="eb3f1-243">**Erreur de configuration/personnalisation** (8)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-243">**Configuration/Customization Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>

<span data-ttu-id="eb3f1-244">**Congestion** (9)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-244">**Congestion** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>

<span data-ttu-id="eb3f1-245">**Données endommagées** (10)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-245">**Corrupt Data** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>

<span data-ttu-id="eb3f1-246">**Limite du nombre de cycles de l’UC dépassée** (11)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-246">**CPU Cycles Limit Exceeded** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>

<span data-ttu-id="eb3f1-247">**Erreur de jeu de données/modem** (12)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-247">**Dataset/Modem Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>

<span data-ttu-id="eb3f1-248">**Signal détérioré** (13)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-248">**Degraded Signal** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>

<span data-ttu-id="eb3f1-249">**Erreur d’interface DTE-DCE** (14)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-249">**DTE-DCE Interface Error** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>

<span data-ttu-id="eb3f1-250">**Porte de boîtier ouverte** (15)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-250">**Enclosure Door Open** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>

<span data-ttu-id="eb3f1-251">**Dysfonctionnements** de l’équipement (16)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-251">**Equipment Malfunction** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>

<span data-ttu-id="eb3f1-252">**Vibration excessive** (17)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-252">**Excessive Vibration** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>

<span data-ttu-id="eb3f1-253">**Erreur de format de fichier** (18)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-253">**File Format Error** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>

<span data-ttu-id="eb3f1-254">**Incendie détecté** (19)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-254">**Fire Detected** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>

<span data-ttu-id="eb3f1-255">**Inondation détectée** (20)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-255">**Flood Detected** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>

<span data-ttu-id="eb3f1-256">**Erreur de tramage** (21)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-256">**Framing Error** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>

<span data-ttu-id="eb3f1-257">**Problème HVAC** (22)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-257">**HVAC Problem** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>

<span data-ttu-id="eb3f1-258">**Humidité inacceptable** (23)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-258">**Humidity Unacceptable** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>

<span data-ttu-id="eb3f1-259">**Erreur de périphérique d’e/s** (24)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-259">**I/O Device Error** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>

<span data-ttu-id="eb3f1-260">**Erreur de l’appareil d’entrée** (25)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-260">**Input Device Error** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>

<span data-ttu-id="eb3f1-261">**Erreur LAN** (26)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-261">**LAN Error** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="eb3f1-262">**Fuite non toxique détectée** (27)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-262">**Non-Toxic Leak Detected** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="eb3f1-263">**Erreur de transmission du nœud local** (28)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-263">**Local Node Transmission Error** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>

<span data-ttu-id="eb3f1-264">**Perte de trame** (29)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-264">**Loss of Frame** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>

<span data-ttu-id="eb3f1-265">**Perte de signal** (30)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-265">**Loss of Signal** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Material_Supply_Exhausted"></span><span id="material_supply_exhausted"></span><span id="MATERIAL_SUPPLY_EXHAUSTED"></span>

<span data-ttu-id="eb3f1-266">**Fourniture de matériel épuisée** (31)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-266">**Material Supply Exhausted** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>

<span data-ttu-id="eb3f1-267">**Problème de multiplexeur** (32)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-267">**Multiplexer Problem** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>

<span data-ttu-id="eb3f1-268">**Mémoire insuffisante** (33)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-268">**Out of Memory** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>

<span data-ttu-id="eb3f1-269">**Erreur de périphérique de sortie** (34)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-269">**Output Device Error** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>

<span data-ttu-id="eb3f1-270">**Performances détériorées** (35)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-270">**Performance Degraded** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>

<span data-ttu-id="eb3f1-271">**Problème d’alimentation** (36)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-271">**Power Problem** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>

<span data-ttu-id="eb3f1-272">**Pression inacceptable** (37)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-272">**Pressure Unacceptable** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>

<span data-ttu-id="eb3f1-273">**Problème de processeur (erreur d’ordinateur interne)** (38)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-273">**Processor Problem (Internal Machine Error)** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>

<span data-ttu-id="eb3f1-274">**Échec** de la pompe (39)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-274">**Pump Failure** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>

<span data-ttu-id="eb3f1-275">**Taille de file d’attente dépassée** (40)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-275">**Queue Size Exceeded** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>

<span data-ttu-id="eb3f1-276">**Échec de réception** (41)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-276">**Receive Failure** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>

<span data-ttu-id="eb3f1-277">**Échec du récepteur** (42)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-277">**Receiver Failure** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="eb3f1-278">**Erreur de transmission du nœud distant** (43)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-278">**Remote Node Transmission Error** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>

<span data-ttu-id="eb3f1-279">**Capacité de la ressource à une capacité proche** (44)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-279">**Resource at or Nearing Capacity** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>

<span data-ttu-id="eb3f1-280">**Temps de réponse excessif** (45)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-280">**Response Time Excessive** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>

<span data-ttu-id="eb3f1-281">**Taux de retransmission excessif** (46)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-281">**Retransmission Rate Excessive** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

<span data-ttu-id="eb3f1-282">**Erreur logicielle** (47)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-282">**Software Error** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>

<span data-ttu-id="eb3f1-283">**Programme logiciel terminé anormalement** (48)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-283">**Software Program Abnormally Terminated** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>

<span data-ttu-id="eb3f1-284">**Erreur du programme logiciel (résultats incorrects)** (49)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-284">**Software Program Error (Incorrect Results)** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>

<span data-ttu-id="eb3f1-285">**Problème de capacité de stockage** (50)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-285">**Storage Capacity Problem** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>

<span data-ttu-id="eb3f1-286">**Température inacceptable** (51)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-286">**Temperature Unacceptable** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>

<span data-ttu-id="eb3f1-287">**Seuil dépassé** (52)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-287">**Threshold Crossed** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>

<span data-ttu-id="eb3f1-288">**Problème de synchronisation** (53)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-288">**Timing Problem** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="eb3f1-289">**Fuite toxique détectée** (54)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-289">**Toxic Leak Detected** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>

<span data-ttu-id="eb3f1-290">**Échec** de la transmission (55)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-290">**Transmit Failure** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>

<span data-ttu-id="eb3f1-291">**Échec** de l’émetteur (56)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-291">**Transmitter Failure** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>

<span data-ttu-id="eb3f1-292">**Ressource sous-jacente non disponible** (57)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-292">**Underlying Resource Unavailable** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Version_MisMatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>

<span data-ttu-id="eb3f1-293">**Incompatibilité de version** (58)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-293">**Version MisMatch** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>

<span data-ttu-id="eb3f1-294">**Alerte précédente effacée** (59)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-294">**Previous Alert Cleared** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Login_Attempts_Failed"></span><span id="login_attempts_failed"></span><span id="LOGIN_ATTEMPTS_FAILED"></span>

<span data-ttu-id="eb3f1-295">**Échec des tentatives de connexion** (60)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-295">**Login Attempts Failed** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>

<span data-ttu-id="eb3f1-296">**Virus logiciel détecté** (61)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-296">**Software Virus Detected** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>

<span data-ttu-id="eb3f1-297">**Violation de la sécurité matérielle** (62)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-297">**Hardware Security Breached** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>

<span data-ttu-id="eb3f1-298">**Déni de service détecté** (63)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-298">**Denial of Service Detected** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Security_Credential_MisMatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>

<span data-ttu-id="eb3f1-299">Non- **concordance des informations d’identification de sécurité** (64)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-299">**Security Credential MisMatch** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>

<span data-ttu-id="eb3f1-300">**Accès non autorisé** (65)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-300">**Unauthorized Access** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>

<span data-ttu-id="eb3f1-301">**Alarme reçue** (66)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-301">**Alarm Received** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>

<span data-ttu-id="eb3f1-302">**Perte de pointeur** (67)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-302">**Loss of Pointer** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>

<span data-ttu-id="eb3f1-303">**Incompatibilité de charge utile** (68)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-303">**Payload Mismatch** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>

<span data-ttu-id="eb3f1-304">**Erreur de transmission** (69)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-304">**Transmission Error** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>

<span data-ttu-id="eb3f1-305">**Taux d’erreur excessif** (70)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-305">**Excessive Error Rate** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>

<span data-ttu-id="eb3f1-306">**Problème de suivi** (71)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-306">**Trace Problem** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>

<span data-ttu-id="eb3f1-307">**Élément non disponible** (72)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-307">**Element Unavailable** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>

<span data-ttu-id="eb3f1-308">**Élément manquant** (73)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-308">**Element Missing** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>

<span data-ttu-id="eb3f1-309">**Perte de plusieurs trames** (74)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-309">**Loss of Multi Frame** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>

<span data-ttu-id="eb3f1-310">**Échec du canal de diffusion** (75)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-310">**Broadcast Channel Failure** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>

<span data-ttu-id="eb3f1-311">**Message reçu non valide** (76)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-311">**Invalid Message Received** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>

<span data-ttu-id="eb3f1-312">**Échec de routage** (77)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-312">**Routing Failure** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>

<span data-ttu-id="eb3f1-313">**Échec du fond de panier** (78)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-313">**Backplane Failure** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>

<span data-ttu-id="eb3f1-314">**Duplication des identificateurs** (79)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-314">**Identifier Duplication** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>

<span data-ttu-id="eb3f1-315">**Échec du chemin d’accès de protection** (80)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-315">**Protection Path Failure** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>

<span data-ttu-id="eb3f1-316">**Perte ou incompatibilité** de la synchronisation (81)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-316">**Sync Loss or Mismatch** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>

<span data-ttu-id="eb3f1-317">**Problème de terminal** (82)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-317">**Terminal Problem** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>

<span data-ttu-id="eb3f1-318">**Échec de l’horloge en temps réel** (83)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-318">**Real Time Clock Failure** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>

<span data-ttu-id="eb3f1-319">**Défaillance** de l’antenne (84)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-319">**Antenna Failure** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>

<span data-ttu-id="eb3f1-320">**Échec de chargement** de la batterie (85)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-320">**Battery Charging Failure** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>

<span data-ttu-id="eb3f1-321">**Défaillance du disque** (86)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-321">**Disk Failure** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>

<span data-ttu-id="eb3f1-322">**Échec du saut de fréquence** (87)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-322">**Frequency Hopping Failure** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>

<span data-ttu-id="eb3f1-323">**Perte de redondance** (88)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-323">**Loss of Redundancy** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>

<span data-ttu-id="eb3f1-324">**Échec** de l’alimentation (89)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-324">**Power Supply Failure** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>

<span data-ttu-id="eb3f1-325">**Problème de qualité du signal** (90)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-325">**Signal Quality Problem** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Discharging"></span><span id="battery_discharging"></span><span id="BATTERY_DISCHARGING"></span>

<span data-ttu-id="eb3f1-326">**Déchargement** de la batterie (91)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-326">**Battery Discharging** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>

<span data-ttu-id="eb3f1-327">**Défaillance** de la batterie (92)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-327">**Battery Failure** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>

<span data-ttu-id="eb3f1-328">**Problème commercial** de l’électricité (93)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-328">**Commercial Power Problem** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>

<span data-ttu-id="eb3f1-329">**Défaillance du ventilateur** (94)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-329">**Fan Failure** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>

<span data-ttu-id="eb3f1-330">**Défaillance du moteur** (95)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-330">**Engine Failure** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>

<span data-ttu-id="eb3f1-331">**Défaillance du capteur** (96)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-331">**Sensor Failure** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>

<span data-ttu-id="eb3f1-332">**Échec de fusible** (97)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-332">**Fuse Failure** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>

<span data-ttu-id="eb3f1-333">**Échec du générateur** (98)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-333">**Generator Failure** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>

<span data-ttu-id="eb3f1-334">**Batterie faible** (99)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-334">**Low Battery** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>

<span data-ttu-id="eb3f1-335">**Carburant faible** (100)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-335">**Low Fuel** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>

<span data-ttu-id="eb3f1-336">**Faible eau** (101)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-336">**Low Water** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>

<span data-ttu-id="eb3f1-337">**Gaz explosif** (102)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-337">**Explosive Gas** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>

<span data-ttu-id="eb3f1-338">**Vents élevés** (103)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-338">**High Winds** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>

<span data-ttu-id="eb3f1-339">**Accumulations de glace** (104)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-339">**Ice Buildup** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>

<span data-ttu-id="eb3f1-340">**Fumée** (105)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-340">**Smoke** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>

<span data-ttu-id="eb3f1-341">**Incompatibilité de mémoire** (106)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-341">**Memory Mismatch** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>

<span data-ttu-id="eb3f1-342">**Cycles de processeur insuffisants** (107)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-342">**Out of CPU Cycles** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>

<span data-ttu-id="eb3f1-343">**Problème de l’environnement logiciel** (108)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-343">**Software Environment Problem** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>

<span data-ttu-id="eb3f1-344">**Échec du téléchargement de logiciels** (109)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-344">**Software Download Failure** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>

<span data-ttu-id="eb3f1-345">**Élément réinitialisé** (110)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-345">**Element Reinitialized** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>

<span data-ttu-id="eb3f1-346">**Délai d’expiration** (111)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-346">**Timeout** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>

<span data-ttu-id="eb3f1-347">**Problèmes de journalisation** (112)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-347">**Logging Problems** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>

<span data-ttu-id="eb3f1-348">**Fuite détectée** (113)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-348">**Leak Detected** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>

<span data-ttu-id="eb3f1-349">**Échec du mécanisme de protection** (114)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-349">**Protection Mechanism Failure** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="Protecting_Resource_Failure"></span><span id="protecting_resource_failure"></span><span id="PROTECTING_RESOURCE_FAILURE"></span>

<span data-ttu-id="eb3f1-350">**Protection des échecs de ressource** (115)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-350">**Protecting Resource Failure** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>

<span data-ttu-id="eb3f1-351">**Incohérence de base de données** (116)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-351">**Database Inconsistency** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>

<span data-ttu-id="eb3f1-352">**Échec de l’authentification** (117)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-352">**Authentication Failure** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>

<span data-ttu-id="eb3f1-353">**Violation de la confidentialité** (118)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-353">**Breach of Confidentiality** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>

<span data-ttu-id="eb3f1-354">**Falsification de câble** (119)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-354">**Cable Tamper** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>

<span data-ttu-id="eb3f1-355">**Informations retardées** (120)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-355">**Delayed Information** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>

<span data-ttu-id="eb3f1-356">**Informations dupliquées** (121)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-356">**Duplicate Information** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>

<span data-ttu-id="eb3f1-357">**Informations manquantes** (122)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-357">**Information Missing** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>

<span data-ttu-id="eb3f1-358">**Modification des informations** (123)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-358">**Information Modification** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>

<span data-ttu-id="eb3f1-359">**Informations hors séquence** (124)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-359">**Information Out of Sequence** (124)</span></span>


</dt> <dd></dd> <dt>

<span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>

<span data-ttu-id="eb3f1-360">**Clé expirée** (125)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-360">**Key Expired** (125)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>

<span data-ttu-id="eb3f1-361">**Échec de la non-répudiation** (126)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-361">**Non-Repudiation Failure** (126)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>

<span data-ttu-id="eb3f1-362">**Activité en dehors des heures** (127)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-362">**Out of Hours Activity** (127)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>

<span data-ttu-id="eb3f1-363">**Hors service** (128)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-363">**Out of Service** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>

<span data-ttu-id="eb3f1-364">**Erreur de procédure** (129)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-364">**Procedural Error** (129)</span></span>


</dt> <dd></dd> <dt>

<span id="Unexpected_Information"></span><span id="unexpected_information"></span><span id="UNEXPECTED_INFORMATION"></span>

<span data-ttu-id="eb3f1-365">**Informations inattendues** (130)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-365">**Unexpected Information** (130)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eb3f1-366">**ProbableCauseDescription**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-366">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb3f1-367">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-368">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb3f1-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-369">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**ProbableCause**")</span><span class="sxs-lookup"><span data-stu-id="eb3f1-369">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="eb3f1-370">Informations supplémentaires relatives à la propriété **ProbableCause** .</span><span class="sxs-lookup"><span data-stu-id="eb3f1-370">Additional information related to the **ProbableCause** property.</span></span>

</dd> <dt>

<span data-ttu-id="eb3f1-371">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-371">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb3f1-372">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-373">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb3f1-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-374">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-374">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="eb3f1-375">Nom du fournisseur qui a généré l’indication.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-375">The name of the provider that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="eb3f1-376">**RecommendedActions**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-376">**RecommendedActions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb3f1-377">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-377">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-378">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb3f1-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-379">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Actions de réparation proposées»)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-379">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Proposed repair actions")</span></span>
</dt> </dl>

<span data-ttu-id="eb3f1-380">Descriptions de forme libre des actions recommandées pour résoudre la cause de la notification.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-380">Free form descriptions of the recommended actions to take to resolve the cause of the notification.</span></span>

</dd> <dt>

<span data-ttu-id="eb3f1-381">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-381">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb3f1-382">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-383">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb3f1-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-384">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-384">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="eb3f1-385">Valeur **CreationClassName** du système d’étendue pour le fournisseur qui a généré l’indication.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-385">The **CreationClassName** value of the scoping system for the provider that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="eb3f1-386">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-386">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb3f1-387">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb3f1-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-389">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-389">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="eb3f1-390">Nom du système d’étendue pour le fournisseur qui a généré l’indication.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-390">The scoping system name for the provider that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="eb3f1-391">**Tendances**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-391">**Trending**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb3f1-392">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-392">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-393">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb3f1-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb3f1-394">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. TrendIndication")</span><span class="sxs-lookup"><span data-stu-id="eb3f1-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.TrendIndication")</span></span>
</dt> </dl>

<span data-ttu-id="eb3f1-395">Fournit des informations sur la tendance à la tendance à la hausse, à la baisse ou à la non-modification.</span><span class="sxs-lookup"><span data-stu-id="eb3f1-395">Provides information on trending - trending up, down or no change.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eb3f1-396">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-396">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="eb3f1-397">**Non applicable** (1)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-397">**Not Applicable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Trending_Up"></span><span id="trending_up"></span><span id="TRENDING_UP"></span>

<span data-ttu-id="eb3f1-398">**Tendance** à la hausse (2)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-398">**Trending Up** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Trending_Down"></span><span id="trending_down"></span><span id="TRENDING_DOWN"></span>

<span data-ttu-id="eb3f1-399">**Tendance à la baisse** (3)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-399">**Trending Down** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="eb3f1-400">**Aucune modification** (4)</span><span class="sxs-lookup"><span data-stu-id="eb3f1-400">**No Change** (4)</span></span>


<span data-ttu-id="eb3f1-401"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="eb3f1-401"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="eb3f1-402">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb3f1-402">Requirements</span></span>



| <span data-ttu-id="eb3f1-403">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb3f1-403">Requirement</span></span> | <span data-ttu-id="eb3f1-404">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb3f1-404">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb3f1-405">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb3f1-405">Minimum supported client</span></span><br/> | <span data-ttu-id="eb3f1-406">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="eb3f1-406">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="eb3f1-407">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb3f1-407">Minimum supported server</span></span><br/> | <span data-ttu-id="eb3f1-408">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="eb3f1-408">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="eb3f1-409">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="eb3f1-409">Namespace</span></span><br/>                | <span data-ttu-id="eb3f1-410">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="eb3f1-410">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="eb3f1-411">MOF</span><span class="sxs-lookup"><span data-stu-id="eb3f1-411">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb3f1-412"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb3f1-412"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb3f1-413">DLL</span><span class="sxs-lookup"><span data-stu-id="eb3f1-413">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb3f1-414"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eb3f1-414"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="eb3f1-415">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb3f1-415">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb3f1-416">**\_PROCESSINDICATION CIM**</span><span class="sxs-lookup"><span data-stu-id="eb3f1-416">**CIM\_ProcessIndication**</span></span>](cim-processindication.md)
</dt> </dl>

 

