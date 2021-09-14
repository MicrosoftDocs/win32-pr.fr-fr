---
title: Attribut PeakValue
description: L’attribut PeakValue est une valeur d’amplitude de 16 bits indiquant le niveau de volume maximal.
ms.assetid: 5d80a1f3-015c-4740-bd1c-f3bbf88a9df2
keywords:
- Lecteur Windows Media de l’attribut PeakValue
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74fde522e043adb8b11c25bede763bed6b252f2f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192767"
---
# <a name="peakvalue-attribute"></a>Attribut PeakValue

L’attribut **PeakValue** est une valeur d’amplitude de 16 bits indiquant le niveau de volume maximal.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [fichiers multimédias Windows couramment utilisés](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.

Lecteur Windows Media définit cette valeur dans l’une des instances suivantes :

-   Après avoir extrait un fichier.
-   Après avoir lu un fichier (lorsque l’optimisation du niveau de volume automatique est activée).

la constante du kit de développement logiciel (SDK) du Format multimédia Windows pour cet attribut est g \_ wszPeakValue.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





