---
title: Interfaces d’objets connectables
description: Interfaces d’objets connectables
ms.assetid: 136fb7bd-7a38-4051-b47b-3d08f1dbee79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc2d747d7aabe25788c34d80bddb8ca1466e9c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840793"
---
# <a name="connectable-object-interfaces"></a><span data-ttu-id="a7ea9-103">Interfaces d’objets connectables</span><span class="sxs-lookup"><span data-stu-id="a7ea9-103">Connectable Object Interfaces</span></span>

<span data-ttu-id="a7ea9-104">La prise en charge des objets connectables nécessite la prise en charge de quatre interfaces :</span><span class="sxs-lookup"><span data-stu-id="a7ea9-104">Support for connectable objects requires support for four interfaces:</span></span>

-   <span data-ttu-id="a7ea9-105">[**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) sur l’objet connectable</span><span class="sxs-lookup"><span data-stu-id="a7ea9-105">[**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) on the connectable object</span></span>
-   <span data-ttu-id="a7ea9-106">[**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) sur l’objet point de connexion</span><span class="sxs-lookup"><span data-stu-id="a7ea9-106">[**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) on the connection point object</span></span>
-   <span data-ttu-id="a7ea9-107">[**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) sur un objet énumérateur</span><span class="sxs-lookup"><span data-stu-id="a7ea9-107">[**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) on an enumerator object</span></span>
-   <span data-ttu-id="a7ea9-108">[**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) sur un objet énumérateur</span><span class="sxs-lookup"><span data-stu-id="a7ea9-108">[**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) on an enumerator object</span></span>

<span data-ttu-id="a7ea9-109">Les deux derniers sont définis en tant qu’énumérateurs standard pour les types **IConnectionPoint \*** et [**CONNECTDATA**](/windows/win32/api/ocidl/ns-ocidl-connectdata).</span><span class="sxs-lookup"><span data-stu-id="a7ea9-109">The latter two are defined as standard enumerators for the types **IConnectionPoint \*** and [**CONNECTDATA**](/windows/win32/api/ocidl/ns-ocidl-connectdata).</span></span>

<span data-ttu-id="a7ea9-110">En outre, l’objet connectable peut éventuellement prendre en charge [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) et [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) pour fournir suffisamment d’informations à un client afin que le client puisse assurer la prise en charge de l’interface sortante au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="a7ea9-110">Additionally, the connectable object can optionally support [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) and [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) to provide enough information to a client so that the client can provide support for the outgoing interface at run time.</span></span>

<span data-ttu-id="a7ea9-111">Enfin, le client doit fournir un objet récepteur qui implémente l’interface sortante, qui est une interface COM personnalisée définie par l’objet connectable.</span><span class="sxs-lookup"><span data-stu-id="a7ea9-111">Finally, the client must provide a sink object that implements the outgoing interface, which is a custom COM interface defined by the connectable object.</span></span>

<span data-ttu-id="a7ea9-112">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="a7ea9-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="a7ea9-113">Utilisation de IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="a7ea9-113">Using IConnectionPointContainer</span></span>](using-iconnectionpointcontainer.md)
-   [<span data-ttu-id="a7ea9-114">Utilisation de IConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="a7ea9-114">Using IConnectionPoint</span></span>](using-iconnectionpoint.md)
-   [<span data-ttu-id="a7ea9-115">Utilisation de IProvideClassInfo</span><span class="sxs-lookup"><span data-stu-id="a7ea9-115">Using IProvideClassInfo</span></span>](using-iprovideclassinfo.md)

## <a name="related-topics"></a><span data-ttu-id="a7ea9-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a7ea9-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7ea9-117">Architecture des objets connectables</span><span class="sxs-lookup"><span data-stu-id="a7ea9-117">Architecture of Connectable Objects</span></span>](architecture-of-connectable-objects.md)
</dt> </dl>

 

 




