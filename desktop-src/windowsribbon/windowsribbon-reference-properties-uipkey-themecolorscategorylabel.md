---
title: UI_PKEY_ThemeColorsCategoryLabel
description: Identifie la propriété ThemeColorsCategoryLabel de l’interface utilisateur \_ \_ .
ms.assetid: 704f5c3f-f222-4d98-8a1b-e18a2e094a41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6ecd1bf3a3150a8ed1de30b299ca785ad271f69
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309621"
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

## <a name="remarks"></a>Notes

L’interface utilisateur \_ \_ ThemeColorsCategoryLabel est utilisée par une application pour interroger la valeur de l’étiquette associée à la catégorie de **couleurs de thème** d’un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

L’interface utilisateur \_ \_ ThemeColorsCategoryLabel est valide uniquement pour un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) où `ThemeColors` est spécifié comme valeur de l’attribut **ColorTemplate** (il s’agit du seul modèle qui contient des catégories étiquetées).

La capture d’écran suivante montre un `ThemeColors`  [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

![capture d’écran de l’élément dropdowncolorpicker avec l’attribut colortemplate défini sur ThemeColors.](images/markup/colortemplate.themedcolors.1.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du sélecteur de couleurs](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




