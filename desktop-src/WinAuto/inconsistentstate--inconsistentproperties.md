---
title: InconsistentState, InconsistentProperties
description: InconsistentState, InconsistentProperties
ms.assetid: 82A2ECA8-0155-402A-A745-B97D3F633643
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5522025eff8aecbdf0f4313c0052afebd4a17958
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672018"
---
# <a name="inconsistentstate-inconsistentproperties"></a><span data-ttu-id="78050-103">InconsistentState, InconsistentProperties</span><span class="sxs-lookup"><span data-stu-id="78050-103">InconsistentState, InconsistentProperties</span></span>

## <a name="text"></a><span data-ttu-id="78050-104">Texte</span><span class="sxs-lookup"><span data-stu-id="78050-104">Text</span></span>

<span data-ttu-id="78050-105">Les États/propriétés d’un contrôle sont incohérents {0} et {1}</span><span class="sxs-lookup"><span data-stu-id="78050-105">A control has states/properties that are inconsistent {0} and {1}</span></span>

## <a name="type"></a><span data-ttu-id="78050-106">Type</span><span class="sxs-lookup"><span data-stu-id="78050-106">Type</span></span>

<span data-ttu-id="78050-107">Error</span><span class="sxs-lookup"><span data-stu-id="78050-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="78050-108">Description</span><span class="sxs-lookup"><span data-stu-id="78050-108">Description</span></span>

<span data-ttu-id="78050-109">Un élément signale des États MSAA incohérents ou incompatibles ou des propriétés UI Automation.</span><span class="sxs-lookup"><span data-stu-id="78050-109">An element is reporting inconsistent or conflicting MSAA states or UI Automation properties.</span></span> <span data-ttu-id="78050-110">Par exemple, lorsque la méthode [**obtenir \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) retourne l’une des combinaisons suivantes.</span><span class="sxs-lookup"><span data-stu-id="78050-110">For example, when the [**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) method returns any of the following combinations.</span></span>

-   <span data-ttu-id="78050-111">Système d’état \_ \_ développé et \_ système d’état \_ réduit</span><span class="sxs-lookup"><span data-stu-id="78050-111">STATE\_SYSTEM\_EXPANDED and STATE\_SYSTEM\_COLLAPSED</span></span>
-   <span data-ttu-id="78050-112">Système d’état \_ \_ sélectionné et non \_ \_ sélectionnable par le système</span><span class="sxs-lookup"><span data-stu-id="78050-112">STATE\_SYSTEM\_SELECTED and not STATE\_SYSTEM\_SELECTABLE</span></span>
-   <span data-ttu-id="78050-113">Système d’État axé sur le système d’état \_ \_ et non sur \_ le système d’état \_</span><span class="sxs-lookup"><span data-stu-id="78050-113">STATE\_SYSTEM\_FOCUSED and not STATE\_SYSTEM\_FOCUSABLE</span></span>

<span data-ttu-id="78050-114">Ce problème provoque des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car un état d’élément incorrect peut être signalé à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="78050-114">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an incorrect element state might be reported to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="78050-115">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="78050-115">Possible causes</span></span>

<span data-ttu-id="78050-116">L’État MSAA de l’élément ou de son parent est incorrect.</span><span class="sxs-lookup"><span data-stu-id="78050-116">The element or its parent has an MSAA state set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78050-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="78050-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78050-118">**IAccessible :: \_ accState**</span><span class="sxs-lookup"><span data-stu-id="78050-118">**IAccessible::get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[<span data-ttu-id="78050-119">**Constantes d’état d’objet**</span><span class="sxs-lookup"><span data-stu-id="78050-119">**Object State Constants**</span></span>](object-state-constants.md)
</dt> <dt>

[<span data-ttu-id="78050-120">États et propriétés</span><span class="sxs-lookup"><span data-stu-id="78050-120">States and Properties</span></span>](uiauto-msaa.md)
</dt> </dl>

 

 




