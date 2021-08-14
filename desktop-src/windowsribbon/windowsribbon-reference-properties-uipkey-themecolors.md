---
title: UI_PKEY_ThemeColors
description: Identifie la propriété ThemeColors de l’interface utilisateur \_ \_ .
ms.assetid: d539cbaa-45dc-4f9e-830e-e81fb289b4ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab5c4582561e3c86ba19b2821cf600d0a1da614cfc9fc7144b935665c8af7f14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437794"
---
# <a name="ui_pkey_themecolors"></a>IU \_ \_ ThemeColors

Identifie la propriété ThemeColors de l’interface utilisateur \_ \_ .

```
propertyDescription
   name = UI_PKEY_ThemeColors
   shellPKey = UI_PKEY_ThemeColors
   formatID = 00000409-7363-696e-8441798acf5aebb7
   propID = 409
   typeInfo
      type = VT_VECTOR | VT_UI4
```

## <a name="remarks"></a>Remarques

L’interface utilisateur \_ \_ ThemeColors est utilisée par une application pour interroger les valeurs des échantillons de couleur d’un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

Chaque valeur [COLORREF](../gdi/colorref.md) correspond à un échantillon de couleur dans un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) où `ThemeColors` est spécifié comme valeur de l’attribut **ColorTemplate** .

La valeur de la propriété est un tableau de valeurs [COLORREF](../gdi/colorref.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du sélecteur de couleurs](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 