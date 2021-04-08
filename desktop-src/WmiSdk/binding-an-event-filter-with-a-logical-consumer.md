---
description: Après avoir créé le consommateur d’événements logiques et le filtre d’événements, vous devez les lier, ce qui permet d’inscrire le consommateur logique pour recevoir une notification concernant les événements spécifiés par le filtre.
ms.assetid: 2fc3d781-2b93-4e9e-90a1-1b975ab40a01
ms.tgt_platform: multiple
title: Liaison d’un filtre d’événements à un consommateur logique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f44c4b64b98877231b73543d8753c765c3219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867789"
---
# <a name="binding-an-event-filter-with-a-logical-consumer"></a><span data-ttu-id="c9f19-103">Liaison d’un filtre d’événements à un consommateur logique</span><span class="sxs-lookup"><span data-stu-id="c9f19-103">Binding an Event Filter with a Logical Consumer</span></span>

<span data-ttu-id="c9f19-104">Après avoir créé le consommateur d’événements logiques et le filtre d’événements, vous devez les lier, ce qui permet d’inscrire le consommateur logique pour recevoir une notification concernant les événements spécifiés par le filtre.</span><span class="sxs-lookup"><span data-stu-id="c9f19-104">After you create the logical event consumer and the event filter you must link them, which registers the logical consumer to receive notification about the events specified by the filter.</span></span>

<span data-ttu-id="c9f19-105">La procédure suivante décrit comment lier un filtre d’événement à un consommateur logique.</span><span class="sxs-lookup"><span data-stu-id="c9f19-105">The following procedure describes how to bind an event filter with a logical consumer.</span></span>

<span data-ttu-id="c9f19-106">**Pour lier un filtre d’événement à un consommateur logique**</span><span class="sxs-lookup"><span data-stu-id="c9f19-106">**To bind an event filter with a logical consumer**</span></span>

1.  <span data-ttu-id="c9f19-107">Créez une instance de la classe système [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) dans l’espace de stockage WMI.</span><span class="sxs-lookup"><span data-stu-id="c9f19-107">Create an instance of the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) system class in the WMI repository.</span></span>

    <span data-ttu-id="c9f19-108">La classe [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) est une classe d’association qui lie l’instance de filtre d’événements et l’instance de consommateur logique à l’aide des propriétés de référence de **filtre** et de **consommateur** .</span><span class="sxs-lookup"><span data-stu-id="c9f19-108">The [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) class is an association class that links the event filter instance and the logical consumer instance together through the **Filter** and **Consumer** reference properties.</span></span> <span data-ttu-id="c9f19-109">Pour plus d’informations, consultez [déclaration d’une classe d’association](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="c9f19-109">For more information, see [Declaring an Association Class](declaring-an-association-class.md).</span></span>

2.  <span data-ttu-id="c9f19-110">Définissez la propriété **Filter** sur l’instance de votre filtre.</span><span class="sxs-lookup"><span data-stu-id="c9f19-110">Set the **Filter** property to the instance of your filter.</span></span>
3.  <span data-ttu-id="c9f19-111">Affectez à la propriété de **consommateur** l’instance de votre consommateur logique.</span><span class="sxs-lookup"><span data-stu-id="c9f19-111">Set the **Consumer** property to the instance of your logical consumer.</span></span>
4.  <span data-ttu-id="c9f19-112">Définissez la propriété **DeliverSynchronously** pour déterminer le type de remise souhaité.</span><span class="sxs-lookup"><span data-stu-id="c9f19-112">Set the **DeliverSynchronously** property to determine the type of delivery you want.</span></span>

    <span data-ttu-id="c9f19-113">La propriété **DeliverSynchronously** détermine quand WMI remet les notifications d’événements de façon synchrone ou asynchrone.</span><span class="sxs-lookup"><span data-stu-id="c9f19-113">The **DeliverSynchronously** property determines when WMI delivers event notifications synchronously or asynchronously.</span></span> <span data-ttu-id="c9f19-114">L’affectation de la **valeur true** à cette propriété demande une remise synchrone.</span><span class="sxs-lookup"><span data-stu-id="c9f19-114">Setting this property to **TRUE** requests a synchronous delivery.</span></span> <span data-ttu-id="c9f19-115">Utilisez la remise synchrone uniquement lorsque le consommateur permanent peut traiter des événements dans environ 100 microsecondes.</span><span class="sxs-lookup"><span data-stu-id="c9f19-115">Use synchronous delivery only when the permanent consumer can process events within approximately 100 microseconds.</span></span>

    > [!Note]  
    > <span data-ttu-id="c9f19-116">Étant donné que le rappel au récepteur peut ne pas être retourné au même niveau d’authentification que celui requis par le client, il est recommandé d’utiliser le mode semi-synchrone au lieu de la communication asynchrone.</span><span class="sxs-lookup"><span data-stu-id="c9f19-116">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="c9f19-117">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="c9f19-117">For more information, see [Calling a Method](calling-a-method.md).</span></span>

     

5.  <span data-ttu-id="c9f19-118">Lors de l’annulation de l’inscription de votre consommateur d’événements logiques, veillez à supprimer l’instance [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="c9f19-118">When unregistering your logical event consumer, ensure you delete the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) instance.</span></span>

    <span data-ttu-id="c9f19-119">Chaque instance [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) représente une inscription pour une notification d’événement spécifique.</span><span class="sxs-lookup"><span data-stu-id="c9f19-119">Each [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) instance represents a registration for a specific event notification.</span></span> <span data-ttu-id="c9f19-120">Lorsque vous supprimez une liaison, WMI désactive l’inscription.</span><span class="sxs-lookup"><span data-stu-id="c9f19-120">When you delete a binding, WMI deactivates the registration.</span></span> <span data-ttu-id="c9f19-121">Vous devrez peut-être supprimer les instances de consommateur logique et de filtre d’événements pour désactiver l’inscription, en fonction de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="c9f19-121">You might have to delete the logical consumer and event filter instances to deactivate registration, depending on the implementation.</span></span>

<span data-ttu-id="c9f19-122">L’exemple de code suivant montre une instance [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) qui associe une instance d’une classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) à un filtre d’événement spécifique (l’instance du consommateur d’événements a été créée dans la rubrique [création d’un consommateur logique](creating-a-logical-consumer.md) et le filtre d’événement a été créé dans la rubrique [création d’un filtre d’événements](creating-an-event-filter.md) ).</span><span class="sxs-lookup"><span data-stu-id="c9f19-122">The following code example shows you a [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) instance that associates an instance of an [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class with a specific event filter (the instance of the event consumer was created in the [Creating a Logical Consumer](creating-a-logical-consumer.md) topic, and the event filter was created in the [Creating an Event Filter](creating-an-event-filter.md) topic).</span></span>

``` syntax
instance of __FilterToConsumerBinding
{
    Filter = $FILTER;
    Consumer = $CONSUMER;
    DeliverSynchronously=FALSE;

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

<span data-ttu-id="c9f19-123">Deux consommateurs, [**ActiveScriptEventConsumer**](activescripteventconsumer.md) et [**CommandLineEventConsumer**](commandlineeventconsumer.md), ne fonctionneront pas, sauf si leur créateur est membre du groupe Administrateurs local.</span><span class="sxs-lookup"><span data-stu-id="c9f19-123">Two consumers, [**ActiveScriptEventConsumer**](activescripteventconsumer.md) and [**CommandLineEventConsumer**](commandlineeventconsumer.md), will not work unless their creator is a member of the local Administrators group.</span></span>

<span data-ttu-id="c9f19-124">**:** Lorsqu’un administrateur crée un abonnement, son SID n’est pas utilisé pour la propriété **CreatorSID** , mais le SID du groupe Administrateurs local est utilisé à la place.</span><span class="sxs-lookup"><span data-stu-id="c9f19-124">**:** When an administrator creates a subscription, his SID is not used for the **CreatorSID** property, but the SID of the local Administrators group is used instead.</span></span> <span data-ttu-id="c9f19-125">Par conséquent, les instances peuvent être créées par des administrateurs différents et l’abonnement fonctionnera toujours.</span><span class="sxs-lookup"><span data-stu-id="c9f19-125">Therefore, instances can be created by different administrators and the subscription will still work.</span></span> <span data-ttu-id="c9f19-126">Pour plus d’informations, consultez [réception d’événements en toute sécurité](receiving-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="c9f19-126">For more information, see [Receiving Events Securely](receiving-events-securely.md).</span></span>

<span data-ttu-id="c9f19-127">Lorsqu’un filtre est lié à un consommateur logique, l’événement est enregistré par le [suivi d’événements](/windows/desktop/ETW/event-tracing-portal) pour Windows (ETW).</span><span class="sxs-lookup"><span data-stu-id="c9f19-127">When a filter is bound to a logical consumer the event is recorded by [Event Tracing](/windows/desktop/ETW/event-tracing-portal) for Windows (ETW).</span></span> <span data-ttu-id="c9f19-128">Pour plus d’informations, consultez suivi de l' [activité WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="c9f19-128">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9f19-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c9f19-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9f19-130">Réception d’événements à tout moment</span><span class="sxs-lookup"><span data-stu-id="c9f19-130">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> </dl>

 

 
