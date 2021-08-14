---
title: BOUTON. image
description: L’attribut image spécifie ou récupère l’image par défaut du bouton.
ms.assetid: d0d97f14-2c4d-4769-b45c-c6cde7282bea
keywords:
- bouton. image Lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTON.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85874c79db8f3174b70af68c3ff1e58511c3f00cc7d648389dbca971c7efd96e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342907"
---
# <a name="buttonimage"></a>BOUTON. image

L’attribut **image** spécifie ou récupère l’image par défaut du **bouton**.

``` syntax
        elementID.image
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant le nom du fichier image.

## <a name="remarks"></a>Remarques

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

 

 





