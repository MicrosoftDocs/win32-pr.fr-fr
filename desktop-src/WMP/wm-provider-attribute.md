---
title: Attribut WM/Provider
description: L’attribut WM/Provider est le nom du fournisseur des valeurs d’attribut.
ms.assetid: 358651d3-5bcd-4a03-a9aa-a33745d0323a
keywords:
- Attribut WM/Provider lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/Provider
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d7c2c1c796edf28a567f72708c60c7976f718bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542537"
---
# <a name="wmprovider-attribute"></a>Attribut WM/Provider

L’attribut **WM/Provider** est le nom du fournisseur des valeurs d’attribut.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [Sélections de CD](cd-playlist-attributes.md)
-   [Pistes de CD](cd-track-attributes.md)
-   [Attributs de fichiers Windows Media couramment utilisés](commonly-used-windows-media-file-attributes.md)
-   [Éléments radio](radio-item-attributes.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké à la fois dans la bibliothèque (ou le cache) et dans le fichier multimédia numérique.

La **redatasource** est un alias pour cet attribut.

La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMProvider.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure (l’élément photo est pris en charge uniquement dans le lecteur Windows Media 10 ou version ultérieure)<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





