---
title: Contrôle header (référence des éléments d’interface utilisateur MSAA)
description: Un contrôle header affiche des en-têtes en haut des colonnes d’informations et permet à l’utilisateur de trier les informations en cliquant sur les en-têtes. L’Explorateur Windows utilise un contrôle d’en-tête lorsque le mode Détails est sélectionné.
ms.assetid: 669d6bb8-7bc4-4e6f-bf4f-207887f44b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d069770b14ad3ba58022af28ad07fc78cb8c5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310761"
---
# <a name="header-control-msaa-ui-element-reference"></a><span data-ttu-id="64e39-104">Contrôle header (référence des éléments d’interface utilisateur MSAA)</span><span class="sxs-lookup"><span data-stu-id="64e39-104">Header Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="64e39-105">Cette rubrique décrit les objets de **contrôle header** à des fins de référence des éléments d’interface utilisateur MSAA.</span><span class="sxs-lookup"><span data-stu-id="64e39-105">This topic describes **Header Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="64e39-106">La procédure de création d’objets de **contrôle header** dans différentes infrastructures d’interface utilisateur n’est pas décrite ici.</span><span class="sxs-lookup"><span data-stu-id="64e39-106">How to create **Header Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="64e39-107">Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="64e39-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="64e39-108">Un contrôle header affiche des en-têtes en haut des colonnes d’informations et permet à l’utilisateur de trier les informations en cliquant sur les en-têtes.</span><span class="sxs-lookup"><span data-stu-id="64e39-108">A header control displays headings at the top of columns of information and lets the user sort the information by clicking the headings.</span></span> <span data-ttu-id="64e39-109">L’Explorateur Windows utilise un contrôle d’en-tête lorsque le mode Détails est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="64e39-109">Windows Explorer uses a header control when the Details view is selected.</span></span>

<span data-ttu-id="64e39-110">Le nom de la classe de fenêtre pour un contrôle header est l' \_ en-tête WC, qui est défini comme « SysHeader32 » dans commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="64e39-110">The window class name for a header control is WC\_HEADER, which is defined as "SysHeader32" in Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="64e39-111">Méthodes IAccessible</span><span class="sxs-lookup"><span data-stu-id="64e39-111">IAccessible Methods</span></span>

<span data-ttu-id="64e39-112">Un contrôle header prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="64e39-112">A header control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>



| <span data-ttu-id="64e39-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="64e39-113">Method</span></span>                                                                    | <span data-ttu-id="64e39-114">Commentaires</span><span class="sxs-lookup"><span data-stu-id="64e39-114">Comments</span></span>                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="64e39-115">**accDoDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="64e39-115">**accDoDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | <span data-ttu-id="64e39-116">Cette méthode effectue l’action par défaut en cliquant sur l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="64e39-116">This method performs the default action by clicking the header.</span></span> |
| [<span data-ttu-id="64e39-117">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="64e39-117">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                 |
| [<span data-ttu-id="64e39-118">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="64e39-118">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                 |
| [<span data-ttu-id="64e39-119">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="64e39-119">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                 |
| [<span data-ttu-id="64e39-120">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="64e39-120">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                 |



 

## <a name="iaccessible-properties"></a><span data-ttu-id="64e39-121">Propriétés IAccessible</span><span class="sxs-lookup"><span data-stu-id="64e39-121">IAccessible Properties</span></span>

<span data-ttu-id="64e39-122">Un contrôle header prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="64e39-122">A header control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="64e39-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="64e39-123">Property</span></span>                                                                       | <span data-ttu-id="64e39-124">Commentaires</span><span class="sxs-lookup"><span data-stu-id="64e39-124">Comments</span></span>                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64e39-125">**Obtient \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="64e39-125">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | <span data-ttu-id="64e39-126">La propriété **ChildCount** est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="64e39-126">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                   |
| [<span data-ttu-id="64e39-127">**Obtient \_ accDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="64e39-127">**get\_accDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | <span data-ttu-id="64e39-128">La propriété **DefaultAction** est « Click ».</span><span class="sxs-lookup"><span data-stu-id="64e39-128">The **DefaultAction** property is "Click".</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="64e39-129">**Obtient \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="64e39-129">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 |                                                                                                                                                                                                                                        |
| [<span data-ttu-id="64e39-130">**Obtient \_ accName**</span><span class="sxs-lookup"><span data-stu-id="64e39-130">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | <span data-ttu-id="64e39-131">La propriété **Name** est identique au nom de l’en-tête de colonne.</span><span class="sxs-lookup"><span data-stu-id="64e39-131">The **Name** property is the same as the name of the column header.</span></span>                                                                                                                                                                    |
| [<span data-ttu-id="64e39-132">**Obtient \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="64e39-132">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)               | <span data-ttu-id="64e39-133">La propriété **parent** est une fenêtre ( [**\_ \_ liste système de rôles**](object-roles.md) ) qui entoure le contrôle et possède le même nom de classe de fenêtre que le contrôle.</span><span class="sxs-lookup"><span data-stu-id="64e39-133">The **Parent** property is a window ( [**ROLE\_SYSTEM\_LIST**](object-roles.md) ) that surrounds the control and has the same window class name as the control.</span></span>                                                      |
| [<span data-ttu-id="64e39-134">**Obtient \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="64e39-134">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | <span data-ttu-id="64e39-135">La propriété **role** est le [**système de rôle \_ \_ COLUMNHEADER**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="64e39-135">The **Role** property is [**ROLE\_SYSTEM\_COLUMNHEADER**](object-roles.md).</span></span>                                                                                                                                  |
| [<span data-ttu-id="64e39-136">**Obtient \_ accState**</span><span class="sxs-lookup"><span data-stu-id="64e39-136">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | <span data-ttu-id="64e39-137">La valeur de la propriété **State** est toujours le [**système d’état \_ \_ ReadOnly**](object-state-constants.md) et peut également inclure le [**système d’état \_ \_ invisible**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="64e39-137">The value for the **State** property is always [**STATE\_SYSTEM\_READONLY**](object-state-constants.md) and can also include [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="64e39-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="64e39-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64e39-139">IAccessible, interface</span><span class="sxs-lookup"><span data-stu-id="64e39-139">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




