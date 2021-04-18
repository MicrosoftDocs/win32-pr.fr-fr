---
title: Attribut WM/ProviderStyle
description: L’attribut WM/ProviderStyle est le style de l’élément assigné par le fournisseur des valeurs d’attribut.
ms.assetid: 43994d6b-0d71-4f2c-834a-47bbcd32b461
keywords:
- Attribut WM/ProviderStyle lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/ProviderStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a18af02254e7ce476ffc9c1e427465966cd66c84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540541"
---
# <a name="wmproviderstyle-attribute"></a>Attribut WM/ProviderStyle

L’attribut **WM/ProviderStyle** est le style de l’élément assigné par le fournisseur des valeurs d’attribut.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [Sélections de CD](cd-playlist-attributes.md)
-   [Pistes de CD](cd-track-attributes.md)
-   [Attributs de fichiers Windows Media couramment utilisés](commonly-used-windows-media-file-attributes.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké à la fois dans la bibliothèque (ou le cache) et dans le fichier multimédia numérique.

**Style** est un alias pour cet attribut.

La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMProviderStyle.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





