---
title: Contrôle de barre d’État (référence des éléments d’interface utilisateur MSAA)
description: Les barres d’état affichent des informations d’État dans une fenêtre horizontale au bas d’une fenêtre d’application.
ms.assetid: e910a5c6-84d5-4ade-abf5-792ff1915021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81bddf2898b9b7eca5385d86d6dabc6a50d3d4df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311203"
---
# <a name="status-bar-control-msaa-ui-element-reference"></a><span data-ttu-id="2ba78-103">Contrôle de barre d’État (référence des éléments d’interface utilisateur MSAA)</span><span class="sxs-lookup"><span data-stu-id="2ba78-103">Status Bar Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="2ba78-104">Cette rubrique décrit les objets de **contrôle de barre d’État** à des fins de référence d’élément d’interface utilisateur MSAA.</span><span class="sxs-lookup"><span data-stu-id="2ba78-104">This topic describes **Status Bar Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="2ba78-105">La procédure de création d’objets de **contrôle de barre d’État** dans différentes infrastructures d’interface utilisateur n’est pas décrite ici.</span><span class="sxs-lookup"><span data-stu-id="2ba78-105">How to create **Status Bar Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="2ba78-106">Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="2ba78-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="2ba78-107">Les barres d’état affichent des informations d’État dans une fenêtre horizontale au bas d’une fenêtre d’application.</span><span class="sxs-lookup"><span data-stu-id="2ba78-107">Status bars display status information in a horizontal window at the bottom of an application window.</span></span> <span data-ttu-id="2ba78-108">Les barres d’État sont souvent divisées en parties, appelées volets, et chaque volet affiche des informations d’État différentes.</span><span class="sxs-lookup"><span data-stu-id="2ba78-108">Status bars are often divided into parts, called panes, and each pane displays different status information.</span></span> <span data-ttu-id="2ba78-109">En outre, les barres d’État peuvent contenir des objets de types différents, notamment des boutons et des barres de progression.</span><span class="sxs-lookup"><span data-stu-id="2ba78-109">Additionally, status bars can contain objects of different types, including buttons and progress bars.</span></span> <span data-ttu-id="2ba78-110">Le nom de la classe de fenêtre pour un contrôle de barre d’État est STATUSCLASSNAME, qui est défini comme « msctls \_ statusbar32 » dans commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="2ba78-110">The window class name for a status bar control is STATUSCLASSNAME, which is defined as "msctls\_statusbar32" in Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="2ba78-111">Méthodes IAccessible</span><span class="sxs-lookup"><span data-stu-id="2ba78-111">IAccessible Methods</span></span>

<span data-ttu-id="2ba78-112">Les barres d’État prennent en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="2ba78-112">Status bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="2ba78-113">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="2ba78-113">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="2ba78-114">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="2ba78-114">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="2ba78-115">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="2ba78-115">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="2ba78-116">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="2ba78-116">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="2ba78-117">Propriétés IAccessible</span><span class="sxs-lookup"><span data-stu-id="2ba78-117">IAccessible Properties</span></span>

<span data-ttu-id="2ba78-118">Les barres d’État prennent en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="2ba78-118">Status bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="2ba78-119">Propriété</span><span class="sxs-lookup"><span data-stu-id="2ba78-119">Property</span></span>                                                                 | <span data-ttu-id="2ba78-120">Commentaires</span><span class="sxs-lookup"><span data-stu-id="2ba78-120">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ba78-121">**Obtient \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="2ba78-121">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="2ba78-122">La propriété **ChildCount** est le nombre de volets dans la barre d’État.</span><span class="sxs-lookup"><span data-stu-id="2ba78-122">The **ChildCount** property is the number of panes in the status bar.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="2ba78-123">**Obtient \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="2ba78-123">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="2ba78-124">**Obtient \_ accName**</span><span class="sxs-lookup"><span data-stu-id="2ba78-124">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="2ba78-125">L’objet de barre d’État lui-même n’a pas de propriété **Name** .</span><span class="sxs-lookup"><span data-stu-id="2ba78-125">The status bar object itself does not have a **Name** property.</span></span> <span data-ttu-id="2ba78-126">La propriété **Name** de chaque volet de la barre d’État est la même que le texte affiché.</span><span class="sxs-lookup"><span data-stu-id="2ba78-126">The **Name** property of each pane in the status bar is the same as the displayed text.</span></span>                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="2ba78-127">**Obtient \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="2ba78-127">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="2ba78-128">La propriété **parent** de l’objet de barre d’État est une fenêtre ( [**\_ \_ fenêtre système de rôle**](object-roles.md) ) qui entoure le contrôle et possède le même nom de classe de fenêtre que le contrôle.</span><span class="sxs-lookup"><span data-stu-id="2ba78-128">The **Parent** property of the status bar object is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same window class name as the control.</span></span> <span data-ttu-id="2ba78-129">La propriété **parent** des volets dans la barre d’État est l’objet de barre d’État.</span><span class="sxs-lookup"><span data-stu-id="2ba78-129">The **Parent** property of the panes in the status bar is the status bar object.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="2ba78-130">**Obtient \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="2ba78-130">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="2ba78-131">La propriété de **rôle** pour l’objet de barre d’État proprement dit est le [**\_ \_ STATUSBAR système Role**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2ba78-131">The **Role** property for the status bar object itself is [**ROLE\_SYSTEM\_STATUSBAR**](object-roles.md).</span></span> <span data-ttu-id="2ba78-132">Le texte affiché dans une barre d’État présente le [**rôle \_ système \_ STATICTEXT**](object-roles.md) en tant que propriété de **rôle** .</span><span class="sxs-lookup"><span data-stu-id="2ba78-132">The text displayed in a status bar has [**ROLE\_SYSTEM\_STATICTEXT**](object-roles.md) as its **Role** property.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="2ba78-133">**Obtient \_ accState**</span><span class="sxs-lookup"><span data-stu-id="2ba78-133">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="2ba78-134">La propriété d' **État** est une combinaison d’une ou plusieurs des [valeurs](object-state-constants.md)suivantes : état du système d’état [**\_ \_ invisible**](object-state-constants.md) système d’état \| [**\_ \_ non disponible**](object-state-constants.md) système \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="2ba78-134">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="notes"></a><span data-ttu-id="2ba78-135">Notes</span><span class="sxs-lookup"><span data-stu-id="2ba78-135">Notes</span></span>

<span data-ttu-id="2ba78-136">Comme les raccourcis clavier ne sont pas pris en charge pour les contrôles de barre d’État ou les zones de texte sur les barres d’État, l' [**\_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2ba78-136">Because keyboard shortcuts are not supported for status bar controls or text areas on status bars, [**get\_accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) is not supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ba78-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2ba78-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ba78-138">IAccessible, interface</span><span class="sxs-lookup"><span data-stu-id="2ba78-138">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





