---
title: EDITBOX. editStyle
description: L’attribut editStyle spécifie ou récupère le style du contrôle zone d’édition.
ms.assetid: 1b3052c4-3087-4d41-af03-d7758680cc3b
keywords:
- EDITBOX. editStyle Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.editStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229f225dfca0ec00dd4f45a4eb63f6b2503d5df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525524"
---
# <a name="editboxeditstyle"></a>EDITBOX. editStyle

L’attribut **editStyle** spécifie ou récupère le style du contrôle zone d’édition.

``` syntax
        elementID.editStyle
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant l’une des valeurs suivantes.



| Valeur     | Description                                                                     |
|-----------|---------------------------------------------------------------------------------|
| normal    | Par défaut. Affiche le texte normal sur une seule ligne.                                 |
| mot de passe  | Affiche des astérisques ( \* ) à la place du texte. Peut uniquement être spécifié au moment de la conception. |
| majuscules | Affiche le texte en majuscules.                                                 |
| minuscules | Affiche le texte en minuscules.                                                 |
| nombre    | Affiche uniquement les nombres.                                                          |
| lambda | Affiche plusieurs lignes de texte. Peut uniquement être spécifié au moment de la conception.          |



 

## <a name="remarks"></a>Notes

Cet attribut peut uniquement être défini sur « mot de passe » ou « multiligne » au moment de la conception. S’il est défini sur « multiligne », la valeur ne peut pas être modifiée au moment de l’exécution.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------|
| Version<br/> | Lecteur Windows Media pour Windows XP ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément EDITBOX**](editbox-element.md)
</dt> </dl>

 

 





