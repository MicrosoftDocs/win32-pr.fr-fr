---
title: Comment Active Accessibility expose les éléments d’interface utilisateur
description: Microsoft Active Accessibility crée un objet proxy pour chaque élément de l’interface utilisateur qu’il expose.
ms.assetid: 64aa8fac-cea7-4466-ae34-2760956c296b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b450ebe79aa467100fe9b6fb3bc4cdfb5540b60c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196761"
---
# <a name="how-active-accessibility-exposes-user-interface-elements"></a><span data-ttu-id="658f7-103">Comment Active Accessibility expose les éléments d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="658f7-103">How Active Accessibility Exposes User Interface Elements</span></span>

<span data-ttu-id="658f7-104">Microsoft Active Accessibility crée un objet *proxy* pour chaque élément de l’interface utilisateur qu’il expose.</span><span class="sxs-lookup"><span data-stu-id="658f7-104">Microsoft Active Accessibility creates a *proxy* object for each user interface element that it exposes.</span></span> <span data-ttu-id="658f7-105">Un objet proxy joue le rôle d’intermédiaire entre l’utilitaire client et l’élément d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="658f7-105">A proxy object acts as an intermediary between the client utility and the UI element.</span></span> <span data-ttu-id="658f7-106">L’objectif de l’objet proxy est de surveiller l’étendue de la durée de vie de l’élément d’interface utilisateur et d’implémenter les propriétés et les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour le compte de l’élément d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="658f7-106">The purpose of the proxy object is to monitor the life span of the UI element and to implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods on behalf of the UI element.</span></span> <span data-ttu-id="658f7-107">Les développeurs de serveurs qui créent des contrôles personnalisés ou d’autres éléments d’interface utilisateur personnalisés doivent également créer des objets proxy.</span><span class="sxs-lookup"><span data-stu-id="658f7-107">Server developers who create custom controls or other custom UI elements should also create proxy objects.</span></span> <span data-ttu-id="658f7-108">Pour plus d’informations, consultez [création d’objets proxy](creating-proxy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="658f7-108">For more information, see [Creating Proxy Objects](creating-proxy-objects.md).</span></span>

<span data-ttu-id="658f7-109">Lorsque Microsoft Active Accessibility crée un objet pour exposer un contrôle prédéfini ou commun, il crée en fait au moins deux objets : un pour le contrôle et un pour la fenêtre qui entoure le contrôle.</span><span class="sxs-lookup"><span data-stu-id="658f7-109">When Microsoft Active Accessibility creates an object to expose a predefined or common control, it actually creates at least two objects: one for the control and one for the window that surrounds the control.</span></span> <span data-ttu-id="658f7-110">Dans la plupart des cas, ces fenêtres parentes possèdent la [propriété Role](role-property.md) de la [**\_ \_ fenêtre système Role**](object-roles.md) et ont les mêmes [propriété Name](name-property.md) et Name Class Name que le contrôle.</span><span class="sxs-lookup"><span data-stu-id="658f7-110">In most cases, these parent windows have the [Role property](role-property.md) of [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) and have the same [Name property](name-property.md) and window class name as the control.</span></span> <span data-ttu-id="658f7-111">Les informations sur le contrôle que les clients transmettent aux utilisateurs finaux sont contenues dans l’objet que Microsoft Active Accessibility crée pour exposer le contrôle, et non l’objet parent qui expose la fenêtre qui entoure le contrôle.</span><span class="sxs-lookup"><span data-stu-id="658f7-111">The information about the control that clients convey to end users is contained in the object that Microsoft Active Accessibility creates to expose the control, not the parent object that exposes the window that surrounds the control.</span></span>

<span data-ttu-id="658f7-112">Pour plus d'informations, consultez les rubriques ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="658f7-112">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="658f7-113">Filtrage des objets inutiles</span><span class="sxs-lookup"><span data-stu-id="658f7-113">Screening Out Unnecessary Objects</span></span>](screening-out-unnecessary-objects.md)
-   [<span data-ttu-id="658f7-114">Fourniture de la propriété Name</span><span class="sxs-lookup"><span data-stu-id="658f7-114">Providing the Name Property</span></span>](providing-the-name-property.md)
-   [<span data-ttu-id="658f7-115">S’assurer que les éléments d’interface utilisateur sont correctement nommés</span><span class="sxs-lookup"><span data-stu-id="658f7-115">Ensuring that UI Elements are Correctly Named</span></span>](ensure-that-ui-elements-are-named-correctly.md)
-   [<span data-ttu-id="658f7-116">Éléments d’interface utilisateur non pris en charge</span><span class="sxs-lookup"><span data-stu-id="658f7-116">Unsupported User Interface Elements</span></span>](unsupported-user-interface-elements.md)

 

 




