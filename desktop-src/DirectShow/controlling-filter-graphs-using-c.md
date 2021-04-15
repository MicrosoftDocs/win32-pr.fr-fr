---
description: Contrôle des graphiques de filtre à l’aide de C
ms.assetid: 56e41f0a-2ea6-422c-8d3f-7849e91e3731
title: Contrôle des graphiques de filtre à l’aide de C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce6d78875c6b0d5f028ea89dfbd2b061285f1c1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392720"
---
# <a name="controlling-filter-graphs-using-c"></a><span data-ttu-id="b05fc-103">Contrôle des graphiques de filtre à l’aide de C</span><span class="sxs-lookup"><span data-stu-id="b05fc-103">Controlling Filter Graphs Using C</span></span>

<span data-ttu-id="b05fc-104">Si vous écrivez une application DirectShow en C (au lieu de C++), vous devez utiliser un pointeur vtable pour appeler des méthodes.</span><span class="sxs-lookup"><span data-stu-id="b05fc-104">If you are writing a DirectShow application in C (rather than C++), you must use a vtable pointer to call methods.</span></span> <span data-ttu-id="b05fc-105">L’exemple suivant illustre l’appel de la méthode **IUnknown :: QueryInterface** à partir d’une application écrite en C :</span><span class="sxs-lookup"><span data-stu-id="b05fc-105">The following example illustrates how to call the **IUnknown::QueryInterface** method from an application written in C:</span></span>


```C++
pGraph->lpVtbl->QueryInterface(pGraph, &IID_IMediaEvent, (void **)&pEvent);
```



<span data-ttu-id="b05fc-106">L’exemple suivant illustre l’appel équivalent en C++ :</span><span class="sxs-lookup"><span data-stu-id="b05fc-106">The following shows the equivalent call in C++:</span></span>


```C++
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



<span data-ttu-id="b05fc-107">En C, les interfaces COM sont définies en tant que structures.</span><span class="sxs-lookup"><span data-stu-id="b05fc-107">In C, COM interfaces are defined as structures.</span></span> <span data-ttu-id="b05fc-108">Le membre **lpVtbl** est un pointeur vers une table de méthodes d’interface (vtable).</span><span class="sxs-lookup"><span data-stu-id="b05fc-108">The **lpVtbl** member is a pointer to a table of interface methods (the vtable).</span></span> <span data-ttu-id="b05fc-109">Toutes les méthodes prennent un paramètre supplémentaire, qui est un pointeur vers l’interface.</span><span class="sxs-lookup"><span data-stu-id="b05fc-109">All methods take an additional parameter, which is a pointer to the interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b05fc-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b05fc-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b05fc-111">Annexes</span><span class="sxs-lookup"><span data-stu-id="b05fc-111">Appendixes</span></span>](appendixes.md)
</dt> </dl>

 

 



