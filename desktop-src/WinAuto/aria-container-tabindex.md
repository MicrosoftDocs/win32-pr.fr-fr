---
title: Erreur de TabIndex du conteneur ARIA
description: Erreur de TabIndex du conteneur ARIA
ms.assetid: CCEA9490-903D-423D-B9FD-641E8B7D3E0B
keywords:
- AriaContainerTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6af684b401627181aaef656215240a312393f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380307"
---
# <a name="aria-container-tabindex-error"></a>Erreur de TabIndex du conteneur ARIA

## <a name="text"></a>Texte

L’élément est un conteneur pouvant être actif avec des descendants actifs définis, mais sans valeur **TabIndex** supérieure ou égale à 0.

## <a name="type"></a>Type

Error

## <a name="description"></a>Description

Cette erreur s’applique aux éléments qui ont l’attribut **Aria-activedescendant** , qui ne sont pas désactivés et dont l’attribut **TabIndex** n’est pas défini sur une valeur supérieure ou égale à 0. Ces éléments doivent être dans l’ordre de tabulation, car ils sont chargés de gérer les événements de clavier pour leurs éléments enfants.

Pour corriger cette erreur, affectez à l’attribut **TabIndex** une valeur supérieure ou égale à 0.

## <a name="example"></a>Exemple


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1"> 
       <div role="option" id="listbox1-1" class="selected">Item 1</div> 
       <div role="option" id="listbox1-2">Item 2</div> 

       <div role="option" id="listbox1-3">Item 3</div>
      ... 
<div>
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Erreur TabIndex du rôle de conteneur ARIA (sans descendant actif)](aria-container--no-active-descendant--tabindex.md)
</dt> </dl>

 

 




