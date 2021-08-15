---
title: UI_PKEY_RecentColorsCategoryLabel
description: Identifie la propriété RecentColorsCategoryLabel de l’interface utilisateur \_ \_ .
ms.assetid: e9336b98-59ae-4118-8535-009fc0fda4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f3a7a513afb50f01ee3a03c3a3240a2eae7a6ed7b6b8228c4a49e7343e052e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118031472"
---
# <a name="ui_pkey_recentcolorscategorylabel"></a>IU \_ \_ RecentColorsCategoryLabel

Identifie la propriété RecentColorsCategoryLabel de l’interface utilisateur \_ \_ .

```
propertyDescription
   name = UI_PKEY_RecentColorsCategoryLabel
   shellPKey = UI_PKEY_RecentColorsCategoryLabel
   formatID = 00000405-7363-696e-8441798acf5aebb7
   propID = 405
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Remarques

L’interface utilisateur \_ \_ RecentColorsCategoryLabel est utilisée par une application pour interroger la valeur de l’étiquette associée à la catégorie de **couleurs récentes** d’un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

L’interface utilisateur \_ \_ RecentColorsCategoryLabel est valide uniquement pour un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) où `ThemeColors` est spécifié comme valeur de l’attribut **ColorTemplate** (il s’agit du seul modèle qui contient des catégories étiquetées).

La capture d’écran suivante montre un `ThemeColors` [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

![capture d’écran de l’élément dropdowncolorpicker avec l’attribut colortemplate défini sur ThemeColors.](images/markup/colortemplate.themedcolors.recentcolors.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du sélecteur de couleurs](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




