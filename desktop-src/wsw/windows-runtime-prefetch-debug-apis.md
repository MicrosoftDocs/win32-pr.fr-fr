---
title: Prérécupération des API de débogage pour les applications du Windows Store
description: Les API suivantes sont utilisées pour déboguer et tester le comportement de prérécupération de contenu dans une application du Windows Store qui implémente la classe ContentPrefetcher.
ms.assetid: 4FEB0320-7BE4-4B81-A9A1-C1FB5014A4BD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 907cb44382f25e53ce9d4243539f5a7af3247a82
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382271"
---
# <a name="prefetch-debug-apis-for-windows-store-apps"></a><span data-ttu-id="34835-103">Prérécupération des API de débogage pour les applications du Windows Store</span><span class="sxs-lookup"><span data-stu-id="34835-103">Prefetch debug APIs for Windows Store apps</span></span>

<span data-ttu-id="34835-104">Les API suivantes sont utilisées pour déboguer et tester le comportement de prérécupération de contenu dans une application du Windows Store qui implémente la classe [**ContentPrefetcher**](/uwp/api/Windows.Networking.BackgroundTransfer.ContentPrefetcher) .</span><span class="sxs-lookup"><span data-stu-id="34835-104">The following APIs are used to debug and test content prefetching behavior in a Windows Store app that implements the [**ContentPrefetcher**](/uwp/api/Windows.Networking.BackgroundTransfer.ContentPrefetcher) class.</span></span>



| <span data-ttu-id="34835-105">Interface</span><span class="sxs-lookup"><span data-stu-id="34835-105">Interface</span></span>                                                              | <span data-ttu-id="34835-106">Description</span><span class="sxs-lookup"><span data-stu-id="34835-106">Description</span></span>                                                                                                                                                                      |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34835-107">**IContentPrefetcherTaskTrigger**</span><span class="sxs-lookup"><span data-stu-id="34835-107">**IContentPrefetcherTaskTrigger**</span></span>](/windows/desktop/api/IContentPrefetcherTaskTrigger/nn-icontentprefetchertasktrigger-icontentprefetchertasktrigger) | <span data-ttu-id="34835-108">Utilisez cette interface pour vérifier qu’un package d’application du Windows Store installé est inscrit pour cette tâche en arrière-plan et déclencher manuellement ses opérations de prérécupération de contenu.</span><span class="sxs-lookup"><span data-stu-id="34835-108">Use this interface to verify that an installed Windows Store app package is registered for this background task and manually trigger its content prefetch operations.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="34835-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="34835-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34835-110">**ContentPrefetcher**</span><span class="sxs-lookup"><span data-stu-id="34835-110">**ContentPrefetcher**</span></span>](/uwp/api/Windows.Networking.BackgroundTransfer.ContentPrefetcher)
</dt> </dl>

 

