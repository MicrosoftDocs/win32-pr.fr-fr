---
title: Erreur de TabIndex du conteneur ARIA
description: Erreur de TabIndex du conteneur ARIA
ms.assetid: CCEA9490-903D-423D-B9FD-641E8B7D3E0B
keywords:
- AriaContainerTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ff7149a82ddf45abb50175202ba2ea2ef8be854eef307643b207e796ab26cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899579"
---
# <a name="aria-container-tabindex-error"></a>Erreur de TabIndex du conteneur ARIA

## <a name="text"></a>Texte

L’élément est un conteneur pouvant être actif avec des descendants actifs définis, mais sans valeur **TabIndex** supérieure ou égale à 0.

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

Cette erreur s’applique aux éléments qui ont l’attribut **Aria-activedescendant** , qui ne sont pas désactivés et dont l’attribut **TabIndex** n’est pas défini sur une valeur supérieure ou égale à 0. Ces éléments doivent être dans l’ordre de tabulation, car ils sont chargés de gérer les événements de clavier pour leurs éléments enfants.

Pour corriger cette erreur, affectez à l’attribut **TabIndex** une valeur supérieure ou égale à 0.

## <a name="example"></a>Exemples


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

 

 




