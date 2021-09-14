---
title: EDITBOX. fontFace
description: L’attribut fontFace spécifie ou récupère la police du texte dans le contrôle zone d’édition.
ms.assetid: 5fb5e6d2-8535-402e-9ca1-d43e334e94e3
keywords:
- EDITBOX. fontFace Lecteur Windows Media
topic_type:
- apiref
api_name:
- EDITBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c5794da93821db840a48facbba45540da9249a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127191808"
---
# <a name="editboxfontface"></a>EDITBOX. fontFace

L’attribut **fontFace** spécifie ou récupère la police du texte dans le contrôle zone d’édition.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.

## <a name="remarks"></a>Notes

Cet attribut peut être le nom de toute police valide disponible dans Windows. Lecteur Windows Media ne prend pas en charge l’installation de polices, vous devez choisir une police sur le système souhaité.

si le **fontFace** spécifié n’est pas disponible sur le système de l’utilisateur, le contrôle de zone d’édition est défini par défaut sur la police système Windows. La valeur par défaut pour les systèmes en langue anglaise est « Tahoma ». Pour les systèmes internationaux, la valeur par défaut est chargée à partir d’un fichier de ressources.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------|
| Version<br/> | Lecteur Windows Media pour Windows XP ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément EDITBOX**](editbox-element.md)
</dt> <dt>

[**EDITBOX. FontSize**](editbox-fontsize.md)
</dt> <dt>

[**EDITBOX. fontStyle**](editbox-fontstyle.md)
</dt> </dl>

 

 





