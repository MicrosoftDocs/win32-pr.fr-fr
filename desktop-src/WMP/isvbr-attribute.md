---
title: Attribut IsVBR
description: L’attribut IsVBR indique si le contenu a été encodé à l’aide de l’encodage VBR (variable binaire rate).
ms.assetid: faec0940-ef53-40a1-be54-a990884e907d
keywords:
- Attribut IsVBR lecteur Windows Media
topic_type:
- apiref
api_name:
- IsVBR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaec9f740e7b251c73ed12f5897ff9d95b023886
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537096"
---
# <a name="isvbr-attribute"></a>Attribut IsVBR

L’attribut **IsVBR** indique si le contenu a été encodé à l’aide de l’encodage VBR (variable binaire rate).

## <a name="applies-to"></a>S'applique à

-   [Fichiers Windows Media couramment utilisés](commonly-used-windows-media-file-attributes.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké uniquement dans le fichier multimédia numérique.

La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMIsVBR.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





