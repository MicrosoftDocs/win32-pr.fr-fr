---
title: Attribut WM/TrackNumber
description: L’attribut WM/TrackNumber est le numéro de suivi de l’élément sur l’album sur lequel il a été publié à l’origine.
ms.assetid: d1fc5bac-c440-470f-be5c-5aca74aee99e
keywords:
- Attribut WM/TrackNumber lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/TrackNumber
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecd9adf3a939a5087ee270e8bef4d4d510b678ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539932"
---
# <a name="wmtracknumber-attribute"></a>Attribut WM/TrackNumber

L’attribut **WM/TrackNumber** est le numéro de suivi de l’élément sur l’album sur lequel il a été publié à l’origine.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [Attributs de fichiers Windows Media couramment utilisés](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.

Le suivi des nombres pour un album commence à 1.

**OriginalIndex** et **OriginalIndexLeft** sont des alias de cet attribut.

La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMTrackNumber.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





