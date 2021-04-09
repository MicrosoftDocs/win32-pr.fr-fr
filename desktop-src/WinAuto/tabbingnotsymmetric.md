---
title: TabbingNotSymmetric
description: TabbingNotSymmetric
ms.assetid: 1E14ED9F-27C1-4054-B0A6-702167222196
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc19efbbbce0f299044726466dd8f87b133fc26d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101876"
---
# <a name="tabbingnotsymmetric"></a><span data-ttu-id="27ba5-103">TabbingNotSymmetric</span><span class="sxs-lookup"><span data-stu-id="27ba5-103">TabbingNotSymmetric</span></span>

## <a name="text"></a><span data-ttu-id="27ba5-104">Texte</span><span class="sxs-lookup"><span data-stu-id="27ba5-104">Text</span></span>

<span data-ttu-id="27ba5-105">La tabulation descendante et les transferts ne génèrent pas le même élément.</span><span class="sxs-lookup"><span data-stu-id="27ba5-105">Tabbing backwards and forwards does not yield the same element.</span></span> <span data-ttu-id="27ba5-106">ATTENDU, {0} mais reçu {1}</span><span class="sxs-lookup"><span data-stu-id="27ba5-106">Expected {0} but received {1}</span></span>

## <a name="type"></a><span data-ttu-id="27ba5-107">Type</span><span class="sxs-lookup"><span data-stu-id="27ba5-107">Type</span></span>

<span data-ttu-id="27ba5-108">Error</span><span class="sxs-lookup"><span data-stu-id="27ba5-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="27ba5-109">Description</span><span class="sxs-lookup"><span data-stu-id="27ba5-109">Description</span></span>

<span data-ttu-id="27ba5-110">Lors de l’utilisation de la navigation au clavier standard (Tab ou Maj + Tab), il n’est pas possible de répéter le chemin d’accès dans l’arborescence des éléments de la cible de vérification si la direction du parcours est inversée.</span><span class="sxs-lookup"><span data-stu-id="27ba5-110">When using standard keyboard navigation (Tab or Shift+Tab), it isn't possible to repeat the path of traversal through the element tree of the verification target if the direction of traversal is reversed.</span></span> <span data-ttu-id="27ba5-111">Par exemple, la tabulation suivante (tabulation) x fois de l’élément A (0) à l’élément A (x), puis la tabulation vers l’arrière (Maj + Tab) x fois, l’élément A (0) regagne le focus via un ensemble différent d’éléments intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="27ba5-111">For example, tabbing forward (Tab) x times from element A(0) to element A(x) and then tabbing backward (Shift+Tab) x times results in element A(0) regaining focus through a different set of intermediate elements.</span></span>

<span data-ttu-id="27ba5-112">Ce problème provoque des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car le parcours des éléments semble irrégulier et imprévisible.</span><span class="sxs-lookup"><span data-stu-id="27ba5-112">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because traversing elements appears erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="27ba5-113">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="27ba5-113">Possible causes</span></span>

-   <span data-ttu-id="27ba5-114">Plusieurs éléments ou leurs parents sont des contrôles personnalisés qui n’implémentent pas correctement la tabulation.</span><span class="sxs-lookup"><span data-stu-id="27ba5-114">Multiple elements or their parents are custom controls that don't implement tabbing correctly.</span></span> <span data-ttu-id="27ba5-115">Par exemple, la propriété d’État MSAA n’est pas définie correctement.</span><span class="sxs-lookup"><span data-stu-id="27ba5-115">For example, the MSAA State property is not set correctly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27ba5-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="27ba5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27ba5-117">Recommandations en matière de conception d’interface utilisateur clavier</span><span class="sxs-lookup"><span data-stu-id="27ba5-117">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 