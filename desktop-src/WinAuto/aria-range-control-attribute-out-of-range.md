---
title: Attributs de contrôle de plage ARIA incompatibles
description: Attributs de contrôle de plage ARIA incompatibles
ms.assetid: 265AE578-D841-4931-9F4A-97BB86ECEC88
keywords:
- AriaRangeControlAttributesIncompatibleId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991f5de18be88682046cac6c4d4156f48fd3e4994d2e7b9ab1bbdc52f0a2e768
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326747"
---
# <a name="aria-range-control-attributes-incompatible"></a>Attributs de contrôle de plage ARIA incompatibles

## <a name="text"></a>Texte

L’élément a le rôle **ProgressBar** ou **Slider** , mais la valeur **Aria-valuenow** exposée est en dehors de la plage Aria **-valuemin** **Aria-ValueMax** .

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

Cette erreur s’applique aux éléments qui ont un [**rôle**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implicite ou explicite) égal à **ProgressBar**, **Slider** ou **SpinButton**.

Cette erreur indique que la valeur [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) exposée n’est pas dans la plage définie par les attributs [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) et [**Aria-ValueMax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .

Pour corriger cette erreur, vérifiez votre implémentation pour vous assurer que les attributs [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) et [**Aria-ValueMax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) sont correctement définis et que la valeur de l’attribut [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) est correctement gérée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attributs de contrôle de plage ARIA manquants](aria-range-control-attributes-missing.md)
</dt> </dl>

 

 




