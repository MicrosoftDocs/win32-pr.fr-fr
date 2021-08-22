---
description: la classe NTEventLogEventConsumer écrit un message dans le journal des événements Windows lorsqu’un événement spécifié se produit. Cette classe est un consommateur d’événements standard fourni par WMI.
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
ms.openlocfilehash: c8c070b1a52fe41f32b8610ff0931d33be7feb33f9f5cd6f6067652e963f6824
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050707"
---
# <a name="logging-to-nt-event-log-based-on-an-event"></a>Journalisation dans le journal des événements NT en fonction d’un événement

la classe [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) écrit un message dans le journal des événements Windows lorsqu’un événement spécifié se produit. Cette classe est un consommateur d’événements standard fourni par WMI.

> [!Note]  
> Les utilisateurs authentifiés ne peuvent pas, par défaut, consigner les événements dans le journal des applications sur un ordinateur distant. Par conséquent, l’exemple décrit dans cette rubrique échouera si vous utilisez la propriété **UNCServerName** de la classe [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) et que vous spécifiez un ordinateur distant comme valeur. Pour savoir comment modifier la sécurité du journal des événements, consultez cet article de la [base de connaissances](https://support.microsoft.com/kb/323076).

 

La procédure de base pour l’utilisation d’un consommateur standard est décrite dans [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md). Vous trouverez ci-dessous des étapes supplémentaires au-delà de la procédure de base, requises lors de l’utilisation de la classe [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) . Les étapes décrivent comment créer un consommateur d’événements qui écrit dans le journal des événements de l’application.

La procédure suivante décrit comment créer un consommateur d’événements qui écrit dans le journal des événements NT.

**pour créer un consommateur d’événements qui écrit dans le journal des événements Windows**

1.  Dans un fichier format MOF (MOF), créez une instance de [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) pour recevoir les événements que vous demandez dans la requête. Pour plus d’informations sur l’écriture de code MOF, consultez [conception de Classes format MOF (MOF)](designing-managed-object-format--mof--classes.md).
2.  Créez et nommez une instance de [**\_ \_ EventFilter**](--eventfilter.md), puis créez une requête pour spécifier le type d’événement qui déclenche l’écriture dans le journal des événements NT.

    Pour plus d’informations, consultez [interrogation avec WQL](querying-with-wql.md).

3.  Créez une instance de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) pour associer le filtre à l’instance de [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).
4.  Compilez le fichier MOF à l’aide de [**Mofcomp.exe**](mofcomp.md).

## <a name="example"></a>Exemples

L’exemple de cette section se trouve dans le code MOF, mais vous pouvez créer des instances par programme à l’aide [de l’API de script pour WMI](scripting-api-for-wmi.md) ou [de l’API com pour WMI](com-api-for-wmi.md). L’exemple montre comment créer un consommateur pour écrire dans le journal des événements de l’application à l’aide de [**NTEventLogEventConsumer**](nteventlogeventconsumer.md). Le MOF crée une nouvelle classe nommée « NTLogCons \_ example », un filtre d’événements pour interroger les opérations, telles que la création, sur une instance de cette nouvelle classe et une liaison entre le filtre et le consommateur. Étant donné que la dernière action du MOF consiste à créer une instance de NTLogCons \_ exemple, vous pouvez immédiatement voir l’événement dans le journal des événements d’application en exécutant Eventvwr.exe.

Le `EventID=0x0A for SourceName="WinMgmt"` identifie un message avec le texte suivant. « %1 », « %2 », « %3 » sont des espaces réservés pour les chaînes correspondantes spécifiées dans le tableau InsertionStringTemplates.

``` syntax
Event filter with query "%2" could not be [re]activated in 
namespace "%1" because of error %3. Events may not be delivered 
through this filter until the problem is corrected.
```

La procédure suivante décrit comment utiliser l’exemple.

**Pour utiliser l’exemple**

1.  Copiez le Listing MOF ci-dessous dans un fichier texte et enregistrez-le avec une extension. mof.
2.  Dans un Fenêtre Commande, compilez le fichier MOF à l’aide de la commande suivante :

    Fichier **mofcomp** ** * *. mof**

3.  Exécutez Eventvwr.exe. Examinez le journal des événements de l’application. Vous devez voir un événement avec ID = 10 (l' **eventID**), source = « WMI » et type = Error.
4.  Double-cliquez sur le message de **type informations** de WMI avec 10 dans la colonne **événement** . La description suivante s’affichera pour l’événement.

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

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



