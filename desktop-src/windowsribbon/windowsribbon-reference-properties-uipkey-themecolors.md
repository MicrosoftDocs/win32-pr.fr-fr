---
title: UI_PKEY_ThemeColors
description: Identifie la propriété ThemeColors de l’interface utilisateur \_ \_ .
ms.assetid: d539cbaa-45dc-4f9e-830e-e81fb289b4ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5991ce5058de5a6f49ca8929de02e19657a610
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404720"
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

## <a name="remarks"></a>Notes

L’interface utilisateur \_ \_ ThemeColors est utilisée par une application pour interroger les valeurs des échantillons de couleur d’un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

Chaque valeur [COLORREF](../gdi/colorref.md) correspond à un échantillon de couleur dans un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) où `ThemeColors` est spécifié comme valeur de l’attribut **ColorTemplate** .

La valeur de la propriété est un tableau de valeurs [COLORREF](../gdi/colorref.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du sélecteur de couleurs](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 