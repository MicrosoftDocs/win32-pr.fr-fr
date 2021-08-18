---
title: TEXT. fontFace
description: L’attribut fontFace spécifie ou récupère le caractère du contrôle de texte.
ms.assetid: 3b39e245-139a-4361-b678-0f9e962996b7
keywords:
- TEXT. fontFace Lecteur Windows Media
topic_type:
- apiref
api_name:
- TEXT.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3b1044d01ac3ca6a8cc4f1212232bfcc630eb73831f90eb7fd5f423f5dc38d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118355"
---
# <a name="textfontface"></a>TEXT. fontFace

L’attribut **fontFace** spécifie ou récupère le caractère du contrôle de texte.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.

## <a name="remarks"></a>Remarques

Cet attribut peut être le nom de toute police valide disponible sur Windows. Lecteur Windows Media ne prend pas en charge l’installation de polices, vous devez choisir une police sur le système souhaité.

si le **fontFace** spécifié n’est pas disponible sur le système de l’utilisateur, le contrôle de texte est défini par défaut sur la police système Windows.

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

 

 





