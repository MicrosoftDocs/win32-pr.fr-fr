---
description: Les considérations suivantes relatives aux threads Tablet PC sont spécifiques à l’utilisation du modèle COM (Component Object Model) et de l’automatisation.
ms.assetid: cf8feba5-a391-4396-a5d8-1ef58df304a7
title: Considérations relatives aux threads COM et Automation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe0cf67d427ce89074a605f664e94f35d3d3eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515400"
---
# <a name="com-and-automation-threading-considerations"></a><span data-ttu-id="a8749-103">Considérations relatives aux threads COM et Automation</span><span class="sxs-lookup"><span data-stu-id="a8749-103">COM and Automation Threading Considerations</span></span>

<span data-ttu-id="a8749-104">Les considérations suivantes relatives aux threads Tablet PC sont spécifiques à l’utilisation du modèle COM (Component Object Model) et de l’automatisation.</span><span class="sxs-lookup"><span data-stu-id="a8749-104">The following Tablet PC threading considerations are specific to when Component Object Model (COM) and Automation are used.</span></span>

-   [<span data-ttu-id="a8749-105">Cohérence de thread</span><span class="sxs-lookup"><span data-stu-id="a8749-105">Thread Safety</span></span>](#thread-safety)
-   [<span data-ttu-id="a8749-106">Applications STA et MTA</span><span class="sxs-lookup"><span data-stu-id="a8749-106">STA and MTA Applications</span></span>](#sta-and-mta-applications)
-   [<span data-ttu-id="a8749-107">InkCollector et InkOverlay</span><span class="sxs-lookup"><span data-stu-id="a8749-107">InkCollector and InkOverlay</span></span>](#inkcollector-and-inkoverlay)
-   [<span data-ttu-id="a8749-108">Récepteurs d’événements</span><span class="sxs-lookup"><span data-stu-id="a8749-108">Event Sinks</span></span>](#event-sinks)
-   [<span data-ttu-id="a8749-109">Exceptions dans les gestionnaires d’événements</span><span class="sxs-lookup"><span data-stu-id="a8749-109">Exceptions within Event Handlers</span></span>](#exceptions-within-event-handlers)
-   [<span data-ttu-id="a8749-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a8749-110">Related topics</span></span>](#related-topics)

## <a name="thread-safety"></a><span data-ttu-id="a8749-111">Cohérence de thread</span><span class="sxs-lookup"><span data-stu-id="a8749-111">Thread Safety</span></span>

<span data-ttu-id="a8749-112">À l’exception des contrôles [InkPicture](inkpicture-control.md) et [InkEdit](inkedit-control.md) , les objets Tablet PC sont thread-safe et sont marqués comme les deux.</span><span class="sxs-lookup"><span data-stu-id="a8749-112">Except for the [InkPicture](inkpicture-control.md) and [InkEdit](inkedit-control.md) controls, Tablet PC objects are thread-safe and are marked as both.</span></span> <span data-ttu-id="a8749-113">Si elles sont marquées comme étant toutes les deux, elles peuvent s’exécuter dans un thread cloisonné (STA, Single-Threaded Apartment) ou un cloisonnement multithread (MTA).</span><span class="sxs-lookup"><span data-stu-id="a8749-113">By being marked as both, they can run in either a single threaded apartment (STA) or a multithreaded apartment (MTA).</span></span>

<span data-ttu-id="a8749-114">Windows Forms utilise le modèle STA, car les Windows Forms sont basés sur des fenêtres Win32 natives qui sont intrinsèquement des threads cloisonnés.</span><span class="sxs-lookup"><span data-stu-id="a8749-114">Windows forms use the STA model because windows forms are based on native Win32 windows that are inherently apartment threaded.</span></span>

## <a name="sta-and-mta-applications"></a><span data-ttu-id="a8749-115">Applications STA et MTA</span><span class="sxs-lookup"><span data-stu-id="a8749-115">STA and MTA Applications</span></span>

<span data-ttu-id="a8749-116">Si votre application s’exécute dans un MTA ou utilise le marshaleur de thread libre (FTM), vous devez écrire du code thread-safe. Toutefois, en procédant ainsi, vous pouvez améliorer certains problèmes de performances de gestion des événements.</span><span class="sxs-lookup"><span data-stu-id="a8749-116">If your application runs in an MTA or uses the free threaded marshaler (FTM), you must write thread-safe code; however, by doing so you can improve certain event handling performance issues.</span></span>

## <a name="inkcollector-and-inkoverlay"></a><span data-ttu-id="a8749-117">InkCollector et InkOverlay</span><span class="sxs-lookup"><span data-stu-id="a8749-117">InkCollector and InkOverlay</span></span>

<span data-ttu-id="a8749-118">Votre application ne doit pas libérer sa référence finale à l’objet [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) , ce qui a pour conséquence la destruction de l’objet, directement à partir du thread Ink.</span><span class="sxs-lookup"><span data-stu-id="a8749-118">Your application should not release its final reference to the [**InkCollector**](inkcollector-class.md) or the [**InkOverlay**](inkoverlay-class.md) object, thus destroying the object, directly from the ink thread.</span></span> <span data-ttu-id="a8749-119">Au lieu de cela, l’application doit libérer l’objet **InkCollector** ou **InkOverlay** à partir d’un thread d’application.</span><span class="sxs-lookup"><span data-stu-id="a8749-119">Instead, the application should release the **InkCollector** or the **InkOverlay** object from an application thread.</span></span>

<span data-ttu-id="a8749-120">**Attention :** Une application marquée comme MTA ou utilisant FTM, qui autorise les appels directs à partir du thread Ink dans le cloisonnement de l’application, peut libérer sa référence finale à l’objet [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) directement à partir du thread d’encre. Toutefois, cela provoque l’échec d’une application irrécupérable.</span><span class="sxs-lookup"><span data-stu-id="a8749-120">**Caution:** An application that is marked MTA or uses the FTM, which allows direct calls from the ink thread into the application's apartment, can release its final reference to the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object directly from the ink thread; however, this causes unrecoverable application failure.</span></span>

## <a name="event-sinks"></a><span data-ttu-id="a8749-121">Récepteurs d’événements</span><span class="sxs-lookup"><span data-stu-id="a8749-121">Event Sinks</span></span>

<span data-ttu-id="a8749-122">Si votre application n’utilise pas FTM et qu’un objet et que son récepteur d’événements sont créés dans différents cloisonnements, l’événement s’exécute sur le thread qui dessert le récepteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="a8749-122">If your application is not using the FTM and an object and its event sink are created in different apartments, then the event executes on the thread servicing the event sink.</span></span>

## <a name="exceptions-within-event-handlers"></a><span data-ttu-id="a8749-123">Exceptions dans les gestionnaires d’événements</span><span class="sxs-lookup"><span data-stu-id="a8749-123">Exceptions within Event Handlers</span></span>

<span data-ttu-id="a8749-124">Les exceptions levées à partir des gestionnaires d’événements Tablet PC sont consommées et ne sont pas visibles par le reste ou votre application.</span><span class="sxs-lookup"><span data-stu-id="a8749-124">Exceptions thrown from within Tablet PC event handlers are consumed and are not visible to the rest or your application.</span></span> <span data-ttu-id="a8749-125">De même, les valeurs HRESULT ne sont pas propagées à partir des gestionnaires d’événements Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="a8749-125">Likewise, HRESULT values are not propagated from Tablet PC event handlers.</span></span> <span data-ttu-id="a8749-126">Si une application utilisant la couche COM lève une exception, le thread d’arrière-plan se termine et l’exception est perdue.</span><span class="sxs-lookup"><span data-stu-id="a8749-126">If an application using the COM layer throws an exception, the background thread terminates, and the exception will be lost.</span></span> <span data-ttu-id="a8749-127">Aucun gestionnaire d’événements supplémentaire n’est appelé.</span><span class="sxs-lookup"><span data-stu-id="a8749-127">No additional event handlers will be called.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8749-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a8749-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8749-129">Exemple de récepteurs d’événements C++</span><span class="sxs-lookup"><span data-stu-id="a8749-129">C++ Event Sinks Sample</span></span>](c---event-sinks-sample.md)
</dt> <dt>

[<span data-ttu-id="a8749-130">Considérations générales sur les threads</span><span class="sxs-lookup"><span data-stu-id="a8749-130">General Threading Considerations</span></span>](general-threading-considerations.md)
</dt> <dt>

[<span data-ttu-id="a8749-131">Considérations sur les threads de bibliothèque managée</span><span class="sxs-lookup"><span data-stu-id="a8749-131">Managed Library Threading Considerations</span></span>](managed-library-threading-considerations.md)
</dt> </dl>

 

 



