---
title: ElementIsChildOfParentMulipleTimes
description: ElementIsChildOfParentMulipleTimes
ms.assetid: B966ABE0-5109-4DAD-8125-EB4A3B3A5F61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da27c66027f7948dfa794c85dace015565d636c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197467"
---
# <a name="elementischildofparentmulipletimes"></a><span data-ttu-id="8275e-103">ElementIsChildOfParentMulipleTimes</span><span class="sxs-lookup"><span data-stu-id="8275e-103">ElementIsChildOfParentMulipleTimes</span></span>

## <a name="text"></a><span data-ttu-id="8275e-104">Texte</span><span class="sxs-lookup"><span data-stu-id="8275e-104">Text</span></span>

<span data-ttu-id="8275e-105">Le accParent de l’élément est ( {0} ), mais l’élément d’origine est une {1} heure enfant</span><span class="sxs-lookup"><span data-stu-id="8275e-105">Element's accParent is ({0}), but original element is a child {1} times</span></span>

## <a name="type"></a><span data-ttu-id="8275e-106">Type</span><span class="sxs-lookup"><span data-stu-id="8275e-106">Type</span></span>

<span data-ttu-id="8275e-107">Error</span><span class="sxs-lookup"><span data-stu-id="8275e-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="8275e-108">Description</span><span class="sxs-lookup"><span data-stu-id="8275e-108">Description</span></span>

<span data-ttu-id="8275e-109">Lorsque la méthode [**\_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) est appelée sur l’élément cible, elle signale qu’elle est un enfant du même parent plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="8275e-109">When [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the target element, it reports being a child of the same parent multiple times.</span></span>

<span data-ttu-id="8275e-110">Ce problème peut entraîner des problèmes de navigation pour les outils automatisés, car le parcours des éléments peut être erratique et imprévisible.</span><span class="sxs-lookup"><span data-stu-id="8275e-110">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="8275e-111">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="8275e-111">Possible causes</span></span>

<span data-ttu-id="8275e-112">Implémentation MSAA incorrecte ou non valide.</span><span class="sxs-lookup"><span data-stu-id="8275e-112">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8275e-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8275e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8275e-114">**IAccessible :: \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="8275e-114">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




