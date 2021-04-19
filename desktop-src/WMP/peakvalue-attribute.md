---
title: Attribut PeakValue
description: L’attribut PeakValue est une valeur d’amplitude de 16 bits indiquant le niveau de volume maximal.
ms.assetid: 5d80a1f3-015c-4740-bd1c-f3bbf88a9df2
keywords:
- Attribut PeakValue lecteur Windows Media
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74fde522e043adb8b11c25bede763bed6b252f2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537874"
---
# <a name="peakvalue-attribute"></a>Attribut PeakValue

L’attribut **PeakValue** est une valeur d’amplitude de 16 bits indiquant le niveau de volume maximal.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [Fichiers Windows Media couramment utilisés](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.

Le lecteur Windows Media définit cette valeur dans l’une ou l’autre des situations suivantes :

-   Après avoir extrait un fichier.
-   Après avoir lu un fichier (lorsque l’optimisation du niveau de volume automatique est activée).

La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszPeakValue.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





