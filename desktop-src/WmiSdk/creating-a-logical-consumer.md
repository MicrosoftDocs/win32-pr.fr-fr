---
description: Un consommateur logique est une instance d’une classe de consommateur d’événements permanente.
ms.assetid: fd984de8-0fe6-4b32-8e8c-4e2db84b4cc0
ms.tgt_platform: multiple
title: Création d’un consommateur logique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dcbd62f2eee57a9e254d5700344d7b8da414469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520148"
---
# <a name="creating-a-logical-consumer"></a>Création d’un consommateur logique

Un consommateur logique est une instance d’une classe de consommateur d’événements permanente. L’objectif principal d’un consommateur logique est de fournir au consommateur physique les paramètres des activités effectuées par le consommateur physique. Pour plus d’informations, consultez [création d’une classe de consommateur d’événements permanent](creating-a-new-permanent-event-consumer-class.md). Le consommateur permanent doit avoir le même [**CreatorSID**](--eventconsumer.md) dans les instances de consommateur, de filtre et de liaison. Pour plus d’informations, consultez [réception d’événements en toute sécurité](receiving-events-securely.md). Pour obtenir un exemple d’utilisation d’un consommateur logique, consultez [exécution d’un script basé sur un événement](running-a-script-based-on-an-event.md), qui illustre l’utilisation de la classe de consommateur standard [**ActiveScriptEventConsumer**](activescripteventconsumer.md) pour configurer un consommateur permanent.

La procédure suivante décrit comment créer un consommateur logique.

**Pour créer un consommateur logique**

1.  Créez une instance de votre classe de consommateur permanente.
2.  Remplissez les propriétés de l’instance avec les paramètres de l’action que le consommateur physique doit effectuer.

L’exemple de code MOF suivant décrit un consommateur logique qui contient un script.

``` syntax
#pragma namespace("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $CONSUMER
{
    Name = "MyConsumerName";
    ScriptingEngine = "VBScript";
    ScriptText = 

        "Set objFS = CreateObject(\"Scripting.FileSystemObject\")\n"
        "Set objFile = objFS.OpenTextFile(\"C:\\\\ASEC.log\", 8, true);\n"
        "objFile.WriteLine \"Time: \" + new Date() + \";\n"
        "objFile.WriteLine \"Entry made by: \\\"ActiveScript\\\"\";\n"
        "objFile.Close\n";
    
    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

Après avoir créé le consommateur logique, vous devez lier chaque filtre à un filtre d’événements pour affecter l’action à un événement particulier. Pour plus d’informations, consultez [création d’un filtre d’événements](creating-an-event-filter.md).

 

 



