---
description: API de plateforme Media Foundation
ms.assetid: 1eb20c44-58cb-4e34-a108-1b3c27d54ff1
title: API de plateforme Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed1e8d8aa0dcd5d7b1184a406e09910a98892f4f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106522877"
---
# <a name="media-foundation-platform-apis"></a><span data-ttu-id="c681e-103">API de plateforme Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c681e-103">Media Foundation Platform APIs</span></span>

<span data-ttu-id="c681e-104">La couche de plateforme de Media Foundation contient des primitives et des objets d’assistance utilisés par les autres couches.</span><span class="sxs-lookup"><span data-stu-id="c681e-104">The platform layer of Media Foundation contains primitives and helper objects used by the other layers.</span></span>

<span data-ttu-id="c681e-105">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="c681e-105">This section contains the following topics:</span></span>



| <span data-ttu-id="c681e-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="c681e-106">Topic</span></span>                                                                           | <span data-ttu-id="c681e-107">Description</span><span class="sxs-lookup"><span data-stu-id="c681e-107">Description</span></span>                                                                                                                                                       |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c681e-108">Initialisation de la plateforme Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c681e-108">Initializing the Media Foundation Platform</span></span>](initializing-media-foundation.md) | <span data-ttu-id="c681e-109">Comment initialiser la plateforme Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="c681e-109">How to initialize the Media Foundation platform.</span></span>                                                                                                                  |
| [<span data-ttu-id="c681e-110">Media Foundation et COM</span><span class="sxs-lookup"><span data-stu-id="c681e-110">Media Foundation and COM</span></span>](media-foundation-and-com.md)                        | <span data-ttu-id="c681e-111">Décrit l’interaction entre COM et Microsoft Media Foundation, et définit certaines meilleures pratiques à utiliser lors du développement de composants de plug-in Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="c681e-111">Describes the interaction between COM and Microsoft Media Foundation, and defines some best practices to use when developing Media Foundation plug-in components.</span></span> |
| [<span data-ttu-id="c681e-112">Méthodes de rappel asynchrones</span><span class="sxs-lookup"><span data-stu-id="c681e-112">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)              | <span data-ttu-id="c681e-113">Comment appeler des méthodes asynchrones et comment implémenter des opérations asynchrones dans Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="c681e-113">How to call asynchronous methods and how to implement asynchronous operations in Media Foundation.</span></span>                                                                |
| [<span data-ttu-id="c681e-114">Files d’attente de travail</span><span class="sxs-lookup"><span data-stu-id="c681e-114">Work Queues</span></span>](work-queues.md)                                                  | <span data-ttu-id="c681e-115">Une file d’attente de travail est un moyen efficace d’effectuer des opérations asynchrones sur un autre thread.</span><span class="sxs-lookup"><span data-stu-id="c681e-115">A work queue is an efficient way to perform asynchronous operations on another thread.</span></span>                                                                            |
| [<span data-ttu-id="c681e-116">Générateurs d’événements de média</span><span class="sxs-lookup"><span data-stu-id="c681e-116">Media Event Generators</span></span>](media-event-generators.md)                            | <span data-ttu-id="c681e-117">Comment recevoir des événements asynchrones et comment déclencher des événements dans Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="c681e-117">How to receive asynchronous events and how to raise events in Media Foundation.</span></span>                                                                                   |
| [<span data-ttu-id="c681e-118">Interfaces de service</span><span class="sxs-lookup"><span data-stu-id="c681e-118">Service Interfaces</span></span>](service-interfaces.md)                                    | <span data-ttu-id="c681e-119">Une interface de service est une interface COM fournie par un objet, mais exposée à l’application par le biais d’un autre objet.</span><span class="sxs-lookup"><span data-stu-id="c681e-119">A service interface is a COM interface provided by one object, but exposed to the application through another object.</span></span>                                             |
| [<span data-ttu-id="c681e-120">Objets d’activation</span><span class="sxs-lookup"><span data-stu-id="c681e-120">Activation Objects</span></span>](activation-objects.md)                                    | <span data-ttu-id="c681e-121">Un objet d’activation est un objet qui crée un autre objet.</span><span class="sxs-lookup"><span data-stu-id="c681e-121">An activation object is an object that creates another object.</span></span>                                                                                                    |
| [<span data-ttu-id="c681e-122">Horloge de présentation</span><span class="sxs-lookup"><span data-stu-id="c681e-122">Presentation Clock</span></span>](presentation-clock.md)                                    | <span data-ttu-id="c681e-123">L’horloge de présentation génère l’heure de l’horloge qui est utilisée pour contrôler la lecture, ainsi que les flux audio et vidéo synchrones.</span><span class="sxs-lookup"><span data-stu-id="c681e-123">The presentation clock generates the clock time that is used to control playback, and also to synchronous audio and video streams.</span></span>                                |



 

## <a name="related-topics"></a><span data-ttu-id="c681e-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c681e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c681e-125">Architecture Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c681e-125">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="c681e-126">Guide de programmation Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c681e-126">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 



