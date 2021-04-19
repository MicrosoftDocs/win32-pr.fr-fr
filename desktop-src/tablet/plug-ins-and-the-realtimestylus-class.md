---
description: L’objet RealTimeStylus est conçu pour fournir un accès en temps réel au flux de données à partir du stylet du Tablet PC.
ms.assetid: 7217e2d5-ca62-4d65-bf22-9511b367c798
title: Plug-ins et classe RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08177c5f4110897fa1887857788766f67ae38167
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521992"
---
# <a name="plug-ins-and-the-realtimestylus-class"></a><span data-ttu-id="947da-103">Plug-ins et classe RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="947da-103">Plug-ins and the RealTimeStylus Class</span></span>

<span data-ttu-id="947da-104">L’objet [**RealTimeStylus**](realtimestylus-class.md) est conçu pour fournir un accès en temps réel au flux de données à partir du stylet du Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="947da-104">The [**RealTimeStylus**](realtimestylus-class.md) object is designed to provide real-time access to the data stream from the tablet pen.</span></span> <span data-ttu-id="947da-105">Les plug-ins, objets qui implémentent l’interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) ou [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) , peuvent être ajoutés à un objet **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="947da-105">Plug-ins, objects that implement the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) or [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interface, can be added to a **RealTimeStylus** object.</span></span> <span data-ttu-id="947da-106">Les plug-ins synchrones sont généralement appelés directement par l’objet **RealTimeStylus** sur un thread de priorité élevée, tandis que les plug-ins asynchrones sont généralement appelés sur le thread d’interface utilisateur de l’application.</span><span class="sxs-lookup"><span data-stu-id="947da-106">Synchronous plug-ins are generally called directly by the **RealTimeStylus** object on a high-priority thread, while asynchronous plug-ins are generally called on the application's user interface (UI) thread.</span></span> <span data-ttu-id="947da-107">Créez ou utilisez des plug-ins synchrones pour les tâches qui nécessitent un accès en temps réel au flux de données et qui font l’objet d’une indemande de calcul, comme le filtrage de paquets.</span><span class="sxs-lookup"><span data-stu-id="947da-107">Create or use synchronous plug-ins for tasks that require real-time access to the data stream and are computationally undemanding, such as packet filtering.</span></span> <span data-ttu-id="947da-108">Créez ou utilisez des plug-ins asynchrones pour les tâches qui ne nécessitent pas d’accès en temps réel au flux de données, telles que la collecte d’encres.</span><span class="sxs-lookup"><span data-stu-id="947da-108">Create or use asynchronous plug-ins for tasks that do not require real-time access to the data stream, such as ink collection.</span></span>

<span data-ttu-id="947da-109">Certaines tâches peuvent nécessiter un calcul exigeant un accès en temps réel au flux de données, par exemple la reconnaissance de mouvement à multitrait.</span><span class="sxs-lookup"><span data-stu-id="947da-109">Certain tasks may be computationally demanding yet require real-time access to the data stream, such as multistroke gesture recognition.</span></span> <span data-ttu-id="947da-110">Pour répondre à ces besoins, les API StylusInput fournissent un modèle [**RealTimeStylus**](realtimestylus-class.md) monté en cascade qui vous permet d’utiliser deux objets **RealTimeStylus** , chacun s’exécutant sur son propre thread.</span><span class="sxs-lookup"><span data-stu-id="947da-110">To address these needs, the StylusInput APIs provide a cascaded [**RealTimeStylus**](realtimestylus-class.md) model that allows you to use two **RealTimeStylus** objects, each running on its own thread.</span></span> <span data-ttu-id="947da-111">Pour plus d’informations sur le modèle **RealTimeStylus** monté en cascade, consultez [le modèle RealTimeStylus monté en cascade](the-cascaded-realtimestylus-model.md).</span><span class="sxs-lookup"><span data-stu-id="947da-111">For more information about the cascaded **RealTimeStylus** model, see [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).</span></span>

<span data-ttu-id="947da-112">Les interfaces [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) et [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) définissent les mêmes méthodes.</span><span class="sxs-lookup"><span data-stu-id="947da-112">Both the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) and [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interfaces define the same methods.</span></span> <span data-ttu-id="947da-113">Ces méthodes permettent à l’objet [**RealTimeStylus**](realtimestylus-class.md) de passer les données de stylet à chaque plug-in, qu’il s’agisse d’un plug-in asynchrone ou synchrone.</span><span class="sxs-lookup"><span data-stu-id="947da-113">These methods allow the [**RealTimeStylus**](realtimestylus-class.md) object to pass the pen data to each plug-in, regardless of whether it is an asynchronous or synchronous plug-in.</span></span> <span data-ttu-id="947da-114">Les propriétés [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms824752(v=msdn.10)) et [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms824769(v=msdn.10)) permettent à chaque plug-in de s’abonner à des données spécifiques dans le flux de données de stylet de tablette.</span><span class="sxs-lookup"><span data-stu-id="947da-114">The [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms824752(v=msdn.10)) and [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms824769(v=msdn.10)) properties allow each plug-in to subscribe to specific data in the tablet pen data stream.</span></span> <span data-ttu-id="947da-115">Un plug-in doit uniquement s’abonner aux données nécessaires à l’exécution de sa tâche, ce qui réduit les demandes de performances.</span><span class="sxs-lookup"><span data-stu-id="947da-115">A plug-in should only subscribe to the data necessary to perform its task, minimizing performance demands.</span></span> <span data-ttu-id="947da-116">Pour plus d’informations sur les threads et la classe **RealTimeStylus** , consultez [Considérations sur les threads pour les API StylusInput](threading-considerations-for-the-stylusinput-apis.md).</span><span class="sxs-lookup"><span data-stu-id="947da-116">For more information about threading and the **RealTimeStylus** class, see [Threading Considerations for the StylusInput APIs](threading-considerations-for-the-stylusinput-apis.md).</span></span>

<span data-ttu-id="947da-117">L’objet [**RealTimeStylus**](realtimestylus-class.md) utilise les objets de l’espace de noms [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) pour passer les données de stylet à ses plug-ins. L' **RealTimeStylus** intercepte également les exceptions levées par les plug-ins. Lorsque l' **RealTimeStylus** intercepte les exceptions, il avertit les plug-ins en appelant la méthode [IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) ou [IStylusAsyncPlugin. Error](/previous-versions/ms824771(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="947da-117">The [**RealTimeStylus**](realtimestylus-class.md) object uses objects in the [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) namespace to pass the pen data to its plug-ins. The **RealTimeStylus** also catches exceptions thrown by plug-ins. When the **RealTimeStylus** catches exceptions, it notifies the plug-ins by calling the [IStylusSyncPlugin.Error](/previous-versions/ms824754(v=msdn.10)) or [IStylusAsyncPlugin.Error](/previous-versions/ms824771(v=msdn.10)) method.</span></span> <span data-ttu-id="947da-118">Pour plus d’informations sur l’utilisation des données de plug-in, consultez [données de plug-in et classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="947da-118">For more information about using plug-in data, see [Plug-in Data and the RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md) Class.</span></span> <span data-ttu-id="947da-119">Pour plus d’informations sur la gestion des erreurs, consultez [considérations relatives à la gestion des erreurs pour les API StylusInput](error-handling-considerations-for-the-stylusinput-apis.md) et la section données d’erreur des données de plug-in et de la classe RealTimeStylus.</span><span class="sxs-lookup"><span data-stu-id="947da-119">For more information about error handling, see [Error Handling Considerations for the StylusInput APIs](error-handling-considerations-for-the-stylusinput-apis.md) and the Error Data section of Plug-in Data and the RealTimeStylus Class.</span></span>

> [!Note]  
> <span data-ttu-id="947da-120">Au moins un plug-in doit être attaché à l’objet [**RealTimeStylus**](realtimestylus-class.md) pour que l’objet **RealTimeStylus** puisse être activé.</span><span class="sxs-lookup"><span data-stu-id="947da-120">At least one plug-in must be attached to the [**RealTimeStylus**](realtimestylus-class.md) object before the **RealTimeStylus** object can be enabled.</span></span>

 

<span data-ttu-id="947da-121">Les rubriques suivantes décrivent certaines catégories courantes de plug-ins.</span><span class="sxs-lookup"><span data-stu-id="947da-121">The following topics describe some common categories of plug-ins.</span></span>

-   [<span data-ttu-id="947da-122">Plug-ins de collection d’encres</span><span class="sxs-lookup"><span data-stu-id="947da-122">Ink-Collection Plug-ins</span></span>](ink-collection-plug-ins.md)
-   [<span data-ttu-id="947da-123">Plug-ins de rendu dynamique</span><span class="sxs-lookup"><span data-stu-id="947da-123">Dynamic-Renderer Plug-ins</span></span>](dynamic-renderer-plug-ins.md)
-   [<span data-ttu-id="947da-124">Plug-ins de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="947da-124">Recognizer Plug-ins</span></span>](recognizer-plug-ins.md)

## <a name="special-considerations"></a><span data-ttu-id="947da-125">Considérations spéciales</span><span class="sxs-lookup"><span data-stu-id="947da-125">Special Considerations</span></span>

<span data-ttu-id="947da-126">En raison de la nature complexe de l’objet [**RealTimeStylus**](realtimestylus-class.md) , vous devez prendre note des points suivants.</span><span class="sxs-lookup"><span data-stu-id="947da-126">Because of the complex nature of the [**RealTimeStylus**](realtimestylus-class.md) object, you should take note of the following.</span></span>

<span data-ttu-id="947da-127">L’objet [**RealTimeStylus**](realtimestylus-class.md) lève une exception si un plug-in modifie la collection de plug-ins à laquelle il est attaché.</span><span class="sxs-lookup"><span data-stu-id="947da-127">The [**RealTimeStylus**](realtimestylus-class.md) object throws an exception if a plug-in modifies the plug-in collection to which it is attached.</span></span> <span data-ttu-id="947da-128">Cela se produit uniquement lorsque le plug-in le fait pendant qu’il est appelé par l’objet **RealTimeStylus** en tant que membre de cette collection.</span><span class="sxs-lookup"><span data-stu-id="947da-128">This happens only when the plug-in does so while it is being called by the **RealTimeStylus** object as a member of that collection.</span></span>

<span data-ttu-id="947da-129">L’exemple C suivant \# est du code qui provoque la levée d’une exception par l’objet [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="947da-129">The following C\# example is code that causes the [**RealTimeStylus**](realtimestylus-class.md) object to throw an exception.</span></span>


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



<span data-ttu-id="947da-130">L’objet [**RealTimeStylus**](realtimestylus-class.md) lève une exception si un plug-in appelle la méthode [dispose](/previous-versions/ms825891(v=msdn.10)) de l’objet **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="947da-130">The [**RealTimeStylus**](realtimestylus-class.md) object throws an exception if a plug-in calls the **RealTimeStylus** object's [Dispose](/previous-versions/ms825891(v=msdn.10)) method.</span></span> <span data-ttu-id="947da-131">Cela se produit uniquement lorsque le plug-in le fait pendant qu’il est appelé par l’objet **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="947da-131">This happens only when the plug-in does so while it is being called by the **RealTimeStylus** object.</span></span>

<span data-ttu-id="947da-132">L’exemple C suivant \# est du code qui provoque la levée d’une exception par l’objet [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="947da-132">The following C\# example is code that causes the [**RealTimeStylus**](realtimestylus-class.md) object to throw an exception.</span></span>


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



<span data-ttu-id="947da-133">Les collections de plug-ins peuvent être modifiées lorsque l’objet [**RealTimeStylus**](realtimestylus-class.md) est activé ; Toutefois, cela peut rendre le comportement de votre application plus difficile à prédire.</span><span class="sxs-lookup"><span data-stu-id="947da-133">Plug-in collections can be modified while the [**RealTimeStylus**](realtimestylus-class.md) object is enabled; however, this can make the behavior of your application harder to predict.</span></span> <span data-ttu-id="947da-134">Lorsqu’un plug-in est ajouté alors que l’objet **RealTimeStylus** est activé, l’objet **RealTimeStylus** appelle la méthode [IStylusAsyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) ou IStylusSyncPlugin. [RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) du plug-in.</span><span class="sxs-lookup"><span data-stu-id="947da-134">When a plug-in is added while the **RealTimeStylus** object is enabled, the **RealTimeStylus** object calls the plug-in's [IStylusAsyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) or [IStylusSyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) method.</span></span> <span data-ttu-id="947da-135">Quand un plug-in est supprimé alors que l’objet **RealTimeStylus** est activé, l’objet **RealTimeStylus** appelle la méthode [IStylusAsyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) ou IStylusSyncPlugin. [RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) du plug-in.</span><span class="sxs-lookup"><span data-stu-id="947da-135">When a plug-in is removed while the **RealTimeStylus** object is enabled, the **RealTimeStylus** object calls the plug-in's [IStylusAsyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) or [IStylusSyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) method.</span></span> <span data-ttu-id="947da-136">Cela permet au plug-in de conserver son état approprié sans avoir à vérifier la propriété [Enabled](/previous-versions/ms824832(v=msdn.10)) de l’objet **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="947da-136">This allows the plug-in to maintain its proper state without having to check the [Enabled](/previous-versions/ms824832(v=msdn.10)) property of the **RealTimeStylus** object.</span></span>

<span data-ttu-id="947da-137">Quand un plug-in est ajouté alors que l’objet [**RealTimeStylus**](realtimestylus-class.md) est activé, les données de plug-in reçues par le plug-in peuvent ne pas contenir suffisamment d’informations pour établir correctement le contexte des données initiales.</span><span class="sxs-lookup"><span data-stu-id="947da-137">When a plug-in is added while the [**RealTimeStylus**](realtimestylus-class.md) object is enabled, the plug-in data that the plug-in receives may not contain enough information to adequately establish the context of the initial data.</span></span> <span data-ttu-id="947da-138">Par exemple, le plug-in qui vient d’être ajouté peut commencer à recevoir des données de paquets à partir d’un stylet mi-course.</span><span class="sxs-lookup"><span data-stu-id="947da-138">For example, the newly added plug-in could start receiving packet data from a pen that is mid-stroke.</span></span> <span data-ttu-id="947da-139">De même, lorsqu’un plug-in est supprimé alors que l’objet **RealTimeStylus** est activé, les données de plug-in que le plug-in a reçues sont peut-être insuffisantes pour terminer le traitement des données.</span><span class="sxs-lookup"><span data-stu-id="947da-139">Similarly, when a plug-in removed while the **RealTimeStylus** object is enabled, the plug-in data that the plug-in has received may be insufficient to finish processing the data.</span></span>

> [!Note]  
> <span data-ttu-id="947da-140">Pour la stabilité globale, réinitialisez l’état interne d’un plug-in lorsque sa méthode [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) ou [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) est appelée.</span><span class="sxs-lookup"><span data-stu-id="947da-140">For overall stability, reset a plug-in's internal state when either its [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) or [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) method is called.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="947da-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="947da-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="947da-142">Modèle RealTimeStylus monté en cascade</span><span class="sxs-lookup"><span data-stu-id="947da-142">The Cascaded RealTimeStylus Model</span></span>](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[<span data-ttu-id="947da-143">Considérations relatives à la gestion des erreurs pour les API StylusInput</span><span class="sxs-lookup"><span data-stu-id="947da-143">Error Handling Considerations for the StylusInput APIs</span></span>](error-handling-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[<span data-ttu-id="947da-144">Données de plug-in et classe RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="947da-144">Plug-in Data and the RealTimeStylus Class</span></span>](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[<span data-ttu-id="947da-145">Considérations relatives aux threads pour les API StylusInput</span><span class="sxs-lookup"><span data-stu-id="947da-145">Threading Considerations for the StylusInput APIs</span></span>](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
