---
title: Attributs de contrôle de plage ARIA manquants
description: Attributs de contrôle de plage ARIA manquants
ms.assetid: B79F6277-5339-406A-B5FC-A3657BFC5034
keywords:
- AriaRangeControlAttributesAbsentId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8cd32a7a4807f06c26bd013ee3fd294d33cc57
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104032025"
---
# <a name="aria-range-control-attributes-missing"></a>Attributs de contrôle de plage ARIA manquants

## <a name="text"></a>Texte

L’élément a un rôle **ProgressBar** ou **Slider** , mais il n’expose pas les attributs **Aria-valuemin** , **Aria-ValueMax** et **Aria-valuenow** correspondants.

## <a name="type"></a>Type

Error

## <a name="description"></a>Description

Cette erreur s’applique aux éléments qui ont un [**rôle**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implicite ou explicite) qui est égal à **ProgressBar**, **Slider** ou **SpinButton**.

Conformément à la spécification de l’initiative de l’accessibilité du Web (WAI-ARIA) accessible par le Web, les éléments qui ont le rôle **ProgressBar**, **Slider** ou **SpinButton** doivent exposer les attributs [**Aria-ValueMax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)et [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .

Pour corriger cette erreur, définissez les attributs [**Aria-ValueMax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)et [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) , et conservez dynamiquement la valeur **Aria-valuenow** pour vous assurer que la valeur actuelle est exposée. Vous devez également définir l’attribut [**Aria-ValueText**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) pour ajouter une plus grande signification à la valeur **Aria-valuenow** exposée.

## <a name="example"></a>Exemple


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

 

 




