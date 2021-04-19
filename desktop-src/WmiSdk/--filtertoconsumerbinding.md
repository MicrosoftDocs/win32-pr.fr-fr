---
description: Est utilisé dans l’inscription des consommateurs d’événements permanents pour associer une instance de \_ \_ EventConsumer à une instance de \_ \_ EventFilter.
ms.assetid: e6a06161-0f1c-4754-ac34-263ccf7bf10d
ms.tgt_platform: multiple
title: Classe __FilterToConsumerBinding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __FilterToConsumerBinding
- All
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
ms.openlocfilehash: 0fd9b7f3cf60d14d27fdf5b5014b57e6f599d67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521163"
---
# <a name="__filtertoconsumerbinding-class"></a><span data-ttu-id="f00b6-103">\_\_FilterToConsumerBinding, classe</span><span class="sxs-lookup"><span data-stu-id="f00b6-103">\_\_FilterToConsumerBinding class</span></span>

<span data-ttu-id="f00b6-104">La classe système **\_ \_ FilterToConsumerBinding** est utilisée dans l’inscription des consommateurs d’événements permanents pour associer une instance de [**\_ \_ EventConsumer**](--eventconsumer.md) à une instance de [**\_ \_ EventFilter**](--eventfilter.md).**\_ \_ FilterToConsumerBinding** est une classe d’association.</span><span class="sxs-lookup"><span data-stu-id="f00b6-104">The **\_\_FilterToConsumerBinding** system class is used in the registration of permanent event consumers to relate an instance of the [**\_\_EventConsumer**](--eventconsumer.md) to an instance of [**\_\_EventFilter**](--eventfilter.md).**\_\_FilterToConsumerBinding** is an association class.</span></span>

<span data-ttu-id="f00b6-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f00b6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f00b6-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="f00b6-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f00b6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f00b6-107">Syntax</span></span>

``` syntax
class __FilterToConsumerBinding : __IndicationRelated
{
  __EventConsumer REF Consumer;
  uint8               CreatorSID[];
  boolean             DeliverSynchronously = False;
  uint32              DeliveryQoS;
  __EventFilter   REF Filter;
  boolean             MaintainSecurityContext = False;
  boolean             SlowDownProviders = False;
};
```

## <a name="members"></a><span data-ttu-id="f00b6-108">Membres</span><span class="sxs-lookup"><span data-stu-id="f00b6-108">Members</span></span>

<span data-ttu-id="f00b6-109">La classe **\_ \_ FilterToConsumerBinding** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f00b6-109">The **\_\_FilterToConsumerBinding** class has these types of members:</span></span>

-   [<span data-ttu-id="f00b6-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f00b6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f00b6-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f00b6-111">Properties</span></span>

<span data-ttu-id="f00b6-112">La classe **\_ \_ FilterToConsumerBinding** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="f00b6-112">The **\_\_FilterToConsumerBinding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f00b6-113">**Consommateur**</span><span class="sxs-lookup"><span data-stu-id="f00b6-113">**Consumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f00b6-114">Type de données : **\_ \_ EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="f00b6-114">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="f00b6-115">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f00b6-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f00b6-116">Qualificateurs : [ **clé**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="f00b6-116">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="f00b6-117">Référence à une instance de [**\_ \_ EventConsumer**](--eventconsumer.md) qui représente le chemin d’accès de l’objet à un consommateur logique, le destinataire d’un événement.</span><span class="sxs-lookup"><span data-stu-id="f00b6-117">Reference to an instance of [**\_\_EventConsumer**](--eventconsumer.md) that represents the object path to a logical consumer, the recipient of an event.</span></span> <span data-ttu-id="f00b6-118">Un consommateur logique est une instance d’une classe dérivée de **\_ \_ EventConsumer**.</span><span class="sxs-lookup"><span data-stu-id="f00b6-118">A logical consumer is an instance of a class derived from **\_\_EventConsumer**.</span></span>

</dd> <dt>

<span data-ttu-id="f00b6-119">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="f00b6-119">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f00b6-120">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="f00b6-120">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f00b6-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f00b6-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f00b6-122">Identificateur de sécurité (SID) qui identifie de façon unique l’utilisateur qui a créé la liaison.</span><span class="sxs-lookup"><span data-stu-id="f00b6-122">Security identifier (SID) that uniquely identifies the user who created the binding.</span></span> <span data-ttu-id="f00b6-123">Selon le système d’exploitation, WMI stocke le SID de l’administrateur ou le SID de l’utilisateur qui crée une instance de **\_ \_ FilterToConsumerBinding**.</span><span class="sxs-lookup"><span data-stu-id="f00b6-123">Depending on the operating system, WMI stores the Administrator SID or the SID of the user that creates an instance of **\_\_FilterToConsumerBinding**.</span></span> <span data-ttu-id="f00b6-124">Pour plus d’informations, consultez [liaison d’un filtre d’événements avec un consommateur logique](binding-an-event-filter-with-a-logical-consumer.md) et [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="f00b6-124">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

</dd> <dt>

<span data-ttu-id="f00b6-125">**DeliverSynchronously**</span><span class="sxs-lookup"><span data-stu-id="f00b6-125">**DeliverSynchronously**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f00b6-126">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f00b6-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f00b6-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f00b6-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f00b6-128">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="f00b6-128">Obsolete.</span></span> <span data-ttu-id="f00b6-129">Utilisez plutôt la propriété **DeliveryQoS** à la place de cette propriété, car si **DeliverSynchronously** est défini sur **true** , il remplace le paramètre de la propriété **DeliveryQoS** .</span><span class="sxs-lookup"><span data-stu-id="f00b6-129">Instead use the **DeliveryQoS** property in place of this property, because if **DeliverSynchronously** is set to **True** it overrides the setting of the **DeliveryQoS** property.</span></span>

</dd> <dt>

<span data-ttu-id="f00b6-130">**DeliveryQoS**</span><span class="sxs-lookup"><span data-stu-id="f00b6-130">**DeliveryQoS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f00b6-131">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f00b6-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f00b6-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f00b6-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f00b6-133">Qualité de service pour un abonnement.</span><span class="sxs-lookup"><span data-stu-id="f00b6-133">Quality of service for a subscription.</span></span> <span data-ttu-id="f00b6-134">Si la propriété **DeliverSynchronously** est définie sur **true**, elle remplace la valeur de la propriété **DeliveryQoS** .</span><span class="sxs-lookup"><span data-stu-id="f00b6-134">If the **DeliverSynchronously** property is set to **True**, it overrides the setting of the **DeliveryQoS** property.</span></span>

<dt>

<span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>

<span data-ttu-id="f00b6-135"><span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>**WMIMSG \_ INDICATEUR de \_ QoS \_ synchrone** (0)</span><span class="sxs-lookup"><span data-stu-id="f00b6-135"><span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>**WMIMSG\_FLAG\_QOS\_SYNCHRONOUS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f00b6-136">Remise synchrone</span><span class="sxs-lookup"><span data-stu-id="f00b6-136">Synchronous delivery</span></span>

<span data-ttu-id="f00b6-137">**Faux**.</span><span class="sxs-lookup"><span data-stu-id="f00b6-137">**False**.</span></span> <span data-ttu-id="f00b6-138">L’événement est remis au consommateur logique de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="f00b6-138">The event is delivered to the logical consumer synchronously.</span></span>

</dd> <dt>

<span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>

<span data-ttu-id="f00b6-139"><span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>**WMIMSG \_ INDICATEUR \_ QoS \_ Express** (1)</span><span class="sxs-lookup"><span data-stu-id="f00b6-139"><span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>**WMIMSG\_FLAG\_QOS\_EXPRESS** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f00b6-140">Livraison express</span><span class="sxs-lookup"><span data-stu-id="f00b6-140">Express delivery</span></span>

<span data-ttu-id="f00b6-141">**Vrai**.</span><span class="sxs-lookup"><span data-stu-id="f00b6-141">**True**.</span></span> <span data-ttu-id="f00b6-142">L’événement est remis au consommateur logique de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="f00b6-142">The event is delivered to the logical consumer asynchronously.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f00b6-143">**Filter**</span><span class="sxs-lookup"><span data-stu-id="f00b6-143">**Filter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f00b6-144">Type de données : **\_ \_ EventFilter**</span><span class="sxs-lookup"><span data-stu-id="f00b6-144">Data type: **\_\_EventFilter**</span></span>
</dt> <dt>

<span data-ttu-id="f00b6-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f00b6-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f00b6-146">Qualificateurs : [ **clé**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="f00b6-146">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="f00b6-147">Référence à une instance de [**\_ \_ EventFilter**](--eventfilter.md) qui représente le chemin d’accès de l’objet à un filtre d’événement qui est une requête qui spécifie le type d’événement à recevoir.</span><span class="sxs-lookup"><span data-stu-id="f00b6-147">Reference to an instance of [**\_\_EventFilter**](--eventfilter.md) that represents the object path to an event filter which is a query that specifies the type of event to be received.</span></span>

</dd> <dt>

<span data-ttu-id="f00b6-148">**MaintainSecurityContext**</span><span class="sxs-lookup"><span data-stu-id="f00b6-148">**MaintainSecurityContext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f00b6-149">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f00b6-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f00b6-150">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f00b6-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f00b6-151">Si la **valeur est true**, les événements sont remis dans le contexte de sécurité dans lequel se trouvait le fournisseur lorsqu’il les a fournies.</span><span class="sxs-lookup"><span data-stu-id="f00b6-151">If **True**, the events are delivered in the same security context that the provider was in when it provided them.</span></span>

> [!Note]  
> <span data-ttu-id="f00b6-152">Seul un consommateur implémenté en tant que DLL (un consommateur in-process) peut recevoir des événements dans le contexte de sécurité du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f00b6-152">Only a consumer implemented as a DLL (an in-process consumer) can receive events in the security context of the provider.</span></span> <span data-ttu-id="f00b6-153">Pour plus d’informations sur la sécurité et les fournisseurs in-process, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="f00b6-153">For more information about in-process providers and security, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span> <span data-ttu-id="f00b6-154">Pour plus d’informations et pour obtenir des exemples, consultez remplacement :[réception d’événements en toute sécurité](receiving-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="f00b6-154">For more information and examples, see replace:[Receiving Events Securely](receiving-events-securely.md).</span></span>

 

</dd> <dt>

<span data-ttu-id="f00b6-155">**SlowDownProviders**</span><span class="sxs-lookup"><span data-stu-id="f00b6-155">**SlowDownProviders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f00b6-156">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f00b6-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f00b6-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f00b6-157">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f00b6-158">Si la **valeur est true**, les fournisseurs sont ralentis si ce consommateur ne peut pas continuer.</span><span class="sxs-lookup"><span data-stu-id="f00b6-158">If **True**, providers are slowed down if this consumer cannot keep up.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f00b6-159">Notes</span><span class="sxs-lookup"><span data-stu-id="f00b6-159">Remarks</span></span>

<span data-ttu-id="f00b6-160">La classe **\_ \_ FilterToConsumerBinding** est dérivée de [**\_ \_ IndicationRelated**](--indicationrelated.md), qui n’a pas de propriétés.</span><span class="sxs-lookup"><span data-stu-id="f00b6-160">The **\_\_FilterToConsumerBinding** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

<span data-ttu-id="f00b6-161">Les consommateurs d’événements permanents utilisent la classe système **\_ \_ FilterToConsumerBinding** pour lier les filtres d’événements aux consommateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="f00b6-161">Permanent event consumers use the **\_\_FilterToConsumerBinding** system class to bind event filters to final consumers.</span></span> <span data-ttu-id="f00b6-162">Une fois que le filtre et le consommateur sont liés, WMI peut transférer les événements qui correspondent au filtre au consommateur correspondant.</span><span class="sxs-lookup"><span data-stu-id="f00b6-162">After the filter and consumer are bound together, WMI can forward events that match the filter to the corresponding consumer.</span></span>

## <a name="examples"></a><span data-ttu-id="f00b6-163">Exemples</span><span class="sxs-lookup"><span data-stu-id="f00b6-163">Examples</span></span>

<span data-ttu-id="f00b6-164">L’exemple de création d’un [événement WMI permanent pour surveiller les fichiers](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell sur la Galerie TechNet utilise **\_ \_ FilterToConsumerBinding** dans le cadre d’un script complexe pour configurer une inscription d’événement WMI permanente.</span><span class="sxs-lookup"><span data-stu-id="f00b6-164">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **\_\_FilterToConsumerBinding** as part of a complex script to set up a permanent WMI event registration.</span></span>

## <a name="requirements"></a><span data-ttu-id="f00b6-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f00b6-165">Requirements</span></span>



| <span data-ttu-id="f00b6-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f00b6-166">Requirement</span></span> | <span data-ttu-id="f00b6-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="f00b6-167">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f00b6-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f00b6-168">Minimum supported client</span></span><br/> | <span data-ttu-id="f00b6-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f00b6-169">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f00b6-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f00b6-170">Minimum supported server</span></span><br/> | <span data-ttu-id="f00b6-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f00b6-171">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="f00b6-172">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f00b6-172">Namespace</span></span><br/>                | <span data-ttu-id="f00b6-173">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="f00b6-173">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="f00b6-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f00b6-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f00b6-175">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="f00b6-175">**\_\_IndicationRelated**</span></span>](--indicationrelated.md)
</dt> <dt>

[<span data-ttu-id="f00b6-176">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="f00b6-176">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="f00b6-177">Surveillance et réponse aux événements avec des consommateurs standard</span><span class="sxs-lookup"><span data-stu-id="f00b6-177">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[<span data-ttu-id="f00b6-178">Événements d’analyse</span><span class="sxs-lookup"><span data-stu-id="f00b6-178">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="f00b6-179">Création d’un filtre d’événements</span><span class="sxs-lookup"><span data-stu-id="f00b6-179">Creating an Event Filter</span></span>](creating-an-event-filter.md)
</dt> <dt>

[<span data-ttu-id="f00b6-180">Sécurisation des événements WMI</span><span class="sxs-lookup"><span data-stu-id="f00b6-180">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

 




