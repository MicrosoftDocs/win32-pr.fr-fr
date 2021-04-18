---
title: AmbientAttributes.clippingImage
description: L’attribut clippingImage spécifie ou récupère la zone dans laquelle détourer le contrôle.
ms.assetid: e4b51d31-f9c7-4398-983d-95867a2cab45
keywords:
- Lecteur Windows Media AmbientAttributes. clippingImage
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e05e05ca9c7c3efdf842ffd4297da6f9fee035d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533312"
---
# <a name="ambientattributesclippingimage"></a>AmbientAttributes.clippingImage

L’attribut **clippingImage** spécifie ou récupère la zone dans laquelle détourer le contrôle.

``` syntax
        elementID.clippingImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture indiquant le nom du fichier image. Il n'a aucune valeur par défaut.

## <a name="remarks"></a>Notes

L’attribut **clippingImage** prend en charge les fichiers PNG, jpg, BMP et GIF (à l’exclusion des fichiers GIF animés). Étant donné que les JPGs sont perdus et, par conséquent, soumis à une modification de couleur inattendue, ils ne sont pas recommandés pour les images de découpage.

Cet attribut est utile lorsque vous souhaitez afficher uniquement une partie de l’image de contrôle, et non l’intégralité de la zone rectangulaire. L’attribut **clippingColor** indique les régions de l’image de découpage qui correspondent à des portions transparentes et non intercliquables du contrôle. Le contrôle peut donc être de n’importe quelle forme. Pour de meilleurs résultats, l’image de découpage doit être de la même taille que l’image de contrôle.

L’attribut **clippingImage** n’est pas pris en charge par les éléments **playlist**, **View** et **subview** . Une image de découpage ne fonctionne pas avec l’élément **vidéo** si la *vidéo* est. **sans fenêtre** est défini sur false, ni avec l’élément **Effects** si *Effects*. **Windowed** a la valeur true.

Étant donné que l’utilisation d’images de découpage impose une baisse des performances, elles ne doivent pas être utilisées lorsque l’efficacité est un problème.

## <a name="examples"></a>Exemples

Consultez l’attribut [BUTTONELEMENT. mappingColor](buttonelement-mappingcolor.md) pour obtenir un exemple illustrant l’utilisation de cet attribut.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attributs ambiants**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.clippingColor**](ambientattributes-clippingcolor.md)
</dt> </dl>

 

 





