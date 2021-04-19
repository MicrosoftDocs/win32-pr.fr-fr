---
title: Attribut WM/PartOfSet
description: L’attribut WM/PartOfSet est le numéro de référence et le nombre total de parties de l’ensemble auquel appartient l’élément.
ms.assetid: c6827c31-c625-4283-a50d-f08eccf87271
keywords:
- Attribut WM/PartOfSet lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/PartOfSet
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27d6297931c503c95c8ef0462bf7b119a0ffb75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537605"
---
# <a name="wmpartofset-attribute"></a>Attribut WM/PartOfSet

L’attribut **WM/PartOfSet** est le numéro de référence et le nombre total de parties de l’ensemble auquel appartient l’élément.

## <a name="applies-to"></a>S'applique à

-   [Fichiers musicaux](music-file-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké uniquement dans un fichier musical qui ne se trouve pas dans la bibliothèque.

La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMPartOfSet.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





