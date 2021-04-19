---
title: TEXT. fontFace
description: L’attribut fontFace spécifie ou récupère le caractère du contrôle de texte.
ms.assetid: 3b39e245-139a-4361-b678-0f9e962996b7
keywords:
- TEXT. fontFace Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 183b25547e456cb90cac4d2137354679e13d8a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526325"
---
# <a name="textfontface"></a>TEXT. fontFace

L’attribut **fontFace** spécifie ou récupère le caractère du contrôle de texte.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.

## <a name="remarks"></a>Notes

Cet attribut peut être le nom de toute police valide disponible sur Windows. Le lecteur Windows Media ne prend pas en charge l’installation de polices. vous devez donc choisir une police sur le système souhaité.

Si le **fontFace** spécifié n’est pas disponible sur le système de l’utilisateur, le contrôle de texte prend par défaut la police système Windows.

Pour obtenir un exemple illustrant l’utilisation des attributs de l’élément de **texte** , consultez l’attribut [value](text-value.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément de texte**](text-element.md)
</dt> <dt>

[**TEXT. FontSize**](text-fontsize.md)
</dt> </dl>

 

 





