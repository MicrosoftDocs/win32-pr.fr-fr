---
title: Contrôles (COM)
description: Commandes
ms.assetid: 73947c81-6727-4112-9da0-efa60360f458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f440fff8f855f70c1a5ab3df78a6f6f6ed365ea
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104316974"
---
# <a name="controls-com"></a><span data-ttu-id="0a994-103">Contrôles (COM)</span><span class="sxs-lookup"><span data-stu-id="0a994-103">Controls (COM)</span></span>

<span data-ttu-id="0a994-104">Un contrôle ActiveX n’est qu’un autre terme pour un objet OLE ou plus spécifiquement, un objet COM.</span><span class="sxs-lookup"><span data-stu-id="0a994-104">An ActiveX control is really just another term for OLE object or more specifically, COM object.</span></span> <span data-ttu-id="0a994-105">En d’autres termes, un contrôle, au moins, est un objet COM qui prend en charge l’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) et est également auto-inscrit.</span><span class="sxs-lookup"><span data-stu-id="0a994-105">In other words, a control, at the very least, is some COM object that supports the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface and is also self-registering.</span></span> <span data-ttu-id="0a994-106">Via [**IUnknown :: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) , un conteneur peut gérer la durée de vie du contrôle, ainsi que découvrir de manière dynamique l’étendue complète des fonctionnalités d’un contrôle en fonction des interfaces disponibles.</span><span class="sxs-lookup"><span data-stu-id="0a994-106">Through [**IUnknown::QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) a container can manage the lifetime of the control as well as dynamically discover the full extent of a control's functionality based on the available interfaces.</span></span> <span data-ttu-id="0a994-107">Cela permet à un contrôle d’implémenter le moins de fonctionnalités qu’il le doit, au lieu de prendre en charge un grand nombre d’interfaces qui ne font rien.</span><span class="sxs-lookup"><span data-stu-id="0a994-107">This allows a control to implement as little functionality as it needs to, instead of supporting a large number of interfaces that actually don't do anything.</span></span> <span data-ttu-id="0a994-108">En résumé, cette exigence minimale pour ne pas dépasser **IUnknown** permet à un contrôle d’être aussi léger que possible.</span><span class="sxs-lookup"><span data-stu-id="0a994-108">In short, this minimal requirement for nothing more than **IUnknown** allows any control to be as lightweight as it can.</span></span>

<span data-ttu-id="0a994-109">En résumé, autre que [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) et auto-inscription, aucune autre exigence n’est requise pour un contrôle.</span><span class="sxs-lookup"><span data-stu-id="0a994-109">In short, other than [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) and self-registration, there are no other requirements for a control.</span></span> <span data-ttu-id="0a994-110">Toutefois, il existe des conventions qui doivent être suivies en ce qui concerne la prise en charge d’une interface, en termes de fonctionnalités fournies au conteneur par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="0a994-110">There are, however, conventions that should be followed about what the support of an interface means in terms of functionality provided to the container by the control.</span></span> <span data-ttu-id="0a994-111">Cette section décrit ensuite ce que cela signifie pour qu’un contrôle prenne en charge une interface, ainsi que les méthodes, propriétés et événements qu’un contrôle doit fournir comme ligne de base s’il a l’occasion de prendre en charge des méthodes, des propriétés et des événements.</span><span class="sxs-lookup"><span data-stu-id="0a994-111">This section then describes what it means for a control to actually support an interface, as well as methods, properties, and events that a control should provide as a baseline if it has occasion to support methods, properties, and events.</span></span>

<span data-ttu-id="0a994-112">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a994-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="0a994-113">Inscription automatique pour les contrôles</span><span class="sxs-lookup"><span data-stu-id="0a994-113">Self Registration for Controls</span></span>](self-registration-for-controls.md)
-   [<span data-ttu-id="0a994-114">Prise en charge d’une interface</span><span class="sxs-lookup"><span data-stu-id="0a994-114">What Support for an Interface Means</span></span>](what-support-for-an-interface-means.md)
-   [<span data-ttu-id="0a994-115">Interfaces de persistance</span><span class="sxs-lookup"><span data-stu-id="0a994-115">Persistence Interfaces</span></span>](persistence-interfaces.md)
-   [<span data-ttu-id="0a994-116">Méthodes facultatives dans les interfaces de contrôle</span><span class="sxs-lookup"><span data-stu-id="0a994-116">Optional Methods in Control Interfaces</span></span>](optional-methods-in-control-interfaces.md)
-   [<span data-ttu-id="0a994-117">Options de fabrique de classes</span><span class="sxs-lookup"><span data-stu-id="0a994-117">Class Factory Options</span></span>](class-factory-options.md)
-   [<span data-ttu-id="0a994-118">Exposition des propriétés via IDispatch</span><span class="sxs-lookup"><span data-stu-id="0a994-118">Exposing Properties through IDispatch</span></span>](properties.md)
-   [<span data-ttu-id="0a994-119">Exposer des méthodes par le biais de IDispatch</span><span class="sxs-lookup"><span data-stu-id="0a994-119">Exposing Methods through IDispatch</span></span>](exposing-methods-through-idispatch.md)
-   [<span data-ttu-id="0a994-120">Événements dans les contrôles</span><span class="sxs-lookup"><span data-stu-id="0a994-120">Events in Controls</span></span>](events-in-controls.md)
-   [<span data-ttu-id="0a994-121">Pages de propriétés</span><span class="sxs-lookup"><span data-stu-id="0a994-121">Property Pages</span></span>](property-pages.md)
-   [<span data-ttu-id="0a994-122">Propriétés ambiantes pour les contrôles</span><span class="sxs-lookup"><span data-stu-id="0a994-122">Ambient Properties for Controls</span></span>](ambient-properties-for-controls.md)
-   [<span data-ttu-id="0a994-123">Utilisation des fonctionnalités du conteneur</span><span class="sxs-lookup"><span data-stu-id="0a994-123">Using the Container's Functionality</span></span>](using-the-container-s-functionality.md)

## <a name="related-topics"></a><span data-ttu-id="0a994-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0a994-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a994-125">Instructions relatives au contrôle ActiveX et au conteneur de contrôles</span><span class="sxs-lookup"><span data-stu-id="0a994-125">ActiveX Control and Control Container Guidelines</span></span>](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 




