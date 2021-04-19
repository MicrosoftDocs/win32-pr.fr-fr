---
title: Description, attribut (kit de développement logiciel (SDK) WMP)
description: L’attribut Description est une description du contenu.
ms.assetid: 8bf76bf5-2bba-4ceb-bc98-f8b8ab2c8b6f
keywords:
- Description attribute Windows Media Player
topic_type:
- apiref
api_name:
- Description
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c4bc3562e7b807dc0e333c887aad1550d05b0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530442"
---
# <a name="description-attribute"></a>Description (attribut)

L’attribut **Description** est une description du contenu.

## <a name="applies-to"></a>S'applique à

-   [Fichiers musicaux](music-file-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké dans des fichiers musicaux, et non dans la bibliothèque.

Cet attribut peut avoir plusieurs valeurs. Pour récupérer toutes les valeurs d’un attribut à valeurs multiples, vous devez utiliser le *média*. méthode **getItemInfoByType** , et non la méthode *Media*. getItemInfo.

La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMDescription.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





