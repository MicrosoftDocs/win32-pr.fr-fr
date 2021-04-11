---
title: RadioButton, contrôle
description: Définit un contrôle de case d’option.
ms.assetid: c427080f-0408-42b4-8888-7333f3eb985d
keywords:
- Menus de contrôle RadioButton et autres ressources
topic_type:
- apiref
api_name:
- RADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67dd559c2d61ca8b2735d393170c177a65735b4b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031239"
---
# <a name="radiobutton-control"></a>RadioButton, contrôle

Définit un contrôle de case d’option. Le contrôle est un petit cercle sur lequel le texte indiqué s’affiche en regard de celui-ci, généralement à sa droite. Le contrôle met en surbrillance le cercle et envoie un message à sa fenêtre parente lorsque l’utilisateur sélectionne le bouton. Le contrôle supprime la mise en surbrillance et envoie un message lorsque le bouton est sélectionné ensuite.

``` syntax
RADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*style*
</dt> <dd>

Styles de la case d’option, qui peuvent être une combinaison de styles de classe de bouton et les styles suivants : **WS \_ TABSTOP**, **WS \_ Disabled** et **WS \_ Group**.

Si vous ne spécifiez pas de style, le style par défaut est `BS_RADIOBUTTON | WS_TABSTOP` .

</dd> </dl>

Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation de l’instruction **RadioButton** :

``` syntax
RADIOBUTTON "Italic", 100, 10, 10, 40, 10
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[Cases d’option](https://www.bing.com/search?q=Radio+Buttons)
</dt> </dl>

 

 