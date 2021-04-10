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
# <a name="aria-container-role-without-active-descendant-tabindex-error"></a><span data-ttu-id="a54c9-104">Erreur TabIndex du rôle de conteneur ARIA (sans descendant actif)</span><span class="sxs-lookup"><span data-stu-id="a54c9-104">ARIA Container Role (without active descendant) Tabindex Error</span></span>

## <a name="text"></a><span data-ttu-id="a54c9-105">Texte</span><span class="sxs-lookup"><span data-stu-id="a54c9-105">Text</span></span>

<span data-ttu-id="a54c9-106">L’élément est un conteneur pouvant être actif sans descendant actif défini, mais aucun élément enfant n’a une valeur **TabIndex** supérieure ou égale à 0.</span><span class="sxs-lookup"><span data-stu-id="a54c9-106">Element is a focusable container without active descendant defined, but no child element has **tabindex** greater or equal to 0.</span></span>

## <a name="type"></a><span data-ttu-id="a54c9-107">Type</span><span class="sxs-lookup"><span data-stu-id="a54c9-107">Type</span></span>

<span data-ttu-id="a54c9-108">Error</span><span class="sxs-lookup"><span data-stu-id="a54c9-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="a54c9-109">Description</span><span class="sxs-lookup"><span data-stu-id="a54c9-109">Description</span></span>

<span data-ttu-id="a54c9-110">Cette erreur s’applique aux éléments qui ont un rôle de conteneur, ne disposent pas d’un attribut **Aria-activedescendant** et ne sont pas désactivés.</span><span class="sxs-lookup"><span data-stu-id="a54c9-110">This error applies to elements that have a container role, do not have an **aria-activedescendant** attribute, and are not disabled.</span></span> <span data-ttu-id="a54c9-111">Ces éléments implémentent la navigation au clavier entre les éléments enfants à l’aide du concept appelé *index itinérant*.</span><span class="sxs-lookup"><span data-stu-id="a54c9-111">These elements implement keyboard navigation among child elements by using the concept known as *roving index*.</span></span> <span data-ttu-id="a54c9-112">Dans ce concept, les attributs **TabIndex** des éléments enfants sont conservés de manière dynamique, ce qui garantit qu’à tout moment, un seul élément enfant est dans l’ordre de tabulation.</span><span class="sxs-lookup"><span data-stu-id="a54c9-112">In this concept, the **tabindex** attributes of child elements are maintained dynamically, ensuring that at all times only one child element is in tab order.</span></span>

<span data-ttu-id="a54c9-113">Pour corriger cette erreur, affectez à l’attribut **TabIndex** de l’un des éléments enfants une valeur supérieure ou égale à 0.</span><span class="sxs-lookup"><span data-stu-id="a54c9-113">To fix this error, set the **tabindex** attribute of one of the child elements to a value equal to or greater than 0.</span></span>

## <a name="example"></a><span data-ttu-id="a54c9-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="a54c9-114">Example</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a54c9-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a54c9-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a54c9-116">Erreur de TabIndex du conteneur ARIA</span><span class="sxs-lookup"><span data-stu-id="a54c9-116">ARIA Container Tabindex Error</span></span>](aria-container-tabindex.md)
</dt> </dl>

 

 




