---
title: ElementsChildHasDifferentParent
description: ElementsChildHasDifferentParent
ms.assetid: 2347A33C-8FBD-4C30-8B40-9CB35F121C8E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ea0f0ec7708f91d407f1fa7a55fa59a813234
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311521"
---
# <a name="elementschildhasdifferentparent"></a><span data-ttu-id="94956-103">ElementsChildHasDifferentParent</span><span class="sxs-lookup"><span data-stu-id="94956-103">ElementsChildHasDifferentParent</span></span>

## <a name="text"></a><span data-ttu-id="94956-104">Texte</span><span class="sxs-lookup"><span data-stu-id="94956-104">Text</span></span>

<span data-ttu-id="94956-105">L’enfant de l’élément ( {0} ) a un {1} élément parent () différent</span><span class="sxs-lookup"><span data-stu-id="94956-105">Element's child({0}) has different parent({1}) than element</span></span>

## <a name="type"></a><span data-ttu-id="94956-106">Type</span><span class="sxs-lookup"><span data-stu-id="94956-106">Type</span></span>

<span data-ttu-id="94956-107">Error</span><span class="sxs-lookup"><span data-stu-id="94956-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="94956-108">Description</span><span class="sxs-lookup"><span data-stu-id="94956-108">Description</span></span>

<span data-ttu-id="94956-109">Cette erreur indique que, lorsque la méthode [**\_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) est appelée sur les enfants de l’élément cible, les enfants ne signalent pas un parent cohérent.</span><span class="sxs-lookup"><span data-stu-id="94956-109">This error indicates that, when [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the children of the target element, the children do not report a consistent parent.</span></span>

![exemple des enfants d’un élément qui signale un parent incohérent](images/accchecker-inconsistent-parent.png)

<span data-ttu-id="94956-111">Ce problème peut entraîner des problèmes de navigation pour les outils automatisés, car le parcours des éléments peut être erratique et imprévisible.</span><span class="sxs-lookup"><span data-stu-id="94956-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="94956-112">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="94956-112">Possible causes</span></span>

<span data-ttu-id="94956-113">Implémentation MSAA incorrecte ou non valide.</span><span class="sxs-lookup"><span data-stu-id="94956-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94956-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="94956-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94956-115">**AccessibleChildren**</span><span class="sxs-lookup"><span data-stu-id="94956-115">**AccessibleChildren**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)
</dt> </dl>

 

 




