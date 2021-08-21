---
title: UI_PKEY_StandardColorsCategoryLabel
description: Identifie la propriété StandardColorsCategoryLabel de l’interface utilisateur \_ \_ .
ms.assetid: 59452d4b-acc9-4a5f-a06c-a67b0e676a57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4301fe8874ef4eb3fae0ad931114a7ed305cbc4893ad12c58cf182babe8a16c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437921"
---
# <a name="ui_pkey_standardcolorscategorylabel"></a>IU \_ \_ StandardColorsCategoryLabel

Identifie la propriété StandardColorsCategoryLabel de l’interface utilisateur \_ \_ .

```
propertyDescription
   name = UI_PKEY_StandardColorsCategoryLabel
   shellPKey = UI_PKEY_StandardColorsCategoryLabel
   formatID = 00000404-7363-696e-8441798acf5aebb7
   propID = 404
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Remarques

L’interface utilisateur \_ \_ StandardColorsCategoryLabel est utilisée par une application pour interroger la valeur de l’étiquette associée à la catégorie de **couleurs standard** d’un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

L’interface utilisateur \_ \_ StandardColorsCategoryLabel est valide uniquement pour un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) où `ThemeColors` est spécifié comme valeur de l’attribut **ColorTemplate** (il s’agit du seul modèle qui contient des catégories étiquetées).

La capture d’écran suivante montre un `ThemeColors` [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

![capture d’écran de l’élément dropdowncolorpicker avec l’attribut colortemplate défini sur ThemeColors.](images/markup/colortemplate.themedcolors.1.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du sélecteur de couleurs](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




