---
title: Rôle de conteneur ARIA (sans descendant actif) erreur d’accessibilité du clavier
description: Rôle de conteneur ARIA (sans descendant actif) erreur d’accessibilité du clavier
ms.assetid: 15EDD3CC-FC2A-42FC-95DD-B04D9AF3515E
keywords:
- AriaContainerWithoutActiveDescendantKeyboardAccessiblityId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30b653ac3bf2dc8254b25c52a89cdb3503b89b9f05997a3ea9fb4f4ef3a77cb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071879"
---
# <a name="aria-container-role-without-active-descendant-keyboard-accessibility-error"></a>Rôle de conteneur ARIA (sans descendant actif) erreur d’accessibilité du clavier

## <a name="text"></a>Texte

L’élément est un conteneur pouvant être actif sans descendant actif défini et sans /  / gestionnaires d’événements OnKeyDown OnKeyPress **onkeyup** (ni sur le conteneur, ni sur l’un des éléments enfants).

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

Cette erreur s’applique aux éléments qui ont un rôle de conteneur, ne disposent pas d’un attribut **Aria-activedescendant** et ne sont pas désactivés. Ces éléments implémentent la navigation au clavier entre les éléments enfants à l’aide du concept appelé *index itinérant*. Dans ce concept, les attributs **TabIndex** des éléments enfants sont conservés de manière dynamique, ce qui garantit qu’à tout moment, un seul élément enfant est dans l’ordre de tabulation.

Cette erreur indique qu’un élément conteneur qui n’a pas l’attribut **Aria-activedescendant** , et qui n’est pas désactivé, n’est pas accessible aux utilisateurs du clavier. Le problème est dû au fait que le conteneur n’a pas les gestionnaires d’événements de clavier nécessaires (**keypg**, **KeyUp** ou **KeyPress**) et qu’aucun des éléments enfants du conteneur n’est utilisé.

Pour corriger cette erreur, définissez un gestionnaire d’événements **keyverse**, **KeyUp** ou **KeyPress** pour le conteneur ou l’un de ses éléments enfants.

## <a name="example"></a>Exemples


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Erreur d’accessibilité du clavier du rôle de conteneur ARIA](aria-container-keyboard-events.md)
</dt> </dl>

 

 




