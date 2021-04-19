---
title: BOUTON. image
description: L’attribut image spécifie ou récupère l’image par défaut du bouton.
ms.assetid: d0d97f14-2c4d-4769-b45c-c6cde7282bea
keywords:
- BUTTON. image lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTON.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d27363383d72110ebe7b3e94187013ab701a6a3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533191"
---
# <a name="buttonimage"></a>BOUTON. image

L’attribut **image** spécifie ou récupère l’image par défaut du **bouton**.

``` syntax
        elementID.image
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant le nom du fichier image.

## <a name="remarks"></a>Notes

Les formats d’image pris en charge sont BMP, JPG, PNG et GIF (y compris les images GIF animées).

Si l’image du **bouton** est plus grande que la région définie par les attributs **Width** et **Height** , l’image est rognée.

Si l’image n’est pas spécifiée, mais que la **hauteur** et la **largeur** sont, l’image située directement derrière ce contrôle s’affiche. Cela peut faciliter le dessin de l’image sur la **vue** elle-même, ce qui réduit le nombre de fichiers image distincts nécessaires.

Si l’image ne peut pas être récupérée, une image par défaut (l’image rouge-x) s’affiche.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BUTTON, élément**](button-element.md)
</dt> </dl>

 

 





