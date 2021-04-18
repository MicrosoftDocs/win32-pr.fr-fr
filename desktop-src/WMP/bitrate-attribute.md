---
title: Attribut de débit binaire
description: L’attribut de débit binaire est la vitesse de transmission de l’élément, en bits par seconde.
ms.assetid: 19117ca7-fad3-469e-8208-c0b899e13919
keywords:
- Attribut de débit binaire Windows Media Player
topic_type:
- apiref
api_name:
- Bitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9869ffdf9df85fdfb019d6a088fabfb0cb05c2b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540603"
---
# <a name="bitrate-attribute"></a>Attribut de débit binaire

L’attribut de **débit** binaire est la vitesse de transmission de l’élément, en bits par seconde.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [Fichiers Windows Media couramment utilisés](commonly-used-windows-media-file-attributes.md)
-   [Autres éléments](other-item-attributes.md)
-   [Éléments radio](radio-item-attributes.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.

La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMBitrate.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





