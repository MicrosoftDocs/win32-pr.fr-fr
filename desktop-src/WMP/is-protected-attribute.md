---
title: Attribut Is_Protected
description: L' \_ attribut is protected indique si le contenu est protégé à l’aide de la gestion des droits numériques (DRM).
ms.assetid: 049d4116-7ba6-49f5-ad54-82a98b79d6bc
keywords:
- attribut Is_Protected Lecteur Windows Media
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 520631b90e4ff379d3a613008dee2db5d76784a831ef54ef0d3551fbf99a85f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763859"
---
# <a name="is_protected-attribute"></a>\_Attribut protégé

L’attribut **is \_ protected** indique si le contenu est protégé à l’aide de la gestion des droits numériques (DRM).

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [fichiers multimédias Windows couramment utilisés](commonly-used-windows-media-file-attributes.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Remarques

Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.

**DigitallySecure** est un alias pour cet attribut.

la constante du kit de développement logiciel (SDK) du Format multimédia Windows pour cet attribut est g \_ wszWMProtected.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





