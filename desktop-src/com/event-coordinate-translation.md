---
title: Traduction de la coordonnée d’événement
description: Traduction de la coordonnée d’événement
ms.assetid: e7de8af1-a409-4140-9e85-e035bd583912
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c40a742ead8fc8d7e431c1caa5210f0978168cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675013"
---
# <a name="event-coordinate-translation"></a><span data-ttu-id="f61e3-103">Traduction de la coordonnée d’événement</span><span class="sxs-lookup"><span data-stu-id="f61e3-103">Event Coordinate Translation</span></span>

<span data-ttu-id="f61e3-104">La spécification 96 pour les contrôles exige que les coordonnées passées pour les événements déclenchés par le contrôle changent d’être HIMETRIC à des points basés.</span><span class="sxs-lookup"><span data-stu-id="f61e3-104">The 96 specification for controls requires that coordinates passed for events fired by the control change from being HIMETRIC to being points based.</span></span> <span data-ttu-id="f61e3-105">Cette modification amène l’événement à passer des coordonnées en ligne avec les propriétés et les méthodes et, par conséquent, la coordination de la correspondance n’est plus la responsabilité du conteneur.</span><span class="sxs-lookup"><span data-stu-id="f61e3-105">This change brings the event passing of coordinates in line with properties and methods and thus coordinate translation is no longer the responsibility of the container.</span></span> <span data-ttu-id="f61e3-106">Cela soulève certains problèmes de compatibilité lorsqu’un contrôle déclenche des événements à l’aide d’une base de coordonnées qu’il n’attend pas, cela ne doit être qu’un problème où un conteneur de contrôle 96 héberge un contrôle antérieur à 96, comme suit :</span><span class="sxs-lookup"><span data-stu-id="f61e3-106">This raises certain compatibility issues where a control fires events using a coordinate base that it is not expecting, this should only be an issue where a 96 control container is hosting an older pre-96 control as follows:</span></span>

-   <span data-ttu-id="f61e3-107">Quand un conteneur antérieur à 96 héberge un contrôle 96, le contrôle présente les coordonnées d’événement en tant que points. cela ne doit pas entraîner de problèmes au niveau du conteneur, car le conteneur doit reconnaître le type de paramètre.</span><span class="sxs-lookup"><span data-stu-id="f61e3-107">When an older pre-96 container hosts a 96 control the control will present the event coordinates as points, this should not cause the container any problems as the container should recognize the parameter type.</span></span>
-   <span data-ttu-id="f61e3-108">Quand un conteneur 96 héberge un contrôle antérieur à 96, le contrôle présente le conteneur avec des coordonnées et s’attend à ce que la traduction du conteneur soit nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f61e3-108">When a 96 container hosts a pre-96 control the control will present the container with coordinates and expect the container to any translation necessary.</span></span> <span data-ttu-id="f61e3-109">Toutefois, le conteneur 96 attendra un contrôle pour se conformer à la spécification de contrôles 96 et présentera ses coordonnées en tant que points.</span><span class="sxs-lookup"><span data-stu-id="f61e3-109">However the 96 container will be expecting a control to conform to the 96 controls specification and present its coordinates as points.</span></span> <span data-ttu-id="f61e3-110">Le contrôle utilise la méthode [**TransformCoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) sur l’interface [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) fournie par le conteneur de la même façon que pour les propriétés et les méthodes pour y parvenir.</span><span class="sxs-lookup"><span data-stu-id="f61e3-110">The control uses the [**TransformCoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) method on the [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) interface provided by the container in the same way as it does for properties and methods to achieve this.</span></span>

<span data-ttu-id="f61e3-111">Par conséquent, l’utilisateur d’un conteneur 96 hébergeant des contrôles antérieurs à 96 devra savoir qu’une traduction supplémentaire de coordonnées peut être nécessaire lorsque des événements sont déclenchés.</span><span class="sxs-lookup"><span data-stu-id="f61e3-111">As a result the user of a 96 container hosting pre-96 controls will need to be aware that further translation of coordinates may be necessary when events are fired.</span></span>

 

 




