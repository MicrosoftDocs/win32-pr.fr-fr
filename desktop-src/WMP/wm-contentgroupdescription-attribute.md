---
title: Attribut WM/ContentGroupDescription
description: L’attribut WM/ContentGroupDescription est la description du groupe de contenu, qui est une collection d’éléments multimédias tels qu’un jeu de CD boxed.
ms.assetid: b2615f78-2d45-45f0-89f7-f1e8e083be9b
keywords:
- Attribut WM/ContentGroupDescription lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/ContentGroupDescription
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4690e52f2745fa2761252fdba4ad4df31b18619
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530487"
---
# <a name="wmcontentgroupdescription-attribute"></a>Attribut WM/ContentGroupDescription

L’attribut **WM/ContentGroupDescription** est la description du groupe de contenu, qui est une collection d’éléments multimédias tels qu’un jeu de CD boxed.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [Attributs de fichiers Windows Media couramment utilisés](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.

**ContentGroupDescription** est un alias pour cet attribut.

La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMContentGroupDistribution.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





