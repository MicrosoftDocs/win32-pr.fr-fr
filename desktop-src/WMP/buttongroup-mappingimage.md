---
title: BUTTONGROUP. mappingImage
description: L’attribut mappingImage spécifie ou récupère le nom de l’image représentant le mappage de bouton du BUTTONGROUP.
ms.assetid: bfea52d1-0e7f-4f77-a212-d34e356a4d85
keywords:
- BUTTONGROUP. mappingImage Lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTONGROUP.mappingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c26a920042aae4ba144f194845f350030f5675c1b9cc3fcfed552346904add1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119896"
---
# <a name="buttongroupmappingimage"></a>BUTTONGROUP. mappingImage

L’attribut **mappingImage** spécifie ou récupère le nom de l’image représentant le mappage de bouton du **BUTTONGROUP**.

``` syntax
        elementID.mappingImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.

## <a name="remarks"></a>Remarques

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

 

 





