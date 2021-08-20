---
title: UI_PKEY_ThemeColorsCategoryLabel
description: Identifie la propriété ThemeColorsCategoryLabel de l’interface utilisateur \_ \_ .
ms.assetid: 704f5c3f-f222-4d98-8a1b-e18a2e094a41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57a622d1958f52713ff8a869524f53e0e4f7f70da723ccada8f83daef69d29eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028557"
---
# <a name="ui_pkey_themecolorscategorylabel"></a>IU \_ \_ ThemeColorsCategoryLabel

Identifie la propriété ThemeColorsCategoryLabel de l’interface utilisateur \_ \_ .

```
propertyDescription
   name = UI_PKEY_ThemeColorsCategoryLabel
   shellPKey = UI_PKEY_ThemeColorsCategoryLabel
   formatID = 00000403-7363-696e-8441798acf5aebb7
   propID = 403
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Remarques

L’interface utilisateur \_ \_ ThemeColorsCategoryLabel est utilisée par une application pour interroger la valeur de l’étiquette associée à la catégorie de **couleurs de thème** d’un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

L’interface utilisateur \_ \_ ThemeColorsCategoryLabel est valide uniquement pour un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) où `ThemeColors` est spécifié comme valeur de l’attribut **ColorTemplate** (il s’agit du seul modèle qui contient des catégories étiquetées).

La capture d’écran suivante montre un `ThemeColors` [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

![capture d’écran de l’élément dropdowncolorpicker avec l’attribut colortemplate défini sur ThemeColors.](images/markup/colortemplate.themedcolors.1.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du sélecteur de couleurs](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




