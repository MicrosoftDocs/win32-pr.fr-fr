---
title: Attribut AverageLevel
description: L’attribut AverageLevel est une valeur d’amplitude de 16 bits indiquant le niveau de volume moyen.
ms.assetid: 04ff19f1-a9a5-4e47-86a6-50c6f08b0d7d
keywords:
- Lecteur Windows Media de l’attribut AverageLevel
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e169b1e2d63e6f8215515acc852d431ff13ccd513924e4c2a237b16c17dacfc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582744"
---
# <a name="averagelevel-attribute"></a>Attribut AverageLevel

L’attribut **AverageLevel** est une valeur d’amplitude de 16 bits indiquant le niveau de volume moyen.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [fichiers multimédias Windows couramment utilisés](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.

Lecteur Windows Media définit cette valeur dans l’une des instances suivantes :

-   Après avoir extrait un fichier.
-   Après avoir lu un fichier (lorsque l’optimisation du niveau de volume automatique est activée).

la constante du kit de développement logiciel (SDK) du Format multimédia Windows pour cet attribut est g \_ wszAverageLevel.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





