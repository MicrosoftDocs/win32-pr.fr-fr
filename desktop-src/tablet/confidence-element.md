---
description: Contient le niveau de confiance retourné par l’analyseur d’encre journal pour le InkWord.
ms.assetid: cb0ed0d0-5e2f-44a3-b72b-61cbfd22bae8
title: Élément confidence
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cef4869776a6cafc4e6ef4758649b918e0b5988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112015"
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

Aucun

## <a name="attributes"></a>Attributs

Aucun

## <a name="element-information"></a>Informations sur les éléments



|              |                                            |
|--------------|--------------------------------------------|
| Type d'élément | **xs:string**                              |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk |
| Nom du schéma  | Lecteur de journal                             |



 

 

 



