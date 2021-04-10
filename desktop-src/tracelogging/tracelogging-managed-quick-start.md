---
title: Démarrage rapide managé TraceLogging
description: La section suivante décrit les étapes de base requises pour ajouter TraceLogging à du code managé.
ms.assetid: E144214D-8DCC-4263-8232-9F468C1A3CC0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7108dfc094f3183950dd94e5398263f4bf7cfd5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309829"
---
# <a name="tracelogging-managed-quick-start"></a><span data-ttu-id="e2f50-103">Démarrage rapide managé TraceLogging</span><span class="sxs-lookup"><span data-stu-id="e2f50-103">TraceLogging Managed Quick Start</span></span>

<span data-ttu-id="e2f50-104">La section suivante décrit les étapes de base requises pour ajouter TraceLogging à du code managé.</span><span class="sxs-lookup"><span data-stu-id="e2f50-104">The following section describes the basic steps required to add TraceLogging to managed code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e2f50-105">Prérequis</span><span class="sxs-lookup"><span data-stu-id="e2f50-105">Prerequisites</span></span>

-   <span data-ttu-id="e2f50-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="e2f50-106">Windows 10</span></span>

### <a name="simpletraceloggingexamplecs"></a><span data-ttu-id="e2f50-107">SimpleTraceLoggingExample. cs</span><span class="sxs-lookup"><span data-stu-id="e2f50-107">SimpleTraceLoggingExample.cs</span></span>

<span data-ttu-id="e2f50-108">Cet exemple montre comment enregistrer des événements Tracelogging sans avoir besoin de créer manuellement un fichier XML de manifeste d’instrumentation distinct.</span><span class="sxs-lookup"><span data-stu-id="e2f50-108">This example demonstrates how to log Tracelogging events without the need to manually create a separate instrumentation manifest XML file.</span></span>


```CSharp
using System;
using System.Diagnostics.Tracing;

namespace SimpleTraceLoggingExample
{
    class Program
    {
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider");
        static void Main(string[] args)
        {
            log.Write("Event 1"); // write an event with no fields
            log.Write("Event 2", new { someEventData = DateTime.Now }); // Sending an anonymous type as event data

            ExampleStructuredData EventData = new ExampleStructuredData() { TransactionID = 1234, TransactionDate = DateTime.Now };
            log.Write("Event 3", EventData); // Sending a class decorated with [EventData] as event data
        }
    }

    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public sealed class ExampleStructuredData
    {
        public int TransactionID { get; set; }
        public DateTime TransactionDate { get; set; }
    }
}
```



### <a name="create-the-eventsource"></a><span data-ttu-id="e2f50-109">Créer le EventSource</span><span class="sxs-lookup"><span data-stu-id="e2f50-109">Create the EventSource</span></span>

<span data-ttu-id="e2f50-110">Avant de pouvoir enregistrer des événements, vous devez créer une instance de la classe EventSource.</span><span class="sxs-lookup"><span data-stu-id="e2f50-110">Before you can log events you must create an instance of the EventSource class.</span></span> <span data-ttu-id="e2f50-111">Le premier paramètre de constructeur identifie le nom de ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e2f50-111">The first constructor parameter identifies the name of this provider.</span></span> <span data-ttu-id="e2f50-112">Le fournisseur est automatiquement inscrit pour vous, comme illustré dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="e2f50-112">The provider is automatically registered for you as illustrated in the example.</span></span>


```CSharp
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider");
```



<span data-ttu-id="e2f50-113">L’instance est statique, car il ne doit y avoir qu’une seule instance d’un fournisseur spécifique dans votre application à la fois.</span><span class="sxs-lookup"><span data-stu-id="e2f50-113">The instance is static because there should only be one instance of a specific provider in your application at a time.</span></span>

### <a name="log-tracelogging-events"></a><span data-ttu-id="e2f50-114">Journaliser les événements Tracelogging</span><span class="sxs-lookup"><span data-stu-id="e2f50-114">Log Tracelogging events</span></span>

<span data-ttu-id="e2f50-115">Une fois le fournisseur créé, le code suivant de l’exemple ci-dessus enregistre un événement simple.</span><span class="sxs-lookup"><span data-stu-id="e2f50-115">After the provider is created, the following code from the example above logs a simple event.</span></span>


```CSharp
            log.Write("Event 1"); // write an event with no fields
```



### <a name="log-structured-event-payload-data"></a><span data-ttu-id="e2f50-116">Journaliser les données de charge utile d’événement structuré</span><span class="sxs-lookup"><span data-stu-id="e2f50-116">Log structured event payload data</span></span>

<span data-ttu-id="e2f50-117">Vous pouvez définir des données de charge utile structurées journalisées avec l’événement.</span><span class="sxs-lookup"><span data-stu-id="e2f50-117">You can define structured payload data that is logged with the event.</span></span> <span data-ttu-id="e2f50-118">Fournissez des données de charge utile structurées en tant que type anonyme ou en tant qu’instance d’une classe qui a été annotée avec l' `[EventData]` attribut, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="e2f50-118">Provide structured payload data either as an anonymous type or as an instance of a class that has been annotated with the `[EventData]` attribute as shown in the following example.</span></span>


```CSharp
            log.Write("Event 2", new { someEventData = DateTime.Now }); // Sending an anonymous type as event data

            ExampleStructuredData EventData = new ExampleStructuredData() { TransactionID = 1234, TransactionDate = DateTime.Now };
            log.Write("Event 3", EventData); // Sending a class decorated with [EventData] as event data
```



<span data-ttu-id="e2f50-119">Vous devez ajouter l' `[EventData]` attribut aux classes de charge utile d’événement que vous définissez comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="e2f50-119">You must add the `[EventData]` attribute to event payload classes that you define as shown below.</span></span>


```CSharp
    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public sealed class ExampleStructuredData
    {
        public int TransactionID { get; set; }
        public DateTime TransactionDate { get; set; }
    }
```



<span data-ttu-id="e2f50-120">L’attribut remplace la nécessité de créer manuellement un fichier manifeste pour décrire les données d’événement.</span><span class="sxs-lookup"><span data-stu-id="e2f50-120">The attribute replaces the need to manually create a manifest file to describe the event data.</span></span> <span data-ttu-id="e2f50-121">Maintenant, il vous suffit de passer une instance de la classe à la méthode EventSource. Write () pour consigner l’événement et les données de charge utile correspondantes.</span><span class="sxs-lookup"><span data-stu-id="e2f50-121">Now all you have to do is pass an instance of the class to the EventSource.Write() method to log the event and corresponding payload data.</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="e2f50-122">Résumé et étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="e2f50-122">Summary and next steps</span></span>

<span data-ttu-id="e2f50-123">Consultez [enregistrement et affichage des événements TraceLogging](tracelogging-record-and-display-tracelogging-events.md) pour plus d’informations sur la capture et l’affichage des données TraceLogging à l’aide des dernières versions internes des outils de performances Windows (WPT).</span><span class="sxs-lookup"><span data-stu-id="e2f50-123">See [Record and Display TraceLogging Events](tracelogging-record-and-display-tracelogging-events.md) for information about how to capture and view TraceLogging data using the latest internal versions of the Windows Performance Tools (WPT).</span></span>

<span data-ttu-id="e2f50-124">Pour obtenir des exemples de TraceLogging managés, consultez [exemples .net Tracelogging](tracelogging-net-examples.md) .</span><span class="sxs-lookup"><span data-stu-id="e2f50-124">See [.NET Tracelogging Examples](tracelogging-net-examples.md) for more managed TraceLogging examples.</span></span>

 

 




