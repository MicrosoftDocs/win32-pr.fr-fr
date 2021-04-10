---
title: Fenêtre cliente MDI (référence des éléments d’interface utilisateur MSAA)
description: L’interface multidocument (MDI) est une spécification qui définit l’interface utilisateur standard pour les applications écrites pour Windows. Une application MDI permet à un utilisateur de travailler avec plusieurs documents à la fois.
ms.assetid: ede2dd19-e4c6-43e8-8f22-f807621dfa0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1557176752d29b7d429a0c434554df09b69a8e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939920"
---
# <a name="mdi-client-window-msaa-ui-element-reference"></a><span data-ttu-id="ccbd8-104">Fenêtre cliente MDI (référence des éléments d’interface utilisateur MSAA)</span><span class="sxs-lookup"><span data-stu-id="ccbd8-104">MDI Client Window (MSAA UI Element Reference)</span></span>

<span data-ttu-id="ccbd8-105">L’interface multidocument (MDI) est une spécification qui définit l’interface utilisateur standard pour les applications écrites pour Windows.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-105">The multiple document interface (MDI) is a specification that defines the standard user interface for applications written for Windows.</span></span> <span data-ttu-id="ccbd8-106">Une application MDI permet à un utilisateur de travailler avec plusieurs documents à la fois.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-106">An MDI application enables a user to work with more than one document at a time.</span></span>

<span data-ttu-id="ccbd8-107">Une application MDI comporte trois types de fenêtres : une fenêtre frame, une fenêtre client et un certain nombre de fenêtres enfants.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-107">An MDI application has three kinds of windows: a frame window, a client window, and a number of child windows.</span></span> <span data-ttu-id="ccbd8-108">La fenêtre frame est semblable à la fenêtre principale d’une application et elle entoure la fenêtre cliente.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-108">The frame window is like the main window of an application, and it surrounds the client window.</span></span> <span data-ttu-id="ccbd8-109">La fenêtre cliente est un enfant de la fenêtre frame et sert d’arrière-plan pour les fenêtres enfants.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-109">The client window is a child of the frame window and serves as the background for the child windows.</span></span> <span data-ttu-id="ccbd8-110">La fenêtre cliente prend également en charge la création et la manipulation des fenêtres enfants dans lesquelles les documents sont affichés.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-110">The client window also provides support for creating and manipulating the child windows in which documents are displayed.</span></span>

<span data-ttu-id="ccbd8-111">Le nom de la classe de fenêtre pour une fenêtre de client MDI est « MDIClient ».</span><span class="sxs-lookup"><span data-stu-id="ccbd8-111">The window class name for an MDI client window is "MDIClient".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="ccbd8-112">Méthodes IAccessible</span><span class="sxs-lookup"><span data-stu-id="ccbd8-112">IAccessible Methods</span></span>

<span data-ttu-id="ccbd8-113">Une fenêtre cliente MDI prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="ccbd8-113">An MDI client window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="ccbd8-114">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="ccbd8-114">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="ccbd8-115">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="ccbd8-115">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="ccbd8-116">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="ccbd8-116">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="ccbd8-117">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="ccbd8-117">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="ccbd8-118">Propriétés IAccessible</span><span class="sxs-lookup"><span data-stu-id="ccbd8-118">IAccessible Properties</span></span>

<span data-ttu-id="ccbd8-119">Une fenêtre cliente MDI prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="ccbd8-119">An MDI client window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="ccbd8-120">Propriété</span><span class="sxs-lookup"><span data-stu-id="ccbd8-120">Property</span></span>                                                                 | <span data-ttu-id="ccbd8-121">Commentaires</span><span class="sxs-lookup"><span data-stu-id="ccbd8-121">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ccbd8-122">**Obtient \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="ccbd8-122">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="ccbd8-123">La propriété **ChildCount** est le nombre de fenêtres enfants dans lesquelles les documents sont affichés.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-123">The **ChildCount** property is the number of child windows in which documents are displayed.</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="ccbd8-124">**Obtient \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="ccbd8-124">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="ccbd8-125">**Obtient \_ accName**</span><span class="sxs-lookup"><span data-stu-id="ccbd8-125">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="ccbd8-126">La propriété **Name** est « Workspace ».</span><span class="sxs-lookup"><span data-stu-id="ccbd8-126">The **Name** property is "Workspace".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="ccbd8-127">**Obtient \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="ccbd8-127">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="ccbd8-128">La propriété **parente** est la fenêtre frame MDI.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-128">The **Parent** property is the MDI frame window.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="ccbd8-129">**Obtient \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="ccbd8-129">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="ccbd8-130">La propriété de **rôle** est [**client de \_ système \_ de rôle**](object-roles.md)</span><span class="sxs-lookup"><span data-stu-id="ccbd8-130">The **Role** property is [**ROLE\_SYSTEM\_CLIENT**](object-roles.md)</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="ccbd8-131">**Obtient \_ accSelection**</span><span class="sxs-lookup"><span data-stu-id="ccbd8-131">**get\_accSelection**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="ccbd8-132">**Obtient \_ accState**</span><span class="sxs-lookup"><span data-stu-id="ccbd8-132">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="ccbd8-133">La propriété d' **État** est une combinaison d’une ou plusieurs des [valeurs](object-state-constants.md)suivantes : état du système d’état [**\_ \_ invisible**](object-state-constants.md) système d’état \| [**\_ \_ non disponible**](object-state-constants.md) système \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="ccbd8-133">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="ccbd8-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ccbd8-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccbd8-135">IAccessible, interface</span><span class="sxs-lookup"><span data-stu-id="ccbd8-135">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





