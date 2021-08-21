---
title: Attribut WM/ProtectionType
description: L’attribut WM/ProtectionType est le type de protection utilisé sur le contenu.
ms.assetid: aab36b57-5b4e-4a3f-80cf-872ec8369c49
keywords:
- Lecteur Windows Media de l’attribut WM/ProtectionType
topic_type:
- apiref
api_name:
- WM/ProtectionType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7888273aaca38a4fb87c5a19fc7c7bc8d47b13a8b6a03a578354b1a8bcd2b3dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900349"
---
# <a name="wmprotectiontype-attribute"></a>Attribut WM/ProtectionType

L’attribut **WM/ProtectionType** est le type de protection utilisé sur le contenu.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [attributs de fichier multimédia Windows couramment utilisés](commonly-used-windows-media-file-attributes.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Remarques

Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.

**ProtectionType** est un alias pour cet attribut.

la constante du kit de développement logiciel (SDK) du Format multimédia Windows pour cet attribut est g \_ wszWMProtectionType.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





