---
title: Erreur d’accessibilité du clavier du rôle de conteneur ARIA
description: Erreur d’accessibilité du clavier du rôle de conteneur ARIA
ms.assetid: 364F26D7-7B65-418B-9DA5-F3B7B59284F7
keywords:
- AriaContainerKeyboardAccessibilityErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085591e4f4834e8088b5ca199918d621f518e678
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310513"
---
# <a name="aria-container-role-keyboard-accessibility-error"></a><span data-ttu-id="781a2-104">Erreur d’accessibilité du clavier du rôle de conteneur ARIA</span><span class="sxs-lookup"><span data-stu-id="781a2-104">ARIA Container Role Keyboard Accessibility Error</span></span>

## <a name="text"></a><span data-ttu-id="781a2-105">Texte</span><span class="sxs-lookup"><span data-stu-id="781a2-105">Text</span></span>

<span data-ttu-id="781a2-106">L’élément est un conteneur avec une fonctionnalité descendante active et une fonctionnalité de souris personnalisée, mais sans la fonctionnalité de clavier correspondante : gestionnaires d’événements JavaScript pour **OnKeyDown** ou **OnKeyPress**.</span><span class="sxs-lookup"><span data-stu-id="781a2-106">Element is a container with active descendant and custom mouse functionality but without the corresponding keyboard functionality: JavaScript event handlers for **OnKeyDown** or **OnKeyPress**.</span></span>

## <a name="type"></a><span data-ttu-id="781a2-107">Type</span><span class="sxs-lookup"><span data-stu-id="781a2-107">Type</span></span>

<span data-ttu-id="781a2-108">Error</span><span class="sxs-lookup"><span data-stu-id="781a2-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="781a2-109">Description</span><span class="sxs-lookup"><span data-stu-id="781a2-109">Description</span></span>

<span data-ttu-id="781a2-110">Cette erreur s’applique aux éléments qui ont l’attribut **Aria-activedescendant** .</span><span class="sxs-lookup"><span data-stu-id="781a2-110">This error applies to elements that have the **aria-activedescendant** attribute.</span></span> <span data-ttu-id="781a2-111">Ces éléments ont un ou plusieurs gestionnaires d’événements de souris (**MouseMove**, **MouseDown** ou **MouseUp**), mais ils ne contiennent pas les gestionnaires d’événements de clavier équivalents (**keypg**, **KeyUp** ou **KeyPress**).</span><span class="sxs-lookup"><span data-stu-id="781a2-111">These elements have one or more mouse event handlers (**mousemove**, **mousedown** or **mouseup**), but are missing the equivalent keyboard event handlers (**keydown**, **keyup** or **keypress**).</span></span> <span data-ttu-id="781a2-112">Les gestionnaires d’événements de clavier sont nécessaires pour s’assurer que l’utilisateur peut appeler la fonctionnalité de l’élément à l’aide du clavier et pour s’assurer que l’élément gère l’attribut **Aria-activedescendant** .</span><span class="sxs-lookup"><span data-stu-id="781a2-112">The keyboard event handlers are needed to ensure that the user can invoke the element's functionality by using the keyboard, and to ensure that the element maintains the **aria-activedescendant** attribute.</span></span>

<span data-ttu-id="781a2-113">Pour corriger cette erreur, implémentez l’un des gestionnaires d’événements de clavier.</span><span class="sxs-lookup"><span data-stu-id="781a2-113">To fix this error, implement one of the keyboard event handlers.</span></span>

## <a name="example"></a><span data-ttu-id="781a2-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="781a2-114">Example</span></span>


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1"> 
  <div role="option" id="listbox1-1" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
</div>

<script>

   ...

  listbox1.addEventListener('keyup', function(e) {
    var itm = document.getElementById(this.getAttribute('aria-activedescendant'));
    var prev = itm.previousElementSibling;
    var next = itm.nextElementSibling;
    
    if ( e.keyCode  38 && prev ) {
      // Arrow up to move active descendant to the previous item
      itm.removeAttribute('class’);
      prev.setAttribute("class", "selected");
      this.setAttribute ('aria-activedescendant', prev.id)
    } 

    else if ( e.keyCode == 40 && next) {
      // Arrow down to move focus to the next item
      itm.removeAttribute('class’);
      next.setAttribute("class", "selected");
      this.setAttribute ('aria-activedescendant', next.id)
    }
  });      

</script>
```



## <a name="related-topics"></a><span data-ttu-id="781a2-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="781a2-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="781a2-116">Rôle de conteneur ARIA (sans descendant actif) erreur d’accessibilité du clavier</span><span class="sxs-lookup"><span data-stu-id="781a2-116">ARIA Container Role (without active descendant) Keyboard Accessibility Error</span></span>](aria-container--no-active-descendants--keyboard-events.md)
</dt> </dl>

 

 




