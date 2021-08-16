---
title: Attribut WM/EncodingTime
description: L’attribut WM/EncodingTime est la date et l’heure auxquelles le contenu a été encodé.
ms.assetid: 264f379a-0bec-4143-bc23-ab45fb725af6
keywords:
- Lecteur Windows Media de l’attribut WM/EncodingTime
topic_type:
- apiref
api_name:
- WM/EncodingTime
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b143218b854177852049c1ae1ed530360c196eecd217db3ed53d9f46bd2915
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122659"
---
# <a name="wmencodingtime-attribute"></a>Attribut WM/EncodingTime

L’attribut **WM/EncodingTime** est la date et l’heure auxquelles le contenu a été encodé.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [attributs de fichier multimédia Windows couramment utilisés](commonly-used-windows-media-file-attributes.md)
-   [Sélections](playlist-attributes-ref.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Remarques

Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.

**CreationDate** est un alias pour cet attribut.

la constante du kit de développement logiciel (SDK) du Format multimédia Windows pour cet attribut est g \_ wszWMEncodingTime.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





