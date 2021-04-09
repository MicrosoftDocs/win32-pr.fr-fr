---
description: La classe NTEventLogEventConsumer écrit un message dans le journal des événements Windows lorsqu’un événement spécifié se produit. Cette classe est un consommateur d’événements standard fourni par WMI.
ms.assetid: ca998a91-d9f7-44ff-bb83-5ba92d68f31e
ms.tgt_platform: multiple
title: Journalisation dans le journal des événements NT en fonction d’un événement
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 69bf24c0d64c95a012b8681b88bde34dc28fa179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866873"
---
# <a name="logging-to-nt-event-log-based-on-an-event"></a><span data-ttu-id="06e16-104">Journalisation dans le journal des événements NT en fonction d’un événement</span><span class="sxs-lookup"><span data-stu-id="06e16-104">Logging to NT Event Log Based on an Event</span></span>

<span data-ttu-id="06e16-105">La classe [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) écrit un message dans le journal des événements Windows lorsqu’un événement spécifié se produit.</span><span class="sxs-lookup"><span data-stu-id="06e16-105">The [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) class writes a message to the Windows Event log when a specified event occurs.</span></span> <span data-ttu-id="06e16-106">Cette classe est un consommateur d’événements standard fourni par WMI.</span><span class="sxs-lookup"><span data-stu-id="06e16-106">This class is a standard event consumer that WMI provides.</span></span>

> [!Note]  
> <span data-ttu-id="06e16-107">Les utilisateurs authentifiés ne peuvent pas, par défaut, consigner les événements dans le journal des applications sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="06e16-107">Authenticated users cannot, by default, log events to the Application log on a remote computer.</span></span> <span data-ttu-id="06e16-108">Par conséquent, l’exemple décrit dans cette rubrique échouera si vous utilisez la propriété **UNCServerName** de la classe [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) et que vous spécifiez un ordinateur distant comme valeur.</span><span class="sxs-lookup"><span data-stu-id="06e16-108">As a result, the example described in this topic will fail if you use the **UNCServerName** property of the [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) class and specify a remote computer as its value.</span></span> <span data-ttu-id="06e16-109">Pour savoir comment modifier la sécurité du journal des événements, consultez cet article de la [base de connaissances](https://support.microsoft.com/kb/323076).</span><span class="sxs-lookup"><span data-stu-id="06e16-109">To learn how to change event log security, consult this [KB article](https://support.microsoft.com/kb/323076).</span></span>

 

<span data-ttu-id="06e16-110">La procédure de base pour l’utilisation d’un consommateur standard est décrite dans [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="06e16-110">The basic procedure for using a standard consumer is described in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="06e16-111">Vous trouverez ci-dessous des étapes supplémentaires au-delà de la procédure de base, requises lors de l’utilisation de la classe [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="06e16-111">The following are additional steps beyond the basic procedure, required when using the [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) class.</span></span> <span data-ttu-id="06e16-112">Les étapes décrivent comment créer un consommateur d’événements qui écrit dans le journal des événements de l’application.</span><span class="sxs-lookup"><span data-stu-id="06e16-112">The steps describe how to create an event consumer that writes to the Application event log.</span></span>

<span data-ttu-id="06e16-113">La procédure suivante décrit comment créer un consommateur d’événements qui écrit dans le journal des événements NT.</span><span class="sxs-lookup"><span data-stu-id="06e16-113">The following procedure describes how to create an event consumer that writes to the NT Event Log.</span></span>

<span data-ttu-id="06e16-114">**Pour créer un consommateur d’événements qui écrit dans le journal des événements Windows**</span><span class="sxs-lookup"><span data-stu-id="06e16-114">**To create an event consumer that writes to the Windows Event Log**</span></span>

1.  <span data-ttu-id="06e16-115">Dans un fichier format MOF (MOF), créez une instance de [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) pour recevoir les événements que vous demandez dans la requête.</span><span class="sxs-lookup"><span data-stu-id="06e16-115">In a Managed Object Format (MOF) file, create an instance of [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) to receive the events you request in the query.</span></span> <span data-ttu-id="06e16-116">Pour plus d’informations sur l’écriture de code MOF, consultez [conception de Classes format MOF (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="06e16-116">For more information about writing MOF code, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>
2.  <span data-ttu-id="06e16-117">Créez et nommez une instance de [**\_ \_ EventFilter**](--eventfilter.md), puis créez une requête pour spécifier le type d’événement qui déclenche l’écriture dans le journal des événements NT.</span><span class="sxs-lookup"><span data-stu-id="06e16-117">Create, and name, an instance of [**\_\_EventFilter**](--eventfilter.md), and then create a query to specify the type of event which triggers writing to the NT Event Log.</span></span>

    <span data-ttu-id="06e16-118">Pour plus d’informations, consultez [interrogation avec WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="06e16-118">For more information see, [Querying with WQL](querying-with-wql.md).</span></span>

3.  <span data-ttu-id="06e16-119">Créez une instance de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) pour associer le filtre à l’instance de [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="06e16-119">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span></span>
4.  <span data-ttu-id="06e16-120">Compilez le fichier MOF à l’aide de [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="06e16-120">Compile the MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>

## <a name="example"></a><span data-ttu-id="06e16-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="06e16-121">Example</span></span>

<span data-ttu-id="06e16-122">L’exemple de cette section se trouve dans le code MOF, mais vous pouvez créer des instances par programme à l’aide [de l’API de script pour WMI](scripting-api-for-wmi.md) ou [de l’API com pour WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="06e16-122">The example in this section is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="06e16-123">L’exemple montre comment créer un consommateur pour écrire dans le journal des événements de l’application à l’aide de [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="06e16-123">The example shows how to create a consumer to write to the Application event log by using [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span></span> <span data-ttu-id="06e16-124">Le MOF crée une nouvelle classe nommée « NTLogCons \_ example », un filtre d’événements pour interroger les opérations, telles que la création, sur une instance de cette nouvelle classe et une liaison entre le filtre et le consommateur.</span><span class="sxs-lookup"><span data-stu-id="06e16-124">The MOF creates a new class named "NTLogCons\_Example", an event filter to query for operations, such as creation, on an instance of this new class, and a binding between filter and consumer.</span></span> <span data-ttu-id="06e16-125">Étant donné que la dernière action du MOF consiste à créer une instance de NTLogCons \_ exemple, vous pouvez immédiatement voir l’événement dans le journal des événements d’application en exécutant Eventvwr.exe.</span><span class="sxs-lookup"><span data-stu-id="06e16-125">Because the last action in the MOF is to create an instance of NTLogCons\_Example, you can immediately see the event in the Application event log by running Eventvwr.exe.</span></span>

<span data-ttu-id="06e16-126">Le `EventID=0x0A for SourceName="WinMgmt"` identifie un message avec le texte suivant.</span><span class="sxs-lookup"><span data-stu-id="06e16-126">The `EventID=0x0A for SourceName="WinMgmt"` identifies a message with the following text.</span></span> <span data-ttu-id="06e16-127">« %1 », « %2 », « %3 » sont des espaces réservés pour les chaînes correspondantes spécifiées dans le tableau InsertionStringTemplates.</span><span class="sxs-lookup"><span data-stu-id="06e16-127">The "%1", "%2", "%3" are placeholders for corresponding strings specified in InsertionStringTemplates array.</span></span>

``` syntax
Event filter with query "%2" could not be [re]activated in 
namespace "%1" because of error %3. Events may not be delivered 
through this filter until the problem is corrected.
```

<span data-ttu-id="06e16-128">La procédure suivante décrit comment utiliser l’exemple.</span><span class="sxs-lookup"><span data-stu-id="06e16-128">The following procedure describes how to use the example.</span></span>

<span data-ttu-id="06e16-129">**Pour utiliser l’exemple**</span><span class="sxs-lookup"><span data-stu-id="06e16-129">**To use the example**</span></span>

1.  <span data-ttu-id="06e16-130">Copiez le Listing MOF ci-dessous dans un fichier texte et enregistrez-le avec une extension. mof.</span><span class="sxs-lookup"><span data-stu-id="06e16-130">Copy the MOF listing below into a text file and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="06e16-131">Dans un Fenêtre Commande, compilez le fichier MOF à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="06e16-131">In a Command window, compile the MOF file by using the following command:</span></span>

    <span data-ttu-id="06e16-132">Fichier **mofcomp** \*\* \* *. mof*\*</span><span class="sxs-lookup"><span data-stu-id="06e16-132">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

3.  <span data-ttu-id="06e16-133">Exécutez Eventvwr.exe.</span><span class="sxs-lookup"><span data-stu-id="06e16-133">Run Eventvwr.exe.</span></span> <span data-ttu-id="06e16-134">Examinez le journal des événements de l’application.</span><span class="sxs-lookup"><span data-stu-id="06e16-134">Look at the Application event log.</span></span> <span data-ttu-id="06e16-135">Vous devez voir un événement avec ID = 10 (l' **eventID**), source = « WMI » et type = Error.</span><span class="sxs-lookup"><span data-stu-id="06e16-135">You should see an event with ID = 10 (the **EventID**), Source = "WMI", and Type = Error.</span></span>
4.  <span data-ttu-id="06e16-136">Double-cliquez sur le message de **type informations** de WMI avec 10 dans la colonne **événement** .</span><span class="sxs-lookup"><span data-stu-id="06e16-136">Double-click the **Information type** message from WMI with 10 in the **Event** column.</span></span> <span data-ttu-id="06e16-137">La description suivante s’affichera pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="06e16-137">The following description will be displayed for the event.</span></span>

    ``` syntax
    Event filter with query "STRING2" could not be [re]activated in 
    namespace "STRING1" because of error STRING3. Events cannot be 
    delivered through this filter until the problem is corrected.
    ```

``` syntax
// Set the namespace as root\subscription.
// The NTEventLogEventConsumer is already
// compiled in the root\subscription namespace. 

#pragma namespace ("\\\\.\\Root\\subscription")
class NTLogCons_Example
{
 [key] string name;
 string InsertionString;
};

// Create an instance of the NT Event log consumer
// and give it the alias $CONSUMER

instance of NTEventLogEventConsumer as $CONSUMER
{
    // Unique instance name
    Name = "NTConsumerTest"; 
    // System component that generates the event
    SourceName = "WinMgmt";
    // Event message WBEM_MC_CANNOT_ACTIVATE_FILTER
    EventID = 0xC000000A;
    // EVENTLOG_ERROR_TYPE
    EventType = 1;
    // WMI event messages do not have multiple categories
    Category = 0;
    // Number of strings in InsertionStringTemplates property
    NumberOfInsertionStrings = 3;

    InsertionStringTemplates =
       {"%TargetInstance.Name%",
        "%TargetInstance.InsertionString%",
        "STRING3"};
};

// Create an instance of the event filter
// and give it the alias $FILTER
// The filter queries for any instance operation event
// for instances of the NTLogCons_Example class

instance of __EventFilter as $FILTER
{
    // Unique instance name
    Name = "NTLogConsFilter";
    Query = "SELECT * from __InstanceOperationEvent"
            " WHERE TargetInstance ISA \"NTLogCons_Example\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding
// between filter and consumer instances.

instance of __FilterToConsumerBinding
{
    Consumer = $CONSUMER;
    Filter = $FILTER;
};

// Create an instance of this class right now. 

instance of NTLogCons_Example
{
   Name = "STRING1";
   InsertionString = "STRING2";
};
```

## <a name="related-topics"></a><span data-ttu-id="06e16-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="06e16-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06e16-139">Surveillance et réponse aux événements avec des consommateurs standard</span><span class="sxs-lookup"><span data-stu-id="06e16-139">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



