---
title: Création d’objets proxy
description: En plus de concevoir des classes qui implémentent des propriétés et des méthodes IAccessible, les développeurs de serveurs peuvent également être amenés à concevoir des objets proxy qui surveillent la durée de vie des objets accessibles.
ms.assetid: d140206a-9918-438b-96bd-df141da2f04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e005af4f02430376bc013a45c68cdecef8c0feba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671902"
---
# <a name="creating-proxy-objects"></a><span data-ttu-id="e0115-103">Création d’objets proxy</span><span class="sxs-lookup"><span data-stu-id="e0115-103">Creating Proxy Objects</span></span>

<span data-ttu-id="e0115-104">En plus de concevoir des classes qui implémentent des propriétés et des méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , les développeurs de serveurs peuvent également être amenés à concevoir des objets *proxy* qui surveillent la durée de vie des objets accessibles.</span><span class="sxs-lookup"><span data-stu-id="e0115-104">In addition to designing classes that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods, server developers may also need to design *proxy* objects that monitor the life span of accessible objects.</span></span> <span data-ttu-id="e0115-105">Si un objet accessible dans une application est disponible pendant toute la durée d’exécution de l’application, vous n’avez pas besoin de créer un objet proxy.</span><span class="sxs-lookup"><span data-stu-id="e0115-105">If an accessible object in an application is available the entire time the application is running, then you do not need to create a proxy object.</span></span> <span data-ttu-id="e0115-106">S’il est possible de détruire l’objet accessible pendant que l’application est en cours d’exécution, vous devez créer un objet proxy.</span><span class="sxs-lookup"><span data-stu-id="e0115-106">If it is possible to destroy the accessible object while the application is running, then you must create a proxy object.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e0115-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="e0115-107">In this section</span></span>

-   [<span data-ttu-id="e0115-108">Que sont les objets proxy ?</span><span class="sxs-lookup"><span data-stu-id="e0115-108">What Are Proxy Objects?</span></span>](what-are-proxy-objects.md)
-   [<span data-ttu-id="e0115-109">Raisons pour lesquelles les objets proxy sont nécessaires</span><span class="sxs-lookup"><span data-stu-id="e0115-109">Why Proxy Objects Are Needed</span></span>](why-proxy-objects-are-needed.md)
-   [<span data-ttu-id="e0115-110">Considérations relatives à la conception des objets proxy</span><span class="sxs-lookup"><span data-stu-id="e0115-110">Design Considerations for Proxy Objects</span></span>](design-considerations-for-proxy-objects.md)

 

 




