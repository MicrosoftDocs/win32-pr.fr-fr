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
ms.openlocfilehash: 33cc82925b6afc1690f2cd87607f21e9ea02fdbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202275"
---
# <a name="writing-to-a-log-file-based-on-an-event"></a><span data-ttu-id="b8955-104">Écriture dans un fichier journal basé sur un événement</span><span class="sxs-lookup"><span data-stu-id="b8955-104">Writing to a Log File Based on an Event</span></span>

<span data-ttu-id="b8955-105">La classe [**LogFileEventConsumer**](logfileeventconsumer.md) peut écrire du texte prédéfini dans un fichier journal lorsqu’un événement spécifié se produit.</span><span class="sxs-lookup"><span data-stu-id="b8955-105">The [**LogFileEventConsumer**](logfileeventconsumer.md) class can write predefined text to a log file when a specified event occurs.</span></span> <span data-ttu-id="b8955-106">Cette classe est un consommateur d’événements standard fourni par WMI.</span><span class="sxs-lookup"><span data-stu-id="b8955-106">This class is a standard event consumer that WMI provides.</span></span>

<span data-ttu-id="b8955-107">La procédure de base pour l’utilisation de consommateurs standard est toujours la même, et se trouve dans la [surveillance et la réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="b8955-107">The basic procedure for using standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="b8955-108">La procédure suivante ajoute à la procédure de base, est spécifique à la classe [**LogFileEventConsumer**](logfileeventconsumer.md) et décrit comment créer un consommateur d’événements qui exécute un programme.</span><span class="sxs-lookup"><span data-stu-id="b8955-108">The following procedure adds to the basic procedure, is specific to the [**LogFileEventConsumer**](logfileeventconsumer.md) class, and describes how to create an event consumer that runs a program.</span></span>

<span data-ttu-id="b8955-109">**Pour créer un consommateur d’événements qui écrit dans un fichier journal**</span><span class="sxs-lookup"><span data-stu-id="b8955-109">**To create an event consumer that writes to a log file**</span></span>

1.  <span data-ttu-id="b8955-110">Dans le fichier format MOF (MOF), créez une instance de [**LogFileEventConsumer**](logfileeventconsumer.md) pour recevoir les événements que vous demandez dans la requête, nommez l’instance dans la propriété **Name** , puis placez le chemin d’accès au fichier journal dans la propriété **filename** .</span><span class="sxs-lookup"><span data-stu-id="b8955-110">In the Managed Object Format (MOF) file, create an instance of [**LogFileEventConsumer**](logfileeventconsumer.md) to receive the events you request in the query, name the instance in the **Name** property, and then place the path to the log file in the **Filename** property.</span></span>

    <span data-ttu-id="b8955-111">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="b8955-111">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

2.  <span data-ttu-id="b8955-112">Fournissez le modèle de texte à écrire dans le fichier journal dans la propriété Text.</span><span class="sxs-lookup"><span data-stu-id="b8955-112">Provide the text template to write to the log file in the Text property.</span></span>

    <span data-ttu-id="b8955-113">Pour plus d’informations, consultez [utilisation de modèles de chaîne standard](using-standard-string-templates.md).</span><span class="sxs-lookup"><span data-stu-id="b8955-113">For more information, see [Using Standard String Templates](using-standard-string-templates.md).</span></span>

3.  <span data-ttu-id="b8955-114">Créez une instance de [**\_ \_ EventFilter**](--eventfilter.md) et définissez une requête pour spécifier les événements qui activeront le consommateur.</span><span class="sxs-lookup"><span data-stu-id="b8955-114">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and define a query to specify the events that will activate the consumer.</span></span>

    <span data-ttu-id="b8955-115">Pour plus d’informations, consultez [interrogation avec WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="b8955-115">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="b8955-116">Créez une instance de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) pour associer le filtre à l’instance de [**LogFileEventConsumer**](logfileeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="b8955-116">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**LogFileEventConsumer**](logfileeventconsumer.md).</span></span>
5.  <span data-ttu-id="b8955-117">Pour contrôler qui lit ou écrit dans votre fichier journal, définissez la sécurité sur le répertoire où le journal se trouve au niveau requis.</span><span class="sxs-lookup"><span data-stu-id="b8955-117">To control who reads or writes to your log file, set the security on the directory where the log is located to the required level.</span></span>
6.  <span data-ttu-id="b8955-118">Compilez votre fichier MOF à l’aide de [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="b8955-118">Compile your MOF file using [**Mofcomp.exe**](mofcomp.md).</span></span>

## <a name="example"></a><span data-ttu-id="b8955-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="b8955-119">Example</span></span>

<span data-ttu-id="b8955-120">L’exemple de cette section se trouve dans le code MOF, mais vous pouvez créer des instances par programme à l’aide [de l’API de script pour WMI](scripting-api-for-wmi.md) ou [de l’API com pour WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="b8955-120">The example in this section is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="b8955-121">L’exemple utilise le LogFileEventConsumer standard pour créer une classe de consommateur nommée LogFileEvent qui écrit une ligne dans le fichier c : \\ logfile. log lorsqu’une instance de la classe LogFileEvent est créée.</span><span class="sxs-lookup"><span data-stu-id="b8955-121">The example uses the standard LogFileEventConsumer to create a consumer class named LogFileEvent that writes a line to the file c:\\Logfile.log when an instance of the class LogFileEvent is created.</span></span>

<span data-ttu-id="b8955-122">La procédure suivante décrit comment utiliser l’exemple.</span><span class="sxs-lookup"><span data-stu-id="b8955-122">The following procedure describes how to use the example.</span></span>

<span data-ttu-id="b8955-123">**Pour utiliser l’exemple**</span><span class="sxs-lookup"><span data-stu-id="b8955-123">**To use the example**</span></span>

1.  <span data-ttu-id="b8955-124">Copiez le Listing MOF ci-dessous dans un fichier texte et enregistrez-le avec une extension. mof.</span><span class="sxs-lookup"><span data-stu-id="b8955-124">Copy the MOF listing below into a text file and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="b8955-125">Dans une fenêtre de commande, compilez le fichier MOF à l’aide de la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="b8955-125">In a command window, compile the MOF file by using the following command.</span></span>

    <span data-ttu-id="b8955-126">Fichier **mofcomp** \*\* \* *. mof*\*</span><span class="sxs-lookup"><span data-stu-id="b8955-126">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

3.  <span data-ttu-id="b8955-127">Ouvrez logfile. log pour voir la ligne spécifiée par LogFileEvent.Name : « logfile Event Consumer Event ».</span><span class="sxs-lookup"><span data-stu-id="b8955-127">Open Logfile.log to see the line specified by LogFileEvent.Name: "Logfile Event Consumer event".</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="b8955-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b8955-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8955-129">Surveillance et réponse aux événements avec des consommateurs standard</span><span class="sxs-lookup"><span data-stu-id="b8955-129">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



