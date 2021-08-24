---
title: Attributs de contrôle de plage ARIA manquants
description: Attributs de contrôle de plage ARIA manquants
ms.assetid: B79F6277-5339-406A-B5FC-A3657BFC5034
keywords:
- AriaRangeControlAttributesAbsentId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b44e4e5c69ea6971846ed9ef5f3a6108bb488c6effb21a6cbc75953ed1bb780e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645118"
---
# <a name="aria-range-control-attributes-missing"></a>Attributs de contrôle de plage ARIA manquants

## <a name="text"></a>Texte

L’élément a un rôle **ProgressBar** ou **Slider** , mais il n’expose pas les attributs **Aria-valuemin** , **Aria-ValueMax** et **Aria-valuenow** correspondants.

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

Cette erreur s’applique aux éléments qui ont un [**rôle**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implicite ou explicite) qui est égal à **ProgressBar**, **Slider** ou **SpinButton**.

Conformément à la spécification de l’initiative de l’accessibilité du Web (WAI-ARIA) accessible par le Web, les éléments qui ont le rôle **ProgressBar**, **Slider** ou **SpinButton** doivent exposer les attributs [**Aria-ValueMax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)et [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .

Pour corriger cette erreur, définissez les attributs [**Aria-ValueMax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)et [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) , et conservez dynamiquement la valeur **Aria-valuenow** pour vous assurer que la valeur actuelle est exposée. Vous devez également définir l’attribut [**Aria-ValueText**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) pour ajouter une plus grande signification à la valeur **Aria-valuenow** exposée.

## <a name="example"></a>Exemples


```HTML
<div role="slider" id="sl" aria-valuemin="1" aria-valuemax="5" aria-valuenow="3" aria-valuetext="good"…>
</div>

<script>
  // This function should be triggered when the slider value changes.
  function manageValue()
  {
    ...
    sl.setAttribute("aria-valuenow", currentValue);
    sl.setAttribute("aria-valuetext", currentValueText);
    ...
  }
</script>
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attributs de contrôle de plage ARIA incompatibles](aria-range-control-attribute-out-of-range.md)
</dt> </dl>

 

 




