---
title: Attribut WM/paroles
description: L’attribut WM/paroles correspond aux paroles du contenu.
ms.assetid: 125a2a51-81f2-478a-a9e9-234662a17bc0
keywords:
- Lecteur Windows Media des attributs WM/paroles
topic_type:
- apiref
api_name:
- WM/Lyrics
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f35f6b131fc41258dcce4490c731fde61ef8823cac164523b9b912c7d9586d9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122639"
---
# <a name="wmlyrics-attribute"></a>Attribut WM/paroles

L’attribut **WM/paroles** correspond aux paroles du contenu.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [Pistes de CD](cd-track-attributes.md)
-   [attributs de fichier multimédia Windows couramment utilisés](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Remarques

Cet attribut est stocké à la fois dans la bibliothèque (ou le cache) et dans le fichier multimédia numérique.

**Paroles** est un alias pour cet attribut.

la constante du kit de développement logiciel (SDK) du Format multimédia Windows pour cet attribut est g \_ wszWMLyrics.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





