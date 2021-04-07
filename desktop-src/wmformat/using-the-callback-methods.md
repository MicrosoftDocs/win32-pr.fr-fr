---
title: Utilisation des méthodes de rappel
description: Utilisation des méthodes de rappel
ms.assetid: 098cb90b-8c21-4692-a4f9-bacce042520a
keywords:
- Windows Media Format SDK, méthodes de rappel
- Windows Media Format SDK, méthodes appelées de façon asynchrone
- méthodes de rappel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d39201c101c9031a7157f79f6c12ec88f07decfc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723418"
---
# <a name="using-the-callback-methods"></a><span data-ttu-id="c2835-106">Utilisation des méthodes de rappel</span><span class="sxs-lookup"><span data-stu-id="c2835-106">Using the Callback Methods</span></span>

<span data-ttu-id="c2835-107">Plusieurs interfaces du kit de développement logiciel (SDK) de format Windows Media contiennent des méthodes appelées de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="c2835-107">Several interfaces in the Windows Media Format SDK contain methods that are called asynchronously.</span></span> <span data-ttu-id="c2835-108">La plupart de ces méthodes utilisent des fonctions de rappel pour transmettre des informations à l’application de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c2835-108">Most of these methods use callback functions to pass information to the controlling application.</span></span>

<span data-ttu-id="c2835-109">Les sections suivantes décrivent certains des problèmes généraux relatifs à l’utilisation des méthodes de rappel avec le kit de développement logiciel (SDK) de format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c2835-109">The following sections describe some of the general issues regarding the use of callback methods with the Windows Media Format SDK.</span></span>



| <span data-ttu-id="c2835-110">Section</span><span class="sxs-lookup"><span data-stu-id="c2835-110">Section</span></span>                                                                          | <span data-ttu-id="c2835-111">Description</span><span class="sxs-lookup"><span data-stu-id="c2835-111">Description</span></span>                                                                                                                                                                                          |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2835-112">Utilisation du rappel OnStatus</span><span class="sxs-lookup"><span data-stu-id="c2835-112">Using the OnStatus Callback</span></span>](using-the-onstatus-callback.md)                   | <span data-ttu-id="c2835-113">Décrit comment implémenter la méthode de rappel [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) , qui est utilisée par plusieurs objets pour informer les applications de la progression de l’opération du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="c2835-113">Describes how to implement the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method, which is used by several objects to advise applications of SDK operation progress.</span></span> |
| [<span data-ttu-id="c2835-114">Utilisation d’événements avec des appels asynchrones</span><span class="sxs-lookup"><span data-stu-id="c2835-114">Using Events with Asynchronous Calls</span></span>](using-events-with-asynchronous-calls.md) | <span data-ttu-id="c2835-115">Décrit une technique courante pour gérer les appels de méthode asynchrones dans une application.</span><span class="sxs-lookup"><span data-stu-id="c2835-115">Describes a common technique to handle asynchronous method calls in an application.</span></span>                                                                                                                  |
| [<span data-ttu-id="c2835-116">Utilisation du paramètre de contexte</span><span class="sxs-lookup"><span data-stu-id="c2835-116">Using the Context Parameter</span></span>](using-the-context-parameter.md)                   | <span data-ttu-id="c2835-117">Présente le paramètre *pvContext* , partagé par plusieurs rappels et leurs méthodes d’appel, et explique comment l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="c2835-117">Introduces the *pvContext* parameter, shared by several callbacks and their calling methods, and explains how to use it.</span></span>                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="c2835-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c2835-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2835-119">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="c2835-119">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




