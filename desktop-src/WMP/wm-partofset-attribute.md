---
title: Attribut WM/PartOfSet
description: L’attribut WM/PartOfSet est le numéro de référence et le nombre total de parties de l’ensemble auquel appartient l’élément.
ms.assetid: c6827c31-c625-4283-a50d-f08eccf87271
keywords:
- Lecteur Windows Media de l’attribut WM/PartOfSet
topic_type:
- apiref
api_name:
- WM/PartOfSet
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27d6297931c503c95c8ef0462bf7b119a0ffb75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521941"
---
# <a name="wmpartofset-attribute"></a>Attribut WM/PartOfSet

L’attribut **WM/PartOfSet** est le numéro de référence et le nombre total de parties de l’ensemble auquel appartient l’élément.

## <a name="applies-to"></a>S'applique à

-   [Musique Fichiers](music-file-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké uniquement dans un fichier musical qui ne se trouve pas dans la bibliothèque.

la constante du kit de développement logiciel (SDK) du Format multimédia Windows pour cet attribut est g \_ wszWMPartOfSet.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





