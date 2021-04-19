---
title: Les éléments DragPattern/DragDropPattern requièrent un nom
description: Les éléments DragPattern/DragDropPattern requièrent un nom
ms.assetid: DEF58FB2-5830-4162-87D0-40DEC1237529
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc60eeca59f4754f9c160696cdfa2556c36a5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511198"
---
# <a name="dragpatterndragdroppattern-elements-requires-name"></a><span data-ttu-id="00045-103">Les éléments DragPattern/DragDropPattern requièrent un nom</span><span class="sxs-lookup"><span data-stu-id="00045-103">DragPattern/DragDropPattern elements requires Name</span></span>

## <a name="text"></a><span data-ttu-id="00045-104">Texte</span><span class="sxs-lookup"><span data-stu-id="00045-104">Text</span></span>

<span data-ttu-id="00045-105">Les éléments qui prennent en charge le glisser-déplacer doivent avoir un’name’valide</span><span class="sxs-lookup"><span data-stu-id="00045-105">Elements that support Drag/Drop should have a valid 'Name' set</span></span>

## <a name="type"></a><span data-ttu-id="00045-106">Type</span><span class="sxs-lookup"><span data-stu-id="00045-106">Type</span></span>

<span data-ttu-id="00045-107">Error</span><span class="sxs-lookup"><span data-stu-id="00045-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="00045-108">Description</span><span class="sxs-lookup"><span data-stu-id="00045-108">Description</span></span>

<span data-ttu-id="00045-109">L’élément prend en charge [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) ou [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), mais n’a pas de nom valide défini.</span><span class="sxs-lookup"><span data-stu-id="00045-109">The element supports either [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) or [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), but does not have a valid Name set.</span></span>

<span data-ttu-id="00045-110">Ce problème provoque des problèmes pour les personnes qui reposent sur un lecteur d’écran.</span><span class="sxs-lookup"><span data-stu-id="00045-110">This issue causes problems for people who rely on a screen-reader.</span></span> <span data-ttu-id="00045-111">L’utilisateur ne sera pas en mesure d’indiquer cet objet, car la lecture de l’écran ne lit pas un nom valide pour distinguer ce que cet élément est en déplacement.</span><span class="sxs-lookup"><span data-stu-id="00045-111">The user will not be able to tell what this object is since the screen read will not read out a valid name to distinguish what this element is when dragging.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="00045-112">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="00045-112">Possible causes</span></span>

-   <span data-ttu-id="00045-113">L’élément, ou son parent, a un nom ou une étiquette incorrectement attribué.</span><span class="sxs-lookup"><span data-stu-id="00045-113">The element, or its parent, has an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="00045-114">Un développeur ne sait pas que les lecteurs d’écran lisent les noms et les types de contrôle.</span><span class="sxs-lookup"><span data-stu-id="00045-114">A developer is not aware that screen readers read names and control types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="00045-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="00045-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00045-116">**IAccessible :: \_ accName**</span><span class="sxs-lookup"><span data-stu-id="00045-116">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="00045-117">Propriété Name</span><span class="sxs-lookup"><span data-stu-id="00045-117">Name Property</span></span>](name-property.md)
</dt> <dt>

[<span data-ttu-id="00045-118">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="00045-118">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="00045-119">**IUIAutomationElement::CurrentName**</span><span class="sxs-lookup"><span data-stu-id="00045-119">**IUIAutomationElement::CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




