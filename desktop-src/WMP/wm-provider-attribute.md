---
title: Attribut WM/Provider
description: L’attribut WM/Provider est le nom du fournisseur des valeurs d’attribut.
ms.assetid: 358651d3-5bcd-4a03-a9aa-a33745d0323a
keywords:
- attribut WM/Provider Lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/Provider
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7fa8312d095151145cfe33a139def23e20082aec2cd1d5f1c3344b9b565dfb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119735369"
---
# <a name="wmprovider-attribute"></a>Attribut WM/Provider

L’attribut **WM/Provider** est le nom du fournisseur des valeurs d’attribut.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [Sélections de CD](cd-playlist-attributes.md)
-   [Pistes de CD](cd-track-attributes.md)
-   [attributs de fichier multimédia Windows couramment utilisés](commonly-used-windows-media-file-attributes.md)
-   [Éléments radio](radio-item-attributes.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Remarques

Cet attribut est stocké à la fois dans la bibliothèque (ou le cache) et dans le fichier multimédia numérique.

La **redatasource** est un alias pour cet attribut.

la constante du kit de développement logiciel (SDK) du Format multimédia Windows pour cet attribut est g \_ wszWMProvider.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure (l’élément photo est pris en charge uniquement dans Lecteur Windows Media 10 ou version ultérieure)<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





