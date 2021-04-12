---
title: Définition des catégories de composants
description: Définition des catégories de composants
ms.assetid: 2d67a998-5200-4285-bd99-48cf59683569
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4609654827789949705a2f32803c154152d3f9c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197453"
---
# <a name="defining-component-categories"></a><span data-ttu-id="458bc-103">Définition des catégories de composants</span><span class="sxs-lookup"><span data-stu-id="458bc-103">Defining Component Categories</span></span>

<span data-ttu-id="458bc-104">L’auteur d’une définition de catégorie de composant crée un GUID unique (le CATID) qui est publié avec la définition.</span><span class="sxs-lookup"><span data-stu-id="458bc-104">The author of a component category definition creates a unique GUID (the CATID) that is published along with the definition.</span></span> <span data-ttu-id="458bc-105">Les autres parties connaissent la définition de ce type et peuvent utiliser ses classes prises en charge en conséquence.</span><span class="sxs-lookup"><span data-stu-id="458bc-105">Other parties know the definition of this type and can make use of its supported classes accordingly.</span></span> <span data-ttu-id="458bc-106">À l’instar de la signature de méthode d’une interface, la sémantique d’une catégorie ne doit pas être modifiée après son installation.</span><span class="sxs-lookup"><span data-stu-id="458bc-106">Like the method signature of an interface, a category's semantics should not be modified after being installed.</span></span> <span data-ttu-id="458bc-107">Il est préférable de conserver la compatibilité descendante de la catégorie en introduisant un nouvel identificateur de catégorie avec la sémantique révisée.</span><span class="sxs-lookup"><span data-stu-id="458bc-107">It is better to maintain backward compatibility of the category by introducing a new category identifier with revised semantics.</span></span>

<span data-ttu-id="458bc-108">Étant donné que les identificateurs d’interface (IID) et les identificateurs de catégories de composants (CATID) existent dans des espaces de noms différents, il semble qu’il soit possible d’utiliser le même GUID pour un IID et un CATID.</span><span class="sxs-lookup"><span data-stu-id="458bc-108">Because interface identifiers (IID) and component category identifiers (CATID) exist in different namespaces, it seems as if it would be possible to use the same GUID for both an IID and a CATID.</span></span> <span data-ttu-id="458bc-109">Toutefois, étant donné que les IID sont souvent utilisés pour le CLSID du serveur proxy/stub de l’interface, il y a un risque de conflit.</span><span class="sxs-lookup"><span data-stu-id="458bc-109">However, since IIDs are often used for the CLSID of the interface's proxy/stub server, there is the potential for conflict.</span></span> <span data-ttu-id="458bc-110">Par conséquent, n’utilisez pas le même GUID pour un IID et un CATID.</span><span class="sxs-lookup"><span data-stu-id="458bc-110">Therefore, do not use the same GUID for an IID and CATID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="458bc-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="458bc-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="458bc-112">Association d’icônes à une catégorie</span><span class="sxs-lookup"><span data-stu-id="458bc-112">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="458bc-113">Catégorisation par fonctionnalités de composant</span><span class="sxs-lookup"><span data-stu-id="458bc-113">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="458bc-114">Catégorisation par fonctionnalités de conteneur</span><span class="sxs-lookup"><span data-stu-id="458bc-114">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="458bc-115">Classes et associations par défaut</span><span class="sxs-lookup"><span data-stu-id="458bc-115">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="458bc-116">Gestionnaire de catégories de composants</span><span class="sxs-lookup"><span data-stu-id="458bc-116">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




