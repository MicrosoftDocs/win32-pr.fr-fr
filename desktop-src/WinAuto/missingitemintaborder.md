---
title: MissingItemInTabOrder
description: MissingItemInTabOrder
ms.assetid: 49DE892E-1B15-4F46-B316-217CC76AA1A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9841ab71e9f5d40cf25454e737b9790ce27a04de
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727517"
---
# <a name="missingitemintaborder"></a><span data-ttu-id="f72c1-103">MissingItemInTabOrder</span><span class="sxs-lookup"><span data-stu-id="f72c1-103">MissingItemInTabOrder</span></span>

## <a name="text"></a><span data-ttu-id="f72c1-104">Texte</span><span class="sxs-lookup"><span data-stu-id="f72c1-104">Text</span></span>

<span data-ttu-id="f72c1-105">Cet élément semble être tabbable, mais il n’est pas dans l’ordre de tabulation.</span><span class="sxs-lookup"><span data-stu-id="f72c1-105">This element appears to be tabbable but is not in the tab order.</span></span>

## <a name="type"></a><span data-ttu-id="f72c1-106">Type</span><span class="sxs-lookup"><span data-stu-id="f72c1-106">Type</span></span>

<span data-ttu-id="f72c1-107">Error</span><span class="sxs-lookup"><span data-stu-id="f72c1-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="f72c1-108">Description</span><span class="sxs-lookup"><span data-stu-id="f72c1-108">Description</span></span>

<span data-ttu-id="f72c1-109">Un élément pouvant être actif n’est pas accessible à l’aide de la navigation au clavier standard (Tab ou Maj + Tab).</span><span class="sxs-lookup"><span data-stu-id="f72c1-109">A focusable element is not accessible using standard keyboard navigation (Tab or Shift+Tab).</span></span> <span data-ttu-id="f72c1-110">Par exemple, l’élément n’a pas été marqué comme taquet de tabulation ou a assigné un index de tabulation.</span><span class="sxs-lookup"><span data-stu-id="f72c1-110">For example, the element has not been marked as a tab stop or assigned a tab index.</span></span> <span data-ttu-id="f72c1-111">Ce problème provoque des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car :</span><span class="sxs-lookup"><span data-stu-id="f72c1-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because:</span></span>

-   <span data-ttu-id="f72c1-112">L’élément n’est pas détectable.</span><span class="sxs-lookup"><span data-stu-id="f72c1-112">The element is not discoverable.</span></span>
-   <span data-ttu-id="f72c1-113">Si l’élément est un enfant d’un contrôle de liste personnalisé, les signaux indiquant que l’élément enfant peut être parcouru à l’aide des touches de direction ou de page sont peut-être manquants.</span><span class="sxs-lookup"><span data-stu-id="f72c1-113">If the element is a child of a custom list control, cues indicating the child element can be navigated using the Arrow or Page keys may be missing.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="f72c1-114">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="f72c1-114">Possible causes</span></span>

-   <span data-ttu-id="f72c1-115">Le rôle MSAA de l’élément ou de son parent n’est pas défini correctement.</span><span class="sxs-lookup"><span data-stu-id="f72c1-115">The MSAA role of the element or its parent is not set correctly.</span></span> <span data-ttu-id="f72c1-116">Par exemple, si tous les éléments de liste d’un contrôle List View ne sont pas exposés via MSAA comme un ListItem de système de rôle \_ \_ , la vérification échoue parce que les éléments de liste ne sont pas accessibles à l’aide de la touche Tab.</span><span class="sxs-lookup"><span data-stu-id="f72c1-116">For example, if all list items in a list view control are not exposed through MSAA as a ROLE\_SYSTEM\_LISTITEM, the verification fails because the list items are not accessible using the Tab key.</span></span>
-   <span data-ttu-id="f72c1-117">L’élément ou son parent est un contrôle personnalisé qui n’implémente pas correctement la tabulation.</span><span class="sxs-lookup"><span data-stu-id="f72c1-117">The element or its parent is a custom control that doesn't implement tabbing correctly.</span></span> <span data-ttu-id="f72c1-118">Par exemple, la propriété d’État MSAA n’est jamais définie sur STATE \_ System \_ Focusable.</span><span class="sxs-lookup"><span data-stu-id="f72c1-118">For example, the MSAA State property is never set to STATE\_SYSTEM\_FOCUSABLE.</span></span>
-   <span data-ttu-id="f72c1-119">Un élément qui joue le rôle d’un conteneur pour d’autres éléments a été sélectionné pour la vérification, mais ne prend pas en charge la navigation au clavier lui-même.</span><span class="sxs-lookup"><span data-stu-id="f72c1-119">An element that acts as a container for other elements was selected for verification but does not support keyboard navigation itself.</span></span> <span data-ttu-id="f72c1-120">Par exemple, une barre d’outils et ses éléments enfants ne sont pas accessibles à l’aide de la touche TAB.</span><span class="sxs-lookup"><span data-stu-id="f72c1-120">For example, a toolbar and its child elements are not accessible using the TAB key.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f72c1-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f72c1-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f72c1-122">Recommandations en matière de conception d’interface utilisateur clavier</span><span class="sxs-lookup"><span data-stu-id="f72c1-122">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 