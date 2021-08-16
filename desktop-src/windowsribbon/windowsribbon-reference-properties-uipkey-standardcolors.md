---
title: UI_PKEY_StandardColors
description: Identifie la propriété StandardColors de l’interface utilisateur \_ \_ .
ms.assetid: fbdce7ba-4417-4f7f-928b-fba6af6eb396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2dd46462e9a123b0a8c64c3fd06fdfbc6ccbe3aa35274505dc4722dd2a40e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850070"
---
# <a name="ui_pkey_standardcolors"></a>IU \_ \_ StandardColors

Identifie la propriété StandardColors de l’interface utilisateur \_ \_ .

```
propertyDescription
   name = UI_PKEY_StandardColors
   shellPKey = UI_PKEY_StandardColors
   formatID = 00000410-7363-696e-8441798acf5aebb7
   propID = 410
   typeInfo
      type = VT_VECTOR | VT_UI4
```

## <a name="remarks"></a>Remarques

L’interface utilisateur \_ \_ StandardColors est utilisée par une application pour interroger les valeurs des échantillons de couleur d’un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

Chaque valeur [COLORREF](../gdi/colorref.md) correspond à un échantillon de couleur dans un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) , quelle que soit la valeur spécifiée pour l’attribut **ColorTemplate** .

La valeur de la propriété est un tableau de valeurs [COLORREF](../gdi/colorref.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du sélecteur de couleurs](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 