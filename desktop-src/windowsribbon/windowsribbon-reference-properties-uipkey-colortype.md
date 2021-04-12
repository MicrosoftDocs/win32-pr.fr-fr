---
title: UI_PKEY_ColorType
description: Identifie la propriété de la propriété de la propriété de l’interface utilisateur \_ \_ .
ms.assetid: 7eaa9d8b-0c21-487c-9093-79ddffcae131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313d2a657d889a7c582d86d8f8c9e4ebd2cfd01e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315701"
---
# <a name="ui_pkey_colortype"></a>Interface utilisateur de l’IU \_ \_ ColorType

Identifie la propriété de la propriété de la propriété de l’interface utilisateur \_ \_ .

```
propertyDescription
   name = UI_PKEY_ColorType
   shellPKey = UI_PKEY_ColorType
   formatID = 00000401-7363-696e-8441798acf5aebb7
   propID = 401
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>Notes

L’interface utilisateur de l’IU \_ \_ ColorType est utilisée par une application pour interroger le paramètre de couleur du contrôle [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) .

La valeur de la propriété provient de l’énumération [**\_ SWATCHCOLORTYPE de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .



|                                |                                                                                                                                                                                 |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nocolor SWATCHCOLORTYPE de l’interface utilisateur \_ \_   | L’application doit traiter le paramètre de couleur comme étant transparent. Généralement utilisé conjointement avec le paramètre de couleur **sans** couleur.                                                   |
| \_SWATCHCOLORTYPE \_ automatique de l’interface utilisateur | L’application doit interroger [GetSysColor (couleur \_ WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor). Généralement utilisé conjointement avec le paramètre de couleur **automatique** . |
| interface utilisateur \_ SWATCHCOLORTYPE \_ RGB       | L’application doit interroger la [ \_ \_ couleur](windowsribbon-reference-properties-uipkey-color.md) de la couleur de l’interface utilisateur pour le paramètre de couleur.                                                          |



 

L’interface utilisateur de l’IU \_ \_ ColorType est transmise à la méthode de rappel [**IUICommandHandler :: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) lorsqu’un échantillon de couleur est sélectionné dans un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du sélecteur de couleurs](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 