---
title: Fournisseurs de moniker
description: Fournisseurs de moniker
ms.assetid: 4d4820d2-bf5f-4543-b318-59481dcc51de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde584e12daddacbc940b23b21a0386aa37de2c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673101"
---
# <a name="moniker-providers"></a><span data-ttu-id="9835c-103">Fournisseurs de moniker</span><span class="sxs-lookup"><span data-stu-id="9835c-103">Moniker Providers</span></span>

<span data-ttu-id="9835c-104">En général, un composant doit être un fournisseur de monikers lorsqu’il autorise l’accès à l’un de ses objets, tout en contrôlant encore le stockage de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9835c-104">In general, a component should be a moniker provider when it allows access to one of its objects, while still controlling the object's storage.</span></span> <span data-ttu-id="9835c-105">Si un composant va distribuer des monikers qui identifient ses objets, il doit être capable d’effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="9835c-105">If a component is going to hand out monikers that identify its objects, it must be capable of performing the following tasks:</span></span>

-   <span data-ttu-id="9835c-106">Sur demande, créez un moniker qui identifie un objet.</span><span class="sxs-lookup"><span data-stu-id="9835c-106">On request, create a moniker that identifies an object.</span></span>
-   <span data-ttu-id="9835c-107">Permet au moniker d’être lié lorsqu’un client appelle [**IMoniker :: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) sur celui-ci.</span><span class="sxs-lookup"><span data-stu-id="9835c-107">Enable the moniker to be bound when a client calls [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) on it.</span></span>

<span data-ttu-id="9835c-108">Un fournisseur de monikers doit créer un moniker d’une *classe de moniker* appropriée pour identifier un objet.</span><span class="sxs-lookup"><span data-stu-id="9835c-108">A moniker provider must create a moniker of an appropriate *moniker class* to identify an object.</span></span> <span data-ttu-id="9835c-109">La classe moniker fait référence à une implémentation spécifique de l’interface [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) qui définit le type de moniker créé.</span><span class="sxs-lookup"><span data-stu-id="9835c-109">The moniker class refers to a specific implementation of the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface that defines the type of moniker created.</span></span> <span data-ttu-id="9835c-110">Bien que vous puissiez implémenter **IMoniker** pour créer une nouvelle classe moniker, il est souvent inutile, car OLE fournit des implémentations de plusieurs classes de moniker, chacune avec son propre CLSID.</span><span class="sxs-lookup"><span data-stu-id="9835c-110">While you can implement **IMoniker** to create a new moniker class, it is frequently unnecessary because OLE provides implementations of several different moniker classes, each with its own CLSID.</span></span> <span data-ttu-id="9835c-111">Pour obtenir les descriptions des classes moniker fournies par OLE, consultez [implémentations de moniker OLE](ole-moniker-implementations.md) .</span><span class="sxs-lookup"><span data-stu-id="9835c-111">See [OLE Moniker Implementations](ole-moniker-implementations.md) for descriptions of moniker classes that OLE provides.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9835c-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9835c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9835c-113">Clients moniker</span><span class="sxs-lookup"><span data-stu-id="9835c-113">Moniker Clients</span></span>](moniker-clients.md)
</dt> <dt>

[<span data-ttu-id="9835c-114">Implémentations du moniker OLE</span><span class="sxs-lookup"><span data-stu-id="9835c-114">OLE Moniker Implementations</span></span>](ole-moniker-implementations.md)
</dt> </dl>

 

 




