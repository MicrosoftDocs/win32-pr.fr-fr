---
title: LISTBOX. fontFace
description: L’attribut fontFace spécifie ou récupère la police du contrôle de zone de liste.
ms.assetid: 15e3180a-6e1e-4654-a0bb-164d66a86a26
keywords:
- LISTBOX. fontFace Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c03c367001b307dd8bd5059ec7e3f4a0b364e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532617"
---
# <a name="listboxfontface"></a>LISTBOX. fontFace

L’attribut **fontFace** spécifie ou récupère la police du contrôle de zone de liste.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.

## <a name="remarks"></a>Notes

Cet attribut peut être le nom de toute police valide disponible dans Windows. Le lecteur Windows Media ne prend pas en charge l’installation de polices. vous devez donc choisir une police sur le système souhaité.

Si le **fontFace** spécifié n’est pas disponible sur le système de l’utilisateur, le contrôle de zone de liste est défini par défaut sur la police système Windows. La valeur par défaut pour les systèmes en langue anglaise est « Tahoma ». Pour les systèmes internationaux, la valeur par défaut est chargée à partir d’un fichier de ressources.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------|
| Version<br/> | Lecteur Windows Media pour Windows XP ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément LISTBOX**](listbox-element.md)
</dt> <dt>

[**LISTBOX. FontSize**](listbox-fontsize.md)
</dt> <dt>

[**LISTBOX. fontStyle**](listbox-fontstyle.md)
</dt> </dl>

 

 





