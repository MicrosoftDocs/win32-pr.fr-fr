---
description: Contient le niveau de confiance retourné par l’analyseur d’encre journal pour le InkWord.
ms.assetid: cb0ed0d0-5e2f-44a3-b72b-61cbfd22bae8
title: Élément Confidence
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fdaaed8d9c57822ad94ec49183a399ed317917
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294043"
---
# <a name="confidence-element"></a>Élément Confidence

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



 

 

 



