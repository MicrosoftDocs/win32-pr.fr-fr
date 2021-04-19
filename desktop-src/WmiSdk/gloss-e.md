---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 40d26ea1-3081-4afd-8b12-bc6521fad390
ms.tgt_platform: multiple
title: E (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd162feb3936712b396db016de036f78aea35a09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524433"
---
# <a name="e-wmi"></a><span data-ttu-id="f5e06-103">E (WMI)</span><span class="sxs-lookup"><span data-stu-id="f5e06-103">E (WMI)</span></span>

<span data-ttu-id="f5e06-104">[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) e [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="f5e06-104">[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) E [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="f5e06-105"><span id="wmi.gloss_event_class"></span><span id="WMI.GLOSS_EVENT_CLASS"></span>**Event, classe**</span><span class="sxs-lookup"><span data-stu-id="f5e06-105"><span id="wmi.gloss_event_class"></span><span id="WMI.GLOSS_EVENT_CLASS"></span>**event class**</span></span>
</dt> <dd>

<span data-ttu-id="f5e06-106">Classe WMI à laquelle les *consommateurs d’événements* peuvent s’abonner par une requête d' *événement*.</span><span class="sxs-lookup"><span data-stu-id="f5e06-106">A WMI class that *event consumers* can subscribe to by an *event query*.</span></span> <span data-ttu-id="f5e06-107">La classe signale un type spécifique d’occurrence.</span><span class="sxs-lookup"><span data-stu-id="f5e06-107">The class reports a specific type of occurrence.</span></span> <span data-ttu-id="f5e06-108">Par exemple, la [**classe \_ ProcessStopTrace Win32**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) signale qu’un processus spécifique s’est arrêté.</span><span class="sxs-lookup"><span data-stu-id="f5e06-108">For example, the [**Win32\_ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) class reports that a specific process has stopped.</span></span>

</dd> <dt>

<span data-ttu-id="f5e06-109"><span id="wmi.gloss_event_consumer"></span><span id="WMI.GLOSS_EVENT_CONSUMER"></span>**consommateur d’événements**</span><span class="sxs-lookup"><span data-stu-id="f5e06-109"><span id="wmi.gloss_event_consumer"></span><span id="WMI.GLOSS_EVENT_CONSUMER"></span>**event consumer**</span></span>
</dt> <dd>

<span data-ttu-id="f5e06-110">Destinataire des notifications qui font état de l'occurrence d'un événement.</span><span class="sxs-lookup"><span data-stu-id="f5e06-110">A recipient of notifications that report an occurrence of an event.</span></span> <span data-ttu-id="f5e06-111">Un consommateur d’événements est [*temporaire*](gloss-t.md) ou [*permanent*](gloss-p.md).</span><span class="sxs-lookup"><span data-stu-id="f5e06-111">An event consumer is either [*temporary*](gloss-t.md) or [*permanent*](gloss-p.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5e06-112"><span id="wmi.gloss_event_consumer_provider"></span><span id="WMI.GLOSS_EVENT_CONSUMER_PROVIDER"></span>**fournisseur de consommateur d’événements**</span><span class="sxs-lookup"><span data-stu-id="f5e06-112"><span id="wmi.gloss_event_consumer_provider"></span><span id="WMI.GLOSS_EVENT_CONSUMER_PROVIDER"></span>**event consumer provider**</span></span>
</dt> <dd>

<span data-ttu-id="f5e06-113">Fournisseur qui détermine quel consommateur d'événements permanent gère un événement donné.</span><span class="sxs-lookup"><span data-stu-id="f5e06-113">A provider that determines which permanent event consumer handles a given event.</span></span> <span data-ttu-id="f5e06-114">Un fournisseur de consommateur d’événements est inscrit auprès de WMI par une instance de [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md), qui contient une liste des classes de [*consommateur logiques*](gloss-l.md) prises en charge par le fournisseur de consommateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="f5e06-114">An event consumer provider is registered with WMI by an instance of [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md), which contains a list of the [*logical consumer*](gloss-l.md) classes that the event consumer provider supports.</span></span> <span data-ttu-id="f5e06-115">Un fournisseur de consommateur d’événements est un serveur COM qui mappe des [*consommateurs physiques*](gloss-p.md) à des *consommateurs logiques*.</span><span class="sxs-lookup"><span data-stu-id="f5e06-115">An event consumer provider is a COM server that maps [*physical consumers*](gloss-p.md) to *logical consumers*.</span></span> <span data-ttu-id="f5e06-116">Un fournisseur de consommateur d’événements prend en charge l’interface [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) et est un composant de l’architecture du consommateur permanent.</span><span class="sxs-lookup"><span data-stu-id="f5e06-116">An event consumer provider supports the [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) interface and is a component of the permanent consumer architecture.</span></span>

</dd> <dt>

<span data-ttu-id="f5e06-117"><span id="wmi.gloss_event_filter"></span><span id="WMI.GLOSS_EVENT_FILTER"></span>**filtre d’événement**</span><span class="sxs-lookup"><span data-stu-id="f5e06-117"><span id="wmi.gloss_event_filter"></span><span id="WMI.GLOSS_EVENT_FILTER"></span>**event filter**</span></span>
</dt> <dd>

<span data-ttu-id="f5e06-118">Instance de la classe système [**\_ \_ EventFilter**](--eventfilter.md) qui décrit un type d’événement et les conditions pour la transmission d’une notification.</span><span class="sxs-lookup"><span data-stu-id="f5e06-118">An instance of the [**\_\_EventFilter**](--eventfilter.md) system class that describes an event type and the conditions for delivering a notification.</span></span> <span data-ttu-id="f5e06-119">Un consommateur utilise un filtre d’événement pour s’inscrire afin de recevoir une notification d’un type spécifique d’événement.</span><span class="sxs-lookup"><span data-stu-id="f5e06-119">A consumer uses an event filter to register to receive notification of a specific type of event.</span></span>

</dd> <dt>

<span data-ttu-id="f5e06-120"><span id="wmi.gloss_event_provider"></span><span id="WMI.GLOSS_EVENT_PROVIDER"></span>**fournisseur d’événements**</span><span class="sxs-lookup"><span data-stu-id="f5e06-120"><span id="wmi.gloss_event_provider"></span><span id="WMI.GLOSS_EVENT_PROVIDER"></span>**event provider**</span></span>
</dt> <dd>

<span data-ttu-id="f5e06-121">Fournisseur WMI qui surveille une source d’événements et notifie WMI lorsque des événements se produisent.</span><span class="sxs-lookup"><span data-stu-id="f5e06-121">A WMI provider that monitors a source of events and notifies WMI when events occur.</span></span> <span data-ttu-id="f5e06-122">Un fournisseur d’événements implémente les interfaces [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) et [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) , et parfois [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink).</span><span class="sxs-lookup"><span data-stu-id="f5e06-122">An event provider implements the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) interfaces, and sometimes [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink).</span></span>

</dd> <dt>

<span data-ttu-id="f5e06-123"><span id="wmi.gloss_event_query"></span><span id="WMI.GLOSS_EVENT_QUERY"></span>**requête d’événement**</span><span class="sxs-lookup"><span data-stu-id="f5e06-123"><span id="wmi.gloss_event_query"></span><span id="WMI.GLOSS_EVENT_QUERY"></span>**event query**</span></span>
</dt> <dd>

<span data-ttu-id="f5e06-124">Instruction [*langage de requêtes WMI (WQL)*](gloss-w.md) que les consommateurs d’événements utilisent pour s’inscrire afin de recevoir des notifications d’événements spécifiques.</span><span class="sxs-lookup"><span data-stu-id="f5e06-124">A [*WMI Query Language*](gloss-w.md) statement that event consumers use to register to receive notification of specific events.</span></span> <span data-ttu-id="f5e06-125">Un fournisseur d'événements utilise une requête d'événement pour s'inscrire afin de générer des notifications d'événements spécifiques.</span><span class="sxs-lookup"><span data-stu-id="f5e06-125">An event provider uses an event query to register to generate notifications of specific events.</span></span>

</dd> <dt>

<span data-ttu-id="f5e06-126"><span id="wmi.gloss_extension_schema"></span><span id="WMI.GLOSS_EXTENSION_SCHEMA"></span>**schéma d’extension**</span><span class="sxs-lookup"><span data-stu-id="f5e06-126"><span id="wmi.gloss_extension_schema"></span><span id="WMI.GLOSS_EXTENSION_SCHEMA"></span>**extension schema**</span></span>
</dt> <dd>

<span data-ttu-id="f5e06-127">Troisième couche du [*schéma CIM*](gloss-c.md), qui comprend des extensions spécifiques à la plateforme du schéma CIM, telles que Windows, UNIX et Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f5e06-127">The third layer of the [*CIM schema*](gloss-c.md), which includes platform-specific extensions of the CIM schema such as Windows, UNIX, and Exchange Server.</span></span> <span data-ttu-id="f5e06-128">Voir aussi modèle [*commun*](gloss-c.md) et modèle principal.</span><span class="sxs-lookup"><span data-stu-id="f5e06-128">Also see [*common model*](gloss-c.md) and core model.</span></span>

</dd> <dt>

<span data-ttu-id="f5e06-129"><span id="wmi.gloss_extrinsic_event"></span><span id="WMI.GLOSS_EXTRINSIC_EVENT"></span>**événement extrinsèque**</span><span class="sxs-lookup"><span data-stu-id="f5e06-129"><span id="wmi.gloss_extrinsic_event"></span><span id="WMI.GLOSS_EXTRINSIC_EVENT"></span>**extrinsic event**</span></span>
</dt> <dd>

<span data-ttu-id="f5e06-130">Notification d’événement d’un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f5e06-130">An event notification from a provider.</span></span> <span data-ttu-id="f5e06-131">La plupart des fournisseurs créent une instance d’une classe d’événements définie dans les fichiers MOF du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f5e06-131">Most providers create an instance of an event class defined in the provider MOF files.</span></span> <span data-ttu-id="f5e06-132">Un événement extrinsèque hérite de [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md).</span><span class="sxs-lookup"><span data-stu-id="f5e06-132">An extrinsic event inherits from [**\_\_ExtrinsicEvent**](--extrinsicevent.md).</span></span> <span data-ttu-id="f5e06-133">Par exemple, le [fournisseur du journal des événements](/previous-versions/windows/desktop/eventlogprov/event-log-provider) définit la classe d’événements [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span><span class="sxs-lookup"><span data-stu-id="f5e06-133">For example, the [Event Log Provider](/previous-versions/windows/desktop/eventlogprov/event-log-provider) defines the event class [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span></span> <span data-ttu-id="f5e06-134">Consultez également [*événement intrinsèque*](gloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="f5e06-134">Also see [*intrinsic event*](gloss-i.md).</span></span>

</dd> </dl>

 

 
