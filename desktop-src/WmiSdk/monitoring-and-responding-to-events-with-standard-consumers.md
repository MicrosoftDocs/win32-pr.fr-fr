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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010448"
---
# <a name="monitoring-and-responding-to-events-with-standard-consumers"></a>Surveillance et réponse aux événements avec des consommateurs standard

Vous pouvez utiliser les [classes de consommateur standard](standard-consumer-classes.md) installées pour effectuer des actions basées sur les événements d’un système d’exploitation. Les consommateurs standard sont des classes simples qui sont déjà inscrites et qui définissent des classes de consommateur permanentes. Chaque consommateur standard prend une mesure spécifique après avoir reçu une notification d’événement. Par exemple, vous pouvez définir une instance de [**ActiveScriptEventConsumer**](activescripteventconsumer.md) pour exécuter un script lorsque l’espace disque libre sur un ordinateur est différent d’une taille spécifiée.

WMI compile les consommateurs standard dans des espaces de noms par défaut qui dépendent du système d’exploitation, par exemple :

-   dans Windows Server 2003, tous les consommateurs standard sont compilés par défaut dans l’espace de \\ noms « abonnement racine ».

> [!Note]  
> Pour les espaces de noms et les systèmes d’exploitation par défaut spécifiques à chaque classe WMI, consultez les sections remarques et exigences de chaque classe.

 

Le tableau suivant répertorie et décrit les consommateurs standard WMI.



| Consommateur standard                                              | Description                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActiveScriptEventConsumer**](activescripteventconsumer.md) | Exécute un script lorsqu’il reçoit une notification d’événement. Pour plus d’informations, consultez [exécution d’un script basé sur un événement](running-a-script-based-on-an-event.md).                                                                                                                                                                                                                                                       |
| [**LogFileEventConsumer**](logfileeventconsumer.md)           | Écrit des chaînes personnalisées dans un fichier journal texte lorsqu’il reçoit une notification d’événement. Pour plus d’informations, consultez [écriture dans un fichier journal basé sur un événement](writing-to-a-log-file-based-on-an-event.md).                                                                                                                                                                                                                  |
| [**NTEventLogEventConsumer**](nteventlogeventconsumer.md)     | Enregistre un message spécifique dans le journal des événements de l’application. Pour plus d’informations, consultez [journalisation dans le journal des événements NT basé sur un événement](logging-to-nt-event-log-based-on-an-event.md).                                                                                                                                                                                                                                             |
| [**SMTPEventConsumer**](smtpeventconsumer.md)                 | Envoie un message électronique à l’aide du protocole SMTP à chaque fois qu’un événement lui est remis. Pour plus d’informations, consultez [envoi de courriers électroniques en fonction d’un événement](sending-e-mail-based-on-an-event.md).                                                                                                                                                                                                                                          |
| [**CommandLineEventConsumer**](commandlineeventconsumer.md)   | Lance un processus lorsqu’un événement est remis à un système local. Le fichier exécutable doit se trouver dans un emplacement sécurisé, ou sécurisé avec une liste de contrôle d’accès (ACL) forte pour empêcher un utilisateur non autorisé de remplacer votre exécutable par un autre exécutable. Pour plus d’informations, consultez [exécution d’un programme à partir de la ligne de commande en fonction d’un événement](running-a-program-from-the-command-line-based-on-an-event.md). |



 

La procédure suivante décrit comment surveiller les événements et y répondre à l’aide d’un consommateur standard. Notez que la procédure est la même pour un fichier, un script ou une application format MOF (MOF).

**Pour surveiller les événements et y répondre à l’aide d’un consommateur standard**

1.  Spécifiez l’espace de noms dans un fichier MOF à l’aide de l' [ \# espace de noms du pragma](pragma-namespace.md)de commande du préprocesseur MOF. Dans un script ou une application, spécifiez l’espace de noms dans le code qui se connecte à WMI.

    L’exemple de code MOF suivant montre comment spécifier l’espace de noms de l' \\ abonnement racine.

    ```syntax
    #pragma namespace ("\\\\.\\root\\subscription")
    ```

    La plupart des [*événements intrinsèques*](gloss-i.md) sont associés aux modifications apportées aux instances de classe dans l' \\ espace de noms CIMV2 racine. Toutefois, les événements de Registre tels que [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) sont déclenchés dans l' \\ espace de noms racine par défaut par le [fournisseur de Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider).

    Un consommateur peut inclure des classes d’événements situées dans d’autres espaces de noms en spécifiant l’espace de noms dans la propriété **EventNamespace** de la requête [**\_ \_ EventFilter**](--eventfilter.md) pour les événements. Les classes d' [*événements intrinsèques*](gloss-i.md) , telles que [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md) , sont disponibles dans chaque espace de noms.

2.  Créer et remplir une instance d’une classe de consommateur standard.

    Cette instance peut avoir une valeur unique dans la propriété **Name** . Vous pouvez mettre à jour un consommateur existant en réutilisant le même nom.

    **InsertionStringTemplates** contient le texte à insérer dans un événement que vous spécifiez dans **eventType**. Vous pouvez utiliser des chaînes littérales ou faire directement référence à une propriété. Pour plus d’informations, consultez [utilisation de modèles de chaîne standard](using-standard-string-templates.md) et [instruction SELECT pour les requêtes d’événement](select-statement-for-event-queries.md).

    Utilisez une source existante pour le journal des événements qui prend en charge une chaîne d’insertion sans texte associé.

    L’exemple de code MOF suivant montre comment utiliser une source existante de WSH et une valeur **eventID** 8.

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

3.  Créez une instance de [**\_ \_ EventFilter**](--eventfilter.md) et définissez une requête pour les événements.

    Dans l’exemple suivant, le filtre analyse la clé de Registre dans laquelle les programmes de démarrage sont inscrits. La surveillance de cette clé de Registre peut être importante, car un programme non autorisé peut s’enregistrer sous la clé, ce qui entraîne son lancement au démarrage de l’ordinateur.

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

4.  Identifiez un événement pour surveiller et créer une requête d’événement.

    Vous pouvez vérifier s’il existe un événement intrinsèque ou extrinsèque qui utilise. Par exemple, utilisez la classe [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) du fournisseur Registry pour surveiller les modifications apportées au registre système.

    S’il n’existe pas de classe qui décrit un événement que vous devez surveiller, vous devez créer votre propre fournisseur d’événements et définir de nouvelles classes d’événements extrinsèques. Pour plus d’informations, consultez [écriture d’un fournisseur d’événements](writing-an-event-provider.md).

    Dans un fichier MOF, vous pouvez définir un [*alias*](gloss-a.md) pour le filtre et le consommateur, ce qui fournit un moyen simple de décrire les chemins d’accès d’instance.

    L’exemple suivant montre comment définir un [*alias*](gloss-a.md) pour le filtre et le consommateur.

    ```syntax
    instance of __EventFilter as $FILTER
    instance of LogFileEventConsumer as $CONSUMER
    ```

5.  Créez une instance de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) pour associer le filtre et les classes de consommateur. Cette instance détermine que, lorsqu’un événement qui correspond au filtre spécifié se produit, l’action spécifiée par le consommateur doit se produire. [**\_ \_ EventFilter**](--eventfilter.md), [**\_ \_ EventConsumer**](--eventconsumer.md)et **\_ \_ FilterToConsumerBinding** doivent avoir le même identificateur de sécurité (SID) individuel dans la propriété **CreatorSID** . Pour plus d’informations, consultez [liaison d’un filtre d’événements à un consommateur logique](binding-an-event-filter-with-a-logical-consumer.md).

    L’exemple suivant montre comment identifier une instance par le chemin d’accès de l’objet ou utiliser un alias comme expression abrégée pour le chemin d’accès de l’objet.

    ```syntax
    instance of __EventFilter as $FILTER
    instance of NTEventLogEventConsumer as $CONSUMER
    ```

    L’exemple suivant lie le filtre au consommateur à l’aide d’alias.

    ```syntax
    instance of __FilterToConsumerBinding
    {
        Filter = $FILTER;
        Consumer = $CONSUMER;
        
    };
    ```

    Vous pouvez lier un filtre à plusieurs consommateurs, ce qui indique que lorsque des événements correspondants se produisent, plusieurs actions doivent être effectuées ; vous pouvez ou lier un consommateur à plusieurs filtres, ce qui indique que l’action doit être effectuée lorsque des événements qui correspondent à l’un des filtres se produisent.

    Les actions suivantes sont effectuées en fonction de la condition des consommateurs et des événements :

    -   Si l’un des consommateurs permanents échoue, les autres consommateurs qui demandent l’événement reçoivent une notification.
    -   En cas de suppression d’un événement, WMI déclenche [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).
    -   Si vous vous abonnez à cet événement, il retourne l’événement qui est supprimé, et une référence à [**\_ \_ EventConsumer**](--eventconsumer.md) représente le consommateur qui a échoué.
    -   En cas de défaillance d’un consommateur, WMI déclenche [**\_ \_ ConsumerFailureEvent**](--consumerfailureevent.md), qui peut contenir plus d’informations dans les propriétés **ErrorCode**, **ErrorDescription** et **ErrorObject** .

    Pour plus d’informations, consultez [liaison d’un filtre d’événements à un consommateur logique](binding-an-event-filter-with-a-logical-consumer.md).

## <a name="example"></a>Exemple

L’exemple suivant montre le fichier MOF pour une instance de [**NTEventLogEventConsumer**](nteventlogeventconsumer.md). une fois que vous avez compilé ce fichier MOF, toute tentative de création, de suppression ou de modification d’une valeur dans le chemin d’accès au registre **HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run** enregistre une entrée dans le journal des événements de l’Application, sous la source « WSH ».


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Réception des événements en toute sécurité](receiving-events-securely.md)
</dt> </dl>

 

 
