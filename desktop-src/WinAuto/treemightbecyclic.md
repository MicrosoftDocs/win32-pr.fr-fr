---
title: TreeMightBeCyclic
description: TreeMightBeCyclic
ms.assetid: 9A997949-A1A2-448C-9739-BE176621F1B4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9647f4429ba17226f342a8dceb3c51b033d08b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315281"
---
# <a name="treemightbecyclic"></a><span data-ttu-id="e8190-103">TreeMightBeCyclic</span><span class="sxs-lookup"><span data-stu-id="e8190-103">TreeMightBeCyclic</span></span>

## <a name="text"></a><span data-ttu-id="e8190-104">Texte</span><span class="sxs-lookup"><span data-stu-id="e8190-104">Text</span></span>

<span data-ttu-id="e8190-105">L’arborescence est {0} Deep Levels.</span><span class="sxs-lookup"><span data-stu-id="e8190-105">Tree is {0} levels deep.</span></span> <span data-ttu-id="e8190-106">Cela peut indiquer que l’arborescence d’accessibilité est cyclique et qu’elle semble donc être infinie.</span><span class="sxs-lookup"><span data-stu-id="e8190-106">This might indicate that the accessibility tree is cyclic, and thus it would appear to be infinite.</span></span>

## <a name="type"></a><span data-ttu-id="e8190-107">Type</span><span class="sxs-lookup"><span data-stu-id="e8190-107">Type</span></span>

<span data-ttu-id="e8190-108">Error</span><span class="sxs-lookup"><span data-stu-id="e8190-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="e8190-109">Description</span><span class="sxs-lookup"><span data-stu-id="e8190-109">Description</span></span>

<span data-ttu-id="e8190-110">L’arborescence des éléments est cyclique et la profondeur de l’arborescence peut être infinie.</span><span class="sxs-lookup"><span data-stu-id="e8190-110">The element tree is cyclic and the tree depth might be infinite.</span></span>

<span data-ttu-id="e8190-111">Ce problème entraîne des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car il n’y aura aucune limite apparente au parcours des éléments dans l’application cible.</span><span class="sxs-lookup"><span data-stu-id="e8190-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because there will be no apparent limit to the traversal of elements in the target application.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="e8190-112">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="e8190-112">Possible causes</span></span>

<span data-ttu-id="e8190-113">Plusieurs éléments, ou leurs parents, sont des contrôles personnalisés qui n’implémentent pas correctement la tabulation.</span><span class="sxs-lookup"><span data-stu-id="e8190-113">Multiple elements, or their parents, are custom controls that do not implement tabbing correctly.</span></span> <span data-ttu-id="e8190-114">Par exemple, la propriété d' [État](state-property.md) MSAA n’est pas mise à jour correctement.</span><span class="sxs-lookup"><span data-stu-id="e8190-114">For example, the MSAA [State](state-property.md) property is not updated correctly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8190-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e8190-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8190-116">Recommandations en matière de conception d’interface utilisateur clavier</span><span class="sxs-lookup"><span data-stu-id="e8190-116">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> <dt>

[<span data-ttu-id="e8190-117">Instructions relatives à l’interaction avec l’expérience utilisateur Windows-clavier</span><span class="sxs-lookup"><span data-stu-id="e8190-117">Windows User Experience Interaction Guidelines - Keyboard</span></span>](https://msdn.microsoft.com/library/bb545460.aspx#guidelines)
</dt> </dl>

 

 