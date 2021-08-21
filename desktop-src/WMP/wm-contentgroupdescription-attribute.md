---
title: Attribut WM/ContentGroupDescription
description: L’attribut WM/ContentGroupDescription est la description du groupe de contenu, qui est une collection d’éléments multimédias tels qu’un jeu de CD boxed.
ms.assetid: b2615f78-2d45-45f0-89f7-f1e8e083be9b
keywords:
- Lecteur Windows Media de l’attribut WM/ContentGroupDescription
topic_type:
- apiref
api_name:
- WM/ContentGroupDescription
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49af85d5064da7950c3208e0307f027accb5e31b4e474eb743e629ecdf05aa0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332448"
---
# <a name="wmcontentgroupdescription-attribute"></a>Attribut WM/ContentGroupDescription

L’attribut **WM/ContentGroupDescription** est la description du groupe de contenu, qui est une collection d’éléments multimédias tels qu’un jeu de CD boxed.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [attributs de fichier multimédia Windows couramment utilisés](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Remarques

Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.

**ContentGroupDescription** est un alias pour cet attribut.

la constante du kit de développement logiciel (SDK) du Format multimédia Windows pour cet attribut est g \_ wszWMContentGroupDistribution.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





