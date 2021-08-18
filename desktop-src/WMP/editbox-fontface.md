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
ms.openlocfilehash: c3994c9cef1f645dc9c1129876b9144471caf9f608f5911641b180deae437194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996859"
---
# <a name="editboxfontface"></a>EDITBOX. fontFace

L’attribut **fontFace** spécifie ou récupère la police du texte dans le contrôle zone d’édition.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.

## <a name="remarks"></a>Remarques

Cet attribut peut être le nom de toute police valide disponible dans Windows. Lecteur Windows Media ne prend pas en charge l’installation de polices, vous devez choisir une police sur le système souhaité.

si le **fontFace** spécifié n’est pas disponible sur le système de l’utilisateur, le contrôle de zone d’édition est défini par défaut sur la police système Windows. La valeur par défaut pour les systèmes en langue anglaise est « Tahoma ». Pour les systèmes internationaux, la valeur par défaut est chargée à partir d’un fichier de ressources.

## <a name="requirements"></a>Configuration requise



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

 

 





