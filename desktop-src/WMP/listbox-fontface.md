---
title: LISTBOX. fontFace
description: L’attribut fontFace spécifie ou récupère la police du contrôle de zone de liste.
ms.assetid: 15e3180a-6e1e-4654-a0bb-164d66a86a26
keywords:
- LISTBOX. fontFace Lecteur Windows Media
topic_type:
- apiref
api_name:
- LISTBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54cf9eb2f1377a92e83d3bc27f8c9491a50369a317af19d16eb2bde765f70958
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054697"
---
# <a name="listboxfontface"></a>LISTBOX. fontFace

L’attribut **fontFace** spécifie ou récupère la police du contrôle de zone de liste.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.

## <a name="remarks"></a>Remarques

Cet attribut peut être le nom de toute police valide disponible dans Windows. Lecteur Windows Media ne prend pas en charge l’installation de polices, vous devez choisir une police sur le système souhaité.

si le **fontFace** spécifié n’est pas disponible sur le système de l’utilisateur, le contrôle de zone de liste est défini par défaut sur la police système Windows. La valeur par défaut pour les systèmes en langue anglaise est « Tahoma ». Pour les systèmes internationaux, la valeur par défaut est chargée à partir d’un fichier de ressources.

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

 

 





