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
# <a name="tracelogging-managed-quick-start"></a>Démarrage rapide managé TraceLogging

La section suivante décrit les étapes de base requises pour ajouter TraceLogging à du code managé.

## <a name="prerequisites"></a>Prérequis

-   Windows 10

### <a name="simpletraceloggingexamplecs"></a>SimpleTraceLoggingExample. cs

Cet exemple montre comment enregistrer des événements Tracelogging sans avoir besoin de créer manuellement un fichier XML de manifeste d’instrumentation distinct.


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



### <a name="create-the-eventsource"></a>Créer le EventSource

Avant de pouvoir enregistrer des événements, vous devez créer une instance de la classe EventSource. Le premier paramètre de constructeur identifie le nom de ce fournisseur. Le fournisseur est automatiquement inscrit pour vous, comme illustré dans l’exemple.


```CSharp
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider");
```



L’instance est statique, car il ne doit y avoir qu’une seule instance d’un fournisseur spécifique dans votre application à la fois.

### <a name="log-tracelogging-events"></a>Journaliser les événements Tracelogging

Une fois le fournisseur créé, le code suivant de l’exemple ci-dessus enregistre un événement simple.


```CSharp
            log.Write("Event 1"); // write an event with no fields
```



### <a name="log-structured-event-payload-data"></a>Journaliser les données de charge utile d’événement structuré

Vous pouvez définir des données de charge utile structurées journalisées avec l’événement. Fournissez des données de charge utile structurées en tant que type anonyme ou en tant qu’instance d’une classe qui a été annotée avec l' `[EventData]` attribut, comme indiqué dans l’exemple suivant.


```CSharp
            log.Write("Event 2", new { someEventData = DateTime.Now }); // Sending an anonymous type as event data

            ExampleStructuredData EventData = new ExampleStructuredData() { TransactionID = 1234, TransactionDate = DateTime.Now };
            log.Write("Event 3", EventData); // Sending a class decorated with [EventData] as event data
```



Vous devez ajouter l' `[EventData]` attribut aux classes de charge utile d’événement que vous définissez comme indiqué ci-dessous.


```CSharp
    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public sealed class ExampleStructuredData
    {
        public int TransactionID { get; set; }
        public DateTime TransactionDate { get; set; }
    }
```



L’attribut remplace la nécessité de créer manuellement un fichier manifeste pour décrire les données d’événement. Maintenant, il vous suffit de passer une instance de la classe à la méthode EventSource. Write () pour consigner l’événement et les données de charge utile correspondantes.

## <a name="summary-and-next-steps"></a>Résumé et étapes suivantes

Consultez [enregistrement et affichage des événements TraceLogging](tracelogging-record-and-display-tracelogging-events.md) pour plus d’informations sur la capture et l’affichage des données TraceLogging à l’aide des dernières versions internes des outils de performances Windows (WPT).

Pour obtenir des exemples de TraceLogging managés, consultez [exemples .net Tracelogging](tracelogging-net-examples.md) .

 

 




