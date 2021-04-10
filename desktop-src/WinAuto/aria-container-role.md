---
title: Erreur de rôle de conteneur ARIA
description: Erreur de rôle de conteneur ARIA
ms.assetid: AF207293-1172-43D0-B92C-C3070876DF54
keywords:
- AriaContainerRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02554c868816c05981fa9f008c8f79f0a3eb0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940272"
---
# <a name="aria-container-role-error"></a>Erreur de rôle de conteneur ARIA

## <a name="text"></a>Texte

L’élément avec un **descendant actif** défini n’a pas de rôle de conteneur (**ComboBox**, **Grid**, **ListBox**, **menu**, **BarreMenus**, **RadioGroup**, **Tree**, **contrôle TreeGrid**, **TabList**, **ligne**).

## <a name="type"></a>Type

Error

## <a name="description"></a>Description

Cette erreur s’applique aux éléments qui ont l’attribut **Aria-activedescendant** .

Un élément semble être un conteneur avec l’attribut **Aria-activedescendant** défini, mais l’attribut Role de l’élément n’a pas de valeur valide pour un conteneur.

Pour corriger cette erreur, définissez l’attribut **role** sur une valeur de rôle WAI-ARIA (Rich Internet applications) accessible par le Web Accessibility, qui est valide pour un élément conteneur : **ComboBox**, **Grid**, **ListBox**, **menu**, **BarreMenus**, **RadioGroup**, **TabList**, **Tree** ou **contrôle TreeGrid**.

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

[Erreur de rôle ARIA](aria-role-invalid.md)
</dt> </dl>

 

 




