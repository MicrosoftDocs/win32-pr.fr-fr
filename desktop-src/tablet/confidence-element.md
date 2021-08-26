---
description: Contient le niveau de confiance retourné par l’analyseur d’encre journal pour le InkWord.
ms.assetid: cb0ed0d0-5e2f-44a3-b72b-61cbfd22bae8
title: Élément confidence
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86e4169767f3bf40d49e71e84214d50d3c0c0b4ecf5d3f7a9034ee6c8ea279d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936979"
---
# <a name="confidence-element"></a>Élément confidence

Contient le niveau de confiance retourné par l’analyseur d’encre journal pour le [**InkWord**](inkword-element.md).

## <a name="definition"></a>Définition

``` syntax
<xs:element name="Confidence" type="xs:string" minOccurs="0" />
```

## <a name="parent-elements"></a>Éléments parents

[**InkWord**](inkword-element.md)

## <a name="values"></a>Valeurs

Les valeurs valides pour ce champ sont « 0 », « 1 » et « 2 ». 0 indique une confiance forte, 1 indique une confiance intermédiaire et 2 indique une confiance médiocre.

## <a name="child-elements"></a>Éléments enfants

Aucun.

## <a name="attributes"></a>Attributs

Aucun.

## <a name="element-information"></a>Informations sur les éléments



|                  | Valeur                                      |
|------------------|--------------------------------------------|
| **Type d’élément** | xs:string                                  |
| **Espace de noms**    | urn : schemas-microsoft-com : TabletPC : RichInk |
| **Nom du schéma**  | Lecteur de journal                             |



 

 

 



