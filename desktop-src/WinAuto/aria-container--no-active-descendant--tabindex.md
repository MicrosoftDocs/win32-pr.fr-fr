---
title: Erreur TabIndex du rôle de conteneur ARIA (sans descendant actif)
description: Erreur TabIndex du rôle de conteneur ARIA (sans descendant actif)
ms.assetid: E3CCA500-7104-4163-927C-94EA8F1E89D8
keywords:
- AriaContainerWithoutActiveDescendantTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a01d3391d93b7e7f146f379bcfecd629e14bce7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196808"
---
# <a name="aria-container-role-without-active-descendant-tabindex-error"></a>Erreur TabIndex du rôle de conteneur ARIA (sans descendant actif)

## <a name="text"></a>Texte

L’élément est un conteneur pouvant être actif sans descendant actif défini, mais aucun élément enfant n’a une valeur **TabIndex** supérieure ou égale à 0.

## <a name="type"></a>Type

Error

## <a name="description"></a>Description

Cette erreur s’applique aux éléments qui ont un rôle de conteneur, ne disposent pas d’un attribut **Aria-activedescendant** et ne sont pas désactivés. Ces éléments implémentent la navigation au clavier entre les éléments enfants à l’aide du concept appelé *index itinérant*. Dans ce concept, les attributs **TabIndex** des éléments enfants sont conservés de manière dynamique, ce qui garantit qu’à tout moment, un seul élément enfant est dans l’ordre de tabulation.

Pour corriger cette erreur, affectez à l’attribut **TabIndex** de l’un des éléments enfants une valeur supérieure ou égale à 0.

## <a name="example"></a>Exemple


```HTML
<div id="listbox" role="listbox1">
  <div role="option" id="listbox1-1" tabindex="0" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
</div>

<script>

  ...

  listbox1.addEventListener('keyup', function(e) {
    var itm = e.srcElement;
    var prev = itm.previousElementSibling;
    var next = itm.nextElementSibling;

    if (e.keyCode == 38 && prev) {
      // Arrow up to move focus to the previous item.
      itm.setAttribute('tabindex', '-1');
      prev.setAttribute('tabindex','0');
      prev.focus();
    } 

    else if (e.keyCode == 40 && next) {
      // Arrow down to move focus to the next item.
      itm.setAttribute('tabindex', '-1');
      next.setAttribute('tabindex','0');
      next.focus();
    }
  });

</script>
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Erreur de TabIndex du conteneur ARIA](aria-container-tabindex.md)
</dt> </dl>

 

 




