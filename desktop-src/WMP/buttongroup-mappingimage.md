---
title: BUTTONGROUP. mappingImage
description: L’attribut mappingImage spécifie ou récupère le nom de l’image représentant le mappage de bouton du BUTTONGROUP.
ms.assetid: bfea52d1-0e7f-4f77-a212-d34e356a4d85
keywords:
- Lecteur Windows Media BUTTONGROUP. mappingImage
topic_type:
- apiref
api_name:
- BUTTONGROUP.mappingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26e4afc44a00d5ce9b15ee01d4a0dc1aff52c555
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522818"
---
# <a name="buttongroupmappingimage"></a>BUTTONGROUP. mappingImage

L’attribut **mappingImage** spécifie ou récupère le nom de l’image représentant le mappage de bouton du **BUTTONGROUP**.

``` syntax
        elementID.mappingImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.

## <a name="remarks"></a>Notes

Il s’agit d’un attribut obligatoire qui doit être spécifié.

Les dimensions de l’image de mappage doivent être identiques à celles de l' **image** principale. Il s’agit d’une carte des zones cliquables de l’image principale. Construisez la carte en remplissant chaque zone interactive avec une couleur différente.

Quand vous définissez chaque **BUTTONELEMENT**, vous spécifiez sa couleur à partir de la carte à l’aide de l’attribut **mappingColor** . Par exemple, si vous avez un graphique de bouton en forme d’arrêt dans l’image principale, vous pouvez créer une carte avec la zone du signe de couleur rouge. L’attribut **BUTTONELEMENT** doit ensuite être spécifié en rouge pour que l’image d’arrêt soit cliquable.

Les formats d’image pris en charge sont BMP, JPG, PNG et GIF (à l’exclusion des GIF animés). Étant donné que les JPGs sont perdus et, par conséquent, soumis à une modification de couleur inattendue, ils ne sont pas recommandés pour le mappage d’images.

## <a name="examples"></a>Exemples

L’illustration suivante est un exemple de **mappingImage** et de l’image visible à laquelle elle correspond. Ces images font partie de l’apparence dans le petit dossier inclus dans le kit de développement logiciel (SDK).

![exemple d’image de mappage](images/absam01m.png)![exemple d’image d’arrière-plan](images/absam01f.png)

Consultez *BUTTONELEMENT*. attribut [mappingColor](buttonelement-mappingcolor.md) pour un exemple de code illustrant l’utilisation de cet attribut.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BUTTONELEMENT. mappingColor**](buttonelement-mappingcolor.md)
</dt> <dt>

[**Élément BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP. image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP. transparencyColor**](buttongroup-transparencycolor.md)
</dt> </dl>

 

 





