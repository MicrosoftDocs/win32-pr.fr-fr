---
title: ToolTip, contrôle (référence des éléments d’interface utilisateur MSAA)
description: Un contrôle ToolTip affiche une petite fenêtre contextuelle qui contient une ligne de texte qui décrit l’objectif d’un outil, représenté sous la forme d’un objet graphique, dans une application.
ms.assetid: d3a65d7b-b882-4a1a-bac2-6995b64cf4af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37557fd116084fc9ac53e8567afc90eda339750d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840045"
---
# <a name="tooltip-control-msaa-ui-element-reference"></a><span data-ttu-id="48974-103">ToolTip, contrôle (référence des éléments d’interface utilisateur MSAA)</span><span class="sxs-lookup"><span data-stu-id="48974-103">ToolTip Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="48974-104">Cette rubrique décrit les objets de **contrôle ToolTip** à des fins de référence des éléments d’interface utilisateur MSAA.</span><span class="sxs-lookup"><span data-stu-id="48974-104">This topic describes **ToolTip Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="48974-105">La création d’objets de **contrôle ToolTip** dans différentes infrastructures d’interface utilisateur n’est pas décrite ici.</span><span class="sxs-lookup"><span data-stu-id="48974-105">How to create **ToolTip Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="48974-106">Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="48974-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="48974-107">Un contrôle ToolTip affiche une petite fenêtre contextuelle qui contient une ligne de texte qui décrit l’objectif d’un outil, représenté sous la forme d’un objet graphique, dans une application.</span><span class="sxs-lookup"><span data-stu-id="48974-107">A tooltip control displays a small pop-up window that contains a line of text that describes the purpose of a tool, represented as a graphical object, in an application.</span></span>

<span data-ttu-id="48974-108">Le nom de la classe de fenêtre pour une info-bulle est la classe info-bulles \_ , qui est définie en tant que « classe info-bulles \_ » dans commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="48974-108">The window class name for a tooltip is TOOLTIPS\_CLASS, which is defined as "tooltips\_class" in Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="48974-109">Méthodes IAccessible</span><span class="sxs-lookup"><span data-stu-id="48974-109">IAccessible Methods</span></span>

<span data-ttu-id="48974-110">Un contrôle ToolTip prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="48974-110">A tooltip control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="48974-111">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="48974-111">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="48974-112">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="48974-112">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="48974-113">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="48974-113">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="48974-114">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="48974-114">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="48974-115">Propriétés IAccessible</span><span class="sxs-lookup"><span data-stu-id="48974-115">IAccessible Properties</span></span>

<span data-ttu-id="48974-116">Un contrôle ToolTip prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="48974-116">A tooltip control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="48974-117">Propriété</span><span class="sxs-lookup"><span data-stu-id="48974-117">Property</span></span>                                                                 | <span data-ttu-id="48974-118">Commentaires</span><span class="sxs-lookup"><span data-stu-id="48974-118">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48974-119">**Obtient \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="48974-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="48974-120">La propriété **ChildCount** est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="48974-120">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="48974-121">**Obtient \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="48974-121">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="48974-122">**Obtient \_ accName**</span><span class="sxs-lookup"><span data-stu-id="48974-122">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="48974-123">La propriété **Name** est le texte contenu dans le contrôle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="48974-123">The **Name** property is the text contained in the tooltip control.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="48974-124">**Obtient \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="48974-124">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="48974-125">La propriété **parente** est une fenêtre [**( \_ \_ fenêtre système de rôle**](object-roles.md) ) qui entoure le contrôle et possède les mêmes propriétés de **nom** et nom de classe de fenêtre que le contrôle.</span><span class="sxs-lookup"><span data-stu-id="48974-125">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="48974-126">**Obtient \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="48974-126">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="48974-127">La propriété **role** est [**l' \_ \_ info-bulle du système Role**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="48974-127">The **Role** property is [**ROLE\_SYSTEM\_TOOLTIP**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="48974-128">**Obtient \_ accState**</span><span class="sxs-lookup"><span data-stu-id="48974-128">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="48974-129">La propriété d' **État** est une combinaison d’une ou plusieurs des [valeurs](object-state-constants.md)suivantes : état du système d’état [**\_ \_ invisible**](object-state-constants.md) système d’état \| [**\_ \_ non disponible**](object-state-constants.md) système \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="48974-129">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="48974-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="48974-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48974-131">IAccessible, interface</span><span class="sxs-lookup"><span data-stu-id="48974-131">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





