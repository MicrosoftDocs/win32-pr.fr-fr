---
title: TabbingNotCyclic
description: TabbingNotCyclic
ms.assetid: F6BCC613-1EA1-438C-AC09-8A282870E021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08fd2e9f6613e07840f432b646c1bdc06a34b5f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031463"
---
# <a name="tabbingnotcyclic"></a><span data-ttu-id="d7e76-103">TabbingNotCyclic</span><span class="sxs-lookup"><span data-stu-id="d7e76-103">TabbingNotCyclic</span></span>

## <a name="text"></a><span data-ttu-id="d7e76-104">Texte</span><span class="sxs-lookup"><span data-stu-id="d7e76-104">Text</span></span>

<span data-ttu-id="d7e76-105">La tabulation dans cette application n’est pas cyclique.</span><span class="sxs-lookup"><span data-stu-id="d7e76-105">The tabbing in this application is not cyclic.</span></span> <span data-ttu-id="d7e76-106">La tabulation vers l’avant ou vers {0} l’arrière ne revient pas au même contrôle.</span><span class="sxs-lookup"><span data-stu-id="d7e76-106">Tabbing forwards or backwards {0} times doesn't come back to the same control.</span></span>

## <a name="type"></a><span data-ttu-id="d7e76-107">Type</span><span class="sxs-lookup"><span data-stu-id="d7e76-107">Type</span></span>

<span data-ttu-id="d7e76-108">Error</span><span class="sxs-lookup"><span data-stu-id="d7e76-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="d7e76-109">Description</span><span class="sxs-lookup"><span data-stu-id="d7e76-109">Description</span></span>

<span data-ttu-id="d7e76-110">Lors de l’utilisation de la navigation au clavier standard (Tab ou Maj + Tab), il n’est pas possible de parcourir l’arborescence d’éléments de la cible de vérification jusqu’à ce que l’élément de départ devienne l’élément de fin (en utilisant le même nombre de séquences de touches) en inversant la direction de traversée.</span><span class="sxs-lookup"><span data-stu-id="d7e76-110">When using standard keyboard navigation (Tab or Shift+Tab), it isn't possible to traverse the element tree of the verification target until the starting element becomes the ending element (using the same number of keystrokes) by reversing the direction of traversal.</span></span> <span data-ttu-id="d7e76-111">Par exemple, la tabulation suivante (tabulation) x fois de l’élément A (0) à l’élément A (x), puis la tabulation vers l’arrière (Maj + Tab) x fois n’entraîne pas l’élément A (0) qui regagne le focus.</span><span class="sxs-lookup"><span data-stu-id="d7e76-111">For example, tabbing forward (Tab) x times from element A(0) to element A(x) and then tabbing backward (Shift+Tab) x times does not result in element A(0) regaining focus.</span></span>

<span data-ttu-id="d7e76-112">Ce problème entraîne des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car il n’existe pas de moyen prévisible de revenir à un contrôle après l’avoir visité.</span><span class="sxs-lookup"><span data-stu-id="d7e76-112">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because there is no predictable way to return to a control after it has been visited.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="d7e76-113">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="d7e76-113">Possible causes</span></span>

-   <span data-ttu-id="d7e76-114">L’élément ou son parent est un contrôle personnalisé qui n’implémente pas correctement la tabulation.</span><span class="sxs-lookup"><span data-stu-id="d7e76-114">The element or its parent is a custom control that doesn't implement tabbing correctly.</span></span> <span data-ttu-id="d7e76-115">Par exemple, la propriété d’État MSAA n’est pas définie correctement.</span><span class="sxs-lookup"><span data-stu-id="d7e76-115">For example, the MSAA State property isn't set correctly.</span></span>
-   <span data-ttu-id="d7e76-116">Certaines applications, telles que le bloc-notes, présentent ce comportement de manière innateuse.</span><span class="sxs-lookup"><span data-stu-id="d7e76-116">Some applications, such as the Notepad, exhibit this behavior innately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7e76-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d7e76-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7e76-118">Recommandations en matière de conception d’interface utilisateur clavier</span><span class="sxs-lookup"><span data-stu-id="d7e76-118">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 