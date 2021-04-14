---
title: Gestion de l’allocation de mémoire
description: Gestion de l’allocation de mémoire
ms.assetid: 8a189fe8-5555-44bb-968b-04408fa7fce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2af04b4ecc5b8480230b17ae710b84ce8e6ce5d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104383011"
---
# <a name="managing-memory-allocation"></a><span data-ttu-id="382b2-103">Gestion de l’allocation de mémoire</span><span class="sxs-lookup"><span data-stu-id="382b2-103">Managing Memory Allocation</span></span>

<span data-ttu-id="382b2-104">Dans COM, de nombreuses méthodes d’interface sont appelées par du code écrit par une organisation de programmation et implémentées par du code écrit par un autre.</span><span class="sxs-lookup"><span data-stu-id="382b2-104">In COM, many, if not most, interface methods are called by code written by one programming organization and implemented by code written by another.</span></span> <span data-ttu-id="382b2-105">La plupart des paramètres et valeurs de retour de ces fonctions sont des types qui peuvent être passés par valeur.</span><span class="sxs-lookup"><span data-stu-id="382b2-105">Many of the parameters and return values of these functions are of types that can be passed around by value.</span></span> <span data-ttu-id="382b2-106">Toutefois, il est parfois nécessaire de passer des structures de données pour lesquelles ce n’est pas le cas. par conséquent, il est nécessaire que l’appelant et l’appel aient une stratégie d’allocation et de désallocation compatible.</span><span class="sxs-lookup"><span data-stu-id="382b2-106">Sometimes, however, it is necessary to pass data structures for which this is not the case, so it is necessary for both caller and called to have a compatible allocation and de-allocation policy.</span></span> <span data-ttu-id="382b2-107">COM définit une Convention universelle pour l’allocation de mémoire, car il est plus raisonnable de définir des règles de cas par cas et de sorte que l’implémentation de l’appel de procédure distante COM puisse gérer correctement la mémoire.</span><span class="sxs-lookup"><span data-stu-id="382b2-107">COM defines a universal convention for memory allocation, because it is more reasonable than defining case-by-case rules and so that the COM remote procedure call implementation can correctly manage memory.</span></span>

<span data-ttu-id="382b2-108">Les méthodes d’une interface COM fournissent toujours la gestion de la mémoire des pointeurs à l’interface en appelant les fonctions [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) et [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) qui se trouvent dans l’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , à partir desquelles toutes les autres interfaces COM dérivent.</span><span class="sxs-lookup"><span data-stu-id="382b2-108">The methods of a COM interface always provide memory management of pointers to the interface by calling the [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) functions found in the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, from which all other COM interfaces derive.</span></span> <span data-ttu-id="382b2-109">(Pour plus d’informations, consultez [règles de gestion des décomptes de références](rules-for-managing-reference-counts.md) .)</span><span class="sxs-lookup"><span data-stu-id="382b2-109">(See [Rules for Managing Reference Counts](rules-for-managing-reference-counts.md) for more information.)</span></span>

<span data-ttu-id="382b2-110">Cette section décrit uniquement comment allouer de la mémoire pour des paramètres qui ne sont pas passés par valeur, et non des pointeurs vers des interfaces, mais des éléments plus banals comme des chaînes, des pointeurs vers des structures, etc.</span><span class="sxs-lookup"><span data-stu-id="382b2-110">This section describes only how to allocate memory for parameters that are not passed by value — not pointers to interfaces, but more mundane things like strings, pointers to structures, and so forth.</span></span>

<span data-ttu-id="382b2-111">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="382b2-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="382b2-112">Allocateur de mémoire OLE</span><span class="sxs-lookup"><span data-stu-id="382b2-112">The OLE Memory Allocator</span></span>](the-ole-memory-allocator.md)
-   [<span data-ttu-id="382b2-113">Règles de gestion de la mémoire</span><span class="sxs-lookup"><span data-stu-id="382b2-113">Memory Management Rules</span></span>](memory-management-rules.md)
-   [<span data-ttu-id="382b2-114">Débogage des allocations de mémoire</span><span class="sxs-lookup"><span data-stu-id="382b2-114">Debugging Memory Allocations</span></span>](debugging-memory-allocations.md)

 

 