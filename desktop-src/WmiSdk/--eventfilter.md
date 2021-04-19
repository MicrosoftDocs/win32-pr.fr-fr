---
description: L’inscription d’un consommateur d’événements permanent requiert une instance de la \_ \_ classe système EventFilter.
ms.assetid: 369d3c28-2b69-456f-9144-d7c73e3123bc
ms.tgt_platform: multiple
title: Classe __EventFilter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventFilter
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0316e158eb2098f89106c64ba0057f8d9b4fc26b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520612"
---
# <a name="__eventfilter-class"></a><span data-ttu-id="4881f-103">\_\_EventFilter, classe</span><span class="sxs-lookup"><span data-stu-id="4881f-103">\_\_EventFilter class</span></span>

<span data-ttu-id="4881f-104">L’inscription d’un consommateur d’événements permanent requiert une instance de la classe système **\_ \_ EventFilter** .</span><span class="sxs-lookup"><span data-stu-id="4881f-104">The registration of a permanent event consumer requires an instance of the **\_\_EventFilter** system class.</span></span>

<span data-ttu-id="4881f-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4881f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4881f-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="4881f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4881f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4881f-107">Syntax</span></span>

``` syntax
class __EventFilter : __IndicationRelated
{
  uint8  CreatorSID[] = {1,1,0,0,0,0,0,5,18,0,0,0};
  string EventAccess;
  string EventNamespace;
  string Name;
  string Query;
  string QueryLanguage;
};
```

## <a name="members"></a><span data-ttu-id="4881f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="4881f-108">Members</span></span>

<span data-ttu-id="4881f-109">La classe **\_ \_ EventFilter** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4881f-109">The **\_\_EventFilter** class has these types of members:</span></span>

-   [<span data-ttu-id="4881f-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4881f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4881f-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4881f-111">Properties</span></span>

<span data-ttu-id="4881f-112">La classe **\_ \_ EventFilter** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="4881f-112">The **\_\_EventFilter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4881f-113">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="4881f-113">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4881f-114">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="4881f-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="4881f-115">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4881f-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4881f-116">Identificateur de sécurité (SID) qui identifie de façon unique l’utilisateur qui crée ce filtre.</span><span class="sxs-lookup"><span data-stu-id="4881f-116">Security identifier (SID) that uniquely identifies the user who creates this filter.</span></span> <span data-ttu-id="4881f-117">Windows Management Instrumentation (WMI) stocke le SID de l’utilisateur qui crée une instance de **\_ \_ EventFilter** ou le SID d’administrateur, selon le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4881f-117">Windows Management Instrumentation (WMI) stores the SID of the user that creates an instance of **\_\_EventFilter** or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="4881f-118">Pour plus d’informations, consultez [liaison d’un filtre d’événements avec un consommateur logique](binding-an-event-filter-with-a-logical-consumer.md) et [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="4881f-118">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

</dd> <dt>

<span data-ttu-id="4881f-119">**EventAccess**</span><span class="sxs-lookup"><span data-stu-id="4881f-119">**EventAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4881f-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4881f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4881f-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4881f-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4881f-122">Descripteur de sécurité (SD) dans le langage SDDL (Security Descriptor Definition Language) qui contrôle l’accès aux événements remis au filtre.</span><span class="sxs-lookup"><span data-stu-id="4881f-122">Security descriptor (SD) in Security Descriptor Definition Language (SDDL) that controls access for events delivered to the filter.</span></span> <span data-ttu-id="4881f-123">Utilisez cette propriété pour spécifier que seuls les événements dans le contexte de sécurité de comptes spécifiques peuvent être remis à ce filtre.</span><span class="sxs-lookup"><span data-stu-id="4881f-123">Use this property to specify that only events in the security context of specific accounts can be delivered to this filter.</span></span> <span data-ttu-id="4881f-124">Par exemple, un consommateur d’événements permanent peut effacer les journaux de sécurité uniquement lorsqu’un événement spécifique est généré par un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="4881f-124">For example, a permanent event consumer may clear the security logs only when a specific event is generated by a specific user.</span></span> <span data-ttu-id="4881f-125">Pour spécifier qui peut publier des événements sur ce filtre, utilisez le masque de **\_ \_ publication approprié WBEM** dans l’entrée de Access Control (ACE) pour la propriété [**\_ descripteur de sécurité**](--event.md) .</span><span class="sxs-lookup"><span data-stu-id="4881f-125">To specify who can publish events to this filter, use the **WBEM\_RIGHT\_PUBLISH** mask in the Access Control Entry (ACE) for the [**SECURITY\_DESCRIPTOR**](--event.md) property.</span></span> <span data-ttu-id="4881f-126">Pour plus d’informations, consultez [langage de définition du descripteur de sécurité](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span><span class="sxs-lookup"><span data-stu-id="4881f-126">For more information, see [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span></span> <span data-ttu-id="4881f-127">Pour plus d’informations sur les constantes utilisées pour définir ce descripteur de sécurité, voir la rubrique sur les [constantes de sécurité WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="4881f-127">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span> <span data-ttu-id="4881f-128">Pour plus d’informations et pour obtenir des exemples, consultez remplacement :[réception d’événements en toute sécurité](receiving-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="4881f-128">For more information and examples, see replace:[Receiving Events Securely](receiving-events-securely.md).</span></span>

<span data-ttu-id="4881f-129">Vous pouvez configurer un descripteur de sécurité d’accès aux événements pour autoriser la remise d’un événement uniquement lorsque le compte système local génère l’événement.</span><span class="sxs-lookup"><span data-stu-id="4881f-129">You can configure an event access security descriptor to allow an event to be delivered only when the local system account generates the event.</span></span> <span data-ttu-id="4881f-130">Pour plus d’informations sur la création d’un descripteur de sécurité et l’autorisation de l’accès, consultez [Access Control](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="4881f-130">For more information about creating security descriptor and authorizing access, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="4881f-131">Exemple : la chaîne SDDL suivante autorise uniquement les administrateurs à fournir des événements au filtre.</span><span class="sxs-lookup"><span data-stu-id="4881f-131">Example: The following SDDL string allows only administrators to provide events to the filter.</span></span> <span data-ttu-id="4881f-132">Le droit requis pour fournir des événements est la **\_ publication WBEM Right \_ Publish** (x80).</span><span class="sxs-lookup"><span data-stu-id="4881f-132">The right required to provide events is **WBEM\_RIGHT\_PUBLISH** (x80).</span></span>


```VB
O:BAG:BAD:(A;;0x80;;;BA)
```



</dd> <dt>

<span data-ttu-id="4881f-133">**EventNamespace**</span><span class="sxs-lookup"><span data-stu-id="4881f-133">**EventNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4881f-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4881f-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4881f-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4881f-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4881f-136">Espace de noms de l’instance d’événement utilisée pour les abonnements entre espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="4881f-136">Namespace of the event instance used for cross-namespace subscriptions.</span></span>

</dd> <dt>

<span data-ttu-id="4881f-137">**Nom**</span><span class="sxs-lookup"><span data-stu-id="4881f-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4881f-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4881f-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4881f-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4881f-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4881f-140">Qualificateurs : [ **clé**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="4881f-140">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="4881f-141">Identificateur unique d’un filtre d’événement.</span><span class="sxs-lookup"><span data-stu-id="4881f-141">Unique identifier of an event filter.</span></span> <span data-ttu-id="4881f-142">Étant donné qu’un filtre d’événements est uniquement utilisé en interne par WMI, il est recommandé de définir cette propriété sur un identificateur global unique (**GUID**) converti en chaîne.</span><span class="sxs-lookup"><span data-stu-id="4881f-142">Because an event filter is only used internally by WMI, it is recommended that you set this property to a globally unique identifier (**GUID**) converted to a string.</span></span> <span data-ttu-id="4881f-143">Toutefois, les consommateurs peuvent utiliser n’importe quel schéma privé pour un nom de filtre, à condition qu’il n’y ait pas de conflit avec d’autres filtres.</span><span class="sxs-lookup"><span data-stu-id="4881f-143">However, consumers can use any private scheme for a filter name as long as there is not a conflict with other filters.</span></span>

</dd> <dt>

<span data-ttu-id="4881f-144">**Requête**</span><span class="sxs-lookup"><span data-stu-id="4881f-144">**Query**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4881f-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4881f-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4881f-146">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4881f-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4881f-147">Requête d’événement WQL (Windows Management Instrumentation Query Language) qui spécifie le jeu d’événements pour la notification du consommateur et les conditions spécifiques pour la notification.</span><span class="sxs-lookup"><span data-stu-id="4881f-147">Windows Management Instrumentation Query Language (WQL) event query that specifies the set of events for consumer notification, and the specific conditions for notification.</span></span>

</dd> <dt>

<span data-ttu-id="4881f-148">**QueryLanguage**</span><span class="sxs-lookup"><span data-stu-id="4881f-148">**QueryLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4881f-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4881f-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4881f-150">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4881f-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4881f-151">Langue utilisée pour la requête.</span><span class="sxs-lookup"><span data-stu-id="4881f-151">Language used for the query.</span></span> <span data-ttu-id="4881f-152">Étant donné que WMI prend actuellement en charge uniquement Langage de requêtes WMI (WQL) (WQL) en tant que langage de requête, cette propriété doit avoir la valeur « WQL ».</span><span class="sxs-lookup"><span data-stu-id="4881f-152">Because WMI currently supports only WMI Query Language (WQL) as a query language, this property must be set to "WQL".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4881f-153">Notes</span><span class="sxs-lookup"><span data-stu-id="4881f-153">Remarks</span></span>

<span data-ttu-id="4881f-154">La classe **\_ \_ EventFilter** est dérivée de [**\_ \_ IndicationRelated**](--indicationrelated.md).</span><span class="sxs-lookup"><span data-stu-id="4881f-154">The **\_\_EventFilter** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4881f-155">Exemples</span><span class="sxs-lookup"><span data-stu-id="4881f-155">Examples</span></span>

<span data-ttu-id="4881f-156">L’exemple de création d’un [événement WMI permanent pour surveiller les fichiers](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell sur la Galerie TechNet utilise **\_ \_ EventFilter** dans le cadre d’un script complexe pour configurer une inscription d’événement WMI permanente.</span><span class="sxs-lookup"><span data-stu-id="4881f-156">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **\_\_EventFilter** as part of a complex script to set up a permanent WMI event registration.</span></span>

## <a name="requirements"></a><span data-ttu-id="4881f-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4881f-157">Requirements</span></span>



| <span data-ttu-id="4881f-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4881f-158">Requirement</span></span> | <span data-ttu-id="4881f-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="4881f-159">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4881f-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4881f-160">Minimum supported client</span></span><br/> | <span data-ttu-id="4881f-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4881f-161">Windows Vista</span></span><br/>       |
| <span data-ttu-id="4881f-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4881f-162">Minimum supported server</span></span><br/> | <span data-ttu-id="4881f-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4881f-163">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="4881f-164">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4881f-164">Namespace</span></span><br/>                | <span data-ttu-id="4881f-165">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="4881f-165">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="4881f-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4881f-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4881f-167">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="4881f-167">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="4881f-168">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="4881f-168">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="4881f-169">Création d’un filtre d’événements</span><span class="sxs-lookup"><span data-stu-id="4881f-169">Creating an Event Filter</span></span>](creating-an-event-filter.md)
</dt> <dt>

[<span data-ttu-id="4881f-170">Réception d’événements à tout moment</span><span class="sxs-lookup"><span data-stu-id="4881f-170">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="4881f-171">Surveillance et réponse aux événements avec des consommateurs standard</span><span class="sxs-lookup"><span data-stu-id="4881f-171">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[<span data-ttu-id="4881f-172">Événements d’analyse</span><span class="sxs-lookup"><span data-stu-id="4881f-172">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="4881f-173">Classes de consommateur standard</span><span class="sxs-lookup"><span data-stu-id="4881f-173">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="4881f-174">Sécurisation des événements WMI</span><span class="sxs-lookup"><span data-stu-id="4881f-174">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

