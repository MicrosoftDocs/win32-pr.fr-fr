---
title: Attributs de contrôle de plage ARIA incompatibles
description: Attributs de contrôle de plage ARIA incompatibles
ms.assetid: 265AE578-D841-4931-9F4A-97BB86ECEC88
keywords:
- AriaRangeControlAttributesIncompatibleId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef55ee57c4966896e666dd5a7ac1d20eb5257c6
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104508182"
---
# <a name="aria-range-control-attributes-incompatible"></a>Attributs de contrôle de plage ARIA incompatibles

## <a name="text"></a>Texte

L’élément a le rôle **ProgressBar** ou **Slider** , mais la valeur **Aria-valuenow** exposée est en dehors de la plage Aria **-valuemin** **Aria-ValueMax** .

## <a name="type"></a>Type

Error

## <a name="description"></a>Description

Cette erreur s’applique aux éléments qui ont un [**rôle**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implicite ou explicite) égal à **ProgressBar**, **Slider** ou **SpinButton**.

Cette erreur indique que la valeur [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) exposée n’est pas dans la plage définie par les attributs [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) et [**Aria-ValueMax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .

Pour corriger cette erreur, vérifiez votre implémentation pour vous assurer que les attributs [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) et [**Aria-ValueMax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) sont correctement définis et que la valeur de l’attribut [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) est correctement gérée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attributs de contrôle de plage ARIA manquants](aria-range-control-attributes-missing.md)
</dt> </dl>

 

 




