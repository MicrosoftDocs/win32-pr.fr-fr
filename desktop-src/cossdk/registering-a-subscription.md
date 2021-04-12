---
description: Une fois que vous avez inscrit une classe d’événements dans le catalogue COM+, vous pouvez ajouter des abonnés à la classe d’événements et des abonnements aux abonnés.
ms.assetid: 101b1075-3724-4508-9c9e-2f12ac6ab65d
title: Inscription d’un abonnement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03d5710fc792cad6282683d51df21d2ede10451
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393175"
---
# <a name="registering-a-subscription"></a><span data-ttu-id="3b064-103">Inscription d’un abonnement</span><span class="sxs-lookup"><span data-stu-id="3b064-103">Registering a Subscription</span></span>

<span data-ttu-id="3b064-104">Une fois que vous avez inscrit une classe d’événements dans le catalogue COM+, vous pouvez ajouter des abonnés à la classe d’événements et des abonnements aux abonnés.</span><span class="sxs-lookup"><span data-stu-id="3b064-104">After you have registered an event class in the COM+ catalog, you can add subscribers to the event class and subscriptions to the subscribers.</span></span> <span data-ttu-id="3b064-105">Les abonnements peuvent s’abonner à une méthode unique ou à toutes les méthodes d’une interface.</span><span class="sxs-lookup"><span data-stu-id="3b064-105">Subscriptions can subscribe to a single method or to all the methods of an interface.</span></span> <span data-ttu-id="3b064-106">Pour recevoir des appels sur plus d’une méthode, mais pas sur chaque méthode, d’une interface, vous devez ajouter un abonnement pour chaque méthode à laquelle vous souhaitez recevoir un appel.</span><span class="sxs-lookup"><span data-stu-id="3b064-106">To receive calls on more than one method—but not to every method—of an interface, you must add a subscription for each method to which you want to receive a call.</span></span> <span data-ttu-id="3b064-107">L’outil d’administration Services de composants peut rechercher dans le catalogue COM+ des classes d’événements inscrites qui prennent en charge les interfaces implémentées par l’abonné et vous offre le choix de s’abonner.</span><span class="sxs-lookup"><span data-stu-id="3b064-107">The Component Services administration tool can search the COM+ catalog for registered event classes that support the interfaces implemented by the subscriber and offers you the choice to subscribe.</span></span> <span data-ttu-id="3b064-108">Choisissez le serveur de publication qui vous offre les événements souhaités.</span><span class="sxs-lookup"><span data-stu-id="3b064-108">Choose the publisher that offers you the desired events.</span></span>

<span data-ttu-id="3b064-109">Pour ajouter des abonnés au composant abonné, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="3b064-109">To add subscribers to the subscriber component, use the following steps:</span></span>

1.  <span data-ttu-id="3b064-110">Après avoir créé une application COM+ et installé le composant d’abonné, cliquez avec le bouton droit sur le dossier **abonnements** pour activer l’Assistant Création d’un nouvel abonnement com+.</span><span class="sxs-lookup"><span data-stu-id="3b064-110">After creating a new COM+ application and installing the subscriber component, right-click the **Subscriptions** folder to enable the COM+ New Subscription Wizard.</span></span>

2.  <span data-ttu-id="3b064-111">Choisissez la classe d’événements à partir de laquelle vous souhaitez recevoir des événements.</span><span class="sxs-lookup"><span data-stu-id="3b064-111">Choose the event class from which you want to receive events.</span></span>

3.  <span data-ttu-id="3b064-112">Entrez un nom pour l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="3b064-112">Enter a name for the subscription.</span></span>

4.  <span data-ttu-id="3b064-113">Activez l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="3b064-113">Enable the subscription.</span></span>

5.  <span data-ttu-id="3b064-114">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="3b064-114">Click **OK**.</span></span>

<span data-ttu-id="3b064-115">Quand une application de serveur de publication souhaite déclencher un événement, le serveur de publication instancie l’objet de classe d’événements et appelle une méthode sur celui-ci.</span><span class="sxs-lookup"><span data-stu-id="3b064-115">When a publisher application wants to fire an event, the publisher instantiates the event class object and calls a method on it.</span></span> <span data-ttu-id="3b064-116">COM+ recherche tous les abonnés dans le catalogue COM+.</span><span class="sxs-lookup"><span data-stu-id="3b064-116">COM+ searches the COM+ catalog to find all the subscribers.</span></span> <span data-ttu-id="3b064-117">Il crée l’objet d’abonné (directement, en file d’attente ou avec un moniker) et passe sur l’appel de méthode initialement effectué par le serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="3b064-117">It creates the subscriber object (directly, queued, or with a moniker) and passes on the method call originally made by the publisher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b064-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3b064-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b064-119">Inscription d’une classe d’événements</span><span class="sxs-lookup"><span data-stu-id="3b064-119">Registering an Event Class</span></span>](registering-an-event-class.md)
</dt> </dl>

 

 



