---
title: Attribut IsVBR
description: L’attribut IsVBR indique si le contenu a été encodé à l’aide de l’encodage VBR (variable binaire rate).
ms.assetid: faec0940-ef53-40a1-be54-a990884e907d
keywords:
- Lecteur Windows Media de l’attribut IsVBR
topic_type:
- apiref
api_name:
- IsVBR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6b5b190e67c07978207823cef9992243be772d430e2f03f40695ae6510c39a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054817"
---
# <a name="isvbr-attribute"></a>Attribut IsVBR

L’attribut **IsVBR** indique si le contenu a été encodé à l’aide de l’encodage VBR (variable binaire rate).

## <a name="applies-to"></a>S'applique à

-   [fichiers multimédias Windows couramment utilisés](commonly-used-windows-media-file-attributes.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Remarques

Cet attribut est stocké uniquement dans le fichier multimédia numérique.

la constante du kit de développement logiciel (SDK) du Format multimédia Windows pour cet attribut est g \_ wszWMIsVBR.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





