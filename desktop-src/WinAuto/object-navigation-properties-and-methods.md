---
title: Propriétés et méthodes de navigation entre les objets
description: Les clients naviguent d’un objet à un autre à l’aide de méthodes telles que IAccessible accNavigate et IAccessible accHitTest.
ms.assetid: c6bcd044-bf70-4eec-92ae-66f9bd836c33
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7645d5179015280fd40f6618722191e588c74a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939861"
---
# <a name="object-navigation-properties-and-methods"></a><span data-ttu-id="74603-103">Propriétés et méthodes de navigation entre les objets</span><span class="sxs-lookup"><span data-stu-id="74603-103">Object Navigation Properties and Methods</span></span>

<span data-ttu-id="74603-104">Les clients *naviguent* d’un objet à un autre à l’aide de méthodes telles que [**IAccessible :: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) et [**IAccessible :: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest).</span><span class="sxs-lookup"><span data-stu-id="74603-104">Clients *navigate* from one object to another using methods such as [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) and [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest).</span></span> <span data-ttu-id="74603-105">Ces méthodes permettent aux clients de récupérer un ID enfant ou l’adresse de l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) d’un autre objet.</span><span class="sxs-lookup"><span data-stu-id="74603-105">These methods allow clients to retrieve either a child ID or the address of another object's [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="74603-106">La navigation permet aux clients d’explorer les relations entre les objets.</span><span class="sxs-lookup"><span data-stu-id="74603-106">Navigation allows clients to explore how objects are related to each other.</span></span> <span data-ttu-id="74603-107">Notez que la navigation vers un autre objet ne modifie pas la sélection ou le focus.</span><span class="sxs-lookup"><span data-stu-id="74603-107">Note that navigating to another object does not change the selection or focus.</span></span>

<span data-ttu-id="74603-108">L’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) fournit des propriétés et des méthodes qui prennent en charge les types de navigation suivants :</span><span class="sxs-lookup"><span data-stu-id="74603-108">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface provides properties and methods that support the following kinds of navigation:</span></span>

-   [<span data-ttu-id="74603-109">Navigation hiérarchique</span><span class="sxs-lookup"><span data-stu-id="74603-109">Hierarchical Navigation</span></span>](hierarchical-navigation.md)
-   [<span data-ttu-id="74603-110">Navigation spatiale et logique</span><span class="sxs-lookup"><span data-stu-id="74603-110">Spatial and Logical Navigation</span></span>](spatial-and-logical-navigation.md)
-   [<span data-ttu-id="74603-111">Navigation via le test de positionnement et l’emplacement à l’écran</span><span class="sxs-lookup"><span data-stu-id="74603-111">Navigation Through Hit Testing and Screen Location</span></span>](navigation-through-hit-testing-and-screen-location.md)

 

 




