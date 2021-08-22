---
description: La classe LogFileEventConsumer peut écrire du texte prédéfini dans un fichier journal lorsqu’un événement spécifié se produit. Cette classe est un consommateur d’événements standard fourni par WMI.
ms.assetid: c337e9f7-f40c-4d7d-a180-c053e24c882b
ms.tgt_platform: multiple
title: Écriture dans un fichier journal basé sur un événement
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 881435986a1097c2ba97160693ed15e28bae3d86019fb703adf6bf1e8b07f8a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049727"
---
# <a name="writing-to-a-log-file-based-on-an-event"></a>Écriture dans un fichier journal basé sur un événement

La classe [**LogFileEventConsumer**](logfileeventconsumer.md) peut écrire du texte prédéfini dans un fichier journal lorsqu’un événement spécifié se produit. Cette classe est un consommateur d’événements standard fourni par WMI.

La procédure de base pour l’utilisation de consommateurs standard est toujours la même, et se trouve dans la [surveillance et la réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).

La procédure suivante ajoute à la procédure de base, est spécifique à la classe [**LogFileEventConsumer**](logfileeventconsumer.md) et décrit comment créer un consommateur d’événements qui exécute un programme.

**Pour créer un consommateur d’événements qui écrit dans un fichier journal**

1.  Dans le fichier format MOF (MOF), créez une instance de [**LogFileEventConsumer**](logfileeventconsumer.md) pour recevoir les événements que vous demandez dans la requête, nommez l’instance dans la propriété **Name** , puis placez le chemin d’accès au fichier journal dans la propriété **filename** .

    Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](designing-managed-object-format--mof--classes.md).

2.  Fournissez le modèle de texte à écrire dans le fichier journal dans la propriété Text.

    Pour plus d’informations, consultez [utilisation de modèles de chaîne standard](using-standard-string-templates.md).

3.  Créez une instance de [**\_ \_ EventFilter**](--eventfilter.md) et définissez une requête pour spécifier les événements qui activeront le consommateur.

    Pour plus d’informations, consultez [interrogation avec WQL](querying-with-wql.md).

4.  Créez une instance de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) pour associer le filtre à l’instance de [**LogFileEventConsumer**](logfileeventconsumer.md).
5.  Pour contrôler qui lit ou écrit dans votre fichier journal, définissez la sécurité sur le répertoire où le journal se trouve au niveau requis.
6.  Compilez votre fichier MOF à l’aide de [**Mofcomp.exe**](mofcomp.md).

## <a name="example"></a>Exemples

L’exemple de cette section se trouve dans le code MOF, mais vous pouvez créer des instances par programme à l’aide [de l’API de script pour WMI](scripting-api-for-wmi.md) ou [de l’API com pour WMI](com-api-for-wmi.md). L’exemple utilise le LogFileEventConsumer standard pour créer une classe de consommateur nommée LogFileEvent qui écrit une ligne dans le fichier c : \\ logfile. log lorsqu’une instance de la classe LogFileEvent est créée.

La procédure suivante décrit comment utiliser l’exemple.

**Pour utiliser l’exemple**

1.  Copiez le Listing MOF ci-dessous dans un fichier texte et enregistrez-le avec une extension. mof.
2.  Dans une fenêtre de commande, compilez le fichier MOF à l’aide de la commande suivante.

    Fichier **mofcomp** ** * *. mof**

3.  Ouvrez logfile. log pour voir la ligne spécifiée par LogFileEvent.Name : « logfile Event Consumer Event ».

``` syntax
// Set the namespace as root\subscription.
// The LogFileEventConsumer is already compiled 
//     in the root\subscription namespace. 

#pragma namespace ("\\\\.\\Root\\subscription")

class LogFileEvent
{
    [key]string Name;
};

// Create an instance of the standard log
// file consumer and give it the alias $CONSUMER

instance of LogFileEventConsumer as $CONSUMER
{
    // If the file does not already exist, it is created.
    Filename = "c:\\Logfile.log";  
    IsUnicode = FALSE;
    // Name of this instance of LogFileEventConsumer
    Name = "LogfileEventConsumer_Example";  
    // See "Using Standard String Templates"; 
    Text = "%TargetInstance.Name%"; 
    // TargetInstance is the instance of LogFileEvent 
    //    requested in the filter        
                                         
};

// Create an instance of the event filter 
// and give it the alias $FILTER
// Query for any instance operation type,
// such as instance creation, for LogFileEvent class

instance of __EventFilter as $FILTER
{
    Name = "LogFileFilter";
    Query = "SELECT * FROM __InstanceOperationEvent "
        "WHERE TargetInstance.__class = \"LogFileEvent\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding.

instance of __FilterToConsumerBinding
{
    Consumer=$CONSUMER;
    Filter=$FILTER;
 DeliverSynchronously=FALSE;
};

// Create an instance of this class right now
// Look at the file c:\Logfile.log to see
// that a line has been written.

instance of LogFileEvent
{
 Name = "Logfile Event Consumer event";  
};
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



