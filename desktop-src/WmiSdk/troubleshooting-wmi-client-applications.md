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
ms.openlocfilehash: 0a84646aa42cd0ccd649e3937f0eba257343e9a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203954"
---
# <a name="troubleshooting-wmi-client-applications"></a><span data-ttu-id="4eb6a-103">Résolution des problèmes des applications clientes WMI</span><span class="sxs-lookup"><span data-stu-id="4eb6a-103">Troubleshooting WMI Client Applications</span></span>

<span data-ttu-id="4eb6a-104">WMI contient un ensemble de classes permettant de [résoudre les problèmes liés](wmi-troubleshooting-classes.md) aux applications clientes qui utilisent des fournisseurs WMI.</span><span class="sxs-lookup"><span data-stu-id="4eb6a-104">WMI contains a set of classes for [troubleshooting](wmi-troubleshooting-classes.md) client applications that use WMI providers.</span></span> <span data-ttu-id="4eb6a-105">Les classes d’événements de dépannage sont associées aux classes d’événements WMI, ce qui vous permet de suivre l’exécution de votre application à l’aide d’un journal des événements de résolution des problèmes capturés.</span><span class="sxs-lookup"><span data-stu-id="4eb6a-105">The troubleshooting event classes are coupled to WMI event classes, such that you can track your application execution using a log of captured troubleshooting events.</span></span>

<span data-ttu-id="4eb6a-106">La liste suivante contient des exemples de classes d’événements de dépannage :</span><span class="sxs-lookup"><span data-stu-id="4eb6a-106">The following list contains examples of troubleshooting event classes:</span></span>

-   [<span data-ttu-id="4eb6a-107">**Msft \_ wmiprovider \_ ExecMethodAsyncEvent \_**</span><span class="sxs-lookup"><span data-stu-id="4eb6a-107">**Msft\_WmiProvider\_ExecMethodAsyncEvent\_Pre**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-pre)

    <span data-ttu-id="4eb6a-108">Déclenché avant que WMI n’appelle [**IWbemServices :: ExecMethodAsync ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) sur le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4eb6a-108">Raised before WMI calls [**IWbemServices::ExecMethodAsync()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) on the provider.</span></span>

-   [<span data-ttu-id="4eb6a-109">**\_Publication wmiprovider \_ ExecMethodAsyncEvent \_ msft**</span><span class="sxs-lookup"><span data-stu-id="4eb6a-109">**Msft\_WmiProvider\_ExecMethodAsyncEvent\_Post**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-post)

    <span data-ttu-id="4eb6a-110">Déclenché après que WMI a appelé [**IWbemServices :: ExecMethodAsync ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) sur le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4eb6a-110">Raised after WMI calls [**IWbemServices::ExecMethodAsync()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) on the provider.</span></span>

<span data-ttu-id="4eb6a-111">La procédure suivante montre comment résoudre les problèmes d’exécution de l’application.</span><span class="sxs-lookup"><span data-stu-id="4eb6a-111">The following procedure shows how to troubleshoot application execution.</span></span>

<span data-ttu-id="4eb6a-112">**Pour configurer la résolution des problèmes WMI**</span><span class="sxs-lookup"><span data-stu-id="4eb6a-112">**To set up WMI troubleshooting**</span></span>

1.  <span data-ttu-id="4eb6a-113">Créez et compilez un fichier MOF pour utiliser le consommateur d’événements de journalisation WMI.</span><span class="sxs-lookup"><span data-stu-id="4eb6a-113">Create and compile a MOF file to use the WMI logging event consumer.</span></span>
2.  <span data-ttu-id="4eb6a-114">Exécutez votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="4eb6a-114">Run your client application.</span></span>
3.  <span data-ttu-id="4eb6a-115">Affichez le fichier journal de résolution des problèmes pour tous les événements d’échec et d’opération du fournisseur, puis analysez le journal pour diagnostiquer les problèmes de client que vous rencontrez.</span><span class="sxs-lookup"><span data-stu-id="4eb6a-115">View the troubleshooting log file for all provider operation and failure events, and analyze the log to diagnose the client problems you are encountering.</span></span>

<span data-ttu-id="4eb6a-116">Une autre approche de résolution des problèmes consiste à afficher la liste des fournisseurs actuellement dans le cache de l’ordinateur, en énumérant les [**\_ fournisseurs msft**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) dans l’espace de noms **\\ cimv2 racine** .</span><span class="sxs-lookup"><span data-stu-id="4eb6a-116">Another troubleshooting approach is to view the list of providers currently in the computer cache, by enumerating [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) in the **root\\cimv2** namespace.</span></span> <span data-ttu-id="4eb6a-117">Cette classe contient des méthodes qui vous permettent de charger et de décharger des fournisseurs à des fins de débogage ou de configuration.</span><span class="sxs-lookup"><span data-stu-id="4eb6a-117">There are methods in this class that enable you to load and unload providers for debugging or setup purposes.</span></span>

<span data-ttu-id="4eb6a-118">L’exemple de code suivant utilise le consommateur d’événements de journalisation WMI pour capturer tous les événements de la classe d’événements parent, capturant ainsi tous les événements d’opération du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4eb6a-118">The following code example uses the WMI logging event consumer to capture all events of the parent event class, thus capturing all provider operation events.</span></span>

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

<span data-ttu-id="4eb6a-119">Lorsque les messages d’erreur indiquent un échec de chargement du fournisseur, utilisez [**msft \_ wmiprovider \_ LoadOperationFailureEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent) pour identifier le fournisseur à l’origine de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4eb6a-119">When error messages indicate provider load failure, use [**MSFT\_WmiProvider\_LoadOperationFailureEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent) to identify which provider caused the fault.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4eb6a-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4eb6a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4eb6a-121">Résolution des problèmes WMI</span><span class="sxs-lookup"><span data-stu-id="4eb6a-121">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="4eb6a-122">Classes de résolution des problèmes WMI</span><span class="sxs-lookup"><span data-stu-id="4eb6a-122">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
