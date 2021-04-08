---
title: Rôle de conteneur ARIA (sans descendant actif) erreur d’accessibilité du clavier
description: Rôle de conteneur ARIA (sans descendant actif) erreur d’accessibilité du clavier
ms.assetid: 15EDD3CC-FC2A-42FC-95DD-B04D9AF3515E
keywords:
- AriaContainerWithoutActiveDescendantKeyboardAccessiblityId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9e30e0194f156426e2b61aa774ac1f3e0f5b91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840002"
---
# <a name="aria-container-role-without-active-descendant-keyboard-accessibility-error"></a><span data-ttu-id="d48b7-104">Rôle de conteneur ARIA (sans descendant actif) erreur d’accessibilité du clavier</span><span class="sxs-lookup"><span data-stu-id="d48b7-104">ARIA Container Role (without active descendant) Keyboard Accessibility Error</span></span>

## <a name="text"></a><span data-ttu-id="d48b7-105">Texte</span><span class="sxs-lookup"><span data-stu-id="d48b7-105">Text</span></span>

<span data-ttu-id="d48b7-106">L’élément est un conteneur pouvant être actif sans descendant actif défini et sans /  / gestionnaires d’événements OnKeyDown OnKeyPress **onkeyup** (ni sur le conteneur, ni sur l’un des éléments enfants).</span><span class="sxs-lookup"><span data-stu-id="d48b7-106">Element is a focusable container without active descendant defined and without **OnKeyDown**/**OnKeyPress**/**OnKeyUp** event handlers (neither on container nor on one of child elements).</span></span>

## <a name="type"></a><span data-ttu-id="d48b7-107">Type</span><span class="sxs-lookup"><span data-stu-id="d48b7-107">Type</span></span>

<span data-ttu-id="d48b7-108">Error</span><span class="sxs-lookup"><span data-stu-id="d48b7-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="d48b7-109">Description</span><span class="sxs-lookup"><span data-stu-id="d48b7-109">Description</span></span>

<span data-ttu-id="d48b7-110">Cette erreur s’applique aux éléments qui ont un rôle de conteneur, ne disposent pas d’un attribut **Aria-activedescendant** et ne sont pas désactivés.</span><span class="sxs-lookup"><span data-stu-id="d48b7-110">This error applies to elements that have a container role, do not have an **aria-activedescendant** attribute, and are not disabled.</span></span> <span data-ttu-id="d48b7-111">Ces éléments implémentent la navigation au clavier entre les éléments enfants à l’aide du concept appelé *index itinérant*.</span><span class="sxs-lookup"><span data-stu-id="d48b7-111">These elements implement keyboard navigation among child elements by using the concept known as *roving index*.</span></span> <span data-ttu-id="d48b7-112">Dans ce concept, les attributs **TabIndex** des éléments enfants sont conservés de manière dynamique, ce qui garantit qu’à tout moment, un seul élément enfant est dans l’ordre de tabulation.</span><span class="sxs-lookup"><span data-stu-id="d48b7-112">In this concept, the **tabindex** attributes of child elements are maintained dynamically, ensuring that at all times only one child element is in tab order.</span></span>

<span data-ttu-id="d48b7-113">Cette erreur indique qu’un élément conteneur qui n’a pas l’attribut **Aria-activedescendant** , et qui n’est pas désactivé, n’est pas accessible aux utilisateurs du clavier.</span><span class="sxs-lookup"><span data-stu-id="d48b7-113">This error indicates that a container element that does not have the **aria-activedescendant** attribute, and that is not disabled, is not accessible to keyboard users.</span></span> <span data-ttu-id="d48b7-114">Le problème est dû au fait que le conteneur n’a pas les gestionnaires d’événements de clavier nécessaires (**keypg**, **KeyUp** ou **KeyPress**) et qu’aucun des éléments enfants du conteneur n’est utilisé.</span><span class="sxs-lookup"><span data-stu-id="d48b7-114">The problem exists because the container does not have the needed keyboard event handlers (**keydown**, **keyup**, or **keypress**), and neither do any of the container's child elements.</span></span>

<span data-ttu-id="d48b7-115">Pour corriger cette erreur, définissez un gestionnaire d’événements **keyverse**, **KeyUp** ou **KeyPress** pour le conteneur ou l’un de ses éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="d48b7-115">To fix this error, define a **keydown**, **keyup**, or **keypress** event handler for the container or one of its child elements.</span></span>

## <a name="example"></a><span data-ttu-id="d48b7-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="d48b7-116">Example</span></span>


```HTML
<div role="listbox" id="listbox1" >
  <div role="option" id="listbox1-1" tabindex="0" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
  ...
<div>

<script>

  ...

  listbox1.addEventListener('keyup', function(e) {
    var itm = e.srcElement;
    var prev = itm.previousElementSibling;
    var next = itm.nextElementSibling;

    if (e.keyCode == 38 && prev) {
      // On arrow up move focus to the previous item.
      itm.setAttribute('tabindex', '-1');
      prev.setAttribute('tabindex','0');
      prev.focus();
    }

    else if (e.keyCode == 40 && next) {
      // On arrow down move focus to the next item.
      itm.setAttribute('tabindex', '-1');
      next.setAttribute('tabindex','0');
      next.focus();
    }
  });

</script>
```



## <a name="related-topics"></a><span data-ttu-id="d48b7-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d48b7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d48b7-118">Erreur d’accessibilité du clavier du rôle de conteneur ARIA</span><span class="sxs-lookup"><span data-stu-id="d48b7-118">ARIA Container Role Keyboard Accessibility Error</span></span>](aria-container-keyboard-events.md)
</dt> </dl>

 

 




