---
title: Utilisation d’événements avec des appels asynchrones
description: Utilisation d’événements avec des appels asynchrones
ms.assetid: 98c24176-a632-400e-b23b-5e13f1bd9a27
keywords:
- Windows Media Format SDK, événements avec appels asynchrones
- Windows Media Format SDK, appels asynchrones (événements)
- événements, appels asynchrones
- événements d’appel asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1729108cae5b73ec96be208709c1360e9401ac0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380268"
---
# <a name="using-events-with-asynchronous-calls"></a><span data-ttu-id="91aa5-107">Utilisation d’événements avec des appels asynchrones</span><span class="sxs-lookup"><span data-stu-id="91aa5-107">Using Events with Asynchronous Calls</span></span>

<span data-ttu-id="91aa5-108">Souvent, lorsque vous utilisez des méthodes qui sont appelées de façon asynchrone, vous devez arrêter le traitement de votre application jusqu’à ce que la méthode termine le traitement.</span><span class="sxs-lookup"><span data-stu-id="91aa5-108">Frequently, when using methods that are called asynchronously, you will want to halt further processing of your application until after the method completes processing.</span></span> <span data-ttu-id="91aa5-109">Vous pouvez implémenter n’importe quelle technique pour gérer cette situation.</span><span class="sxs-lookup"><span data-stu-id="91aa5-109">You can implement any technique you like to handle this situation.</span></span> <span data-ttu-id="91aa5-110">Cette section décrit l’utilisation d’un événement pour attendre des appels asynchrones dans le thread appelant.</span><span class="sxs-lookup"><span data-stu-id="91aa5-110">This section describes using an event to wait for asynchronous calls in the calling thread.</span></span> <span data-ttu-id="91aa5-111">Cette technique est fréquemment utilisée avec le kit de développement logiciel (SDK) du format Windows Media et est illustrée dans certains des exemples d’applications.</span><span class="sxs-lookup"><span data-stu-id="91aa5-111">This technique is frequently used with the Windows Media Format SDK, and is demonstrated in some of the sample applications.</span></span>

<span data-ttu-id="91aa5-112">La liste suivante résume l’utilisation des événements pour attendre des appels asynchrones.</span><span class="sxs-lookup"><span data-stu-id="91aa5-112">The following list summarizes the use of events to wait for asynchronous calls.</span></span>

1.  <span data-ttu-id="91aa5-113">Créez un événement à utiliser avec votre application en appelant la fonction **CreateEvent** du kit de développement logiciel (SDK) de plateforme.</span><span class="sxs-lookup"><span data-stu-id="91aa5-113">Create an event for use with your application by calling the **CreateEvent** function of the Platform SDK.</span></span>
2.  <span data-ttu-id="91aa5-114">Lorsque vous implémentez les rappels appropriés pour votre application, interceptez les messages que vous devez attendre.</span><span class="sxs-lookup"><span data-stu-id="91aa5-114">When implementing the appropriate callbacks for your application, trap the messages for which you need to wait.</span></span> <span data-ttu-id="91aa5-115">Dans la logique de gestion des messages pour les messages souhaités, signalez l’événement en appelant la fonction **SetEvent** du kit de développement logiciel (SDK) de plateforme.</span><span class="sxs-lookup"><span data-stu-id="91aa5-115">In the message handling logic for the desired messages, signal the event by calling the **SetEvent** function of the Platform SDK.</span></span>
3.  <span data-ttu-id="91aa5-116">Une fois les appels aux événements asynchrones effectués dans votre application, attendez que l’événement signale en appelant la fonction **WaitForSingleObject** du kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="91aa5-116">After calls to asynchronous events are made in your application, wait for the event to signal by calling the **WaitForSingleObject** function of the Platform SDK.</span></span> <span data-ttu-id="91aa5-117">Si vous concevez une application Windows, vous devez créer une boucle pour rechercher les messages Windows et inclure un appel à **WaitForSingleObject** dans la boucle avec un délai d’attente bref.</span><span class="sxs-lookup"><span data-stu-id="91aa5-117">If you are designing a Windows application, you should create a loop to check for Windows messages and include a call to **WaitForSingleObject** in the loop with a short wait time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91aa5-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="91aa5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91aa5-119">**Utilisation des méthodes de rappel**</span><span class="sxs-lookup"><span data-stu-id="91aa5-119">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




