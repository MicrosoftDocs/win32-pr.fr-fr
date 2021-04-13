---
title: Imbrication/délégation
description: Le mécanisme le plus courant pour la réutilisation d’objets dans COM est la relation contenant-contenu et la délégation.
ms.assetid: 56396c11-889a-4f28-8fa7-9e48c805c501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d26e0c1d1e48596cb9acef740405c797f6f0f46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311296"
---
# <a name="containmentdelegation"></a><span data-ttu-id="24e9a-103">Imbrication/délégation</span><span class="sxs-lookup"><span data-stu-id="24e9a-103">Containment/Delegation</span></span>

<span data-ttu-id="24e9a-104">Le mécanisme le plus courant pour la réutilisation d’objets dans COM est la *relation contenant-contenu et la délégation*.</span><span class="sxs-lookup"><span data-stu-id="24e9a-104">The most common mechanism for object reuse in COM is *containment/delegation*.</span></span> <span data-ttu-id="24e9a-105">Ce type de réutilisation est un concept familier trouvé dans la plupart des langages et systèmes orientés objet.</span><span class="sxs-lookup"><span data-stu-id="24e9a-105">This type of reuse is a familiar concept found in most object-oriented languages and systems.</span></span> <span data-ttu-id="24e9a-106">L’objet externe, qui doit utiliser l’objet interne, agit comme un client d’objet pour l’objet interne.</span><span class="sxs-lookup"><span data-stu-id="24e9a-106">The outer object, which needs to make use of the inner object, acts as an object client to the inner object.</span></span> <span data-ttu-id="24e9a-107">L’objet externe « contient » l’objet interne et, lorsque l’objet externe requiert les services de l’objet interne, l’objet externe délègue explicitement l’implémentation aux méthodes de l’objet interne.</span><span class="sxs-lookup"><span data-stu-id="24e9a-107">The outer object "contains" the inner object, and when the outer object requires the services of the inner object, the outer object explicitly delegates implementation to the inner object's methods.</span></span> <span data-ttu-id="24e9a-108">Autrement dit, l’objet externe utilise les services de l’objet interne pour implémenter lui-même.</span><span class="sxs-lookup"><span data-stu-id="24e9a-108">That is, the outer object uses the inner object's services to implement itself.</span></span>

<span data-ttu-id="24e9a-109">Il n’est pas nécessaire que les objets externes et internes prennent en charge les mêmes interfaces, bien qu’il soit certainement raisonnable de contenir un objet qui implémente une interface que l’objet externe n’utilise pas et qui implémentent simplement les méthodes de l’objet externe comme des appels aux méthodes correspondantes dans l’objet interne.</span><span class="sxs-lookup"><span data-stu-id="24e9a-109">It is not necessary for the outer and inner objects to support the same interfaces, although it certainly is reasonable to contain an object that implements an interface that the outer object does not and implement the methods of the outer object simply as calls to the corresponding methods in the inner object.</span></span> <span data-ttu-id="24e9a-110">Toutefois, lorsque la complexité des objets externes et internes diffère sensiblement, l’objet externe peut implémenter certaines des méthodes de ses interfaces en déléguant les appels aux méthodes d’interface implémentées dans l’objet interne.</span><span class="sxs-lookup"><span data-stu-id="24e9a-110">When the complexity of the outer and inner objects differs greatly, however, the outer object may implement some of the methods of its interfaces by delegating calls to interface methods implemented in the inner object.</span></span>

<span data-ttu-id="24e9a-111">Il est facile d’implémenter la relation contenant-contenu pour un objet externe.</span><span class="sxs-lookup"><span data-stu-id="24e9a-111">It is simple to implement containment for an outer object.</span></span> <span data-ttu-id="24e9a-112">L’objet externe crée les objets internes qu’il doit utiliser comme n’importe quel autre client.</span><span class="sxs-lookup"><span data-stu-id="24e9a-112">The outer object creates the inner objects it needs to use as any other client would.</span></span> <span data-ttu-id="24e9a-113">Ce n’est rien de nouveau : le processus est comme un objet C++ qui contient lui-même un objet de chaîne C++ qu’il utilise pour exécuter certaines fonctions de chaîne, même si l’objet externe n’est pas considéré comme un objet de chaîne dans son propre droit.</span><span class="sxs-lookup"><span data-stu-id="24e9a-113">This is nothing new—the process is like a C++ object that itself contains a C++ string object that it uses to perform certain string functions, even if the outer object is not considered a string object in its own right.</span></span> <span data-ttu-id="24e9a-114">Ensuite, à l’aide de son pointeur vers l’objet interne, un appel à une méthode dans l’objet externe génère un appel à une méthode d’objet interne.</span><span class="sxs-lookup"><span data-stu-id="24e9a-114">Then, using its pointer to the inner object, a call to a method in the outer object generates a call to an inner object method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24e9a-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="24e9a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24e9a-116">Agrégation</span><span class="sxs-lookup"><span data-stu-id="24e9a-116">Aggregation</span></span>](aggregation.md)
</dt> </dl>

 

 




