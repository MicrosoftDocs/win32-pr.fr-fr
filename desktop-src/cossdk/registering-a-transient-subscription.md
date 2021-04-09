---
description: Les abonnements temporaires ne peuvent pas être définis à l’aide de l’outil d’administration Services de composants. Vous devez utiliser les interfaces d’administration COM+ pour créer ou mettre à jour un abonnement temporaire.
ms.assetid: 28d48d59-abb2-4682-ab54-60b6aa7b31b1
title: Inscription d’un abonnement temporaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3fc85f189d14fbe6220d6f3760509e1ba0248a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110638"
---
# <a name="registering-a-transient-subscription"></a><span data-ttu-id="f0285-104">Inscription d’un abonnement temporaire</span><span class="sxs-lookup"><span data-stu-id="f0285-104">Registering a Transient Subscription</span></span>

<span data-ttu-id="f0285-105">Les abonnements temporaires demandent un événement pour un objet d’abonné spécifique qui existe déjà.</span><span class="sxs-lookup"><span data-stu-id="f0285-105">Transient subscriptions request an event for a specific subscriber object that already exists.</span></span> <span data-ttu-id="f0285-106">Les abonnements temporaires sont stockés dans le catalogue COM+, mais l’abonnement est supprimé si le système d’événements ou le système d’exploitation est arrêté.</span><span class="sxs-lookup"><span data-stu-id="f0285-106">Transient subscriptions are stored in the COM+ catalog, but the subscription is deleted if the event system or operating system is stopped.</span></span> <span data-ttu-id="f0285-107">Contrairement aux abonnements persistants, les abonnements temporaires sont liés à un objet particulier et sont stockés uniquement dans le système d’événements.</span><span class="sxs-lookup"><span data-stu-id="f0285-107">Unlike persistent subscriptions, transient subscriptions are tied to a particular object and are stored only in the event system.</span></span> <span data-ttu-id="f0285-108">En cas de problème avec le système d’exploitation ou le système d’exploitation, l’abonnement disparaît.</span><span class="sxs-lookup"><span data-stu-id="f0285-108">If there is a problem with the event system or operating system, the subscription disappears.</span></span> <span data-ttu-id="f0285-109">Les abonnements temporaires peuvent être plus efficaces que les abonnements persistants, mais vous devez gérer leurs cycles de vie d’objet.</span><span class="sxs-lookup"><span data-stu-id="f0285-109">Transient subscriptions can be more efficient than persistent subscriptions, but you must manage their object life cycles.</span></span>

<span data-ttu-id="f0285-110">Les abonnements temporaires ne peuvent pas être définis à l’aide de l’outil d’administration Services de composants.</span><span class="sxs-lookup"><span data-stu-id="f0285-110">Transient subscriptions cannot be set by using the Component Services administration tool.</span></span> <span data-ttu-id="f0285-111">Vous devez utiliser les interfaces d’administration COM+ pour créer ou mettre à jour un abonnement temporaire.</span><span class="sxs-lookup"><span data-stu-id="f0285-111">You must use the COM+ administrative interfaces to create or update a transient subscription.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="f0285-112">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="f0285-112">Visual Basic</span></span>

<span data-ttu-id="f0285-113">La procédure suivante décrit comment créer un abonnement temporaire à l’aide de Microsoft Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="f0285-113">The following procedure describes how to create a transient subscription using Microsoft Visual Basic:</span></span>

1.  <span data-ttu-id="f0285-114">Spécifiez un abonnement transitoire en ajoutant une nouvelle entrée à la collection [**TransientSubscriptions**](transientsubscriptions.md) et en affectant à la propriété SubscriberInterface l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) de l’objet abonné.</span><span class="sxs-lookup"><span data-stu-id="f0285-114">Specify a subscription as transient by adding a new entry to the [**TransientSubscriptions**](transientsubscriptions.md) collection and setting the SubscriberInterface property to the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface of the subscriber object.</span></span> <span data-ttu-id="f0285-115">Les événements COM+ ne créent pas de nouvelle instance de l’objet d’abonné lors du déclenchement d’un événement, mais utilisent à la place l’instance que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="f0285-115">COM+ Events does not create a new instance of the subscriber object when firing an event but instead uses the instance you specify.</span></span> <span data-ttu-id="f0285-116">Les événements COM+ contiennent un décompte de références pour l’objet abonné jusqu’à ce que l’abonnement soit supprimé du système.</span><span class="sxs-lookup"><span data-stu-id="f0285-116">COM+ Events holds a reference count for the subscriber object until the subscription is removed from the system.</span></span>
2.  <span data-ttu-id="f0285-117">Créez une application serveur COM+ (fichier. exe,. dll ou. ocx) avec un objet qui implémente les interfaces ou les méthodes auxquelles vous voulez vous abonner.</span><span class="sxs-lookup"><span data-stu-id="f0285-117">Create a COM+ server application (an .exe, a .dll, or an .ocx file) with an object that implements the interfaces or methods you want to subscribe to.</span></span>
3.  <span data-ttu-id="f0285-118">Créez votre abonnement temporaire en utilisant le code suivant, en passant le CLSID de l’objet de [classe d’événements](the-com--event-class-object.md) et l’instance de l’objet d’abonné.</span><span class="sxs-lookup"><span data-stu-id="f0285-118">Create your transient subscription using the following code, by passing in the CLSID of the [event class](the-com--event-class-object.md) object and the instance of the subscriber object.</span></span> <span data-ttu-id="f0285-119">À l’aide de l’outil d’administration Services de composants, vous pouvez obtenir la propriété EventCLSID en cliquant avec le bouton droit sur le composant COM+, en sélectionnant **Propriétés**, puis en sélectionnant l’onglet **général** .</span><span class="sxs-lookup"><span data-stu-id="f0285-119">Using the Component Services administrative tool, you can get the EventCLSID property by right-clicking the COM+ component, selecting **Properties**, and selecting the **General** tab.</span></span>

    ``` syntax
    Public Function CreateTransientSubscription( _
      ByVal clsid As String, ByVal objref As Object) As String 
        Dim oCOMAdminCatalog As COMAdmin.COMAdminCatalog
        Dim oTSCol As COMAdminCatalogCollection
        Dim oSubscription As ICatalogObject
        Dim objvar As Variant
        On Error GoTo CreateTransientSubscriptionError
        Set oCOMAdminCatalog = CreateObject("COMAdmin.COMAdminCatalog")
        'Gets the TransientSubscriptions collection
        Set oTSCol = oCOMAdminCatalog.GetCollection( _
          "TransientSubscriptions")
        Set oSubscription = oTSCol.Add
        Set objvar = objref
        oSubscription.Value("SubscriberInterface") = objref
        oSubscription.Value("EventCLSID") = clsid
        oSubscription.Value("Name") = "TransientSubscription"
        oTSCol.SaveChanges
        CreateTransientSubscription = oSubscription.Value("ID")
        Set oSubscription = Nothing
        Set oTSCol = Nothing
        Set oCOMAdminCatalog = Nothing
        Set objvar = Nothing
        Exit Function
    CreateTransientSubscriptionError:
        CreateTransientSubscription = ""
        Err.Raise Err.Number, "[CreateTransientSubscription]" & _
          Err.Source, Err.Description
    End Function
    ```

<span data-ttu-id="f0285-120">L’exemple suivant illustre l’appel de la fonction CreateTransientSubscription pour s’abonner à une interface appelée IStockTicker, qui a une méthode appelée UpdateStock.</span><span class="sxs-lookup"><span data-stu-id="f0285-120">The following example illustrates how to call the CreateTransientSubscription function to subscribe to an interface called IStockTicker, which has a method called UpdateStock.</span></span>

1.  <span data-ttu-id="f0285-121">Créez une classe d’événements qui prend en charge l’interface IStockTicker, qui a une méthode, UpdateStock.</span><span class="sxs-lookup"><span data-stu-id="f0285-121">Create an event class that supports the interface IStockTicker, which has one method, UpdateStock.</span></span>
2.  <span data-ttu-id="f0285-122">Dans votre projet d’abonné, ajoutez une classe qui implémente l’interface IStockTicker.</span><span class="sxs-lookup"><span data-stu-id="f0285-122">In your subscriber project, add a class that implements the IStockTicker interface.</span></span>
3.  <span data-ttu-id="f0285-123">Lorsque vous souhaitez vous abonner, exécutez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="f0285-123">When you want to subscribe execute the following code:</span></span>

    ``` syntax
    Dim oMyTicker As Object
    Dim sSubscriptionID As String
    Set oMyTicker = CreateObject("TheProject.CMyTicker")
    sSubscriptionID = CreateTransientSubscription( _
      "{..CLSID for the Event Class..}", oMyTicker)
    ```

<span data-ttu-id="f0285-124">La fonction CreateTransientSubscription retourne une chaîne, qui est un GUID qui peut être utilisé comme un handle ou un cookie pour révoquer l’abonnement ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="f0285-124">The CreateTransientSubscription function returns a string, which is a GUID that can be used as a handle or a cookie to revoke the subscription later.</span></span> <span data-ttu-id="f0285-125">Pour supprimer l’abonnement, appelez la méthode [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de [**COMAdminCatalogCollection**](comadmincatalogcollection.md) sur la collection [**TransientSubscriptions**](transientsubscriptions.md) , en transmettant l’index correspondant à l’abonnement avec le GUID précédemment reçu.</span><span class="sxs-lookup"><span data-stu-id="f0285-125">To remove the subscription, call the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of [**COMAdminCatalogCollection**](comadmincatalogcollection.md) on the [**TransientSubscriptions**](transientsubscriptions.md) collection, passing in the index corresponding to the subscription with the GUID previously received.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0285-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f0285-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0285-127">Inscription d’un abonnement</span><span class="sxs-lookup"><span data-stu-id="f0285-127">Registering a Subscription</span></span>](registering-a-subscription.md)
</dt> </dl>

 

 
