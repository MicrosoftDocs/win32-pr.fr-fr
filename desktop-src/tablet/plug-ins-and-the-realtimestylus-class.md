---
description: L’objet RealTimeStylus est conçu pour fournir un accès en temps réel au flux de données à partir du stylet du Tablet PC.
ms.assetid: 7217e2d5-ca62-4d65-bf22-9511b367c798
title: Plug-ins et classe RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc522eb6f73b384d0c2c1846edb2b20cdcb89d34ef42633b08ca865950c8ce16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119843379"
---
# <a name="plug-ins-and-the-realtimestylus-class"></a>Plug-ins et classe RealTimeStylus

L’objet [**RealTimeStylus**](realtimestylus-class.md) est conçu pour fournir un accès en temps réel au flux de données à partir du stylet du Tablet PC. Les plug-ins, objets qui implémentent l’interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) ou [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) , peuvent être ajoutés à un objet **RealTimeStylus** . Les plug-ins synchrones sont généralement appelés directement par l’objet **RealTimeStylus** sur un thread de priorité élevée, tandis que les plug-ins asynchrones sont généralement appelés sur le thread d’interface utilisateur de l’application. Créez ou utilisez des plug-ins synchrones pour les tâches qui nécessitent un accès en temps réel au flux de données et qui font l’objet d’une indemande de calcul, comme le filtrage de paquets. Créez ou utilisez des plug-ins asynchrones pour les tâches qui ne nécessitent pas d’accès en temps réel au flux de données, telles que la collecte d’encres.

Certaines tâches peuvent nécessiter un calcul exigeant un accès en temps réel au flux de données, par exemple la reconnaissance de mouvement à multitrait. Pour répondre à ces besoins, les API StylusInput fournissent un modèle [**RealTimeStylus**](realtimestylus-class.md) monté en cascade qui vous permet d’utiliser deux objets **RealTimeStylus** , chacun s’exécutant sur son propre thread. Pour plus d’informations sur le modèle **RealTimeStylus** monté en cascade, consultez [le modèle RealTimeStylus monté en cascade](the-cascaded-realtimestylus-model.md).

Les interfaces [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) et [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) définissent les mêmes méthodes. Ces méthodes permettent à l’objet [**RealTimeStylus**](realtimestylus-class.md) de passer les données de stylet à chaque plug-in, qu’il s’agisse d’un plug-in asynchrone ou synchrone. Les propriétés [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms824752(v=msdn.10)) et [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms824769(v=msdn.10)) permettent à chaque plug-in de s’abonner à des données spécifiques dans le flux de données de stylet de tablette. Un plug-in doit uniquement s’abonner aux données nécessaires à l’exécution de sa tâche, ce qui réduit les demandes de performances. Pour plus d’informations sur les threads et la classe **RealTimeStylus** , consultez [Considérations sur les threads pour les API StylusInput](threading-considerations-for-the-stylusinput-apis.md).

L’objet [**RealTimeStylus**](realtimestylus-class.md) utilise les objets de l’espace de noms [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) pour passer les données de stylet à ses plug-ins. L' **RealTimeStylus** intercepte également les exceptions levées par les plug-ins. Lorsque l' **RealTimeStylus** intercepte les exceptions, il avertit les plug-ins en appelant la méthode [IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) ou [IStylusAsyncPlugin. Error](/previous-versions/ms824771(v=msdn.10)) . Pour plus d’informations sur l’utilisation des données de plug-in, consultez [données de plug-in et classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md) . Pour plus d’informations sur la gestion des erreurs, consultez [considérations relatives à la gestion des erreurs pour les API StylusInput](error-handling-considerations-for-the-stylusinput-apis.md) et la section données d’erreur des données de plug-in et de la classe RealTimeStylus.

> [!Note]  
> Au moins un plug-in doit être attaché à l’objet [**RealTimeStylus**](realtimestylus-class.md) pour que l’objet **RealTimeStylus** puisse être activé.

 

Les rubriques suivantes décrivent certaines catégories courantes de plug-ins.

-   [Plug-ins de collection d’encres](ink-collection-plug-ins.md)
-   [Plug-ins de rendu dynamique](dynamic-renderer-plug-ins.md)
-   [Plug-ins de reconnaissance](recognizer-plug-ins.md)

## <a name="special-considerations"></a>Considérations spéciales

En raison de la nature complexe de l’objet [**RealTimeStylus**](realtimestylus-class.md) , vous devez prendre note des points suivants.

L’objet [**RealTimeStylus**](realtimestylus-class.md) lève une exception si un plug-in modifie la collection de plug-ins à laquelle il est attaché. Cela se produit uniquement lorsque le plug-in le fait pendant qu’il est appelé par l’objet **RealTimeStylus** en tant que membre de cette collection.

L’exemple C suivant \# est du code qui provoque la levée d’une exception par l’objet [**RealTimeStylus**](realtimestylus-class.md) .


```csharp
using Microsoft.Ink;
using Microsoft.StylusInput;
using Microsoft.StylusInput.PluginData;

// ...
public class thePlugin : Microsoft.StylusInput.IStylusAsyncPlugin
{
    // ...

    // Called when a system gesture occurs.
    public void SystemGesture(RealTimeStylus sender, SystemGestureData data)
    {
        // The following line will cause the realtime stylus that calls this method
        // to throw an exception.
        sender.Dispose();
    }
    
    // ...
}
```



L’objet [**RealTimeStylus**](realtimestylus-class.md) lève une exception si un plug-in appelle la méthode [dispose](/previous-versions/ms825891(v=msdn.10)) de l’objet **RealTimeStylus** . Cela se produit uniquement lorsque le plug-in le fait pendant qu’il est appelé par l’objet **RealTimeStylus** .

L’exemple C suivant \# est du code qui provoque la levée d’une exception par l’objet [**RealTimeStylus**](realtimestylus-class.md) .


```csharp
using Microsoft.Ink;
using Microsoft.StylusInput;
using Microsoft.StylusInput.PluginData;

// ...
public class thePlugin : Microsoft.StylusInput.IStylusAsyncPlugin
{
    Microsoft.StylusInput.GestureRecognizer theGestureRecognizer;

    // ...

    // Called when a system gesture occurs.
    public void SystemGesture(RealTimeStylus sender, SystemGestureData data)
    {
        // The following line will cause the realtime stylus that calls this method
        // to throw an exception.
        sender.AsyncPluginCollection.Add(this.theGestureRecognizer);
    }
    
    // ...
}
```



Les collections de plug-ins peuvent être modifiées lorsque l’objet [**RealTimeStylus**](realtimestylus-class.md) est activé ; Toutefois, cela peut rendre le comportement de votre application plus difficile à prédire. Lorsqu’un plug-in est ajouté alors que l’objet **RealTimeStylus** est activé, l’objet **RealTimeStylus** appelle la méthode [IStylusAsyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) ou IStylusSyncPlugin. [RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) du plug-in. Quand un plug-in est supprimé alors que l’objet **RealTimeStylus** est activé, l’objet **RealTimeStylus** appelle la méthode [IStylusAsyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) ou IStylusSyncPlugin. [RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) du plug-in. Cela permet au plug-in de conserver son état approprié sans avoir à vérifier la propriété [Enabled](/previous-versions/ms824832(v=msdn.10)) de l’objet **RealTimeStylus** .

Quand un plug-in est ajouté alors que l’objet [**RealTimeStylus**](realtimestylus-class.md) est activé, les données de plug-in reçues par le plug-in peuvent ne pas contenir suffisamment d’informations pour établir correctement le contexte des données initiales. Par exemple, le plug-in qui vient d’être ajouté peut commencer à recevoir des données de paquets à partir d’un stylet mi-course. De même, lorsqu’un plug-in est supprimé alors que l’objet **RealTimeStylus** est activé, les données de plug-in que le plug-in a reçues sont peut-être insuffisantes pour terminer le traitement des données.

> [!Note]  
> Pour la stabilité globale, réinitialisez l’état interne d’un plug-in lorsque sa méthode [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) ou [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) est appelée.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèle RealTimeStylus monté en cascade](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[Considérations relatives à la gestion des erreurs pour les API StylusInput](error-handling-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[Données de plug-in et classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[Considérations relatives aux threads pour les API StylusInput](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
