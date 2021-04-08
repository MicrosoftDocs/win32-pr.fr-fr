---
title: Architecture des contrôles ActiveX
description: La technologie des contrôles ActiveX s’appuie sur une base de nombreux objets et interfaces de niveau inférieur dans OLE. Les interfaces exactes disponibles sur un contrôle varient en fonction de ses capacités. Cette section examine de plus près les fonctionnalités qu’un contrôle peut fournir.
ms.assetid: 42959a11-8bfb-4f7e-ba27-5dc1ed49cdaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0592d774e1930623803d0769fb7890709a2f21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672569"
---
# <a name="activex-controls-architecture"></a><span data-ttu-id="c5dc0-105">Architecture des contrôles ActiveX</span><span class="sxs-lookup"><span data-stu-id="c5dc0-105">ActiveX Controls Architecture</span></span>

<span data-ttu-id="c5dc0-106">La technologie des contrôles ActiveX s’appuie sur une base de nombreux objets et interfaces de niveau inférieur dans OLE.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-106">ActiveX controls technology builds on a foundation of many lower-level objects and interfaces in OLE.</span></span> <span data-ttu-id="c5dc0-107">Les interfaces exactes disponibles sur un contrôle varient en fonction de ses capacités.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-107">The exact interfaces available on a control vary with its capabilities.</span></span> <span data-ttu-id="c5dc0-108">Cette section examine de plus près les fonctionnalités qu’un contrôle peut fournir.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-108">This section takes a closer look at the capabilities a control might provide.</span></span>

<span data-ttu-id="c5dc0-109">Les contrôles ActiveX sont utilisés pour fournir les blocs de construction permettant de créer des interfaces utilisateur dans des applications.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-109">ActiveX controls are used to provide the building blocks for creating user interfaces in applications.</span></span> <span data-ttu-id="c5dc0-110">Par exemple, un bouton qui lance une action dans l’application conteneur quand l’utilisateur clique dessus est un contrôle simple.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-110">For example, a button that initiates some action in the container application when it is clicked is a simple control.</span></span> <span data-ttu-id="c5dc0-111">Les aspects suivants sont impliqués dans la fourniture de ces blocs de construction d’interface utilisateur :</span><span class="sxs-lookup"><span data-stu-id="c5dc0-111">The following aspects are involved in providing these user interface building blocks:</span></span>

-   <span data-ttu-id="c5dc0-112">Un contrôle peut être incorporé dans son client de conteneur pour prendre en charge une activité de l’interface utilisateur au sein du client.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-112">A control can be embedded within its container client to support some user interface activity within the client.</span></span> <span data-ttu-id="c5dc0-113">Ainsi, un contrôle doit fournir une représentation visuelle de lui-même lorsqu’il est incorporé dans le conteneur et doit fournir un moyen d’enregistrer son état, par exemple ses valeurs de propriété et sa position dans son conteneur.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-113">Thus, a control needs to provide a visual representation of itself when it is embedded within the container and needs to provide a way to save its state, for example, its property values and its position within its container.</span></span> <span data-ttu-id="c5dc0-114">Le client doit prendre en charge un conteneur avec des objets incorporés dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-114">The client must support being a container with objects embedded in it.</span></span>
-   <span data-ttu-id="c5dc0-115">En activant le contrôle à l’aide d’un clavier ou d’une souris, l’utilisateur final lance une action dans l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-115">By activating the control using a keyboard or mouse, the end user initiates some action in the client application.</span></span> <span data-ttu-id="c5dc0-116">Ainsi, un contrôle doit répondre à l’activité du clavier et doit être en mesure de communiquer avec son client pour qu’il puisse notifier son conteneur de ses activités et déclencher des événements dans le client.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-116">Thus, a control must respond to keyboard activity and must be able to communicate with its client so it can notify its container of its activities and trigger events in the client.</span></span>
-   <span data-ttu-id="c5dc0-117">Le client fournit également un langage de programmation par le biais duquel l’utilisateur final peut lancer des actions fournies par les propriétés et les méthodes du contrôle.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-117">The client also typically provides a programming language through which the end user can initiate actions provided by the control's properties and methods.</span></span> <span data-ttu-id="c5dc0-118">Par conséquent, un contrôle doit prendre en charge l’automatisation et un ensemble de fonctionnalités au moment du design plutôt qu’au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-118">Thus, a control must support automation and some set of design-time versus run-time features as well.</span></span>

<span data-ttu-id="c5dc0-119">En raison de son rôle dans la fourniture des blocs de construction de l’interface utilisateur, un contrôle prend généralement en charge les fonctionnalités dans les domaines suivants à l’aide des technologies OLE, comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="c5dc0-119">As a result of its role in providing user interface building blocks, a control typically supports features in the following areas using OLE technologies as indicated:</span></span>

<dl> <dt>

<span data-ttu-id="c5dc0-120"><span id="Properties_and_methods"></span><span id="properties_and_methods"></span><span id="PROPERTIES_AND_METHODS"></span>Propriétés et méthodes</span><span class="sxs-lookup"><span data-stu-id="c5dc0-120"><span id="Properties_and_methods"></span><span id="properties_and_methods"></span><span id="PROPERTIES_AND_METHODS"></span>Properties and methods</span></span>
</dt> <dd>

<span data-ttu-id="c5dc0-121">Comme tout objet OLE, un contrôle peut fournir une grande partie de ses fonctionnalités via un ensemble d’interfaces entrantes avec des propriétés et des méthodes.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-121">Like any OLE object, a control can provide much of its functionality through a set of incoming interfaces with properties and methods.</span></span> <span data-ttu-id="c5dc0-122">Le conteneur peut fournir des propriétés ambiantes supplémentaires et peut prendre en charge l’extension des propriétés du contrôle par le biais de l’agrégation.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-122">The container can supply additional ambient properties, and it can support extending the control's properties through aggregation.</span></span> <span data-ttu-id="c5dc0-123">Ces fonctionnalités reposent sur OLE Automation, les pages de propriétés, les objets connectables et les technologies de contrôle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-123">These features rest on OLE automation, property pages, connectable objects, and ActiveX control technologies.</span></span>

</dd> <dt>

<span data-ttu-id="c5dc0-124"><span id="Events"></span><span id="events"></span><span id="EVENTS"></span>Événements</span><span class="sxs-lookup"><span data-stu-id="c5dc0-124"><span id="Events"></span><span id="events"></span><span id="EVENTS"></span>Events</span></span>
</dt> <dd>

<span data-ttu-id="c5dc0-125">En plus de fournir des propriétés et des méthodes, un contrôle ActiveX peut également fournir des interfaces sortantes pour notifier son client d’événements.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-125">In addition to providing properties and methods, an ActiveX control can also provide outgoing interfaces to notify its client of events.</span></span> <span data-ttu-id="c5dc0-126">Le client doit prendre en charge la gestion de ces événements.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-126">The client must support handling of these events.</span></span> <span data-ttu-id="c5dc0-127">Ces fonctionnalités utilisent l’automatisation OLE et les objets connectables.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-127">These features use OLE automation and connectable objects.</span></span>

</dd> <dt>

<span data-ttu-id="c5dc0-128"><span id="Visual_representation"></span><span id="visual_representation"></span><span id="VISUAL_REPRESENTATION"></span>Représentation visuelle</span><span class="sxs-lookup"><span data-stu-id="c5dc0-128"><span id="Visual_representation"></span><span id="visual_representation"></span><span id="VISUAL_REPRESENTATION"></span>Visual representation</span></span>
</dt> <dd>

<span data-ttu-id="c5dc0-129">Un contrôle peut prendre en charge le positionnement et s’afficher dans son conteneur.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-129">A control can support positioning and displaying itself within its container.</span></span> <span data-ttu-id="c5dc0-130">Le conteneur positionne le contrôle et détermine sa taille.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-130">The container positions the control and determines its size.</span></span> <span data-ttu-id="c5dc0-131">Ces fonctionnalités utilisent la technologie de document composé, y compris la technologie glisser-déplacer OLE.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-131">These features use compound document technology, including OLE drag and drop technology.</span></span>

</dd> <dt>

<span data-ttu-id="c5dc0-132"><span id="Keyboard_handling"></span><span id="keyboard_handling"></span><span id="KEYBOARD_HANDLING"></span>Gestion du clavier</span><span class="sxs-lookup"><span data-stu-id="c5dc0-132"><span id="Keyboard_handling"></span><span id="keyboard_handling"></span><span id="KEYBOARD_HANDLING"></span>Keyboard handling</span></span>
</dt> <dd>

<span data-ttu-id="c5dc0-133">Un contrôle peut répondre aux accélérateurs de clavier afin que l’utilisateur final puisse lancer des actions effectuées par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-133">A control can respond to keyboard accelerators so the end-user can initiate actions performed by the control.</span></span> <span data-ttu-id="c5dc0-134">Le conteneur gère l’activité du clavier pour tous ses contrôles incorporés.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-134">The container manages keyboard activity for all its embedded controls.</span></span> <span data-ttu-id="c5dc0-135">Ces fonctionnalités utilisent les technologies de contrôle et de document composé.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-135">These features use control and compound document technologies.</span></span>

</dd> <dt>

<span data-ttu-id="c5dc0-136"><span id="Persistence"></span><span id="persistence"></span><span id="PERSISTENCE"></span>Persistance</span><span class="sxs-lookup"><span data-stu-id="c5dc0-136"><span id="Persistence"></span><span id="persistence"></span><span id="PERSISTENCE"></span>Persistence</span></span>
</dt> <dd>

<span data-ttu-id="c5dc0-137">Un contrôle peut enregistrer son état.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-137">A control can save its state.</span></span> <span data-ttu-id="c5dc0-138">Le client gère la persistance de ses contrôles incorporés.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-138">The client manages the persistence of its embedded controls.</span></span> <span data-ttu-id="c5dc0-139">Ces fonctionnalités utilisent le stockage structuré et les technologies de persistance des objets.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-139">These features use structured storage and object persistence technologies.</span></span>

</dd> <dt>

<span data-ttu-id="c5dc0-140"><span id="Registration_and_licensing"></span><span id="registration_and_licensing"></span><span id="REGISTRATION_AND_LICENSING"></span>Inscription et licences</span><span class="sxs-lookup"><span data-stu-id="c5dc0-140"><span id="Registration_and_licensing"></span><span id="registration_and_licensing"></span><span id="REGISTRATION_AND_LICENSING"></span>Registration and licensing</span></span>
</dt> <dd>

<span data-ttu-id="c5dc0-141">En général, un contrôle prend en charge l’inscription automatique et crée un jeu d’entrées de Registre lorsqu’il est instancié.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-141">A control typically supports self-registration and creates a set of registry entries when it is instantiated.</span></span> <span data-ttu-id="c5dc0-142">Un contrôle peut également être concédé sous licence pour empêcher toute utilisation non autorisée.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-142">A control can also be licensed to help prevent unauthorized use.</span></span>

</dd> </dl>

<span data-ttu-id="c5dc0-143">La plupart de ces fonctionnalités impliquent à la fois le contrôle et son conteneur client.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-143">Most of these features involve both the control and its client container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5dc0-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c5dc0-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5dc0-145">Contrôles ActiveX</span><span class="sxs-lookup"><span data-stu-id="c5dc0-145">ActiveX Controls</span></span>](activex-controls.md)
</dt> </dl>

 

 




