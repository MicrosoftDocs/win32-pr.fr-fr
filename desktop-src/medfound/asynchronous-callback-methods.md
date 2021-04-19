---
description: Méthodes de rappel asynchrones
ms.assetid: ea778eaa-6460-4a93-bd6a-1857ea8b6230
title: Méthodes de rappel asynchrones
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0064873a5b026b6910597ebc9911f56f00584b03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515806"
---
# <a name="asynchronous-callback-methods"></a><span data-ttu-id="7bf0f-103">Méthodes de rappel asynchrones</span><span class="sxs-lookup"><span data-stu-id="7bf0f-103">Asynchronous Callback Methods</span></span>

<span data-ttu-id="7bf0f-104">Media Foundation offre un moyen cohérent d’implémenter des méthodes asynchrones à l’aide d’une interface de rappel.</span><span class="sxs-lookup"><span data-stu-id="7bf0f-104">Media Foundation provides a consistent way to implement asynchronous methods, using a callback interface.</span></span>

<span data-ttu-id="7bf0f-105">Cette section décrit comment implémenter l’interface de rappel et comment écrire des méthodes asynchrones qui utilisent cette interface.</span><span class="sxs-lookup"><span data-stu-id="7bf0f-105">This section describes how to implement the callback interface and how to write asynchronous methods that use this interface.</span></span> <span data-ttu-id="7bf0f-106">Elle contient les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="7bf0f-106">It contains the following topics.</span></span>



| <span data-ttu-id="7bf0f-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="7bf0f-107">Topic</span></span>                                                                                | <span data-ttu-id="7bf0f-108">Description</span><span class="sxs-lookup"><span data-stu-id="7bf0f-108">Description</span></span>                                                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7bf0f-109">Appeler des méthodes asynchrones</span><span class="sxs-lookup"><span data-stu-id="7bf0f-109">Calling Asynchronous Methods</span></span>](calling-asynchronous-methods.md)                     | <span data-ttu-id="7bf0f-110">Comment appeler des méthodes asynchrones dans Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="7bf0f-110">How to call asynchronous methods in Media Foundation.</span></span>                                               |
| [<span data-ttu-id="7bf0f-111">Implémentation du rappel asynchrone</span><span class="sxs-lookup"><span data-stu-id="7bf0f-111">Implementing the Asynchronous Callback</span></span>](implementing-the-asynchronous-callback.md) | <span data-ttu-id="7bf0f-112">Comment implémenter la méthode de rappel dans l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="7bf0f-112">How to implement the callback method in the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> |
| [<span data-ttu-id="7bf0f-113">Prise en charge de plusieurs rappels</span><span class="sxs-lookup"><span data-stu-id="7bf0f-113">Supporting Multiple Callbacks</span></span>](supporting-multiple-callbacks.md)                   | <span data-ttu-id="7bf0f-114">Comment prendre en charge plusieurs rappels au sein de la même classe C++.</span><span class="sxs-lookup"><span data-stu-id="7bf0f-114">How to support multiple callbacks within the same C++ class.</span></span>                                        |
| [<span data-ttu-id="7bf0f-115">Files d’attente de travail</span><span class="sxs-lookup"><span data-stu-id="7bf0f-115">Work Queues</span></span>](work-queues.md)                                                       | <span data-ttu-id="7bf0f-116">Les files d’attente de travail offrent un moyen efficace d’effectuer des opérations asynchrones sur un autre thread.</span><span class="sxs-lookup"><span data-stu-id="7bf0f-116">Work queues provide an efficient way to perform asynchronous operations on another thread.</span></span>          |
| [<span data-ttu-id="7bf0f-117">Écriture d’une méthode asynchrone</span><span class="sxs-lookup"><span data-stu-id="7bf0f-117">Writing an Asynchronous Method</span></span>](writing-an-asynchronous-method.md)                 | <span data-ttu-id="7bf0f-118">Comment implémenter des méthodes asynchrones dans Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="7bf0f-118">How to implement asynchronous methods in Media Foundation.</span></span>                                          |
| [<span data-ttu-id="7bf0f-119">Objets de résultats asynchrones personnalisés</span><span class="sxs-lookup"><span data-stu-id="7bf0f-119">Custom Asynchronous Result Objects</span></span>](custom-asynchronous-result-objects.md)         | <span data-ttu-id="7bf0f-120">Comment fournir une implémentation personnalisée de l’interface [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) .</span><span class="sxs-lookup"><span data-stu-id="7bf0f-120">How to provide a custom implementation of the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="7bf0f-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7bf0f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bf0f-122">**Interface IMFAsyncCallback**</span><span class="sxs-lookup"><span data-stu-id="7bf0f-122">**IMFAsyncCallback Interface**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
</dt> <dt>

[<span data-ttu-id="7bf0f-123">**Interface IMFAsyncResult**</span><span class="sxs-lookup"><span data-stu-id="7bf0f-123">**IMFAsyncResult Interface**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)
</dt> <dt>

[<span data-ttu-id="7bf0f-124">API de plateforme Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7bf0f-124">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



