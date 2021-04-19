---
description: Un filtre d’événements est une classe WMI qui décrit les événements que WMI remet à un consommateur physique.
ms.assetid: c0ce26a4-5ff2-44b4-8550-c7d8ad0ba0f0
ms.tgt_platform: multiple
title: Création d’un filtre d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 693e4ef2eee5de14550b8efbf25a9b6720d6a8b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535684"
---
# <a name="creating-an-event-filter"></a><span data-ttu-id="d883f-103">Création d’un filtre d’événements</span><span class="sxs-lookup"><span data-stu-id="d883f-103">Creating an Event Filter</span></span>

<span data-ttu-id="d883f-104">Un filtre d’événements est une classe WMI qui décrit les événements que WMI remet à un consommateur physique.</span><span class="sxs-lookup"><span data-stu-id="d883f-104">An event filter is a WMI class that describes which events WMI delivers to a physical consumer.</span></span> <span data-ttu-id="d883f-105">Par exemple, un filtre d’événements peut indiquer à WMI de remettre à un consommateur tous les événements de gestion de l’alimentation, ou tous les événements de redémarrage du système.</span><span class="sxs-lookup"><span data-stu-id="d883f-105">For example, an event filter can instruct WMI to deliver to a consumer all power management events, or all system reboot events.</span></span> <span data-ttu-id="d883f-106">Un filtre d’événements décrit également les conditions dans lesquelles WMI remet les événements.</span><span class="sxs-lookup"><span data-stu-id="d883f-106">An event filter also describes the conditions under which WMI delivers the events.</span></span> <span data-ttu-id="d883f-107">Un filtre d’événements peut spécifier un événement intrinsèque ou extrinsèque ; et le filtre peut faire référence aux événements qui proviennent de l’espace de noms, autrement dit, à l’exception de l’espace de noms du filtre.</span><span class="sxs-lookup"><span data-stu-id="d883f-107">An event filter can specify an intrinsic or extrinsic event; and the filter can refer to events that originate in the namespace—that is, other than the namespace of the filter.</span></span> <span data-ttu-id="d883f-108">Le consommateur permanent doit avoir le même [**CreatorSID**](--eventconsumer.md) dans les instances de consommateur, de filtre et de liaison.</span><span class="sxs-lookup"><span data-stu-id="d883f-108">The permanent consumer must have the same [**CreatorSID**](--eventconsumer.md) in the consumer, filter, and binding instances.</span></span> <span data-ttu-id="d883f-109">Pour plus d’informations, consultez [réception d’événements en toute sécurité](receiving-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="d883f-109">For more information, see [Receiving Events Securely](receiving-events-securely.md).</span></span>

<span data-ttu-id="d883f-110">La procédure suivante décrit comment créer un filtre d’événements.</span><span class="sxs-lookup"><span data-stu-id="d883f-110">The following procedure describes how to create an event filter.</span></span>

<span data-ttu-id="d883f-111">**Pour créer un filtre d’événements**</span><span class="sxs-lookup"><span data-stu-id="d883f-111">**To create an event filter**</span></span>

1.  <span data-ttu-id="d883f-112">Créez une instance de la classe système [**\_ \_ EventFilter**](--eventfilter.md) WMI.</span><span class="sxs-lookup"><span data-stu-id="d883f-112">Create an instance of the WMI [**\_\_EventFilter**](--eventfilter.md) system class.</span></span>
2.  <span data-ttu-id="d883f-113">Créez un identificateur unique pour votre filtre avec la propriété **Name** , de l’une des deux manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="d883f-113">Create a unique identifier for your filter with the **Name** property, in one of two ways:</span></span>

    -   <span data-ttu-id="d883f-114">Utilisez un schéma privé.</span><span class="sxs-lookup"><span data-stu-id="d883f-114">Use a private scheme.</span></span>

        <span data-ttu-id="d883f-115">Le fait de nommer arbitrairement vos filtres d’événements fonctionne tant que vous n’êtes pas en conflit avec d’autres modèles de noms de filtre.</span><span class="sxs-lookup"><span data-stu-id="d883f-115">Arbitrarily naming your event filters works as long as you do not conflict with other filter naming schemes.</span></span> <span data-ttu-id="d883f-116">Vous devez éviter les conflits de noms, car l’ajout d’une instance avec une valeur de **nom** en double remplace l’ancienne instance.</span><span class="sxs-lookup"><span data-stu-id="d883f-116">You must avoid naming conflicts because adding an instance with a duplicate **Name** value overwrites the old instance.</span></span>

    -   <span data-ttu-id="d883f-117">Utilisez un identificateur global unique (GUID).</span><span class="sxs-lookup"><span data-stu-id="d883f-117">Use a globally unique identifier (GUID).</span></span>

        <span data-ttu-id="d883f-118">Si vous laissez le **nom** vide, WMI remplit le **nom** avec un GUID.</span><span class="sxs-lookup"><span data-stu-id="d883f-118">If you leave **Name** empty, WMI fills **Name** with a GUID.</span></span>

3.  <span data-ttu-id="d883f-119">Décrivez le type d’événement que vous souhaitez filtrer à l’aide de la propriété de **requête** .</span><span class="sxs-lookup"><span data-stu-id="d883f-119">Describe the type of event you want filtered with the **Query** property.</span></span>

    <span data-ttu-id="d883f-120">La propriété de **requête** contient la requête langage de requêtes WMI (WQL) (WQL) qui décrit le type d’événement que vous souhaitez filtrer.</span><span class="sxs-lookup"><span data-stu-id="d883f-120">The **Query** property contains the WMI Query Language (WQL) query that describes the type of event you want filtered.</span></span> <span data-ttu-id="d883f-121">Vous pouvez obtenir un filtrage précis à l’aide d’un ensemble d’opérateurs et d’extensions pour WQL.</span><span class="sxs-lookup"><span data-stu-id="d883f-121">You can achieve precise filtering using a variety of operators and extensions to WQL.</span></span>

    <span data-ttu-id="d883f-122">Un événement de journal NT est généré lorsqu’une requête d’un consommateur d’événements permanent échoue.</span><span class="sxs-lookup"><span data-stu-id="d883f-122">An NT Log event is generated when a query from a permanent event consumer fails.</span></span> <span data-ttu-id="d883f-123">La source de l’événement est WinMgmt, l’ID d’événement est 10 et le type d’événement est Error.</span><span class="sxs-lookup"><span data-stu-id="d883f-123">The event's source is WinMgmt, the event ID is 10, and the event type is Error.</span></span>

    <span data-ttu-id="d883f-124">WMI est plus efficace pour traiter des requêtes spécifiques et restrictives que les requêtes larges.</span><span class="sxs-lookup"><span data-stu-id="d883f-124">WMI is more efficient at processing restrictive, specific queries than broad queries.</span></span> <span data-ttu-id="d883f-125">En créant une requête spécifique, vous pouvez éviter la communication entre processus et le trafic réseau inutiles.</span><span class="sxs-lookup"><span data-stu-id="d883f-125">By creating a specific query, you can avoid unnecessary inter-process communication and network traffic.</span></span> <span data-ttu-id="d883f-126">Dans les cas d’événements générés par un fournisseur, WMI effectue le filtrage en cours au fournisseur ; Cela garantit que seuls les événements correspondant au filtre entraînent le coût de communication entre processus.</span><span class="sxs-lookup"><span data-stu-id="d883f-126">In cases of events generated by a provider, WMI performs the filtering in process to the provider; this ensures that only events matching the filter incur the interprocess communication cost.</span></span> <span data-ttu-id="d883f-127">Pour plus d’informations, consultez [interrogation de WMI](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="d883f-127">For more information, see [Querying WMI](querying-wmi.md).</span></span>

4.  <span data-ttu-id="d883f-128">Définissez la propriété **QueryLanguage** sur le type de langage de requête que vous utilisez dans la propriété de **requête** .</span><span class="sxs-lookup"><span data-stu-id="d883f-128">Set the **QueryLanguage** property to the type of query language you use in the **Query** property.</span></span>

    <span data-ttu-id="d883f-129">Vous allez presque toujours définir **QueryLanguage** sur « WQL ».</span><span class="sxs-lookup"><span data-stu-id="d883f-129">You will almost always set **QueryLanguage** to "WQL".</span></span>

<span data-ttu-id="d883f-130">L’exemple de code suivant décrit un filtre d’événement qui signale un événement chaque fois que WMI crée une instance de la classe [**\_ \_ TimerEvent**](--timerevent.md) dans l' \\ espace de noms CIMV2 racine.</span><span class="sxs-lookup"><span data-stu-id="d883f-130">The following code example describes an event filter that signals an event each time WMI creates an instance of the [**\_\_TimerEvent**](--timerevent.md) class in the root\\cimv2 namespace.</span></span>

``` syntax
instance of __EventFilter as $FILTER
{
    Name = "MyFilterName";
    Query = "select * from __TimerEvent where TimerID=\"MyTimer\"";
    QueryLanguage = "WQL";
    EventNamespace = "\root\cimv2";

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

<span data-ttu-id="d883f-131">La propriété **EventNamespace** spécifie l’espace de noms à partir duquel les événements proviennent.</span><span class="sxs-lookup"><span data-stu-id="d883f-131">The **EventNamespace** property specifies the namespace from which the events originate.</span></span> <span data-ttu-id="d883f-132">Vous n’avez pas besoin de créer une instance des filtres dans l’espace de noms où proviennent les événements.</span><span class="sxs-lookup"><span data-stu-id="d883f-132">You do not have to create an instance of the filters in the namespace where the events originate.</span></span> <span data-ttu-id="d883f-133">Si vous ne spécifiez pas l’espace de noms, WMI crée le filtre dans l’espace de noms par défaut.</span><span class="sxs-lookup"><span data-stu-id="d883f-133">If you do not specify the namespace, then WMI creates the filter in the default namespace.</span></span> <span data-ttu-id="d883f-134">Les classes d’événements intrinsèques, telles que [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md) , sont disponibles dans chaque espace de noms.</span><span class="sxs-lookup"><span data-stu-id="d883f-134">The intrinsic events classes, such as [**\_\_InstanceOperationEvent**](--instanceoperationevent.md) are available in every namespace.</span></span>

<span data-ttu-id="d883f-135">Pour inscrire votre consommateur logique pour les notifications d’événements, vous devez lier les filtres d’événements à un consommateur logique.</span><span class="sxs-lookup"><span data-stu-id="d883f-135">To register your logical consumer for event notifications, you must bind the event filters to a logical consumer.</span></span> <span data-ttu-id="d883f-136">Pour plus d’informations, consultez [liaison d’un filtre d’événements à un consommateur logique](binding-an-event-filter-with-a-logical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="d883f-136">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md).</span></span>

 

 



