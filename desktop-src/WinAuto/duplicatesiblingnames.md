---
title: DuplicateSiblingNames
description: DuplicateSiblingNames
ms.assetid: 4E9FFD16-EAC0-4778-8DEB-D179E2197411
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aed5a7caeadc34519988fe8a4a1f12ec4e05ce13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675874"
---
# <a name="duplicatesiblingnames"></a><span data-ttu-id="9bc78-103">DuplicateSiblingNames</span><span class="sxs-lookup"><span data-stu-id="9bc78-103">DuplicateSiblingNames</span></span>

## <a name="text"></a><span data-ttu-id="9bc78-104">Texte</span><span class="sxs-lookup"><span data-stu-id="9bc78-104">Text</span></span>

<span data-ttu-id="9bc78-105">Le nom frère dupliqué et le rôle \\ " {0} \\ " lèvent une ambiguïté entre les éléments.</span><span class="sxs-lookup"><span data-stu-id="9bc78-105">Duplicate sibling Name+Role \\"{0}\\" will cause ambiguity between elements.</span></span>

## <a name="type"></a><span data-ttu-id="9bc78-106">Type</span><span class="sxs-lookup"><span data-stu-id="9bc78-106">Type</span></span>

<span data-ttu-id="9bc78-107">Error</span><span class="sxs-lookup"><span data-stu-id="9bc78-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="9bc78-108">Description</span><span class="sxs-lookup"><span data-stu-id="9bc78-108">Description</span></span>

<span data-ttu-id="9bc78-109">Un élément a le même nom et le même rôle/ControlType qu’un autre élément.</span><span class="sxs-lookup"><span data-stu-id="9bc78-109">An element has the same Name and Role/ControlType as another element.</span></span>

<span data-ttu-id="9bc78-110">Ce problème peut entraîner une confusion, car les lecteurs d’écran lisent le même texte pour tous les éléments portant le même nom et le même rôle/ControlType.</span><span class="sxs-lookup"><span data-stu-id="9bc78-110">This issue can cause confusion because screen readers will read the same text for all the elements with the same Name and Role/ControlType.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="9bc78-111">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="9bc78-111">Possible causes</span></span>

-   <span data-ttu-id="9bc78-112">Le nom de l’élément contient le texte Role/ControlType.</span><span class="sxs-lookup"><span data-stu-id="9bc78-112">Element’s name contain Role/ControlType text.</span></span>
-   <span data-ttu-id="9bc78-113">Le nom de l’élément ou le nom de son parent n’est pas défini ou n’est pas défini correctement.</span><span class="sxs-lookup"><span data-stu-id="9bc78-113">Element’s name or the name of its parent is not set or is set incorrectly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9bc78-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9bc78-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bc78-115">**IAccessible :: \_ accName**</span><span class="sxs-lookup"><span data-stu-id="9bc78-115">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="9bc78-116">Propriété Name</span><span class="sxs-lookup"><span data-stu-id="9bc78-116">Name Property</span></span>](name-property.md)
</dt> <dt>

[<span data-ttu-id="9bc78-117">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9bc78-117">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="9bc78-118">**IUIAutomationElement.CurrentName**</span><span class="sxs-lookup"><span data-stu-id="9bc78-118">**IUIAutomationElement.CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




