---
description: "\\_L’indication CIM est la classe de base abstraite pour toutes les notifications relatives aux modifications dans les objets de schéma et les données d’objet de schéma, les événements détectés par les fournisseurs et l’instrumentation. Les sous-classes de l' \\_ indication CIM représentent des types de notifications spécifiques."
ms.assetid: 85a70425-7b32-449c-9fc0-1cfbf34d9187
title: Classe CIM_Indication
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Indication
- CIM_Indication.IndicationIdentifier
- CIM_Indication.CorrelatedIndications
- CIM_Indication.IndicationTime
- CIM_Indication.PerceivedSeverity
- CIM_Indication.OtherSeverity
- CIM_Indication.IndicationFilterName
- CIM_Indication.SequenceContext
- CIM_Indication.SequenceNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 46b8d50f2e90d9a51c8ffa0b93de9ac16c889340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527859"
---
# <a name="cim_indication-class"></a><span data-ttu-id="c9d8c-104">\_Classe d’indication CIM</span><span class="sxs-lookup"><span data-stu-id="c9d8c-104">CIM\_Indication class</span></span>

<span data-ttu-id="c9d8c-105">**CIM \_ L’indication** est la classe de base abstraite pour toutes les notifications relatives aux modifications dans les objets de schéma et les données d’objet de schéma, les événements détectés par les fournisseurs et l’instrumentation.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-105">**CIM\_Indication** is the abstract base class for all notifications about changes in schema objects, and schema object data, events detected by providers and instrumentation.</span></span> <span data-ttu-id="c9d8c-106">Les sous-classes de l' **\_ indication CIM** représentent des types de notifications spécifiques.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-106">Subclasses of **CIM\_Indication** represent specific types of notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9d8c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9d8c-107">Syntax</span></span>

``` syntax
[Indication, Version("2.24.0"), UMLPackagePath("CIM::Event"), AMENDMENT]
class CIM_Indication : __ExtrinsicEvent
{
  string   IndicationIdentifier;
  string   CorrelatedIndications[];
  datetime IndicationTime;
  uint16   PerceivedSeverity;
  string   OtherSeverity;
  string   IndicationFilterName;
  string   SequenceContext;
  sint64   SequenceNumber;
};
```

## <a name="members"></a><span data-ttu-id="c9d8c-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c9d8c-108">Members</span></span>

<span data-ttu-id="c9d8c-109">La classe d' **\_ indication CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c9d8c-109">The **CIM\_Indication** class has these types of members:</span></span>

-   [<span data-ttu-id="c9d8c-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c9d8c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c9d8c-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c9d8c-111">Properties</span></span>

<span data-ttu-id="c9d8c-112">La classe d' **\_ indication CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-112">The **CIM\_Indication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c9d8c-113">**CorrelatedIndications**</span><span class="sxs-lookup"><span data-stu-id="c9d8c-113">**CorrelatedIndications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9d8c-114">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="c9d8c-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c9d8c-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9d8c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9d8c-116">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Notifications corrélées»), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ indication CIM**.**IndicationIdentifier**")</span><span class="sxs-lookup"><span data-stu-id="c9d8c-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Correlated notifications"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Indication**.**IndicationIdentifier**")</span></span>
</dt> </dl>

<span data-ttu-id="c9d8c-117">Tableau qui contient les valeurs **IndicationIdentifier** des notifications associées à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-117">A array that contains **IndicationIdentifier** values of notifications that are related this one.</span></span>

</dd> <dt>

<span data-ttu-id="c9d8c-118">**IndicationFilterName**</span><span class="sxs-lookup"><span data-stu-id="c9d8c-118">**IndicationFilterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9d8c-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c9d8c-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9d8c-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9d8c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9d8c-121">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ IndicationFilter.Name")</span><span class="sxs-lookup"><span data-stu-id="c9d8c-121">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_IndicationFilter.Name")</span></span>
</dt> </dl>

<span data-ttu-id="c9d8c-122">Identificateur du filtre d’indication qui traite l’indication.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-122">The identifier of the indication filter that processes the indication.</span></span> <span data-ttu-id="c9d8c-123">Le service d’envoi définit cette propriété.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-123">The sending service sets this property.</span></span> <span data-ttu-id="c9d8c-124">Cette propriété est corrélée avec la propriété **Name** de l’objet **CIM \_ IndicationFilter** .</span><span class="sxs-lookup"><span data-stu-id="c9d8c-124">This property correlates with the **Name** property of the **CIM\_IndicationFilter** object.</span></span> <span data-ttu-id="c9d8c-125">La valeur de **IndicationFilterName** doit utiliser le format suivant :</span><span class="sxs-lookup"><span data-stu-id="c9d8c-125">The value of **IndicationFilterName** should use the following format:</span></span>

-   <span data-ttu-id="c9d8c-126">*<OrgID>*:*<LocalID>*</span><span class="sxs-lookup"><span data-stu-id="c9d8c-126">*<OrgID>*:*<LocalID>*</span></span>
-   <span data-ttu-id="c9d8c-127">*<OrgID>* doit inclure un nom de droits d’auteur, de marque déposée ou unique qui est détenu par l’entité commerciale propriétaire de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-127">*<OrgID>* must include a copyrighted, trademarked, or unique name that is owned by the business entity that owns the object.</span></span>
-   <span data-ttu-id="c9d8c-128">*<OrgID>* ne doivent pas contenir de deux-points ( :)</span><span class="sxs-lookup"><span data-stu-id="c9d8c-128">*<OrgID>* must not contain a colon (:)</span></span>
-   <span data-ttu-id="c9d8c-129">*<LocalID>* identificateur unique choisi par l’entité métier propriétaire de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-129">*<LocalID>* a unique identifier chosen by the business entity that owns the object.</span></span>

</dd> <dt>

<span data-ttu-id="c9d8c-130">**IndicationIdentifier**</span><span class="sxs-lookup"><span data-stu-id="c9d8c-130">**IndicationIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9d8c-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c9d8c-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9d8c-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9d8c-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9d8c-133">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Identificateur de notification»)</span><span class="sxs-lookup"><span data-stu-id="c9d8c-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Notification identifier")</span></span>
</dt> </dl>

<span data-ttu-id="c9d8c-134">Identificateur de l’indication.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-134">An identifier of the indication.</span></span> <span data-ttu-id="c9d8c-135">Cette propriété peut être utilisée comme valeur de clé dans le tableau de propriétés **CorrelatedIndications** .</span><span class="sxs-lookup"><span data-stu-id="c9d8c-135">This property can be used as a key value in the **CorrelatedIndications** property array.</span></span> <span data-ttu-id="c9d8c-136">Par conséquent, **IndicationIdentifier** doit être une valeur unique dans l’espace de noms de cette instance de classe.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-136">Therefore, **IndicationIdentifier** should be a unique value within the namespace of this class instance.</span></span>

<span data-ttu-id="c9d8c-137">Pour vous assurer que **IndicationIdentifier** est unique, il doit utiliser le format suivant :</span><span class="sxs-lookup"><span data-stu-id="c9d8c-137">To ensure that **IndicationIdentifier** is unique, it should use the following format:</span></span>

-   <span data-ttu-id="c9d8c-138">*<OrgID>*:*<LocalID>*</span><span class="sxs-lookup"><span data-stu-id="c9d8c-138">*<OrgID>*:*<LocalID>*</span></span>
-   <span data-ttu-id="c9d8c-139">*<OrgID>* doit inclure un nom de droits d’auteur, de marque déposée ou unique qui est détenu par l’entité commerciale propriétaire de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-139">*<OrgID>* must include a copyrighted, trademarked, or unique name that is owned by the business entity that owns the object.</span></span>
-   <span data-ttu-id="c9d8c-140">*<OrgID>* ne doivent pas contenir de deux-points ( :)</span><span class="sxs-lookup"><span data-stu-id="c9d8c-140">*<OrgID>* must not contain a colon (:)</span></span>
-   <span data-ttu-id="c9d8c-141">*<LocalID>* identificateur unique choisi par l’entité métier propriétaire de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-141">*<LocalID>* a unique identifier chosen by the business entity that owns the object.</span></span>
-   <span data-ttu-id="c9d8c-142">Pour les instances définies par DMTF, *<OrgID>* doit avoir la valeur « CIM ».</span><span class="sxs-lookup"><span data-stu-id="c9d8c-142">For DMTF-defined instances, *<OrgID>* should be set to "CIM".</span></span>

</dd> <dt>

<span data-ttu-id="c9d8c-143">**IndicationTime**</span><span class="sxs-lookup"><span data-stu-id="c9d8c-143">**IndicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9d8c-144">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c9d8c-144">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c9d8c-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9d8c-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9d8c-146">Date et heure de création de l’indication.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-146">The time and date when the indication was created.</span></span> <span data-ttu-id="c9d8c-147">La propriété peut avoir la valeur **null** si l’entité qui a créé l’indication ne peut pas déterminer ces informations.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-147">The property can be set to **NULL** if the entity that created the indication is not capable of determining this information.</span></span>

> [!Note]  
> <span data-ttu-id="c9d8c-148">La valeur **IndicationTime** peut être la même pour les indications générées rapidement.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-148">The **IndicationTime** value can be the same for indications that are generated in rapid succession.</span></span>

 

</dd> <dt>

<span data-ttu-id="c9d8c-149">**OtherSeverity**</span><span class="sxs-lookup"><span data-stu-id="c9d8c-149">**OtherSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9d8c-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c9d8c-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9d8c-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9d8c-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9d8c-152">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ AlertIndication**](cim-alertindication.md).**PerceivedSeverity**")</span><span class="sxs-lookup"><span data-stu-id="c9d8c-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_AlertIndication**](cim-alertindication.md).**PerceivedSeverity**")</span></span>
</dt> </dl>

<span data-ttu-id="c9d8c-153">Gravité de l’indication du point de vue du notificateur lorsque **PerceivedSeverity** a la valeur « 1 » (autre).</span><span class="sxs-lookup"><span data-stu-id="c9d8c-153">The severity of the indication from the notifier's point of view when **PerceivedSeverity** is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="c9d8c-154">**PerceivedSeverity**</span><span class="sxs-lookup"><span data-stu-id="c9d8c-154">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9d8c-155">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9d8c-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c9d8c-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9d8c-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9d8c-157">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Gravité perçue»)</span><span class="sxs-lookup"><span data-stu-id="c9d8c-157">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Perceived severity")</span></span>
</dt> </dl>

<span data-ttu-id="c9d8c-158">Gravité de l’indication du point de vue du notificateur.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-158">The severity of the indication from the notifier's point of view.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c9d8c-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="c9d8c-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c9d8c-160">la gravité perçue de l’indication est inconnue ou indéterminée.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-160">the Perceived Severity of the indication is unknown or indeterminate.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c9d8c-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="c9d8c-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c9d8c-162">Indique que la valeur de la gravité se trouve dans la propriété **OtherSeverity** .</span><span class="sxs-lookup"><span data-stu-id="c9d8c-162">Indicates that the Severity's value can be found in the **OtherSeverity** property.</span></span>

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span data-ttu-id="c9d8c-163"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informations** (2)</span><span class="sxs-lookup"><span data-stu-id="c9d8c-163"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c9d8c-164">Les informations doivent être utilisées lors de la fourniture d’une réponse informatif.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-164">Information should be used when providing an informative response.</span></span>

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="c9d8c-165"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Détérioré/AVERTISSEMENT** (3)</span><span class="sxs-lookup"><span data-stu-id="c9d8c-165"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c9d8c-166">Doit être utilisé pour permettre à l’utilisateur de décider si une action est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-166">Should be used when its appropriate to let the user decide if action is needed.</span></span>

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span data-ttu-id="c9d8c-167"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Mineure** (4)</span><span class="sxs-lookup"><span data-stu-id="c9d8c-167"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Minor** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c9d8c-168">Une action est nécessaire, mais la situation n’est pas grave pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-168">Action is needed, but the situation is not serious at this time.</span></span>

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span data-ttu-id="c9d8c-169"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Principal** (5)</span><span class="sxs-lookup"><span data-stu-id="c9d8c-169"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Major** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c9d8c-170">Une action est nécessaire maintenant.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-170">Action is needed NOW.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="c9d8c-171"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critique** (6)</span><span class="sxs-lookup"><span data-stu-id="c9d8c-171"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c9d8c-172">L’action est nécessaire maintenant et l’étendue est large (peut-être une interruption imminente d’une ressource critique se produira-t-elle).</span><span class="sxs-lookup"><span data-stu-id="c9d8c-172">Action is needed NOW and the scope is broad (perhaps an imminent outage to a critical resource will result).</span></span>

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span data-ttu-id="c9d8c-173"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Irrécupérable/irrécupérable** (7)</span><span class="sxs-lookup"><span data-stu-id="c9d8c-173"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/NonRecoverable** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c9d8c-174">une erreur s’est produite, mais il est trop tard pour prendre une mesure corrective.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-174">an error occurred, but it's too late to take remedial action.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c9d8c-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="c9d8c-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c9d8c-176">**SequenceContext**</span><span class="sxs-lookup"><span data-stu-id="c9d8c-176">**SequenceContext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9d8c-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c9d8c-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9d8c-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9d8c-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9d8c-179">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ indication CIM**.\*\*\*\* Pas à pas»)</span><span class="sxs-lookup"><span data-stu-id="c9d8c-179">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Indication**.**SequenceNumber**")</span></span>
</dt> </dl>

<span data-ttu-id="c9d8c-180">Contexte de séquence de l’identificateur de séquence pour l’indication.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-180">The sequence context of the sequence identifier for the indication.</span></span> <span data-ttu-id="c9d8c-181">Si un service ne prend pas en charge les identificateurs de séquence pour les indications, cette propriété doit avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-181">If a service does not support sequence identifiers for indications, this property should be set to **NULL**.</span></span> <span data-ttu-id="c9d8c-182">Si l’indication est redistribuée, cette propriété reste la même.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-182">If the indication is redelivered, this property remains the same.</span></span>

> [!Note]  
> <span data-ttu-id="c9d8c-183">L’identificateur de séquence pour l’indication permet à un écouteur d’identifier les indications dupliquées lorsque le service tente de réenvoyer des indications, de réorganiser les indications qui arrivent dans le désordre et de détecter les indications perdues.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-183">The sequence identifier for the indication enables a listener to identify duplicate indications when the service attempts to redeliver indications, reorder indications that arrive out of order, and detect lost indications.</span></span>

 

<span data-ttu-id="c9d8c-184">Pour vous assurer que **SequenceContext** est unique, il doit utiliser le format suivant :</span><span class="sxs-lookup"><span data-stu-id="c9d8c-184">To ensure that **SequenceContext** is unique, it should use the following format:</span></span>

-   <span data-ttu-id="c9d8c-185">*indication-Service-Name* \# *CIM-service-START-ID* \# *écouteur-destination-création-heure*</span><span class="sxs-lookup"><span data-stu-id="c9d8c-185">*indication-service-name*\#*cim-service-start-id* \#*listener-destination-creation-time*</span></span>
-   <span data-ttu-id="c9d8c-186">*indication-Service-Name* est la valeur de la propriété **Name** de l’instance **CIM \_ IndicationService** qui fournit l’indication.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-186">*indication-service-name* is the value of the **Name** property of the **CIM\_IndicationService** instance that delivers the indication.</span></span>
-   <span data-ttu-id="c9d8c-187">*CIM-service-START-ID* est un identificateur qui identifie de façon unique l’opération de démarrage d’un service.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-187">*cim-service-start-id* is an identifier that uniquely identifies the start operation of a service.</span></span> <span data-ttu-id="c9d8c-188">Par exemple, il peut s’agir d’un horodateur de l’heure de début ou d’un compteur qui augmente pour chaque démarrage ou redémarrage du service.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-188">For example, this could be a timestamp of the start time, or a counter that increases for each start or restart of the service.</span></span>
-   <span data-ttu-id="c9d8c-189">l' *écouteur-destination-Creation-Time* est un horodateur de l’heure de création de l’instance **CIM \_ ListenerDestination** représentant la destination de l’écouteur. nSince ce format n’est qu’une recommandation, les clients CIM doivent traiter la valeur comme un identificateur opaque pour le contexte de séquence et ne pas reposer sur ce format.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-189">*listener-destination-creation-time* is a timestamp of the creation time of the **CIM\_ListenerDestination** instance representing the listener destination.nSince this format is only a recommendation, CIM clients shall treat the value as an opaque identifier for the sequence context and shall not rely on this format.</span></span>

</dd> <dt>

<span data-ttu-id="c9d8c-190">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="c9d8c-190">**SequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9d8c-191">Type de données : **sint64**</span><span class="sxs-lookup"><span data-stu-id="c9d8c-191">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="c9d8c-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9d8c-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9d8c-193">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ indication CIM**.**SequenceContext**")</span><span class="sxs-lookup"><span data-stu-id="c9d8c-193">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Indication**.**SequenceContext**")</span></span>
</dt> </dl>

<span data-ttu-id="c9d8c-194">Numéro de séquence de l’identificateur de séquence pour l’indication.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-194">The sequence number of the sequence identifier for the indication.</span></span>

> [!Note]  
> <span data-ttu-id="c9d8c-195">L’identificateur de séquence pour l’indication permet à un écouteur d’identifier les indications dupliquées lorsque le service tente de réenvoyer des indications, de réorganiser les indications qui arrivent dans le désordre et de détecter les indications perdues.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-195">The sequence identifier for the indication enables a listener to identify duplicate indications when the service attempts to redeliver indications, reorder indications that arrive out of order, and detect lost indications.</span></span>

 

<span data-ttu-id="c9d8c-196">Le numéro de séquence présente les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="c9d8c-196">The sequence number has the following characteristics:</span></span>

-   <span data-ttu-id="c9d8c-197">Le numéro de séquence est réinitialisé à « 0 » chaque fois que la valeur **SequenceContext** change.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-197">The sequence number is reset to "0" whenever the **SequenceContext** value changes.</span></span>
-   <span data-ttu-id="c9d8c-198">Chaque fois que la destination de l’écouteur reçoit une nouvelle indication, le numéro de séquence est augmenté de « 1 ».</span><span class="sxs-lookup"><span data-stu-id="c9d8c-198">Whenever the listener destination receives a new indication, the sequence number is increased by "1".</span></span>
-   <span data-ttu-id="c9d8c-199">Le numéro de séquence est renvoyé à « 0 » lorsque la plage de valeurs est dépassée.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-199">The sequence number wraps to "0" when the value range is exceeded.</span></span>
-   <span data-ttu-id="c9d8c-200">Si l’indication est redistribuée, le pas à **pas reste le** même.</span><span class="sxs-lookup"><span data-stu-id="c9d8c-200">If the indication is redelivered, the **SequenceNumber** remains the same.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9d8c-201">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9d8c-201">Requirements</span></span>



| <span data-ttu-id="c9d8c-202">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9d8c-202">Requirement</span></span> | <span data-ttu-id="c9d8c-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9d8c-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9d8c-204">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9d8c-204">Minimum supported client</span></span><br/> | <span data-ttu-id="c9d8c-205">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c9d8c-205">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="c9d8c-206">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9d8c-206">Minimum supported server</span></span><br/> | <span data-ttu-id="c9d8c-207">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c9d8c-207">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="c9d8c-208">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c9d8c-208">Namespace</span></span><br/>                | <span data-ttu-id="c9d8c-209">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c9d8c-209">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c9d8c-210">MOF</span><span class="sxs-lookup"><span data-stu-id="c9d8c-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9d8c-211"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9d8c-211"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9d8c-212">DLL</span><span class="sxs-lookup"><span data-stu-id="c9d8c-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9d8c-213"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c9d8c-213"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c9d8c-214">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9d8c-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9d8c-215">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="c9d8c-215">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 

