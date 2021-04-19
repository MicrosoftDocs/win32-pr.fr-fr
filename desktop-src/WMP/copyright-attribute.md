---
title: Attribut de Copyright (msfeeds. h)
description: L’attribut Copyright est le message de copyright de l’élément.
ms.assetid: 617272cb-883f-46d6-b0a9-29ac32c63148
keywords:
- Attribut de Copyright Windows Media Player
topic_type:
- apiref
api_name:
- Copyright
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c77a0db25663afde4f11199b23732c0cebe6226
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532602"
---
# <a name="copyright-attribute"></a>Attribut Copyright

L’attribut **Copyright** est le message de copyright de l’élément.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [Sélections de CD](cd-playlist-attributes.md)
-   [Pistes de CD](cd-track-attributes.md)
-   [Fichiers Windows Media couramment utilisés](commonly-used-windows-media-file-attributes.md)
-   [DVD](dvd-attributes.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké à la fois dans la bibliothèque (ou le cache) et dans le fichier multimédia numérique.

La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMCopyright.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/>                                    |
| En-tête<br/>  | <dl> <dt>Msfeeds. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





