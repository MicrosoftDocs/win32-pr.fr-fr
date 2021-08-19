---
description: Le consommateur standard implémenté par la classe ActiveScriptEventConsumer permet à un ordinateur d’exécuter un script et de prendre des mesures lorsque des événements importants se produisent pour s’assurer qu’un ordinateur peut détecter et résoudre les problèmes automatiquement.
ms.assetid: 0d2ac139-3e2b-4089-ae9c-289d376e27a2
ms.tgt_platform: multiple
title: Exécution d’un script basé sur un événement
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b5950ae8a4e7260932fd4df559a73f3abea2bfaf7722444db0b92470649dd312
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816737"
---
# <a name="running-a-script-based-on-an-event"></a>Exécution d’un script basé sur un événement

Le consommateur standard implémenté par la classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) permet à un ordinateur d’exécuter un script et de prendre des mesures lorsque des événements importants se produisent pour s’assurer qu’un ordinateur peut détecter et résoudre les problèmes automatiquement.

Ce consommateur est chargé par défaut dans l’espace de noms de l' **\\ abonnement racine** .

Vous pouvez configurer les performances de toutes les instances de [**ActiveScriptEventConsumer**](activescripteventconsumer.md) sur un système en définissant les valeurs de la propriété **timeout** ou **MaximumScripts** dans une seule instance de [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md).

La procédure de base pour l’utilisation de consommateurs standard est toujours la même, et se trouve dans la [surveillance et la réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md). La procédure suivante, qui ajoute à la procédure de base, est spécifique à la classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) et décrit comment créer un consommateur d’événements qui exécute un script.

> [!Caution]  
> La classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) a des contraintes de sécurité spéciales. Ce consommateur standard doit être configuré par un membre local du groupe Administrateurs sur l’ordinateur local. Si vous utilisez un compte de domaine pour créer l’abonnement, le compte LocalSystem doit disposer des autorisations nécessaires sur le domaine pour vérifier que le créateur est membre du groupe Administrateurs local.

 

La procédure suivante décrit comment créer un consommateur d’événements qui exécute un script.

**Pour créer un consommateur d’événements qui exécute un script**

1.  Écrivez le script à exécuter lorsqu’un événement se produit.

    Vous pouvez écrire le script dans n’importe quel langage, mais assurez-vous qu’un moteur de script pour le langage que vous choisissez est installé sur votre ordinateur. Le script n’a pas besoin d’utiliser les objets de script WMI.

    Seul un administrateur peut configurer un consommateur de script et le script s’exécute sous les informations d’identification LocalSystem, ce qui offre aux consommateurs des fonctionnalités étendues, à l’exception de l’accès réseau. Toutefois, le script n’a pas accès à des données d’ouverture de session utilisateur spécifiques, par exemple, des variables d’environnement et des partages réseau.

2.  Dans le fichier format MOF (MOF), créez une instance de [**ActiveScriptEventConsumer**](activescripteventconsumer.md) pour recevoir les événements que vous demandez dans la requête.

    Vous pouvez placer le texte du script dans **ScriptText**, ou vous pouvez spécifier le chemin d’accès et le nom de fichier du script dans **ScriptFileName**. Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](designing-managed-object-format--mof--classes.md).

3.  Créez une instance de [**\_ \_ EventFilter**](--eventfilter.md), nommez-la, puis créez une requête pour spécifier le type d’événement, qui déclenche l’exécution du script.

    Pour plus d’informations, consultez [interrogation avec WQL](querying-with-wql.md).

4.  Créez une instance de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) pour associer le filtre à l’instance de [**ActiveScriptEventConsumer**](activescripteventconsumer.md).
5.  Compilez le fichier MOF à l’aide de [**Mofcomp.exe**](mofcomp.md).

Les exemples de la section suivante présentent deux façons d’implémenter un script piloté par les événements. Le premier exemple utilise un script défini dans un fichier externe, et le deuxième exemple utilise un script intégré au code MOF. Les exemples se trouvent dans du code MOF, mais vous pouvez créer des instances par programme à l’aide [de l’API de script pour WMI](scripting-api-for-wmi.md) ou de l' [API com pour WMI](com-api-for-wmi.md).

## <a name="example-using-an-external-script"></a>Exemple utilisant un script externe

La procédure suivante décrit comment utiliser l’exemple de script externe.

**Pour utiliser l’exemple de script externe**

1.  Créez un fichier nommé c : \\Asec.vbs, puis copiez le script dans cet exemple dans celui-ci.
2.  Copiez la liste MOF dans un fichier texte et enregistrez-la avec une extension. mof.
3.  Dans une fenêtre d’invite de commandes, compilez le fichier MOF à l’aide de la commande suivante.

    Fichier **mofcomp** ** * *. mof**

4.  Exécutez la calculatrice, qui crée un processus de calc.exe. Attendez plus de cinq secondes, fermez la fenêtre calculatrice, puis recherchez \\ un fichier nommé ASEC. log dans le répertoire C :.

    Le texte suivant est similaire au texte qui sera contenu dans le fichier ASEC. log.

    ``` syntax
    Time: 12/31/2002 2:56:33 PM; Entry made by: ASEC
    Application closed. UserModeTime:  1562500; 
    KernelModeTime: 3125000 [hundreds of nanoseconds]
    ```

L’exemple de code VBScript suivant montre le script qui est appelé lorsqu’un événement est reçu par le consommateur permanent. L’objet **TargetEvent** est une instance [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md) , de sorte qu’il possède une propriété nommée **TargetInstance**, qui est une instance de [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) utilisée pour déclencher l’événement. La classe de **\_ processus Win32** a les propriétés **UserModeTime** et **KernelModeTime** qui sont placées dans le fichier journal créé par le script.


```VB
' asec.vbs script
Dim objFS, objFile
Set objFS = CreateObject("Scripting.FileSystemObject")
Set objFile = objFS.OpenTextFile("C:\ASEC.log", 8, true)
objFile.WriteLine "Time: " & Now & "; Entry made by: ASEC"

objFile.WriteLine "Application closed. UserModeTime:  " & _
    TargetEvent.TargetInstance.UserModeTime & _
    "; KernelModeTime: " & _
    TargetEvent.TargetInstance.KernelModeTime & _
    " [hundreds of nanoseconds]"
objFile.Close
```



L’exemple de code MOF suivant appelle le script lorsqu’un événement est reçu. Il crée le filtre, le consommateur et la liaison entre eux dans l’espace de noms de l' **\\ abonnement racine** .

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $Cons
{
    Name = "ASEC";
    ScriptingEngine = "VBScript";
    ScriptFileName = "c:\\asec2.vbs";
};

instance of __EventFilter as $Filt
{
    Name = "EF";
    Query = "SELECT * FROM __InstanceDeletionEvent WITHIN 5 "
        "WHERE TargetInstance ISA \"Win32_Process\" "
        "AND TargetInstance.Name = \"calc.exe\"";
    QueryLanguage = "WQL";
    EventNamespace = "root\\cimv2";
};

instance of __FilterToConsumerBinding
{
    Filter = $Filt;
    Consumer = $Cons;
};
```

## <a name="example-using-inline-script"></a>Exemple utilisant un script inline

La procédure suivante décrit comment utiliser l’exemple de script inline.

**Pour utiliser l’exemple de script inline**

1.  Copiez la liste MOF de cette section dans un fichier texte, puis enregistrez-la avec une extension. mof.
2.  Dans une fenêtre d’invite de commandes, compilez le fichier MOF à l’aide de la commande suivante.

    Fichier **mofcomp** ** * *. mof**

L’exemple de code MOF suivant crée le filtre, le consommateur et la liaison entre eux et contient également le script inline.

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $Cons
{
    Name = "ASEC";
    ScriptingEngine = "VBScript";
    
    ScriptText =
        "Dim objFS, objFile\n"
        "Set objFS = CreateObject(\"Scripting.FileSystemObject\")\n"
        "Set objFile = objFS.OpenTextFile(\"C:\\ASEC.log\","
        " 8, true)\nobjFile.WriteLine \"Time: \" & Now & \";"
        " Entry made by: ASEC\"\nobjFile.WriteLine"
        " \"Application closed. UserModeTime:  \" & "
        "TargetEvent.TargetInstance.UserModeTime &_\n"
        "\"; KernelModeTime: \" & "
        "TargetEvent.TargetInstance.KernelModeTime "
        "& \" [hundreds of nanoseconds]\"\n"
        "objFile.Close\n";
};

instance of __EventFilter as $Filt
{
    Name = "EF";
    Query = "SELECT * FROM __InstanceDeletionEvent WITHIN 5 "
        "WHERE TargetInstance ISA \"Win32_Process\" "
        "AND TargetInstance.Name = \"calc.exe\"";
    QueryLanguage = "WQL";
    EventNamespace = "root\\cimv2";
};

instance of __FilterToConsumerBinding
{
    Filter = $Filt;
    Consumer = $Cons;
};
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
