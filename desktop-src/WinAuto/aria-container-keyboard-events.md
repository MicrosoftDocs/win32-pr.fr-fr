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
# <a name="aria-container-role-keyboard-accessibility-error"></a>Erreur d’accessibilité du clavier du rôle de conteneur ARIA

## <a name="text"></a>Texte

L’élément est un conteneur avec une fonctionnalité descendante active et une fonctionnalité de souris personnalisée, mais sans la fonctionnalité de clavier correspondante : gestionnaires d’événements JavaScript pour **OnKeyDown** ou **OnKeyPress**.

## <a name="type"></a>Type

Error

## <a name="description"></a>Description

Cette erreur s’applique aux éléments qui ont l’attribut **Aria-activedescendant** . Ces éléments ont un ou plusieurs gestionnaires d’événements de souris (**MouseMove**, **MouseDown** ou **MouseUp**), mais ils ne contiennent pas les gestionnaires d’événements de clavier équivalents (**keypg**, **KeyUp** ou **KeyPress**). Les gestionnaires d’événements de clavier sont nécessaires pour s’assurer que l’utilisateur peut appeler la fonctionnalité de l’élément à l’aide du clavier et pour s’assurer que l’élément gère l’attribut **Aria-activedescendant** .

Pour corriger cette erreur, implémentez l’un des gestionnaires d’événements de clavier.

## <a name="example"></a>Exemple


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rôle de conteneur ARIA (sans descendant actif) erreur d’accessibilité du clavier](aria-container--no-active-descendants--keyboard-events.md)
</dt> </dl>

 

 




