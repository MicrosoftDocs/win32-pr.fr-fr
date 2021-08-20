---
description: WMI contient un ensemble de classes permettant de résoudre les problèmes liés aux applications clientes qui utilisent des fournisseurs WMI.
ms.assetid: f69b360a-2c24-4776-bcda-b51edde0dcde
ms.tgt_platform: multiple
title: Résolution des problèmes des applications clientes WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7fb9eb8c438faab8915691ee2c9c8a4c77d247c6802f8f114683a79d2833bd15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050027"
---
# <a name="troubleshooting-wmi-client-applications"></a>Résolution des problèmes des applications clientes WMI

WMI contient un ensemble de classes permettant de [résoudre les problèmes liés](wmi-troubleshooting-classes.md) aux applications clientes qui utilisent des fournisseurs WMI. Les classes d’événements de dépannage sont associées aux classes d’événements WMI, ce qui vous permet de suivre l’exécution de votre application à l’aide d’un journal des événements de résolution des problèmes capturés.

La liste suivante contient des exemples de classes d’événements de dépannage :

-   [**Msft \_ wmiprovider \_ ExecMethodAsyncEvent \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-pre)

    Déclenché avant que WMI n’appelle [**IWbemServices :: ExecMethodAsync ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) sur le fournisseur.

-   [**\_Publication wmiprovider \_ ExecMethodAsyncEvent \_ msft**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-post)

    Déclenché après que WMI a appelé [**IWbemServices :: ExecMethodAsync ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) sur le fournisseur.

La procédure suivante montre comment résoudre les problèmes d’exécution de l’application.

**Pour configurer la résolution des problèmes WMI**

1.  Créez et compilez un fichier MOF pour utiliser le consommateur d’événements de journalisation WMI.
2.  Exécutez votre application cliente.
3.  Affichez le fichier journal de résolution des problèmes pour tous les événements d’échec et d’opération du fournisseur, puis analysez le journal pour diagnostiquer les problèmes de client que vous rencontrez.

Une autre approche de résolution des problèmes consiste à afficher la liste des fournisseurs actuellement dans le cache de l’ordinateur, en énumérant les [**\_ fournisseurs msft**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) dans l’espace de noms **\\ cimv2 racine** . Cette classe contient des méthodes qui vous permettent de charger et de décharger des fournisseurs à des fins de débogage ou de configuration.

L’exemple de code suivant utilise le consommateur d’événements de journalisation WMI pour capturer tous les événements de la classe d’événements parent, capturant ainsi tous les événements d’opération du fournisseur.

``` syntax
#pragma autorecover
#pragma namespace("\\\\.\\root\\subscription")

instance of __EventFilter as $Filter
{
  Name = "ProviderOperationEvents" ;
  EventNamespace = "root\\cimv2" ;
  Query = "SELECT * FROM MSFT_WmiProvider_OperationEvent" ;
  QueryLanguage = "WQL" ;
} ;

Instance of LogFileEventConsumer as $Consumer
{
  Name = "ProviderOperationEvents" ;
  FileName = "C:\\test.txt" ;
  Text = "Operation - %__TEXT%" ;
} ;

instance of __FilterToConsumerBinding
{
  Filter = $Filter ;
  Consumer = $Consumer ;
  MaintainSecurityContext = TRUE ;
} ;
```

Lorsque les messages d’erreur indiquent un échec de chargement du fournisseur, utilisez [**msft \_ wmiprovider \_ LoadOperationFailureEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent) pour identifier le fournisseur à l’origine de l’erreur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes WMI](wmi-troubleshooting.md)
</dt> <dt>

[Classes de résolution des problèmes WMI](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
