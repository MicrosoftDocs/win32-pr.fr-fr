---
description: La classe CommandLineEventConsumer exécute un programme exécutable spécifié à partir d’une ligne de commande lorsqu’un événement spécifié se produit. Cette classe est un consommateur d’événements standard fourni par WMI.
ms.assetid: b912a4a1-7b1c-43a9-b098-fcfd62a2c2db
ms.tgt_platform: multiple
title: Exécution d’un programme à partir de la ligne de commande en fonction d’un événement
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c499713b3c6496759d94229e291138b0cb07de9e9f35d116eb19b4a7aeb3829
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553967"
---
# <a name="running-a-program-from-the-command-line-based-on-an-event"></a>Exécution d’un programme à partir de la ligne de commande en fonction d’un événement

La classe [**CommandLineEventConsumer**](commandlineeventconsumer.md) exécute un programme exécutable spécifié à partir d’une ligne de commande lorsqu’un événement spécifié se produit. Cette classe est un consommateur d’événements standard fourni par WMI.

Lorsque vous utilisez [**CommandLineEventConsumer**](commandlineeventconsumer.md), vous devez sécuriser l’exécutable que vous souhaitez démarrer. Si l’exécutable ne se trouve pas dans un emplacement sécurisé ou n’est pas sécurisé avec une liste de contrôle d’accès (ACL) forte, un utilisateur sans privilèges d’accès peut remplacer votre exécutable par un autre exécutable. Vous pouvez utiliser les classes [**Win32 \_ LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) ou [**Win32 \_ LogicalShareSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) pour modifier par programmation la sécurité d’un fichier ou d’un partage. Pour plus d’informations, consultez [création d’un descripteur de sécurité pour un nouvel objet en C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

La procédure de base pour utiliser des consommateurs standard est toujours la même et se trouve dans [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md). La procédure suivante ajoute à la procédure de base, est spécifique à la classe [**CommandLineEventConsumer**](commandlineeventconsumer.md) et décrit comment créer un consommateur d’événements qui exécute un programme.

> [!Caution]
>
> La classe [**CommandLineEventConsumer**](commandlineeventconsumer.md) a des contraintes de sécurité spéciales. Ce consommateur standard doit être configuré par un membre local du groupe Administrateurs sur l’ordinateur local. Si vous utilisez un compte de domaine pour créer l’abonnement, le compte LocalSystem doit disposer des autorisations nécessaires sur le domaine pour vérifier que le créateur est membre du groupe Administrateurs local.
>
> [**CommandLineEventConsumer**](commandlineeventconsumer.md) ne peut pas être utilisé pour démarrer un processus qui s’exécute de manière interactive.

 

La procédure suivante décrit comment créer un consommateur d’événements qui exécute un processus à partir d’une ligne de commande.

**Pour créer un consommateur d’événements qui exécute un processus à partir d’une ligne de commande**

1.  Dans le fichier format MOF (MOF), créez une instance de [**CommandLineEventConsumer**](commandlineeventconsumer.md) pour recevoir les événements que vous demandez dans la requête. Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](designing-managed-object-format--mof--classes.md).
2.  Créez une instance de [**\_ \_ EventFilter**](--eventfilter.md) et donnez-lui un nom.
3.  Créez une requête pour spécifier le type d’événement. Pour plus d’informations, consultez [interrogation avec WQL](querying-with-wql.md).
4.  Créez une instance de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) pour associer le filtre à l’instance de [**CommandLineEventConsumer**](commandlineeventconsumer.md).
5.  Compilez votre fichier MOF à l’aide de [**Mofcomp.exe**](mofcomp.md).

## <a name="example"></a>Exemple

L’exemple de code suivant crée une nouvelle classe appelée « MyCmdLineConsumer » pour générer des événements lorsqu’une instance de la nouvelle classe est créée à la fin d’un MOF. L’exemple se trouve dans du code MOF, mais vous pouvez créer des instances par programme à l’aide [de l’API de script pour WMI](scripting-api-for-wmi.md) ou de l' [API com pour WMI](com-api-for-wmi.md).

La procédure suivante décrit comment créer une nouvelle classe appelée MyCmdLineConsumer.

**Pour créer une nouvelle classe appelée MyCmdLineConsumer**

1.  Créez le fichier de \\test.bat c : cmdline \_ avec une commande qui exécute un programme visible, tel que « calc.exe ».
2.  Copiez le fichier MOF dans un fichier texte et enregistrez-le avec une extension. mof.
3.  Dans un Fenêtre Commande, compilez le fichier MOF à l’aide de la commande suivante : **mofcomp nom_fichier. mof**.

> [!Note]  
> Le programme spécifié dans cmdline \_test.bat doit s’exécuter.

 

``` syntax
// Set the namespace as root\subscription.
// The CommandLineEventConsumer is already compiled
// in the root\subscription namespace. 
#pragma namespace ("\\\\.\\Root\\subscription")

class MyCmdLineConsumer
{
 [key]string Name;
};

// Create an instance of the command line consumer
// and give it the alias $CMDLINECONSUMER

instance of CommandLineEventConsumer as $CMDLINECONSUMER
{
 Name = "CmdLineConsumer_Example";
 CommandLineTemplate = "c:\\cmdline_test.bat";
 RunInteractively = True;
 WorkingDirectory = "c:\\";
};    

// Create an instance of the event filter
// and give it the alias $CMDLINEFILTER
// The filter queries for instance creation event
// for instances of the MyCmdLineConsumer class

instance of __EventFilter as $CMDLINEFILTER
{
    Name = "CmdLineFilter";
    Query = "SELECT * FROM __InstanceCreationEvent"
        " WHERE TargetInstance.__class = \"MyCmdLineConsumer\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding
// between filter and consumer instances.

instance of __FilterToConsumerBinding
{
     Consumer = $CMDLINECONSUMER;
     Filter = $CMDLINEFILTER;
};

// Create an instance of this class right now. 
// The commands in c:\\cmdline_test.bat execute
// as the result of creating the instance
// of MyCmdLineConsumer.
 
instance of MyCmdLineConsumer
{
     Name = "CmdLineEventConsumer test";
};
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
