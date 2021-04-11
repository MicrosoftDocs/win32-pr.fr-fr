---
title: Monikers
description: Un moniker dans COM n’est pas seulement un moyen d’identifier un objet \ 8212 ; un moniker est également implémenté comme un objet.
ms.assetid: ae0cd2f3-8ac0-4388-8781-e86fc4a26b3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf148d63611b5252eec9f5f5f69eacbcece8c65f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028643"
---
# <a name="monikers"></a><span data-ttu-id="4d5bb-103">Monikers</span><span class="sxs-lookup"><span data-stu-id="4d5bb-103">Monikers</span></span>

<span data-ttu-id="4d5bb-104">Un moniker dans COM n’est pas seulement un moyen d’identifier un objet : un moniker est également implémenté comme un objet.</span><span class="sxs-lookup"><span data-stu-id="4d5bb-104">A moniker in COM is not only a way to identify an object—a moniker is also implemented as an object.</span></span> <span data-ttu-id="4d5bb-105">Cet objet fournit des services qui permettent à un composant d’obtenir un pointeur vers l’objet identifié par le moniker.</span><span class="sxs-lookup"><span data-stu-id="4d5bb-105">This object provides services allowing a component to obtain a pointer to the object identified by the moniker.</span></span> <span data-ttu-id="4d5bb-106">Ce processus est appelé *liaison*.</span><span class="sxs-lookup"><span data-stu-id="4d5bb-106">This process is referred to as *binding*.</span></span>

<span data-ttu-id="4d5bb-107">Les monikers sont des objets qui implémentent l’interface [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) et sont généralement implémentés dans des dll en tant qu’objets de composant.</span><span class="sxs-lookup"><span data-stu-id="4d5bb-107">Monikers are objects that implement the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface and are generally implemented in DLLs as component objects.</span></span> <span data-ttu-id="4d5bb-108">Il existe deux façons d’afficher l’utilisation des monikers : en tant que client moniker, composant qui utilise un moniker pour obtenir un pointeur vers un autre objet ; et en tant que fournisseur de monikers, un composant qui fournit des monikers identifiant ses objets aux clients monikers.</span><span class="sxs-lookup"><span data-stu-id="4d5bb-108">There are two ways of viewing the use of monikers: as a moniker client, a component that uses a moniker to get a pointer to another object; and as a moniker provider, a component that supplies monikers identifying its objects to moniker clients.</span></span>

<span data-ttu-id="4d5bb-109">OLE utilise des monikers pour se connecter aux objets et les activer, qu’ils se trouvent sur le même ordinateur ou sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="4d5bb-109">OLE uses monikers to connect to and activate objects, whether they are in the same machine or across a network.</span></span> <span data-ttu-id="4d5bb-110">Une utilisation très importante concerne les connexions réseau.</span><span class="sxs-lookup"><span data-stu-id="4d5bb-110">A very important use is for network connections.</span></span> <span data-ttu-id="4d5bb-111">Elles servent également à identifier, à se connecter à et à exécuter des objets de lien de document composé OLE.</span><span class="sxs-lookup"><span data-stu-id="4d5bb-111">They are also used to identify, connect to, and run OLE compound document link objects.</span></span> <span data-ttu-id="4d5bb-112">Dans ce cas, la source de lien joue le rôle de fournisseur de moniker et le conteneur qui contient l’objet Link agit en tant que client moniker.</span><span class="sxs-lookup"><span data-stu-id="4d5bb-112">In this case, the link source acts as the moniker provider and the container holding the link object acts as the moniker client.</span></span>

<span data-ttu-id="4d5bb-113">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="4d5bb-113">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="4d5bb-114">Clients moniker</span><span class="sxs-lookup"><span data-stu-id="4d5bb-114">Moniker Clients</span></span>](moniker-clients.md)
-   [<span data-ttu-id="4d5bb-115">Fournisseurs de moniker</span><span class="sxs-lookup"><span data-stu-id="4d5bb-115">Moniker Providers</span></span>](moniker-providers.md)
-   [<span data-ttu-id="4d5bb-116">Implémentations du moniker OLE</span><span class="sxs-lookup"><span data-stu-id="4d5bb-116">OLE Moniker Implementations</span></span>](ole-moniker-implementations.md)

## <a name="related-topics"></a><span data-ttu-id="4d5bb-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4d5bb-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d5bb-118">COM (Component Object Model)</span><span class="sxs-lookup"><span data-stu-id="4d5bb-118">The Component Object Model</span></span>](the-component-object-model.md)
</dt> </dl>

 

 




