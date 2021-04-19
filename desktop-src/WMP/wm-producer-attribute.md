---
title: Attribut WM/Producer
description: L’attribut WM/Producer est le nom du producteur du contenu.
ms.assetid: b7c0dbea-ed57-4243-be76-90b2998304ba
keywords:
- Attribut WM/Producer Windows Media Player
topic_type:
- apiref
api_name:
- WM/Producer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 237b03231ac9882884aee1441877dce0de746d4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543289"
---
# <a name="wmproducer-attribute"></a>Attribut WM/Producer

L’attribut **WM/Producer** est le nom du producteur du contenu.

## <a name="applies-to"></a>S'applique à

-   [Attributs de fichiers Windows Media couramment utilisés](commonly-used-windows-media-file-attributes.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.

**ProducedBy** est un alias pour cet attribut.

La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMProducer.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





