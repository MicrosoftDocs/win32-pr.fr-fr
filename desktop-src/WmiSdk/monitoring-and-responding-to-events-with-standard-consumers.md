---
description: Vous pouvez utiliser les classes de consommateur standard installées pour effectuer des actions basées sur les événements d’un système d’exploitation.
ms.assetid: 1979dc55-a440-4c31-832b-36fa84def4c9
ms.tgt_platform: multiple
title: Surveillance et réponse aux événements avec des consommateurs standard
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5bd1d329cd861fa45c99851707177322d0b9d12f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103870221"
---
# <a name="monitoring-and-responding-to-events-with-standard-consumers"></a><span data-ttu-id="87d4f-103">Surveillance et réponse aux événements avec des consommateurs standard</span><span class="sxs-lookup"><span data-stu-id="87d4f-103">Monitoring and Responding to Events with Standard Consumers</span></span>

<span data-ttu-id="87d4f-104">Vous pouvez utiliser les [classes de consommateur standard](standard-consumer-classes.md) installées pour effectuer des actions basées sur les événements d’un système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="87d4f-104">You can use the installed [standard consumer classes](standard-consumer-classes.md) to perform actions based on events in an operating system.</span></span> <span data-ttu-id="87d4f-105">Les consommateurs standard sont des classes simples qui sont déjà inscrites et qui définissent des classes de consommateur permanentes.</span><span class="sxs-lookup"><span data-stu-id="87d4f-105">Standard consumers are simple classes that are already registered, and they define permanent consumer classes.</span></span> <span data-ttu-id="87d4f-106">Chaque consommateur standard prend une mesure spécifique après avoir reçu une notification d’événement.</span><span class="sxs-lookup"><span data-stu-id="87d4f-106">Each standard consumer takes a specific action after it receives an event notification.</span></span> <span data-ttu-id="87d4f-107">Par exemple, vous pouvez définir une instance de [**ActiveScriptEventConsumer**](activescripteventconsumer.md) pour exécuter un script lorsque l’espace disque libre sur un ordinateur est différent d’une taille spécifiée.</span><span class="sxs-lookup"><span data-stu-id="87d4f-107">For example, you can define an instance of [**ActiveScriptEventConsumer**](activescripteventconsumer.md) to execute a script when free disk space on a computer is different from a specified size.</span></span>

<span data-ttu-id="87d4f-108">WMI compile les consommateurs standard dans des espaces de noms par défaut qui dépendent du système d’exploitation, par exemple :</span><span class="sxs-lookup"><span data-stu-id="87d4f-108">WMI compiles the standard consumers into default namespaces that depend on the operating system, for example:</span></span>

-   <span data-ttu-id="87d4f-109">Dans Windows Server 2003, tous les consommateurs standard sont compilés par défaut dans l’espace de \\ noms « abonnement racine ».</span><span class="sxs-lookup"><span data-stu-id="87d4f-109">In Windows Server 2003, all of the standard consumers are compiled by default into the "Root\\Subscription" namespace.</span></span>

> [!Note]  
> <span data-ttu-id="87d4f-110">Pour les espaces de noms et les systèmes d’exploitation par défaut spécifiques à chaque classe WMI, consultez les sections remarques et exigences de chaque classe.</span><span class="sxs-lookup"><span data-stu-id="87d4f-110">For the default namespaces and operating systems that are specific for each WMI class, see the Remarks and Requirements sections of each class topic.</span></span>

 

<span data-ttu-id="87d4f-111">Le tableau suivant répertorie et décrit les consommateurs standard WMI.</span><span class="sxs-lookup"><span data-stu-id="87d4f-111">The following table lists and describes the WMI standard consumers.</span></span>



| <span data-ttu-id="87d4f-112">Consommateur standard</span><span class="sxs-lookup"><span data-stu-id="87d4f-112">Standard consumer</span></span>                                              | <span data-ttu-id="87d4f-113">Description</span><span class="sxs-lookup"><span data-stu-id="87d4f-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="87d4f-114">**ActiveScriptEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="87d4f-114">**ActiveScriptEventConsumer**</span></span>](activescripteventconsumer.md) | <span data-ttu-id="87d4f-115">Exécute un script lorsqu’il reçoit une notification d’événement.</span><span class="sxs-lookup"><span data-stu-id="87d4f-115">Executes a script when it receives an event notification.</span></span> <span data-ttu-id="87d4f-116">Pour plus d’informations, consultez [exécution d’un script basé sur un événement](running-a-script-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="87d4f-116">For more information, see [Running a Script Based on an Event](running-a-script-based-on-an-event.md).</span></span>                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="87d4f-117">**LogFileEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="87d4f-117">**LogFileEventConsumer**</span></span>](logfileeventconsumer.md)           | <span data-ttu-id="87d4f-118">Écrit des chaînes personnalisées dans un fichier journal texte lorsqu’il reçoit une notification d’événement.</span><span class="sxs-lookup"><span data-stu-id="87d4f-118">Writes customized strings to a text log file when it receives an event notification.</span></span> <span data-ttu-id="87d4f-119">Pour plus d’informations, consultez [écriture dans un fichier journal basé sur un événement](writing-to-a-log-file-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="87d4f-119">For more information, see [Writing to a Log File Based on an Event](writing-to-a-log-file-based-on-an-event.md).</span></span>                                                                                                                                                                                                                  |
| [<span data-ttu-id="87d4f-120">**NTEventLogEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="87d4f-120">**NTEventLogEventConsumer**</span></span>](nteventlogeventconsumer.md)     | <span data-ttu-id="87d4f-121">Enregistre un message spécifique dans le journal des événements de l’application.</span><span class="sxs-lookup"><span data-stu-id="87d4f-121">Logs a specific message to the Application event log.</span></span> <span data-ttu-id="87d4f-122">Pour plus d’informations, consultez [journalisation dans le journal des événements NT basé sur un événement](logging-to-nt-event-log-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="87d4f-122">For more information, see [Logging to NT Event Log Based on an Event](logging-to-nt-event-log-based-on-an-event.md).</span></span>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="87d4f-123">**SMTPEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="87d4f-123">**SMTPEventConsumer**</span></span>](smtpeventconsumer.md)                 | <span data-ttu-id="87d4f-124">Envoie un message électronique à l’aide du protocole SMTP à chaque fois qu’un événement lui est remis.</span><span class="sxs-lookup"><span data-stu-id="87d4f-124">Sends an email message by using SMTP each time an event is delivered to it.</span></span> <span data-ttu-id="87d4f-125">Pour plus d’informations, consultez [envoi de courriers électroniques en fonction d’un événement](sending-e-mail-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="87d4f-125">For more information, see [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md).</span></span>                                                                                                                                                                                                                                          |
| [<span data-ttu-id="87d4f-126">**CommandLineEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="87d4f-126">**CommandLineEventConsumer**</span></span>](commandlineeventconsumer.md)   | <span data-ttu-id="87d4f-127">Lance un processus lorsqu’un événement est remis à un système local.</span><span class="sxs-lookup"><span data-stu-id="87d4f-127">Launches a process when an event is delivered to a local system.</span></span> <span data-ttu-id="87d4f-128">Le fichier exécutable doit se trouver dans un emplacement sécurisé, ou sécurisé avec une liste de contrôle d’accès (ACL) forte pour empêcher un utilisateur non autorisé de remplacer votre exécutable par un autre exécutable.</span><span class="sxs-lookup"><span data-stu-id="87d4f-128">The executable file must be in a secure location, or secured with a strong access control list (ACL) to prevent an unauthorized user from replacing your executable with a different executable.</span></span> <span data-ttu-id="87d4f-129">Pour plus d’informations, consultez [exécution d’un programme à partir de la ligne de commande en fonction d’un événement](running-a-program-from-the-command-line-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="87d4f-129">For more information, see [Running a Program from the Command Line Based on an Event](running-a-program-from-the-command-line-based-on-an-event.md).</span></span> |



 

<span data-ttu-id="87d4f-130">La procédure suivante décrit comment surveiller les événements et y répondre à l’aide d’un consommateur standard.</span><span class="sxs-lookup"><span data-stu-id="87d4f-130">The following procedure describes how to monitor and respond to events by using a standard consumer.</span></span> <span data-ttu-id="87d4f-131">Notez que la procédure est la même pour un fichier, un script ou une application format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="87d4f-131">Note that the procedure is the same for a Managed Object Format (MOF) file, script, or application.</span></span>

<span data-ttu-id="87d4f-132">**Pour surveiller les événements et y répondre à l’aide d’un consommateur standard**</span><span class="sxs-lookup"><span data-stu-id="87d4f-132">**To monitor and respond to events with a standard consumer**</span></span>

1.  <span data-ttu-id="87d4f-133">Spécifiez l’espace de noms dans un fichier MOF à l’aide de l' [ \# espace de noms du pragma](pragma-namespace.md)de commande du préprocesseur MOF.</span><span class="sxs-lookup"><span data-stu-id="87d4f-133">Specify the namespace in a MOF file by using the MOF preprocessor command [\#pragma namespace](pragma-namespace.md).</span></span> <span data-ttu-id="87d4f-134">Dans un script ou une application, spécifiez l’espace de noms dans le code qui se connecte à WMI.</span><span class="sxs-lookup"><span data-stu-id="87d4f-134">In a script or application, specify the namespace in the code that connects to WMI.</span></span>

    <span data-ttu-id="87d4f-135">L’exemple de code MOF suivant montre comment spécifier l’espace de noms de l' \\ abonnement racine.</span><span class="sxs-lookup"><span data-stu-id="87d4f-135">The following MOF code example shows how to specify the root\\subscription namespace.</span></span>

    ```syntax
    #pragma namespace ("\\\\.\\root\\subscription")
    ```

    <span data-ttu-id="87d4f-136">La plupart des [*événements intrinsèques*](gloss-i.md) sont associés aux modifications apportées aux instances de classe dans l' \\ espace de noms CIMV2 racine.</span><span class="sxs-lookup"><span data-stu-id="87d4f-136">Most [*intrinsic events*](gloss-i.md) are associated with changes to class instances in the root\\cimv2 namespace.</span></span> <span data-ttu-id="87d4f-137">Toutefois, les événements de Registre tels que [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) sont déclenchés dans l' \\ espace de noms racine par défaut par le [fournisseur de Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider).</span><span class="sxs-lookup"><span data-stu-id="87d4f-137">However, registry events such as [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) are fired in the root\\default namespace by the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider).</span></span>

    <span data-ttu-id="87d4f-138">Un consommateur peut inclure des classes d’événements situées dans d’autres espaces de noms en spécifiant l’espace de noms dans la propriété **EventNamespace** de la requête [**\_ \_ EventFilter**](--eventfilter.md) pour les événements.</span><span class="sxs-lookup"><span data-stu-id="87d4f-138">A consumer can include event classes located in other namespaces by specifying the namespace in the **EventNamespace** property in the [**\_\_EventFilter**](--eventfilter.md) query for events.</span></span> <span data-ttu-id="87d4f-139">Les classes d' [*événements intrinsèques*](gloss-i.md) , telles que [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md) , sont disponibles dans chaque espace de noms.</span><span class="sxs-lookup"><span data-stu-id="87d4f-139">The [*intrinsic events*](gloss-i.md) classes, such as [**\_\_InstanceOperationEvent**](--instanceoperationevent.md) are available in every namespace.</span></span>

2.  <span data-ttu-id="87d4f-140">Créer et remplir une instance d’une classe de consommateur standard.</span><span class="sxs-lookup"><span data-stu-id="87d4f-140">Create and populate an instance of a standard consumer class.</span></span>

    <span data-ttu-id="87d4f-141">Cette instance peut avoir une valeur unique dans la propriété **Name** .</span><span class="sxs-lookup"><span data-stu-id="87d4f-141">This instance may have a unique value in the **Name** property.</span></span> <span data-ttu-id="87d4f-142">Vous pouvez mettre à jour un consommateur existant en réutilisant le même nom.</span><span class="sxs-lookup"><span data-stu-id="87d4f-142">You can update an existing consumer by reusing the same name.</span></span>

    <span data-ttu-id="87d4f-143">**InsertionStringTemplates** contient le texte à insérer dans un événement que vous spécifiez dans **eventType**.</span><span class="sxs-lookup"><span data-stu-id="87d4f-143">**InsertionStringTemplates** contains the text to insert in an event that you specify in **EventType**.</span></span> <span data-ttu-id="87d4f-144">Vous pouvez utiliser des chaînes littérales ou faire directement référence à une propriété.</span><span class="sxs-lookup"><span data-stu-id="87d4f-144">You can use literal strings or refer directly to a property.</span></span> <span data-ttu-id="87d4f-145">Pour plus d’informations, consultez [utilisation de modèles de chaîne standard](using-standard-string-templates.md) et [instruction SELECT pour les requêtes d’événement](select-statement-for-event-queries.md).</span><span class="sxs-lookup"><span data-stu-id="87d4f-145">For more information, see [Using Standard String Templates](using-standard-string-templates.md) and [SELECT Statement for Event Queries](select-statement-for-event-queries.md).</span></span>

    <span data-ttu-id="87d4f-146">Utilisez une source existante pour le journal des événements qui prend en charge une chaîne d’insertion sans texte associé.</span><span class="sxs-lookup"><span data-stu-id="87d4f-146">Use an existing source for the event log that supports an insertion string without associated text.</span></span>

    <span data-ttu-id="87d4f-147">L’exemple de code MOF suivant montre comment utiliser une source existante de WSH et une valeur **eventID** 8.</span><span class="sxs-lookup"><span data-stu-id="87d4f-147">The following MOF code example shows how to use an existing source of WSH and an **EventID** value of 8.</span></span>

    ```syntax
    instance of NTEventLogEventConsumer as $Consumer
    {
        Name = "RunKeyEventlogConsumer";
        SourceName = "WSH";               
        EventID = 8;
        // Warning                              
        EventType = 2;
        // One string supplies the entire message          
        NumberOfInsertionStrings = 1;             
        // the %Hive% and %KeyPath% are properties of
        // the RegistryKeyChangeEvent instance 
        InsertionStringTemplates = 
            {"The key %Hive%\\%RootPath% has been modified."
            "Check if the change is intentional"};
    };
    ```

3.  <span data-ttu-id="87d4f-148">Créez une instance de [**\_ \_ EventFilter**](--eventfilter.md) et définissez une requête pour les événements.</span><span class="sxs-lookup"><span data-stu-id="87d4f-148">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and define a query for events.</span></span>

    <span data-ttu-id="87d4f-149">Dans l’exemple suivant, le filtre analyse la clé de Registre dans laquelle les programmes de démarrage sont inscrits.</span><span class="sxs-lookup"><span data-stu-id="87d4f-149">In the following example, the filter monitors the registry key where startup programs are registered.</span></span> <span data-ttu-id="87d4f-150">La surveillance de cette clé de Registre peut être importante, car un programme non autorisé peut s’enregistrer sous la clé, ce qui entraîne son lancement au démarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="87d4f-150">Monitoring this registry key may be important because an unauthorized program can register itself under the key, which causes it to be launched when the computer boots.</span></span>

    ```syntax
    instance of __EventFilter as $Filter
    {
    Name = "RunKeyFilter";
    QueryLanguage = "WQL"; 
    Query = "Select * from RegistryTreeChangeEvent"
        " where (Hive = \"HKEY_LOCAL_MACHINE\" and "
        "RootPath = \"Software\\\\Microsoft\\\\Windows"
        "\\\\CurrentVersion\\\\Run\")";

    // RegistryTreeChangeEvents only fire in root\default namespace
    EventNamespace = "root\\default";                       
    };
    ```

4.  <span data-ttu-id="87d4f-151">Identifiez un événement pour surveiller et créer une requête d’événement.</span><span class="sxs-lookup"><span data-stu-id="87d4f-151">Identify an event to monitor and create an event query.</span></span>

    <span data-ttu-id="87d4f-152">Vous pouvez vérifier s’il existe un événement intrinsèque ou extrinsèque qui utilise.</span><span class="sxs-lookup"><span data-stu-id="87d4f-152">You can check to see if there is an intrinsic or extrinsic event that use.</span></span> <span data-ttu-id="87d4f-153">Par exemple, utilisez la classe [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) du fournisseur Registry pour surveiller les modifications apportées au registre système.</span><span class="sxs-lookup"><span data-stu-id="87d4f-153">For example, use the [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) class of the Registry provider to monitor changes to the system registry.</span></span>

    <span data-ttu-id="87d4f-154">S’il n’existe pas de classe qui décrit un événement que vous devez surveiller, vous devez créer votre propre fournisseur d’événements et définir de nouvelles classes d’événements extrinsèques.</span><span class="sxs-lookup"><span data-stu-id="87d4f-154">If a class does not exist that describes an event you need to monitor, you must create your own event provider, and define new extrinsic event classes.</span></span> <span data-ttu-id="87d4f-155">Pour plus d’informations, consultez [écriture d’un fournisseur d’événements](writing-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="87d4f-155">For more information, see [Writing an Event Provider](writing-an-event-provider.md).</span></span>

    <span data-ttu-id="87d4f-156">Dans un fichier MOF, vous pouvez définir un [*alias*](gloss-a.md) pour le filtre et le consommateur, ce qui fournit un moyen simple de décrire les chemins d’accès d’instance.</span><span class="sxs-lookup"><span data-stu-id="87d4f-156">In a MOF file, you can define an [*alias*](gloss-a.md) for the filter and consumer, which provides an easy way to describe the instance paths.</span></span>

    <span data-ttu-id="87d4f-157">L’exemple suivant montre comment définir un [*alias*](gloss-a.md) pour le filtre et le consommateur.</span><span class="sxs-lookup"><span data-stu-id="87d4f-157">The following example shows how to define an [*alias*](gloss-a.md) for the filter and consumer.</span></span>

    ```syntax
    instance of __EventFilter as $FILTER
    instance of LogFileEventConsumer as $CONSUMER
    ```

5.  <span data-ttu-id="87d4f-158">Créez une instance de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) pour associer le filtre et les classes de consommateur.</span><span class="sxs-lookup"><span data-stu-id="87d4f-158">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter and the consumer classes.</span></span> <span data-ttu-id="87d4f-159">Cette instance détermine que, lorsqu’un événement qui correspond au filtre spécifié se produit, l’action spécifiée par le consommateur doit se produire.</span><span class="sxs-lookup"><span data-stu-id="87d4f-159">This instance determines that when an event occurs that matches the specified filter, the action specified by the consumer must occur.</span></span> <span data-ttu-id="87d4f-160">[**\_ \_ EventFilter**](--eventfilter.md), [**\_ \_ EventConsumer**](--eventconsumer.md)et **\_ \_ FilterToConsumerBinding** doivent avoir le même identificateur de sécurité (SID) individuel dans la propriété **CreatorSID** .</span><span class="sxs-lookup"><span data-stu-id="87d4f-160">[**\_\_EventFilter**](--eventfilter.md), [**\_\_EventConsumer**](--eventconsumer.md), and **\_\_FilterToConsumerBinding** must have the same individual security identifier (SID) in the **CreatorSID** property.</span></span> <span data-ttu-id="87d4f-161">Pour plus d’informations, consultez [liaison d’un filtre d’événements à un consommateur logique](binding-an-event-filter-with-a-logical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="87d4f-161">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md).</span></span>

    <span data-ttu-id="87d4f-162">L’exemple suivant montre comment identifier une instance par le chemin d’accès de l’objet ou utiliser un alias comme expression abrégée pour le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="87d4f-162">The following example shows how to identify an instance by the object path, or use an alias as a shorthand expression for the object path.</span></span>

    ```syntax
    instance of __EventFilter as $FILTER
    instance of NTEventLogEventConsumer as $CONSUMER
    ```

    <span data-ttu-id="87d4f-163">L’exemple suivant lie le filtre au consommateur à l’aide d’alias.</span><span class="sxs-lookup"><span data-stu-id="87d4f-163">The following example binds the filter to the consumer by using aliases.</span></span>

    ```syntax
    instance of __FilterToConsumerBinding
    {
        Filter = $FILTER;
        Consumer = $CONSUMER;
        
    };
    ```

    <span data-ttu-id="87d4f-164">Vous pouvez lier un filtre à plusieurs consommateurs, ce qui indique que lorsque des événements correspondants se produisent, plusieurs actions doivent être effectuées ; vous pouvez ou lier un consommateur à plusieurs filtres, ce qui indique que l’action doit être effectuée lorsque des événements qui correspondent à l’un des filtres se produisent.</span><span class="sxs-lookup"><span data-stu-id="87d4f-164">You can bind one filter to several consumers, which indicates that when matching events occur, several actions must be taken; or you can bind one consumer to several filters, which indicates that the action must be taken when events that match one of the filters occur.</span></span>

    <span data-ttu-id="87d4f-165">Les actions suivantes sont effectuées en fonction de la condition des consommateurs et des événements :</span><span class="sxs-lookup"><span data-stu-id="87d4f-165">The following actions are taken based on the condition of consumers and events:</span></span>

    -   <span data-ttu-id="87d4f-166">Si l’un des consommateurs permanents échoue, les autres consommateurs qui demandent l’événement reçoivent une notification.</span><span class="sxs-lookup"><span data-stu-id="87d4f-166">If one of the permanent consumers fails, other consumers that request the event receive notification.</span></span>
    -   <span data-ttu-id="87d4f-167">En cas de suppression d’un événement, WMI déclenche [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="87d4f-167">If an event is dropped, WMI fires [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>
    -   <span data-ttu-id="87d4f-168">Si vous vous abonnez à cet événement, il retourne l’événement qui est supprimé, et une référence à [**\_ \_ EventConsumer**](--eventconsumer.md) représente le consommateur qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="87d4f-168">If you subscribe to this event, it returns the event that is dropped, and a reference to the [**\_\_EventConsumer**](--eventconsumer.md) represents the failed consumer.</span></span>
    -   <span data-ttu-id="87d4f-169">En cas de défaillance d’un consommateur, WMI déclenche [**\_ \_ ConsumerFailureEvent**](--consumerfailureevent.md), qui peut contenir plus d’informations dans les propriétés **ErrorCode**, **ErrorDescription** et **ErrorObject** .</span><span class="sxs-lookup"><span data-stu-id="87d4f-169">If a consumer fails, WMI fires [**\_\_ConsumerFailureEvent**](--consumerfailureevent.md), which may contain more information in the **ErrorCode**, **ErrorDescription** and **ErrorObject** properties.</span></span>

    <span data-ttu-id="87d4f-170">Pour plus d’informations, consultez [liaison d’un filtre d’événements à un consommateur logique](binding-an-event-filter-with-a-logical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="87d4f-170">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md).</span></span>

## <a name="example"></a><span data-ttu-id="87d4f-171">Exemple</span><span class="sxs-lookup"><span data-stu-id="87d4f-171">Example</span></span>

<span data-ttu-id="87d4f-172">L’exemple suivant montre le fichier MOF pour une instance de [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="87d4f-172">The following example shows the MOF for an instance of [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span></span> <span data-ttu-id="87d4f-173">Une fois que vous avez compilé ce fichier MOF, toute tentative de création, de suppression ou de modification d’une valeur dans le chemin d’accès au Registre **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run** enregistre une entrée dans le journal des événements de l’application, sous la source « WSH ».</span><span class="sxs-lookup"><span data-stu-id="87d4f-173">After you compile this MOF, any attempt to create, delete, or modify a value in the Registry path **HKEY\_LOCAL\_MACHINE\\ Software\\Microsoft\\Windows\\CurrentVersion\\Run** logs an entry in the Application eventlog, under the source "WSH".</span></span>


```mof
#pragma namespace ("\\\\.\\root\\subscription")
 
instance of __EventFilter as $Filter
{
    Name = "RunKeyFilter";
    QueryLanguage = "WQL";
    Query = "Select * from RegistryTreeChangeEvent"
            " where (Hive = \"HKEY_LOCAL_MACHINE\" and "
            "KeyPath = \"Software\\\\Microsoft\\\\Windows"
            "\\\\CurrentVersion\\\\Run\")";

    // RegistryTreeChangeEvents only fire
    // in root\default namespace
    EventNamespace = "root\\default";   
};
 
instance of NTEventLogEventConsumer as $Consumer
{
    Name = "RunKeyEventlogConsumer";
    SourceName = "WSH";               
    EventID = 8;
    EventType = 2;                            // Warning
    Category = 0;
    NumberOfInsertionStrings = 1;

    // the %Hive% and %KeyPath% are properties
    // of the RegistryKeyChangeEvent instance 
    InsertionStringTemplates = {"The key %Hive%\\%RootPath% "
        "has been modified. Check if the change is intentional"};
};
 

// Bind the filter to the consumer
instance of __FilterToConsumerBinding
{
    Filter = $Filter;
    Consumer = $Consumer;
};
```



## <a name="related-topics"></a><span data-ttu-id="87d4f-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="87d4f-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87d4f-175">Réception des événements en toute sécurité</span><span class="sxs-lookup"><span data-stu-id="87d4f-175">Receiving Events Securely</span></span>](receiving-events-securely.md)
</dt> </dl>

 

 
